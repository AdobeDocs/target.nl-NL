---
keywords: aanbeveling sleutel;aanbeveling logica;huidige categorie;aangepast kenmerk;laatst gekocht item;laatst bekeken item;meest bekeken item;meest bekeken item;favoriete categorie;populariteit;onlangs bekeken item;laatst gekocht;laatst bekeken item;laatst bekeken;meest bekeken;meest bekeken;favoriet;onlangs bekeken
description: Leer hoe u aanbevelingen kunt gebruiken op basis van toetsen die de context van het gedrag van de bezoeker gebruiken om relevante resultaten in [!UICONTROL Recommendations] -activiteiten weer te geven.
title: Hoe baseer ik de [!UICONTROL Recommendation] op een [!UICONTROL Recommendation Key]?
feature: Recommendations
mini-toc-levels: 2
exl-id: 49764f18-88fb-41be-b2a0-e7ced9de742c
source-git-commit: 02ffe8da6cdf96039218656b9690fa719a77910c
workflow-type: tm+mt
source-wordcount: '3463'
ht-degree: 0%

---

# De aanbeveling baseren op een aanbevelingen

Aanbevelingen op basis van algoritmen gebruiken de context van het gedrag van de bezoeker om relevante resultaten in [!DNL Adobe Target] [!DNL Recommendations] -activiteiten weer te geven.

Elk type algoritme verstrekt verschillende algoritmen aangewezen voor zijn type, zoals aangetoond in de volgende lijst:

| Het type Algorithm | Wanneer/Beschikbare algoritmen gebruiken |
| --- | --- |
| [!UICONTROL Cart-Based] | Aanbevelingen doen op basis van de inhoud van het winkelwagentje.<ul><li>[!UICONTROL People Who Viewed These, Also Viewed]</li><li>[!UICONTROL People Who Viewed These, Also Bought]</li><li>[!UICONTROL People Who Bought These, Also Bought]</li></ul> |
| [!UICONTROL Popularity-Based] | Aanbevelingen doen op basis van de algemene populariteit van een item op uw site of op basis van de populariteit van items in de favoriete of meest bekeken categorie, het merk, het genre enzovoort van een gebruiker. <ul><li>[!UICONTROL Most Viewed Across the Site]</li><li>[!UICONTROL Most Viewed by Category]</li><li>[!UICONTROL Most Viewed by Item Attribute]</li><li>[!UICONTROL Top Sellers Across the Site]</li><li>[!UICONTROL Top Sellers by Category]</li><li>[!UICONTROL Top Sellers by Item Attribute]</li><li>[!UICONTROL Top by Analytics Metric]</li></ul> |
| [!UICONTROL Item-Based] | Aanbevelingen doen op basis van het zoeken naar objecten die vergelijkbaar zijn met een item dat de gebruiker momenteel bekijkt of onlangs heeft bekeken. <ul><li>[!UICONTROL People Who Viewed This, Viewed That]</li><li>[!UICONTROL People Who Viewed This, Bought That]</li><li>[!UICONTROL People Who Bought This, Bought That]</li><li>[!UICONTROL Items with Similar Attributes]</li></ul> |
| [!UICONTROL User-Based] | Aanbevelingen doen op basis van het gedrag van de gebruiker. <ul><li>[!UICONTROL Recently Viewed Items]</li><li>[!UICONTROL Recommended for You]</li></ul> |
| [!UICONTROL Custom Criteria] | Aanbevelingen doen op basis van een aangepast bestand dat u uploadt. <ul><li>Aangepast algoritme</li></ul> |

Elk criterium wordt gedefinieerd in een eigen tabblad. Het verkeer wordt gelijkmatig verdeeld over uw verschillende criteria testen. Met andere woorden, als je twee criteria hebt, is het verkeer gelijk verdeeld. Als u twee criteria en twee ontwerpen hebt, wordt het verkeer gelijkmatig verdeeld tussen de vier combinaties. U kunt ook een percentage bezoekers van de site opgeven die de standaardinhoud ter vergelijking zien. In dat geval ziet het opgegeven percentage bezoekers de standaardinhoud en worden de rest opgedeeld tussen uw criteria en ontwerpcombinaties.

Voor meer informatie over het creëren van criteria en het bepalen van zijn algoritmenypes en algoritmen, zie [&#x200B; criteria &#x200B;](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md) creëren.

Verschillende aanbevelingen voor algoritmen kunnen op verschillende typen pagina&#39;s worden geplaatst. Raadpleeg de volgende secties voor meer informatie over elk type algoritme en de beschikbare algoritmen.

## Op basis van winkelwagentje {#cart-based}

Met het algoritme [!UICONTROL Cart-Based] kunt u items aanbevelen op basis van de inhoud van het huidige winkelwagentje van de bezoeker. De aanbevelingssleutels worden geleverd door [&#x200B; mbox parameter `cartIds` &#x200B;](https://experienceleague.adobe.com/docs/target-dev/developer/recommendations.html?lang=nl-NL){target=_blank} in komma-gescheiden waarden. Alleen de eerste tien waarden worden in aanmerking genomen.

De op kunst-gebaseerde aanbeveling logica is gelijkaardig aan &quot;[!UICONTROL Recommended For You]&quot;op gebruiker-gebaseerd algoritme en aan &quot;[!UICONTROL People Who Viewed These, Bought Those]&quot;en &quot;[!UICONTROL People Who Bought These, Bought Those]&quot;op punt-gebaseerde algoritmen.

[!DNL Target] gebruikt samenwerkende filtertechnieken om gelijkenissen voor elk punt in de kar van de bezoeker te bepalen, dan combineert deze gedragsgelijkenissen over elk punt om een samengevoegde lijst te krijgen.

[!DNL Target] biedt marketers ook de keuze om het gedrag van de bezoeker binnen één sessie of over meerdere sessies te bekijken:

* **[!UICONTROL Single Session]**: Gebaseerd op wat andere bezoekers binnen één sessie deden.

  Het bekijken van gedrag binnen één enkele zitting zou kunnen zinvol zijn wanneer er een gevoel is dat de producten sterk &quot;met&quot;elkaar op een gebruik, een gelegenheid, of een gebeurtenis &quot;gaan. Een bezoeker koopt bijvoorbeeld een printer en heeft inkt en papier nodig. Of een bezoeker koopt pindakaas en heeft misschien ook brood en gelei nodig.

* **[!UICONTROL Across Sessions]**: Gebaseerd op wat andere bezoekers tijdens meerdere sessies hebben gedaan.

  Wanneer u gedrag in meerdere sessies bekijkt, kan het logisch zijn dat producten sterk &quot;met elkaar meegaan&quot; op basis van de voorkeur of smaak van de bezoeker. Bijvoorbeeld, houdt een bezoeker van Star Wars en zou ook als Indiana Jones kunnen houden, zelfs als de bezoeker niet noodzakelijk beide films in de zelfde vergadering wil bekijken. Of een bezoeker houdt van het bordspel &quot;Codenames&quot; en zou ook van het bordspel &quot;Avalon&quot; kunnen houden, zelfs als de bezoeker beide games niet gelijktijdig kan spelen.

[!DNL Target] geeft aanbevelingen voor elke bezoeker op basis van de items in zijn huidige winkelwagentje, ongeacht of u het gedrag van de bezoeker in één sessie of in meerdere sessies bekijkt.

De volgende algoritmen zijn beschikbaar met het algoritme [!UICONTROL Cart-Based] type:

### [!UICONTROL People Who Viewed This, Also Viewed]

Hiermee worden items aanbevolen die het vaakst worden weergegeven in dezelfde sessie als waarin het opgegeven item wordt weergegeven.

Deze logica retourneert andere producten die worden weergegeven na het bekijken van deze logica. Het opgegeven product wordt niet opgenomen in de resultatenset.

Met deze logica kunt u aanvullende conversiemogelijkheden creëren door items aan te bevelen die andere bezoekers die een item hebben bekeken, ook hebben weergegeven. Bezoekers die op uw site fietsen bekijken, kunnen bijvoorbeeld ook fietshelmen, fietskits, sloten enzovoort bekijken. U kunt een aanbeveling tot stand brengen gebruikend deze logica die andere producten aanbeveelt u helpen opbrengst verhogen.

Als u dit algoritme selecteert, kunt u de volgende toetsen voor Aanbevelingen selecteren:

* [!UICONTROL Current Item]
* [!UICONTROL Last Purchased Item]
* [!UICONTROL Last Viewed Item]
* [!UICONTROL Most Viewed Item]

### [!UICONTROL People Who Viewed This, Also Bought]

Hiermee raadt u objecten aan die het vaakst worden aangeschaft in dezelfde sessie als waarin het opgegeven item wordt weergegeven.

Deze logica retourneert andere producten die mensen hebben gekocht na het bekijken van deze logica. Het opgegeven product wordt niet opgenomen in de resultatenset.

Met deze logica kunt u de mogelijkheden voor cross-selling vergroten door bijvoorbeeld een aanbeveling weer te geven op een productpagina die items weergeeft die andere bezoekers hebben bekeken die het object hebben aangeschaft. Als de bezoeker bijvoorbeeld een vispool bekijkt, kan de aanbeveling extra items weergeven die andere bezoekers hebben aangeschaft, zoals hakbalken, golven en blaasjes. Wanneer bezoekers door uw site bladeren, geeft u hun aanvullende aankoopaanbevelingen.

Als u dit algoritme selecteert, kunt u de volgende toetsen voor Aanbevelingen selecteren:

* [!UICONTROL Current Item]
* [!UICONTROL Last Purchased Item]
* [!UICONTROL Last Viewed Item]
* [!UICONTROL Most Viewed Item]

### [!UICONTROL People Who Bought This, Also Bought]

Aanbevolen objecten die het meest door klanten tegelijk met het opgegeven item worden aangeschaft.

Deze logica retourneert andere producten die mensen hebben gekocht na deze aankoop. Het opgegeven product wordt niet opgenomen in de resultatenset.

Met deze logica kunt u de mogelijkheden voor cross-selling vergroten door bijvoorbeeld een aanbeveling weer te geven op een overzichtspagina van winkelwagentjes waarin objecten worden weergegeven die andere kopers ook hebben gekocht. Als de bezoeker bijvoorbeeld een pak koopt, kan de aanbeveling extra artikelen weergeven die andere bezoekers samen met het pak hebben gekocht, zoals bijvoorbeeld banden, jurkschoenen en knipsels. Wanneer bezoekers hun aankopen bekijken, geeft u aanvullende aanbevelingen aan hen.

Als u dit algoritme selecteert, kunt u de volgende toetsen voor Aanbevelingen selecteren:

* [!UICONTROL Current Item]
* [!UICONTROL Last Purchased Item]
* [!UICONTROL Last Viewed Item]
* [!UICONTROL Most Viewed Item]

## [!UICONTROL Popularity-Based]

Met het algoritme [!UICONTROL Popularity-Based] kunt u aanbevelingen doen op basis van de algemene populariteit van een item op uw site of op basis van de populariteit van items in de favoriete of meest bekeken categorie, het merk, het genre enzovoort van een gebruiker.

De volgende algoritmen zijn beschikbaar met het algoritme [!UICONTROL Popularity-Based] type:

### [!UICONTROL Most Viewed Across the Site] {#most-viewed}

De aanbeveling wordt bepaald door het punt dat het vaakst is bekeken. Dit wordt bepaald aan de hand van de recenentie-/frequentiecriteria die als volgt werken:

* 10 punten voor de eerste productweergave
* 5 punten voor elke volgende weergave
* Aan het einde van de sessie worden alle waarden door 2 gedeeld

Als u bijvoorbeeld surfboard A en daarna surfboard B in één sessie weergeeft, resulteert dit in A: 10, B: 5. Wanneer de sessie wordt beëindigd, hebt u A: 5, B: 2.5. Als u dezelfde items in de volgende sessie bekijkt, veranderen de waarden in A: 15 B: 7.5.

Gebruik dit algoritme op algemene pagina&#39;s, zoals startpagina&#39;s of bestemmingspagina&#39;s en offsite advertenties.

### [!UICONTROL Most Viewed by Category] {#most-viewed-category}

De aanbeveling wordt bepaald door de categorie die de meeste activiteit heeft ontvangen, gebruikend de zelfde methode die voor &quot;het meest bekeken punt&quot;wordt gebruikt behalve dat de categorieën in plaats van producten worden gescoord.

Dit wordt bepaald aan de hand van de recenentie-/frequentiecriteria die als volgt werken:

* 10 punten voor de weergave van de eerste categorie
* 5 punten voor elke volgende weergave

De categorieën die voor het eerst worden bezocht, krijgen 10 punten. 5 punten voor latere bezoeken aan dezelfde categorie. Bij elk bezoek worden niet-huidige categorieën die eerder zijn bekeken, verlaagd met 1.

Als u bijvoorbeeld categorie A en vervolgens categorie B in één sessie weergeeft, resulteert dit in A: 9, B: 10. Als u dezelfde items in de volgende sessie weergeeft, veranderen de waarden in A: 20 B: 9.

Gebruik dit algoritme op algemene pagina&#39;s, zoals startpagina&#39;s of bestemmingspagina&#39;s en offsite advertenties.

Als u het algoritme Meest bekeken door Categorie selecteert, kunt u de volgende Sleutels van Aanbevelingen selecteren:

* [!UICONTROL Current Category]
* [!UICONTROL Favorite Category]

### [!UICONTROL Most Viewed by Item Attribute]

Aanbevolen items of media die vergelijkbaar zijn met de meest bekeken items of media op uw site.

Met dit algoritme kunt u selecteren op welk itemkenmerk u de aanbeveling wilt baseren, bijvoorbeeld &quot;Naam&quot; of &quot;Merk&quot;.

Vervolgens selecteert u welke profielkenmerken uit het profiel van de bezoeker overeenkomen, bijvoorbeeld Favoriete merk, Laatste object toegevoegd aan winkelwagentje of Meest bekeken presentatie.

### [!UICONTROL Top Sellers Across the Site] {#top-sellers}

Toont de punten die in de meest voltooide orden van over de plaats inbegrepen zijn. Meerdere eenheden van hetzelfde item in één volgorde worden als één volgorde geteld.

Met dit algoritme kunt u aanbevelingen maken voor de meest verkochte items op uw site om de conversie en de inkomsten te verhogen. Deze logica is vooral geschikt voor nieuwe bezoekers van uw site.

### [!UICONTROL Top Sellers by Category]

Hiermee geeft u de items weer die zijn opgenomen in de meest voltooide bestellingen per categorie. Meerdere eenheden van hetzelfde item in één volgorde worden als één volgorde geteld.

Met dit algoritme kunt u aanbevelingen maken voor de meest verkochte items op uw site op basis van categorie om de conversie en de omzet te verhogen. Deze logica is vooral geschikt voor nieuwe bezoekers van uw site.

Als u het algoritme [!UICONTROL Most Viewed by Category] selecteert, kunt u het volgende selecteren [!UICONTROL Recommendations Keys] :

* [!UICONTROL Current Category]
* [!UICONTROL Favorite Category]

### [!UICONTROL Top Sellers by Item Attribute]

Aanbevolen objecten of media die vergelijkbaar zijn met de meest aangeschafte items of media op uw site.

Met dit algoritme kunt u selecteren op welk itemkenmerk u de aanbeveling wilt baseren, bijvoorbeeld &quot;Naam&quot; of &quot;Merk&quot;.

Vervolgens selecteert u welke profielkenmerken uit het profiel van de bezoeker overeenkomen, bijvoorbeeld Favoriete merk, Laatste object toegevoegd aan winkelwagentje of Meest bekeken presentatie.

### [!UICONTROL Top by Analytics Metric]

Toont &quot;Bovenste x&quot;waar *x* willekeurig [!DNL Analytics] metrisch is. Wanneer u gedragsgegevens uit vakken gebruikt, kunt u [!UICONTROL Top Sold] of [!UICONTROL Top Viewed] (x = &quot;Verkocht&quot; of x = &quot;Weergegeven&quot;) gebruiken. Als u gedragsgegevens van [!DNL Adobe Analytics] gebruikt, zou u x = &quot;Kar Adds&quot;of één of andere andere [!DNL Analytics] metrisch kunnen gebruiken.

## [!UICONTROL Item-Based]

Het [!UICONTROL Item-Based] aanbevelingen type laat u aanbevelingen doen die op het vinden van gelijkaardige punten aan een punt worden gebaseerd dat de gebruiker momenteel bekijkt of onlangs heeft bekeken.

De volgende algoritmen zijn beschikbaar met het algoritme [!UICONTROL Item-Based] type:

### [!UICONTROL People Who Viewed This, Viewed That] {#viewed-viewed}

Hiermee worden items aanbevolen die het vaakst worden weergegeven in dezelfde sessie als waarin het opgegeven item wordt weergegeven.

Deze logica retourneert andere producten die worden weergegeven nadat deze is bekeken. Het opgegeven product is niet opgenomen in de resultatenset.

Met deze logica kunt u aanvullende conversiemogelijkheden creëren door items aan te bevelen die andere bezoekers die een item hebben bekeken, ook hebben weergegeven. Bezoekers die op uw site fietsen bekijken, kunnen bijvoorbeeld ook fietshelmen, fietskits, sloten enzovoort bekijken. U kunt een aanbeveling tot stand brengen gebruikend deze logica die andere producten aanbeveelt u helpen opbrengst verhogen.

Als u dit algoritme selecteert, kunt u het volgende selecteren [!UICONTROL Recommendations Keys] :

* [!UICONTROL Current Item]
* [!UICONTROL Last Purchased Item]
* [!UICONTROL Last Viewed Item]
* [!UICONTROL Most Viewed Item]

### [!UICONTROL People Who Viewed This, Bought That] {#viewed-bought}

Hiermee raadt u objecten aan die het vaakst worden aangeschaft in dezelfde sessie als waarin het opgegeven item wordt weergegeven. Dit criterium retourneert andere producten die mensen hebben aangeschaft nadat deze is bekeken. Het opgegeven product is niet opgenomen in de resultatenset.

Deze logica retourneert andere producten die mensen hebben gekocht na het bekijken van deze software. Het opgegeven product is niet opgenomen in de resultatenset.

Met deze logica kunt u de mogelijkheden voor cross-selling vergroten door bijvoorbeeld een aanbeveling weer te geven op een productpagina die items weergeeft die andere bezoekers hebben bekeken die het object hebben aangeschaft. Als de bezoeker bijvoorbeeld een vispool bekijkt, kan de aanbeveling extra items weergeven die andere bezoekers hebben aangeschaft, zoals hakbalken, golven en blaasjes. Wanneer bezoekers door uw site bladeren, geeft u hun aanvullende aankoopaanbevelingen.

Als u dit algoritme selecteert, kunt u het volgende selecteren [!UICONTROL Recommendations Keys] :

* [!UICONTROL Current Item]
* [!UICONTROL Last Purchased Item]
* [!UICONTROL Last Viewed Item]
* [!UICONTROL Most Viewed Item]

### [!UICONTROL People Who Bought This, Bought That] {#bought-bought}

Aanbevolen objecten die het meest door klanten tegelijk met het opgegeven item worden aangeschaft.

Deze logica retourneert andere producten die mensen hebben gekocht na deze aankoop. Het opgegeven product wordt niet opgenomen in de resultatenset.

Met deze logica kunt u de mogelijkheden voor cross-selling vergroten door bijvoorbeeld een aanbeveling weer te geven op een overzichtspagina van winkelwagentjes waarin objecten worden weergegeven die andere kopers ook hebben gekocht. Als de bezoeker bijvoorbeeld een pak koopt, kan de aanbeveling extra artikelen weergeven die andere bezoekers samen met het pak hebben gekocht, zoals bijvoorbeeld banden, jurkschoenen en knipsels. Wanneer bezoekers hun aankopen bekijken, geeft u aanvullende aanbevelingen aan hen.

Als u dit algoritme selecteert, kunt u het volgende selecteren [!UICONTROL Recommendations Keys] :

* [!UICONTROL Current Item]
* [!UICONTROL Last Purchased Item]
* [!UICONTROL Last Viewed Item]
* [!UICONTROL Most Viewed Item]

### [!UICONTROL Items with Similar Attributes] {#similar-attributes}

Aanbevolen items of media die vergelijkbaar zijn met items of media op basis van de huidige paginageactiviteit of het gedrag van een bezoeker.

Als u [!UICONTROL Items with Similar Attributes] of [!UICONTROL Media with Similar Attributes] selecteert, kunt u regels voor gelijkenis van inhoud instellen.

Het gebruik van gelijkenis in de inhoud om aanbevelingen te genereren is vooral effectief voor nieuwe items. Deze worden waarschijnlijk niet weergegeven in aanbevelingen met [!UICONTROL People Who Viewed This] , [!UICONTROL Viewed That] en andere logica op basis van gedrag in het verleden. U kunt de gelijkenis van de inhoud ook gebruiken om nuttige aanbevelingen voor nieuwe bezoekers te produceren, die geen vroegere aankopen of andere historische gegevens hebben.

Als u dit algoritme selecteert, kunt u het volgende selecteren [!UICONTROL Recommendations Keys] :

* [!UICONTROL Current Item]
* [!UICONTROL Last Purchased Item]
* [!UICONTROL Last Viewed Item]
* [!UICONTROL Most Viewed Item]

Voor meer informatie, zie [&#x200B; Vergelijkbaarheid van de Inhoud &#x200B;](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md#similarity).

## [!UICONTROL User-Based]

Met het type algoritme [!UICONTROL User-Based] kunt u aanbevelingen doen op basis van het gedrag van de gebruiker.

De volgende algoritmen zijn beschikbaar met het algoritme [!UICONTROL User-Based] type:

### [!UICONTROL Recently Viewed Items] {#recently-viewed}

Gebruikt de geschiedenis van de bezoeker (overspannend zittingen) om de laatste *x* punten voor te stellen de bezoeker heeft bekeken, die op het aantal groeven in het ontwerp worden gebaseerd.

Het [!UICONTROL Recently Viewed Items] algoritme keert resultaat specifiek op a bepaalde [&#x200B; milieu &#x200B;](/help/main/administrating-target/hosts.md) terug. Als twee sites tot verschillende omgevingen behoren en een bezoeker tussen de twee sites schakelt, worden op elke site alleen recent bekeken items van de desbetreffende site weergegeven. Als twee sites zich in dezelfde omgeving bevinden en een bezoeker schakelt tussen de twee sites, ziet de bezoeker dezelfde onlangs weergegeven items voor beide sites.

>[!NOTE]
>
>U kunt de criteria van [!UICONTROL Recently Viewed Items] niet gebruiken voor back-upaanbevelingen.

[!UICONTROL Recently Viewed Items] of [!UICONTROL Recently Viewed Media] kan worden gefilterd, zodat alleen items met een bepaald kenmerk worden weergegeven.

* De criteria van [!UICONTROL Recently Viewed] zijn configureerbaar, zoals andere criteria in aanbevelingen.
* U kunt [&#x200B; inzamelingen &#x200B;](/help/main/c-recommendations/c-products/collections.md) gebruiken, [&#x200B; uitsluitingen &#x200B;](/help/main/c-recommendations/c-products/exclusions.md), en [&#x200B; opneming &#x200B;](/help/main/c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md) (met inbegrip van de speciale regels voor Prijs en Inventaris) op de zelfde manier zoals om het even welke andere criteria.

Mogelijke gebruiksgevallen zijn onder andere: een multinationaal bedrijf met meerdere bedrijven kan bezoekers artikelen laten zien over meerdere digitale eigenschappen. In dit geval kunt u de onlangs weergegeven items beperken tot weergave voor de desbetreffende eigenschap waar deze is weergegeven. Hiermee voorkomt u dat onlangs bekeken items worden weergegeven op de site van een andere digitale eigenschap.

Gebruik dit algoritme op algemene pagina&#39;s, zoals startpagina&#39;s of bestemmingspagina&#39;s en offsite advertenties.

>[!NOTE]
>
>[!UICONTROL Recently Viewed Items] respecteert zowel de globale instellingen voor uitsluitingen als de geselecteerde verzamelingsinstelling voor de activiteit. Als een item wordt uitgesloten door een algemene uitsluiting of niet in de geselecteerde verzameling voorkomt, wordt het item niet weergegeven. Daarom moet bij het gebruik van een [!UICONTROL Recently Viewed Items] -criterium doorgaans de instelling Alle verzamelingen worden gebruikt.

### [!UICONTROL Recommended for You] {#recommended-for-you}

Aanbevolen objecten op basis van de browsergeschiedenis, weergavegeschiedenis en aankoopgeschiedenis van elke bezoeker.

Met dit algoritme kunt u persoonlijke inhoud en ervaringen leveren aan zowel nieuwe als geretourneerde bezoekers. De lijst met aanbevelingen is gericht op de meest recente activiteit van de bezoeker en wordt tijdens de sessie bijgewerkt en wordt meer gepersonaliseerd naarmate de gebruiker door uw site bladert.

Zowel weergaven als aankopen worden gebruikt om de aanbevolen items te bepalen. De opgegeven aanbevelingssleutel (bijvoorbeeld [!UICONTROL Current Item] ) wordt gebruikt om filters toe te passen die u voor de invoegregel selecteert.

U kunt bijvoorbeeld:

* Sluit items uit die niet aan bepaalde criteria voldoen (producten die niet in voorraad zijn, artikelen die meer dan 30 dagen geleden zijn gepubliceerd, films met R enzovoort).
* Beperk opgenomen objecten tot één categorie of tot de huidige categorie.

Als u dit algoritme selecteert, kunt u de volgende Filtrerende Sleutels selecteren:

* [!UICONTROL Current Item]
* [!UICONTROL Last Purchased Item]
* [!UICONTROL Last Viewed Item]
* [!UICONTROL Most Viewed Item]

## Aangepaste criteria {#custom}

Met het type algoritme [!UICONTROL Custom Criteria] kunt u aanbevelingen doen op basis van een aangepast bestand dat u uploadt.

De aanbeveling wordt bepaald door een punt dat in het profiel van een bezoeker, gebruikend één van beide gebruiker wordt opgeslagen.*x* of profiel.*x* attributen.

Als deze optie is geselecteerd, moet de waarde `entity.id` aanwezig zijn in het profielkenmerk.

Wanneer u aanbevelingen baseert op douanekenmerken, moet u het douanekenmerk selecteren en dan het aanbevelingstype selecteren.

U kunt filter in real time bovenop uw eigen output van douanecriteria uitvoeren. U kunt bijvoorbeeld de aanbevolen objecten beperken tot objecten van de favoriete rubriek of het favoriete merk van een bezoeker. Dit geeft u de macht om off-line berekeningen met het filtreren in real time te combineren.

Deze functionaliteit houdt in dat u met [!DNL Target] personalisatie kunt toevoegen boven op uw offline berekende aanbevelingen of lijsten met aangepaste cursisten. Dit combineert de kracht van uw gegevenswetenschappers en onderzoek met de beproefde levering van Adobe, runtime het filtreren, A/B het testen, het richten, het melden, de integratie, en meer.

Met toevoeging van inclusieregels op [!UICONTROL Custom Criteria], verandert dit anders statische aanbevelingen in dynamische aanbevelingen gebaseerd op de belangen van een bezoeker.

* De criteria van de douane zijn configureerbaar, zoals andere criteria in aanbevelingen.
* U kunt [&#x200B; inzamelingen &#x200B;](/help/main/c-recommendations/c-products/collections.md) gebruiken, [&#x200B; uitsluitingen &#x200B;](/help/main/c-recommendations/c-products/exclusions.md), en [&#x200B; opneming &#x200B;](/help/main/c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md) (met inbegrip van de speciale regels voor Prijs en Inventaris) op de zelfde manier zoals om het even welke andere criteria.

Mogelijke gebruiksgevallen zijn:

* U wilt films aanbevelen vanuit een lijst met aangepaste cursisten, maar alleen als de bezoeker deze nog niet heeft bekeken.
* U wilt een off-line algoritme in werking stellen en de resultaten gebruiken om uw aanbevelingen aan te drijven, maar u moet ervoor zorgen dat de uit-van-voorraad punten nooit worden geadviseerd.
* Je wilt alleen objecten opnemen die afkomstig zijn uit de favoriete rubriek van deze bezoeker.

## Aanbevolen toetsen {#keys}

De volgende aanbevelingen zijn beschikbaar in de vervolgkeuzelijst [!UICONTROL Recommendation Key] :

### [!UICONTROL Current Item] {#current-item}

De aanbeveling wordt bepaald door het item dat de bezoeker momenteel bekijkt.

De aanbevelingen tonen andere punten die bezoekers zouden kunnen interesseren die in het gespecificeerde punt geïnteresseerd zijn.

Als deze optie is geselecteerd, moet de waarde `entity.id` als parameter in het weergavevak worden doorgegeven.

Kan met de volgende algoritmen worden gebruikt:

* [!UICONTROL Items with similar attributes]
* [!UICONTROL People Who Viewed This, Viewed That]
* [!UICONTROL People Who Viewed This, Bought That]
* [!UICONTROL People Who Bought This, Bought That]

Gebruik de toets [!UICONTROL Current Item] recommendations op uw site op:

* Pagina&#39;s met één item, zoals productpagina&#39;s.
* Niet gebruiken op pagina&#39;s met zoekresultaten die null zijn.

### [!UICONTROL Last Purchased Item] {#last-purchased}

De aanbeveling wordt bepaald door het laatste item dat door elke unieke bezoeker is aangeschaft. Dit wordt automatisch vastgelegd, zodat er geen waarden op de pagina moeten worden doorgegeven.

Kan met de volgende algoritmen worden gebruikt:

* [!UICONTROL Items with similar attributes]
* [!UICONTROL People Who Viewed This, Viewed That]
* [!UICONTROL People Who Viewed This, Bought That]
* [!UICONTROL People Who Bought This, Bought That]

Gebruik de toets [!UICONTROL Last Purchased Item] recommendations op uw site op:

* Homepage, pagina Mijn account, offsite advertenties.
* Niet gebruiken op productpagina&#39;s of pagina&#39;s die relevant zijn voor aankopen.

#### Aangepaste aanbevelingen

U kunt aanbevelingen op de waarde van een attribuut van het douaneprofiel baseren. Stel dat u aanbevolen films wilt weergeven op basis van de film die een bezoeker het laatst aan de wachtrij heeft toegevoegd.

1. Selecteer uw attribuut van het douaneprofiel van de **[!UICONTROL Recommendation Key]** drop-down lijst (bijvoorbeeld, &quot;[!UICONTROL Last Show Added to Watchlist]&quot;).
1. Selecteer vervolgens uw **[!UICONTROL Recommendation Logic]** (bijvoorbeeld &quot;[!UICONTROL People Who Viewed This, Viewed That]&quot;).

Als uw attribuut van het douaneprofiel niet direct met één enkele entiteitidentiteitskaart aanpast, is het noodzakelijk om aan [!DNL Recommendations] uit te leggen hoe u de gelijke aan een entiteit wilt voorkomen. Stel dat u bijvoorbeeld de meest verkochte objecten van het favoriete merk van een bezoeker wilt weergeven.

1. Selecteer het aangepaste profielkenmerk in de vervolgkeuzelijst **[!UICONTROL Recommendation Key]** (bijvoorbeeld Favoriete merk).

1. Selecteer vervolgens de **[!UICONTROL Recommendation Logic]** die u met deze toets wilt gebruiken (bijvoorbeeld &quot;[!UICONTROL Top Sellers]&quot;).

   De optie [!UICONTROL Group By Unique Value Of] wordt weergegeven.

1. Selecteer het entiteitattribuut dat aan de sleutel aanpast u hebt gekozen. In dit geval komt &quot;[!UICONTROL Favorite Brand]&quot; overeen met `entity.brand` .

   [!DNL Recommendations] produceert nu &quot;[!UICONTROL Top Sellers]&quot;lijst voor elk merk en toont de bezoeker aangewezen &quot;[!UICONTROL Top Sellers]&quot;lijst die op de waarde wordt gebaseerd in het [!UICONTROL Favorite Brand] profielattribuut van de bezoeker wordt opgeslagen.

### [!UICONTROL Last Viewed Item] {#last-viewed}

De aanbeveling wordt bepaald door het laatste item dat door elke unieke bezoeker is bekeken. Dit wordt automatisch vastgelegd, zodat er geen waarden op de pagina moeten worden doorgegeven.

Kan met de volgende algoritmen worden gebruikt:

* [!UICONTROL Items with similar attributes]
* [!UICONTROL People Who Viewed This, Viewed That]
* [!UICONTROL People Who Viewed This, Bought That]
* [!UICONTROL People Who Bought This, Bought That]

Gebruik de toets [!UICONTROL Last Viewed Item] recommendations op uw site op:

* Homepage, pagina Mijn account, offsite advertenties.
* Niet gebruiken op productpagina&#39;s of pagina&#39;s die relevant zijn voor aankopen.

### [!UICONTROL Most Viewed Item] {#most-viewed-logic}

Hiermee geeft u de items of media weer die het vaakst op uw site worden weergegeven.

Met deze logica kunt u aanbevelingen weergeven op basis van de meest bekeken items op uw site om de conversies voor andere items te verhogen. Een mediasite kan bijvoorbeeld op haar homepage aanbevelingen weergeven voor de meest bekeken video&#39;s om bezoekers aan te moedigen aanvullende video&#39;s te bekijken.

Deze advisesleutel kan met de volgende algoritmen worden gebruikt:

* [!UICONTROL Items with similar attributes]
* [!UICONTROL People Who Viewed This, Viewed That]
* [!UICONTROL People Who Viewed This, Bought That]
* [!UICONTROL People Who Bought This, Bought That]

### [!UICONTROL Current Category] {#current-category}

De aanbeveling wordt bepaald door de productcategorie die de bezoeker momenteel bekijkt.

Aanbevelingen geven items weer in de opgegeven productcategorie.

Als deze optie is geselecteerd, moet de waarde `entity.categoryId` als parameter aan de weergavekader worden doorgegeven.

Deze advisesleutel kan met de volgende algoritmen worden gebruikt:

* [!UICONTROL Top Sellers]
* [!UICONTROL Most Viewed]

Gebruik de toets [!UICONTROL Current Category] recommendations op uw site op:

* Pagina&#39;s van één categorie.
* Niet gebruiken op pagina&#39;s met zoekresultaten die null zijn.

### [!UICONTROL Favorite Category] {#favorite-category}

De aanbeveling wordt bepaald door de favoriete productcategorie van de bezoeker.

Aanbevelingen geven items weer in de opgegeven productcategorie.

Als deze optie is geselecteerd, moet de waarde `entity.categoryId` als parameter aan de weergavekader worden doorgegeven.

Deze advisesleutel kan met de volgende algoritmen worden gebruikt:

* [!UICONTROL Top Sellers]
* [!UICONTROL Most Viewed]

Gebruik de toets [!UICONTROL Current Category] recommendations op uw site op:

* Pagina&#39;s van één categorie.
* Niet gebruiken op pagina&#39;s met zoekresultaten die null zijn.

### [!UICONTROL Site Affinity] {#site-affinity}

Aanbevolen items op basis van de zekerheid van een relatie tussen items. U kunt deze criteria configureren om te bepalen hoeveel gegevens vereist zijn voordat een aanbeveling wordt weergegeven met de schuifregelaar [!UICONTROL Inclusion Rules] . Als u bijvoorbeeld erg sterk selecteert, worden de producten met de grootste zekerheid van een overeenkomst aanbevolen.

Bijvoorbeeld, als u een zeer sterke affiniteit plaatst en uw ontwerp vijf punten omvat, waarvan drie aan de sterkte van verbindingsdrempel voldoen, worden de twee punten die niet aan de minimumsterktevereisten voldoen niet getoond in uw aanbevelingen en door uw bepaalde reservepunten vervangen. De items met de sterkste affiniteit worden eerst weergegeven.

Een online retailer kan bijvoorbeeld items in volgende bezoeken aanbevelen die een bezoeker in de afgelopen sessies heeft willen zien. De activiteit voor elke sessie van de bezoeker wordt vastgelegd om een affiniteit te berekenen op basis van een recentiemodel en een frequentiemodel. Wanneer deze bezoeker terugkeert naar uw site, wordt de affiniteit van de site gebruikt om aanbevelingen weer te geven op basis van eerdere acties op uw site.

Sommige klanten met diverse productinzamelingen en diverse plaatsgedrag zouden de beste resultaten kunnen krijgen als zij een zwakke plaatsaffiniteit plaatsen.

Deze logica kan met de volgende advisesleutels worden gebruikt:

* [!UICONTROL Current Item]
* [!UICONTROL Last Purchased Item]
* [!UICONTROL Last Viewed Item]
* [!UICONTROL Most Viewed Item]
