---
keywords: Adobe Experience Platform Web SDK;aep web sdk;aep sdk;search engine optimization;search engine optimization;seo;edge clusters, central clusters;at.js;mbox.js;
description: Leer hoe Adobe [!DNL Target] works, including information about the [!DNL Target] JavaScript bibliotheken (at.js en AEP Web SDK), de gegevenscentra van Adobe, en SEO het testen.
title: Hoe werkt [!DNL Target] ?
feature: Overzicht
exl-id: 8a93e061-0be7-4ecc-b511-2210094547f2
translation-type: tm+mt
source-git-commit: 6b13753c7254891bcf66003d69938ef90195bc78
workflow-type: tm+mt
source-wordcount: '2548'
ht-degree: 0%

---

# Hoe werkt Adobe [!DNL Target]

Leer hoe [!DNL Adobe Target] werkt, met inbegrip van informatie over [!DNL Adobe Experience Platform Web SDK] en bibliotheken JavaScript (at.js en mbox.js). In dit artikel worden ook de verschillende typen activiteiten geïntroduceerd die u kunt maken met [!DNL Target]. U kunt ook leren over het [!DNL Target] randnetwerk, de Optimalisering van de Motor van het Onderzoek (SEO), en hoe [!DNL Target] bots ontdekt.

## [!DNL Target] Platform Web SDK&#39;s en JavaScript-bibliotheken  {#libraries}

[!DNL Target] Wordt geïntegreerd met websites die gebruikmaken van de JavaScript-  [!DNL AEP Web SDK] of JavaScript-bibliotheken:

* **Adobe Experience Platform Web SDK:** De  [AEP Web ](/help/c-implementing-target/c-implementing-target-for-client-side-web/aep-web-sdk.md) SDK is een nieuwe client-side JavaScript-bibliotheek. Met de AEP Web SDK kunnen klanten van [!DNL Adobe Experience Cloud] via het [!DNL AEP] Edge Network communiceren met de verschillende services in [!DNL Experience Cloud] (inclusief [!DNL Target]). Adobe raadt alle nieuwe [!DNL Target]-klanten aan [!DNL AEP Web SDK] te implementeren.
* **at.js:** De  [bibliotheek at.js is een implementatiebibliotheek voor ](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-target-atjs-implementation/target-atjs-implementation.md#concept_8AC8D169E02944B1A547A0CAD97EAC17)   [!DNL Target]. De bibliotheek at.js verbetert de laadtijden voor webimplementaties en biedt betere implementatieopties voor toepassingen van één pagina. at.js wordt regelmatig bijgewerkt met nieuwe mogelijkheden. Adobe raadt alle klanten die at.js gebruiken aan hun implementaties bij te werken naar de [nieuwste versie van at.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md#reference_DBB5EDB79EC44E558F9E08D4774A0F7A).
* **mbox.js:** De  [mbox.js-](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/mbox-download.md) bibliotheek is de oudere implementatiebibliotheek voor  [!DNL Target]. De bibliotheek mbox.js wordt ondersteund tot 31 maart 2021; er zijn echter geen functie-updates.

>[!IMPORTANT]
>
>Alle klanten moeten naar [!DNL AEP Web SDK] of naar de recentste versie van at.js migreren. Zie [Adobe Experience Platform Web SDK](/help/c-implementing-target/c-implementing-target-for-client-side-web/aep-web-sdk.md) of [Migreren naar at.js vanuit mbox.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-target-atjs-implementation/target-migrate-atjs.md#task_DE55DCE9AC2F49728395665DE1B1E6EA) voor meer informatie.

Verwijs [!DNL AEP Web SDK] of at.js op elke pagina op uw plaats. U kunt bijvoorbeeld een van deze bibliotheken toevoegen aan uw algemene koptekst. U kunt ook [Adobe Platform launch](https://experienceleague.adobe.com/docs/launch/using/overview.html) gebruiken om [!DNL Target] te implementeren.

De volgende bronnen bevatten gedetailleerde informatie om u te helpen bij het implementeren van de AEP Web SDK of at.js:

* [Adobe Experience Platform Web SDK-extensie](https://experienceleague.adobe.com/docs/launch/using/extensions-ref/adobe-extension/aep-extension/overview.html?lang=en#configure-the-aep-web-sdk-extension)
* [Doel implementeren met Adobe Experience Platform Launch](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/cmp-implementing-target-using-adobe-launch.md)

Telkens wanneer een bezoeker een pagina aanvraagt die voor [!DNL Target] is geoptimaliseerd, wordt een verzoek verzonden naar het doelsysteem. Aan de hand van de aanvraag kunt u bepalen welke inhoud voor die bezoeker moet worden gebruikt. Dit proces vindt in real time plaats. Telkens wanneer een pagina wordt geladen, wordt een verzoek om de inhoud gedaan en vervuld door het systeem. De inhoud wordt bepaald door de regels van door de markt gecontroleerde activiteiten en ervaringen en is gericht op de individuele bezoeker van de site. Inhoud wordt weergegeven waarmee elke bezoeker van de site meestal kan reageren op, communiceren met of uiteindelijk aankopen. De gepersonaliseerde inhoud helpt reactiesnelheden, aanschafpercentages, en opbrengst maximaliseren.

In [!DNL Target] maakt elk element op de pagina deel uit van één enkele ervaring voor de gehele pagina. Elke ervaring kan meerdere elementen op de pagina bevatten.

De inhoud die aan bezoekers wordt weergegeven, is afhankelijk van het type activiteit dat u maakt:

### [!UICONTROL A/B Test]

De inhoud die wordt weergegeven in een standaard A/B-test, wordt willekeurig gekozen uit de ervaringen die u toewijst aan de activiteit. U kunt de percentages van de verkeerstoewijzing voor elke ervaring toewijzen. Als gevolg van deze willekeurige splitsing van het verkeer kan het een aanzienlijke hoeveelheid eerste verkeer nemen vóór de percentages zelfs uit. Als u bijvoorbeeld twee ervaringen creëert, wordt de startervaring willekeurig gekozen. Als er weinig verkeer is, is het mogelijk dat het percentage bezoekers naar één ervaring kan worden scheefgetrokken. Naarmate het verkeer toeneemt, worden de percentages gelijkgetrokken.

U kunt percentagedoelstellingen voor elke ervaring specificeren. In dit geval wordt een willekeurig getal gegenereerd en wordt dat nummer gebruikt om de ervaring te kiezen die u wilt weergeven. De resulterende percentages zouden niet precies de gespecificeerde doelstellingen kunnen aanpassen, maar meer verkeer betekent dat de ervaringen dichter aan de doeldoelstellingen zouden moeten worden verdeeld.

1. Een klant vraagt om een pagina van uw server en het toont in browser.
1. In de browser van de klant wordt een cookie van de eerste partij ingesteld om het gedrag van de klant op te slaan.
1. De pagina roept het doelsysteem aan.
1. De inhoud wordt weergegeven op basis van de regels van uw activiteit.

Zie [Een A/B-test maken](/help/c-activities/t-test-ab/t-test-create-ab/test-create-ab.md) voor meer informatie.

### [!UICONTROL Auto-Allocate]

[!UICONTROL Auto-Allocate] geeft de winnaar aan uit twee of meer ervaringen. [!UICONTROL Auto-Allocate] Wijst automatisch meer verkeer aan de het winnen ervaring opnieuw toe, die helpt om omzettingen te verhogen terwijl de test blijft lopen en leren.

Zie [[!UICONTROL Auto-Allocate]](/help/c-activities/automated-traffic-allocation/automated-traffic-allocation.md#concept_A1407678796B4C569E94CBA8A9F7F5D4) voor meer informatie.

### [!UICONTROL Auto-Target] (AT)

Auto-Doel gebruikt geavanceerd machine leren om uit veelvoudige hoog-presterende tellers-bepaalde ervaringen te selecteren. Auto-Target dient voor elke bezoeker de meest toegesneden ervaring. De levering van de ervaring is gebaseerd op individuele klantenprofielen en het gedrag van vorige bezoekers met gelijkaardige profielen. Gebruik Auto-Target om inhoud en aandrijvingsomzettingen aan te passen.

Zie [Auto-Target](/help/c-activities/auto-target/auto-target-to-optimize.md) voor meer informatie.

### [!UICONTROL Automated Personalization] (AP)

Automated Personalization (AP) combineert aanbiedingen of berichten en maakt gebruik van geavanceerd computerleren om verschillende aanbiedingsvariaties voor elke bezoeker aan te passen. De levering van de ervaring is gebaseerd op individuele klantenprofielen om inhoud en aandrijfhefboom te personaliseren.

Zie [Automated Personalization](/help/c-activities/t-automated-personalization/automated-personalization.md#task_8AAF837796D74CF893CA2F88BA1491C9) voor meer informatie.

### [!UICONTROL Experience Targeting] (XT)

Experience Targeting (XT) levert inhoud aan een specifiek publiek die op een reeks van tellers-bepaalde regels en criteria wordt gebaseerd.

Gerichte ervaring, met inbegrip van geotargeting, is nuttig voor het bepalen van regels die een specifieke ervaring of een inhoud aan een bepaald publiek richten. Verschillende regels kunnen in een activiteit worden gedefinieerd om verschillende inhoudvariaties aan verschillende doelgroepen te bieden. Wanneer bezoekers uw site bekijken, evalueert Experience Targeting (XT) ze om te bepalen of ze voldoen aan de criteria die u instelt. Als ze aan de criteria voldoen, voeren ze de activiteit in en wordt de ervaring die is ontworpen voor gekwalificeerd publiek weergegeven. U kunt ervaringen maken voor meerdere soorten publiek binnen één activiteit.

Zie [Experience Targeting](/help/c-activities/t-experience-target/experience-target.md#task_A53DF336CB9F4D7BB87EF2106099EFC4) voor meer informatie.

### [!UICONTROL Multivariate Test] (MVT)

Multivariate Testing (MVT) vergelijkt combinaties aanbiedingen in elementen op een pagina om te bepalen welke combinatie het beste voor een specifiek publiek presteert. MVT helpt te bepalen welk element het succes van de activiteit het meest beïnvloedt.

Zie [Multivariate Test](/help/c-activities/c-multivariate-testing/multivariate-testing.md#concept_628695CDC71B449B8DCC2F5654C11499) voor meer informatie.

### [!UICONTROL Recommendations]

Bij Recommendations-activiteiten worden automatisch producten of inhoud weergegeven die uw klanten interessant kunnen maken op basis van eerdere gebruikersactiviteiten of andere algoritmen. Recommendations helpt klanten om relevante objecten te sturen waarvan ze anders wellicht niet op de hoogte zijn.

Zie [Recommendations](/help/c-recommendations/recommendations.md#concept_7556C8A4543942F2A77B13A29339C0C0) voor meer informatie.

## Het Edge-netwerk {#concept_0AE2ED8E9DE64288A8B30FCBF1040934}

Een &quot;Rand&quot; is een geografisch gedistribueerde serverarchitectuur die optimale responstijden garandeert voor bezoekers die inhoud aanvragen, ongeacht waar ze zich over de hele wereld bevinden.

Om reactietijden te verbeteren, [!DNL Target] Randen gastheer slechts activiteitenlogica, caching profielen, en aanbiederinformatie.

Databanken voor activiteiten en inhoud, [!DNL Analytics]-gegevens, API&#39;s en markeergebruikersinterfaces zijn gehuisvest in de centrale clusters van Adobe. De updates worden dan verzonden naar [!DNL Target] Randen. De centrale clusters en de Edge-clusters worden automatisch gesynchroniseerd om de in de cache opgeslagen activiteitengegevens voortdurend bij te werken. Alle 1:1-modellering wordt ook opgeslagen op elke rand, zodat die complexere verzoeken ook aan de rand kunnen worden verwerkt.

Elke Edge-cluster beschikt over alle informatie die nodig is om te reageren op de aanvraag van de bezoeker voor inhoud en om analysegegevens over die aanvraag bij te houden. Bezoekersverzoeken worden naar de dichtstbijzijnde Edge-cluster gerouteerd.

Voor meer informatie, zie [het Witboek van het Overzicht van de Veiligheid van Adobe Target](https://www.adobe.com/content/dam/cc/en/security/pdfs/AdobeTargetSecurityOverview.pdf).

De [!DNL Target]-oplossing wordt gehost op datacenters in Adobe-eigendom en Adobe-leased over de hele wereld.

De centrale plaatsen van de Cluster bevatten zowel een centrum van de gegevensinzameling als een centrum van de gegevensverwerking. De plaatsen van de Cluster van de rand bevatten slechts een centrum van de gegevensinzameling. Elke rapportsuite wordt toegewezen aan een specifiek gegevensverwerkingscentrum.

De gegevens over de activiteiten op de locatie van de klant worden verzameld door de dichtstbijzijnde zeven Edge-clusters. Dit gegeven wordt geleid aan de vooraf bepaalde Centrale bestemming van de Cluster van een klant (één van drie plaatsen: Oregon, Dublin, Singapore) voor verwerking. Bezoekersprofielgegevens worden opgeslagen in de Edge-cluster die het dichtst bij de bezoeker van de site staat. De locaties van Edge-clusters omvatten de centrale clusterlocaties en Virginia, Amsterdam, Sydney, Tokio en Hongkong.

In plaats van te reageren op alle doelverzoeken van één locatie, worden aanvragen verwerkt door de Edge-cluster die het dichtst bij de bezoeker ligt. Dit proces helpt de gevolgen van netwerk/Internet reistijd verlichten.

![Kaart die de verschillende types van de servers van het Doel toont](/help/c-intro/assets/target-servers.png)

[!DNL Target] Centrale clusters, gehost op Amazon Web Services (AWS), omvatten:

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

De [!DNL Target Recommendations]-service wordt gehost in een [!DNL Adobe]-datacenter in Oregon.

>[!IMPORTANT]
>
>[!DNL Adobe Target] heeft momenteel geen Edge Cluster in China en de prestaties van de bezoeker blijven beperkt voor  [!DNL Target] klanten in China. Vanwege de firewall en het gebrek aan Edge Clusters in het land kunnen de ervaringen van sites met [!DNL Target] geïmplementeerd worden beïnvloed. De ervaring kan traag zijn bij het renderen en het laden van pagina&#39;s kan hierdoor worden beïnvloed. Ook, zouden de marketers latentie kunnen ervaren wanneer het gebruiken van [!DNL Target] auteursUI.

Desgewenst kunt u Edge-clusters lijsten van gewenste personen. [!DNL Target] Voor meer informatie, zie [de randknopen van het Doel van de lijst van gewenste personen](/help/c-implementing-target/c-considerations-before-you-implement-target/allowlist-edges.md).

## Beveiligde gebruikerservaring {#concept_40A5E781D90A41E4955F80EA9E5F8F96}

Adobe zorgt ervoor dat de beschikbaarheid en prestaties van de doelinfrastructuur zo betrouwbaar mogelijk zijn. Een communicatiestoring tussen de browser van een bezoeker en de servers van de Adobe kan echter een onderbreking in de levering van de inhoud veroorzaken.

Om tegen de dienstonderbrekingen en connectiviteitskwesties te beschermen, zijn alle plaatsen opstelling om standaardinhoud (die door de cliënt wordt bepaald) te omvatten. Deze standaardinhoud wordt weergegeven als de browser van de gebruiker geen verbinding kan maken met [!DNL Target].

Er worden geen wijzigingen aangebracht in de pagina als de browser van de gebruiker geen verbinding kan maken binnen een gedefinieerde time-outperiode (standaard: 15 seconden). Als deze time-outdrempel is bereikt, wordt standaardlocatie-inhoud weergegeven.

Adobe beschermt de gebruikerservaring door de prestaties te optimaliseren en te beveiligen.

* Adobe zorgt voor prestatiebenchmarks op basis van industriestandaarden, die worden gegarandeerd door de Adobe Service Level Agreement.
* Het Edge-netwerk zorgt voor tijdige gegevenslevering.
* Adobe gebruikt een multi-tiered benadering om zijn toepassingen te beveiligen om het hoogste niveau van beschikbaarheid en betrouwbaarheid voor klanten te verstrekken.
* [!DNL Target] Consulting biedt implementatieondersteuning en doorlopende productondersteuning.

## SEO (Search Engine Optimization, optimalisatie van zoekprogramma&#39;s) - vriendelijke tests {#concept_C0C865663CAB4251B66A1F250FD25E6A}

[!DNL Adobe Target] wordt uitgelijnd op de richtlijnen voor zoekprogramma&#39;s voor testen.

Google moedigt gebruikerstests aan. Google stelt in zijn documentatie dat A/B en Multivariate Testing geen schade toebrengen aan de classificatie van organische zoekmachines als u bepaalde richtlijnen opvolgt.

Zie de volgende Google-bronnen voor meer informatie:

* [Testen van websites en Google Search](https://webmasters.googleblog.com/2012/08/website-testing-google-search.html)
* [Experimenten en kleding](https://support.google.com/analytics/answer/2576845?hl=en&amp;ref_topic=1745207)

Richtlijnen zijn gepresenteerd in een bericht [Google Webmaster Central Blog](https://webmasters.googleblog.com/2012/08/website-testing-google-search.html). Hoewel de post dateert van 2012, blijft de meest recente verklaring van Google over deze kwestie en blijven de richtsnoeren relevant.

* **Geen camouflage**: Bij Camoufleren wordt één set inhoud weergegeven voor uw gebruikers en een andere set inhoud voor zoekprogrammavakken. Camoufleren wordt uitgevoerd door bots specifiek te identificeren en ze doelbewust verschillende inhoud te geven.

   [!DNL Target], als platform, is gevormd om onderzoeksmotor bots te behandelen het zelfde als om het even welke gebruiker. Als gevolg hiervan kunnen bots in de activiteiten worden opgenomen als de bots willekeurig worden geselecteerd en de testvariaties &quot;zie&quot;.

* **rel=&quot;canonical&quot;** gebruiken: Soms moet een A/B-test worden ingesteld met verschillende URL&#39;s voor de variaties. In deze gevallen moeten alle variaties een `rel="canonical"`-tag bevatten die verwijst naar de oorspronkelijke (controle)URL. Stel bijvoorbeeld dat Adobe de startpagina test met verschillende URL&#39;s voor elke variatie. De volgende canonieke tag voor de startpagina wordt in de tag `<head>` geplaatst voor elk van de variaties:

   `<link rel="canonical" href="https://www.adobe.com" />`

* **Gebruik 302 (tijdelijke) omleidingen**: In de gevallen waarin afzonderlijke URL&#39;s worden gebruikt voor de variatiepagina&#39;s in een test, raadt Google aan om een omleiding van 302 te gebruiken om direct verkeer naar de testvariaties te leiden. De 302 omleiding vertelt de zoekmachines dat de omleiding tijdelijk is en alleen actief zolang de test loopt.

   Een omleiding van 302 is een omleiding aan de serverzijde en [!DNL Target] gebruikt, samen met de meeste optimalisatieproviders, mogelijkheden aan de clientzijde. Daarom is omleiding een gebied waar [!DNL Target] niet volledig voldoet aan de aanbevelingen van Google. Deze praktijk is echter slechts van invloed op een klein deel van de tests. De standaardbenadering voor het runnen van tests door [!DNL Target] roept om inhoud binnen één enkele URL te veranderen, zodat zijn geen omleidingen noodzakelijk. Er zijn gevallen waarin clients meerdere URL&#39;s moeten gebruiken om hun testvariaties weer te geven. In deze gevallen gebruikt [!DNL Target] de JavaScript-opdracht `window.location`. Deze opdracht geeft gebruikers de opdracht om variaties te testen, wat niet expliciet aangeeft of omleiding een 301- of een 302-waarde is.

   Adobe blijft zoeken naar haalbare oplossingen om zich volledig aan te passen aan de richtlijnen van zoekprogramma&#39;s. Voor die cliënten die afzonderlijke URLs voor het testen moeten gebruiken, is Adobe zeker dat juiste implementatie van de canonieke markeringen het risico verbonden aan deze benadering verlicht.

* **Alleen experimenten uitvoeren zolang als nodig**: Adobe is van mening dat &quot;zo lang als nodig&quot; is om statistische significantie te bereiken. [!DNL Target] [biedt de beste ](https://docs.adobe.com/content/target-microsite/testcalculator.html) praktijken om te bepalen wanneer uw test dit punt heeft bereikt. Adobe raadt u aan om de hardcoded implementatie van het winnen van tests in uw testworkflow op te nemen en de juiste bronnen toe te wijzen.

   Het gebruik van het [!DNL Target]-platform voor het &quot;publiceren&quot; van winnende tests wordt niet aanbevolen als een permanente oplossing. Als de winnende test voor 100% van de gebruikers 100% van de tijd wordt gepubliceerd, kan deze benadering worden gebruikt terwijl het proces van het hardcoderen van de het winnen test wordt voltooid.

   Het is belangrijk om te overwegen wat uw test ook is veranderd. Als u de kleur van knoppen of andere kleine, niet-tekstuele items op de pagina bijwerkt, heeft dit geen invloed op uw organische waarderingen. Wijzigingen in tekst moeten echter wel worden gecodeerd.

   Het is ook belangrijk om de toegankelijkheid van de pagina te overwegen u test. Als de pagina niet toegankelijk is voor zoekprogramma&#39;s en nooit is ontworpen om in de eerste plaats een plaats te krijgen in biologisch zoeken, zijn geen van de bovenstaande overwegingen van toepassing. Een voorbeeld is een speciale bestemmingspagina voor een e-mailcampagne.

Google stelt dat het volgen van deze richtlijnen &quot;ertoe zou moeten leiden dat uw tests weinig of geen invloed hebben op uw site in zoekresultaten.&quot;

Naast deze richtlijnen geeft Google in de documentatie bij het programma Content Experiments ook een extra richtlijn:

* &quot;Uw variatiepagina&#39;s moeten de geest van de inhoud op de oorspronkelijke pagina&#39;s behouden. Deze variaties mogen de betekenis van of de algemene perceptie van de gebruiker van die originele inhoud niet veranderen.&quot;

Google geeft als voorbeeld dat &quot;als de originele pagina van een site wordt geladen met trefwoorden die geen betrekking hebben op de combinaties die worden weergegeven aan gebruikers, we die site mogelijk uit onze index kunnen verwijderen.&quot;

Adobe is van mening dat het moeilijk zou zijn om de betekenis van de oorspronkelijke inhoud onbedoeld te wijzigen in testvariaties. Adobe raadt echter aan de trefwoordthema&#39;s op een pagina onder de aandacht te brengen en deze thema&#39;s te behouden. Wijzigingen in de pagina-inhoud, met name het toevoegen of verwijderen van relevante trefwoorden, kunnen ertoe leiden dat wijzigingen in de positie van de URL in de organische zoekopdracht worden gewijzigd. Adobe adviseert dat u met uw partner SEO als deel van uw het testen protocol in dienst neemt.

## Bots {#bots}

Adobe [!DNL Target] gebruikt [DeviceAtlas](https://deviceatlas.com/device-data/user-agent-tester/) metrische &quot;isRobot&quot;om bekende bots te ontdekken die op het Koord van de Agent van de Gebruiker worden gebaseerd in de Kopbal van het Verzoek wordt overgegaan.

>[!NOTE]
>
> Voor [!DNL Server-Side] verzoeken, wordt de waarde die in [de &quot;Context&quot;knoop ](https://developers.adobetarget.com/api/delivery-api/#tag/Delivery-API) van het Verzoek wordt overgegaan gegeven belangrijkheid over het Koord van de Agent van de Gebruiker voor beide opsporing.

Verkeer dat door een bot wordt gegenereerd, wordt nog steeds aangeboden. Bots worden behandeld als een normale gebruiker om ervoor te zorgen dat [!DNL Target] in overeenstemming is met SEO-richtlijnen. Door beide verkeer te gebruiken, kunnen A/B-tests of verpersoonlijkingsalgoritmen scheeftrekken als ze worden behandeld als normale gebruikers. Daarom als een bekende bot in uw [!DNL Target] activiteit wordt ontdekt, wordt het verkeer lichtjes verschillend behandeld. Het verwijderen van beide verkeer zorgt voor een nauwkeurigere meting van de gebruikersactiviteit.

Voor bekende beide geldt dat verkeer [!DNL Target] niet:

* Een bezoekersprofiel maken of ophalen
* Profielkenmerken vastleggen of profielscripts uitvoeren
* Adobe Audience Manager-segmenten (AAM) opzoeken (indien van toepassing)
* Gebruik zowel het verkeer in modellering en het dienen van gepersonaliseerde inhoud voor Recommendations, auto-Doel, Automated Personalization of [!UICONTROL Auto-Allocate] activiteiten
* Een activiteitenbezoek aanmelden voor rapportage
* Loggegevens die naar het [!DNL Adobe Experience Cloud]-platform moeten worden verzonden
