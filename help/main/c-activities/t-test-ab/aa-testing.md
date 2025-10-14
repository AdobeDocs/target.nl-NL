---
keywords: a/b;a/a;aa
description: Leer wat een A/A test is, waarom u een A/A test zou kunnen willen uitvoeren, hoe lang u de test zou moeten in werking stellen, en hoe te om de resultaten te interpreteren.
title: Wat is een A/A-test?
feature: A/B Tests
exl-id: 7489f4f5-3655-45f9-a743-651ba1c23c53
source-git-commit: 4f0ebdd06287a438e519d9bccb677ab1a9093396
workflow-type: tm+mt
source-wordcount: '940'
ht-degree: 0%

---

# A/A-tests

Voordat u met [!DNL Adobe Target] een A/A-test op uw site uitvoert, is het belangrijk dat u begrijpt wat een A/A-test is, waarom u een A/A-test wilt uitvoeren, hoe lang u de test moet uitvoeren en hoe u de resultaten moet interpreteren.

## Wat wordt A/A getest?

Voordat u de A/A-tests gaat verklaren, is het goed om de A/B-tests te beoordelen, zodat we vervolgens de verschillen kunnen bespreken.

In een standaard A/B test, wordt het verkeer toegewezen aan twee of meer verschillende ervaringen. Een ervaring is doorgaans de &quot;bediening&quot; en variaties van de ervaring worden getest op basis van het bedieningsorgaan om te zien welke ervaring de meeste lift in een bepaalde metrische waarde creëert.

Bij A/A-tests moet echter het verkeer worden verdeeld over twee identieke ervaringen, doorgaans met een verdeling van 50/50 verkeersfrequenties. Met een standaard A/B test, wilt u typisch een lift in omzetting ontdekken. Dit verschilt van een test A/A waarin uw doel gewoonlijk is te bepalen dat er *geen* verschil in lift tussen de identieke ervaringen is.

## Waarom zou je twee identieke ervaringen willen testen en wat doet dit?

Sommige organisaties voeren A/A-tests uit bij de implementatie van een nieuw testgereedschap, zoals [!DNL Target] , om te bepalen of:

* De activiteit is correct ingesteld
* De code is correct geïmplementeerd
* De rapportage is accuraat

Hoewel weinig organisaties A/A tests in werking stellen, is het goede praktijk om hen als &quot;sanitaire&quot;experimenten in werking te stellen om vertrouwen te bouwen na het uitvoeren van het hulpmiddel of alvorens A/B tests uit te voeren die omzetting en opbrengst zouden kunnen beïnvloeden.

## Waarom zou je een lift zien voor één ervaring als de ervaringen identiek zijn?

Er zijn vele redenen waarom u in één ervaring over een andere (identieke) ervaring zou kunnen zien optillen:

### De A/A-test werd voortdurend gecontroleerd

Een veelvoorkomend probleem bij het uitvoeren van een test, inclusief een A/A-test, is dat de resultaten voortdurend worden bekeken en dat een test voortijdig wordt stopgezet wanneer u statistische significantie ziet, en dat een winnende ervaring wordt gedeclareerd. De analisten doen vaak wat &quot;gegevens het zoeken&quot;wordt genoemd. Bij het zoeken naar gegevens worden de testgegevens in een vroeg stadium en vaak bekeken, terwijl wordt geprobeerd te bepalen welke ervaring beter presteert. Het risico bestaat dat de test voortijdig wordt stopgezet, waardoor de resultaten ongeldig zouden kunnen worden.

Bij een A/A-test kan gegevensspieken er vaak toe leiden dat analisten in één ervaring een lift zien, terwijl er in feite geen verschil moet zijn, omdat de twee ervaringen identiek zijn. In feite, met ononderbroken het trekken, zijn de tests A/A *gewaarborgd* om &quot;statistische betekenis&quot;te tonen (namelijk een vertrouwen boven een bepaalde drempel, zoals 95%) op één of ander punt tijdens de test.

Om dit te vermijden, en zoals met een regelmatige A/B test, zou u daarom van tevoren moeten beslissen welke steekproefgrootte te gebruiken, die op de minimumeffect grootte (de minimumlift onder waarvan een effect niet belangrijk voor uw zaken is), macht, en significantieniveaus wordt gebaseerd u aanvaardbaar vindt.

In een test A/A, zou het doel dan zijn *niet* een statistisch significant resultaat zien nadat uw test de gewenste steekproefgrootte heeft bereikt.

[!UICONTROL Adobe Target Sample Size Calculator] is een belangrijk hulpmiddel om u te helpen bepalen welke steekproefgrootte u zou moeten richten en hoe lang u de test zou moeten in werking stellen.

* [Adobe Target Size Calculator](/help/main/c-activities/t-test-ab/sample-size-determination.md#section_6B8725BD704C4AFE939EF2A6B6E834E6)

Zie ook de volgende artikelen voor informatie over hoe lang u een activiteit moet uitvoeren en andere nuttige tips en trucs:

* [Hoelang moet u een A/B test in werking stellen?](/help/main/c-activities/t-test-ab/sample-size-determination.md)
* [Tien gemeenschappelijke A/B-valkuilen en hoe deze te vermijden](/help/main/c-activities/t-test-ab/common-ab-testing-pitfalls.md)

### Statistische significantie beïnvloedt uw testresultaten

Het significantieniveau van een test bepaalt hoe waarschijnlijk het is dat de test een significant verschil in omrekeningskoersen tussen twee verschillende aanbiedingen meldt, terwijl er in feite geen echt verschil is. Dit wordt een fout van het type I genoemd. Het significantieniveau is een drempel die door de gebruiker is opgegeven en er is een wisselwerking tussen de tolerantie voor valse positieven en het aantal bezoekers dat bij de test moet worden betrokken bij de keuze van het juiste significantieniveau.

Een algemeen gebruikt significantieniveau bij A/A- en A/B-tests is 5%, wat overeenkomt met een betrouwbaarheidsniveau van 95% (betrouwbaarheidsniveau = 100% - significantieniveau). Een betrouwbaarheidsniveau van 95% betekent dat er telkens wanneer u een test uitvoert, een kans van 5% is om een statistisch significante lift te detecteren, zelfs als er geen verschil is tussen de ervaringen.

Stel dat u met uw A/A-test een betrouwbaarheidsniveau van 95% wilt bereiken. Met een betrouwbaarheid van 95% kon 1 op de 20 A/A tests statistisch significante verhoging van de conversies laten zien. Met een betrouwbaarheid van 90% kan 1 op de 10 tests bij het testen van identieke ervaringen een lift in omzettingen laten zien.

## Beste praktijken

Als u besluit dat een A/A test in uw organisatie noodzakelijk is, ben zich ervan bewust dat de identieke ervaringen tijdelijk een verschil van de controle zouden kunnen tonen. Dit kan normaal zijn, afhankelijk van de tijd de test wordt toegestaan te lopen. Het verschil zou moeten verminderen gegeven meer tijd en bezoekers.

De beste praktijken moeten regelmatige A/B testende methodologie gebruiken: besluit de steekproefgrootte voor tijd die op een minimale relevante effect grootte, gewenste macht, en betekenis door de [&#x200B; calculator van de Grootte van Adobe Target &#x200B;](/help/main/c-activities/t-test-ab/sample-size-determination.md#section_6B8725BD704C4AFE939EF2A6B6E834E6) wordt gebaseerd te gebruiken.

Zorg er vervolgens voor dat er voldoende tijd en bezoekers zijn voordat u tot conclusies komt. Vergeet niet dat er, afhankelijk van het significantieniveau van uw test, een kans is dat je ervaring een verschil in lift laat zien en zelfs tot winnaar wordt uitgeroepen.
