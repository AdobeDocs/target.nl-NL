---
keywords: partiële gegevens;partiële gegevens;A4T;discrepanties;analyses voor doel;wees;virtueel rapportsuite;fantoom;problemen oplossen;ongestikt;opgepompt;niet gespecificeerd
description: Leer hoe te om de gevolgen van opgeblazen Bezoek en het tellen van de Bezoeker te minimaliseren wanneer het gebruiken van Analytics voor  [!DNL Target]  (A4t). Leer wat "gedeeltelijke gegevens"is en hoe te om het te verminderen.
title: Hoe minimaliseer ik het aantal opgeblazen bezoekers en bezoekers in A4T?
feature: Analytics for Target (A4T)
exl-id: 308711f7-e630-4f6b-8a6d-a1f36ed7902d
source-git-commit: 122484056e73f8f679312a3e776e623d905701d5
workflow-type: tm+mt
source-wordcount: '1321'
ht-degree: 0%

---

# Het aantal opgeblazen bezoeken en bezoekers in A4T minimaliseren

Informatie die u helpt de effecten van opgeblazen bezoeken en bezoekers te minimaliseren wanneer u [!DNL Adobe Analytics] als rapportagebron voor [!DNL Adobe Target] (A4T) gebruikt.

>[!IMPORTANT]
>Op 14 november 2016 heeft Adobe Analytics de manier gewijzigd waarop sommige gegevens voor klanten worden verwerkt met Analytics Reporting for Target (A4T). Door deze wijzigingen worden Adobe Target-gegevens beter afgestemd op het gegevensmodel voor Adobe Analytics. Deze veranderingen werden opgesteld voor alle klanten die A4T gebruiken. Deze wijzigingen hebben specifiek betrekking op een probleem waarbij sommige klanten een opgeblazen aantal bezoekers hebben opgemerkt wanneer Target-activiteiten worden uitgevoerd.
>
>Deze wijziging is niet met terugwerkende kracht. Als uw historische rapporten opgeblazen aantallen tonen, en u zou hen van uw rapporten willen uitsluiten, kunt u een virtueel rapportreeks tot stand brengen, zoals hieronder verklaard.
>
>Verschillende JavaScript-bibliotheken zijn bijgewerkt om het opblaasbare aantal tot een minimum te beperken. Adobe raadt u aan een upgrade uit te voeren naar de volgende (of nieuwere) bibliotheekversies:
>
>* Experience Cloud Visitor ID Service: bezoekerAPI.js versie 2.3.0 of hoger.
>* Adobe Analytics: appMeasurement.js versie 2.1.
>* Adobe Target: at.js versie 0.9.6 of hoger (behalve versie 1.1.0 als u aanbiedingen omleiden met A4T gebruikt).

## Wat is er veranderd? {#section_9CCF45F5D66D48EBA88F3A178B27D986}

Wanneer [!DNL Adobe Analytics] wordt gebruikt om [!DNL Target] activiteiten (A4T genoemd) te meten, verzamelt [!DNL Analytics] extra gegevens die niet beschikbaar zijn wanneer er geen [!DNL Target] activiteit op de pagina is. Met de activiteit [!DNL Target] wordt boven aan de pagina een aanroep geactiveerd, maar [!DNL Analytics] wordt doorgaans onder aan de pagina de aanroepen voor gegevensverzameling geactiveerd. Bij de implementatie van A4T tot op heden, omvat Adobe deze extra gegevens wanneer een [!DNL Target] activiteit actief was. Adobe neemt deze aanvullende gegevens alleen op als de tags [!DNL Target] en [!DNL Analytics] zijn geactiveerd.

## Waarom heeft Adobe deze wijziging doorgevoerd? {#section_92380A4BD69E4B8886692DD27540C92A}

Adobe is trots op gegevensnauwkeurigheid en -kwaliteit. Wanneer de tag [!DNL Target] wordt geactiveerd, maar de tag [!DNL Analytics] dit niet doet, worden in Analytics &quot;gedeeltelijke gegevens&quot; vastgelegd (ook wel &quot;niet-opgeslagen resultaten&quot; genoemd). Deze ongestipte treffers worden niet vastgelegd door [!DNL Analytics] als er geen [!DNL Target] -activiteit is. Hoewel het opnemen van deze deelgegevens in [!DNL Analytics] -rapportage aanvullende informatie biedt, leidt dit ook tot inconsistentie met historische gegevens uit perioden waarin er geen [!DNL Target] -activiteiten werden uitgevoerd. Deze situatie kan problemen veroorzaken voor [!DNL Analytics] gebruikers die trends in de loop der tijd analyseren. Met het oog op de consistentie van gegevens in [!DNL Analytics] sluit Adobe alle gedeeltelijke gegevens uit.

## Wat draagt bij aan gedeeltelijke gegevens? {#section_C9C906BEAA7D44DAB9D3C03932A2FEB8}

Adobe heeft klanten ontmoet met hoge percentages van gedeeltelijke gegevens in [!DNL Analytics]. De hoge percentages van gedeeltelijke gegevens kunnen uit onjuiste implementatie voortvloeien, maar er zijn ook legitieme oorzaken.

De geïdentificeerde oorzaken van gedeeltelijke gegevens zijn onder meer:

* **Verkeerd richten rapportreeks IDs (Implementatie):** de rapportreeks die tijdens activiteitenopstelling wordt gespecificeerd past niet de rapportreeks op de pagina aan waar de test wordt geleverd. De gegevens kunnen niet worden afgestemd op [!DNL Analytics] -servers, zodat het lijkt op gedeeltelijke gegevens.
* **Trage pagina&#39;s:** [!DNL Target] de vraag is bij de bovenkant van de pagina en [!DNL Analytics] de vraag is typisch bij de bodem van de pagina. Als de pagina langzaam wordt geladen, vergroot dit de kans dat een bezoeker de pagina verlaat nadat de aanroep van [!DNL Target] is geactiveerd, maar vóór de aanroep van [!DNL Analytics] . Trage pagina&#39;s kunnen vooral problematisch zijn op mobiele websites, waar de verbindingen vaak trager zijn.
* **fouten van de Pagina:** als er de fouten van JavaScript of andere scenario&#39;s zijn waar elk van de aanrakingspunten niet (de dienst van identiteitskaart van Experience Cloud, Doel, en Analytics) in brand steken, gedeeltelijke gegevensresultaten.
* **richt aanbiedingen in [!DNL Target] activiteit om:** voor omleiding aanbiedingen in activiteiten die A4T gebruiken, moet uw implementatie aan bepaalde minimumvereisten voldoen. Bovendien is er belangrijke informatie die u moet weten. Voor meer informatie, zie [&#x200B; Aanbiedingen opnieuw richten - Veelgestelde vragen A4T &#x200B;](/help/main/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-redirect-offers.md#section_FA9384C2AA9D41EDBCE263FFFD1D9B58).
* **Oude versies van de bibliotheken:** In het afgelopen jaar heeft Adobe verscheidene verbeteringen aangebracht in de bibliotheken van JavaScript ( [!DNL appMeasurement.js], `at.js`, en `visitorAPI.js`) om ervoor te zorgen dat de gegevens zo efficiënt mogelijk worden verzonden. Meer over implementatievereisten leren, zie [&#x200B; alvorens u &#x200B;](/help/main/c-integrating-target-with-mac/a4t/before-implement.md#concept_046BC89C03044417A30B63CE34C22543) uitvoert.

## Wat zijn de beste praktijken om gedeeltelijke gegevens te verminderen? {#section_065C38501527451C8058278054A1818D}

Controleer de volgende stappen om gedeeltelijke gegevensverzameling te verminderen:

| Stap | Taak |
| --- | --- |
| ![&#x200B; Stap 1 &#x200B;](assets/step1_icon.png) | Zorg ervoor dat de rapportsuite die u hebt geselecteerd in [!DNL Target] gelijk is aan de suite op de pagina&#39;s waar de activiteit wordt weergegeven. |
| ![&#x200B; Stap 2 &#x200B;](assets/step2_icon.png) | Zorg ervoor dat de bibliotheken bezoekerAPI.js, appMeasurement.js en at.js zich in versies bevinden die compatibel zijn met A4T. Meer over implementatievereisten leren, zie [&#x200B; alvorens u &#x200B;](/help/main/c-integrating-target-with-mac/a4t/before-implement.md) uitvoert. |
| ![&#x200B; Stap 3 &#x200B;](assets/step3_icon.png) | Zorg ervoor dat de SDID wordt ingesteld voor alle [!DNL Target] - en [!DNL Analytics] -aanroepen die de pagina verlaten en dat deze overeenkomen.<br/> gebruik een netwerkanalysator of het zuiveren hulpmiddel om ervoor te zorgen dat de `mboxMCSDID` parameter op [!DNL Target] vraag de parameter van SDID in de [!DNL Analytics] vraag aanpast. |
| ![&#x200B; Stap 4 &#x200B;](assets/step4_icon.png) | Controleer of de implementatiebibliotheken in de juiste volgorde op uw sites worden geladen. Voor meer informatie, zie [&#x200B; Analytics voor de Implementatie van het Doel &#x200B;](/help/main/c-integrating-target-with-mac/a4t/a4timplementation.md). |

## Hoe kan ik zien hoeveel gedeeltelijke gegevens ik heb? {#section_89B663E2824A4805AB934153508A0F4B}

Hoewel deze informatie niet rechtstreeks beschikbaar is in [!DNL Analytics] , kunt u contact opnemen met de klantenservice van Adobe om een rapport van Gedeeltelijke gegevens op te halen. Dit rapport is bedoeld om te helpen bij het opsporen van fouten.

## Hoe kan ik historische tendensen zonder gedeeltelijke gegevens bekijken? {#section_4C9DED560FAD4428B362DDA2064897C3}

Deze verwerkingswijziging heeft alleen invloed op gegevens na de releasedatum (14 november 2016). Als u de historische gegevens op elkaar wilt afstemmen, raadt Adobe u aan een segment te maken om gedeeltelijke gegevens uit te sluiten.

De volgende informatie met betrekking tot deze verandering omvat instructies om u te helpen het segment bepalen en het op een virtuele rapportreeks toepassen zodat dit segment altijd op uw [!DNL Analytics] meningen wordt toegepast.

In de meeste gevallen wordt een [!DNL Target] -hit gekoppeld aan een [!DNL Analytics] -hit op elke webpagina. Dit stitching gebeurt als er een verenigbare SDID in zowel de [!DNL Target] als [!DNL Analytics] vraag en een [!DNL Experience Cloud ID] (MCID) in de [!DNL Analytics] vraag op de zelfde pagina is. [!DNL Target] heeft doorgaans ook de MCID, maar als de aanroep naar [!DNL Target] plaatsvindt voordat de bezoeker-id wordt geretourneerd, wordt de hit nog steeds vastgezet vanwege de SDID. De gebruiker moet ook lang genoeg op de pagina blijven staan om een [!DNL Analytics] -aanroep te starten nadat een [!DNL Target] -aanroep is geactiveerd. Dit scenario is ideaal.

**Partial-gegevens klappen:** de gebruikers blijven soms niet lang genoeg op een pagina om een [!DNL Analytics] vraag te verzenden, maar [!DNL Target] heeft juiste MCID. Dit scenario resulteert in resultaten met gedeeltelijke gegevens (resultaten zonder paginaweergave [!DNL Analytics] ). Als deze gebruikers terugkeren naar uw site en een pagina met [!DNL Analytics] -code weergeven, worden ze correct geteld als bezoekers met terugzending. Deze treffers zouden verloren zijn gegaan als u slechts [!DNL Analytics] code op de pagina had. Sommige cliënten willen geen gegevens voor deze klappen omdat zij bepaalde metriek (bezoeken) opblazen en andere metriek (paginameningen per bezoek, tijd per bezoek, etc.) leegmaken. U ziet ook bezoeken zonder paginaweergaven. Er zijn echter nog geldige redenen om deze gegevens te bewaren.

Om gedeeltelijk-gegevensklappen te minimaliseren, kunt u uw paginalading sneller maken, aan de recentste versies van de bibliotheken bijwerken, of a [&#x200B; virtuele rapportreeks &#x200B;](https://experienceleague.adobe.com/docs/analytics/components/virtual-report-suites/vrs-workflow/vrs-create.html) creëren die die klappen uitsluiten. Voor geleidelijke instructies, zie [&#x200B; virtuele rapportsuites &#x200B;](https://experienceleague.adobe.com/docs/analytics/components/virtual-report-suites/vrs-workflow/vrs-create.html) in de *Gids van Componenten van Analytics* creëren.

De volgende illustratie toont voor de segmentdefinitie voor de virtuele rapportreeks:

![&#x200B; ts_a4t beeld &#x200B;](assets/ts_a4t.png)

Wanneer het creëren van de virtuele rapportreeks, specificeer de volgende configuratie voor de segmentdefinitie (zoals aangetoond in de bovengenoemde illustratie):

* **toon Actief:**
* Analyses voor doel: bestaat
* en
* Paginaweergaven: bestaat niet
* en
* Aangepaste koppelingsinstanties: bestaat niet
* en
* Koppelingsinstanties downloaden: bestaat niet
* en
* Koppelingsinstanties afsluiten: bestaat niet

**Geweesde klappen:** In minder situaties, blijven de gebruikers niet lang genoeg op de pagina voor een vraag van de Analyse en het Doel kreeg geen juiste MCID. Deze hits worden door Adobe gedefinieerd als &#39;zwevende&#39; hits. Deze treffers vertegenwoordigen klanten die zelden terugkeren en ze verhogen bezoek en bezoekers tellen onterecht.

Om deze &quot;weesse&quot;klappen te minimaliseren, kunt u a [&#x200B; virtuele rapportreeks &#x200B;](https://experienceleague.adobe.com/docs/analytics/components/virtual-report-suites/vrs-workflow/vrs-create.html) tot stand brengen die die klappen, zoals hierboven verklaard uitsluit.

## Wat betekent dit voor mijn [!DNL Target] rapportage? {#section_AAD354C722BE46D4875507F0FCBA5E36}

Wanneer deze wijziging optreedt, neemt het aantal nieuwe bezoekers en bezoeken aan live tests mogelijk af, omdat [!DNL Adobe] inkomende gedeeltelijke gegevens niet verwerkt. Conversies en treffers naar andere [!DNL Analytics] -meetgegevens worden niet gewijzigd.
