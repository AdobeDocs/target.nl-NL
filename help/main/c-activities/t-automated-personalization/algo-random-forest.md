---
keywords: willekeurig bos;beslissingsboom;ap;Automated Personalization
description: Leer hoe  [!DNL Adobe Target]  het Random Bos algoritme in zowel [!UICONTROL Automated Personalization] (AP) als [!UICONTROL Auto-Target] activiteiten gebruikt.
title: Hoe gebruikt  [!DNL Target]  het Willekeurige Bosalgoritme?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=nl-NL#premium newtab=true" tooltip="Kijk wat er in Target Premium is opgenomen."
feature: Automated Personalization
exl-id: 07a89525-4071-4434-ac96-c59a4f4422ad
source-git-commit: d5b24f298ae405d57c2ba639082cbe99c4e358fd
workflow-type: tm+mt
source-wordcount: '1413'
ht-degree: 0%

---

# Random Forest-algoritme

Het belangrijkste verpersoonlijkingsalgoritme dat in zowel (AP) als [!DNL Auto-Target] activiteiten wordt gebruikt is Random Forest. Met methoden zoals Random Forest kunt u meerdere leeralgoritmen gebruiken om betere voorspellende prestaties te verkrijgen dan met elk van de deelleeralgoritmen. Het algoritme Random Forest in [!UICONTROL Automated Personalization] en [!UICONTROL Auto-Target] is een classificatie- of regressiemethode die werkt door een groot aantal beslissingsbomen te maken wanneer deze wordt getraind.

Als je aan statistieken denkt, kan één enkel regressiemodel dat wordt gebruikt om een resultaat te voorspellen, in gedachten komen. Het meest recente onderzoek in de gegevenswetenschap suggereert dat &#39;ensemble methods&#39;, waarbij meerdere modellen worden gemaakt op basis van dezelfde gegevensset en vervolgens op intelligente wijze worden gecombineerd, betere resultaten opleveren dan op basis van één enkel model voorspeld.

Het Random Forest-algoritme is het belangrijkste onderliggende verpersoonlijkingsalgoritme dat wordt gebruikt in [!UICONTROL Automated Personalization] - en [!UICONTROL Auto-Target] -activiteiten. Willekeurig bos combineert honderden beslissingsbomen om tot een betere voorspelling te komen dan één boom op zich zou kunnen maken.

## Wat is een beslissingsboom? {#section_7F5865D8064447F4856FED426243FDAC}

Het doel van een beslissingsboom is alle beschikbare bezoekgegevens te verdelen een systeem van kan leren en dan dat gegevens groeperen, waarin de bezoeken binnen elke groep zo gelijkaardig mogelijk aan elkaar met betrekking tot het doel metrisch zijn. Over groepen heen zijn de bezoeken echter zo verschillend mogelijk wat betreft de maatstaf van het doel (bijvoorbeeld de omrekeningskoers). In de beslissingsstructuur wordt gekeken naar de verschillende variabelen in de trainingsreeks om te bepalen hoe de gegevens op een MECE-manier (Mutual Exclusive Collective Exhaustive) in deze groepen (of &quot;bladeren&quot;) worden gesplitst om dit doel te bereiken.

In een eenvoudig voorbeeld, veronderstellen wij twee inputvariabelen:

* Geslacht (met twee potentiële waarden, mannen of vrouwen)
* Postcode (met vijf mogelijke waarden in de kleine gegevensset: 11111, 2222, 3333, 44444 of 5555)

Als doel metrisch omzetting is, dan zou de boom eerst bepalen welke van de twee variabelen de grootste hoeveelheid variatie in de de omzettingssnelheid van bezoekgegevens verklaart.

ZIP-code is het meest voorspellend. Deze variabele zou dan de eerste &quot;tak&quot;van de boom vormen. De beslissingsstructuur zou vervolgens bepalen hoe de bezoekgegevens moeten worden gesplitst, zoals de omrekeningskoers van de records in elke splitsing zo vergelijkbaar mogelijk was, en de omrekeningskoers tussen de splitsingen zo verschillend mogelijk. In dit voorbeeld wordt ervan uitgegaan dat 11111, 2222, 33333 één splitsing zijn en dat 44444 en 55555 een tweede splitsing.

Deze actie resulteert in de eerste laag van de beslissingsboom:

![&#x200B; decsion_tree_1 beeld &#x200B;](assets/decsion_tree_1.png)

De beslissingsboom stelt de vraag: &quot;Wat is de meest voorspellende variabele?&quot; In dit voorbeeld zijn er slechts twee variabelen, dus het antwoord hier is duidelijk gender. De boom kijkt nu om een gelijkaardige oefening te voltooien om de gegevens *binnen elke tak* te verdelen. Laten we eerst eens kijken naar de vertakking 1111, 2222 en 33333. In deze postcodes, als er een verschil is in conversie tussen mannen en vrouwen, dan zouden er twee bladeren (mannen en vrouwen) zijn, en deze tak zou compleet zijn. In de andere takken, 44444 en 55555, gaan we ervan uit dat er geen statistisch verschil is tussen de manier waarop vrouwen en mannen zich omzetten. In dit geval wordt de eerste vertakking de laatste splitsing.

Het voorbeeld resulteert in de volgende boomstructuur:

![&#x200B; decsion_tree_2 beeld &#x200B;](assets/decsion_tree_2.png)

## Hoe worden beslissingsbomen gebruikt door Random Forest? {#section_536C105EF9F540C096D60450CAC6F627}

Beslissingsbomen kunnen een krachtig statistisch instrument zijn. Ze hebben echter enkele nadelen. Het meest kritiek, kunnen zij de gegevens &quot;overdreven-passen&quot;zodat een individuele boom slecht toekomstige gegevens voorspelt die niet werden gebruikt om de aanvankelijke boom te bouwen. Deze uitdaging is gekend als [&#x200B; bias-variantie handel &#x200B;](https://en.wikipedia.org/wiki/Bias%E2%80%93variance_tradeoff) in het statistische leren. Willekeurige bossen helpen deze overdreven passende uitdaging het hoofd te bieden. Op het hoogste niveau is een willekeurig bos een verzameling beslissingsbomen die iets anders worden gebouwd op dezelfde gegevensset die samen &quot;stemmen&quot; om een beter model te krijgen dan een individuele boom. De bomen worden gebouwd door willekeurig een subset van bezoeken te selecteren met vervangingen (bekend als bagging) en willekeurig een subset van de kenmerken te selecteren, zodat het bos uit iets verschillende beslissingsbomen bestaat. Deze methode introduceert kleine variaties in de bomen die in het Willekeurige Bos worden gecreeerd. Door deze gecontroleerde hoeveelheid variantie toe te voegen, verbetert u de voorspellende nauwkeurigheid van het algoritme.

## Hoe gebruiken de [!DNL Target] verpersoonlijkingsalgoritmen Random Forest? {#section_32FB53CAD8DF40FB9C0F1217FBDBB691}

### Hoe modellen worden gebouwd

In het volgende diagram wordt een overzicht gegeven van de manier waarop modellen voor [!UICONTROL Auto-Target] - en [!UICONTROL Automated Personalization] -activiteiten zijn gemaakt:

![&#x200B; random_forest_flow beeld &#x200B;](assets/random_forest_flow.png){width="650" zoomable="yes"}

1. Het doel verzamelt gegevens over bezoekers terwijl willekeurig het dienen ervaringen of aanbiedingen
1. Nadat [!DNL Target] een kritische massa aan gegevens heeft bereikt, voert [!DNL Target] functietechniek uit
1. [!DNL Target] maakt Willekeurige Forest-modellen voor elke ervaring of aanbieding
1. [!DNL Target] controleert of het model voldoet aan een drempelkwaliteitsscore
1. [!DNL Target] zet het model op productie om toekomstig verkeer te personaliseren

[!DNL Target] gebruikt automatisch gegevens die het verzamelt, en douanegegevens die door u worden verstrekt, om zijn verpersoonlijkingsalgoritmen te bouwen. Deze modellen voorspellen de beste ervaring of de beste aanbieding aan bezoekers te tonen. Over het algemeen wordt één model gemaakt per ervaring (als een [!UICONTROL Auto-Target] activiteit) of per aanbieding (als een [!UICONTROL Automated Personalization] activiteit). [!DNL Target] geeft vervolgens de ervaring of aanbieding weer die de hoogst voorspelde succesfactor oplevert (bijvoorbeeld de conversiesnelheid). Deze modellen moeten worden opgeleid bij willekeurig bezochte bezoeken voordat ze kunnen worden gebruikt voor voorspellingen. Als een activiteit voor het eerst begint, worden zelfs bezoekers die deel uitmaken van de gepersonaliseerde groep willekeurig verschillende ervaringen of aanbiedingen getoond totdat de verpersoonlijkingsalgoritmen klaar zijn.

Elk model moet worden gevalideerd om te kunnen bepalen of het goed is in het voorspellen van het gedrag van bezoekers voordat het in uw activiteit wordt gebruikt. Modellen worden gevalideerd op basis van het gebied onder de curve (AUC). Wegens de behoefte aan bevestiging, hangt het nauwkeurige tijdstip wanneer een model begint te dienen gepersonaliseerde ervaringen van de details van de gegevens af. In de praktijk, en voor verkeer planningsdoeleinden, neemt het gewoonlijk meer dan het minimumaantal omzettingen alvorens elk model geldig is.

Wanneer een model geldig wordt voor een ervaring of een aanbieding, verandert het klokpictogram links van ervaring/aanbiedingsnaam in groen checkbox. Wanneer er geldige modellen voor minstens twee ervaringen of aanbiedingen zijn, beginnen sommige bezoeken gepersonaliseerd te worden.

### Eigenschaptransformatie

Voordat de gegevens door het verpersoonlijkingsalgoritme gaan, ondergaat het een eigenschaptransformatie, die kan worden overwogen om de gegevens te prepping die in de opleidingsverslagen voor gebruik door de verpersoonlijkingsmodellen worden verzameld.

De eigenschaptransformaties hangen van het type van attribuut af. Vooral zijn er twee soorten kenmerken (of &quot;eigenschappen&quot; zoals soms beschreven door wetenschappers):

* **Categorisch:** de Categorische eigenschappen kunnen niet worden geteld maar kunnen in verschillende groepen worden gesorteerd. Het kunnen kenmerken zijn zoals land, geslacht of postcode.
* **Numeriek:** de numerieke eigenschappen kunnen worden gemeten of, zoals leeftijd, inkomen, etc. worden geteld.

Voor categoriale functies blijft een set van alle mogelijke functies behouden en wordt de waarschijnlijke transformatie gebruikt om de gegevensgrootte te reduceren. Voor numerieke functies zorgt het opnieuw schalen ervoor dat de functies over de hele linie vergelijkbaar zijn.

### Het in evenwicht brengen van leren tegenover het personaliseren met de multi-gewapende bandit

Nadat [!DNL Target] verpersoonlijkingsmodellen heeft die worden gebouwd om uw verkeer te personaliseren, is er een duidelijke compensatie voor toekomstige bezoekers aan uw activiteit die wordt geconfronteerd. Moet u al verkeer personaliseren dat op het huidige model wordt gebaseerd of zou u van nieuwe bezoekers moeten blijven leren door hen willekeurig aanbiedingen te dienen? U wilt ervoor zorgen het verpersoonlijkingsalgoritme altijd over nieuwe tendensen in uw bezoekers leert, terwijl het personaliseren van het grootste deel van het verkeer.

De bandit met meerdere armen is hoe [!DNL Target] u helpt dit doel te bereiken. De multi-armbandit zorgt ervoor dat het model altijd een klein fractie verkeer &quot;uitgeeft&quot;om door het leven van het activiteit leren te blijven leren en overexploitatie van eerder geleerde tendensen te verhinderen.

In de wereld van de data-wetenschap is het veelbewapende bankenprobleem een klassiek voorbeeld van het dilemma van exploratie versus uitbuiting waarin een inzameling van één-gewapende bandieten, elk met onbekende beloningswaarschijnlijkheid, wordt gegeven. Het belangrijkste idee is om een strategie te ontwikkelen die uitmondt in de arm met de grootste kans op succes, zodat de totale verkregen beloning gemaximaliseerd wordt. Meervoudig bewapende bandit wordt in het systeem gebruikt voor online scoring nadat de onlinemodellen zijn gemaakt. Dit proces helpt bij online leren tijdens de exploratie. Het huidige veelbewapende algoritme is een epsilon (estimé) greedy algoritme. In dit algoritme, met waarschijnlijkheid 1- en 0,5 wordt de beste arm gekozen. En bij waarschijnlijkheidspreuk wordt elke andere arm willekeurig gekozen.
