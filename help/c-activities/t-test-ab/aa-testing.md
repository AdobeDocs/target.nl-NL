---
keywords: a/b;a/a;aa;
description: Leer wat een A/A test is, waarom u een A/A test zou kunnen willen uitvoeren, hoe lang u de test zou moeten in werking stellen, en hoe te om de resultaten te interpreteren.
title: Wat is een A/A-test?
feature: A/B Tests
translation-type: tm+mt
source-git-commit: bb27f6e540998f7dbe7642551f7a5013f2fd25b4
workflow-type: tm+mt
source-wordcount: '890'
ht-degree: 0%

---


# A/A-tests

Voordat u een A/A-test op uw site uitvoert met behulp van [!DNL Adobe Target], is het belangrijk te begrijpen wat een A/A-test is, waarom u een A/A-test wilt uitvoeren, hoe lang u de test moet uitvoeren en hoe u de resultaten moet interpreteren.

## Wat wordt A/A getest?

Voordat u de A/A-tests gaat verklaren, is het goed om de A/B-tests te beoordelen, zodat we vervolgens de verschillen kunnen bespreken.

In een standaard A/B test, wordt het verkeer toegewezen aan twee of meer verschillende ervaringen. Een ervaring is doorgaans de &quot;bediening&quot; en variaties van de ervaring worden getest op basis van het bedieningsorgaan om te zien welke ervaring de meest lifteffecten in een bepaalde metrische waarde oplevert.

Bij A/A-tests moet echter het verkeer worden verdeeld over twee identieke ervaringen, doorgaans met een verdeling van 50/50 verkeersfrequenties. Met een standaard A/B test, wilt u typisch een lift in omzetting ontdekken. Dit verschilt van een A/A test waarin uw doel gewoonlijk is te bepalen dat er *no* verschil in lift tussen de identieke ervaringen is.

## Waarom zou je twee identieke ervaringen willen testen en wat doet dit?

Sommige organisaties voeren A/A-tests uit bij de implementatie van een nieuw testgereedschap, zoals [!DNL Target], om te bepalen of:

* De activiteit is correct ingesteld
* De code is correct geïmplementeerd
* De rapportage is accuraat

Hoewel weinig organisaties A/A tests in werking stellen, is het eigenlijk goede praktijk om hen als &quot;sanitaire&quot;experimenten in werking te stellen om vertrouwen te bouwen na het uitvoeren van het hulpmiddel of alvorens A/B tests uit te voeren die omzetting en opbrengst zouden kunnen beïnvloeden.

## Waarom zou je een lift zien voor één ervaring als de ervaringen identiek zijn?

Er zijn vele redenen waarom u in één ervaring over een andere (identieke) ervaring zou kunnen zien optillen:

### De A/A-test mag niet lang genoeg worden uitgevoerd

Een algemeen probleem bij het uitvoeren van een test, inclusief een A/A-test, is dat een test voortijdig wordt stopgezet en een winnende ervaring wordt gedeclareerd. Analysten doen vaak wat &#39;data peeking&#39; wordt genoemd. Bij het zoeken naar gegevens worden de testgegevens in een vroeg stadium en vaak bekeken, terwijl wordt geprobeerd te bepalen welke ervaring beter presteert. Het risico bestaat dat de test voortijdig wordt stopgezet, waardoor de resultaten ongeldig kunnen worden.

Bij een A/A-test kan gegevensspieken er vaak toe leiden dat analisten in één ervaring een lift zien, terwijl ze ervan uitgaan dat er geen verschil mag zijn, omdat de twee ervaringen identiek zijn. Na verloop van tijd en voldoende bezoeken dient het verschil in lift te dalen.

Net als bij een gewone A/B-test, moet u daarom van tevoren bepalen welke monstergrootte moet worden gebruikt, op basis van de minimale effectgrootte, het vermogen en de significantieniveaus die u acceptabel vindt. In een A/A test, zou het doel dan zijn om *not* een statistisch significant resultaat te zien nadat uw test de gewenste steekproefgrootte heeft bereikt.

[!UICONTROL Adobe Target Sample Size Calculator] is een belangrijk hulpmiddel om u te helpen bepalen welke steekproefgrootte u zou moeten richten en hoe lang u de test zou moeten in werking stellen.

* [Adobe Target Size Calculator](/help/c-activities/t-test-ab/sample-size-determination.md#section_6B8725BD704C4AFE939EF2A6B6E834E6)

Zie ook de volgende artikelen voor informatie over hoe lang u een activiteit moet uitvoeren en voor andere handige tips en trucs:

* [Hoelang moet u een A/B test in werking stellen?](/help/c-activities/t-test-ab/sample-size-determination.md)
* [Tien gemeenschappelijke A/B-valkuilen en hoe deze te vermijden](/help/c-activities/t-test-ab/common-ab-testing-pitfalls.md)

### Statistische significantie beïnvloedt uw testresultaten

Het significantieniveau van een test bepaalt hoe waarschijnlijk het is dat de test een significant verschil in omrekeningskoersen tussen twee verschillende aanbiedingen meldt, terwijl er in feite geen echt verschil is. Dit wordt een fout van het type I genoemd. Het significantieniveau is een drempel die door de gebruiker is opgegeven en er is een wisselwerking tussen de tolerantie voor valse positieven en het aantal bezoekers dat bij de test moet worden betrokken bij de keuze van het juiste significantieniveau.

Een algemeen gebruikt significantieniveau bij A/A- en A/B-tests is 5%, wat overeenkomt met een betrouwbaarheidsniveau van 95% (betrouwbaarheidsniveau = 100% - significantieniveau). Een betrouwbaarheidsniveau van 95% betekent dat er telkens wanneer u een test uitvoert, een kans van 5% is om een statistisch significante lift te detecteren, zelfs als er geen verschil is tussen de ervaringen.

Stel dat u met uw A/A-test een betrouwbaarheidsniveau van 95% wilt bereiken. Met een betrouwbaarheid van 95% kon 1 op de 20 A/A tests statistisch significante verhoging van de conversies laten zien. Met een betrouwbaarheid van 90% kan 1 op de 10 tests bij het testen van identieke ervaringen een lift in omzettingen laten zien.

## Beste praktijken

Als u besluit dat een A/A test in uw organisatie noodzakelijk is, ben zich ervan bewust dat de identieke ervaringen tijdelijk een verschil van de controle zouden kunnen tonen. Dit kan normaal zijn, afhankelijk van de tijd de test wordt toegestaan te lopen. Het verschil zou moeten verminderen gegeven meer tijd en bezoekers.

De beste manier is om regelmatig een A/B-testmethode te gebruiken: bepaalt de steekproefgrootte voor tijd die op een minimum effect grootte, gewenste macht en belangrijkheid wordt gebaseerd door [de Calculator van de Grootte van Adobe Target](/help/c-activities/t-test-ab/sample-size-determination.md#section_6B8725BD704C4AFE939EF2A6B6E834E6) te gebruiken.

Zorg er vervolgens voor dat er voldoende tijd en bezoekers zijn voordat u tot conclusies komt. Vergeet niet dat er, afhankelijk van het significantieniveau van uw test, een kans is dat je ervaring een verschil in lift laat zien en zelfs tot winnaar wordt uitgeroepen.
