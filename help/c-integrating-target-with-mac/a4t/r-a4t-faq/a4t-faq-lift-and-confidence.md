---
keywords: faq;frequently asked questions;analytics for target;a4T;lift;ad hoc;report builder;confidence
description: Dit onderwerp bevat antwoorden op vragen die vaak over lift en vertrouwen worden gevraagd wanneer het gebruiken van Analytics als rapporteringsbron voor Doel (A4T).
title: Optillen en vertrouwen - A4T veelgestelde vragen
topic: Standard
uuid: 7d0402f3-d6f2-422e-b69c-86e10120ac83
translation-type: tm+mt
source-git-commit: 217ca811521e67dcd1b063d77a644ba3ae94a72c

---


# Optillen en vertrouwen - A4T veelgestelde vragen{#lift-and-confidence-a-t-faq}

Dit onderwerp bevat antwoorden op vragen die vaak over lift en vertrouwen worden gevraagd wanneer het gebruiken van Analytics als rapporteringsbron voor Doel (A4T).

## Kan ik off-line berekeningen voor A4T uitvoeren? {#section_55B5B750E17D414CAECBEECE27B15D81}

U kunt offlineberekeningen voor A4T uitvoeren, maar het vereist een stap met gegevens het uitvoeren binnen [!DNL Analytics]. Voor meer informatie, zie &quot;het Uitvoeren Offline Berekeningen voor Analytics voor Doel (A4T)&quot;in het Niveau van het [Vertrouwen en het Interval](../../../c-reports/conversion-rate.md#concept_0D0002A1EBDF420E9C50E2A46F36629B)van het Vertrouwen.

## Hoe wordt lift berekend? {#section_8CAE788EED5646C4B1D64A0D22070734}

Lift is het percentageverschil tussen uw resultaten van de controlepagina en een succesvolle testvariant.

## Hoe wordt het vertrouwen berekend? {#section_97DB24D833E742988318CA65DA65DAD9}

Het betrouwbaarheidsniveau is de waarschijnlijkheid dat de gemeten omrekeningskoers om andere redenen dan toeval verschilt van de omrekeningskoers van de kampioene pagina.

## Waarom kan ik geen lift en vertrouwen zien op berekende maatstaven? {#section_D3E44E24782A409DBD88AE4D1595CB58}

Optillen en vertrouwen kunnen momenteel niet worden gegenereerd voor berekende metriek. In de meeste gevallen is dit echter geen probleem, omdat de lift wordt genormaliseerd door de normalisatie-instelling. Als u bijvoorbeeld lift selecteert voor bestellingen en de normalisatie-instelling bezoeken is, wordt lift berekend op basis van de verhouding van beide, namelijk de conversiekoers.

## Hoe verwerkt A4T betrouwbaarheidsberekeningen? {#section_66115EAF1BA34F7A8FCED7B08DA4F99C}

A4T gebruikt niet-binaire metrische berekeningen met de som van vierkante gegevens. De variantie wordt berekend met de som van de gegevens van de vierkanten. Extreme bestellingen worden niet in aanmerking genomen.

Om het even welk segment van Analytics kan op het rapport worden toegepast. Zo krijgt u de &quot;extreme volgorde&quot; onder andere segmentopties. Een metrische waarde kan ook worden gemaakt om het aantal keren dat een bezoeker heeft geconverteerd te beperken.

## Werken optillen en vertrouwen in Ad Hoc en Report Builder? Als het niet inheems is, kan ik het daar zelf doen? {#section_D8BB69AE700B4C5CB5FD28DB51F9A4E9}

Optillen en vertrouwen werken niet in Ad hoc of Report Builder en kunnen niet zelf worden berekend voor doorlopende variabelen. Het is mogelijk om het voor binaire metriek manueel te berekenen.
