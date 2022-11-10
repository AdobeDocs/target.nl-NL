---
keywords: Adobe Experience Platform Web SDK;aep web sdk;aep sdk;search engine optimization;search engine optimization;seo;edge clusters, central clusters;at.js;mbox.js;
description: Meer informatie [!DNL Adobe Target] werken, waaronder informatie over JavaScript-bibliotheken (AEP Web SDK at.js), Adobe-datacenters, SEO-tests en bots.
title: Hoe werkt [!DNL Target] Werken?
feature: Overview
exl-id: 8a93e061-0be7-4ecc-b511-2210094547f2
source-git-commit: 4564e0b95bbd19f20c75e5e83d452d12a5403083
workflow-type: tm+mt
source-wordcount: '2541'
ht-degree: 0%

---

# Hoe [!DNL Adobe Target] werken

Meer informatie [!DNL Adobe Target] werken, waaronder informatie over de JavaScript-bibliotheken ([!DNL Adobe Experience Platform Web SDK] en at.js). In dit artikel worden ook de verschillende typen activiteiten geïntroduceerd die u kunt maken met [!DNL Target]. U kunt ook meer informatie krijgen over de [!DNL Target] randnetwerk, de Optimalisering van de Motor van het Onderzoek (SEO), en hoe [!DNL Target] detecteert bots.

## [!DNL Adobe Target] JavaScript-bibliotheken {#libraries}

[!DNL Target] integreert met websites die de [!DNL Experience Platform Web SDK] of at.js:

* **[!DNL Adobe Experience Platform Web SDK]:** De [Experience Platform Web SDK](https://developer.adobe.com/target/implement/client-side/aep-web-sdk/){target=_blank} is een nieuwe JavaScript-bibliotheek aan de clientzijde. De [!DNL Experience Platform Web SDK] laat klanten van [!DNL Adobe Experience Cloud] in de [!DNL Experience Cloud] (inclusief [!DNL Target]via de [!DNL Experience Platform] Edge Network. [!DNL Adobe] beveelt aan dat alle nieuwe [!DNL Target] klanten implementeren [!DNL Experience Platform Web SDK].
* **at.js:** De bibliotheek at.js is een implementatiebibliotheek voor [!DNL Target]. De bibliotheek at.js verbetert de laadtijden voor webimplementaties en biedt betere implementatieopties voor toepassingen van één pagina. at.js wordt regelmatig bijgewerkt met nieuwe mogelijkheden. [!DNL Adobe] raadt alle klanten die at.js gebruiken aan hun implementaties bij te werken naar de [nieuwste versie van at.js](https://developer.adobe.com/target/implement/client-side/atjs/target-atjs-versions/){target=_blank}.

>[!NOTE]
>
>De bibliotheek mbox.js is een oudere uitvoeringsbibliotheek voor [!DNL Target]. De bibliotheek mbox.js wordt na 31 maart 2021 niet meer ondersteund. Voer een upgrade uit naar de SDK van het Web Experience Platform (voorkeur) of naar de nieuwste versie van at.js.

Verwijs naar de [!DNL Experience Platform Web SDK] of om.js op elke pagina op uw plaats. U kunt bijvoorbeeld een van deze bibliotheken toevoegen aan uw algemene koptekst. U kunt ook overwegen om [tags in Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/tags/home.html) uitvoeren [!DNL Target].

De volgende bronnen bevatten gedetailleerde informatie om u te helpen de [!DNL Experience Platform Web SDK] of at.js:

* [[!DNL Adobe Experience Platform Web SDK] extension](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/adobe/sdk/overview.html?lang=en)
* [Implementeren [!DNL Target] gebruiken [!DNL Adobe Experience Platform]](https://developer.adobe.com/target/implement/client-side/atjs/how-to-deployatjs/implement-target-using-adobe-launch/)

Telkens wanneer een bezoeker een pagina aanvraagt waarvoor is geoptimaliseerd [!DNL Target], wordt een verzoek naar het doelsysteem verzonden. Aan de hand van de aanvraag kunt u bepalen welke inhoud voor die bezoeker moet worden gebruikt. Dit proces vindt in real time plaats. Telkens wanneer een pagina wordt geladen, wordt een verzoek om de inhoud gedaan en vervuld door het systeem. De inhoud wordt bepaald door de regels van door de markt gecontroleerde activiteiten en ervaringen en is gericht op de individuele bezoeker van de site. Inhoud wordt weergegeven waarmee elke bezoeker van de site meestal kan reageren op, communiceren met of uiteindelijk aankopen. De gepersonaliseerde inhoud helpt reactiesnelheden, aanschafpercentages, en opbrengst maximaliseren.

In [!DNL Target], maakt elk element op de pagina deel uit van één enkele ervaring voor de gehele pagina. Elke ervaring kan meerdere elementen op de pagina bevatten.

De inhoud die aan bezoekers wordt weergegeven, is afhankelijk van het type activiteit dat u maakt:

### [!UICONTROL A/B Test]

De inhoud die wordt weergegeven in een standaard A/B-test, wordt willekeurig gekozen uit de ervaringen die u toewijst aan de activiteit. U kunt de percentages van de verkeerstoewijzing voor elke ervaring toewijzen. Als gevolg van deze willekeurige splitsing van het verkeer kan het een aanzienlijke hoeveelheid eerste verkeer nemen vóór de percentages zelfs uit. Als u bijvoorbeeld twee ervaringen maakt, wordt de startervaring willekeurig gekozen. Als er weinig verkeer is, is het mogelijk dat het percentage bezoekers naar één ervaring kan worden scheefgetrokken. Naarmate het verkeer toeneemt, worden de percentages gelijkgetrokken.

U kunt percentagedoelstellingen voor elke ervaring specificeren. In dit geval wordt een willekeurig getal gegenereerd en wordt dat nummer gebruikt om de ervaring te kiezen die moet worden weergegeven. De resulterende percentages zouden niet precies de gespecificeerde doelstellingen kunnen aanpassen, maar meer verkeer betekent dat de ervaringen dichter aan de doeldoelstellingen zouden moeten worden verdeeld.

1. Een klant vraagt om een pagina van uw server en het toont in browser.
1. In de browser van de klant wordt een cookie van de eerste partij ingesteld om het gedrag van de klant op te slaan.
1. De pagina roept het doelsysteem aan.
1. De inhoud wordt weergegeven op basis van de regels van uw activiteit.

Zie [Een A/B-test maken](/help/main/c-activities/t-test-ab/t-test-create-ab/test-create-ab.md) voor meer informatie .

### [!UICONTROL Auto-Allocate]

[!UICONTROL Auto-Allocate] geeft de winnaar aan uit twee of meer ervaringen. [!UICONTROL Auto-Allocate] Wijst automatisch meer verkeer aan de het winnen ervaring opnieuw toe, die helpt om omzettingen te verhogen terwijl de test blijft lopen en leren.

Zie [[!UICONTROL Auto-Allocate]](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md#concept_A1407678796B4C569E94CBA8A9F7F5D4) voor meer informatie .

### [!UICONTROL Auto-Target] (AT)

[!UICONTROL Auto-Target] maakt gebruik van geavanceerd leren van computers om een keuze te maken uit meerdere, goed presterende, door markers gedefinieerde ervaringen. [!UICONTROL Auto-Target] biedt elke bezoeker de meest aangepaste ervaring. De levering van de ervaring is gebaseerd op individuele klantenprofielen en het gedrag van vorige bezoekers met gelijkaardige profielen. Gebruiken [!UICONTROL Auto-Target] om inhoud en aandrijvingsomzettingen aan te passen.

Zie [Automatisch doel](/help/main/c-activities/auto-target/auto-target-to-optimize.md) voor meer informatie .

### [!UICONTROL Automated Personalization] (AP)

[!UICONTROL Automated Personalization] (AP) combineert aanbiedingen of berichten en gebruikt geavanceerd computerleren om verschillende aanbiedingsvariaties voor elke bezoeker aan te passen. De levering van de ervaring is gebaseerd op individuele klantenprofielen om inhoud en aandrijfhefboom te personaliseren.

Zie [Automated Personalization](/help/main/c-activities/t-automated-personalization/automated-personalization.md#task_8AAF837796D74CF893CA2F88BA1491C9) voor meer informatie .

### [!UICONTROL Experience Targeting] (XT)

[!UICONTROL Experience Targeting] (XT) levert inhoud aan een specifiek publiek dat op een reeks van tellers-bepaalde regels en criteria wordt gebaseerd.

[!UICONTROL Experience Targeting], met inbegrip van geotarcering, is nuttig voor het bepalen van regels die een specifieke ervaring of inhoud voor een bepaald publiek richten. Verschillende regels kunnen in een activiteit worden gedefinieerd om verschillende inhoudvariaties aan verschillende doelgroepen te bieden. Wanneer bezoekers uw site bekijken, [!UICONTROL Experience Targeting] (XT) evalueert hen om te bepalen of zij aan de criteria voldoen u plaatst. Als ze aan de criteria voldoen, voeren ze de activiteit in en wordt de ervaring die is ontworpen voor gekwalificeerd publiek weergegeven. U kunt ervaringen maken voor meerdere soorten publiek binnen één activiteit.

Zie [Gericht op ervaring](/help/main/c-activities/t-experience-target/experience-target.md#task_A53DF336CB9F4D7BB87EF2106099EFC4) voor meer informatie .

### [!UICONTROL Multivariate Test] (MVT)

[!UICONTROL Multivariate Testing] (MVT) vergelijkt combinaties aanbiedingen in elementen op een pagina om te bepalen welke combinatie het beste voor een specifiek publiek presteert. MVT helpt te bepalen welk element het succes van de activiteit het meest beïnvloedt.

Zie [Multivariatietest](/help/main/c-activities/c-multivariate-testing/multivariate-testing.md#concept_628695CDC71B449B8DCC2F5654C11499) voor meer informatie .

### [!UICONTROL Recommendations]

[!UICONTROL Recommendations] de activiteiten tonen automatisch producten of inhoud die uw klanten op vorige gebruikersactiviteit of andere algoritmen zouden kunnen interesseren. Recommendations helpt klanten om relevante items die ze anders wellicht niet kennen, door te sturen.

Zie [Recommendations](/help/main/c-recommendations/recommendations.md#concept_7556C8A4543942F2A77B13A29339C0C0) voor meer informatie .

## Het Edge-netwerk {#concept_0AE2ED8E9DE64288A8B30FCBF1040934}

Een &quot;Rand&quot; is een geografisch gedistribueerde serverarchitectuur die optimale responstijden garandeert voor bezoekers die inhoud aanvragen, ongeacht waar ze zich over de hele wereld bevinden.

Om de responstijden te verbeteren, [!DNL Target] Met Randen kunt u alleen de logica van de hostactiviteit, profielen in de cache en informatie bieden.

Databanken voor activiteiten en inhoud; [!DNL Analytics] gegevens, APIs, en de gebruikersinterfaces van de tellers worden gehuisvest in Centraal Clusters van Adobe. Updates worden vervolgens verzonden naar de [!DNL Target] Randen. De centrale clusters en de Edge-clusters worden automatisch gesynchroniseerd om de in de cache opgeslagen activiteitengegevens voortdurend bij te werken. Alle 1:1-modellering wordt ook opgeslagen op elke rand, zodat die complexere verzoeken ook aan de rand kunnen worden verwerkt.

Elke Edge-cluster beschikt over alle informatie die nodig is om te reageren op de aanvraag van de bezoeker voor inhoud en om analysegegevens over die aanvraag bij te houden. Bezoekersverzoeken worden naar de dichtstbijzijnde Edge-cluster gerouteerd.

Zie voor meer informatie de [Adobe Target Security - Overzicht](https://www.adobe.com/content/dam/cc/en/security/pdfs/AdobeTargetSecurityOverview.pdf) wit papier.

De [!DNL Target] De oplossing wordt gehost op datacenters in Adobe-eigendom en Adobe-leased over de hele wereld.

De centrale plaatsen van de Cluster bevatten zowel een centrum van de gegevensinzameling als een centrum van de gegevensverwerking. De plaatsen van de Cluster van de rand bevatten slechts een centrum van de gegevensinzameling. Elke rapportsuite wordt toegewezen aan een specifiek gegevensverwerkingscentrum.

De gegevens over de activiteiten op de locatie van de klant worden verzameld door de dichtstbijzijnde zeven Edge-clusters. Deze gegevens worden gericht aan de vooraf bepaalde Centrale bestemming van de Cluster van een klant (één van drie plaatsen: Oregon, Dublin, Singapore) voor verwerking. Bezoekersprofielgegevens worden opgeslagen in de Edge-cluster die het dichtst bij de bezoeker van de site staat. De locaties van Edge-clusters omvatten de centrale clusterlocaties en Virginia, Mumbai, Sydney en Tokio.

In plaats van te reageren op alle doelverzoeken van één locatie, worden aanvragen verwerkt door de Edge-cluster die het dichtst bij de bezoeker ligt. Dit proces helpt de gevolgen van netwerk/Internet reistijd verlichten.

![Kaart die de verschillende types van de servers van het Doel toont](/help/main/c-intro/assets/target-servers.png)

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

De [!DNL Target Recommendations] service wordt gehost in een [!DNL Adobe] datacenter in Oregon.

>[!IMPORTANT]
>
>[!DNL Adobe Target] heeft momenteel geen Edge Cluster in China en de prestaties van de bezoeker blijven beperkt voor [!DNL Target] afnemers in China. Vanwege de firewall en het gebrek aan Edge Clusters in het land, hebben sites met [!DNL Target] kan worden beïnvloed. De ervaring kan traag zijn bij het renderen en het laden van pagina&#39;s kan hierdoor worden beïnvloed. Ook kunnen marketers enige vertraging ervaren bij het gebruik van de [!DNL Target] ontwerpinterface.

U kunt lijst van gewenste personen [!DNL Target] Edge-clusters, indien gewenst. Zie voor meer informatie [lijst van gewenste personen randknooppunten doel](https://developer.adobe.com/target/before-implement/privacy/allowlist-edges/){target=_blank}.

## Beveiligde gebruikerservaring {#concept_40A5E781D90A41E4955F80EA9E5F8F96}

[!DNL Adobe] zorgt ervoor dat de beschikbaarheid en prestaties van de doelinfrastructuur zo betrouwbaar mogelijk zijn. Een communicatiestoornis tussen de browser van een bezoeker en [!DNL Adobe] servers kunnen de levering van inhoud onderbreken.

Om tegen de dienstonderbrekingen en connectiviteitskwesties te beschermen, zijn alle plaatsen opstelling om standaardinhoud (die door de cliënt wordt bepaald) te omvatten. Deze standaardinhoud wordt weergegeven als de browser van de gebruiker geen verbinding kan maken met [!DNL Target].

Er worden geen wijzigingen aangebracht in de pagina als de browser van de gebruiker geen verbinding kan maken binnen een gedefinieerde time-outperiode (standaard: 15 seconden). Als deze time-outdrempel is bereikt, wordt standaardlocatie-inhoud weergegeven.

[!DNL Adobe] beschermt de gebruikerservaring door prestaties te optimaliseren en te beschermen.

* [!DNL Adobe] biedt prestatiebenchmarks die zijn gebaseerd op industriestandaarden, die worden gegarandeerd door de Adobe Service Level Agreement.
* Het Edge-netwerk zorgt voor tijdige gegevenslevering.
* [!UICONTROL Adobe] maakt gebruik van een multi-tiered benadering om zijn toepassingen te beveiligen om het hoogste niveau van beschikbaarheid en betrouwbaarheid voor klanten te verstrekken.
* [!DNL Target] Consulting biedt implementatieondersteuning en doorlopende productondersteuning.

## SEO-tests (Search Engine Optimization, optimalisatie van zoekprogramma&#39;s) {#concept_C0C865663CAB4251B66A1F250FD25E6A}

[!DNL Adobe Target] wordt uitgelijnd op de richtlijnen voor zoekprogramma&#39;s voor testen.

Google moedigt gebruikerstests aan. Google verklaart in haar documentatie dat A/B en [!UICONTROL Multivariate Testing] Hiermee wordt de positie van organische zoekmachines niet geschaad als u bepaalde richtlijnen opvolgt.

Zie de volgende Google-bronnen voor meer informatie:

* [Testen van websites en zoeken in Google](https://webmasters.googleblog.com/2012/08/website-testing-google-search.html)
* [Experimenten en kleding](https://support.google.com/analytics/answer/2576845?hl=en&amp;ref_topic=1745207)

Richtsnoeren werden gepresenteerd in een [Google Webmaster Central-blog](https://webmasters.googleblog.com/2012/08/website-testing-google-search.html) post. Hoewel de post dateert van 2012, blijft de meest recente verklaring van Google over deze kwestie en blijven de richtsnoeren relevant.

* **Geen camouflage**: Bij Camoufleren wordt één set inhoud weergegeven voor uw gebruikers en een andere set inhoud voor zoekprogrammavakken. Camoufleren wordt uitgevoerd door bots specifiek te identificeren en ze doelbewust verschillende inhoud te geven.

   [!DNL Target], als platform, is gevormd om onderzoeksmotor bots te behandelen het zelfde als om het even welke gebruiker. Als gevolg hiervan kunnen bots in de activiteiten worden opgenomen als de bots willekeurig worden geselecteerd en de testvariaties &quot;zie&quot;.

* **rel=&quot;canonical&quot; gebruiken**: Soms moet een A/B-test worden ingesteld met verschillende URL&#39;s voor de variaties. In deze gevallen moeten alle variaties een `rel="canonical"` -tag die verwijst naar de oorspronkelijke (controle)URL. Stel bijvoorbeeld dat [!DNL Adobe] test zijn homepage gebruikend verschillende URLs voor elke variatie. De volgende canonieke tag voor de homepage komt in het dialoogvenster `<head>` tag voor elk van de variaties:

   `<link rel="canonical" href="https://www.adobe.com" />`

* **302 (tijdelijke) omleidingen gebruiken**: In de gevallen waarin afzonderlijke URL&#39;s worden gebruikt voor de variatiepagina&#39;s in een test, raadt Google aan om 302 te gebruiken om het directe verkeer naar de testvariaties te leiden. De 302 omleiding vertelt de zoekmachines dat de omleiding tijdelijk is en alleen actief zolang de test loopt.

   Een omleiding van 302 is een omleiding aan de serverzijde, en [!DNL Target]gebruikt samen met de meeste optimalisatieproviders mogelijkheden aan de clientzijde. Daarom is omleiding een gebied waar [!DNL Target] voldoet niet volledig aan de aanbevelingen van Google. Deze praktijk is echter slechts van invloed op een klein deel van de tests. De standaardaanpak voor het uitvoeren van tests door [!DNL Target] roept om inhoud binnen één enkele URL te veranderen, zodat zijn geen omleidingen noodzakelijk. Er zijn gevallen waarin clients meerdere URL&#39;s moeten gebruiken om hun testvariaties weer te geven. In deze gevallen [!DNL Target] gebruikt het JavaScript `window.location` gebruiken. Deze opdracht geeft gebruikers de opdracht om variaties te testen, wat niet expliciet aangeeft of omleiding een 301- of een 302-waarde is.

   [!DNL Adobe] blijft zoeken naar levensvatbare oplossingen om zich volledig aan te passen aan de richtlijnen van zoekprogramma &#39; s . Voor clients die voor het testen afzonderlijke URL&#39;s moeten gebruiken, [!DNL Adobe] is ervan overtuigd dat een goede implementatie van de canonieke codes het risico dat aan deze aanpak verbonden is, beperkt.

* **Experimenten alleen uitvoeren zolang dat nodig is**: [!DNL Adobe] is van mening dat &quot; zo lang als nodig &quot; is om statistische significantie te bereiken . [!DNL Target] biedt beste praktijken en [!DNL Adobe Target] [Voorbeeldgroottecalculator] (/help/main/c-activities/t-test-ab/sample-size-determination.md#section_6B8725BD704C4AFE939EF2A6B6E834E6) om te bepalen wanneer uw test dit punt heeft bereikt. [!DNL Adobe] raadt u aan om de hardcoded implementatie van het winnen van tests in uw testwerkstroom op te nemen en de aangewezen middelen toe te wijzen.

   Met de [!DNL Target] het wordt niet aanbevolen om een platform te gebruiken voor het &quot; publiceren &quot; van winnende tests . Als de winnende test voor 100% van de gebruikers 100% van de tijd wordt gepubliceerd, kan deze benadering worden gebruikt terwijl het proces van hard-coderen de het winnen test wordt voltooid.

   Het is belangrijk om te overwegen wat uw test ook is veranderd. Als u de kleur van knoppen of andere kleine, niet-tekstuele items op de pagina bijwerkt, heeft dit geen invloed op uw organische waarderingen. Wijzigingen in tekst moeten echter wel worden gecodeerd.

   Het is ook belangrijk om de toegankelijkheid van de pagina te overwegen u test. Als de pagina niet toegankelijk is voor zoekprogramma&#39;s en nooit is ontworpen om in de eerste plaats een plaats te krijgen in biologisch zoeken, zijn geen van de bovenstaande overwegingen van toepassing. Een voorbeeld is een speciale bestemmingspagina voor een e-mailcampagne.

Google stelt dat het volgen van deze richtlijnen ertoe zou moeten leiden dat tests weinig of geen invloed hebben op uw site in zoekresultaten.

Naast deze richtlijnen geeft Google in de documentatie bij het programma Content Experiments nog een andere richtlijn:

* &quot;Uw variatiepagina&#39;s moeten de geest van de inhoud op de oorspronkelijke pagina&#39;s behouden. Deze variaties mogen de betekenis van of de algemene perceptie van de gebruiker van die originele inhoud niet veranderen.&quot;

Google geeft als voorbeeld dat &quot;als de originele pagina van een site wordt geladen met trefwoorden die geen betrekking hebben op de combinaties die worden weergegeven aan gebruikers, we die site mogelijk uit onze index kunnen verwijderen.&quot;

[!UICONTROL Adobe] is van mening dat het moeilijk zou zijn om de betekenis van de oorspronkelijke inhoud onbedoeld te wijzigen in het kader van testvariaties. Maar [!UICONTROL Adobe] Het is raadzaam de trefwoordthema&#39;s op een pagina onder de aandacht te brengen en deze thema&#39;s te behouden. Wijzigingen in de pagina-inhoud, met name het toevoegen of verwijderen van relevante trefwoorden, kunnen ertoe leiden dat wijzigingen in de positie van de URL in de organische zoekopdracht worden gewijzigd. [!DNL Adobe] adviseert dat u met uw partner SEO als deel van uw het testen protocol in dienst neemt.

## Bots {#bots}

Adobe [!DNL Target] gebruikt de [DeviceAtlas](https://deviceatlas.com/device-data/user-agent-tester/) metrische &quot;isRobot&quot;om bekende bots te ontdekken die op het Koord van de Agent van de Gebruiker worden gebaseerd die in de Kopbal van het Verzoek wordt overgegaan.

>[!NOTE]
>
> Voor [!DNL Server-Side] verzoeken, de waarde die in [Context-knooppunt van verzoek](https://developers.adobetarget.com/api/delivery-api/#tag/Delivery-API) wordt gegeven belangrijkheid over het Koord van de Agent van de Gebruiker voor beide opsporing.

Verkeer dat door een bot wordt gegenereerd, wordt nog steeds aangeboden. Bots worden als een normale gebruiker behandeld om ervoor te zorgen dat [!DNL Target] is in overeenstemming met de richtsnoeren van de SEO. Door beide verkeer te gebruiken, kunnen A/B-tests of verpersoonlijkingsalgoritmen scheeftrekken als ze worden behandeld als normale gebruikers. Daarom als een bekende bot in uw wordt ontdekt [!DNL Target] activiteit, wordt het verkeer lichtjes verschillend behandeld. Het verwijderen van beide verkeer zorgt voor een nauwkeurigere meting van de gebruikersactiviteit.

Specifiek, voor bekend bot verkeer [!DNL Target] niet:

* Een bezoekersprofiel maken of ophalen
* Profielkenmerken vastleggen of profielscripts uitvoeren
* Opzoeken [!DNL Adobe Audience Manager] (AAM) segmenten (indien van toepassing)
* Gebruik zowel verkeer in modellering als het dienen van gepersonaliseerde inhoud voor [!UICONTROL Recommendations], [!UICONTROL Auto-Target], [!UICONTROL Automated Personalization], of [!UICONTROL Auto-Allocate] activiteiten
* Een activiteitenbezoek aanmelden voor rapportage
* Loggegevens die naar de [!DNL Adobe Experience Cloud] platform

Voor bekend beide verkeer bij gebruik [!UICONTROL Analytics for Target] (A4T), [!DNL Target] niet:

* Gebeurtenissen verzenden naar [!DNL Analytics]

Voor bekend bot verkeer wanneer het gebruiken van client_side registreren, [!DNL Target] retourneert niet:

* tnta-lading
