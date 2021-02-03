---
keywords: partiële gegevens;partiële gegevens;A4T;discrepanties;analyses voor doel;wees;virtueel rapportsuite;fantoom;problemen oplossen;ongestikt;opgepompt;niet gespecificeerd
description: Informatie die u helpt de gevolgen van opgeblazen Bezoek en Bezoeker te minimaliseren wanneer het gebruiken van Analytics als rapporteringsbron.
title: Inflated Visit and Visitor Counts in A4T minimaliseren
feature: Analytics for Target (A4T)
translation-type: tm+mt
source-git-commit: 48b94f967252f5ddb009597456edf0a43bc54ba6
workflow-type: tm+mt
source-wordcount: '1363'
ht-degree: 0%

---


# Vergrote aantallen bezoeken en bezoekers in A4T minimaliseren{#minimizing-inflated-visit-and-visitor-counts-in-a-t}

Informatie die u helpt de gevolgen van opgeblazen Bezoek en Bezoeker te minimaliseren wanneer het gebruiken van Analytics als rapporteringsbron.

>[!IMPORTANT]
>Op 14 november 2016 heeft Adobe Analytics de manier gewijzigd waarop sommige gegevens voor klanten worden verwerkt met Analytics Reporting for Target (A4T). Door deze wijzigingen worden Adobe Target-gegevens beter afgestemd op het gegevensmodel voor Adobe Analytics. Deze veranderingen werden opgesteld voor alle klanten die A4T gebruiken. Deze wijzigingen hebben specifiek betrekking op een probleem waarbij sommige klanten een opgeblazen aantal bezoekers hebben opgemerkt wanneer Target-activiteiten worden uitgevoerd.
>
>Deze wijziging is niet met terugwerkende kracht. Als uw historische rapporten opgeblazen aantallen tonen, en u zou hen van uw rapporten willen uitsluiten, kunt u een virtueel rapportreeks tot stand brengen, zoals hieronder verklaard.
>
>Bovendien zijn verschillende JavaScript-bibliotheken bijgewerkt om het aantal opgeblazen bestanden te minimaliseren. We raden u aan een upgrade uit te voeren naar de volgende (of nieuwere) bibliotheekversies:
>
>* Experience Cloud Bezoeker-id-service: bezoekerAPI.js versie 2.3.0 of later.
>* Adobe Analytics: appMeasurement.js versie 2.1.
>* Adobe Target: at.js versie 0.9.6 of hoger (behalve versie 1.1.0 als het gebruiken van aanbiedingen om met A4T te richten).

>
>  
De bibliotheek mbox.js ondersteunt geen omleidingsaanbiedingen met A4T. Uw implementatie moet at.js gebruiken.

## Wat is er veranderd? {#section_9CCF45F5D66D48EBA88F3A178B27D986}

Wanneer [!DNL Adobe Analytics] wordt gebruikt om [!DNL Target] activiteiten (genoemd A4T) te meten, [!DNL Analytics] verzamelt extra gegevens die niet beschikbaar zijn wanneer er geen [!DNL Target] activiteit op de pagina is. Dit is omdat de [!DNL Target] activiteit een vraag bij de bovenkant van de pagina in brand brengt, maar [!DNL Analytics] typisch zijn vraag van de gegevensinzameling bij de bodem van de pagina in brand. Bij de implementatie van A4T tot op heden, omvatten wij deze extra gegevens wanneer een [!DNL Target] activiteit actief was. In de toekomst worden deze aanvullende gegevens alleen opgenomen wanneer zowel de [!DNL Target]- als [!DNL Analytics]-tag zijn geactiveerd.

## Waarom heeft Adobe deze wijziging doorgevoerd? {#section_92380A4BD69E4B8886692DD27540C92A}

Adobe is trots op de nauwkeurigheid en kwaliteit van de gegevens. Wanneer de tag [!DNL Target] wordt geactiveerd, maar de tag [!DNL Analytics] niet, nemen we &quot;gedeeltelijke gegevens&quot; op (ook wel &quot;niet-opgeslagen resultaten&quot; genoemd), die niet zouden worden vastgelegd door [!DNL Analytics] als er geen [!DNL Target]-activiteit was. Hoewel het opnemen van deze deelgegevens in [!DNL Analytics]-rapportage aanvullende informatie verschaft, leidt dit ook tot inconsistentie met historische gegevens uit perioden waarin geen [!DNL Target]-activiteiten werden uitgevoerd. Dit kan problemen veroorzaken voor [!DNL Analytics] gebruikers die tendensen in tijd analyseren. Met het oog op de consistentie van gegevens in [!DNL Analytics] worden alle gedeeltelijke gegevens uitgesloten.

## Wat draagt bij aan gedeeltelijke gegevens? {#section_C9C906BEAA7D44DAB9D3C03932A2FEB8}

We hebben een aantal klanten gezien met zeer hoge percentages van gedeeltelijke gegevens in [!DNL Analytics]. Dit kan het gevolg zijn van een onjuiste uitvoering, maar er zijn ook legitieme oorzaken.

De vastgestelde oorzaken van gedeeltelijke gegevens zijn onder meer:

* **Verkeerd-uitgelijnde rapportsuite-id&#39;s (Implementatie):** de rapportsuite die tijdens de activiteiteninstelling is opgegeven, komt niet overeen met de rapportsuite op de pagina waar de test wordt uitgevoerd. Dit lijkt op gedeeltelijke gegevens omdat de gegevens niet kunnen worden afgestemd op [!DNL Analytics]-servers.
* **Trage pagina&#39;s:** Omdat de  [!DNL Target] vraag bij de bovenkant van de pagina is en de  [!DNL Analytics] vraag typisch bij de bodem van de pagina is, als de pagina langzaam laadt, verhoogt het de kans dat een bezoeker de pagina verlaat nadat de  [!DNL Target] vraag, maar vóór de  [!DNL Analytics] vraag brandt. Dit kan vooral problematisch zijn op mobiele websites, waar de verbindingen vaak trager zijn.
* **Paginafouten:** Als er JavaScript-fouten zijn of andere scenario&#39;s waarbij geen van de aanraakpunten wordt geactiveerd (Experience Cloud ID-service, Doel en Analyse), resulteren gedeeltelijke gegevens in.
* **Omleidingsaanbod(s) in  [!DNL Target] activiteit:** Voor omleidingsaanbiedingen in activiteiten die A4T gebruiken, moet uw implementatie aan bepaalde minimumvereisten voldoen. Bovendien is er belangrijke informatie die u moet weten. Zie [Aanbiedingen omleiden - A4T veelgestelde vragen](/help/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-redirect-offers.md#section_FA9384C2AA9D41EDBCE263FFFD1D9B58) voor meer informatie.
* **Oude versies van de bibliotheken:** Het afgelopen jaar heeft Adobe verschillende verbeteringen aangebracht in onze JavaScript-bibliotheken ( [!DNL appMeasurement.js],  `at.js/mbox.js`en  `visitorAPI.js`) om ervoor te zorgen dat gegevens zo efficiënt mogelijk worden verzonden. Meer over implementatievereisten leren, zie [Alvorens u ](/help/c-integrating-target-with-mac/a4t/before-implement.md#concept_046BC89C03044417A30B63CE34C22543) uitvoert.

## Wat zijn de beste praktijken om gedeeltelijke gegevens te verminderen? {#section_065C38501527451C8058278054A1818D}

Controleer de volgende stappen om de gedeeltelijke gegevensverzameling te verminderen:

| Stap | Taak |
| --- | --- |
| ![Stap 1](assets/step1_icon.png) | Zorg ervoor dat de rapportsuite die u hebt geselecteerd in [!DNL Target] gelijk is aan de suite op de pagina(&#39;s) waar de activiteit wordt weergegeven. |
| ![Stap 2](assets/step2_icon.png) | Zorg ervoor dat de bibliotheken bezoekerAPI.js, appMeasurement.js, at.js / mbox.js zich in versies bevinden die compatibel zijn met A4T. Meer over implementatievereisten leren, zie [Alvorens u ](/help/c-integrating-target-with-mac/a4t/before-implement.md) uitvoert. |
| ![Stap 3](assets/step3_icon.png) | Controleer of de SDID wordt ingesteld voor alle [!DNL Target]- en [!DNL Analytics]-aanroepen die de pagina verlaten en of deze overeenkomen.<br/>Doe dit door een netwerkanalysator of het zuiveren hulpmiddel te gebruiken om ervoor te zorgen dat de  `mboxMCSDID` parameter op  [!DNL Target] vraag(en) de parameter SDID in de  [!DNL Analytics] vraag aanpast. |
| ![Stap 4](assets/step4_icon.png) | Controleer of de implementatiebibliotheken in de juiste volgorde op uw sites worden geladen. Zie [Analytics for Target Implementation](/help/c-integrating-target-with-mac/a4t/a4timplementation.md) voor meer informatie. |

## Hoe kan ik zien hoeveel gedeeltelijke gegevens ik heb? {#section_89B663E2824A4805AB934153508A0F4B}

Hoewel deze informatie niet direct beschikbaar is in [!DNL Analytics], kunt u contact opnemen met de klantenservice van Adobe om een rapport van Gedeeltelijke gegevens op te halen. Dit rapport is bedoeld om te helpen bij het opsporen van fouten.

## Hoe kan ik historische tendensen zonder gedeeltelijke gegevens bekijken? {#section_4C9DED560FAD4428B362DDA2064897C3}

Omdat deze verwerkingsverandering gegevens slechts na de versiedatum (14 November, 2016) beïnvloedt, als u uw historische metriek zou willen aanpassen om aan te passen, adviseren wij dat u een segment creeert om gedeeltelijke gegevens uit te sluiten.

De volgende informatie met betrekking tot deze verandering omvat instructies om u te helpen het segment bepalen en het op een virtuele rapportreeks toepassen zodat dit segment altijd op uw [!DNL Analytics] meningen wordt toegepast.

In de meeste gevallen wordt een [!DNL Target] hit gekoppeld aan een [!DNL Analytics] hit op elke webpagina. Dit stitching gebeurt als er een verenigbare SDID in zowel [!DNL Target] als [!DNL Analytics] vraag en een [!DNL Experience Cloud ID] (MCID) in [!DNL Analytics] vraag op de zelfde pagina is. [!DNL Target] heeft doorgaans ook de MCID, maar als de aanroep  [!DNL Target] plaatsvindt voordat de bezoeker-id wordt geretourneerd, wordt de hit nog steeds vastgezet vanwege de SDID. Ook, moet de gebruiker lang genoeg op de pagina blijven om een [!DNL Analytics] vraag in werking te stellen nadat een [!DNL Target] vraag werd ontbrand. Dit is het ideale scenario.

**Gedeeltelijke-gegevenstreffers:** Gebruikers blijven soms niet lang genoeg op een pagina om een  [!DNL Analytics] vraag te verzenden, maar  [!DNL Target] hebben juiste MCID. Dit resulteert in gedeeltelijk-gegevensklare klappen (klappen met geen [!DNL Analytics] paginamening). Als deze gebruikers terugkeren naar uw site en een pagina met [!DNL Analytics] code weergeven, worden ze correct geteld als terugkerende bezoekers. Dit zijn treffers die verloren zouden zijn gegaan als u slechts [!DNL Analytics] code op de pagina had. Sommige cliënten willen geen gegevens voor deze klappen omdat zij bepaalde metriek (bezoeken) opblazen en andere metriek (paginameningen per bezoek, tijd per bezoek, etc.) leegmaken. U zult ook bezoeken zonder enige paginameningen zien. Er zijn echter nog geldige redenen om deze gegevens te bewaren.

Als u hits met gedeeltelijke gegevens wilt minimaliseren, kunt u de pagina sneller laden, bijwerken naar de nieuwste versies van de bibliotheken of een [virtuele rapportsuite](https://experienceleague.adobe.com/docs/analytics/components/virtual-report-suites/vrs-workflow/vrs-create.html) maken die deze resultaten uitsluiten. Zie [Virtuele rapportsuites maken](https://experienceleague.adobe.com/docs/analytics/components/virtual-report-suites/vrs-workflow/vrs-create.html) in de *Handleiding Analytics Components* voor stapsgewijze instructies.

De volgende illustratie toont voor de segmentdefinitie voor de virtuele rapportreeks:

![](assets/ts_a4t.png)

Wanneer het creëren van de virtuele rapportreeks, specificeer de volgende configuratie voor de segmentdefinitie (zoals aangetoond in de bovengenoemde illustratie):

* **Actief tonen:**
* Analyses voor doel: Exists
* en
* Paginaweergaven: Is niet bestaand
* en
* Aangepaste koppelingsinstanties: Is niet bestaand
* en
* Koppelingsinstanties downloaden: Is niet bestaand
* en
* Koppelingsinstanties afsluiten: Is niet bestaand

**Geweesde klappen:** In minder situaties, blijven de gebruikers niet lang genoeg op de pagina voor een vraag van de Analyse en het Doel kreeg geen juiste MCID. Dit zijn wat we definiëren als &#39;zwevende&#39; hits. Deze treffers vertegenwoordigen klanten die zelden terugkeren en ze verhogen bezoek en bezoekers tellen onterecht.

Om deze &quot;wees&quot;klappen te minimaliseren, kunt u een [virtueel rapportreeks ](https://experienceleague.adobe.com/docs/analytics/components/virtual-report-suites/vrs-workflow/vrs-create.html) tot stand brengen die die klappen, zoals hierboven verklaard uitsluiten.

## Wat betekent dit voor mijn [!DNL Target] rapportering? {#section_AAD354C722BE46D4875507F0FCBA5E36}

Als deze wijziging eenmaal is aangebracht, kunnen er minder nieuwe bezoekers en minder bezoekers voor live tests worden weergegeven omdat [!DNL Adobe] geen inkomende gedeeltelijke gegevens zal verwerken. Conversies en treffers naar andere [!DNL Analytics] metriek zullen niet veranderen.
