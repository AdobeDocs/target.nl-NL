---
keywords: faq;frequently asked questions;analytics for target;a4T;lift;ad hoc;report builder;confidence
description: Dit onderwerp bevat antwoorden op vragen die vaak over lift en vertrouwen worden gevraagd wanneer het gebruiken van Analytics als rapporteringsbron voor Doel (A4T).
title: Optillen en vertrouwen - A4T veelgestelde vragen
feature: a4t troubleshooting
topic: Standard
uuid: 7d0402f3-d6f2-422e-b69c-86e10120ac83
translation-type: tm+mt
source-git-commit: 95450abc32be19d04b791af3c62673e9411ab53c
workflow-type: tm+mt
source-wordcount: '496'
ht-degree: 0%

---


# Optillen en vertrouwen - A4T veelgestelde vragen{#lift-and-confidence-a-t-faq}

Dit onderwerp bevat antwoorden op vragen die vaak over lift en vertrouwen worden gevraagd wanneer het gebruiken van Analytics als rapporteringsbron voor Doel (A4T).

## Kan ik off-line berekeningen voor A4T uitvoeren? {#section_55B5B750E17D414CAECBEECE27B15D81}

U kunt offlineberekeningen voor A4T uitvoeren, maar het vereist een stap met gegevens het uitvoeren binnen [!DNL Analytics]. Voor meer informatie, zie &quot;het Uitvoeren Offline Berekeningen voor Analytics voor Doel (A4T)&quot;in het Niveau van het [Vertrouwen en het Interval](/help/c-reports/conversion-rate.md#concept_0D0002A1EBDF420E9C50E2A46F36629B)van het Vertrouwen.

## Hoe wordt lift berekend? {#section_8CAE788EED5646C4B1D64A0D22070734}

Lift is het percentageverschil tussen uw resultaten van de controlepagina en een succesvolle testvariant.

## Hoe wordt het vertrouwen berekend? {#section_97DB24D833E742988318CA65DA65DAD9}

Het betrouwbaarheidsniveau is de waarschijnlijkheid dat de gemeten omrekeningskoers om andere redenen dan toeval verschilt van de omrekeningskoers van de kampioene pagina.

## Waarom kan ik geen lift en vertrouwen zien op berekende maatstaven? {#lift-confidence}

Berekende metriek worden momenteel niet ondersteund in lift- en betrouwbaarheidsfuncties. Dit komt door het feit dat Analytics meetgegevens berekent op geaggregeerd niveau, in plaats van op bezoekersniveau. Vertrouwen is met name een berekening op bezoekersniveau.

Niet-berekende (standaard)gebeurtenissen worden ondersteund in lift en betrouwbaarheid. Zij worden de teller in de lift functie; de teller kan geen berekening zelf zijn. De noemer is de normaliserende metriek (indrukkingen, bezoeken, of bezoekers). Voorbeelden van standaardgebeurtenissen zijn onder andere orders, inkomsten, conversies van activiteiten, aangepaste gebeurtenissen 1-1000, enz. Dit betekent dat gemeenschappelijke optimalisatiemetriek, zoals gesprekstarief (Orders/Bezoeker) en RPV (Inkomsten/Bezoeker) in lift en vertrouwen worden gesteund.

Voorbeelden van niet-ondersteunde metriek- of gebruiksgevallen zijn:

* Gemiddelde bestelwaarde (inkomsten/bestelling, per bezoeker). AOV wordt niet ondersteund omdat de teller een berekende metrische waarde is. In plaats daarvan wordt aanbevolen de twee bepalende meeteenheden van AOV - inkomsten per bezoeker en conversietarief in overweging te nemen.
* Berekende metriek die de som standaardgebeurtenissen zijn. U kunt bijvoorbeeld tien verschillende hoofdformulieren bijhouden in tien aparte gebeurtenissen en deze vervolgens bij elkaar voegen om de totale aantal hoofdinzendingen op te halen. Een aanbevolen methode voor het bijhouden van deze gebeurtenissen is het implementeren van één enkele gebeurtenis voor het verzenden van leads in Analytics en het vervolgens gebruiken van een eVar om het type loodformulier te verzamelen. Het gebruik van deze methode vereist minder variabelen en zorgt ervoor dat u de enige metrische voorlegging van het lood in lift en vertrouwelijkheidsfuncties kunt gebruiken.

## Hoe verwerkt A4T betrouwbaarheidsberekeningen? {#section_66115EAF1BA34F7A8FCED7B08DA4F99C}

A4T gebruikt niet-binaire metrische berekeningen met de som van vierkante gegevens. De variantie wordt berekend met de som van de gegevens van de vierkanten. Extreme bestellingen worden niet in aanmerking genomen. Bovendien wordt bij de betrouwbaarheidsberekening geen Bonferroni-correctie toegepast voor meerdere aanbiedingen.

## Werken lift en vertrouwen in ad hoc en Report Builder? Als het niet inheems is, kan ik het daar zelf doen? {#section_D8BB69AE700B4C5CB5FD28DB51F9A4E9}

Optillen en vertrouwen werken niet in ad-hoc of Report Builder en kunnen niet zelf worden berekend voor continue variabelen. Het is mogelijk om het voor binaire metriek manueel te berekenen.
