---
keywords: multivariatie test;mvt;volledige factorial;mvt of a/b;multivariate a/b;verkeersschatter;wanneer om mvt te gebruiken;mvt overwegingen;multivariate;gedeeltelijk-factorial;gedeeltelijke factor;volledig-factorial
description: Leer hoe te om a [!UICONTROL Multivariate Test] (MVT) in  [!DNL Adobe Target]  te gebruiken om combinaties aanbiedingen in elementen op een pagina te vergelijken om te bepalen welke combinatie het beste presteert.
title: Wat is een [!UICONTROL Multivariate Test] ?
feature: Multivariate Tests
exl-id: c8b60011-cb3a-4e28-b84f-06910687b14b
source-git-commit: 0d73a062f70080057c3323f5150af067e3a2e27e
workflow-type: tm+mt
source-wordcount: '1438'
ht-degree: 0%

---

# [!UICONTROL Multivariate Test] overzicht

Een [!UICONTROL Multivariate Test] (MVT) activiteit in [!DNL Adobe Target] vergelijkt combinaties aanbiedingen in elementen op een pagina om te bepalen welke combinatie het beste voor een specifiek publiek presteert. Met een [!UICONTROL Multivariate Test] -activiteit kunt u ook bepalen welk element het meest van invloed is op het succes van de activiteit.

Door meerdere variaties te testen kunt u zien welke invloed specifieke elementen hebben op de conversie, in vergelijking met andere elementen op de pagina. Het testen met meerdere varianten kan u ook helpen een combinatie van elementen te verfijnen waarvan is aangetoond dat ze effectief zijn.

Een voordeel dat een [!UICONTROL Multivariate Test] biedt in vergelijking met een A/B-test, is de mogelijkheid om te tonen welke elementen op de pagina de grootste invloed hebben op de conversie. Dit voordeel wordt ook wel het &quot;belangrijkste effect&quot; genoemd. Deze informatie is bijvoorbeeld handig om u te helpen bepalen waar u inhoud wilt plaatsen die u de meeste aandacht wilt krijgen.

Met [!UICONTROL Multivariate Test] -activiteiten kunt u ook samengestelde effecten tussen twee of meer elementen op een pagina vinden. Een bepaalde advertentie kan bijvoorbeeld meer conversies produceren wanneer deze wordt gecombineerd met een bepaalde banner of hoofdafbeelding. Dit wordt ook wel &#39;interactieeffect&#39; genoemd.

[!DNL Target] maakt gebruik van multivariatietests die volledig in de fabriek zijn uitgevoerd en die u helpen uw inhoud te optimaliseren. Bij een multivariatietest met volledige factoring worden alle mogelijke combinaties van inhoud met gelijke waarschijnlijkheid onderzocht. Als u bijvoorbeeld twee pagina-elementen hebt met elk drie aanbiedingen, zijn er negen mogelijke combinaties (3x3). Drie elementen, met twee mogelijke aanbiedingen en één met twee aanbiedingen, bieden 18 opties (3x3x2).

In [!DNL Target] is elke combinatie één ervaring. In [!UICONTROL Multivariate Test] wordt elke ervaring vergeleken, zodat u kunt zien welke combinaties het meest succesvol zijn. Tegelijkertijd worden gegevens verzameld en geanalyseerd om te begrijpen hoe elke locatie en de aanbiedingen invloed hebben op de succesmaatstaf.

![&#x200B; multivariate beeld &#x200B;](assets/multivariate.png)

Vanwege het aantal combinaties dat kan worden gegenereerd, vereist een [!UICONTROL Multivariate Test] meer tijd en verkeer dan een A/B-test. De pagina moet voldoende verkeer krijgen om statistisch significante resultaten voor elke ervaring te produceren. Om nuttige resultaten te verkrijgen, moet u begrijpen hoeveel verkeer uw pagina ontvangt en het optimale aantal combinaties voor de juiste hoeveelheid tijd testen om de vereiste resultaten te krijgen.

De schatter van het Verkeer van het doel [&#128279;](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/traffic-estimator.md#task_71AA6922AFD447EA8C5E610A78ABA714) kan u helpen een test ontwerpen die met uw verkeer werkt. Voordat u de Verkeersschatting gebruikt, moet u over goede statistieken beschikken die het aantal afbeeldingen en conversies weergeven dat uw site normaal ontvangt. Overweeg uw verkeersniveaus per dag. Hoe meer ervaringen in een activiteit, hoe meer verkeer de activiteit moet omvatten of hoe langer uw activiteit moet worden uitgevoerd. Als uw hoeveelheid verkeer niet hoog is, zou u een paar combinaties moeten testen; anders, zou de hoeveelheid tijd die wordt vereist om betekenisvolle testresultaten te veroorzaken te lang kunnen zijn nuttig.

## MVT-terminologie {#section_DF475CA7F34B4CFDB7BE7363761D64AE}

Bij het opzetten van een test met meerdere varianten is het handig om enige basisterminologie te begrijpen.

Er zijn meerdere termen die op verschillende manieren in de hele branche worden gebruikt. In deze sectie worden de termen gedefinieerd die door [!DNL Target] worden gebruikt.

**Combinatie:** de inhoudsvariaties die worden gecreeerd wanneer u veelvoudige inhoudsopties in veelvoudige plaatsen test. Als u bijvoorbeeld drie locaties test, elk met drie inhoudsopties, zijn er 27 mogelijke combinaties (3x3x3). Een bezoeker van uw site ziet één combinatie, ook wel een ervaring genoemd.

**Inhoud:** de tekst of het beeld dat een testvariatie binnen een plaats bestaat. In een multivariate test, worden verscheidene inhoudsopties binnen veelvoudige plaatsen vergeleken. In methodologie MVT, wordt de inhoud soms bedoeld als a *niveau*.

**Element:** A DOM element dat inhoudsmariaties bevat die in de test MVT moeten worden getest. Zie ook *Plaats*.

**Plaats:** een specifiek inhoudsgebied op een pagina, vaak bevat door één enkel element DOM. In methodologie MVT, wordt een plaats soms bedoeld als a *factor*. Een full-factorial multivariate test vergelijkt alle mogelijke combinaties aanbiedingen in uw plaatsen.

## Wanneer moet u [!UICONTROL Multivariate Test] versus A/B gebruiken? {#section_3D2B966B6671406C861A1843EA41D28C}

U kunt meerdere tests gebruiken in combinatie met A/B-tests om de pagina te optimaliseren. Voorbeelden van situaties waarin u ze samen wilt gebruiken zijn:

* Gebruik een A/B-test om de paginalay-out te optimaliseren, gevolgd door een MVT-test om de beste inhoud in elk element op de pagina te bepalen.

  Een A/B test kan belangrijke terugkoppelen op de lay-out, en de tests MVT beïnvloeden zich bij het testen van de inhoud binnen de elementen in uw paginaontwerp. Als u een A/B-test uitvoert op de lay-out voordat u meerdere inhoudsopties test, kunt u de beste lay-out en de meest onbruikbare inhoud bepalen.

* Gebruik een MVT-test om te bepalen welk element het belangrijkste is en volg vervolgens een meer gerichte A/B-test op dat element.

  Wanneer het aantal verschillende ervaringen vijf overschrijdt en twee of meer elementen overspant, is het een goed idee om een test MVT alvorens uw tests A/B uit te voeren te overwegen. Uit de MVT-test blijkt welke gebieden op de pagina de conversie waarschijnlijk zullen verbeteren. Dit zijn de elementen waarop een markeerteken zich moet concentreren. De MVT-test kan bijvoorbeeld laten zien dat de call to action het belangrijkste element is voor het bereiken van uw doelen. Zodra u hebt bepaald welke elementen en inhoud het nuttigst om u te helpen uw doelstellingen bereiken, kunt u een test A/B in werking stellen om de resultaten verder te verfijnen. U kunt bijvoorbeeld twee specifieke afbeeldingen tegen elkaar testen of de tekst of kleuren van een call to action vergelijken. Door een MVT-test met een of meer A/B-tests uit te voeren, kunt u de best mogelijke inhoud voor de gewenste resultaten bepalen.

## Overwegingen {#section_979FE3F398654C1EA1C86E7DBC9A8DAD}

* Gebruik een MVT-test wanneer u ten minste drie elementen hebt om te testen. Als u minder hebt, stel een reeks tests A/B in werking.
* Selecteer de pagina-elementen waarvan u denkt dat deze de beste invloed hebben op de resultaten.
* Neem niet te veel elementen of locaties op in een test. Hoe groter het getal, des te langer de testduur.
* Plan het testontwerp vooraf. Bewerk een test niet nadat deze live is gegaan en gegevens zijn verzameld en geanalyseerd.
* Elementen moeten onafhankelijk van elkaar zijn.

  Test bijvoorbeeld niet de lay-out en de inhoud in dezelfde test.

* Plan extra tijd voor QA wegens de toename van het aantal ervaringen. U kunt gedeeltelijk-factoriële het testen ook gebruiken om de hoeveelheid verkeer te verminderen nodig voor een multivariate test. Zie Partial-factorial tests hieronder voor meer informatie:

## Partiële factoriële tests

[!DNL Target] biedt multivariate testen in volledige fabrieken als ingebouwde optie voor activiteit. In de statistiek
Het &quot;ontwerp van Experimenten&quot;biedt vele benaderingen, of ontwerpen, om te bepalen welke factoren de resultaten beïnvloeden. Één dergelijke benadering is de [&#x200B; Methode Taguchi &#x200B;](https://en.wikipedia.org/wiki/Taguchi_methods) voor gedeeltelijk-factoriële het testen. Met Taguchi kunnen marketers een set veronderstellingen maken die het aantal permutaties van ervaringen die getest moeten worden verminderen, en op hun beurt de verkeersvereisten voor een multivariate test verminderen. Deze functionaliteit en het testen benadering kunnen in [!DNL Target] worden toegepast gebruikend dit [&#x200B; off-line spreadsheet &#x200B;](/help/main/assets/MVT-Taguchi-Partial-Factorial-Design-02102017.xlsx).

Als uw team andere benaderingen van het Ontwerp van Experimenten gebruikt, kunt u deze berekeningsspreadsheet als verwijzingsimplementatie voor douaneexperimentontwerpen gebruiken.

Houd rekening met de volgende tips wanneer u het werkblad voor offlineberekeningen gebruikt:

* Kies de elementen die u wilt wijzigen en het aantal versies van elk element (3x2, 4x3, enzovoort).
* Houd de nummering consistent. Als de knop bijvoorbeeld Element 1 is en de opties Blauw, Groen en Geel zijn, is de blauwe knop 1-1, de groene knop 1-2 en de gele knop 1-3.
* Het offline werkblad biedt het juiste aantal benodigde ervaringen (vier voor een 3x2, negen voor een 4x3 enzovoort).
* Bouw de ervaringen in het A/B- werkschema met [&#x200B; Visuele Composer van de Ervaring (VEC) &#x200B;](/help/main/c-experiences/experiences.md). U kunt aangepaste code gebruiken, HTML, WYSIWYG of een willekeurige combinatie bewerken.
* Nadat de activiteit (die op de calculator van de steekproefgrootte wordt gebaseerd) voorbij is, stel de resultaten door spreadsheet in werking om de andere details te krijgen.

Voor meer overwegingen en beste praktijken, zie [&#x200B; Multivariate Beste praktijken van de Test &#x200B;](/help/main/c-activities/c-multivariate-testing/best-practices.md#reference_53635817FFB741EF8C4E56CC70688EDD).

## Trainingsvideo&#39;s

De volgende video&#39;s bevatten meer informatie over de concepten die in dit artikel worden besproken.

### De Types van activiteit (9 :03) ![&#x200B; badge van het Overzicht &#x200B;](/help/main/assets/overview.png)

In deze overzichtsvideo worden de activiteitstypen uitgelegd die beschikbaar zijn in [!DNL Target] . Het multivariate testen wordt besproken begin bij 4 :20.

* Beschrijf de typen activiteiten die zijn opgenomen in [!DNL Adobe Target]
* Selecteer het juiste type activiteit om uw doelen te bereiken
* Beschrijf de driestappenworkflow met instructies die van toepassing is op alle typen activiteiten

>[!VIDEO](https://video.tv.adobe.com/v/17386)

### Creërend Multivariate Tests (9 :25) ![&#x200B; badge van het Leerprogramma &#x200B;](/help/main/assets/tutorial.png)

Deze video verklaart hoe te, een multivariate test te begrijpen te plannen en tot stand te brengen gebruikend het  driestapel geleide werkschema van het Doel.

* Een multivariatietest definiëren en ontwerpen
* Een multivariatietest maken

>[!VIDEO](https://video.tv.adobe.com/v/17395)
