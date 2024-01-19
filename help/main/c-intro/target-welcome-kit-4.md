---
keywords: welkomstkit;doel welkomstkit;intro;introductie;aan de slag
description: Lees tips van ons panel van experts over het gebruik van Adobe [!DNL Target] als onderdeel van uw test- en personaliseringsinspanningen.
title: Waar kan ik tips en trucs voor het gebruiken van Doel vinden?
feature: Overview
exl-id: 86437ad1-83ea-4670-b503-6c3c1fff0c16
source-git-commit: fe1e97710e7692ba7724103853ed7438c3f361b1
workflow-type: tm+mt
source-wordcount: '2890'
ht-degree: 0%

---

# Hoofdstuk 4: Tips voor het gebruik van Doel

Gebaseerd op ons werk met veel [!DNL Target] gebruikers, hebben wij manieren gezien die u meer waarde van uw kunt krijgen [!DNL Target] oplossing. We hebben die samengevat in de vele tips die we in dit hoofdstuk hebben opgenomen. Hoewel u niet bereid zou kunnen zijn om al deze ideeën onmiddellijk te gebruiken, houd aan deze lijst. Hoe meer ervaring u krijgt met de oplossing en hoe meer uw programma rijpt, des te meer u zult zien hoe deze tips u kunnen helpen meer te bereiken met [!DNL Target].

## Tip 1: Vergroot de personalisatie door het profiel van de bezoeker te verhogen met extra gegevens.

U kunt ervaringen personaliseren met [!DNL Target] gegevens direct uit het vak. Maar verpersoonlijker door uw eigen gegevens in de mengeling toe te voegen. U kunt uw profiel uitbreiden met historische gegevens uit [!DNL Adobe Analytics] en real-time gegevens van [!DNL Adobe Audience Manager]. U kunt ook Customer Attributes gebruiken, een functie binnen de People core-service in [!DNL Adobe Experience Cloud]om CRM-gegevens, gegevens van partners van derden en door derden aangekochte gegevens eenvoudig naar [!DNL Target].

U kunt bijvoorbeeld aankoopgegevens van uw verkooppunt koppelen aan een bezoekersprofiel. Hiertoe maakt u gewoon een CSV-bestand met maximaal 200 offlinevariabelen en uploadt u het rechtstreeks naar [!DNL Adobe Experience Cloud] via een bestandsupload of gebruik FTP om het bestand regelmatig te hosten en te plannen. Zodra uw Attributen van de Klant in [!DNL Adobe Experience Cloud], kunt u deze toewijzen aan [!DNL Experience Cloud] oplossingen zoals [!DNL Adobe Analytics] en [!DNL Target] waar zij voor analyse, het testen, en verpersoonlijking beschikbaar zullen zijn.

Zie [Aangepaste kenmerken](https://experienceleague.adobe.com/docs/target/using/audiences/visitor-profiles/working-with-customer-attributes.html) voor stapsgewijze instructies.

**Goed om te weten**: omdat [!DNL Target] is een open en agnostisch platform dat goed werkt met verschillende technologieën, kunt u CRM of gekochte gegevens op verschillende manieren toevoegen. Dat betekent u een methode kunt kiezen die het beste voor uw organisatie werkt.

Zie [Methoden om gegevens op te halen in Doel](https://experienceleague.adobe.com/docs/target-dev/developer/implementation/methods/methods-to-get-data-into-target.html){target=_blank} voor meer informatie .

## Tip 2: Personaliseer dieper door overvloeien [!DNL Target] publiek met ander publiek in Adobe Experience Cloud.

Het mengen publiek dat in verschillende leeft [!DNL Adobe Experience Cloud] de oplossingen kunnen u een veel breder inzicht in uw klanten, evenals de capaciteit geven om zich dieper te personaliseren. Bijvoorbeeld, hoewel [!DNL Target] biedt realtime publieksgegevens; [!DNL Adobe Analytics] biedt gegevens over historische doelgroepen. Het combineren van twee kan u helpen identificeren wanneer het gedrag van een klant verenigbaar is, en wanneer er een kans zou kunnen zijn om op een nieuw gedrag te handelen. Klik op het vervolgkeuzemenu naast &quot;Alle bezoekers&quot; wanneer u een activiteit maakt. Schakel vervolgens de selectievakjes van maximaal twintig soorten publiek in, klik op Meerdere soorten publiek combineren en klik op Opslaan.

Zie [Meerdere doelgroepen combineren](/help/main/c-target/combining-multiple-audiences.md) voor stapsgewijze instructies.

**Goed om te weten**: [!DNL Adobe Audience Manager] publiek is beschikbaar in [!DNL Target] automatisch. Maar [!DNL Adobe Analytics] het delen van het publiek vereist een beetje handopstelling. Schakel het selectievakje &#39;Dit publiek maken tot Experience Cloud&#39; in tijdens het genereren van het publiek in [!DNL Analytics]. Vervolgens vanaf [!DNL Target], klikt u op &#39;Experience Cloud-publiek importeren&#39;.

## Tip 3: gegevens exporteren uit [!DNL Target] te gebruiken met hulpmiddelen van derden.

Met respontokens kunnen beheerders eenvoudig gegevens ophalen uit [!DNL Target] en in hulpmiddelen van derden. Dit kan handig zijn als u gegevens wilt toevoegen aan gegevens die zijn verzameld in een enquêteprogramma. Als een enquête bijvoorbeeld een voorbeeld toont van een populatie met een score van &quot;9&quot; en een andere met een score van &quot;4&quot; toont, kunt u uw gegevens gebruiken om te zien wie ervaring A heeft gezien en wie ervaring B heeft gezien. U kunt ook reactietokens gebruiken om te exporteren [!DNL Target] gegevens aan uw intern gegevenspakhuis. Klik eenvoudig &quot;Beleid,&quot;dan knevel de schakelaar naast het gewenste Symbolische van de Reactie aan op positie. Maak vervolgens een activiteit. De gegevens kunnen vervolgens naar de externe leverancier worden overgedragen. U kunt controleren of [!DNL Target] exporteert de gegevens met behulp van foutopsporingsgereedschappen.

Zie [Reactietokens](/help/main/administrating-target/response-tokens.md) voor stapsgewijze instructies.

**Nuttige tip**: Voordat een beheerder een antwoordtoken kan activeren dat is gekoppeld aan een derde, moet een ontwikkelaar een partnerschap instellen met dat externe bedrijf.

Zie [Reactietokens](/help/main/administrating-target/response-tokens.md) voor stapsgewijze instructies.

**Doe dit eerst**: Zorg dat u versie 1.js of hoger van at.js gebruikt. Als u een vorige versie gebruikt, zult u de reactietokens zien, maar at.js zal niet hen kunnen gebruiken.

## Tip 4: Bouw het publiek op basis van deze sleutelvariabelen om de waarde van uw activiteit te verhogen.

Houd bij het opbouwen van doelgroepen voor het maken van promoties en aanbiedingen eerst rekening met de volgende variabelen:

* Gedrag. Patronen voor bezoeken aan sites en aankooppatronen
* Referrer. Verwijzen naar sites en campagnes
* Tijdelijk. Dag- en weekdagen en seizoensfactoren
* Off line. Bezoek- en aankooppatronen in fysieke winkels
* Omgeving. Land van oorsprong, besturingssysteem, browsertype

## Tip 5: geef gebruikers het toegangsniveau dat ze nodig hebben om hun werk te doen.

Maak het gemakkelijk om met de gegevens van uw organisatie te werken terwijl het houden van het veilig. [!DNL Target Premium] staat beheerders toe om het niveau van toegang te controleren die aan verschillende interne en externe teams wordt gegeven.

Zie [Machtigingen voor Enterprise-gebruikers](/help/main/administrating-target/c-user-management/property-channel/property-channel.md) voor meer informatie .

**Nuttige tip**: Als u gebruikers toevoegt en de naam van een teamlid nog niet eerder aan uw organisatie is toegevoegd, bijvoorbeeld in het geval van een medewerker van een externe organisatie, wordt een e-mailuitnodiging voor deelname aan de werkruimte van een team geactiveerd wanneer u hun e-mailadres en wachtwoord invoert.

Doelstandaard gebruiken? U kunt [drie toegangsniveaus toewijzen](/help/main/administrating-target/c-user-management/c-user-management/user-management.md) voor uw gebruikers met read-only, redacteur, en goedkeurende rollen!

## Tip 6: Ontdek hoe een aanbieding over een klantenreis door het over elke pagina in de reis te testen presteert.

Ontdek hoe een aanbieding, zoals gratis verzending, functioneert tijdens een reis van de klant die op meerdere pagina&#39;s van uw website plaatsvindt.

Zie [Meerdere pagina&#39;s](/help/main/c-experiences/c-visual-experience-composer/multipage-activity.md) voor stapsgewijze instructies.

**Nuttige tip**: Als u de URL wijzigt nadat u een paginabereik hebt opgegeven, wordt de ervaring opnieuw ingesteld. Dit betekent dat de opgegeven variaties niet meer worden weergegeven. Als u de URL moet wijzigen, vergeet dan niet de ervaring opnieuw te definiëren.

## Tip 7: test een aanbieding met verschillende soorten publiek om te ontdekken of het publiek verschillende voorkeuren heeft.

Met de Versies van de Ervaring, kunt u één test met variaties voor zoveel publiek in werking stellen als u houdt van. U kunt bijvoorbeeld een banneradvertentie maken die gratis verzending biedt—met afbeeldingen en valutamaraties voor klanten in de VS, het VK en de VS—zonder tests voor drie verschillende soorten publiek uit te voeren.

Zie voor [Meerdere ervaringsdoelgroepen in een A/B-test](/help/main/c-activities/t-test-ab/t-test-create-ab/target-experience-to-multiple-audiences.md) en [Ervaar versies in Adobe Target](https://helpx.adobe.com/target/how-to/experience-versions.html?playlist=/ccx/v1/collection/product/target/seg-%20ment/business-practitioners/explevel/beginner-adls/applaunch/how-to-2/collection.ccx.js?ref=helpx.adobe.com) voor stapsgewijze instructies.

## Tip 8: Bespaar tijd door activiteiten op vergelijkbare pagina&#39;s te repliceren.

Maak een variatie op één webpagina, zoals een nieuwe knopkleur, en pas deze automatisch toe op alle pagina&#39;s met dezelfde sjabloon. U kunt pagina&#39;s opgeven of de variaties toepassen op alle vergelijkbare pagina&#39;s op uw website.

Zie [Dezelfde ervaring opnemen op vergelijkbare pagina&#39;s](/help/main/c-experiences/c-visual-experience-composer/temtest.md) voor stapsgewijze instructies.

## Tip 9: Verminder de rommel in uw Audience Library door eenmalig publiek te maken.

Als u een segment richt weet u niet zal richten opnieuw-voor voorbeeld, kunnen de klanten die door onverwacht weer gebeurtenis-creërend een eenmalig gebruikspubliek worden beïnvloed u helpen de baan krijgen gedaan zonder het toevoegen van rommelige aan uw Bibliotheek van de Publiek. Hierdoor is het gemakkelijker om steeds weer een publiek te vinden dat u gebruikt.

Zie [Een alleen-activiteitpubliek maken](/help/main/c-target/creating-activity-only-audience.md) voor stapsgewijze instructies.

**Hoogst gevraagde capaciteit**: Onze klanten hebben ons gevraagd het mogelijk te maken om gebruikers voor eenmalig gebruik niet automatisch op te slaan in de Audience Library. Nu hoeven ze niet langer handmatig het publiek te verwijderen om hun bibliotheken te organiseren.

## Tip 10: Voer eenvoudige tests sneller uit door ze niet door het standaard QA-proces te laten lopen.

Er is niets erger dan een activiteit klaar om te gaan en dan weken te wachten tot het het standaard QA proces voltooit. U kunt de meeste activiteiten QA door eenvoudig rond een paar verbindingen QA aan collega&#39;s over te gaan om hen op diverse browsers te proberen. U zult hoogstwaarschijnlijk meer QA tests voor inspanningen willen doen die dramatisch plaatsfunctie veranderen, maar in werkelijkheid, zou u minder van die activiteiten en veel meer van de meer basisactiviteiten moeten hebben. Het toevoegen van betere rechtencontroles zodat minder mensen dingen volledig kunnen doordringen voegt ook zinvolle grenzen toe en laat u doen wat u nodig hebt zonder snelheid en efficiency te offeren. Een andere optie is een aangewezen middel van IT te hebben om tijdig toezicht op het proces van QA te verstrekken.

Zie [Activiteit QA](/help/main/c-activities/c-activity-qa/activity-qa.md) voor stapsgewijze instructies.

## Tip 11: Voer tests uit op pagina&#39;s met veel verkeer, zodat ze sneller statistisch significant worden.

Vele marketers lanceren optimaliseringsprogramma&#39;s voor publiekssegmentatie en richten zonder te controleren of de getoonde verkeersniveaus en het publiek significante resultaten binnen het het testen tijdkader voor hun optimalisering en omzettingsdoelstellingen zullen verstrekken. Om deze gemeenschappelijke fout te vermijden, beantwoord vooraf deze vragen:

* Hoeveel dagelijkse unieke bezoekers heeft de pagina?
* Wat is de omrekeningskoers voor de pagina?
* Hoe lang verwacht u dat u de test moet uitvoeren voordat u deze met vertrouwen volledig kunt noemen?

**Nuttige uiteinde**: Gebruik de [!DNL Adobe Target] [Voorbeeldgroottecalculator](/help/main/c-activities/t-test-ab/sample-size-determination.md#section_6B8725BD704C4AFE939EF2A6B6E834E6) om te bepalen welke monstergrootte nodig is voor een geslaagde test.

## Tip 12: Ontwerp eenvoudigere tests om ervoor te zorgen dat u deze kunt maken en implementeren.

Na het overwegen van alle aspecten van hoe te om een test te ontwerpen, kan een plan zeer complex worden. Gebaseerd op waar uw zaken met het testen zijn, en de capaciteit van uw groep om, de resultaten te ontwerpen, uit te voeren en te analyseren, bepalen als de test te ambitieus lijkt. Als dat het geval is, moet zij bereid zijn de reikwijdte en de complexiteit ervan te beperken. Het is beter om klein te beginnen dan de test helemaal niet uit te voeren. Je kunt geen ondoordringbare lift leveren als je de test nooit start. Het is belangrijk om de aspiraties van het team in evenwicht te brengen met de realiteiten van uw middelen en capaciteiten.

## Tip 13: Complexe tests onderverdelen in kleinere testactiviteiten om ze haalbaar te maken.

In plaats van één grote test met meerdere variabelen en complexe ontwikkeling te ontwikkelen, ontwikkelt u een minder complexe reeks kleinere tests met minimale variabelen. Dit maakt een beter inzicht in de testprestaties mogelijk op basis van specifieke variabelen. Het vermindert ook mogelijke technische kwesties die met de ontwikkeling van grotere projecten gepaard gaan.

![Afbeelding van complexe tests breken](/help/main/c-intro/assets/break-complex-tasks.png)

## Tip 14: Maximaliseer uw testimpact door dichter bij het einde van de conversietrechter te testen.

Testen net als de pagina waarop bezoekers op Aankoop voltooien, Toepassing verzenden of op een andere manier een conversie uitvoeren klikken, levert meestal de meest onbruikbare resultaten op. Bezoekers die het einde van de trechter bereiken, zijn beter gekwalificeerd, hebben meer tijd geïnvesteerd en zijn klaar om te kopen. Het testen van inzichten in hun voorkeuren en acties kan u dus helpen rendabele wijzigingen aan te brengen. Omdat pagina&#39;s op het aankooppad van essentieel belang zijn voor de conversiekoersen, moeten de tests die op deze pagina&#39;s worden uitgevoerd, worden gesocialiseerd naar de belangrijkste belanghebbenden voordat ze worden uitgerold.

![Conversietrechter-illustratie](/help/main/c-intro/assets/conversion-funnel.png)

## Tip 15: Werk uw tests voortdurend bij om herhalende verbeteringen aan te brengen.

Als uw hypothese niet klopt, denk dan aan manieren om uw test te verbeteren. Houd er rekening mee dat zelfs als geen van de geteste ervaringen beter presteerde, uw experiment geen tijdverspilling was. Een succesvolle test betekent niet altijd een verhoging van opbrengst of omzettingen. Als de test uw hypothese daadwerkelijk ondersteunt, dan ben je op weg naar het ontwikkelen van een algemene theorie. Maar zelfs als je een duidelijk winnend resultaat hebt, stop daar niet. Te vaak maken marketeers de fout om eens te testen en dan op die resultaten te bankieren zonder echt te begrijpen wat tot het succes heeft geleid. In plaats daarvan, ben van plan om op die resultaten te herhalen om te weten te komen waarom de front-runner vooruit was. Dit zal u aan diepere inzichten leiden die u in toekomstige campagnes kunt gebruiken.

## Tip 16: Vergelijk tests en personaliseringsactiviteiten voor ideeën om het richten te verbeteren.

Het vergelijken van de omzettingsprestaties van verschillende publiek binnen verschillende tests bij verschillende plaatsen kan helpen de optimaliseringsstrategie van een bedrijf concentreren en verfijnen. Gebruik testvergelijkingen om te bepalen welke doelgroepen het meest geschikt zijn om te testen, welke doelgerichte ervaringen moeten krijgen en welke soorten ervaringen het meest waarschijnlijk een reactie zullen opleveren.

Een klant van financiële services voerde bijvoorbeeld een promotiecampagne uit voor een creditcard die professionele prikkels voor sportevenementen omvatte. Door de gedeeltelijke factoriële multivariate tests van zijn landingspagina&#39;s, kon de klant het overseinen over creditcardvoordelen met sportieve prikkels optimaliseren om verschillend publiek van zijn klantenbasis te richten. Dankzij deze aanpak kon het bedrijf profiteren van de conversie en deze maximaliseren tijdens een tijdgevoelig venster rond een belangrijk sportevenement.

## Tip 17: Maak tests handig door ze alleen te starten als u weet dat u de gegevens kunt bewerken.

Een test is zinloos als u niet duidelijk bent over hoe u op de gegevens gaat handelen. Dit omvat het weten van uw belangrijkste succes metrisch, wat moet gebeuren om een winnaar te duwen, hoe u op testresultaten zult volgen, en wat u met de publieksinformatie zult doen. Voor een snelle en geslaagde test is het van essentieel belang dat elke bij de test betrokken groep (ontwikkelaars, creatieven, testspecialisten en anderen) zich bewust is van zijn rol voordat de test wordt gestart.

## Tip 18: Voordat u een test start, moet u controleren of het bedrijf de winnaar steunt.

Succesvolle optimalisatieorganisaties geloven in het concept van testen en begrijpen dat hun professionele meningen over welke ervaring de test zal winnen niet altijd waar blijken te zijn. Ze bepalen de winnaar op basis van een solide basis van gegevens, en zijn graag en bereid om de winnende ervaring live te zetten nadat de resultaten binnen zijn, zelfs als deze niet in overeenstemming is met hun verwachtingen of als het tegengesteld lijkt.

Zo heeft een klant van de zorgdiensten van de Adobe onlangs de waarde van het testen aangetoond door te laten zien hoe een hoofdbanner die het team als een slam had beschouwd een negatief effect had op de conversie. Als uw organisatie nog niet volledig het testen heeft ingebed, is het best om eenvoudigere, kleinere werkingsgebiedtests eerst uit te voeren zodat de veranderingen van testresultaten incrementeel kunnen worden gemaakt.

## Tip 19: Laat iedereen weten dat u een test hebt gestart om zorgen te voorkomen wanneer de site verandert.

Één van de voordelen om uw activiteiten op te zetten om parameters te gebruiken QA is dat u die verbindingen met iedereen op uw team kunt delen. U maakt meer mensen bewust van de activiteit en zorgt ervoor dat zij niet veronderstellen de plaats behoorlijk werkt wanneer zij een testvariant raken.

Nadat u uw tests voltooit, helpen het communiceren campagnelanceringen, testresultaten, en vooral geleerde lessen u bewustzijn van en interesse in de testresultaten opbouwen. Door de resultaten met iedereen in de organisatie te delen, vermijdt u ook dat een hypothese opnieuw wordt getest, leert u iedereen over wat werkt en helpt u hen fundamenteel hun eigen ideeën uit te dagen over wat werkt op basis van wat u hebt gevonden. Het is raadzaam een sjabloon voor te bereiden die u elke keer gebruikt voor het delen van uw bevindingen en belangrijke lessen.
Vervolgens kunt u een gedeeld boek of Microsoft PowerPoint-pakket maken dat deze lessen opneemt.

## Tip 20: Tik op de mobiele functionaliteit om meer innovatieve mobiele activiteiten te maken.

De gebruikers van tablets en smartphones moeten zich richten op aanraakbesturingselementen als de primaire bezoekersinteractie in plaats van op muisklikken en toetsenbordbesturing. Profiteer van de besturingselementen voor mobiele schermen, zoals vegen met vingers, aanraken, slepen, knijpen en zoomen. Gebruik eenvoudige, grote knoppen om interacties en navigatie aan te geven, zoals een groot winkelwagentje of een knop voor het afspelen van video. Als het ontwerpen voor mobiele detailhandel, rijke productvisualisatie omvat die voor het apparatentype wordt geoptimaliseerd. Zoek altijd naar mogelijkheden om de gebruikerservaring te verplaatsen naar ingesloten, grote kijkers of interactief zoomen en pannen op volledig scherm, 360 graden draaien en verbeterde videofunctionaliteit.

## Tip 21: Help mobiele bezoekers te vinden wat ze willen door de mobiele zoekfunctie te optimaliseren.

Mobiele gebruikers hebben een hoge intentie. De meesten van hen gebruiken onderzoek alvorens zij om het even wat anders op e-commercesites doen, die mobiele plaatsonderzoekoptimalisering cruciaal maken. Gebruik expliciete navigatiemogelijkheden om gemakkelijk te kunnen bladeren om de optimalisatie van zoekprogramma&#39;s voor mobiele apparaten te verbeteren. Implementeer automatisch voorstellen en automatisch corrigeren in de invoervakken voor zoekopdrachten om de moeilijkheid van mobiele typen te verhelpen. Verstrek dwingende, relevante onderzoeksresultaten die voor het schermgrootte en plaats worden geoptimaliseerd.

## Tip 22: Bereik het mobiele publiek beter door tijd-van-dag het richten voor mobiele SEM campagnes te gebruiken.

Begrijp hoe en wanneer u uw publiek kunt bereiken en hoe u uw dagelijkse reclameuitgaven beter kunt beheren door uw mobiele campagnes &#39;dag te parseren&#39; in verschillende segmenten door de dag heen.

Veel marketeers maken de fout dat ze niet genoeg geld toewijzen om dat deel van de stem te laten horen in de uren dat het gebruik van bepaalde apparaten het zwaarst is, waardoor er veel inkomsten en koppen op tafel blijven liggen.

Het tabletgebruik spiekt bijvoorbeeld meestal in de avonduren en veel gebruikers bladeren terwijl ze tv kijken. Smartphonegebruikers hebben daarentegen doorgaans onderweg toegang tot inhoud. De piekomzettingstijden variëren ook door industrie, zodat is het belangrijk om te begrijpen wanneer uw unieke klanten het meest waarschijnlijk zullen handelen.

## Houd rekening met

Overweeg de volgende ideeën voordat we verdergaan met het volgende hoofdstuk: &quot;Inspiration for testing and personalization activities.&quot;

### Als je je tests maakt, versier dan niet, wees bewust.

* Stel de stroom in met doelbewuste oogpaden die zijn gericht op conversiepunten.
* Zorg ervoor dat u uw onroerend goed in uw voordeel gebruikt.
* Gebruik Image Focus om ervoor te zorgen dat afbeeldingen geen decoratie zijn, maar voor u werken.
* Verminder rommelig, wrijving, en vervagen met Vereenvoudigd Exemplaar.
* Ben zeker u efficiënte Vraag aan Acties hebt wanneer u de gebruiker nodig hebt om actie te voeren.
* Voeg waar mogelijk geloofwaardigheid toe via door gebruikers gegenereerde inhoud.

### Vereenvoudig uw website.

* Zorg ervoor dat klanten niet lezen. Ze zullen het niet doen.
* Scannen is gemakkelijk.
* Gebruik blokken met opsommingstekens.
* Zorg ervoor dat uw kopie een duidelijk, opeenvolgend gedachteproces volgt.

### De efficiënte Vraag van het gebruik aan Acties (CTAs)

* Doe jezelf in de schoenen van de klant.
* Gebruik een taal die is georiënteerd op handelingen.
* Denk aan de motivatie voor conversie.
* Het omzettingsresultaat aanpakken.
* Zorg ervoor dat CTA&#39;s zichtbaar zijn!
