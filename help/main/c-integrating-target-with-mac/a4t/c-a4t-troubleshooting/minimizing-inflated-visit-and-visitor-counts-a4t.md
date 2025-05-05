---
keywords: partiële gegevens;partiële gegevens;A4T;discrepanties;analyses voor doel;wees;virtueel rapportsuite;fantoom;problemen oplossen;ongestikt;opgepompt;niet gespecificeerd
description: Leer hoe u de effecten van opgeblazen bezoeken en bezoekers kunt minimaliseren wanneer u Analytics gebruikt voor [!DNL Target] (A4t). Leer wat "gedeeltelijke gegevens"is en hoe te om het te verminderen.
title: Hoe minimaliseer ik het aantal opgeblazen bezoekers en bezoekers in A4T?
feature: Analytics for Target (A4T)
exl-id: 308711f7-e630-4f6b-8a6d-a1f36ed7902d
source-git-commit: 293b2869957c2781be8272cfd0cc9f82d8e4f0f0
workflow-type: tm+mt
source-wordcount: '1345'
ht-degree: 0%

---

# Vergrote aantallen bezoeken en bezoekers in A4T minimaliseren

Informatie om de effecten van opgeblazen bezoeken en bezoekers te minimaliseren wanneer u [!DNL Adobe Analytics] als bron van rapportage voor [!DNL Adobe Target] (A4T).

>[!IMPORTANT]
>Op 14 november 2016 heeft Adobe Analytics de manier gewijzigd waarop sommige gegevens voor klanten worden verwerkt met Analytics Reporting for Target (A4T). Door deze wijzigingen worden Adobe Target-gegevens beter afgestemd op het gegevensmodel voor Adobe Analytics. Deze veranderingen werden opgesteld voor alle klanten die A4T gebruiken. Deze wijzigingen hebben specifiek betrekking op een probleem waarbij sommige klanten een opgeblazen aantal bezoekers hebben opgemerkt wanneer Target-activiteiten worden uitgevoerd.
>
>Deze wijziging is niet met terugwerkende kracht. Als uw historische rapporten opgeblazen aantallen tonen, en u zou hen van uw rapporten willen uitsluiten, kunt u een virtueel rapportreeks tot stand brengen, zoals hieronder verklaard.
>
>Bovendien zijn verschillende JavaScript-bibliotheken bijgewerkt om het aantal opgeblazen bestanden tot een minimum te beperken. Adobe raadt u aan een upgrade uit te voeren naar de volgende (of nieuwere) bibliotheekversies:
>
>* Experience Cloud Bezoeker-id-service: bezoekerAPI.js versie 2.3.0 of later.
>* Adobe Analytics: appMeasurement.js versie 2.1.
>* Adobe Target: at.js versie 0.9.6 of hoger (behalve versie 1.1.0 als het gebruiken van aanbiedingen om met A4T te richten).


## Wat is er veranderd? {#section_9CCF45F5D66D48EBA88F3A178B27D986}

Wanneer [!DNL Adobe Analytics] wordt gebruikt om te meten [!DNL Target] activiteiten (genaamd A4T); [!DNL Analytics] Hiermee worden extra gegevens verzameld die niet beschikbaar zijn als er geen [!DNL Target] activiteit op de pagina. De [!DNL Target] activiteit brengt een vraag bij de bovenkant van de pagina in brand, maar [!DNL Analytics] worden doorgaans onder aan de pagina aanroepen van de gegevensverzameling geactiveerd. Bij de implementatie van A4T tot op heden, omvat Adobe deze extra gegevens wanneer een [!DNL Target] activiteit was actief. Adobe bevat deze aanvullende gegevens alleen als beide [!DNL Target] en [!DNL Analytics] tags zijn afgegaan.

## Waarom heeft Adobe deze wijziging doorgevoerd? {#section_92380A4BD69E4B8886692DD27540C92A}

Adobe is trots op de nauwkeurigheid en kwaliteit van de gegevens. Wanneer de [!DNL Target] tag wordt geactiveerd, maar de tag [!DNL Analytics] tag does not, Analytics registreert &quot;partiële gegevens&quot; (ook wel &quot;niet-opgeslagen resultaten&quot; genoemd). Deze ongestikte treffers worden niet vastgelegd door [!DNL Analytics] als er geen [!DNL Target] activiteit. Hoewel u deze deelgegevens opneemt in [!DNL Analytics] de rapportage verschaft aanvullende informatie en creëert tevens inconsistentie met historische gegevens uit perioden waarin er geen [!DNL Target] activiteiten die worden uitgevoerd. Deze situatie kan problemen veroorzaken voor [!DNL Analytics] gebruikers die trends in de loop der tijd analyseren. Met het oog op de consistentie van de gegevens in [!DNL Analytics], sluit Adobe alle gedeeltelijke gegevens uit.

## Wat draagt bij aan gedeeltelijke gegevens? {#section_C9C906BEAA7D44DAB9D3C03932A2FEB8}

Adobe heeft sommige klanten ontmoet met hoge tarieven van gedeeltelijke gegevens in [!DNL Analytics]. De hoge percentages van gedeeltelijke gegevens kunnen uit onjuiste implementatie voortvloeien, maar er zijn ook legitieme oorzaken.

De vastgestelde oorzaken van gedeeltelijke gegevens zijn onder meer:

* **Verkeerd uitgelijnde rapportsuite-id&#39;s (implementatie):** De rapportsuite die tijdens de activiteiteninstellingen is opgegeven, komt niet overeen met de rapportsuite op de pagina waar de test wordt uitgevoerd. De gegevens kunnen niet worden afgestemd op [!DNL Analytics] servers, zodat ziet het als gedeeltelijke gegevens.
* **Trage pagina&#39;s:** [!DNL Target] de vraag is bij de bovenkant van de pagina en [!DNL Analytics] de vraag is typisch bij de bodem van de pagina. Als de pagina langzaam wordt geladen, neemt de kans toe dat een bezoeker de pagina na de [!DNL Target] oproepen branden, maar voor de [!DNL Analytics] vraag. Trage pagina&#39;s kunnen vooral problematisch zijn op mobiele websites, waar de verbindingen vaak trager zijn.
* **Paginafouten:** Als er JavaScript-fouten zijn of andere scenario&#39;s waarin geen van de aanraakpunten wordt geactiveerd (Experience Cloud ID-service, Doel en Analyse), resulteert dit in gedeeltelijke gegevensresultaten.
* **Aanbiedingen omleiden in [!DNL Target] activiteit:** Voor omleidingsaanbiedingen in activiteiten die A4T gebruiken, moet uw implementatie aan bepaalde minimumvereisten voldoen. Bovendien is er belangrijke informatie die u moet weten. Zie voor meer informatie [Omleidingsvoorstellen - Veelgestelde vragen A4T](/help/main/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-redirect-offers.md#section_FA9384C2AA9D41EDBCE263FFFD1D9B58).
* **Oude versies van de bibliotheken:** Het afgelopen jaar heeft Adobe verschillende verbeteringen aangebracht in de JavaScript-bibliotheken ( [!DNL appMeasurement.js], `at.js`, en `visitorAPI.js`) om ervoor te zorgen dat de gegevens zo efficiënt mogelijk worden verzonden. Ga voor meer informatie over implementatievereisten naar [Voordat u gaat implementeren](/help/main/c-integrating-target-with-mac/a4t/before-implement.md#concept_046BC89C03044417A30B63CE34C22543).

## Wat zijn de beste praktijken om gedeeltelijke gegevens te verminderen? {#section_065C38501527451C8058278054A1818D}

Controleer de volgende stappen om gedeeltelijke gegevensverzameling te verminderen:

| Stap | Taak |
| --- | --- |
| ![Stap 1](assets/step1_icon.png) | Zorg ervoor dat de rapportsuite is geselecteerd in [!DNL Target] is hetzelfde als op de pagina&#39;s waarop de activiteit wordt weergegeven. |
| ![Stap 2](assets/step2_icon.png) | Zorg ervoor dat de bibliotheken bezoekerAPI.js, appMeasurement.js en at.js zich in versies bevinden die compatibel zijn met A4T. Ga voor meer informatie over implementatievereisten naar [Voordat u gaat implementeren](/help/main/c-integrating-target-with-mac/a4t/before-implement.md). |
| ![Stap 3](assets/step3_icon.png) | Zorg ervoor dat de SDID wordt ingesteld op alles [!DNL Target] en [!DNL Analytics] oproepen die de pagina verlaten en dat zij aanpassen.<br/>Gebruik een hulpprogramma voor netwerkanalyse of foutopsporing om ervoor te zorgen dat de `mboxMCSDID` parameter on [!DNL Target] aanroepen komen overeen met de SDID-parameter in het dialoogvenster [!DNL Analytics] vraag. |
| ![Stap 4](assets/step4_icon.png) | Controleer of de implementatiebibliotheken in de juiste volgorde op uw sites worden geladen. Zie voor meer informatie [Analyses voor doelimplementatie](/help/main/c-integrating-target-with-mac/a4t/a4timplementation.md). |

## Hoe kan ik zien hoeveel gedeeltelijke gegevens ik heb? {#section_89B663E2824A4805AB934153508A0F4B}

Hoewel deze informatie niet rechtstreeks beschikbaar is in [!DNL Analytics], kunt u contact opnemen met de klantenservice van Adobe om een gedeeltelijk gegevensrapport op te halen. Dit rapport is bedoeld om te helpen bij het opsporen van fouten.

## Hoe kan ik historische tendensen zonder gedeeltelijke gegevens bekijken? {#section_4C9DED560FAD4428B362DDA2064897C3}

Deze verwerkingswijziging heeft alleen invloed op gegevens na de releasedatum (14 november 2016). Als u uw historische metriek wilt aanpassen om aan te passen, adviseert Adobe dat u een segment creeert om gedeeltelijke gegevens uit te sluiten.

De volgende informatie met betrekking tot deze verandering omvat instructies om u te helpen het segment bepalen en het op een virtuele rapportreeks toepassen zodat dit segment altijd op uw wordt toegepast [!DNL Analytics] weergaven.

In de meeste situaties [!DNL Target] raakgebied is verbonden met een  [!DNL Analytics] op elke webpagina. Dit stitching gebeurt als er een verenigbare SDID in zowel  [!DNL Target] en [!DNL Analytics] oproep en [!DNL Experience Cloud ID] (MCID) in de  [!DNL Analytics] Vraag op de zelfde pagina. [!DNL Target] heeft typisch MCID eveneens, maar als de vraag aan [!DNL Target] gebeurt voordat de bezoeker-id wordt geretourneerd, wordt de hit nog steeds vastgezet vanwege de SDID. De gebruiker moet ook lang genoeg op de pagina blijven staan om een  [!DNL Analytics] bellen na een  [!DNL Target] oproep is afgebroken. Dit scenario is ideaal.

**Partial-data hits:** Gebruikers blijven soms niet lang genoeg op een pagina staan om een [!DNL Analytics] oproepen, maar [!DNL Target] heeft een juiste MCID. Dit scenario resulteert in gedeeltelijk-gegevensklare hits (hits zonder [!DNL Analytics] paginaweergave). Als deze gebruikers terugkeren naar uw site en een pagina weergeven met [!DNL Analytics] code, worden zij behoorlijk geteld als terugkerende bezoekers. Deze treffers zouden verloren zijn gegaan als u alleen [!DNL Analytics] code op de pagina. Sommige cliënten willen geen gegevens voor deze klappen omdat zij bepaalde metriek (bezoeken) opblazen en andere metriek (paginameningen per bezoek, tijd per bezoek, etc.) leegmaken. U ziet ook bezoeken zonder paginaweergaven. Er zijn echter nog geldige redenen om deze gegevens te bewaren.

Als u ongewenste resultaten met gedeeltelijke gegevens wilt minimaliseren, kunt u de pagina sneller laden, bijwerken naar de nieuwste versies van de bibliotheken of een [virtuele rapportsuite](https://experienceleague.adobe.com/docs/analytics/components/virtual-report-suites/vrs-workflow/vrs-create.html) dat sluit deze treffers uit. Voor stapsgewijze instructies raadpleegt u [Virtuele rapportsuites maken](https://experienceleague.adobe.com/docs/analytics/components/virtual-report-suites/vrs-workflow/vrs-create.html) in de *Handleiding Analytics Components*.

De volgende illustratie toont voor de segmentdefinitie voor de virtuele rapportreeks:

![ts_a4t-afbeelding](assets/ts_a4t.png)

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

**Zwevende treffers: &#x200B;** In minder situaties, blijven de gebruikers niet lang genoeg op de pagina voor een vraag van de Analyse en het Doel kreeg geen juiste MCID. Deze hits worden door Adobe gedefinieerd als &#39;zwevende&#39; hits. Deze treffers vertegenwoordigen klanten die zelden terugkeren en ze verhogen bezoek en bezoekers tellen onterecht.

Als u deze &#39;zwevende&#39; treffers wilt minimaliseren, kunt u een [virtuele rapportsuite](https://experienceleague.adobe.com/docs/analytics/components/virtual-report-suites/vrs-workflow/vrs-create.html) dit sluit deze treffers uit , zoals hierboven uiteengezet .

## Wat betekent dit voor mijn [!DNL Target] rapporteren? {#section_AAD354C722BE46D4875507F0FCBA5E36}

Wanneer deze wijziging optreedt, kunnen er minder nieuwe bezoekers en minder bezoekers aan live tests worden getoond omdat [!DNL Adobe] verwerkt geen binnenkomende gedeeltelijke gegevens. Conversies en hits naar andere [!DNL Analytics] metriek verandert niet.
