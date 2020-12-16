---
keywords: recommendation key;recommendation logic;current category;custom attribute;last purchased item;last viewed item;most viewed item;most viewed item;favorite category;popularity;recently viewed item;last purchased;last viewed;most viewed;favorite;recently viewed
description: Recommendations op basis van sleutels gebruikt de gedragscontext van de bezoeker om relevante resultaten te tonen in Adobe Target Recommendations-activiteiten.
title: De aanbeveling baseren op een aanbevelingen
feature: criteria
mini-toc-levels: 2
translation-type: tm+mt
source-git-commit: 381c405e55475f2474881541698d69b87eddf6fb
workflow-type: tm+mt
source-wordcount: '2727'
ht-degree: 0%

---


# De aanbeveling baseren op een aanbevelingen

Recommendations gebaseerd op sleutels gebruikt de context van het bezoekersgedrag om relevante resultaten in [!DNL Adobe Target] [!DNL Recommendations] activiteiten te tonen.

Er zijn twee typen Recommendations:

* **Populariteit:** geeft items weer op basis van de opties Meest bekeken, Boven verkocht en Metrisch boven. De sleutel is leeg voor populiteitscriteria.
* **Op sleutel gebaseerd:** Omvat de rest van de criteria. Recommendations biedt verschillende keuzemogelijkheden met betrekking tot het sleuteltype. De opties variëren van &quot;huidig punt&quot;tot &quot;profielparameters,&quot;die u toestaan om de sleutel van de waarden programmatically te plaatsen aan te bevelen. U kunt meerdere criteria op elkaar testen door de criteria op een andere toets te baseren.

Elk criterium wordt gedefinieerd in een eigen tabblad. Het verkeer wordt gelijkmatig verdeeld over uw verschillende criteria testen. Met andere woorden, als je twee criteria hebt, is het verkeer in gelijke mate verdeeld. Als u twee criteria en twee ontwerpen hebt, wordt het verkeer gelijkmatig verdeeld tussen de vier combinaties. U kunt ook een percentage bezoekers van de site opgeven die de standaardinhoud ter vergelijking zien. In dat geval ziet het opgegeven percentage bezoekers de standaardinhoud en worden de rest opgedeeld tussen uw criteria en ontwerpcombinaties.

1. Maak nieuwe criteria of selecteer een bestaand criterium en klik op **[!UICONTROL Edit]**.
1. Als u de aanbevolen toets wilt wijzigen, selecteert u de nieuwe toets in de vervolgkeuzelijst [!UICONTROL Recommendation Key] en klikt u op **[!UICONTROL Save]** of **[!UICONTROL Update]**.

   Omdat verschillende logica aan verschillende aanbevelingen sleutels in kaart brengt, lenen de verschillende aanbevelingen zich aan plaatsing op verschillende types van pagina&#39;s. Raadpleeg de volgende secties voor meer informatie over elke advisesleutel.

## Aanbevolen toetsen

De volgende aanbevelingen zijn beschikbaar in de vervolgkeuzelijst [!UICONTROL Recommendation Key]:

### Huidig item {#current-item}

De aanbeveling wordt bepaald door het item dat de bezoeker momenteel bekijkt.

Recommendations geeft andere objecten weer die bezoekers interesseren voor het opgegeven object.

Wanneer deze optie is geselecteerd, moet de waarde `entity.id` als parameter in de vertoningsdoos worden overgegaan.

#### Logica (criteria)

* [!UICONTROL Items with similar attributes]
* [!UICONTROL People Who Viewed This, Viewed That]
* [!UICONTROL People Who Viewed This, Bought That]
* [!UICONTROL People Who Bought This, Bought That]
* [!UICONTROL Site Affinity]

#### Waar op uw site gebruiken

* Pagina&#39;s met één item, zoals productpagina&#39;s.
* Niet gebruiken op pagina&#39;s met zoekresultaten die null zijn.

### Huidige categorie {#current-category}

De aanbeveling wordt bepaald door de productcategorie die de bezoeker momenteel bekijkt.

Recommendations geeft objecten weer in de opgegeven productcategorie.

Wanneer deze optie is geselecteerd, moet de waarde `entity.categoryId` als parameter aan de vertoningsdoos worden overgegaan.

#### Logica (criteria)

* Topverkopers
* Meest bekeken

#### Waar op uw site gebruiken

* Pagina&#39;s van één categorie.
* Niet gebruiken op pagina&#39;s met zoekresultaten die null zijn.

### Aangepast kenmerk {#custom}

De aanbeveling wordt bepaald door een punt dat in het profiel van een bezoeker, gebruikend één van beide gebruiker wordt opgeslagen.** xorprofiel.** xattributes.

Als deze optie is geselecteerd, moet de waarde `entity.id` aanwezig zijn in het profielkenmerk.

Wanneer u aanbevelingen baseert op douanekenmerken, moet u het douanekenmerk selecteren en dan het aanbevelingstype selecteren.

U kunt filter in real time bovenop uw eigen output van douanecriteria uitvoeren. U kunt bijvoorbeeld de aanbevolen objecten beperken tot objecten van de favoriete rubriek of het favoriete merk van een bezoeker. Dit geeft u de macht om off-line berekeningen met het filtreren in real time te combineren.

Deze functionaliteit betekent dat u [!DNL Target] kunt gebruiken om verpersoonlijking bovenop uw off-line berekende aanbevelingen of douane-gebogen lijsten toe te voegen. Dit combineert de kracht van gegevenswetenschappers en onderzoek met uw beproefde levering, runtime het filtreren, A/B het testen, het richten, het melden, de integratie, en meer.

Met de toevoeging van inclusieregels op de criteria van de Douane, verandert dit anders statische aanbevelingen in dynamische aanbevelingen gebaseerd op de belangen van een bezoeker.

* De criteria van de douane zijn configureerbaar, zoals andere criteria in aanbevelingen.
* U kunt [inzamelingen](/help/c-recommendations/c-products/collections.md), [uitsluitingen](/help/c-recommendations/c-products/exclusions.md), en [inclusies](/help/c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md) (met inbegrip van de speciale regels voor Prijs en Inventaris) op de zelfde manier gebruiken zoals om het even welke andere criteria.

Mogelijke gebruiksgevallen zijn:

* U wilt films aanbevelen vanuit een lijst met aangepaste cursisten, maar alleen als de bezoeker deze nog niet heeft bekeken.
* U wilt een off-line algoritme in werking stellen en de resultaten gebruiken om uw aanbevelingen te aandrijven, maar u moet ervoor zorgen dat de uit-van-voorraad punten nooit worden geadviseerd.
* Je wilt alleen objecten opnemen die afkomstig zijn uit de favoriete rubriek van deze bezoeker.

#### Logica (criteria)

* [!UICONTROL People Who Viewed This, Viewed That]
* [!UICONTROL People Who Viewed This, Bought That]
* [!UICONTROL People Who Bought This, Bought That]
* [!UICONTROL Overall behavior]
* [!UICONTROL Most Viewed]
* [!UICONTROL Top Sellers]

Als de sleutel een attribuut van het douaneprofiel is en het algoritmetype Meest bekeken of Hoogste Verkopers is, een nieuwe drop-down lijst die &quot;Groep door Unieke Waarde van&quot;toont die een lijst van bekende entiteitattributen (behalve identiteitskaart, categorie, marge, waarde, inventaris, en milieu) heeft. Dit veld is verplicht.

#### Waar op uw site gebruiken

* Kan op elke pagina worden gebruikt.

#### Aangepaste aanbevelingen

U kunt aanbevelingen op de waarde van een attribuut van het douaneprofiel baseren. Stel dat u aanbevolen films wilt weergeven op basis van de film die een bezoeker het laatst aan zijn of haar wachtrij heeft toegevoegd.

1. Selecteer uw attribuut van het douaneprofiel van **[!UICONTROL Recommendation Key]** drop-down lijst (bijvoorbeeld, &quot;Laatste Show die aan Controlelijst wordt toegevoegd&quot;).
1. Selecteer vervolgens uw **[!UICONTROL Recommendation Logic]** (bijvoorbeeld &quot;Personen die dit hebben bekeken, hebben dat weergegeven&quot;).

   ![Nieuwe criteria maken, dialoogvenster](/help/c-recommendations/c-algorithms/assets/create-new-criteria-1.png)

Als uw attribuut van het douaneprofiel niet direct met één enkele entiteitidentiteitskaart aanpast, is het noodzakelijk om aan [!DNL Recommendations] uit te leggen hoe u de gelijke aan een entiteit wilt voorkomen. Stel dat u bijvoorbeeld de meest verkochte objecten van het favoriete merk van een bezoeker wilt weergeven.

1. Selecteer uw attribuut van het douaneprofiel van **[!UICONTROL Recommendation Key]** drop-down lijst (bijvoorbeeld, &quot;Favoriete Merk&quot;).

1. Selecteer vervolgens **[!UICONTROL Recommendation Logic]** die u met deze sleutel wilt gebruiken (bijvoorbeeld &quot;Topverkopers&quot;).

   De optie [!UICONTROL Group By Unique Value Of] wordt weergegeven.

1. Selecteer het entiteitskenmerk dat overeenkomt met de gekozen sleutel. In dit geval komt &quot;Favoriete merk&quot; overeen met `entity.brand`.

   [!DNL Recommendations] produceert nu een lijst met topverkopers voor elk merk en geeft de bezoeker de juiste lijst met topverkopers weer op basis van de waarde die is opgeslagen in het kenmerk Favoriete merk van de bezoeker.

   ![Nieuwe criteria maken, dialoogvenster 2](/help/c-recommendations/c-algorithms/assets/create-new-criteria-2.png)

### Favoriete categorie {#favorite-category}

De aanbeveling wordt bepaald door de categorie die de meeste activiteit heeft ontvangen, gebruikend de zelfde methode die voor &quot;het meest bekeken punt&quot;wordt gebruikt behalve dat de categorieën in plaats van producten worden gescoord.

Dit wordt bepaald aan de hand van de recenentie-/frequentiecriteria die als volgt werken:

* 10 punten voor de weergave van de eerste categorie
* 5 punten voor elke volgende weergave

De categorieën die voor het eerst worden bezocht, krijgen 10 punten. 5 punten voor latere bezoeken aan dezelfde categorie. Bij elk bezoek worden niet-huidige categorieën die eerder zijn bekeken, verlaagd met 1.

Als u bijvoorbeeld CategorieA en daarna CategorieB in één sessie weergeeft, resulteert dit in A: 9, B: 10 Als u dezelfde items in de volgende sessie bekijkt, veranderen de waarden in A: 20 B: 9.

#### Logica (criteria)

* [!UICONTROL Top Sellers]
* [!UICONTROL Most Viewed]

#### Waar op uw site gebruiken

* Algemene pagina&#39;s, zoals startpagina&#39;s of bestemmingspagina&#39;s en offsite advertenties.

### Laatste aangeschafte item {#last-purchased}

De aanbeveling wordt bepaald door het laatste item dat door elke unieke bezoeker is aangeschaft. Dit wordt automatisch vastgelegd, zodat er geen waarden op de pagina hoeven te worden doorgegeven.

#### Logica (criteria)

* [!UICONTROL Items with similar attributes]
* [!UICONTROL People Who Viewed This, Viewed That]
* [!UICONTROL People Who Viewed This, Bought That]
* [!UICONTROL People Who Bought This, Bought That]
* [!UICONTROL Site Affinity]

#### Waar op uw site gebruiken

* Homepage, pagina Mijn account, offsite advertenties.
* Niet gebruiken op productpagina&#39;s of pagina&#39;s die relevant zijn voor aankopen.

### Laatste weergegeven item {#last-viewed}

De aanbeveling wordt bepaald door het laatste item dat door elke unieke bezoeker is bekeken. Dit wordt automatisch vastgelegd, zodat er geen waarden op de pagina hoeven te worden doorgegeven.

#### Logica (criteria)

* [!UICONTROL Items with similar attributes]
* [!UICONTROL People Who Viewed This, Viewed That]
* [!UICONTROL People Who Viewed This, Bought That]
* [!UICONTROL People Who Bought This, Bought That]
* [!UICONTROL Site Affinity]

#### Waar op uw site gebruiken

* Homepage, pagina Mijn account, offsite advertenties.
* Niet gebruiken op productpagina&#39;s of pagina&#39;s die relevant zijn voor aankopen.

### Meest bekeken item {#most-viewed}

De aanbeveling wordt bepaald door het punt dat het vaakst is bekeken, gebruikend de zelfde methode die voor favoriete categorie wordt gebruikt.

Dit wordt bepaald aan de hand van de recenentie-/frequentiecriteria die als volgt werken:

* 10 punten voor de eerste productweergave
* 5 punten voor elke volgende weergave
* Aan het einde van de sessie worden alle waarden door 2 gedeeld

Als u bijvoorbeeld surfboardA en surfboardB in één sessie weergeeft, resulteert dit in A: 10, B: 5. Wanneer de sessie wordt beëindigd, hebt u een A: 5, B: 2.5 Als u dezelfde items in de volgende sessie bekijkt, veranderen de waarden in A: 15 B: 7.5

#### Logica (criteria)

* [!UICONTROL Items with similar attributes]
* [!UICONTROL People Who Viewed This, Viewed That]
* [!UICONTROL People Who Viewed This, Bought That]
* [!UICONTROL People Who Bought This, Bought That]
* [!UICONTROL Site Affinity]

#### Waar op uw site gebruiken

* Algemene pagina&#39;s, zoals startpagina&#39;s of bestemmingspagina&#39;s en offsite advertenties.

### Populariteit {#popularity}

De aanbeveling wordt bepaald door de populariteit van objecten op uw site. De populariteit omvat topverkopers en hoogste bekeken door mbox gegevens en, als u Adobe Analytics gebruikt, alle metriek beschikbaar in het productrapport. De items worden gerangschikt op basis van de door u geselecteerde logica voor aanbevelingen.

#### Logica (criteria)

* [!UICONTROL Top Sellers]
* [!UICONTROL Most Viewed]
* Metrische gegevens van productrapporten (als u Adobe Analytics gebruikt)

#### Waar op uw site gebruiken

* Algemene pagina&#39;s, zoals startpagina&#39;s of bestemmingspagina&#39;s en offsite advertenties.

### Onlangs bekeken items {#recently-viewed}

Gebruikt de geschiedenis van de bezoeker (overspannende zittingen) om de laatste *x* punten voor te stellen de bezoeker, gebaseerd op het aantal groeven in het ontwerp heeft bekeken.

De onlangs Bekeken Criteria van Punten keert resultaten specifiek voor gegeven [milieu](/help/administrating-target/hosts.md) terug. Als twee sites tot verschillende omgevingen behoren en een bezoeker tussen de twee sites schakelt, worden op elke site alleen recent bekeken items van de desbetreffende site weergegeven. Als twee sites zich in dezelfde omgeving bevinden en een bezoeker schakelt tussen de twee sites, ziet de bezoeker dezelfde onlangs weergegeven items voor beide sites.

>[!NOTE]
>
>U kunt de [!UICONTROL Recently Viewed Items] criteria voor reserveaanbevelingen niet gebruiken.

[!UICONTROL Recently Viewed Items]/Media kan worden gefilterd zodat slechts de punten met een bepaald attribuut worden getoond.

* Onlangs bekeken criteria zijn configureerbaar, net als andere criteria in aanbevelingen.
* U kunt [inzamelingen](/help/c-recommendations/c-products/collections.md), [uitsluitingen](/help/c-recommendations/c-products/exclusions.md), en [inclusies](/help/c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md) (met inbegrip van de speciale regels voor Prijs en Inventaris) op de zelfde manier gebruiken zoals om het even welke andere criteria.

Mogelijke gebruiksgevallen zijn:

Een multinationaal bedrijf met meerdere bedrijven kan bezoekers artikelen laten zien over meerdere digitale eigenschappen. In dit geval kunt u de onlangs weergegeven items beperken tot weergave voor de desbetreffende eigenschap waar deze is weergegeven. Hiermee voorkomt u dat onlangs bekeken items worden weergegeven op de site van een andere digitale eigenschap.

#### Waar op uw site gebruiken

* Algemene pagina&#39;s, zoals startpagina&#39;s of bestemmingspagina&#39;s en offsite advertenties.

>[!NOTE]
>
>[!UICONTROL Recently Viewed Items] Hiermee worden zowel de globale instellingen voor uitsluitingen als de geselecteerde verzamelingsinstelling voor de activiteit in acht genomen. Als een item wordt uitgesloten door een algemene uitsluiting of niet in de geselecteerde verzameling voorkomt, wordt het item niet weergegeven. Daarom bij het gebruiken van een [!UICONTROL Recently Viewed Items] criteria, zou de &quot;Alle Inzamelingen&quot;instelling over het algemeen moeten worden gebruikt.

## Instructielogica

[!DNL Target Recommendations] gebruikt geavanceerde algoritmen om te bepalen wanneer de acties van een bezoeker voor de criteria in uw activiteit kwalificeren. De advisesleutel bepaalt de aanbevelingen logische opties die beschikbaar zijn.

De volgende aanbevelingen (criteria) zijn beschikbaar bij [!UICONTROL Recommendation Logic] drop-down lijst:

### Items/media met vergelijkbare kenmerken {#similar-attributes}

Aanbevolen items of media die vergelijkbaar zijn met items of media op basis van de huidige paginageactiviteit of het gedrag van een bezoeker.

Als u Items/media met vergelijkbare kenmerken selecteert, kunt u regels voor gelijkenis van inhoud instellen.

Het gebruik van gelijkenis in de inhoud om aanbevelingen te genereren is vooral effectief voor nieuwe items. Deze worden waarschijnlijk niet weergegeven in aanbevelingen met Personen die dit hebben bekeken, Gezien dat en andere logica die is gebaseerd op gedrag in het verleden. U kunt de gelijkenis van de inhoud ook gebruiken om nuttige aanbevelingen voor nieuwe bezoekers te produceren, die geen vroegere aankopen of andere historische gegevens hebben.

Zie [Vergelijkbare inhoud](/help/c-recommendations/c-algorithms/create-new-algorithm.md#similarity) voor meer informatie.

Deze logica kan met de volgende advisesleutels worden gebruikt:

* Huidig item
* Laatste object aangeschaft
* Laatst weergegeven item
* Meest bekeken item

### Meest bekeken {#most-viewed-logic}

Hiermee geeft u de items of media weer die het vaakst op uw site worden weergegeven.

Met deze logica kunt u aanbevelingen weergeven op basis van de meest bekeken items op uw site om de conversies voor andere items te verhogen. Een mediasite kan bijvoorbeeld op haar homepage aanbevelingen weergeven voor de meest bekeken video&#39;s om bezoekers aan te moedigen aanvullende video&#39;s te bekijken.

Deze logica kan met de volgende advisesleutels worden gebruikt:

* Huidige rubriek
* Aangepast kenmerk
* Favoriete rubriek
* Populariteit

### Mensen die dit hebben gekocht, hebben dat {#bought-bought}

Aanbevolen objecten die het meest door klanten tegelijk met het opgegeven item worden gekocht.

Deze logica retourneert andere producten die mensen hebben gekocht na de aankoop van deze logica. het opgegeven product niet in de resultatenset is opgenomen.

Met deze logica kunt u de mogelijkheden voor cross-selling vergroten door bijvoorbeeld een aanbeveling weer te geven op een overzichtspagina van winkelwagentjes waarin objecten worden weergegeven die andere kopers ook hebben gekocht. Als de bezoeker bijvoorbeeld een pak koopt, kan de aanbeveling extra artikelen weergeven die andere bezoekers samen met het pak hebben gekocht, zoals bijvoorbeeld banden, jurkschoenen en knipsels. Wanneer bezoekers hun aankopen bekijken, geeft u ze aanvullende aanbevelingen.

Deze logica kan met de volgende advisesleutels worden gebruikt:

* Huidig item
* Aangepast kenmerk
* Laatst gekocht object
* Laatst weergegeven item
* Meest bekeken item

### Personen die dit hebben bekeken, hebben dat {#viewed-bought}

raadt objecten aan die het vaakst worden aangeschaft in dezelfde sessie als waarin het opgegeven item wordt weergegeven. Dit criterium retourneert andere producten die mensen hebben aangeschaft nadat deze is bekeken. Het opgegeven product is niet opgenomen in de resultatenset.

Deze logica retourneert andere producten die zijn aangeschaft nadat deze is bekeken. het opgegeven product niet in de resultatenset is opgenomen.

Met deze logica kunt u de mogelijkheden voor cross-selling vergroten door bijvoorbeeld een aanbeveling weer te geven op een productpagina die items weergeeft die andere bezoekers hebben bekeken die het object hebben gekocht. Als de bezoeker bijvoorbeeld een vispool bekijkt, kan de aanbeveling extra items weergeven die andere bezoekers hebben aangeschaft, zoals hakbalken, golven en blaasjes. Wanneer bezoekers door uw site bladeren, geeft u hun aanvullende aankoopaanbevelingen.

Deze logica kan met de volgende advisesleutels worden gebruikt:

* Huidig item
* Aangepast kenmerk
* Laatst gekocht object
* Laatst weergegeven item
* Meest bekeken item

### Personen die dit hebben bekeken, zagen dat {#viewed-viewed}

Hiermee worden items aanbevolen die het vaakst worden weergegeven in dezelfde sessie als waarin het opgegeven item wordt weergegeven.

Deze logica retourneert andere producten die worden weergegeven na het bekijken van deze logica. het opgegeven product niet in de resultatenset is opgenomen.

Met deze logica kunt u aanvullende conversiemogelijkheden creëren door items aan te bevelen die andere bezoekers die een item hebben bekeken, ook hebben weergegeven. Bezoekers die op uw site fietsen bekijken, kunnen bijvoorbeeld ook fietshelmen, fietskits, sloten enzovoort bekijken. U kunt een aanbeveling tot stand brengen gebruikend deze logica die andere producten adviseert om u te helpen opbrengst verhogen.

Deze logica kan met de volgende advisesleutels worden gebruikt:

* Huidig item
* Aangepast kenmerk
* Laatst gekocht object
* Laatst weergegeven item
* Meest bekeken item

### Site-affiniteit {#site-affinity}

Aanbevolen items op basis van de zekerheid van een relatie tussen items. U kunt deze criteria vormen om te bepalen hoeveel gegevens worden vereist alvorens een aanbeveling gebruikend de schuif van de Regels van de Opname wordt voorgesteld. Als u bijvoorbeeld erg sterk selecteert, worden de producten met de grootste zekerheid van een overeenkomst aanbevolen.

Bijvoorbeeld, als u een zeer sterke affiniteit plaatst en uw ontwerp vijf punten omvat, waarvan drie aan de sterkte van verbindingsdrempel voldoen, worden de twee punten die niet aan de minimumsterktevereisten voldoen niet getoond in uw aanbevelingen en door uw bepaalde reservepunten vervangen. De items met de sterkste affiniteit worden eerst weergegeven.

Een online detailhandelaar kan bijvoorbeeld items in volgende bezoeken aanbevelen die een bezoeker in de afgelopen sessies interesseert. De activiteit voor elke sessie van de bezoeker wordt vastgelegd om een affiniteit te berekenen op basis van een recentiemodel en een frequentiemodel. Wanneer deze bezoeker terugkeert naar uw site, wordt de affiniteit van de site gebruikt om aanbevelingen weer te geven op basis van eerdere acties op uw site.

Sommige klanten met diverse productinzamelingen en diverse plaatsgedrag zouden de beste resultaten kunnen krijgen als zij een zwakke plaatsaffiniteit plaatsen.

Deze logica kan met de volgende advisesleutels worden gebruikt:

* Huidig item
* Laatst gekocht object
* Laatst weergegeven item
* Meest bekeken item

### Topverkopers {#top-sellers}

Toont de punten die in de meest voltooide orden inbegrepen zijn. Meerdere eenheden van hetzelfde item in één volgorde worden als één volgorde geteld.

Met deze logica kunt u aanbevelingen maken voor de meest verkochte items op uw site om de conversie en de omzet te verhogen. Deze logica is vooral geschikt voor nieuwe bezoekers van uw site.

Deze logica kan met de volgende advisesleutels worden gebruikt:

* Favoriete rubriek
* Populariteit

### Op gebruiker gebaseerde Recommendations {#user-based}

Aanbevolen objecten op basis van de browsergeschiedenis, weergavegeschiedenis en aankoopgeschiedenis van elke bezoeker. Deze objecten worden doorgaans &#39;Aanbevolen voor je&#39; genoemd.

Met deze criteria kunt u persoonlijke inhoud en ervaringen aanbieden aan zowel nieuwe als geretourneerde bezoekers. De lijst met aanbevelingen is gericht op de meest recente activiteit van de bezoeker en wordt tijdens de sessie bijgewerkt en wordt meer gepersonaliseerd naarmate de gebruiker door uw site bladert.

Zowel weergaven als aankopen worden gebruikt om de aanbevolen items te bepalen. De opgegeven aanbevelingssleutel (bijvoorbeeld Huidig item) wordt gebruikt om filters toe te passen die u voor de invoegregel selecteert.

U kunt bijvoorbeeld:

* Sluit items uit die niet aan bepaalde criteria voldoen (producten die niet in voorraad zijn, artikelen die meer dan 30 dagen geleden zijn gepubliceerd, films met R enzovoort).
* Beperk opgenomen objecten tot één categorie of tot de huidige categorie.

Deze logica kan met de volgende advisesleutels worden gebruikt:

* Huidig item
* Laatst gekocht object
* Laatst weergegeven item
* Meest bekeken item