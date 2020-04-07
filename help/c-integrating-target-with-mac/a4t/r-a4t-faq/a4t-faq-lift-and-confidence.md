---
keywords: faq;frequently asked questions;analytics for target;a4T;lift;ad hoc;report builder;confidence
description: Dit onderwerp bevat antwoorden op vragen die vaak over lift en vertrouwen worden gevraagd wanneer het gebruiken van Analytics als rapporteringsbron voor Doel (A4T).
title: Optillen en vertrouwen - A4T veelgestelde vragen
topic: Standard
uuid: 7d0402f3-d6f2-422e-b69c-86e10120ac83
translation-type: tm+mt
source-git-commit: b5191230c76135d5299754e72c9651d018086e60

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

Lift en Trust worden momenteel niet ondersteund met berekende meetwaarden. In de meeste gevallen zou dit echter geen probleem mogen zijn omdat de in het A4T-rapport berekende omrekeningskoers reeds een berekende maatstaf is waarin de noemer de normaliserende maatstaf is (instanties, bezoeken, bezoekers). Als u bijvoorbeeld de metrische volgorde van de bestellingen selecteert en de normalisatie-instelling bezoekers is, wordt de conversiesnelheid (bestellingen/bezoeker) automatisch berekend via A4T-rapportage. De resulterende lift weerspiegelt het verschil in die conversiesnelheid over de tekstervaringen in vergelijking met de standaardwaarde.

De meeste berekende maatstaven voor optimalisatie vallen in één van twee categorieën: statistische gegevens, en andere omzettingsberekeningen zoals Gemiddelde Waarde van de Orde (AOV).

Samengevoegde metriek worden gebruikt wanneer een organisatie unieke gebeurtenissen gebruikt om verschillende &quot;flavors&quot;van sparen omzetting te vangen. Als uw doel bijvoorbeeld het verzenden van formulieren met leads is en u hebt 10 verschillende hoofdformulieren, kan een bedrijf unieke gebeurtenissen maken om elk type formulierconversie te tellen. Om de totale hoeveelheid van alle ingediende loodformulieren te kunnen zien, moeten deze een eenvoudige, berekende maatstaf maken om ze bij elkaar op te tellen. Een betere, modernere manier om dit te volgen is één enkele gebeurtenis van de loodvoorlegging in Analytics uit te voeren en dan een eVar te gebruiken om het type van loodvorm te verzamelen. Het gebruik van deze methode vereist minder variabelen en elimineert de behoefte om individuele metriek samen te voegen en u hebt nog de capaciteit om holistische loodvormomzetting te zien en het te verdelen door type van loodvorm gebruikend eVar. Dit elimineert ook de behoefte aan gezamenlijke metriek wanneer het evalueren van de prestaties van een Activiteit van het Doel.

Een andere algemeen berekende metrische waarde, Gemiddelde Waarde van de Orde, wordt momenteel niet gesteund met lift &amp; vertrouwen omdat normaliserend metrisch geen standaardmetrisch is (instanties, bezoeken, bezoekers). In plaats daarvan wordt aanbevolen de twee bepalende meetwaarden van AOV, de inkomsten per bezoeker en de omrekeningskoers in de gaten te houden.

## Hoe verwerkt A4T betrouwbaarheidsberekeningen? {#section_66115EAF1BA34F7A8FCED7B08DA4F99C}

A4T gebruikt niet-binaire metrische berekeningen met de som van vierkante gegevens. De variantie wordt berekend met de som van de gegevens van de vierkanten. Extreme bestellingen worden niet in aanmerking genomen.

Om het even welk segment van Analytics kan op het rapport worden toegepast. Zo krijgt u de &quot;extreme volgorde&quot; onder andere segmentopties. Een metrische waarde kan ook worden gemaakt om het aantal keren dat een bezoeker heeft geconverteerd te beperken.

## Werken optillen en vertrouwen in Ad Hoc en Report Builder? Als het niet inheems is, kan ik het daar zelf doen? {#section_D8BB69AE700B4C5CB5FD28DB51F9A4E9}

Optillen en vertrouwen werken niet in Ad hoc of Report Builder en kunnen niet zelf worden berekend voor doorlopende variabelen. Het is mogelijk om het voor binaire metriek manueel te berekenen.
