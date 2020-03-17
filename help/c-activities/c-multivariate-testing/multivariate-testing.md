---
keywords: multivariate test;mvt;full factorial;mvt or a/b;multivariate a/b;traffic estimator;when to use mvt;mvt considerations;multivariate;partial-factorial;partial factorial;full-factorial
description: MVT (Multivariate Testing) in Adobe Target vergelijkt combinaties van aanbiedingen in elementen op een pagina om te bepalen welke combinatie het beste voor een specifiek publiek presteert, en identificeert welk element het meest van invloed is op het succes van de activiteit.
title: Multivariatietest
uuid: a6f0cf9f-bd5e-4ae2-8dbe-0c94ec6a02ba
translation-type: tm+mt
source-git-commit: 65a4fd0d05ad065c9291a83dc0b3066451f7373e

---


# Multivariatietest{#multivariate-test}

[!UICONTROL Multivariate Testing] (MVT) vergelijkt [!DNL Adobe Target] combinaties van aanbiedingen in elementen op een pagina om te bepalen welke combinatie het beste voor een specifiek publiek presteert, en identificeert welk element het meest van invloed is op het succes van de activiteit.

## Overzicht van MVT {#section_C73A2D1409EC42C9B0EDD4B976651C5E}

Door meerdere varianten te testen kunt u zien welke invloed specifieke elementen hebben op de conversie, in vergelijking met andere elementen op de pagina. Het kan u ook helpen een combinatie elementen verfijnen die effectief zijn gebleken.

Een voordeel van een multivariate test in vergelijking met een A/B-test is dat u kunt zien welke elementen op de pagina de grootste invloed hebben op de conversie. Dit wordt ook wel het &quot;belangrijkste effect&quot; genoemd. Deze informatie is bijvoorbeeld handig als u wilt bepalen waar u inhoud wilt plaatsen die u de meeste aandacht wilt krijgen.

Met behulp van verschillende tests kunt u ook samengestelde effecten tussen twee of meer elementen op een pagina vinden. Een bepaalde advertentie kan bijvoorbeeld meer conversies produceren wanneer deze wordt gecombineerd met een bepaalde banner of hoofdafbeelding. Dit wordt ook wel &#39;interactieeffect&#39; genoemd.

[!DNL Target] maakt gebruik van multivariatietests in volledige fabrieken om u te helpen uw inhoud te optimaliseren. Een multivariabeletest met volledige factoriële werking waarbij alle mogelijke combinaties van inhoud met gelijke waarschijnlijkheid worden getest. Als u bijvoorbeeld twee pagina-elementen hebt met elk drie aanbiedingen, zijn er negen mogelijke combinaties (3x3). Drie elementen, met twee mogelijke aanbiedingen en één met twee aanbiedingen, bieden 18 opties (3x3x2).

Bij Doel is elke combinatie één ervaring. De multivariate test vergelijkt elke ervaring zodat kunt u leren welke combinaties het meest succesvol zijn. Tegelijkertijd worden gegevens verzameld en geanalyseerd om te begrijpen hoe elke locatie en de aanbiedingen invloed hebben op de succesmaatstaf.

![](assets/multivariate.png){width=&quot;672px&quot;}

Wegens het aantal combinaties die kunnen worden geproduceerd, vereist een multivariate test meer tijd en verkeer dan een test A/B. De pagina moet voldoende verkeer krijgen om statistisch significante resultaten voor elke ervaring te produceren. Om nuttige resultaten te verkrijgen, moet u begrijpen hoeveel verkeer uw pagina ontvangt en het optimale aantal combinaties voor de juiste hoeveelheid tijd testen om de vereiste resultaten te krijgen. De schatter van het [Verkeer van het doel](../../c-activities/c-multivariate-testing/t-create-multivariate-test/traffic-estimator.md#task_71AA6922AFD447EA8C5E610A78ABA714) kan u helpen een test ontwerpen die met uw verkeer werkt. Voordat u de Verkeersschatting gebruikt, moet u over goede statistieken beschikken die het aantal afbeeldingen en conversies weergeven dat uw site normaal ontvangt. Overweeg uw verkeersniveaus per dag. Hoe meer ervaringen in een activiteit, des te meer verkeer de activiteit zal moeten omvatten of des te langer uw activiteit zal moeten lopen. Als uw verkeer niet zeer hoog is, zou u een klein aantal combinaties moeten testen; anders kan de tijd die nodig is om zinvolle testresultaten te produceren te lang zijn om nuttig te zijn.

## MVT-terminologie {#section_DF475CA7F34B4CFDB7BE7363761D64AE}

Bij het opzetten van een test met meerdere varianten is het handig om enige basisterminologie te begrijpen.

Er zijn meerdere termen die op verschillende manieren in de hele branche worden gebruikt. In deze sectie worden de termen gedefinieerd die worden gebruikt door [!DNL Target].

**Combinatie:** De variaties in de inhoud die worden gemaakt wanneer u meerdere inhoudsopties op meerdere locaties test. Als u bijvoorbeeld drie locaties test, elk met drie inhoudsopties, zijn er 27 mogelijke combinaties (3x3x3). Een bezoeker van uw site ziet één combinatie, ook wel een ervaring genoemd.

**Inhoud:** De tekst of afbeelding bestaande uit een testvariatie binnen een locatie. In een multivariate test, worden een aantal inhoudsopties binnen veelvoudige plaatsen vergeleken. In MVT-methodologie wordt de inhoud soms ook wel een *niveau* genoemd.

**Element:** Een DOM-element met variaties in de inhoud die in de MVT-test moeten worden getest. Zie ook *Locatie*.

**Locatie:** Een specifiek inhoudsgebied op een pagina, dat vaak wordt opgenomen door één DOM-element. In de MVT-methodologie wordt een locatie soms ook wel een *factor* genoemd. Een full-factorial multivariate test vergelijkt alle mogelijke combinaties aanbiedingen in uw plaatsen.

## Wanneer moet u MVT vs. A/B gebruiken? {#section_3D2B966B6671406C861A1843EA41D28C}

U kunt meerdere tests gebruiken in combinatie met A/B-tests om de pagina te optimaliseren. Voorbeelden van situaties waarin u ze samen wilt gebruiken zijn:

* Gebruik een A/B-test om de paginalay-out te optimaliseren, gevolgd door een MVT-test om de beste inhoud in elk element op de pagina te bepalen.

   Een A/B test kan belangrijke terugkoppelen op de lay-out, en de tests MVT beïnvloeden zich bij het testen van de inhoud binnen de elementen in uw paginaontwerp. Als u een A/B-test uitvoert op de lay-out voordat u meerdere inhoudsopties test, kunt u de beste lay-out en de meest onbruikbare inhoud bepalen.

* Gebruik een MVT-test om te bepalen welk element het belangrijkste is en volg vervolgens een meer gerichte A/B-test op dat element.

   Wanneer het aantal verschillende ervaringen vijf overschrijdt en twee of meer elementen overspant, is het een goed idee om een test MVT alvorens uw tests A/B uit te voeren te overwegen. Uit de MVT-test blijkt welke gebieden op de pagina de conversie waarschijnlijk zullen verbeteren. Dit zijn de elementen waarop een markeerteken zich moet concentreren. Bijvoorbeeld, zou de test MVT kunnen tonen dat de vraag aan actie het belangrijkste element voor het bereiken van uw doelstellingen is. Zodra u hebt bepaald welke elementen en inhoud het nuttigst zijn om u te helpen uw doelstellingen bereiken, kunt u een test A/B in werking stellen om de resultaten verder te verfijnen, zoals twee specifieke beelden tegen elkaar te testen, of de formulering of de kleuren van een vraag aan actie te vergelijken. Door een MVT-test met een of meer A/B-tests uit te voeren, kunt u de best mogelijke inhoud voor de gewenste resultaten bepalen.

## Overwegingen {#section_979FE3F398654C1EA1C86E7DBC9A8DAD}

* Gebruik een MVT-test wanneer u ten minste drie elementen hebt om te testen. Als u minder hebt, stel een reeks tests A/B in werking.
* Selecteer de pagina-elementen waarvan u denkt dat deze het meest van invloed zijn op de resultaten.
* Neem niet te veel elementen of locaties op in een test. Hoe groter het getal, hoe langer de test duurt.
* Plan het testontwerp vooraf. Het is niet aan te raden een test te bewerken nadat deze live gaat en gegevens worden verzameld en geanalyseerd.
* Aanbevolen wordt elementen onafhankelijk van elkaar te maken.

   Test bijvoorbeeld niet de lay-out en de inhoud in dezelfde test.

* Plan extra tijd voor QA wegens de toename van het aantal ervaringen. U kunt gedeeltelijk-factoriële het testen ook gebruiken om de hoeveelheid verkeer te verminderen nodig voor een multivariate test. Zie Partial-factorial tests hieronder voor meer informatie:

## Partiële factoriële tests

[!DNL Target] biedt multivariate testen in volledige fabrieken als ingebouwde optie voor activiteit. In statistieken biedt het ontwerpen van experimenten vele benaderingen, of ontwerpen, om te bepalen welke factoren de resultaten beïnvloeden. Een van die benaderingen is de [Taguchi-methode](https://en.wikipedia.org/wiki/Taguchi_methods) voor gedeeltelijke fabriekstests. Met Taguchi kunnen marketers een set veronderstellingen maken die het aantal permutaties van ervaringen die getest moeten worden verminderen, en op hun beurt de verkeersvereisten voor een multivariate test verminderen. Deze functionaliteit en testbenadering kunnen worden gebruikt in [!DNL Target] het gebruiken van dit [off-line spreadsheet](/help/assets/MVT-Taguchi-Partial-Factorial-Design-02102017.xlsx).

Als uw team andere benaderingen van het Ontwerp van Experimenten gebruikt, kunt u deze berekeningsspreadsheet als verwijzingsimplementatie voor douaneexperimentontwerpen gebruiken.

Houd rekening met de volgende tips wanneer u het werkblad voor offlineberekeningen gebruikt:

* Kies de elementen die u wilt wijzigen en het aantal versies van elk element (3x2, 4x3, enzovoort).
* Houd de nummering consistent. Als de knop bijvoorbeeld Element 1 is en de opties Blauw, Groen en Geel zijn, is de blauwe knop 1-1, de groene knop 1-2 en de gele knop 1-3.
* Het offline werkblad biedt het juiste aantal benodigde ervaringen (vier voor een 3x2, negen voor een 4x3 enzovoort).
* Bouw de ervaringen in het A/B- werkschema met Composer van de [Visuele Ervaring (VEC)](/help/c-experiences/experiences.md). U kunt aangepaste code gebruiken, HTML, WYSIWYG of een willekeurige combinatie hiervan bewerken.
* Nadat de activiteit (die op de calculator van de steekproefgrootte wordt gebaseerd) voorbij is, stel resultaten door spreadsheet in werking om de andere details te krijgen.

Voor meer overwegingen en beste praktijken, zie [Multivariate Beste praktijken](../../c-activities/c-multivariate-testing/best-practices.md#reference_53635817FFB741EF8C4E56CC70688EDD)van de Test.

## Trainingsvideo&#39;s:

De volgende video&#39;s bevatten meer informatie over de concepten die in dit artikel worden besproken.

### Activiteitstypen (9:03) ![overzichtspagina](/help/assets/overview.png)

In deze overzichtsvideo worden de activiteitstypen uitgelegd die beschikbaar zijn in Target Standard/Premium. Het testen met meerdere varianten wordt vanaf 4:20 besproken.

* Beschrijf de soorten activiteiten die onder [!DNL Adobe Target]
* Selecteer het juiste type activiteit om uw doelen te bereiken
* Beschrijf de driestappenworkflow met instructies die van toepassing is op alle typen activiteiten

>[!VIDEO](https://video.tv.adobe.com/v/17386)

### Zelfstudie-badge voor meerdere ![tests maken (9:25)](/help/assets/tutorial.png)

In deze video wordt uitgelegd hoe u een multivariate test begrijpt, plant en maakt met behulp van de driestappenworkflow met instructies voor het doel.

* Een multivariatietest definiëren en ontwerpen
* Een multivariatietest maken

>[!VIDEO](https://video.tv.adobe.com/v/17395)