---
keywords: faq;veelgestelde vragen;analyses voor doel;a4T;lift;ad hoc;report builder;trust
description: Vind antwoorden op vragen over lift en vertrouwen wanneer het gebruiken van Analytics voor  [!DNL Target]  (A4T). A4T laat u Analytics gebruiken die voor  [!DNL Target]  activiteiten rapporteert.
title: Waar kan ik informatie vinden over optillen en vertrouwen met A4T?
feature: Analytics for Target (A4T)
exl-id: 42fd179b-944a-4a0a-b299-85ea4a7ea244
source-git-commit: aff96eca1380f4274dba0c1567f6e41d42f4b5ab
workflow-type: tm+mt
source-wordcount: '541'
ht-degree: 0%

---

# Optillen en vertrouwen - A4T veelgestelde vragen

Dit onderwerp bevat antwoorden op vragen die vaak worden gesteld over optillen en vertrouwen wanneer u [!DNL Adobe Analytics] als rapportagebron voor [!DNL Adobe Target] (A4T) gebruikt.

## Kan ik off-line berekeningen voor A4T uitvoeren? {#section_55B5B750E17D414CAECBEECE27B15D81}

+++Antwoord
U kunt offlineberekeningen voor A4T uitvoeren, maar het vereist een stap met gegevens het uitvoeren in [!DNL Analytics]. Voor meer informatie, zie [&#x200B; Statistische berekeningen in tests A/Bn &#x200B;](/help/main/c-reports/statistical-methodology/statistical-calculations.md).

+++

## Hoe wordt lift berekend? {#section_8CAE788EED5646C4B1D64A0D22070734}

+++Antwoord
Lift is het percentageverschil tussen uw resultaten van de controlepagina en een succesvolle testvariant.

+++

## Hoe wordt het vertrouwen berekend? {#section_97DB24D833E742988318CA65DA65DAD9}

+++Antwoord
Het betrouwbaarheidsniveau is een waarschijnlijkheid, uitgedrukt als een percentage, dat gelijk is aan `1 - p-value`, waarbij `p-value` wordt berekend op basis van een t-test. Zie [&#x200B; Statistische berekeningen in tests A/Bn &#x200B;](/help/main/c-reports/statistical-methodology/statistical-calculations.md).

+++

## Waarom kan ik geen lift en vertrouwen zien op berekende maatstaven? {#lift-confidence}

+++Antwoord
Berekende metriek worden momenteel niet ondersteund in lift- en betrouwbaarheidsfuncties. Analyses berekenen de meetwaarden op geaggregeerd niveau in plaats van op bezoekersniveau. Vertrouwen is met name een berekening op bezoekersniveau.

Niet-berekende (standaard)gebeurtenissen worden ondersteund in lift en betrouwbaarheid. Zij worden de teller in de lift functie; de teller kan geen berekening zelf zijn. De noemer is de normaliserende metriek (indrukkingen, bezoeken, of bezoekers). Enkele voorbeelden van standaardgebeurtenissen zijn onder andere orders, inkomsten, conversies van activiteiten, aangepaste gebeurtenissen 1-1000, enzovoort. Gemeenschappelijke optimalisatiemetriek, zoals gesprekstarief (Orders/Bezoeker) en RPV (Inkomsten/Bezoeker) worden gesteund in lift en vertrouwen.

Voorbeelden van niet-ondersteunde metriek- of gebruiksgevallen zijn:

* Gemiddelde bestelwaarde (inkomsten/bestelling, per bezoeker). AOV wordt niet ondersteund omdat de teller een berekende metrische waarde is. In plaats daarvan wordt aanbevolen de twee bepalende meeteenheden van AOV - inkomsten per bezoeker en conversietarief in overweging te nemen.
* Berekende metriek die de som van standaardgebeurtenissen zijn. U kunt bijvoorbeeld tien verschillende hoofdformulieren bijhouden in tien aparte gebeurtenissen en deze vervolgens bij elkaar voegen om de totale hoeveelheid verzonden leads te verkrijgen. Een aanbevolen methode om deze gebeurtenissen te volgen, is het implementeren van één enkele gebeurtenis voor het verzenden van leads in Analytics en vervolgens het verzamelen van het type loodformulier met een eVar. Het gebruik van deze methode vereist minder variabelen en zorgt ervoor dat u de enige metrische voorlegging van het lood in lift en vertrouwelijkheidsfuncties kunt gebruiken.

+++

## Hoe verwerkt A4T betrouwbaarheidsberekeningen? {#section_66115EAF1BA34F7A8FCED7B08DA4F99C}

+++Antwoord
[!DNL Adobe Analytics] behandelt alle metriek als niet binair, en daarom, berekent vertrouwen/p-waarden op een manier die aan het gebruik van binaire metriek in een regelmatige t-test verschillend is. Met name kunnen de door A4T gebruikte berekeningen voor elke gebruiker een continu metrisch resultaat opleveren (niet slechts 1 of 0 voor elke gebruiker), zodat de variantie (of een relatant, de standaardafwijking) voor elke ervaring op de juiste wijze moet worden berekend. Extreme bestellingen worden niet in aanmerking genomen. Bovendien wordt bij de berekening van het betrouwbaarheidsinterval geen Bonferroni-correctie toegepast voor meerdere aanbiedingen.

+++

## Werken lift en vertrouwen in Ad Hoc en Report Builder? Als het niet inheems is, kan ik het daar zelf doen? {#section_D8BB69AE700B4C5CB5FD28DB51F9A4E9}

+++Antwoord
Optillen en vertrouwen werken niet in ad hoc of Report Builder en kunnen niet zelf worden berekend voor continue variabelen. Het is mogelijk om het voor binaire metriek manueel te berekenen.
+++
