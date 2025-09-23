---
keywords: Adobe Experience Platform Web SDK;aep web sdk;aep sdk;search engine optimization;search engine optimization;seo;edge clusters, central clusters;at.js;mbox.js;
description: Leer hoe  [!DNL Adobe Target]  werkt, met inbegrip van informatie over de bibliotheken van JavaScript (het Web van AEP SDK at.js), server-vraag gebruiksstrategieën, gebruik, de gegevenscentra van Adobe, SEO het testen, en bots.
title: Hoe werkt  [!DNL Target] ?
feature: Overview
exl-id: 8a93e061-0be7-4ecc-b511-2210094547f2
source-git-commit: 85edad5c3adb3a7b01ee6d1eaf2c30c7596d5f92
workflow-type: tm+mt
source-wordcount: '2214'
ht-degree: 0%

---

# Hoe [!DNL Adobe Target] werkt

Leer hoe [!DNL Adobe Target] werkt, inclusief informatie over de JavaScript-bibliotheken ([!DNL Adobe Experience Platform Web SDK] en at.js). In dit artikel worden ook de verschillende typen activiteiten beschreven die u kunt maken, [!DNL Target] strategieën voor het tellen van het gebruik, de [!DNL Target] Edge Network, SEO en beide detectie.

De belangrijkste punten zijn:

* **de Bibliotheken van JavaScript**: Leer informatie over de [!DNL Target] bibliotheken van JavaScript: [!DNL Adobe Experience Platform Web SDK] en at.js.
* **server-vraag gebruiksstrategieën**: Begrijp hoe [!DNL Target] diverse servervraag, met inbegrip van eindpunten, enige mbox, batch mbox, uitvoert, prefetch, en berichtvraag telt.
* **Edge Network**: Ontdek hoe [!DNL Target] met [!DNL Adobe Experience Platform Edge Network] interactie aangaat.
* **Beschermde gebruikerservaring**: Leer hoe [!DNL Adobe] de beschikbaarheid en de prestaties van zijn het richten infrastructuur verzekert.
* **SEO Richtlijnen**: Volg beste praktijken voor het richten van [!DNL Target] activiteiten op SEO richtlijnen.
* **Bot Verkeer**: Leer hoe het Doel zowel verkeer behandelt om het scheeftrekken tests en verpersoonlijkingsalgoritmen te vermijden.

## [!DNL Adobe Target] JavaScript-bibliotheken {#libraries}

Het doel kan met websites worden geïntegreerd met behulp van [!DNL Experience Platform Web SDK] of at.js:

* **[SDK van het Web van Adobe Experience Platform ](https://experienceleague.adobe.com/en/docs/target-dev/developer/client-side/aep/aep-web-sdk-overview){target=_blank}**: Deze cliënt-kant bibliotheek van JavaScript staat [!DNL Adobe Experience Cloud] klanten toe om met diverse diensten door [!DNL Experience Platform Edge Network] in wisselwerking te staan. [!DNL Adobe] raadt aan dat nieuwe [!DNL Target] -klanten [!DNL Experience Platform Web SDK] implementeren.
* **[at.js ](https://experienceleague.adobe.com/en/docs/target-dev/developer/client-side/at-js-implementation/deploy-at-js/how-to-deployatjs){target=_blank}**: Deze implementatiebibliotheek voor [!DNL Target] verbetert pagina-lading tijden voor Webimplementaties en biedt betere opties voor single-page toepassingen aan. Vaak bijgewerkt met nieuwe mogelijkheden, [!DNL Adobe] adviseert alle [ at.js gebruikers aan de recentste versie ](https://experienceleague-review.corp.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html){target=_blank} bijwerken.

>[!NOTE]
>
>De bibliotheek mbox.js is een oudere implementatie voor [!DNL Target] en wordt na 31 maart 2021 niet meer ondersteund. Voer een upgrade uit naar [!UICONTROL Experience Platform Web SDK] (voorkeur) of de meest recente versie van at.js.

Verwijs naar [!UICONTROL Experience Platform Web SDK] of at.js op elke pagina van uw plaats. Voeg bijvoorbeeld een van deze bibliotheken toe aan de algemene koptekst. Alternatief, gebruik [ markeringen in Adobe Experience Platform ](https://experienceleague.adobe.com/en/docs/experience-platform/tags/home){target=_blank} om uit te voeren [!DNL Target].

De volgende bronnen bevatten gedetailleerde informatie om u te helpen bij het implementeren van de map [!DNL Experience Platform Web SDK] of at.js:

* [[!DNL Adobe Experience Platform Web SDK]  uitbreiding ](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/adobe/sdk/overview.html){target=_blank}
* [ voert  [!DNL Target]  uit gebruikend  [!DNL Adobe Experience Platform] ](https://experienceleague.adobe.com/en/docs/target-dev/developer/client-side/at-js-implementation/deploy-at-js/implement-target-using-adobe-launch){target=_blank}

Telkens wanneer een bezoeker een pagina aanvraagt die voor [!DNL Target] is geoptimaliseerd, wordt een verzoek in real time verzonden naar het doelsysteem om de te dienen inhoud te bepalen. Dit verzoek wordt gedaan en voldaan telkens als een pagina wordt geladen, die door de markt-gecontroleerde activiteiten en ervaringen wordt geleid. De inhoud is gericht op individuele sitebezoekers, waarbij de responspercentages, de aanschafpercentages en de inkomsten worden gemaximaliseerd. Met persoonlijke inhoud zorgt u ervoor dat bezoekers reageren, communiceren of aankopen doen.

In [!DNL Target] maakt elk element op de pagina deel uit van één ervaring, die meerdere elementen kan bevatten.

De weergegeven inhoud is afhankelijk van het type activiteit dat u maakt:

### [!UICONTROL A/B Test]

Bij een A/B-basistest wordt de inhoud willekeurig gekozen uit de toegewezen ervaringen. U kunt de percentages van de verkeerstoewijzing voor elke ervaring plaatsen. In eerste instantie kan het verkeer ongelijk verdeeld zijn als gevolg van willekeurige splitsingen, maar het wordt gelijk als het verkeer toeneemt. Met twee ervaringen wordt de startervaring bijvoorbeeld willekeurig gekozen. Het lage verkeer kan bezoekerspercentages in de richting van één ervaring schuintrekken, maar deze situatie verdeelt zich uit met meer verkeer.

Geef streefpercentages op voor elke ervaring. Er wordt een willekeurig getal gegenereerd om de ervaring te selecteren die moet worden weergegeven. Terwijl de resulterende percentages niet precies de doelstellingen zouden kunnen aanpassen, leidt het hogere verkeer tot een nauwere splitsing aan de doeldoelstellingen.

1. Een klant vraagt om een pagina van uw server, die in hun browser toont.
1. In de browser van de klant wordt een cookie van de eerste partij ingesteld om het gedrag van de cookie op te slaan.
1. De pagina roept het doelsysteem aan.
1. Inhoud wordt weergegeven op basis van de activiteitenregels.

Zie [ een Test van A/B ](/help/main/c-activities/t-test-ab/t-test-create-ab/test-create-ab.md) voor meer informatie creëren.

### [!UICONTROL Auto-Allocate]

[!UICONTROL Auto-Allocate] geeft de winnende ervaring aan op basis van twee of meer opties. Het wijst dan automatisch meer verkeer aan de winnaar opnieuw toe, die omzettingen verhoogt aangezien de test blijft lopen en leren.

Zie [[!UICONTROL Auto-Allocate]](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md#concept_A1407678796B4C569E94CBA8A9F7F5D4) voor meer informatie.

### [!UICONTROL Auto-Target] (AT)

[!UICONTROL Auto-Target] maakt gebruik van geavanceerd leren van computers en maakt gebruik van meerdere hoogwaardige, door markters gedefinieerde ervaringen. [!UICONTROL Auto-Target] biedt elke bezoeker de meest op maat gemaakte ervaring op basis van individuele klantprofielen en het gedrag van eerdere bezoekers met vergelijkbare profielen. Gebruik [!UICONTROL Auto-Target] om inhoud en stationsomzettingen aan te passen.

Zie [ auto-Doel ](/help/main/c-activities/auto-target/auto-target-to-optimize.md) voor meer informatie.

### [!UICONTROL Automated Personalization] (AP)

[!UICONTROL Automated Personalization] (AP) combineert aanbiedingen of berichten en maakt gebruik van geavanceerd computerleren om verschillende variaties voor elke bezoeker op elkaar af te stemmen. AP past inhoud aan die op individuele klantenprofielen wordt gebaseerd om lift te drijven.

Zie [ Automated Personalization ](/help/main/c-activities/t-automated-personalization/automated-personalization.md#task_8AAF837796D74CF893CA2F88BA1491C9) voor meer informatie.

### [!UICONTROL Experience Targeting] (XT)

[!UICONTROL Experience Targeting] (XT) levert inhoud aan specifiek publiek dat op tellers-bepaalde regels en criteria wordt gebaseerd. Met inbegrip van het gericht richten, XT is waardevol voor het bepalen van regels die specifieke ervaringen of inhoud aan bepaalde doelgroepen richten. In een activiteit kunnen meerdere regels worden ingesteld voor verschillende inhoudvariaties voor verschillende doelgroepen. Wanneer bezoekers uw site bekijken, evalueert XT ze om te bepalen of ze aan de criteria voldoen. Als ze hiervoor in aanmerking komen, betreden ze de activiteit en zien ze de ervaring die voor hen is ontworpen. U kunt ervaringen maken voor meerdere soorten publiek binnen één activiteit.

Zie [ Ervaring richtend ](/help/main/c-activities/t-experience-target/experience-target.md#task_A53DF336CB9F4D7BB87EF2106099EFC4) voor meer informatie.

### [!UICONTROL Multivariate Test] (MV)

[!UICONTROL Multivariate Testing] (MVT) vergelijkt combinaties van aanbiedingen in pagina-elementen om te bepalen welke combinatie het beste presteert voor een bepaald publiek. MVT helpt te bepalen welk element het succes van de activiteit het meest beïnvloedt.

Zie [ Multivariate Test ](/help/main/c-activities/c-multivariate-testing/multivariate-testing.md#concept_628695CDC71B449B8DCC2F5654C11499) voor meer informatie.

### [!UICONTROL Recommendations]

[!UICONTROL Recommendations] -activiteiten geven automatisch producten of inhoud weer die klanten interessant kunnen maken op basis van hun vorige activiteit of andere algoritmen. De hulp van aanbevelingen leidt klanten aan relevante punten die zij anders niet zouden kunnen ontdekken.

Zie [ Aanbevelingen ](/help/main/c-recommendations/recommendations.md#concept_7556C8A4543942F2A77B13A29339C0C0) voor meer informatie.

<!--
## How [!DNL Target] counts server-call usage {#usage}

[!DNL Target] counts only server calls that provide value to customers. The following table shows how [!DNL Target] counts endpoints, single mbox, batch mbox calls, execute, prefetch, and notification calls.

The following information helps you understand the counting strategy used for [!DNL Target] server calls, as shown in the table below:

* **Count Once**: Counts once per API call.
* **Count the Number of mboxes**: Counts the number of mboxes under the array in the payload of a single API call.
* **Ignore**: Is not counted at all.
* **Count the Number of Views (Once)**: Counts the number of views under the array in the payload. In a typical implementation, a view notification has only one view under the notifications array, making this equivalent to counting once in most implementations.

|Endpoint|Fetch type|Options|Counting strategy|
|--- |--- |--- |-- |
|`rest//v1/mbox`|Single|[!UICONTROL execute]|Count once|
|`rest/v2/batchmbox`|Batch|[!UICONTROL execute]|Count the number of mboxes|
||Batch|[!UICONTROL prefetch]|Ignore|
||Batch|[!UICONTROL notifications]|Count the number of mboxes|
|`/ubox/[raw\|image\|page]`|Single|[!UICONTROL execute]|Count once|
|`rest/v1/delivery`<p>`/rest/v1/target-upstream`|Single|[!UICONTROL execute] > [!UICONTROL pageLoad]|Count once|
||Single|[!UICONTROL prefetch] > [!UICONTROL pageLoad]|Ignore|
||Single|[!UICONTROL prefetch] > [!UICONTROL views]|Ignore|
||Batch|[!UICONTROL execute] > [!UICONTROL mboxes]|Count the number of mboxes|
||Batch|[!UICONTROL prefetch] > [!UICONTROL mboxes]|Ignore|
||Batch|[!UICONTROL notifications] > [!UICONTROL views]|Count the number of views (once)|
||Batch|[!UICONTROL notifications] > [!UICONTROL pageLoad]|Count once|
||Batch|[!UICONTROL notifications] > type ([!UICONTROL conversions])|Count once|
||Batch|[!UICONTROL notifications] > [!UICONTROL mboxes]|Count the number of mboxes|

-->

## Het Edge-netwerk {#concept_0AE2ED8E9DE64288A8B30FCBF1040934}

Een &#39;Edge&#39; is een geografisch gedistribueerde serverarchitectuur die ervoor zorgt dat bezoekers die inhoud aanvragen, ongeacht hun locatie een optimale responstijd hebben.

Om reactietijden te verbeteren, [!DNL Target] Randen gastheer slechts activiteitenlogica, caching profielen, en aanbiedingsinformatie.

Databanken met activiteiten en inhoud, [!DNL Analytics] -gegevens, API&#39;s en gebruikersinterfaces voor markeertekens bevinden zich in [!DNL Adobe] Central-clusters. Updates worden verzonden naar de randen van [!DNL Target] . Deze worden automatisch gesynchroniseerd met de centrale clusters om de in de cache opgeslagen activiteitengegevens voortdurend bij te werken. Alle 1 :1 modellering wordt ook opgeslagen op elke rand, toestaand complexe verzoeken om plaatselijk worden verwerkt.

Elke Edge-cluster bevat alle benodigde informatie om te reageren op verzoeken om inhoud van bezoekers en analysegegevens bij te houden. Bezoekersverzoeken worden naar de dichtstbijzijnde Edge-cluster gerouteerd.

Voor meer informatie, zie het [ Witboek van het Overzicht van de Veiligheid van 0&rbrace; Adobe Target.](https://www.adobe.com/content/dam/cc/en/security/pdfs/AdobeTargetSecurityOverview.pdf)

[!DNL Target] wordt wereldwijd gehost op datacenters in Adobe en Adobe.

De centrale plaatsen van de Cluster huisvesten zowel gegevensinzameling als gegevensverwerkingscentra. Edge Cluster-locaties bevatten alleen centra voor gegevensverzameling. Elke rapportsuite wordt toegewezen aan een specifiek gegevensverwerkingscentrum.

Gegevens over activiteiten op de locatie van de klant worden verzameld door de dichtstbijzijnde zeven Edge-clusters. Deze gegevens worden vervolgens naar een vooraf bepaalde centrale clusterbestemming (Oregon, Dublin of Singapore) gestuurd voor verwerking. Bezoekersprofielgegevens worden opgeslagen in de Edge-cluster die het dichtst bij de bezoeker van de site staat. De locaties van Edge Cluster omvatten de centrale clusterlocaties, alsook Virginia, Mumbai, Sydney en Tokio.

In plaats van alle gerichte aanvragen van één locatie te verwerken, worden de aanvragen afgehandeld door de Edge-cluster die het dichtst bij de bezoeker ligt. Deze benadering verlicht het effect van netwerk en de reistijd van Internet.

![ Kaart die de verschillende soorten servers van het Doel tonen ](/help/main/c-intro/assets/target-servers.png)

[!DNL Target] Centrale clusters, gehost op Amazon Web Services (AWS), zijn onder meer:

* Oregon, VS
* Dublin, Ierland
* Republiek Singapore

[!DNL Target] Edge-clusters, gehost op AWS, omvatten:

* Mumbai, India
* Tokio, Japan
* Virginia, VS
* Oregon, VS
* Sydney, Australië
* Dublin, Ierland
* Republiek Singapore

De service [!DNL Target Recommendations] wordt gehost in een [!DNL Adobe] -datacenter in Oregon.

>[!IMPORTANT]
>
>[!DNL Target] heeft momenteel geen Edge Cluster in China, waardoor de prestaties van bezoekers voor [!DNL Target] -klanten in de regio worden beperkt. De firewall en het ontbreken van Edge-clusters kunnen van invloed zijn op de ervaringen van sites, wat leidt tot een trage weergave en een langere laadtijd voor de pagina. Marketers kunnen bovendien latentie ervaren wanneer ze de [!DNL Target] -ontwerpinterface gebruiken.

U kunt desgewenst [!DNL Target] Edge-clusters lijsten van gewenste personen. Voor meer informatie, zie [ de randknopen van het Doel van de lijst van gewenste personen ](https://experienceleague.adobe.com/en/docs/target-dev/developer/implementation/privacy/allowlist-edges){target=_blank}.

## Beveiligde gebruikerservaring {#concept_40A5E781D90A41E4955F80EA9E5F8F96}

[!DNL Adobe] zorgt ervoor dat de beschikbaarheid en prestaties van de doelinfrastructuur zo betrouwbaar mogelijk zijn. Communicatie tussen de browser van een bezoeker en [!DNL Adobe] servers kan echter de levering van inhoud onderbreken.

Om tegen de dienstonderbrekingen en connectiviteitskwesties te beschermen, zijn alle plaatsen opstelling om standaardinhoud (die door de cliënt wordt bepaald) te omvatten. Deze standaardinhoud wordt weergegeven als de browser van de bezoeker geen verbinding kan maken met [!DNL Target] .

Er worden geen wijzigingen aangebracht in de pagina als de browser van de bezoeker geen verbinding kan maken binnen een gedefinieerde time-outperiode (standaard: 15 seconden). Als deze time-outdrempel is bereikt, wordt standaardlocatie-inhoud weergegeven.

[!DNL Adobe] beschermt de gebruikerservaring door de prestaties te optimaliseren en te beveiligen.

* [!DNL Adobe] garandeert prestatiebenchmarks op basis van industriestandaarden, gegarandeerd door de [!UICONTROL Adobe Service Level Agreement] .
* De Edge Network zorgt voor tijdige gegevenslevering.
* [!UICONTROL Adobe] maakt gebruik van een aanpak met meerdere lagen om de toepassingen te beveiligen en biedt klanten het hoogste niveau van beschikbaarheid en betrouwbaarheid.
* [!DNL Target] Consulting biedt ondersteuning bij de implementatie en doorlopende productondersteuning.

## SEO-tests (Search Engine Optimization, optimalisatie van zoekmachines) {#concept_C0C865663CAB4251B66A1F250FD25E6A}

[!DNL Adobe Target] wordt uitgelijnd op de richtlijnen voor zoekprogramma&#39;s voor testen. [!DNL Google] raadt gebruikerstests aan en geeft aan dat A/B en [!UICONTROL Multivariate Testing] de positie van de organische zoekmachine niet nadelig beïnvloeden als bepaalde richtlijnen worden gevolgd.

[!DNL Adobe Target] wordt uitgelijnd op de richtlijnen voor zoekprogramma&#39;s voor testen.

Zie de volgende Google-bronnen voor meer informatie:

* [ het testen van de Website en het Onderzoek van Google ](https://webmasters.googleblog.com/2012/08/website-testing-google-search.html)
* [ Experimenten en het Camoufleren ](https://support.google.com/analytics/answer/12979939?hl)


De richtlijnen werden voorgesteld in a [ Google Webmaster Centrale Blog ](https://webmasters.googleblog.com/2012/08/website-testing-google-search.html) post. Hoewel de post dateert van 2012, blijft de meest recente verklaring van [!DNL Google] over deze kwestie en zijn de richtsnoeren nog steeds relevant.

* **Geen het camoufleren**: Het camoufleren impliceert het tonen van één reeks inhoud aan gebruikers en een verschillende reeks aan de bots van de onderzoeksmotor door bots specifiek te identificeren en hen verschillende inhoud te voeren.

  [!DNL Target] is geconfigureerd voor de behandeling van bots van zoekprogramma&#39;s. Daarom kunnen vleermuizen in de activiteiten worden opgenomen als zij willekeurig worden geselecteerd en &quot;zie&quot; de testvariaties.

* **Gebruik rel= &quot;canonical&quot;**: Soms vereist een A/B test verschillende URLs voor variaties. In deze gevallen moeten alle variaties een rel=&quot;canonical&quot;-tag bevatten die verwijst naar de oorspronkelijke (controle)URL. Als [!DNL Adobe] bijvoorbeeld zijn startpagina test met verschillende URL&#39;s voor elke variatie, moet de volgende canonieke tag voor de startpagina in de tag `<head>` van elke variatie worden geplaatst:

  `<link rel="canonical" href="https://www.adobe.com" />`

* **Gebruik 302 (tijdelijk) richt** opnieuw: Wanneer afzonderlijke URLs voor variatiepagina&#39;s in een test wordt gebruikt, [!DNL Google] adviseert het gebruiken van 302 opnieuw richt aan direct verkeer aan de testvariaties. De 302 omleiding geeft aan zoekprogramma&#39;s aan dat de omleiding slechts tijdelijk en actief is terwijl de test wordt uitgevoerd.

  Een omleiding van 302 is een omleiding aan de serverzijde, terwijl [!DNL Target] en de meeste optimalisatieproviders mogelijkheden aan de clientzijde gebruiken. Daarom voldoet [!DNL Target] niet volledig aan de aanbevelingen van [!DNL Google] voor omleidingen. Dit is echter slechts van invloed op een klein deel van de tests. De standaardbenadering voor het uitvoeren van tests door [!DNL Target] impliceert het veranderen van inhoud binnen één enkele URL, die de behoefte aan omleiding elimineert. In gevallen waarin meerdere URL&#39;s vereist zijn voor testvariaties, gebruikt [!DNL Target] de opdracht JavaScript `window.location` , die niet opgeeft of de omleiding een 301- of 302-URL is.

  [!DNL Adobe] zoekt actief naar oplossingen om volledig te voldoen aan de richtlijnen voor zoekprogramma&#39;s. Voor clients die afzonderlijke URL&#39;s voor tests nodig hebben, gelooft [!DNL Adobe] dat een correcte implementatie van canonieke tags de bijbehorende risico&#39;s beperkt.

* **de experimenten van de Looppas slechts zolang noodzakelijk**: [!DNL Adobe] bepaalt &quot;zo lang als noodzakelijk&quot;zoals de tijd wordt vereist om statistische betekenis te bereiken. [!DNL Target] biedt beste praktijken en de [!DNL Adobe Target] [ calculator van de Grootte van de Steekproef ](/help/main/c-activities/t-test-ab/sample-size-determination.md#section_6B8725BD704C4AFE939EF2A6B6E834E6) aan om te bepalen wanneer uw test dit punt heeft bereikt. [!DNL Adobe] raadt u aan om de hardcoded implementatie van het winnen van tests op te nemen in uw testworkflow en de juiste bronnen toe te wijzen.

  Het gebruik van [!DNL Target] voor het &#39;publiceren&#39; van winnende tests wordt niet aanbevolen als een permanente oplossing. Als de winnende test voortdurend voor 100% van de gebruikers wordt gepubliceerd, kan deze benadering tijdelijk worden gebruikt terwijl hard-codeert de het winnen test.

  Bedenk wat uw test is veranderd. Kleine updates, zoals knopkleuren, zijn niet van invloed op organische waarderingen. Tekstwijzigingen moeten echter wel hard worden gecodeerd.

  Overweeg ook de toegankelijkheid van de pagina die u test. Als de pagina niet toegankelijk is voor zoekprogramma&#39;s en nooit bedoeld was om in de biologische zoekfunctie te worden opgenomen, zijn deze overwegingen niet van toepassing. Een voorbeeld is een speciale bestemmingspagina voor een e-mailcampagne.

Google stelt dat het volgen van deze richtlijnen ertoe zou moeten leiden dat tests weinig of geen invloed hebben op uw site in zoekresultaten.

Naast deze richtlijnen geeft Google in de documentatie bij het programma Content Experiments nog een andere richtlijn:

* &quot;Uw variatiepagina&#39;s moeten de geest van de inhoud op de oorspronkelijke pagina&#39;s behouden. Deze variaties mogen de betekenis van of de algemene perceptie van de gebruiker van die originele inhoud niet veranderen.&quot;

Google geeft als voorbeeld dat &quot;als de originele pagina van een site wordt geladen met trefwoorden die geen betrekking hebben op de combinaties die worden weergegeven aan gebruikers, we die site mogelijk uit onze index kunnen verwijderen.&quot;

[!UICONTROL Adobe] is van mening dat het moeilijk zou zijn om de betekenis van de oorspronkelijke inhoud onbedoeld te wijzigen in testvariaties. [!UICONTROL Adobe] raadt u echter aan rekening te houden met de trefwoordthema&#39;s op een pagina en deze thema&#39;s te behouden. Wijzigingen in de pagina-inhoud, met name het toevoegen of verwijderen van relevante trefwoorden, kunnen ertoe leiden dat wijzigingen in de positie van de URL in de organische zoekopdracht worden gewijzigd. [!DNL Adobe] raadt u aan contact op te nemen met uw SEO-partner als onderdeel van uw testprotocol.

## Bots {#bots}

[!DNL Target] gebruikt [ DeviceAtlas ](https://deviceatlas.com/device-data/user-agent-tester/) metrische &quot;isRobot&quot;om bekende bots te ontdekken die op het Koord van de Agent van de Gebruiker worden gebaseerd die in de Kopbal van het Verzoek wordt overgegaan.

>[!NOTE]
>
> Voor [!DNL Server-Side] verzoeken, wordt de waarde die in de [ &quot;Context&quot;knoop van het Verzoek ](https://developers.adobetarget.com/api/delivery-api/#tag/Delivery-API) wordt overgegaan gegeven belangrijkheid over het Koord van de Agent van de Gebruiker voor beide opsporing.

Het verkeer dat als allebei-geproduceerd wordt geïdentificeerd wordt nog gediend inhoud. De blokken worden als gewone gebruikers behandeld om ervoor te zorgen dat [!DNL Target] zich aan SEO richtlijnen richt. Het beide verkeer kan echter A/B-tests of personalisatiealgoritmen scheeftrekken als het wordt behandeld als normale gebruikers. Daarom wordt zowel bekend beide verkeer in uw [!DNL Target] -activiteit anders behandeld. Het verwijderen van beide verkeer zorgt voor een nauwkeurigere meting van de gebruikersactiviteit.

Voor bekend beide verkeer geldt dat [!DNL Target] niet:

* Een bezoekersprofiel maken of ophalen
* Profielkenmerken vastleggen of profielscripts uitvoeren
* [!DNL Adobe Audience Manager] (AAM) segmenten opzoeken (indien van toepassing)
* Gebruik zowel het verkeer in het modelleren van of het dienen van gepersonaliseerde inhoud voor [!UICONTROL Recommendations], [!UICONTROL Auto-Target], [!UICONTROL Automated Personalization], of [!UICONTROL Auto-Allocate] activiteiten
* Een activiteitenbezoek aanmelden voor rapportage
* Loggegevens die naar het [!DNL Adobe Experience Cloud] -platform moeten worden verzonden

Voor bekend beide verkeer geldt dat [!UICONTROL Analytics for Target] bij gebruik van [!DNL Target] (A4T) niet:

* Gebeurtenissen verzenden naar [!DNL Analytics]

Voor bekend beide verkeer bij het gebruik van `client_side` logging, retourneert [!DNL Target] niet:

* `tnta payload`
