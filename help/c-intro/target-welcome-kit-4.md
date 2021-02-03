---
keywords: welkomstkit;doel welkomstkit;intro;introductie;aan de slag
description: Adobe Target-welkomstkit - Hoofdstuk 4 - Tips voor het gebruik van Target
title: Welkomstkit - Hoofdstuk 4 - Tips voor het gebruik van het doel
feature: Overview
translation-type: tm+mt
source-git-commit: 48b94f967252f5ddb009597456edf0a43bc54ba6
workflow-type: tm+mt
source-wordcount: '2887'
ht-degree: 0%

---


# Hoofdstuk 4: Tips voor het gebruik van Doel

Op basis van ons werk met veel [!DNL Target] gebruikers hebben we manieren gezien waarop u meer waarde kunt krijgen van uw [!DNL Target]-oplossing. Deze zijn samengevat in de vele tips die we in dit hoofdstuk hebben opgenomen. Hoewel u niet bereid zou kunnen zijn om al deze ideeën onmiddellijk te gebruiken, houd aan deze lijst. Hoe meer ervaring u krijgt met de oplossing en hoe meer programma&#39;s er rijpen, des te meer u zult zien hoe deze tips u kunnen helpen om meer te bereiken met [!DNL Target].

## Tip 1: Vergroot de personalisatie door het profiel van de bezoeker te verhogen met extra gegevens.

U kunt ervaringen met [!DNL Target] gegevens direct uit de doos personaliseren. Maar verpersoonlijker door uw eigen gegevens in de mengeling toe te voegen. U kunt uw profiel uitbreiden met historische gegevens van [!DNL Adobe Analytics] en realtime gegevens van [!DNL Adobe Audience Manager]. U kunt de Attributen van de Klant, een eigenschap binnen de de kerndienst van Mensen in [!DNL Adobe Experience Cloud], ook gebruiken om CRM gegevens, de gegevens van de tweede partner, en derde gekochte gegevens in [!DNL Target] gemakkelijk te brengen.

U kunt bijvoorbeeld aankoopgegevens van uw verkooppunt koppelen aan een bezoekersprofiel. Hiertoe maakt u gewoon een CSV-bestand met maximaal 200 offlinevariabelen en uploadt u het bestand rechtstreeks naar [!DNL Adobe Experience Cloud] via een bestandsupload of gebruikt u FTP om het bestand regelmatig te hosten en te plannen dat het wordt bijgewerkt. Als uw klantkenmerken zich in [!DNL Adobe Experience Cloud] bevinden, kunt u ze toewijzen aan [!DNL Experience Cloud]-oplossingen zoals [!DNL Adobe Analytics] en [!DNL Target], waar ze beschikbaar zijn voor analyse, tests en personalisatie.

Zie [Aangepaste kenmerken](https://experienceleague.adobe.com/docs/target/using/audiences/visitor-profiles/working-with-customer-attributes.html) voor stapsgewijze instructies.

**Goed te weten**: Omdat  [!DNL Target] het een open en agnostisch platform is dat goed met verschillende technologieën werkt, kunt u CRM of gekochte gegevens op vele verschillende manieren toevoegen. Dat betekent u een methode kunt kiezen die het beste voor uw organisatie werkt.

Zie [Methoden om gegevens in Doel te krijgen](/help/c-implementing-target/c-considerations-before-you-implement-target/c-methods-to-get-data-into-target/methods-to-get-data-into-target.md) voor meer informatie.

## Tip 2: Personaliseer dieper door het publiek van het Doel met andere publiek van Adobe Experience Cloud te mengen.

Het mengen van publiek dat in verschillende [!DNL Adobe Experience Cloud] oplossingen leeft kan u een veel breder begrip van uw klanten, evenals de capaciteit geven om zich aan te passen dieper. Hoewel [!DNL Target] realtime publieksgegevens biedt, levert [!DNL Adobe Analytics] bijvoorbeeld historische publieksgegevens. Het combineren van twee kan u helpen identificeren wanneer het gedrag van een klant verenigbaar is, en wanneer er een kans zou kunnen zijn om op een nieuw gedrag te handelen. Klik op het vervolgkeuzemenu naast &quot;Alle bezoekers&quot; wanneer u een activiteit maakt. Schakel vervolgens de selectievakjes van maximaal twintig soorten publiek in, klik op Meerdere soorten publiek combineren en klik op Opslaan.

Zie [Meerdere doelgroepen combineren](/help/c-target/combining-multiple-audiences.md) voor stapsgewijze instructies.

**Goed te weten**:  [!DNL Adobe Audience Manager] publiek is  [!DNL Target] automatisch beschikbaar. Maar [!DNL Adobe Analytics] het delen van het publiek vereist een beetje handopstelling. Schakel gewoon het vakje &quot;Make this an Experience Cloud publiek&quot; in tijdens het publieksopbouwproces in [!DNL Analytics]. Klik vervolgens vanuit [!DNL Target] op &quot;Experience Cloud-publiek importeren&quot;.

## Tip 3: Exporteer gegevens van Target voor gebruik met gereedschappen van derden.

Met reactietokens, kunnen de beheerders gegevens uit [!DNL Target] en in derdehulpmiddelen gemakkelijk krijgen. Dit kan handig zijn als u gegevens wilt toevoegen aan gegevens die zijn verzameld in een enquêteprogramma. Als een enquête bijvoorbeeld een voorbeeld toont van een populatie met een score van &quot;9&quot; en een andere met een score van &quot;4&quot; toont, kunt u uw gegevens gebruiken om te zien wie ervaring A heeft gezien en wie ervaring B heeft gezien. U kunt reactietokens ook gebruiken om [!DNL Target] gegevens naar uw intern gegevenspakhuis uit te voeren. Klik eenvoudig &quot;Beleid,&quot;dan knevel de schakelaar naast het gewenste Symbolische van de Reactie aan op positie. Maak vervolgens een activiteit. De gegevens kunnen vervolgens naar de externe leverancier worden overgedragen. U kunt controleren dat [!DNL Target] de gegevens gebruikend het zuiveren hulpmiddelen uitvoert.

Zie [Reactietokens](/help/administrating-target/response-tokens.md) voor stapsgewijze instructies.

**Nuttige tip**: Alvorens een beheerder een reactietoken kan activeren verbonden aan een derde, moet een ontwikkelaar aan opstelling een partnerschap met dat derdebedrijf.

Zie [Reactietokens](/help/administrating-target/response-tokens.md) voor stapsgewijze instructies.

**Doe dit eerst**: Zorg dat u versie 1.js of hoger van versie 1.1 gebruikt. Als u een vorige versie gebruikt, ziet u de reactietokens, maar at.js kan deze niet gebruiken.

## Tip 4: Bouw publiek van deze zeer belangrijke variabelen om de waarde van uw activiteit te verhogen.

Houd bij het opbouwen van doelgroepen voor het maken van promoties en aanbiedingen eerst rekening met de volgende variabelen:

* Gedrag. Patronen voor bezoeken aan sites en aankooppatronen
* Referrer. Verwijzen naar sites en campagnes
* Tijdelijk. Dag- en weekdagen en seizoensfactoren
* Off line. Bezoek- en aankooppatronen in fysieke winkels
* Omgeving. Land van oorsprong, besturingssysteem, browsertype

## Tip 5: Geef gebruikers het toegangsniveau dat ze nodig hebben om hun werk te doen.

Maak het gemakkelijk om met de gegevens van uw organisatie te werken terwijl het houden van het veilig. [!DNL Target Premium] staat beheerders toe om het niveau van toegang te controleren die aan verschillende interne en externe teams wordt gegeven.

Zie [Machtigingen voor Enterprise-gebruikers](/help/administrating-target/c-user-management/property-channel/property-channel.md) voor meer informatie.

**Nuttige tip**: Wanneer u gebruikers toevoegt en de naam van een teamlid nog niet aan uw organisatie is toegevoegd, bijvoorbeeld in het geval van een medewerker van een externe organisatie, wordt door het invoeren van het e-mailadres en wachtwoord een e-mailuitnodiging voor deelname aan de werkruimte van een team geactiveerd.

Doelstandaard gebruiken? U kunt nog [drie niveaus van toegang](/help/administrating-target/c-user-management/c-user-management/user-management.md) voor uw gebruikers met read-only, redacteur, en goedkeurende rollen toewijzen!

## Tip 6: Ontdek hoe een aanbieding over een klantenreis door het over elke pagina in de reis te testen presteert.

Ontdek hoe een aanbieding, zoals gratis verzending, functioneert tijdens een reis van de klant die op meerdere pagina&#39;s van uw website plaatsvindt.

Zie [Activiteiten van meerdere pagina&#39;s](/help/c-experiences/c-visual-experience-composer/multipage-activity.md) voor stapsgewijze instructies.

**Nuttige tip**: Als u de URL wijzigt nadat u een paginabereik hebt opgegeven, wordt de ervaring opnieuw ingesteld. Dit betekent dat de opgegeven variaties niet meer worden weergegeven. Als u de URL moet wijzigen, vergeet dan niet de ervaring opnieuw te definiëren.

## Tip 7: Test een aanbieding met verschillende soorten publiek om te zien of het publiek verschillende voorkeuren heeft.

Met de Versies van de Ervaring, kunt u één test met variaties voor zoveel publiek in werking stellen als u houdt van. U kunt bijvoorbeeld een banneradvertentie maken die gratis verzending biedt—met afbeeldingen en valutamaraties voor klanten in de VS, het VK en de VS—zonder tests voor drie verschillende soorten publiek uit te voeren.

Zie voor [Meerdere ervaringspubliek in een A/B-test](/help/c-activities/t-test-ab/t-test-create-ab/target-experience-to-multiple-audiences.md) en [Ervaar versies in Adobe Target](https://helpx.adobe.com/target/how-to/experience-versions.html?playlist=/ccx/v1/collection/product/target/seg-%20ment/business-practitioners/explevel/beginner-adls/applaunch/how-to-2/collection.ccx.js?ref=helpx.adobe.com) voor stapsgewijze instructies.

## Tip 8: Bespaar tijd door activiteiten op vergelijkbare pagina&#39;s te herhalen.

Maak een variatie op één webpagina, zoals een nieuwe knopkleur, en pas deze automatisch toe op alle pagina&#39;s met dezelfde sjabloon. U kunt pagina&#39;s opgeven of de variaties toepassen op alle vergelijkbare pagina&#39;s op uw website.

Zie [Dezelfde ervaring opnemen op vergelijkbare pagina&#39;s](/help/c-experiences/c-visual-experience-composer/temtest.md) voor stapsgewijze instructies.

## Tip 9: Verminder de rommel in uw Audience Library door eenmalig publiek te maken.

Als u zich richt op een segment waarvan u weet dat het niet opnieuw wordt bedoeld, bijvoorbeeld klanten die worden beïnvloed door een onverwachte weersomstandigheden, kunt u de taak eenvoudig uitvoeren door een publiek te maken dat de taak slechts voor één keer uitvoert, zonder dat u de Audience Library overzichtelijker hoeft te maken. Hierdoor is het gemakkelijker om steeds weer een publiek te vinden dat u gebruikt.

Zie [Een alleen-activiteit publiek maken](/help/c-target/creating-activity-only-audience.md) voor stapsgewijze instructies.

**Hoogst gevraagde capaciteit**: Onze klanten hebben ons gevraagd het mogelijk te maken om gebruikers voor eenmalig gebruik niet automatisch op te slaan in de Audience Library. Nu hoeven ze niet langer handmatig het publiek te verwijderen om hun bibliotheken te organiseren.

## Tip 10: Voer eenvoudige tests sneller uit door ze niet door het standaard QA-proces te laten lopen.

Er is niets erger dan een activiteit klaar om te gaan en dan weken te wachten tot het het standaard QA proces voltooit. U kunt de meeste activiteiten QA door eenvoudig rond een paar verbindingen QA aan collega&#39;s over te gaan om hen op diverse browsers te proberen. U zult hoogstwaarschijnlijk meer QA tests voor inspanningen willen doen die dramatisch plaatsfunctie veranderen, maar in werkelijkheid, zou u minder van die activiteiten en veel meer van de meer basisactiviteiten moeten hebben. Het toevoegen van betere rechtencontroles zodat minder mensen dingen volledig kunnen doordringen voegt ook zinvolle grenzen toe en laat u doen wat u nodig hebt zonder snelheid en efficiency te offeren. Een andere optie is een aangewezen middel van IT te hebben om tijdig toezicht op het proces van QA te verstrekken.

Zie [Activiteit QA](/help/c-activities/c-activity-qa/activity-qa.md) voor stapsgewijze instructies.

## Tip 11: Voer tests uit op pagina&#39;s met veel verkeer, zodat ze sneller statistisch significant worden.

Vele marketers lanceren optimaliseringsprogramma&#39;s voor publiekssegmentatie en richten zonder te controleren of de getoonde verkeersniveaus en het publiek significante resultaten binnen het het testen tijdkader voor hun optimalisering en omzettingsdoelstellingen zullen verstrekken. Om deze gemeenschappelijke fout te vermijden, beantwoord vooraf deze vragen:

* Hoeveel dagelijkse unieke bezoekers heeft de pagina?
* Wat is de omrekeningskoers voor de pagina?
* Hoe lang verwacht u dat u de test moet uitvoeren voordat u deze met vertrouwen volledig kunt noemen?

**Nuttige tip**: Gebruik de  [calculator voor de ](https://docs.adobe.com/content/target-microsite/testcalculator.html) monstergrootte van het Doel als hulpmiddel om de steekproefgrootte te bepalen nodig voor een succesvolle test.

## Tip 12: Ontwerp eenvoudiger tests om ervoor te zorgen dat u deze kunt maken en implementeren.

Na het overwegen van alle aspecten van hoe te om een test te ontwerpen, kan een plan zeer complex worden. Gebaseerd op waar uw zaken met het testen zijn, en de capaciteit van uw groep om, de resultaten te ontwerpen, uit te voeren en te analyseren, bepalen als de test te ambitieus lijkt. Als dat het geval is, moet zij bereid zijn de reikwijdte en de complexiteit ervan te beperken. Het is beter om klein te beginnen dan de test helemaal niet uit te voeren. U kunt geen indrukwekkende lift leveren als u de test nooit start. Het is belangrijk om de aspiraties van het team in evenwicht te brengen met de realiteiten van uw middelen en capaciteiten.

## Tip 13: Breek complexe tests in kleinere testactiviteiten om ze haalbaar te maken.

In plaats van één grote test met meerdere variabelen en complexe ontwikkeling te ontwikkelen, ontwikkelt u een minder complexe reeks kleinere tests met minimale variabelen. Dit maakt een beter inzicht in de testprestaties mogelijk op basis van specifieke variabelen. Het vermindert ook mogelijke technische kwesties die met de ontwikkeling van grotere projecten gepaard gaan.

![Afbeelding van complexe tests breken](/help/c-intro/assets/break-complex-tasks.png)

## Tip 14: Maximaliseer uw testimpact door dichter aan het eind van de conversietrechter te testen.

Testen net als de pagina waarop bezoekers op Aankoop voltooien, Toepassing verzenden of op een andere manier een conversie uitvoeren klikken, levert meestal de meest onbruikbare resultaten op. Bezoekers die het einde van de trechter bereiken, zijn beter gekwalificeerd, hebben meer tijd geïnvesteerd en zijn klaar om te kopen. Het testen van inzichten in hun voorkeuren en acties kan u dus helpen rendabele wijzigingen aan te brengen. Omdat pagina&#39;s op het aankooppad van essentieel belang zijn voor de conversiekoersen, moeten de tests die op deze pagina&#39;s worden uitgevoerd, worden gesocialiseerd naar de belangrijkste belanghebbenden voordat ze worden uitgerold.

![Conversietrechter-illustratie](/help/c-intro/assets/conversion-funnel.png)

## Tip 15: Werk uw tests voortdurend bij om herhalende verbeteringen aan te brengen.

Als uw hypothese niet klopt, denk dan aan manieren om uw test te verbeteren. Houd er rekening mee dat zelfs als geen van de geteste ervaringen beter is, uw experiment geen tijdverspilling was. Een geslaagde test betekent niet altijd een verhoging van de inkomsten of omzettingen. Als de test uw hypothese daadwerkelijk ondersteunt, bent u op weg naar de ontwikkeling van een algemene theorie. Maar zelfs als u een duidelijk winnend resultaat hebt, stop daar niet. Te vaak maken marketeers de fout om eens te testen en dan op die resultaten te bankieren zonder echt te begrijpen wat tot het succes heeft geleid. In plaats daarvan, ben van plan om op die resultaten te herhalen om te weten te komen waarom de front-runner vooruit was. Dit zal u aan diepere inzichten leiden die u in toekomstige campagnes kunt gebruiken.

## Tip 16: Vergelijk tests en verpersoonlijkingsactiviteiten voor ideeën om het richten te verbeteren.

Het vergelijken van de omzettingsprestaties van verschillende soorten publiek binnen verschillende tests bij verschillende plaatsen kan helpen de optimaliseringsstrategie van een bedrijf concentreren en verfijnen. Gebruik testvergelijkingen om te bepalen welke doelgroepen het meest geschikt zijn om te testen, welke doelgerichte ervaringen moeten krijgen en welke soorten ervaringen het meest waarschijnlijk een reactie zullen opleveren.

Een klant van financiële services voerde bijvoorbeeld een promotiecampagne uit voor een creditcard die professionele prikkels voor sportevenementen omvatte. Door de gedeeltelijke factoriële multivariate tests van zijn landingspagina&#39;s, kon de klant het overseinen over creditcardvoordelen met sportieve prikkels optimaliseren om verschillend publiek van zijn klantenbasis te richten. Dankzij deze aanpak kon het bedrijf profiteren van de conversie en deze maximaliseren tijdens een tijdgevoelig venster rond een belangrijk sportevenement.

## Tip 17: Maak tests nuttig door hen slechts te lanceren als u weet u van de gegevens kunt handelen.

Een test is zinloos als u niet precies weet hoe u op de gegevens gaat werken. Dit omvat het weten van uw belangrijkste succes metrisch, wat moet gebeuren om een winnaar te duwen, hoe u op testresultaten zult volgen, en wat u met de publieksinformatie zult doen. Voor een snelle en geslaagde test is het van essentieel belang dat elke bij de test betrokken groep (ontwikkelaars, creatieven, testspecialisten en anderen) zich bewust is van zijn rol voordat de test wordt gestart.

## Tip 18: Voordat u een test start, moet u ervoor zorgen dat het bedrijf de winnaar verder duwt.

Succesvolle optimalisatieorganisaties geloven in het concept van testen en begrijpen dat hun professionele meningen over welke ervaring de test zal winnen niet altijd waar blijken te zijn. Ze bepalen de winnaar op basis van een solide basis van gegevens en zijn graag bereid om de winnende ervaring actief te maken nadat de resultaten zijn bereikt, zelfs als deze niet in overeenstemming is met hun verwachtingen of als het tegenstrijdig lijkt.

Zo heeft een klant van de gezondheidszorg van Adobe onlangs de waarde van het testen aangetoond door te laten zien hoe een hoofdbanner die het team als een slam had beschouwd een negatief effect had op de conversie. Als uw organisatie het testen nog niet volledig heeft geaccepteerd, kunt u het beste eerst eenvoudigere, kleinere tests uitvoeren, zodat wijzigingen in de testresultaten stapsgewijs kunnen worden uitgevoerd.

## Tip 19: Laat iedereen weten dat u een test hebt gestart om zorgen te voorkomen wanneer de site verandert.

Één van de voordelen om uw activiteiten op te zetten om parameters te gebruiken QA is dat u die verbindingen met iedereen op uw team kunt delen. U maakt meer mensen bewust van de activiteit en zorgt ervoor dat ze er niet van uitgaan dat de site niet goed werkt wanneer ze op een testvariant reageren.

Nadat u uw tests voltooit, helpen het communiceren campagnelanceringen, testresultaten, en vooral geleerde lessen u bewustzijn van en interesse in de testresultaten opbouwen. Door de resultaten met iedereen in de organisatie te delen, voorkomt u ook dat u een hypothese opnieuw test, leert u iedereen wat werkt en helpt u hen fundamenteel hun eigen ideeën uit te dagen over wat werkt op basis van wat u hebt gevonden. Het is raadzaam een sjabloon voor te bereiden die u telkens gebruikt voor het delen van uw bevindingen en belangrijke lessen.
Dan denk na creërend een sharable boek of dek van Microsoft PowerPoint dat deze lessen cumulatief vangt.

## Tip 20: Tik op mobiele functionaliteit om meer innovatieve mobiele activiteiten te maken.

De gebruikers van tablets en smartphones moeten zich richten op aanraakbesturingselementen als de primaire bezoekersinteractie in plaats van op muisklikken en toetsenbordbesturing. Maak gebruik van de besturingselementen voor mobiele schermen, zoals vegen met vingers, aanraken, slepen, knijpen en zoomen. Gebruik eenvoudige, grote knoppen om interacties en navigatie aan te geven, zoals een groot winkelwagentje of een knop voor het afspelen van video. Als het ontwerpen voor mobiele detailhandel, rijke productvisualisatie omvat die voor het apparatentype wordt geoptimaliseerd. Zoek altijd naar mogelijkheden om de gebruikerservaring te verplaatsen naar ingesloten, grote kijkers of interactief zoomen en pannen op volledig scherm, 360 graden draaien en verbeterde videofunctionaliteit.

## Tip 21: Mobiele bezoekers helpen bij het zoeken naar wat ze willen door de zoekfunctie voor mobiele apparaten te optimaliseren.

Mobiele gebruikers hebben een hoge intentie. De meesten van hen gebruiken onderzoek alvorens zij om het even wat anders op e-commercesites doen, die mobiele plaatsonderzoekoptimalisering cruciaal maken. Gebruik expliciete navigatiemogelijkheden om gemakkelijk te kunnen bladeren om de optimalisatie van zoekprogramma&#39;s voor mobiele apparaten te verbeteren. Implementeer automatisch voorstellen en automatisch corrigeren in de invoervakken voor zoekopdrachten om de moeilijkheid van mobiele typen te verhelpen. Verstrek dwingende, relevante onderzoeksresultaten die voor het schermgrootte en plaats worden geoptimaliseerd.

## Tip 22: Bereik mobiele doelgroepen beter met tijd-van-dag doelgericht voor mobiele SEM-campagnes.

Begrijp hoe en wanneer u uw publiek kunt bereiken en hoe u uw dagelijkse reclameuitgaven beter kunt beheren door uw mobiele campagnes &#39;dag te parseren&#39; in verschillende segmenten door de dag heen.

Veel marketeers maken de fout dat ze niet genoeg geld toewijzen om dat deel van de stem te laten horen in de uren dat het gebruik van bepaalde apparaten het zwaarst is, waardoor er veel inkomsten en koppen op tafel blijven liggen.

Het tabletgebruik spiekt bijvoorbeeld meestal in de avonduren en veel gebruikers bladeren terwijl ze tv kijken. Smartphonegebruikers hebben daarentegen doorgaans onderweg toegang tot inhoud. De piekomzettingstijden variëren ook per industrie, zodat is het belangrijk om te begrijpen wanneer uw unieke klanten het meest waarschijnlijk zullen handelen.

## Houd rekening met

Overweeg de volgende ideeën voordat we verdergaan met het volgende hoofdstuk: &quot;Inspiratie voor test- en personalisatieactiviteiten.&quot;

### Als je je tests maakt, versier dan niet, wees bewust.

* Stel de stroom in met doelbewuste oogpaden die zijn gericht op conversiepunten.
* Zorg ervoor dat u uw onroerend goed in uw voordeel gebruikt.
* Gebruik Image Focus om ervoor te zorgen dat afbeeldingen geen decoratie zijn, maar voor u werken.
* Verminder rommelig, wrijving, en vervagen met Vereenvoudigd Exemplaar.
* Ben zeker u efficiënte Vraag aan Acties hebt wanneer u de gebruiker nodig hebt om actie te voeren.
* Voeg waar mogelijk geloofwaardigheid toe via door gebruikers gegenereerde inhoud.

### Vereenvoudig uw website.

* Gebruikers niet laten lezen. Ze zullen dat niet doen.
* Scannen is gemakkelijk.
* Gebruik blokken met opsommingstekens.
* Zorg ervoor dat uw kopie een duidelijk, opeenvolgend gedachteproces volgt.

### Gebruik efficiënte Vraag aan Acties (CTAs)

* Zet jezelf in de schoenen van de klant.
* Gebruik een taal die is georiënteerd op handelingen.
* Denk aan de motivatie voor conversie.
* Het omzettingsresultaat aanpakken.
* Zorg ervoor dat CTA&#39;s zichtbaar zijn!