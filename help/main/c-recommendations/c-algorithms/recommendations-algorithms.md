---
keywords: aanbevelingen, algoritmen;modeltraining;model serving;content delivery;item-based;user-based;popularity-based;cart-based;custom criteria
description: Meer informatie over de algoritmen die worden gebruikt in [!DNL Target Recommendations], met inbegrip van modelopleiding en modeldienstverlening.
title: Waar kan ik leren over de wetenschap achter de Recommendations-algoritmen van Target?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="See what's included in Target Premium."
feature: Recommendations
mini-toc-levels: 2
exl-id: c156952b-8eda-491d-a68e-d3d09846f640
source-git-commit: 2a25fdb42ce4470f9126b7e0e7f6fd9e60c350e5
workflow-type: tm+mt
source-wordcount: '2741'
ht-degree: 0%

---

# De wetenschap achter de aanbevelingen van Target algoritmen

Een diepgaande beschrijving van de gebruikte algoritmen [!DNL Adobe Target Recommendations], met inbegrip van de logische en wiskundige details van modeltraining en het proces van modeldienstverlening.

Modeltraining is het proces waarbij aanbevelingen worden gegenereerd door de [!DNL Adobe Target] leeralgoritmen. Model serving is hoe [!DNL Target] geeft aanbevelingen aan uw sitebezoekers (ook wel levering van inhoud genoemd).

[!DNL Target] omvat de volgende brede types van algoritmen in [!DNL Recommendations]:

* **Algoritmen op basis van items**: Neem algoritmen op die de logica &#39;Personen die dit item hebben bekeken/gekocht, hebben deze items ook bekeken/gekocht.&#39; volgen. Deze algoritmen worden gegroepeerd onder de paraplu punt-punt samenwerkende het filtreren, evenals [!UICONTROL Items with Similar Attributes] algoritmen.

* **Op gebruiker gebaseerde algoritmen**: Inclusief de [!UICONTROL Recently Viewed] en [!UICONTROL Recommended for You] algoritmen.

* **Op populariteit gebaseerde algoritmen**: Neem algoritmes op die de bovenste weergegeven of bovenste gekochte items op de website retourneren, of die u bovenaan hebt weergegeven of die u bovenaan hebt aangeschaft op categorie- of itemkenmerk.

* **Op kaarten gebaseerde algoritmen**: Neem aanbevelingen op basis van meerdere objecten op met de logica &quot;Personen die deze objecten hebben bekeken/gekocht, hebben deze objecten ook bekeken/gekocht.&quot;

* **Aangepaste criteria**: Aanbevelingen opnemen op basis van aangepaste bestanden die zijn geüpload naar [!DNL Target].

>[!NOTE]
>
>Zie voor meer algemene informatie over elk type algoritme en de afzonderlijke algoritmen [De aanbeveling baseren op een aanbevelingen](/help/main/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md).

Veel van de bovenstaande algoritmen zijn gebaseerd op de aanwezigheid van een of meerdere toetsen. Deze sleutels worden gebruikt om gelijkaardige punten bij de tijd van de inhoudslevering terug te winnen (wanneer aanbevelingen worden gedaan). Door de klant opgegeven sleutels kunnen het huidige object bevatten dat iemand bekijkt, het laatst bekeken of aangekochte object, het meest bekeken object, de huidige categorie of de favoriete categorie voor die bezoeker. Andere algoritmen, zoals op kar-gebaseerde of op gebruiker-gebaseerde aanbevelingen, gebruiken impliciete sleutels (die niet door de klant kunnen worden gevormd). Zie voor meer informatie *Aanbevolen toetsen*, in [De aanbeveling baseren op een aanbevelingen](/help/main/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md#keys). Deze toetsen zijn echter alleen relevant op het moment dat het model wordt gebruikt (levering van inhoud). Deze toetsen zijn niet van invloed op de logica van de ‘offline’ of de trainingstijd van het model.

De volgende secties groeperen algoritmen op een iets andere manier dan de hierboven beschreven algoritmenypes. De volgende groepering is gebaseerd op de gelijkenis van model opleidingslogica.

## Gezamenlijk filteren van item-item

Algoritmen zijn:

* [!UICONTROL People Who Viewed This, Viewed That]
* [!UICONTROL People Who Viewed This, Bought That]
* [!UICONTROL People Who Bought This, Bought That]

De punt-punt samenwerkings het filtreren aanbevelingen algoritmen zijn gebaseerd op het idee dat u de gedragspatronen van vele gebruikers (vandaar samenwerkingsverband) zou moeten gebruiken om nuttige aanbevelingen voor een bepaald punt (bijvoorbeeld, filter de catalogus van mogelijke punten om aan te bevelen) te verstrekken. Hoewel er veel verschillende algoritmen zijn die onder de algemene paraplu van vallen [gezamenlijk filteren](https://en.wikipedia.org/wiki/Collaborative_filtering)Deze algoritmen gebruiken voor iedereen gedragsgegevensbronnen als input. In [!DNL Target Recommendations]Deze invoer is de unieke weergave en aankoop van objecten door gebruikers.

Voor het algoritme &quot;Personen die dit item hebben bekeken/aangeschaft, hebben deze items ook bekeken/aangeschaft&quot;, is het doel een overeenkomst (A,B) tussen alle paren items te berekenen. Voor een bepaald punt A worden de hoogste aanbevelingen vervolgens geordend op basis van hun gelijkenis s(A,B).

Een voorbeeld van zo&#39;n gelijkenis is de co-existentie tussen items: een eenvoudige telling van het aantal gebruikers dat beide objecten heeft gekocht. Hoewel intuïtief, is zo&#39;n metrische waarde naïef in die zin dat het in de richting gaat van het aanbevelen van populaire objecten. Als de meeste mensen bijvoorbeeld bij een groothandelaar brood kopen, zal brood een grote co-existentie hebben met alle producten, maar het is niet noodzakelijk een goede aanbeveling. [!DNL Target] in plaats daarvan gebruikt een verfijndere metrische gelijkenis die als logboekwaarschijnlijkheidsverhouding (LLR) wordt bekend. Deze hoeveelheid is groot wanneer de kans dat twee items, A en B, samen voorkomen, zeer verschillend is van de waarschijnlijkheid dat ze zich niet samen voordoen. Neem voor de concretisering een geval van [!UICONTROL People Who Viewed This, Bought That] algoritme. De LLR-gelijkenis is groot wanneer de kans dat B werd aangekocht groot is *niet* of iemand A heeft bekeken.

Als

![Formule voor het weergegeven/gekochte algoritme](assets/formula.png)

dan wordt item B niet aanbevolen bij item A. Deze berekening van de waarschijnlijkheidsverhouding van de logaritme wordt uitvoerig toegelicht. [in deze PDF](/help/main/c-recommendations/c-algorithms/assets/log-likelihood-ratios-recommendation-algorithms.pdf).

De logische stroom van de daadwerkelijke algoritmeimplementatie wordt getoond in het volgende schematische diagram:

![Schematisch diagram van een bekeken/gekocht algoritme](assets/diagram1.png)

De details van deze stappen zijn als volgt:

* **Invoergegevens**: Gedragsgegevens, in de vorm van weergaven en aankopen van bezoekers die bij u worden verzameld [Doel implementeren](https://experienceleague.corp.adobe.com/docs/target-dev/developer/recommendations.html){target=_blank} or from [Adobe Analytics](/help/main/c-recommendations/c-algorithms/use-adobe-analytics-with-recommendations.md){target=_blank}.

* **Modeltraining**:

   * **Gegevensreiniging en -bemonstering**: Voor algoritmen met een N-day terugblik, worden de gedragsgegevens eerst gefiltreerd om slechts die N dagen van gegevens te omvatten. De regels van de inzameling en globale uitsluitingen worden dan toegepast om het even welke punten te verwijderen die niet zouden moeten worden geadviseerd. Tot slot hebben bezoekers die met meer dan 1.000 punten interactie hadden hun gebruiksgegevens bemonsterd aan slechts 1.000 punten.
   * **Berekening van gelijkenis van item**: Dit is de belangrijkste computerstap: het berekenen van de de verhoudingsgelijkenis van de logboekwaarschijnlijkheid tussen alle kandidaat puntparen, en het rangschikken van paren punten door deze gelijkenisscore.
   * **Offline filteren**: Ten slotte worden eventuele verdere toepasselijke dynamische filters toegepast (bijvoorbeeld uitsluiting van dynamische categorieën). Na deze stap worden vooraf berekende aanbevelingen globaal in cache geplaatst om beschikbaar te zijn voor het dienen.

* **Modelweergave**: Recommendations-inhoud wordt geleverd door [!DNL Target]s [wereldwijd &quot;Edge&quot;-netwerk](/help/main/c-intro/how-target-works.md#concept_0AE2ED8E9DE64288A8B30FCBF1040934). Wanneer mbox-aanvragen worden ingediend op [!DNL Target] en wordt bepaald dat de inhoud van de aanbevelingen aan de pagina moet worden verstrekt, het verzoek om de passende [itemsleutel](/help/main/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md#keys) voor de aanbevelingen wordt het algoritme of ontleed van het verzoek of opgezocht van het gebruikersprofiel, en dan gebruikt om de aanbevelingen terug te winnen die in de vorige stappen worden gegevens verwerkt. Op dit moment worden verdere dynamische filters toegepast, voordat de juiste [ontwerp](/help/main/c-recommendations/c-design-overview/create-design.md) wordt weergegeven.

## Overeenkomende inhoud

Algoritme inbegrepen:

* [!UICONTROL Items with Similar Attributes]

In dit type algoritme worden twee items beschouwd als gerelateerd als de naam en de beschrijving ervan semantisch vergelijkbaar zijn. In tegenstelling tot de meeste aanbevelingen in algoritmen waarin gedragsgegevensbronnen moeten worden gebruikt, gebruiken algoritmen voor gelijkenis met inhoud metagegevens uit productcatalogi om de gelijkenis tussen items af te leiden. [!DNL Target] kan daarom aanbevelingen doen in zogenaamde &quot;koudstart&quot;-scenario&#39;s, waar geen gedragsgegevens zijn verzameld (bijvoorbeeld aan het begin van een [!DNL Target] activiteit).

Hoewel het model dat dienst doet en de tevreden leveringsaspecten van [!DNL Target]De algoritmen voor de gelijkenis van de inhoud zijn identiek aan andere op items gebaseerde algoritmen. De trainingsstappen van het model zijn drastisch verschillend en omvatten een reeks stappen voor de verwerking en voorbewerking van natuurlijke talen, zoals weergegeven in het volgende diagram. De kern van de gelijkheidsberekening is het gebruik van de cosinusgelijkenis van gewijzigde tf-idf vectoren die elk punt in de catalogus vertegenwoordigen.

![Diagram dat de stroom van het proces van de inhoudsgelijkenis toont](assets/diagram2.png)

De details van deze stappen zijn als volgt:

* **Invoergegevens**: Zoals eerder beschreven, is dit algoritme uitsluitend gebaseerd op catalogusgegevens (opgenomen op [!DNL Target] via een [Catalogusfeed, de Entiteiten-API of updates op de pagina](https://experienceleague.corp.adobe.com/docs/target-dev/developer/recommendations.html){target=_blank}.

* **Modeltraining**:

   * **Kenmerken extraheren**: Na de toepassing van reguliere statische filters, catalogusregels en algemene uitsluitingen haalt dit algoritme relevante tekstvelden uit het entiteitsschema. [!DNL Target] gebruikt automatisch de naam, het bericht en de categorievelden van de entiteitattributen en probeert om het even welke koordgebieden uit douane te halen [entiteitskenmerken](/help/main/c-recommendations/c-products/entity-attributes.md). Dit proces wordt gedaan door ervoor te zorgen dat de meerderheid van waarden voor dat gebied niet parseerbaar als aantal, datum, of booleaanse waarde is.
   * **Afbreken en verwijderen van stopwoorden**: Voor nauwkeurigere overeenkomsten op het gebied van tekstgelijkenis is het verstandig om zeer gebruikelijke stopwoorden te verwijderen die de betekenis van een item niet significant wijzigen (bijvoorbeeld &quot;was&quot;, &quot;is&quot;, &quot;en&quot; enzovoort). Op dezelfde manier verwijst stammen naar het proces om woorden met verschillende achtervoegsels aan hun wortelwoord te verminderen, dat een identieke betekenis heeft (bijvoorbeeld &quot;verbinden,&quot;verbinden,&quot;en &quot;verbinding&quot;allen hebben het zelfde wortelwoord: &quot;connect&quot;). [!DNL Target] gebruikt de Sneeuwbalstemmer. [!DNL Target] voert eerst automatische taaldetectie uit en kan woordverwijdering voor maximaal 50 talen en stammen voor 18 talen wel stoppen.
   * **n-gram maken**: Na de vorige stappen wordt elk woord beschouwd als een token. Het proces waarbij opeenvolgende reeksen tokens worden gecombineerd tot één token, wordt n-gram maken genoemd. [!DNL Target]De algoritmen van de fabrikant overwegen maximaal 2 gram.
   * **tf-idf, berekening**: De volgende stap bestaat uit het maken van tf-idf-vectoren om het relatieve belang van tokens in de itembeschrijving te weerspiegelen. Voor elke token/term t in een item i, in een catalogus D met |D| De term frequentie TF(t, i) wordt als eerste berekend (het aantal keren dat de term voorkomt in item i) en de documentfrequentie DF(t, D). In wezen het aantal items waar het token bestaat. De tf-idf-maatregel is dan

      ![Formule met de tf-idf-maat](assets/formula2.png)

      [!DNL Target] gebruikt Apache Spark&#39;s *tf-idf* de implementatie van de featurisatie, die onder de kap elk teken aan een ruimte van 218 tokens hakt. In deze stap, wordt de klant-gespecificeerde attributenverhoging en het begraven ook toegepast door de term frequenties in elke vector aan te passen die op montages wordt gebaseerd die in [criteria](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md#similarity).

   * **Berekening van gelijkenis van item**: De uiteindelijke berekening van de gelijkenis van het item wordt uitgevoerd op basis van een cosingelijkenis. Voor twee items: *A* en *B* Met de vectoren tA en tB wordt de cosinegelijkenis gedefinieerd als:

      ![Formule die de vergelijkingsberekening van het item weergeeft](assets/formula3.png)

      Om significante complexheid in gegevensverwerkingsgelijkenissen tussen alle N x N punten te vermijden, *tf-idf* de vector wordt afgekapt om slechts zijn grootste 500 ingangen te bevatten, en dan cosinegelijkenissen tussen punten te berekenen gebruikend deze afgekapte vectorvertegenwoordiging. Deze aanpak blijkt robuuster te zijn voor dunne berekeningen van de vectorgelijkenis, in vergelijking met andere benaderende dichtstbijzijnde (ANN) technieken, zoals localiteitsgevoelige hashing.

   * **Modelweergave**: Dit proces is identiek aan punt-punt samenwerkings het filtreren technieken die in de vorige sectie worden beschreven.

## Aanbevelingen voor meerdere sleutels

Algoritmen zijn:

* Aanbevelingen voor winkelwagentjes
* [!UICONTROL Recommended For You]

De meest recente toevoegingen aan de [!DNL Target] reeks aanbevelingen algoritmen zijn [!UICONTROL Recommended For You] en een reeks aanbevelingen op basis van kunst algoritmen. Beide types van algoritmen gebruiken samenwerkings het filtreren technieken om individuele op punt-gebaseerde aanbevelingen te vormen. Dan, bij tijd, veelvoudige punten in de het doorbladeren van de gebruiker geschiedenis (voor [!UICONTROL Recommended For You]) of de huidige winkelwagentje van de gebruiker (voor aanbevelingen op basis van winkelwagentje) wordt gebruikt om deze op items gebaseerde aanbevelingen op te halen, die vervolgens worden samengevoegd tot de definitieve lijst met aanbevelingen. Merk op dat vele vloeren van gepersonaliseerde aanbevelingen algoritmen bestaan. De keuze van een algoritme met meerdere sleutels houdt in dat de aanbevelingen direct beschikbaar zijn nadat een bezoeker een browsergeschiedenis heeft en dat aanbevelingen kunnen worden bijgewerkt om te reageren op het meest recente gedrag van de bezoeker.

Deze algoritmen bouwen op de fundamentele samenwerkings het filtreren technieken voort die in op punt-gebaseerde aanbevelingen sectie worden beschreven, maar omvatten ook hyperparameterhet stemmen om optimale gelijkenis tussen punten te bepalen. Het algoritme voert een chronologische scheiding van gedragsgegevens voor elke gebruiker uit, en treinraadmodellen op de vroegere gegevens terwijl het proberen om de punten te voorspellen die een gebruiker of aankopen later bekijkt. De maatstaf van de gelijkenis die de optimale [Gemiddelde precisie](https://en.wikipedia.org/wiki/Evaluation_measures_(information_retrieval).

De logica van modelopleiding en het scoren stappen worden getoond in het volgende diagram:

![Diagram met de logica van modeltraining en -scoring](assets/diagram3.png)

De details van deze stappen zijn als volgt:

* **Invoergegevens**: Dit is identiek aan punt-punt samenwerkings het filtreren (CF) methodes. [!UICONTROL Both Recommended For You] en algoritmen op basis van winkelwagentjes gedragsgegevens gebruiken, in de vorm van weergaven en aankopen van gebruikers die worden verzameld wanneer u [Doel implementeren](https://experienceleague.corp.adobe.com/docs/target-dev/developer/recommendations.html){target=_blank} or from [Adobe Analytics](/help/main/c-recommendations/c-algorithms/use-adobe-analytics-with-recommendations.md){target=_blank}.

* **Modeltraining**:

   * **Gegevensreiniging en -bemonstering**: Dit is opnieuw het zelfde als voor samenwerkings het filtreren methodes, waar het raadplegingsvenster wordt toegepast op filtergedragsgegevens aan een aangewezen datumwaaier, die door toepassing van catalogusregels en globale uitsluitingen wordt gevolgd. Bezoekers die met meer dan 1000 objecten hebben gewerkt, hebben slechts hun meest recente 1000 gebruikers in overweging genomen.
   * **Treinproefsplitsing**: Voer een chronologische splitsing uit van het gebruik voor elke gebruiker, waarbij de eerste 80% van het gebruik wordt toegewezen aan trainingsgegevens, waarbij de resterende 20% wordt toegewezen aan de testgegevens.
   * **Modeltraining objectgelijkenis**: De berekening van de gelijkenis van het kernitem verschilt voor [!UICONTROL Recommended For You] en algoritmen op basis van illustraties op de manier waarop kandidaat-itemvectoren worden samengesteld. Voor [!UICONTROL Recommended For You], hebben de itemvectoren dimensie NUsers, waar elke ingang de som impliciete ratings voor die gebruiker van het punt vertegenwoordigt-de aankopen van een punt worden gegeven een gewicht van 2x dat van meningen van het punt. Voor op kunst-Gebaseerde aanbevelingen, hebben de puntvectoren binaire ingangen; als het gedrag binnen de sessie alleen moet worden overwogen, is er een nieuwe vermelding voor elke sessie. Anders is er een item in dit item-vector voor elke bezoeker.

   In de trainingsstap worden verschillende typen vectorgelijkenissen berekend: LR-gelijkenis ([hier besproken](/help/main/c-recommendations/c-algorithms/assets/log-likelihood-ratios-recommendation-algorithms.pdf)), cosinegelijkenis (eerder gedefinieerd) en een genormaliseerde L2-gelijkenis, gedefinieerd als:

   ![Formule voor het berekenen van trainingen](assets/formula4.png)

   * **Evaluatie van het model voor gelijkenis van item**: De modelevaluatie wordt uitgevoerd door de in de vorige stap gegenereerde aanbevelingen te nemen en voorspellingen te doen over de reeks testgegevens. De online het scoren fase wordt nagebootst door chronologisch het puntengebruik van elke gebruiker in de testdataset te bepalen, dan het doen van 100 aanbevelingen voor geordende ondergroepen van punten in een poging om verdere meningen en aankopen te voorspellen. Een metrische informatie van de informatieherwinning, [Gemiddelde precisie](https://en.wikipedia.org/wiki/Evaluation_measures_(information_retrieval) wordt gebruikt om de kwaliteit van deze aanbevelingen te evalueren. Deze maatstaf houdt rekening met de volgorde van aanbevelingen, en geeft de voorkeur aan relevante punten hoger in de lijst van aanbevelingen, die een belangrijk bezit voor rangschikkingssystemen is.
   * **Modelselectie**: Na off-line evaluatie, wordt het model dat de hoogste Gemiddelde Precisie heeft geselecteerd, en alle individuele punt-punt aanbevelingen die voor het worden gegevens verwerkt.
   * **Offline filteren**: De laatste fase van modeltraining is de toepassing van eventuele toepasselijke dynamische filters. Na deze stap worden vooraf berekende aanbevelingen globaal in cache geplaatst om beschikbaar te zijn voor het dienen.


* **Modelweergave**: In tegenstelling tot vorige algoritmen waarin het dienen van aanbevelingen het specificeren van één enkele sleutel voor herwinning impliceert, die door toepassing van bedrijfsregels wordt gevolgd, [!UICONTROL Recommended for You] en op kunst-Gebaseerde algoritmen gebruiken een complexer runtime proces.

   * **Ophalen en samenvoegen van meerdere sleutels**: Voor op kunst-Gebaseerde aanbevelingen, worden tot tien punten die in het karretje worden overgegaan beschouwd als sleutels voor terugwinning en de aanbevelingen van elk zijn gelijk gewogen. Voor [!UICONTROL Recommended for You], tot de laatste vijf unieke bekeken objecten en de laatste vijf unieke gekochte objecten worden beschouwd als sleutels voor het ophalen, waarbij aanbevelingen die voortkomen uit aangekochte objecten tweemaal zo veel gewogen worden als aanbevelingen die voortkomen uit bekeken objecten. Als bij het samenvoegen van aanbevelingen een item in meerdere afzonderlijke lijsten met aanbevelingen wordt weergegeven, worden de gewogen resultaten voor de gelijkenis toegevoegd. De definitieve lijst met aanbevelingen uit deze fase is dan de samengevoegde lijst van opnieuw gewogen aanbevelingen, gerangschikt in aflopende volgorde.
   * **Filteren**: Vervolgens worden filterregels zoals verwijdering van eerder weergegeven en/of aangekochte items en andere dynamische bedrijfsregels toegepast.

Deze processen worden geïllustreerd in de volgende afbeelding, waarbij een bezoeker item A heeft bekeken en item B heeft aangeschaft. De individuele aanbevelingen worden teruggewonnen met de off-line gelijkenisscores die onder elk puntetiket worden getoond. Na terugwinning, worden de aanbevelingen samengevoegd met gewogen gelijkenisscores samengevat. Tot slot in een scenario waarin de klant heeft gespecificeerd dat eerder bekeken en gekochte punten uit moeten worden gefiltreerd, verwijdert de het filtreren stap punten A en B uit de lijst van aanbevelingen.

![Diagram van de verwerking van meertalige algoritmen](assets/diagram4.png)

## Gebaseerd op populariteit

Algoritmen zijn:

* [!UICONTROL Most Viewed Across the Site]
* [!UICONTROL Most Viewed by Category]
* [!UICONTROL Most Viewed by Item Attribute]
* [!UICONTROL Top Sellers Across the Site]
* [!UICONTROL Top Sellers by Category]
* [!UICONTROL Top Sellers by Item Attribute]

[!DNL Target] biedt op populariteit gebaseerde algoritmen voor zowel de meest bekeken items als de meest verkochte items op een website of uitgesplitst naar een itemkenmerk of categorie. Op populariteit gebaseerde algoritmen rangschikken items op basis van het aantal sessies waarin dat item in een bepaald tijdkader is weergegeven of aangeschaft.

Al deze algoritmen combineren geaggregeerde gedragsgegevens waarbij het totale aantal sessies waarin items zijn bekeken en aangeschaft, wordt vastgelegd op zowel de uurresolutie als de dagelijkse resolutie. De individuele algoritmen vinden dan de het meest bekeken of meeste gekochte punten voor de klant gevormd raadplegingsvenster.

Afzonderlijke algoritme-nuances zijn als volgt:

* [!UICONTROL Most Viewed Across the Site] en [!UICONTROL Top Sellers Across the Site] Hiermee worden de items gerangschikt op basis van het totale aantal sessies waarin deze items zijn weergegeven of aangeschaft. De uitvoer bestaat uit één (zonder sleutel) lijst met aanbevolen items.
* De meeste weergaven/topverkopers op rubriek/kenmerk zijn aanbevelingen waarbij items worden geordend op basis van de totale aantallen sessies waarin deze items zijn weergegeven of aangeschaft, maar gegroepeerd op de objectcategorie of het specifieke kenmerk. De output is lijsten van geadviseerde punten, die door waarden van categorieën, of waarden van puntattributen worden gehouden.

## Onlangs bekeken

Het algoritme van de &quot;onlangs bekeken&quot;aanbevelingen staat voor in-zittingspersonalisering van aanbevelingen toe. Voor dit algoritme is geen offline &#39;modeltraining&#39; vereist. In plaats daarvan, [!DNL Target] gebruikt het unieke [Bezoekerprofiel](/help/main/c-target/c-visitor-profile/visitor-profile.md) om een lopende lijst van punten te handhaven die in een bepaalde zitting zijn bekeken en deze punten in aanbevelingen activiteiten kunnen behandelen. Dit staat voor updates in real time aan aanbevelingen en volgende-pagina verpersoonlijking toe.

## Aangepaste criteria

Met aangepaste criteria kunnen klanten [uploadt hun eigen aanbevelingen aan [!DNL Target]](/help/main/c-recommendations/c-algorithms/recommendations-csv.md), die belangrijke flexibiliteit bieden en &#39;uw eigen model&#39; mogelijkheden bieden. De aangepaste criteria vervangen het gedeelte &quot;offline training&quot; van [!UICONTROL Item-Based] aanbevelingen, maar gedraagt zich op gelijkaardige wijze aan op punt-Gebaseerde aanbevelingen algoritmen tijdens de online fase van de inhoudslevering, in die zin dat één enkele sleutel voor terugwinning van aanbevelingen wordt gebruikt en bedrijfsregels/filters dan worden toegepast.
