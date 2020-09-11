---
keywords: recommendation key;recommendation logic;current category;custom attribute;last purchased item;last viewed item;most viewed item;most viewed item;favorite category;popularity;recently viewed item;last purchased;last viewed;most viewed;favorite;recently viewed
description: Recommendations op basis van sleutels gebruikt de gedragscontext van de bezoeker om relevante resultaten te tonen in Adobe Target Recommendations-activiteiten.
title: De aanbeveling baseren op een aanbevelingen
feature: criteria
mini-toc-levels: 3
translation-type: tm+mt
source-git-commit: 73af03c895ce98e5b6762950e8cd638d7bef0990
workflow-type: tm+mt
source-wordcount: '2001'
ht-degree: 0%

---


# De aanbeveling baseren op een aanbevelingen

Recommendations op basis van sleutels gebruikt de gedragscontext van de bezoeker om relevante resultaten in [!DNL Adobe Target] [!DNL Recommendations] activiteiten weer te geven.

Er zijn twee typen Recommendations:

* **Populariteit:** Hiermee geeft u items weer op basis van de opties Meest bekeken, Boven verkocht en Metrisch bovenaan. De sleutel is leeg voor populiteitscriteria.
* **Op sleutel gebaseerd:** Omvat de rest van de criteria. Recommendations biedt verschillende keuzemogelijkheden met betrekking tot het sleuteltype. De opties variëren van &quot;huidig punt&quot;tot &quot;profielparameters,&quot;die u toestaan om de sleutel van de waarden programmatically te plaatsen aan te bevelen. U kunt meerdere criteria op elkaar testen door de criteria op een andere toets te baseren.

Elk criterium wordt gedefinieerd in een eigen tabblad. Het verkeer wordt gelijkmatig verdeeld over uw verschillende criteria testen. Met andere woorden, als je twee criteria hebt, is het verkeer in gelijke mate verdeeld. Als u twee criteria en twee ontwerpen hebt, wordt het verkeer gelijkmatig verdeeld tussen de vier combinaties. U kunt ook een percentage bezoekers van de site opgeven die de standaardinhoud ter vergelijking zien. In dat geval ziet het opgegeven percentage bezoekers de standaardinhoud en worden de rest opgedeeld tussen uw criteria en ontwerpcombinaties.

1. Maak nieuwe criteria of selecteer een bestaand criterium en klik op **[!UICONTROL Edit]**.
1. Als u de aanbevolen toets wilt wijzigen, selecteert u de nieuwe toets in de [!UICONTROL Recommendation Key] vervolgkeuzelijst en klikt u **[!UICONTROL Save]** of **[!UICONTROL Update]**.

   Omdat verschillende logica aan verschillende aanbevelingen sleutels in kaart brengt, lenen de verschillende aanbevelingen zich aan plaatsing op verschillende types van pagina&#39;s. Raadpleeg de volgende secties voor meer informatie over elke advisesleutel.

## Aanbevolen toetsen

De volgende aanbevelingen zijn beschikbaar in de [!UICONTROL Recommendation Key] vervolgkeuzelijst:

### Huidig item

De aanbeveling wordt bepaald door het item dat de bezoeker momenteel bekijkt.

Recommendations geeft andere objecten weer die bezoekers interesseren voor het opgegeven object.

Als deze optie is geselecteerd, moet de `entity.id` waarde als een parameter in het weergavevak worden doorgegeven.

#### Logica (criteria)

* [!UICONTROL Items with similar attributes]
* [!UICONTROL People Who Viewed This, Viewed That]
* [!UICONTROL People Who Viewed This, Bought That]
* [!UICONTROL People Who Bought This, Bought That]
* [!UICONTROL Site Affinity]

#### Waar op uw site gebruiken

* Pagina&#39;s met één item, zoals productpagina&#39;s.
* Niet gebruiken op pagina&#39;s met zoekresultaten die null zijn.

### Huidige rubriek

De aanbeveling wordt bepaald door de productcategorie die de bezoeker momenteel bekijkt.

Recommendations geeft objecten weer in de opgegeven productcategorie.

Als deze optie is geselecteerd, moet de `entity.categoryId` waarde als parameter worden doorgegeven aan het weergavevak.

#### Logica (criteria)

* Topverkopers
* Meest bekeken

#### Waar op uw site gebruiken

* Pagina&#39;s van één categorie.
* Niet gebruiken op pagina&#39;s met zoekresultaten die null zijn.

### Aangepast kenmerk {#custom}

De aanbeveling wordt bepaald door een punt dat in het profiel van een bezoeker, gebruikend één van beide gebruiker wordt opgeslagen.*x* of profiel.*x* -kenmerken.

Als deze optie is geselecteerd, moet de `entity.id` waarde aanwezig zijn in het profielkenmerk.

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

1. Selecteer het kenmerk Aangepast profiel in de **[!UICONTROL Recommendation Key]** vervolgkeuzelijst (bijvoorbeeld Laatste weergave Toegevoegd aan lijst met gecontroleerde items).
1. Selecteer vervolgens uw **[!UICONTROL Recommendation Logic]** (bijvoorbeeld &quot;Personen die dit hebben bekeken, hebben dat weergegeven&quot;).

   ![Nieuwe criteria maken, dialoogvenster](/help/c-recommendations/c-algorithms/assets/create-new-criteria-1.png)

Als uw attribuut van het douaneprofiel niet direct met één enkele entiteitidentiteitskaart aanpast, is het noodzakelijk om aan te verklaren [!DNL Recommendations] hoe u de gelijke aan een entiteit wilt voorkomen. Stel dat u bijvoorbeeld de meest verkochte objecten van het favoriete merk van een bezoeker wilt weergeven.

1. Selecteer het aangepaste profielkenmerk in de **[!UICONTROL Recommendation Key]** vervolgkeuzelijst (bijvoorbeeld Favoriete merk).

1. Selecteer vervolgens de **[!UICONTROL Recommendation Logic]** code die u met deze sleutel wilt gebruiken (bijvoorbeeld Topverkopers).

   De [!UICONTROL Group By Unique Value Of] optie wordt weergegeven.

1. Selecteer het entiteitskenmerk dat overeenkomt met de gekozen sleutel. In dit geval komt &quot;Favoriete merk&quot; overeen met `entity.brand`.

   [!DNL Recommendations] produceert nu een lijst met topverkopers voor elk merk en geeft de bezoeker de juiste lijst met topverkopers weer op basis van de waarde die is opgeslagen in het kenmerk Favoriete merk van de bezoeker.

   ![Nieuwe criteria maken, dialoogvenster 2](/help/c-recommendations/c-algorithms/assets/create-new-criteria-2.png)

### Laatst gekocht object

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

### Laatst weergegeven item

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

### Meest bekeken item

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

### Favoriete rubriek

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

### Populariteit

De aanbeveling wordt bepaald door de populariteit van objecten op uw site. De populariteit omvat topverkopers en hoogste bekeken door mbox gegevens en, als u Adobe Analytics gebruikt, alle metriek beschikbaar in het productrapport. De items worden gerangschikt op basis van de door u geselecteerde logica voor aanbevelingen.

#### Logica (criteria)

* [!UICONTROL Top Sellers]
* [!UICONTROL Most Viewed]
* Metrische gegevens van productrapporten (als u Adobe Analytics gebruikt)

#### Waar op uw site gebruiken

* Algemene pagina&#39;s, zoals startpagina&#39;s of bestemmingspagina&#39;s en offsite advertenties.

### Onlangs bekeken objecten {#recently-viewed}

Gebruikt de geschiedenis van de bezoeker (overspannende zittingen) om de laatste *x* punten voor te stellen de bezoeker heeft bekeken, die op het aantal groeven in het ontwerp worden gebaseerd.

De criteria voor onlangs bekeken items geven nu resultaten die specifiek zijn voor een bepaalde [omgeving](/help/administrating-target/hosts.md). Als twee sites tot verschillende omgevingen behoren en een bezoeker tussen de twee sites schakelt, worden op elke site alleen recent bekeken items van de desbetreffende site weergegeven. Als twee sites zich in dezelfde omgeving bevinden en een bezoeker schakelt tussen de twee sites, ziet de bezoeker dezelfde onlangs weergegeven items voor beide sites.

#### Waar op uw site gebruiken

* Algemene pagina&#39;s, zoals startpagina&#39;s of bestemmingspagina&#39;s en offsite advertenties.

>[!NOTE]
>
>Onlangs bekeken items respecteren zowel de globale instellingen voor Uitsluiting als de geselecteerde instelling voor Verzameling voor de activiteit. Als een item is uitgesloten door een algemene uitsluiting of niet is opgenomen in de geselecteerde verzameling, wordt het item niet weergegeven. Daarom moet bij het gebruik van de criteria voor onlangs bekeken items doorgaans de instelling &quot;Alle verzamelingen&quot; worden gebruikt.

## Instructielogica

De volgende aanbevelingen (criteria) zijn beschikbaar bij de [!UICONTROL Recommendation Logic] drop-down lijst:

### Objecten met vergelijkbare kenmerken

De gelijkenis van de inhoud vergelijkt de sleutelwoorden van puntattributen en doet aanbevelingen die op hoeveel sleutelwoorden verschillende punten in gemeenschappelijk hebben worden gebaseerd. Recommendations op basis van gelijkenis met inhoud vereist geen gegevens uit het verleden om sterke resultaten te bereiken.

Het gebruik van gelijkenis in de inhoud om aanbevelingen te genereren is vooral effectief voor nieuwe items. Deze worden waarschijnlijk niet weergegeven in aanbevelingen met Personen die dit hebben bekeken, Gezien dat en andere logica die is gebaseerd op gedrag in het verleden. U kunt de gelijkenis van de inhoud ook gebruiken om nuttige aanbevelingen voor nieuwe bezoekers te produceren, die geen vroegere aankopen of andere historische gegevens hebben.

Zie Vergelijkbaarheid van [inhoud voor meer informatie](/help/c-recommendations/c-algorithms/create-new-algorithm.md#similarity).

Deze logica kan met de volgende advisesleutels worden gebruikt:

* Huidig item
* Laatste object aangeschaft
* Laatst weergegeven item
* Meest bekeken item

### Meest bekeken

Hiermee geeft u de meest bekeken items op uw site weer.

Met deze logica kunt u aanbevelingen weergeven op basis van de meest bekeken items op uw site om de conversies voor andere items te verhogen. Een mediasite kan bijvoorbeeld op haar homepage aanbevelingen weergeven voor de meest populaire video&#39;s om bezoekers aan te moedigen aanvullende video&#39;s te bekijken.

Deze logica kan met de volgende advisesleutels worden gebruikt:

* Huidige rubriek
* Aangepast kenmerk
* Favoriete rubriek
* Populariteit

### Mensen die dit hebben gekocht, hebben het volgende gekocht

Geeft items weer die andere bezoekers ook hebben gekocht en die het geselecteerde item hebben gekocht.

Met deze logica kunt u de mogelijkheden voor cross-selling vergroten door bijvoorbeeld een aanbeveling weer te geven op een overzichtspagina van winkelwagentjes waarin objecten worden weergegeven die andere kopers ook hebben gekocht. Als de bezoeker bijvoorbeeld een pak aanschaft, kan de aanbeveling extra aangeschafte items weergeven, zoals bijvoorbeeld kleding, schoenen voor jurken en knipsels. Wanneer bezoekers hun aankopen bekijken, geeft u hun aanvullende aankoopaanbevelingen.

Deze logica kan met de volgende advisesleutels worden gebruikt:

* Huidig item
* Aangepast kenmerk
* Laatst gekocht object
* Laatst weergegeven item
* Meest bekeken item

### Mensen die dit bekeken hebben, hebben het volgende gekocht

Hiermee geeft u andere items weer die zijn gekocht door bezoekers die het geselecteerde item hebben weergegeven.

Met deze logica kunt u de mogelijkheden voor cross-selling vergroten door bijvoorbeeld een aanbeveling weer te geven op een productpagina die items weergeeft die andere bezoekers hebben bekeken die het object hebben gekocht. Als de bezoeker bijvoorbeeld een vispool bekijkt, kan de aanbeveling andere bezoekers die het aangeschafte artikel bekijken, zoals zakdoeken, golven, en vislazen, extra items laten zien. Wanneer bezoekers door uw site bladeren, geeft u hun aanvullende aankoopaanbevelingen.

Deze logica kan met de volgende advisesleutels worden gebruikt:

* Huidig item
* Aangepast kenmerk
* Laatst gekocht object
* Laatst weergegeven item
* Meest bekeken item

### Personen die dit hebben bekeken, zagen het volgende

Geeft items weer die andere bezoekers ook hebben weergegeven en die het geselecteerde item hebben bekeken.

Met deze logica kunt u aanvullende conversiemogelijkheden creëren door items aan te bevelen die andere bezoekers die een item hebben bekeken, ook hebben weergegeven. Bezoekers die op uw site fietsen bekijken, kunnen bijvoorbeeld ook fietshelmen, fietskits, sloten enzovoort bekijken. U kunt een aanbeveling maken met deze logica die andere producten aanbeveelt.

Deze logica kan met de volgende advisesleutels worden gebruikt:

* Huidig item
* Aangepast kenmerk
* Laatst gekocht object
* Laatst weergegeven item
* Meest bekeken item

### Affiniteit site

Geeft items weer met een eigen algoritme van de Adobe om andere items aan te bevelen op basis van criteria, zoals de weergave van productpagina&#39;s, aankopen en winkelwagenactiviteiten (toevoegen of verwijderen van items, bekijken van het winkelwagentje enz.)

Een onlinewinkel kan bijvoorbeeld items aanbevelen die een bezoeker tijdens eerdere sessies tijdens volgende bezoeken interesseert. De activiteit voor elke sessie van de bezoeker wordt vastgelegd om een affiniteitsscore te berekenen op basis van een recentiemodel en een frequentiemodel. Wanneer deze bezoeker terugkeert naar uw site, wordt de affiniteit van de site gebruikt om aanbevelingen weer te geven op basis van eerdere acties op uw site.

Deze logica kan met de volgende advisesleutels worden gebruikt:

* Huidig item
* Laatst gekocht object
* Laatst weergegeven item
* Meest bekeken item

### Topverkopers

Geeft de meest verkochte objecten op uw site weer op basis van bezoekersconversies.

Met deze logica kunt u aanbevelingen voor populaire items op uw site maken om de conversie te verhogen. Deze logica is vooral geschikt voor nieuwe bezoekers van uw site.

Deze logica kan met de volgende advisesleutels worden gebruikt:

* Favoriete rubriek
* Populariteit
