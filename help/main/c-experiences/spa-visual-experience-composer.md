---
keywords: spa vec;response;angular;response.js;spa visual experience composer;spa experience composer opties;single page apps;single-page-app;spa;mobile experience opties;target view
description: Leer hoe u de SPA VEC in Adobe gebruikt [!DNL Target] om tests tot stand te brengen en inhoud op SPA op een doe-het-zelfmanier zonder ononderbroken ontwikkelingsgebiedsdelen te personaliseren.
title: Hoe gebruik ik Composer van de Ervaring van de Enige Pagina App Visuele (SPA VEC)?
feature: Visual Experience Composer (VEC)
exl-id: fd3dcfaa-e5c6-45a1-8229-9c206562e5b0
source-git-commit: b1e8ea2370fc15f4bfcd960ab2960cafe2db92b8
workflow-type: tm+mt
source-wordcount: '3676'
ht-degree: 0%

---

# Single Page App (SPA) Visual Experience Composer

In [!DNL Adobe Target]de [!UICONTROL Visual Experience Composer] (VEC) biedt marketers de mogelijkheid om zelf activiteiten te maken en ervaringen te personaliseren die dynamisch kunnen worden aangeboden op traditionele toepassingen voor meerdere pagina&#39;s via Adobe Target global mbox. Nochtans, baseert dit zich op het terugwinnen van aanbiedingen op pagina-lading of verdere servervraag, die latentie, zoals aangetoond in het hieronder diagram introduceert. Deze aanpak werkt niet goed met toepassingen voor één pagina (SPA) omdat de gebruikerservaring en de prestaties van de toepassing hierdoor afnemen.

![Traditionele levenscyclus versus SPA levenscyclus](/help/main/c-experiences/assets/trad-vs-spa.png)

Met de nieuwste release introduceren we nu de VEC voor SPA. VEC voor SPA laat marketers toe om tests tot stand te brengen en inhoud op SPA op een doe-het-zelfmanier zonder ononderbroken ontwikkelingsgebiedsdelen te personaliseren. VEC kan worden gebruikt om tot stand te brengen [A/B-test](/help/main/c-activities/t-test-ab/test-ab.md) en [Gericht op ervaring](/help/main/c-activities/t-experience-target/experience-target.md) (XT) activiteiten met betrekking tot populaire frameworks, zoals React en Angular.

## Adobe [!DNL Target] Weergaven en toepassingen voor één pagina

Adobe Target VEC for SPA maakt gebruik van een nieuw concept genaamd Views: een logische groep visuele elementen die samen een SPA ervaring vormen. Een SPA kan daarom worden beschouwd als een overgang door weergaven in plaats van URL&#39;s, op basis van gebruikersinteracties. Een weergave kan doorgaans een hele site of gegroepeerde visuele elementen binnen een site vertegenwoordigen.

Als u meer wilt weten over de weergaven, navigeert u naar deze hypothetische online e-commercesite die u in Reageren hebt geïmplementeerd en verkent u enkele voorbeeldweergaven. Klik op de onderstaande koppelingen om deze site te openen in een nieuw browsertabblad.

**Koppeling: [Home Site](https://target.enablementadobe.com/react/demo/#/)**

![thuissite](/help/main/c-experiences/assets/home.png)

Wanneer we naar de thuissite navigeren, kunnen we meteen een hoofdafbeelding zien die een paasverkoop bevordert en de nieuwste producten die op de site worden verkocht. In dit geval, kan een Mening als volledige homesite worden gedefinieerd. Dit is handig om op te merken, aangezien we hier meer over zullen doen in de sectie Adobe Target-weergaven implementeren hieronder.

**Koppeling: [Productsite](https://target.enablementadobe.com/react/demo/#/products)**

![productsite](/help/main/c-experiences/assets/product-site.png)

Aangezien wij meer in de producten geïnteresseerd raken, besluiten wij om de verbinding van Producten te klikken. Net als op de thuissite kan de hele productsite worden gedefinieerd als een weergave. Deze weergave kan net als de padnaam in `https://target.enablementadobe.com/react/demo/#/products`.

![productsite 2](/help/main/c-experiences/assets/product-site-2.png)

In het begin van deze sectie definieerden we Weergaven als de gehele site of zelfs als een groep visuele elementen op de site. Zoals hierboven wordt getoond, kunnen de vier producten die op de plaats worden getoond ook als Mening worden gegroepeerd en worden beschouwd. Als we deze weergave een naam willen geven, kunnen we deze &quot;producten&quot; noemen.

![productsite 3](/help/main/c-experiences/assets/product-site-3.png)

We besluiten op de knop Meer laden te klikken om meer producten op de site te verkennen. De URL van de website verandert in dit geval niet. Maar een weergave hier kan alleen de tweede rij producten weergeven die hierboven wordt weergegeven. De weergavenaam kan &#39;PRODUCTS-PAGE-2&#39; worden genoemd.

**Koppeling: [Afhandeling](https://target.enablementadobe.com/react/demo/#/checkout)**

![uitcheckpagina](/help/main/c-experiences/assets/checkout.png)

Omdat we bepaalde producten op de site leuk vonden, besloten we een paar te kopen. Nu krijgen we op de uitchecksite enkele opties om normale levering of expreslevering te kiezen. Omdat een weergave elke groep visuele elementen op een site kan zijn, kunnen we deze &quot;Voorkeuren voor levering weergeven&quot; noemen.

Bovendien kan het concept van de standpunten veel verder worden uitgebreid. Als marketers de inhoud op de site willen aanpassen, afhankelijk van de geselecteerde leveringsvoorkeur, kan een Weergave worden gemaakt voor elke leveringsvoorkeur. In dit geval, wanneer wij Normale Levering selecteren, kan de Mening &quot;Normale Levering&quot;worden genoemd. Als Express Delivery is geselecteerd, kan de weergave de naam &quot;Express Delivery&quot; hebben.

Marktdeelnemers kunnen nu een A/B-test uitvoeren om te zien of het wijzigen van de kleur van blauw in rood wanneer Express Delivery is geselecteerd, conversies kan stimuleren in plaats van de knopkleur blauw te houden voor beide leveringsopties.

## Adobe uitvoeren [!DNL Target] Weergaven

Nu we hebben besproken wat Adobe Target Views is, kunnen we dit concept in Target gebruiken om marketers in staat te stellen A/B- en XT-tests uit te voeren op SPA via de VEC. Hiervoor is een eenmalige ontwikkelaarsinstelling vereist. Laten we de stappen doorlopen om dit in te stellen.

1. Installeer om 0.js 2.x.

   Eerst moeten we installeren op .js 2.x. Deze versie van at.js werd ontwikkeld met SPA in mening. Eerdere versies van at.js en bieden geen ondersteuning voor Adobe Target Views en de VEC for SPA.

   ![Dialoogvenster Implementatiedetails](/help/main/c-experiences/assets/imp-200.png)

   Download het bestand at.js 2.x via de gebruikersinterface van Adobe Target in [!UICONTROL Administration > Implementation]. at.js 2.x kan ook worden geïmplementeerd via tags in [Adobe Experience Platform](https://developer.adobe.com/target/implement/client-side/atjs/how-to-deployatjs/implement-target-using-adobe-launch/). De Adobe Target-extensies zijn momenteel echter niet up-to-date en worden wel ondersteund.

1. Implementeer de nieuwste functie van at.js 2.x: [triggerView()](https://developer.adobe.com/target/implement/client-side/atjs/atjs-functions/adobe-target-triggerview-atjs-2/) op uw sites.

   Nadat u de Weergaven van uw SPA hebt gedefinieerd waar u een A/B- of XT-test wilt uitvoeren, implementeert u at.js 2.x `triggerView()` gebruiken met Weergaven die als parameter worden doorgegeven. Dit staat marketers toe om VEC te gebruiken om de tests A/B en XT voor die Gedefinieerde Kijken te ontwerpen en in werking te stellen. Als de `triggerView()` De functie wordt niet bepaald voor die Kijken, zal VEC niet de Kijken ontdekken en zo kunnen de verkopers niet VEC gebruiken om A/B en XT tests te ontwerpen en in werking te stellen.

   **`adobe.target.triggerView(viewName, options)`**

   | Parameter | Type | Vereist? | Validatie | Beschrijving |
   | --- | --- | --- | --- | --- |
   | viewName | String | Ja | 1. Geen navolgende spaties.<br>2. Kan niet leeg zijn.<br>3. De weergavenaam moet uniek zijn voor alle pagina&#39;s.<br>4. **Waarschuwing**: De naam van de weergave mag niet beginnen of eindigen met &#39;`/`&quot;. De reden hiervoor is dat de klant doorgaans de weergavenaam uit het URL-pad haalt. Voor ons, &quot;home&quot; en &quot;`/home`&quot; verschillen.<br>5. **Waarschuwing**: Dezelfde weergave mag niet meerdere keren achtereenvolgens worden geactiveerd met de  `{page: true}` optie. | Geef een willekeurige naam door als een type tekenreeks dat u de weergave wilt vertegenwoordigen. Deze weergavenaam wordt weergegeven in het dialoogvenster [!UICONTROL Modifications] paneel van VEC voor marketers om acties tot stand te brengen en hun activiteiten A/B en XT in werking te stellen. |
   | opties | Object | Nee |  |  |
   | opties > pagina | Boolean | Nee |  | **TRUE**: De standaardwaarde van de pagina is true. Wanneer `page=true`, worden meldingen naar Edge-servers verzonden voor een toename van het aantal impressies.<br>**FALSE**: Wanneer `page=false`, worden meldingen niet verzonden voor het verhogen van het aantal impressies. Dit zou moeten worden gebruikt wanneer u een component op een pagina met een aanbieding slechts opnieuw wilt teruggeven. |

   Laten we nu een aantal voorbeelden bekijken van de manier waarop u de `triggerView()` functie in React voor onze hypothetische e-commerce SPA:

   **Koppeling: [Home Site](https://target.enablementadobe.com/react/demo/#/)**

   ![home-response-1](/help/main/c-experiences/assets/react1.png)

   Als marketers, als wij A/B tests op de volledige homesite willen in werking stellen, dan zouden wij de mening &quot;huis&quot;kunnen noemen die uit URL kan worden gehaald:

   ```javascript
   function targetView() {
     var viewName = window.location.hash; // or use window.location.pathName if router works on path and not hash
   
     viewName = viewName || 'home'; // view name cannot be empty
   
     // Sanitize viewName to get rid of any trailing symbols derived from URL
     if (viewName.startsWith('#') || viewName.startsWith('/')) {
       viewName = viewName.substr(1);
     }
   
     // Validate if the Target Libraries are available on your website
     if (typeof adobe != 'undefined' && adobe.target && typeof adobe.target.triggerView === 'function') {
       adobe.target.triggerView(viewName);
     }
   }
   
   // react router v4
   const history = syncHistoryWithStore(createBrowserHistory(), store);
   history.listen(targetView);
   
   // react router v3
   <Router history={hashHistory} onUpdate={targetView} >
   ```

   **Koppeling: [Productsite](https://target.enablementadobe.com/react/demo/#/products)**

   Laten we nu een voorbeeld bekijken dat wat gecompliceerder is. Als marketers willen we bijvoorbeeld de tweede rij van de producten personaliseren door de kleur van het prijslabel te wijzigen in rood nadat een gebruiker op de knop Meer laden heeft geklikt.

   ![producten reageren](/help/main/c-experiences/assets/react4.png)

   ```javascript
   function targetView(viewName) {
     // Validate if the Target Libraries are available on your website
     if (typeof adobe != 'undefined' && adobe.target && typeof adobe.target.triggerView === 'function') {
       adobe.target.triggerView(viewName);
     }
   }
   
   class Products extends Component {
     render() {
       return (
         <button type="button" onClick={this.handleLoadMoreClicked}>Load more</button>
       );
     }
   
     handleLoadMoreClicked() {
       var page = this.state.page + 1; // assuming page number is derived from component’s state
       this.setState({page: page});
       targetView('PRODUCTS-PAGE-' + page);
     }
   }
   ```

   **Koppeling: [Afhandeling](https://target.enablementadobe.com/react/demo/#/checkout)**

   ![uitchecken reageren](/help/main/c-experiences/assets/react6.png)

   Als marketers de inhoud op de site willen aanpassen, afhankelijk van de geselecteerde leveringsvoorkeur, kan een Weergave worden gemaakt voor elke leveringsvoorkeur. In dit geval, wanneer wij Normale Levering selecteren, kan de Mening &quot;Normale Levering&quot;worden genoemd. Als Express Delivery is geselecteerd, kan de weergave de naam &quot;Express Delivery&quot; hebben.

   Marketers willen nu een A/B-test uitvoeren om te zien of het wijzigen van de kleur van blauw in rood wanneer de optie Uitdrukkelijke levering is ingeschakeld, conversies kan stimuleren in plaats van de knopkleur blauw te houden voor beide leveringsopties.

   ```javascript
   function targetView(viewName) {
     // Validate if the Target Libraries are available on your website
     if (typeof adobe != 'undefined' && adobe.target && typeof adobe.target.triggerView === 'function') {
       adobe.target.triggerView(viewName);
     }
   }
   
   class Checkout extends Component {
     render() {
       return (
         <div onChange={this.onDeliveryPreferenceChanged}>
           <label>
             <input type="radio" id="normal" name="deliveryPreference" value={"Normal Delivery"} defaultChecked={true}/>
             <span> Normal Delivery (7-10 business days)</span>
           </label>
   
           <label>
             <input type="radio" id="express" name="deliveryPreference" value={"Express Delivery"}/>
             <span> Express Delivery* (2-3 business days)</span>
           </label>
         </div>
       );
     }
     onDeliveryPreferenceChanged(evt) {
       var selectedPreferenceValue = evt.target.value;
       targetView(selectedPreferenceValue);
     }
   }
   ```

1. Start A/B- of XT-activiteiten via de VEC.

   Wanneer `adobe.target.triggerView()` wordt uitgevoerd op uw SPA met de namen van de Mening binnen als parameters worden overgegaan, zal VEC deze meningen kunnen ontdekken en gebruikers toestaan om acties en wijzigingen voor hun activiteiten tot stand te brengen A/B of XT.

   >[!NOTE]
   >
   >De VEC voor SPA is eigenlijk dezelfde VEC als die u gebruikt op gewone webpagina&#39;s, maar er zijn enkele extra mogelijkheden beschikbaar wanneer u een app van één pagina opent met `triggerView()` geïmplementeerd.

Er zijn twee belangrijke verbeteringen in de [Wijzigingen](/help/main/c-experiences/c-visual-experience-composer/c-vec-code-editor/vec-code-editor.md) en Acties voor VEC die VEC toestaan om goed met SPA te werken.

**Deelvenster Wijzigingen**

De [!UICONTROL Modifications] worden de acties vastgelegd die voor een bepaalde weergave zijn gemaakt, zoals hieronder wordt weergegeven. Alle acties voor een weergave worden gegroepeerd onder die weergave.

**Handelingen**

Wanneer u op een handeling klikt, wordt het element op de site gemarkeerd waarop deze handeling wordt toegepast. Elke VEC-actie die onder een Weergave wordt gemaakt, heeft de volgende pictogrammen, zoals hieronder wordt getoond: Informatie, Bewerken, Klonen, Verplaatsen en Verwijderen.

![Wijzigingen](/help/main/c-experiences/assets/modifications.png)

In de volgende tabel wordt elke actie beschreven:

| Pagina | Beschrijving |
| --- | --- |
| Informatie | Geeft de details van de handeling weer. |
| Bewerken | Hiermee kunt u de eigenschappen van de handeling rechtstreeks bewerken. |
| Klonen | De handeling klonen naar een of meer weergaven in het dialoogvenster [!UICONTROL Modifications] of naar een of meer weergaven waarnaar u hebt gebladerd en waarnaar u in de VEC hebt genavigeerd. De handeling hoeft niet noodzakelijkerwijs te bestaan in het dialoogvenster [!UICONTROL Modifications] deelvenster.<br>**Opmerking**: Nadat een kloonverrichting wordt gemaakt, moet u aan de Mening in VEC via navigeren [!UICONTROL Browse] om te zien of de gekloonde actie een geldige bewerking was. Als de actie niet op de Mening kan worden toegepast, zult u een fout zien. |
| Verplaatsen | Hiermee wordt de handeling verplaatst naar een gebeurtenis Pagina laden of een andere weergave die al bestaat in het deelvenster Wijzigingen.<br>[!UICONTROL Page Load Event] - alle handelingen die overeenkomen met de gebeurtenis load van de pagina worden toegepast op de eerste pagina die wordt geladen van uw webtoepassing.<br>**Opmerking** Nadat een bewegingsverrichting wordt gemaakt, moet u aan de Mening in VEC via Browse navigeren om te zien of de beweging een geldige verrichting was. Als de handeling niet kan worden toegepast op de weergave, wordt een fout weergegeven |
| Verwijderen | Hiermee verwijdert u de handeling. |

>[!NOTE]
>
>U kunt vele acties uitvoeren alvorens de pagina in VEC laadt, of zelfs als de pagina niet volledig kan laden. Handelingen die niet kunnen worden bewerkt voordat de site wordt geladen, worden uitgeschakeld in de gebruikersinterface.

**Voorbeeld 1**

Zie het bovenstaande voorbeeld waarin we een weergave Home hebben gemaakt. Ons doel is tweeledig voor deze visie:

1. Wijzig de knoppen Toevoegen aan winkelwagentje en Soortgelijk in een lichtere blauwe kleur. Dit moet in de modus &quot;Pagina laden&quot; staan, omdat de componenten van de koptekst veranderen.
1. Wijzig het label &quot;Nieuwste producten voor 2019&quot; in &quot;Hottest Products for 2019&quot; met de tekstkleur gewijzigd in paars.

Om deze doelstellingen uit te voeren, in VEC, klik [!UICONTROL Compose] en pas deze wijzigingen toe in de weergave Home.

![Voorbeeld 1](/help/main/c-experiences/assets/example1.png)

**Voorbeeld 2**

Raadpleeg het bovenstaande voorbeeld waarin we een PRODUCTS-PAGE-2-weergave hebben gemaakt. Ons doel is om het label Prijs te wijzigen in Verkoopprijs met de labelkleur rood.

1. Klikken [!UICONTROL Browse]klikt u op de knop [!UICONTROL Products] koppeling in de koptekst.
1. Klikken [!UICONTROL Load More] één keer om tot de tweede rij producten te komen.
1. Klik op [!UICONTROL Compose].
1. Pas handelingen toe om het tekstlabel te wijzigen in Verkoopprijs en de kleur in rood.

![Voorbeeld 2](/help/main/c-experiences/assets/example2.png)

**Voorbeeld 3**

Tot slot kunnen, zoals eerder vermeld, weergaven in korreligheid worden gedefinieerd. Weergaven kunnen een status of zelfs een optie via een keuzerondje zijn. Eerder hebben we weergaven gemaakt als CHECKOUT-EXPRESS en CHECKOUT-NORMAL. Ons doel is de knopkleur te wijzigen in rood voor de CHECKOUT-EXPRESS-weergave.

1. Klik op [!UICONTROL Browse].
1. Voeg een paar producten toe aan het winkelwagentje.
1. Klik op het pictogram van het winkelwagentje in de rechterbovenhoek.
1. Klik op Uitchecken van uw bestelling.
1. Klik op het keuzerondje Expreslevering.
1. Klik op [!UICONTROL Compose].
1. Klik op de knop Betalen om de knop Bestelling voltooien te lezen en de kleur rood te wijzigen.

![Voorbeeld 3](/help/main/c-experiences/assets/example3.png)

>[!NOTE]
>
>De weergave UITCHECKUNNEN-EXPRESS wordt pas weergegeven in het deelvenster Wijzigen als u op het keuzerondje Uitdrukkelijke levering klikt. Dit komt omdat de `triggerView()` Deze functie wordt geactiveerd wanneer het keuzerondje Expreslevering is geselecteerd en dit is alleen wanneer VEC weet dat er een Weergave moet worden weergegeven in het deelvenster Wijzigen.

## Diep duiken in at.js en SPA

**Hoe kan ik meningen voor de recentste publieksgegevens terugwinnen die door acties na de aanvankelijke paginading op mijn SPA worden gehydrateerd?**

De typische workflow van at.js 2.x is wanneer uw site wordt geladen, worden al uw weergaven en handelingen in het cachegeheugen opgeslagen, zodat volgende gebruikersacties op uw site geen serveraanroepen activeren om aanbiedingen op te halen. Als u weergaven wilt ophalen afhankelijk van de meest actuele profielgegevens die mogelijk zijn bijgewerkt, afhankelijk van de volgende gebruikershandelingen, kunt u `getOffers()` en `applyOffers()` met de recentste publieksgebruiker of profielgegevens overgegaan.

Stel bijvoorbeeld dat u een telecombedrijf bent en dat u een SPA hebt die at.js 2.x gebruikt. Als bedrijf, wilt u de volgende doelstellingen bereiken:

* Voor een aangemelde of anonieme gebruiker kunt u de meest recente bedrijfsbevordering weergeven, zoals het weergeven van een &quot;First month free&quot;-hoofdaanbieding op `http://www.telecom.com/home`.
* Voor een aangemelde gebruiker, toon een verbeteringsbevorderingsaanbieding voor gebruikers van wie contracten omhoog komen, zoals &quot;u verkiest voor een vrije telefoon!&quot; op `http://www.telecom.com/loggedIn/home`.

Nu, noemen uw ontwikkelaars meningen en roepen `triggerView()` op de volgende wijze:

* Voor `http://www.telecom.com/home` de weergavenaam is &quot;Startpagina Afgemeld&quot;
   * `triggerView(“Logged Out Home”)` wordt aangeroepen.
* Voor `http://www.telecom.com/loggedIn/home` de weergavenaam is &quot;Aangemeld thuis&quot;
   * `triggerView(“Logged In Home”)` wordt aangehaald op routeverandering.

Uw marketers voeren dan de volgende A/B-activiteiten door VEC uit:

* A/B activiteit met het &quot;First Month Free&quot; aanbod voor publiek met de parameter &quot;`loggedIn= false`&quot; in `http://www.telecom.com/home`, waarbij de weergavenaam Startpagina Afgemeld is.
* A/B activiteit met &quot;u komt voor een vrije telefoon in aanmerking!&quot; aanbod voor publiek met de parameter &quot;`loggedIn=true`&quot; in `http://www.telecom.com/loggedIn/home`, waarbij de weergavenaam is aangemeld bij hoofdaanbieding.

Nu, laten wij deze gebruikersstroom overwegen:

1. Een anonieme aangemelde gebruiker landt op uw pagina.
1. Omdat u at.js 2.x gebruikt, geeft u de parameter &quot;`loggedIn = false`&quot; tijdens het laden van de pagina om alle weergaven op te halen die aanwezig zijn in actieve activiteiten die in aanmerking komen voor de parameter &quot;`loggedIn = false`&quot;.
1. at.js 2.x wint dan de Logged Out mening en de actie van het Huis terug om de &quot;Eerste Maand Vrije&quot;aanbieding te tonen en het op te slaan in geheim voorgeheugen.
1. Wanneer `triggerView(“Logged Out Home”)` wordt aangehaald, wordt de &quot;Eerste Maand Vrije&quot;aanbieding teruggewonnen van geheim voorgeheugen en de aanbieding wordt getoond zonder een servervraag.
1. De gebruiker klikt nu op Aanmelden en geeft zijn of haar referenties.
1. Omdat uw website een SPA is, wordt de volledige pagina niet geladen en wordt de gebruiker doorgestuurd naar `http://www.telecom.com/loggedIn/home`.

Hier is het probleem. De gebruiker meldt zich aan en wij ontmoeten `triggerView(“Logged In Home”)` omdat wij deze code op routeverandering plaatsten. Dit vertelt at.js 2.x om de mening en de acties van geheim voorgeheugen terug te winnen, maar de enige mening die in geheim voorgeheugen bestaat is Logged Out Huis.

Dus hoe kunnen we dan onze aanmeldingsgegevens ophalen en de &quot;You are acceptable for a free phone&quot; weergeven? aanbieden? En aangezien alle verdere acties op uw plaats van een het programma geopend-in gebruikersperspectief zullen zijn, hoe kunt u ervoor zorgen alle verdere acties in gepersonaliseerde aanbiedingen voor het programma geopende gebruikers resulteren?

U kunt de nieuwe `getOffers()` en `applyOffers()` functies die worden ondersteund in at.js 2.x:

```javascript
adobe.target.getOffers({
  request: {
  prefetch: {
    "views": [
      {
        "parameters": {
          "loggedIn": true
        },
      }
    ]
  },
});
```

Geef de respons van `getOffers()` tot `applyOffers()` en nu zullen alle meningen en acties verbonden aan &quot;het programma geopende = waar&quot;het at.js geheime voorgeheugen bijwerken.

Met andere woorden, 2.x in.js steunt een manier om meningen, acties, en aanbiedingen met de meest bijgewerkte publieksgegevens op een wijze op bestelling terug te winnen.

**Biedt at.js 2.x ondersteuning voor A4T voor toepassingen voor één pagina?**

Ja, bij.js 2.x ondersteunt A4T voor SPA via de `triggerView()` -functie omdat u Adobe Analytics en de Experience Cloud-bezoeker-id-service hebt geïmplementeerd. Zie het onderstaande diagram met stapsgewijze beschrijvingen.

![Doelstroom](/help/main/c-experiences/assets/atjs-spa-flow.png)

| Stap | Beschrijving |
| --- | --- |
| 1 | `triggerView()` wordt opgeroepen in de SPA om een weergave te renderen en acties toe te passen om visuele elementen die aan de weergave zijn gekoppeld, te wijzigen. |
| 2 | De gerichte inhoud voor de mening wordt gelezen van het geheime voorgeheugen. |
| 3 | Gerichte inhoud wordt zo snel mogelijk zichtbaar zonder flikkering van de standaardinhoud. |
| 4 | Het verzoek om een melding wordt verzonden naar de Target Profile Store om de bezoeker te tellen in de activiteit en de verhogingsmetriek. |
| 5 | Analytische gegevens die naar de Servers van de Inzameling van Gegevens worden verzonden. |
| 6 | De doelgegevens worden via de SDID aangepast aan de analysegegevens en worden verwerkt in de analytische rapportageopslag. De analysegegevens kunnen dan in zowel Analytics als Doel via A4T- rapporten worden bekeken. |

>[!NOTE]
>Als u geen berichten naar Adobe Analytics wilt verzenden om de indruk te tellen telkens wanneer een weergave wordt geactiveerd, geeft u `{page: false}` aan de `triggerView()` zodat het tellen van de indruk niet wordt opgeblazen wanneer een mening veelvoudige tijden voor een component wordt teweeggebracht die constant opnieuw teruggeeft. Bijvoorbeeld:
>
>`adobe.target.triggerView(“PRODUCTS-PAGE-2”, {page:false})`

## Ondersteunde activiteiten

| Type activiteit | Ondersteund? |
| --- | --- |
| [A/B-test](/help/main/c-activities/t-test-ab/test-ab.md) | Ja |
| [Recommendations als voorstel](/help/main/c-recommendations/recommendations-as-an-offer.md)<br>in activiteiten voor tests en ervaring met A/B gericht op (XT) activiteiten | Ja |
| [Automatisch toewijzen](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md) | Ja |
| [Gericht op ervaring](/help/main/c-activities/t-experience-target/experience-target.md) | Ja |
| [Multivariatietest](/help/main/c-activities/c-multivariate-testing/multivariate-testing.md) | Nee |
| [Automatisch doel](/help/main/c-activities/auto-target/auto-target-to-optimize.md) | Nee |
| [Automated Personalization](/help/main/c-activities/t-automated-personalization/automated-personalization.md) | Nee |
| [Recommendations](/help/main/c-recommendations/recommendations.md) | Nee |

**Als we op 2.js 2.x hebben geïnstalleerd en geïmplementeerd `triggerView()` op onze plaatsen, hoe stellen wij Auto-Doel A/B activiteiten in werking omdat SPA VEC auto-Doel niet steunt?**

Als u Auto-Doel A/B activiteiten wilt gebruiken, kunt u al uw acties bewegen die op de Gebeurtenis van de Lading van de Pagina in VEC moeten worden uitgevoerd. Houd de muisaanwijzer boven elke actie en klik op de knop [!UICONTROL Move to Page Load Event] knop. Nadat dit, in de volgende stap wordt gedaan, kunt u auto-Doel voor de methode van de verkeerstoewijzing selecteren.

## Ondersteunde integratie

| Integratie | Ondersteund? |
| --- | --- |
| [Analyses voor doel (A4T)](/help/main/c-integrating-target-with-mac/a4t/a4t.md) | Ja |
| [Experience Cloud publiek](/help/main/c-integrating-target-with-mac/mmp.md) | Ja |
| [Klantkenmerken](https://developer.adobe.com/target/before-implement/methods-to-get-data-into-target/customer-attributes/) | Ja |
| [Fragmenten voor AEM](/help/main/c-experiences/c-manage-content/aem-experience-fragments.md) | Ja |

## Ondersteunde functies {#supported-features}

| Functie | Ondersteund? |
| --- | --- |
| [Werkruimten en eigenschappen](/help/main/administrating-target/c-user-management/property-channel/property-channel.md) | Ja |
| [QA-koppelingen](/help/main/c-activities/c-activity-qa/activity-qa.md) | Ja |
| [Form-based Experience Composer](/help/main/c-experiences/form-experience-composer.md) | Nee |
| [Aangepaste code](/help/main/c-experiences/c-visual-experience-composer/c-vec-code-editor/vec-code-editor.md) | Ja |
| [VEC-opties](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md) | Alles |
| [Klikken en bijhouden](/help/main/c-activities/r-success-metrics/click-tracking.md) | Ja |
| [Levering van meerdere activiteiten](/help/main/c-experiences/c-visual-experience-composer/multipage-activity.md) | Ja |

## De montages van de Levering van de pagina voor SPA VEC {#page-delivery-settings}

[!UICONTROL Page Delivery] de montages laten u regels vormen om te bepalen wanneer een activiteit van het Doel voor een publiek zou moeten kwalificeren en uitvoeren.

Om toegang te krijgen tot [!UICONTROL Page Delivery] opties vanuit de workflow voor het maken van activiteiten met instructies in drie delen van de VEC, vanuit de **[!UICONTROL Experiences]** stap, klik op **[!UICONTROL Configure]** (het tandwielpictogram) > **[!UICONTROL Page Delivery]**.

![Dialoogvenster Opties voor paginaaflevering](/help/main/c-experiences/assets/page-delivery.png)

Zoals gedefinieerd door de [!UICONTROL Page Delivery] hierboven weergegeven instellingen, kwalificeert een doelactiviteit en wordt deze uitgevoerd wanneer een bezoeker rechtstreeks landt op `https://www.adobe.com` *of* wanneer een bezoeker landt op een URL die `https://www.adobe.com/products`. Dit werkt perfect voor elke toepassing met meerdere pagina&#39;s waarin elke interactie met de pagina een pagina opnieuw laadt, waarvoor at.js de activiteiten ophaalt die in aanmerking komen voor de URL waarnaar de gebruiker navigeert.

Maar omdat SPA anders werken, [!UICONTROL Page Delivery] de montages moeten op een manier worden gevormd die alle acties om op de Meningen zoals die in de SPA activiteit VEC worden bepaald toelaat worden toegepast.

### Voorbeeld van gebruik

Overweeg dit voorbeeld use-case:

![SPA deelvenster VEC-wijzigingen](/help/main/c-experiences/assets/page-delivery-example.png)

De volgende wijzigingen zijn aangebracht:

* De achtergrondkleur is gewijzigd in de weergave Home, die zich onder de URL bevindt: [https://target.enablementadobe.com/react/demo/#/](https://target.enablementadobe.com/react/demo/#/).
* De knopkleur is gewijzigd in de weergave Producten, die zich onder de URL bevindt: [https://target.enablementadobe.com/react/demo/#/products](https://target.enablementadobe.com/react/demo/#/products).

Met het bovenstaande voorbeeld in mening, wat zou gebeuren wanneer wij vormen [!UICONTROL Page Delivery] alleen in te voegen instellingen: [https://target.enablementadobe.com/react/demo/#/](https://target.enablementadobe.com/react/demo/#/) in een SPA met at.js 2.*x*?

![Dialoogvenster Pagina-aflevering](/help/main/c-experiences/assets/spa-page-delivery.png)

In de volgende afbeelding ziet u de aanvraag voor het laden van de doelstroom - pagina in at.js 2.*x*:

![Doelstroom - bij.js 2.0 Aanvraag voor laden van pagina](/help/main/c-experiences/assets/page-load-request.png)

**Gebruikersreis #1**

* Een gebruiker navigeert rechtstreeks naar [https://target.enablementadobe.com/react/demo/#/](https://target.enablementadobe.com/react/demo/#/).
* te.js 2.*x* maakt een vraag aan Edge om te zien of moet om het even welke activiteit voor URL uitvoeren: [https://target.enablementadobe.com/react/demo/#/](https://target.enablementadobe.com/react/demo/#/).
* In stap 6, keert de Rand van het Doel de acties voor de mening van het Huis en van Producten terug zodat zij binnen browser in het voorgeheugen worden opgeslagen.

**Resultaat**: De gebruiker ziet de groene achtergrondkleur in de weergave Home. Wanneer de gebruiker dan navigeert naar [https://target.enablementadobe.com/react/demo/#/products](https://target.enablementadobe.com/react/demo/#/products)De blauwe achtergrondkleur van de knop wordt weergegeven omdat de handeling in de browser onder de weergave Producten is opgeslagen.

Opmerking: De gebruiker die navigeert naar [https://target.enablementadobe.com/react/demo/#/products](https://target.enablementadobe.com/react/demo/#/products) heeft geen paginalading geactiveerd.

**Gebruikersreis #2**

* Een gebruiker navigeert rechtstreeks naar [https://target.enablementadobe.com/react/demo/#/products](https://target.enablementadobe.com/react/demo/#/products).
* te.js 2.*x* maakt een vraag aan Edge om te zien of moet om het even welke activiteit voor URL uitvoeren: [https://target.enablementadobe.com/react/demo/#/products](https://target.enablementadobe.com/react/demo/#/products).
* Er zijn geen activiteiten die gekwalificeerd zijn voor [https://target.enablementadobe.com/react/demo/#/products](https://target.enablementadobe.com/react/demo/#/products).
* Omdat er geen activiteiten gekwalificeerd zijn, zijn er geen acties en meningen om voor at.js 2 worden in het voorgeheugen onder te brengen.*x* om te activeren vanaf.

**Resultaat**: Zelfs als u `triggerView()` voor de Mening van Producten en maakte een actie aan de Mening van Producten door SPA VEC, zult u niet de verwachte actie zien aangezien u geen regel creeerde die inbegrepen [https://target.enablementadobe.com/react/demo/#/products](https://target.enablementadobe.com/react/demo/#/products) in de instellingen voor Paginaaflevering.

### Beste praktijken

U kunt zien dat het beheren van de gebruikersreis vrij moeilijk kan zijn aangezien de gebruikers op om het even welke URL van uw SPA kunnen landen en aan een andere pagina kunnen navigeren. Daarom is het beter om een regel van de Levering van de Pagina te specificeren die basis URL omvat zodat het uw volledige SPA omvat. Op deze manier hoeft u niet na te denken over alle verschillende reizen en paden die een gebruiker kan maken om naar een pagina te gaan waarop u een doelactiviteit voor A/B-test of -ervaring (XT) wilt weergeven.

Als u bijvoorbeeld het bovenstaande probleem wilt verhelpen, kunt u de basis-URL opgeven in de instellingen voor het leveren van pagina&#39;s als zodanig:

![Dialoogvenster Pagina-aflevering](/help/main/c-experiences/assets/conclusion.png)

Zo zorgt u ervoor dat de acties worden weergegeven wanneer een bezoeker op de SPA landt en naar de weergave Home of Pagina navigeert.

Nu, wanneer u een actie aan een Mening in SPA VEC toevoegt, zullen wij u het volgende pop-up bericht tonen om u eraan te herinneren om over te denken [!UICONTROL Page Delivery] regels.

![Bericht over instellingen pagina](/help/main/c-experiences/assets/pop-up-message.png)

Dit bericht wordt weergegeven wanneer u de eerste actie toevoegt aan een Weergave voor elke nieuwe activiteit die u maakt. Dit bericht helpt ervoor te zorgen dat iedereen in uw organisatie leert hoe te om deze toe te passen [!UICONTROL Page Delivery] correct worden toegepast.

## Trainingsvideo: VEC gebruiken voor SPA in Adobe Target

>[!VIDEO](https://video.tv.adobe.com/v/26249)

Zie [De Visual Experience Composer gebruiken voor de Toepassing van de Enige Pagina (SPA VEC) in Adobe Target](https://helpx.adobe.com/target/kt/using/visual-experience-composer-for-single-page-applications-feature-video-use.html) voor meer informatie .
