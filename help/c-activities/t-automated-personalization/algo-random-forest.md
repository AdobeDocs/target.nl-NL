---
keywords: Targeting
description: Het belangrijkste verpersoonlijkingsalgoritme van het doel dat in zowel Automated Personalization als Auto-Doel wordt gebruikt is Willekeurig bos. Met methoden als Random Forest kunt u meerdere leeralgoritmen gebruiken om betere voorspellende prestaties te verkrijgen dan met elk van de deelleeralgoritmen. Het Random Forest-algoritme in Automated Personalization is een classificatie- of regressiemethode die werkt door het aanleggen van een groot aantal beslissingsbomen tijdens de training.
title: Random Forest-algoritme
feature: ap
translation-type: tm+mt
source-git-commit: 968d36d65016e51290f6bf754f69c91fd8f68405
workflow-type: tm+mt
source-wordcount: '1456'
ht-degree: 0%

---


# ![](/help/assets/premium.png) PREMIUMRandom Forest-algoritme{#random-forest-algorithm}

Het belangrijkste verpersoonlijkingsalgoritme van het doel dat in zowel Automated Personalization als Auto-Doel wordt gebruikt is Willekeurig bos. Met methoden als Random Forest kunt u meerdere leeralgoritmen gebruiken om betere voorspellende prestaties te verkrijgen dan met elk van de deelleeralgoritmen. Het Random Forest-algoritme in Automated Personalization is een classificatie- of regressiemethode die werkt door het aanleggen van een groot aantal beslissingsbomen tijdens de training.

Als je aan statistieken denkt, kan één enkel regressiemodel dat wordt gebruikt om een resultaat te voorspellen, in gedachten komen. Het meest recente onderzoek in de gegevenswetenschap suggereert dat &#39;ensemble methods&#39;, waarbij meerdere modellen worden gemaakt op basis van dezelfde gegevensset en vervolgens op intelligente wijze worden gecombineerd, betere resultaten opleveren dan op basis van één enkel model voorspeld.

Het Random Forest-algoritme is het belangrijkste onderliggende personalisatiealgoritme dat wordt gebruikt in Automated Personalization- en Auto-Target-activiteiten. Willekeurig bos combineert honderden beslissingsbomen om tot een betere voorspelling te komen dan één boom op zich zou kunnen maken.

## Wat is een beslissingsstructuur? {#section_7F5865D8064447F4856FED426243FDAC}

Het doel van een beslissingsboom is alle beschikbare bezoekgegevens te verdelen een systeem van kan leren en dan die gegevens groeperen, waar de bezoeken binnen elke groep zo gelijkaardig mogelijk aan elkaar met betrekking tot het doel metrisch zijn. Over de groepen heen zijn de bezoeken echter zo verschillend mogelijk wat betreft het meetdoel (bv. de omrekeningskoers). In de beslissingsstructuur wordt gekeken naar de verschillende variabelen in de trainingsreeks om te bepalen hoe de gegevens op een MECE-manier (wederzijds-exclusief-collectief-uitputtend) in deze groepen (of &quot;bladeren&quot;) moeten worden gesplitst om dit doel te bereiken.

In een eenvoudig voorbeeld, veronderstellen wij slechts twee inputvariabelen hebben:

* Geslacht (met twee potentiële waarden, mannen of vrouwen)
* Postcode (met vijf mogelijke waarden in onze kleine gegevensset: (11111, 2222, 3333, 4444 of 55555)

Als ons doel metrisch omzetting is, dan zou de boom eerst bepalen welke van onze twee variabelen de grootste hoeveelheid variatie in de de omzettingssnelheid van bezoekgegevens verklaart.

ZIP-code is het meest voorspellend. Deze variabele zou dan de eerste &quot;tak&quot;van de boom vormen. De beslissingsstructuur zou vervolgens bepalen hoe de bezoekgegevens moeten worden gesplitst, zoals de omrekeningskoers van de records in elke splitsing zo vergelijkbaar mogelijk was, en de omrekeningskoers tussen de splitsingen zo verschillend mogelijk. In ons voorbeeld gaan we ervan uit dat 11111, 2222, 33333 één splitsing zijn en dat 4444 en 55555 een tweede splitsing.

Deze actie zou in de eerste laag van onze beslissingsboom resulteren:

![](assets/decsion_tree_1.png)

De beslissingsboom stelde de vraag: &quot;Wat is de meest voorspellende variabele?&quot; In ons voorbeeld hebben we maar twee variabelen, dus het antwoord is duidelijk gender. De boom zal nu een gelijkaardige oefening voltooien om de gegevens *binnen elke tak* te verdelen. Laten we eerst eens kijken naar de vertakking 1111, 2222 en 33333. In deze postcodes, als er een verschil is in conversie tussen mannen en vrouwen, dan zouden er twee bladeren (mannen en vrouwen) zijn, en deze tak zou compleet zijn. In de andere tak, 44444 en 55555, gaan we ervan uit dat er geen statistisch verschil is tussen de manier waarop vrouwen en mannen zich omzetten. In dit geval wordt de eerste vertakking de laatste splitsing.

Ons voorbeeld zou in de volgende boom resulteren:

![](assets/decsion_tree_2.png)

## Hoe worden Besluit Trees gebruikt door Random Forest? {#section_536C105EF9F540C096D60450CAC6F627}

Beslissingsbomen kunnen een krachtig statistisch instrument zijn. Ze hebben echter enkele nadelen. Het meest kritiek, kunnen zij de gegevens &quot;overdreven-passen&quot;zodat een individuele boom slecht toekomstige gegevens voorspelt die niet werden gebruikt om de aanvankelijke boom te bouwen. Deze uitdaging wordt de [bias-variance handelsoff](https://en.wikipedia.org/wiki/Bias%E2%80%93variance_tradeoff) in statistisch leren genoemd. Willekeurige bossen helpen deze overijdelingsuitdaging te overwinnen. Op het hoogste niveau is een willekeurig bos een verzameling beslissingsbomen die iets anders worden gebouwd op dezelfde gegevensset die samen &quot;stemmen&quot; om een beter model te krijgen dan een individuele boom. De bomen worden aangelegd door willekeurig een deelverzameling bezoeken met vervangingen (zogenaamde bagging) te selecteren en door willekeurig een deelverzameling van de kenmerken te selecteren, zodat het bos uit iets verschillende beslissingsbomen bestaat. Deze methode introduceert kleine variaties in de bomen die in het Willekeurige Bos worden gecreeerd. Door deze gecontroleerde hoeveelheid variantie toe te voegen, verbetert u de voorspellende nauwkeurigheid van het algoritme.

## Hoe gebruiken de Algoritmen van de Aanpassing van het Doel Willekeurig Bos? {#section_32FB53CAD8DF40FB9C0F1217FBDBB691}

**Hoe modellen worden gebouwd**

Het volgende diagram vat samen hoe de modellen voor auto-Doel of de activiteiten van Automated Personalization worden gebouwd:

![](assets/random_forest_flow.png)

1. Het doel verzamelt gegevens over bezoekers terwijl willekeurig het dienen ervaringen/aanbiedingen
1. Nadat Target een kritieke massa aan gegevens heeft bereikt, voert het functietechniek uit
1. Doel bouwt Willekeurige modellen van het Bos voor elke ervaring/aanbieding
1. Doel controleert of het model voldoet aan een drempelkwaliteitsscore
1. Het doel duwt het model aan productie om toekomstig verkeer te personaliseren

Het doel gebruikt automatisch gegevens het verzamelt, evenals douanegegevens die door u worden verstrekt, om zijn verpersoonlijkingsalgoritmen te bouwen. Deze modellen voorspellen de beste ervaring of de beste aanbieding aan bezoekers te tonen. Over het algemeen wordt één model per ervaring (als een activiteit van het auto-Doel) of per aanbieding (als een activiteit van Automated Personalization) gebouwd. Doel kiest er vervolgens voor de ervaring of het aanbod weer te geven die de hoogst voorspelde succesmaatstaf oplevert (bv. conversiesnelheid). Deze modellen moeten worden opgeleid bij willekeurig bezochte bezoeken voordat ze kunnen worden gebruikt voor voorspellingen. Als een activiteit voor het eerst begint, worden zelfs bezoekers die deel uitmaken van de gepersonaliseerde groep willekeurig verschillende ervaringen of aanbiedingen getoond totdat de verpersoonlijkingsalgoritmen klaar zijn.

Elk model moet worden gevalideerd om te kunnen bepalen of het goed is in het voorspellen van het gedrag van bezoekers voordat het in uw activiteit wordt gebruikt. Modellen worden gevalideerd op basis van hun AUC (oppervlak onder de curve). Wegens de behoefte aan bevestiging, is het nauwkeurige tijdstip wanneer een model zal beginnen het dienen van gepersonaliseerde ervaringen afhankelijk van de details van de gegevens. In de praktijk, en voor verkeer planningsdoeleinden, neemt het gewoonlijk meer dan het minimumaantal omzettingen alvorens elk model geldig is.

Wanneer een model geldig wordt voor een ervaring of een aanbieding, verandert het klokpictogram links van ervaring/aanbiedingsnaam in groen checkbox. Wanneer er geldige modellen voor minstens twee ervaringen/aanbiedingen zijn, beginnen sommige bezoeken gepersonaliseerd te worden.

**Functietransformatie **

Voordat de gegevens door het verpersoonlijkingsalgoritme gaan, ondergaat het een eigenschaptransformatie, die kan worden overwogen om de gegevens te prepping die in de opleidingsverslagen voor gebruik door de verpersoonlijkingsmodellen worden verzameld.

De eigenschaptransformaties hangen van het type van attribuut af. Vooral zijn er twee soorten kenmerken (of &quot;eigenschappen&quot; zoals soms beschreven door wetenschappers):

* **Categorisch:** Categorische functies kunnen niet worden geteld, maar kunnen in verschillende groepen worden gesorteerd. Het kunnen kenmerken zijn zoals land, geslacht of postcode.
* **Numeriek -** Numerieke kenmerken kunnen worden gemeten of geteld, zoals leeftijd, inkomen, enzovoort.

Voor categoriale functies blijft een set van alle mogelijke functies behouden en wordt de waarschijnlijke transformatie gebruikt om de gegevensgrootte te reduceren. Voor numerieke functies zorgt het opnieuw schalen ervoor dat de functies over de hele linie vergelijkbaar zijn.

**Een evenwicht vinden tussen leren en personaliseren met de Multi-Armed Bandit**

Nadat het Doel verpersoonlijkingsmodellen heeft die worden gebouwd om uw verkeer te personaliseren, is er een duidelijke compensatie u voor toekomstige bezoekers aan uw activiteit wordt geconfronteerd: moet u al verkeer personaliseren dat op het huidige model wordt gebaseerd of moet u van nieuwe bezoekers blijven leren door hen willekeurig aanbiedingen te dienen? U wilt ervoor zorgen het verpersoonlijkingsalgoritme altijd over nieuwe tendensen in uw bezoekers leert, terwijl het personaliseren van het grootste deel van het verkeer.

De multi-armbandit is hoe het Doel u helpt dit doel te bereiken. De multi-armbandit verzekert het model altijd &quot;bestedend&quot;een klein fractie verkeer om door het leven van het activiteit leren te blijven leren en overexploitatie van eerder geleerde tendensen te verhinderen.

In de wereld van de data-wetenschap is het probleem van de multi-gewapende bandit (MAB) een klassiek voorbeeld van het dilemma van exploratie versus uitbuiting waarin een inzameling van één-gewapende bandieten, elk met onbekende beloningswaarschijnlijkheid, wordt gegeven. Het belangrijkste idee is om een strategie te ontwikkelen die uitmondt in de arm met de grootste kans op succes, zodat de totale verkregen beloning gemaximaliseerd wordt. Meervoudig bewapende bandit wordt in het systeem gebruikt wanneer voor online scoring nadat de onlinemodellen zijn gemaakt. Dit helpt bij online leren tijdens de exploratie. Het huidige veelbewapende algoritme is het vettige epsilon-algoritme. In dit algoritme, met waarschijnlijkheid 1- en 0,5 wordt de beste arm gekozen. En bij waarschijnlijkheidspreuk wordt elke andere arm willekeurig gekozen.
