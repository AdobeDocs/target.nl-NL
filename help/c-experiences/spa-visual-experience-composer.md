---
keywords: spa vec;response;angular;response.js;spa visual experience composer;spa experience composer opties;single page apps;single-page-app;spa;mobile experience opties;target view
description: Leer hoe te om SPA VEC in Adobe Target te gebruiken om tests tot stand te brengen en inhoud op SPA op een doe-het-zelfmanier zonder ononderbroken ontwikkelingsgebiedsdelen te personaliseren.
title: Hoe gebruik ik Composer van de Ervaring van de Enige Pagina App Visuele (SPA VEC)?
feature: Visual Experience Composer (VEC)
translation-type: tm+mt
source-git-commit: bb27f6e540998f7dbe7642551f7a5013f2fd25b4
workflow-type: tm+mt
source-wordcount: '3655'
ht-degree: 0%

---


# Single Page App (SPA) Visual Experience Composer

In [!DNL Adobe Target] biedt de [!UICONTROL Visual Experience Composer] (VEC) marketers de mogelijkheid om zelf activiteiten te maken en ervaringen aan te passen die dynamisch kunnen worden geleverd bij traditionele toepassingen voor meerdere pagina&#39;s via Adobe Target global mbox. Nochtans, baseert dit zich op het terugwinnen van aanbiedingen op pagina-lading of verdere servervraag, die latentie, zoals aangetoond in het hieronder diagram introduceert. Deze aanpak werkt niet goed met toepassingen voor één pagina (SPA) omdat de gebruikerservaring en de prestaties van de toepassing hierdoor afnemen.

![Traditionele levenscyclus versus SPA levenscyclus](/help/c-experiences/assets/trad-vs-spa.png)

Met de nieuwste release introduceren we nu de VEC voor SPA. VEC voor SPA laat marketers toe om tests tot stand te brengen en inhoud op SPA op een doe-het-zelfmanier zonder ononderbroken ontwikkelingsgebiedsdelen te personaliseren. De VEC kan worden gebruikt om [A/B Test](/help/c-activities/t-test-ab/test-ab.md) en [Experience Targeting](/help/c-activities/t-experience-target/experience-target.md) (XT) activiteiten op populaire kaders, zoals React en Hoekig tot stand te brengen.

## Adobe Target Views and Single Page Applications

Adobe Target VEC for SPA maakt gebruik van een nieuw concept genaamd Views: een logische groep visuele elementen die samen een SPA ervaring vormen. Een SPA kan daarom worden beschouwd als een overgang door weergaven in plaats van URL&#39;s, op basis van gebruikersinteracties. Een weergave kan doorgaans een hele site of gegroepeerde visuele elementen binnen een site vertegenwoordigen.

Als u meer wilt weten over de weergaven, navigeert u naar deze hypothetische online e-commercesite die u in Reageren hebt geïmplementeerd en verkent u enkele voorbeeldweergaven. Klik op de onderstaande koppelingen om deze site te openen in een nieuw browsertabblad.

**Koppeling:  [Home Site](https://target.enablementadobe.com/react/demo/#/)**

![thuissite](/help/c-experiences/assets/home.png)

Wanneer we naar de thuissite navigeren, kunnen we meteen een hoofdafbeelding zien die een paasverkoop bevordert en de nieuwste producten die op de site worden verkocht. In dit geval, kan een Mening als volledige homesite worden gedefinieerd. Dit is handig om op te merken, aangezien we hier meer over zullen doen in de sectie Adobe Target-weergaven implementeren hieronder.

**Koppeling:  [Productsite](https://target.enablementadobe.com/react/demo/#/products)**

![productsite](/help/c-experiences/assets/product-site.png)

Aangezien wij meer in de producten geïnteresseerd raken, besluiten wij om de verbinding van Producten te klikken. Net als op de thuissite kan de hele productsite worden gedefinieerd als een weergave. We kunnen deze weergave &#39;producten&#39; noemen, net als de padnaam in `https://target.enablementadobe.com/react/demo/#/products`.

![productsite 2](/help/c-experiences/assets/product-site-2.png)

In het begin van deze sectie definieerden we Weergaven als de gehele site of zelfs als een groep visuele elementen op de site. Zoals hierboven wordt getoond, kunnen de vier producten die op de plaats worden getoond ook als Mening worden gegroepeerd en worden beschouwd. Als we deze weergave een naam willen geven, kunnen we deze &quot;producten&quot; noemen.

![productsite 3](/help/c-experiences/assets/product-site-3.png)

We besluiten op de knop Meer laden te klikken om meer producten op de site te verkennen. De URL van de website verandert in dit geval niet. Maar een weergave hier kan alleen de tweede rij producten weergeven die hierboven wordt weergegeven. De weergavenaam kan &#39;PRODUCTS-PAGE-2&#39; worden genoemd.

**Koppeling:  [Afhandeling](https://target.enablementadobe.com/react/demo/#/checkout)**

![uitcheckpagina](/help/c-experiences/assets/checkout.png)

Omdat we bepaalde producten op de site leuk vonden, besloten we een paar te kopen. Nu krijgen we op de uitchecksite enkele opties om normale levering of expreslevering te kiezen. Omdat een weergave elke groep visuele elementen op een site kan zijn, kunnen we deze &quot;Voorkeuren voor levering weergeven&quot; noemen.

Bovendien kan het concept van de standpunten veel verder worden uitgebreid. Als marketers de inhoud op de site willen aanpassen, afhankelijk van de geselecteerde leveringsvoorkeur, kan een Weergave worden gemaakt voor elke leveringsvoorkeur. In dit geval, wanneer wij Normale Levering selecteren, kan de Mening &quot;Normale Levering&quot;worden genoemd. Als Express Delivery is geselecteerd, kan de weergave de naam &quot;Express Delivery&quot; hebben.

Marktdeelnemers kunnen nu een A/B-test uitvoeren om te zien of het wijzigen van de kleur van blauw in rood wanneer Express Delivery is geselecteerd, conversies kan stimuleren in plaats van de knopkleur blauw te houden voor beide leveringsopties.

## Adobe Target-weergaven implementeren

Nu we hebben besproken wat Adobe Target Views is, kunnen we dit concept in Target gebruiken om marketers in staat te stellen A/B- en XT-tests uit te voeren op SPA via de VEC. Hiervoor is een eenmalige ontwikkelaarsinstelling vereist. Laten we de stappen doorlopen om dit in te stellen.

1. Installeer om 0.js 2.x.

   Eerst moeten we installeren op .js 2.x. Deze versie van at.js werd ontwikkeld met SPA in mening. Eerdere versies van at.js en mbox.js bieden geen ondersteuning voor Adobe Target Views en VEC for SPA.

   ![Dialoogvenster Implementatiedetails](/help/c-experiences/assets/imp-200.png)

   Download het bestand at.js 2.x via de gebruikersinterface van Adobe Target in [!UICONTROL Administration > Implementation]. at.js 2.x kan ook worden opgesteld via [Adobe Launch](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/cmp-implementing-target-using-adobe-launch.md). De Adobe Target-extensies zijn momenteel echter niet up-to-date en worden wel ondersteund.

1. Implementeer de nieuwste functie van at.js 2.x: [triggerView()](/help/c-implementing-target/c-implementing-target-for-client-side-web/adobe-target-triggerview-atjs-2.md) op uw sites.

   Nadat u de Weergaven van uw SPA hebt gedefinieerd waar u een A/B- of XT-test wilt uitvoeren, implementeert u de functie `triggerView()` van at.js 2.x met Weergaven die als parameter zijn doorgegeven. Dit staat marketers toe om VEC te gebruiken om de tests A/B en XT voor die Gedefinieerde Kijken te ontwerpen en in werking te stellen. Als de functie `triggerView()` niet voor die Meningen wordt bepaald, zal VEC niet de Meningen ontdekken en zo kunnen de verkopers VEC niet gebruiken om A/B en XT tests te ontwerpen en in werking te stellen.

   **`adobe.target.triggerView(viewName, options)`**

   | Parameter | Type | Vereist? | Validatie | Beschrijving |
   | --- | --- | --- | --- | --- |
   | viewName | String | Ja | 1. Geen navolgende spaties.<br>2. Kan niet leeg zijn.<br>3. De weergavenaam moet uniek zijn voor alle pagina&#39;s.<br>4. **Waarschuwing**: De weergavenaam mag niet beginnen of eindigen met &#39;`/`&#39;. De reden hiervoor is dat de klant doorgaans de weergavenaam uit het URL-pad haalt. Voor ons zijn &quot;home&quot; en &quot;`/home`&quot; anders.<br>5. **Waarschuwing**: Dezelfde weergave mag niet meerdere keren achter elkaar worden geactiveerd met de   `{page: true}` optie. | Geef een willekeurige naam door als een type tekenreeks dat u de weergave wilt vertegenwoordigen. Deze naam van Mening toont in [!UICONTROL Modifications] paneel van VEC voor marketers om acties tot stand te brengen en hun activiteiten A/B en XT in werking te stellen. |
   | opties | Object | Nee |  |  |
   | opties > pagina | Boolean | Nee |  | **TRUE**: De standaardwaarde van de pagina is true. Als `page=true` is, worden meldingen naar Edge-servers verzonden voor een toename van het aantal impressies.<br>**FALSE**: Wanneer  `page=false`worden geen meldingen verzonden voor het verhogen van het aantal impressies. Dit zou moeten worden gebruikt wanneer u een component op een pagina met een aanbieding slechts opnieuw wilt teruggeven. |

   Laten we nu een aantal voorbeelden bekijken van de manier waarop de functie `triggerView()` in Reageren kan worden aangeroepen voor onze hypothetische SPA e-commerce:

   **Koppeling:  [Home Site](https://target.enablementadobe.com/react/demo/#/)**

   ![home-response-1](/help/c-experiences/assets/react1.png)

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

   **Koppeling:  [Productsite](https://target.enablementadobe.com/react/demo/#/products)**

   Laten we nu een voorbeeld bekijken dat wat gecompliceerder is. Als marketers willen we bijvoorbeeld de tweede rij van de producten personaliseren door de kleur van het prijslabel te wijzigen in rood nadat een gebruiker op de knop Meer laden heeft geklikt.

   ![producten reageren](/help/c-experiences/assets/react4.png)

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

   **Koppeling:  [Afhandeling](https://target.enablementadobe.com/react/demo/#/checkout)**

   ![uitchecken reageren](/help/c-experiences/assets/react6.png)

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

   Wanneer `adobe.target.triggerView()` op uw SPA met de namen van de Mening wordt uitgevoerd die binnen als parameters worden overgegaan, zal VEC deze meningen kunnen ontdekken en gebruikers toestaan om acties en wijzigingen voor hun A/B of XT activiteiten tot stand te brengen.

   >[!NOTE]
   >
   >De VEC voor SPA is in feite dezelfde VEC als voor gewone webpagina&#39;s, maar er zijn enkele extra mogelijkheden beschikbaar wanneer u een app van één pagina opent met `triggerView()` geïmplementeerd.

Er zijn twee belangrijke verbeteringen aan [Modifications](/help/c-experiences/c-visual-experience-composer/c-vec-code-editor/vec-code-editor.md) paneel en Acties voor VEC die VEC toestaan om goed met SPA te werken.

**Deelvenster Wijzigingen**

In het deelvenster [!UICONTROL Modifications], zoals hieronder wordt weergegeven, worden de acties vastgelegd die voor een bepaalde weergave zijn gemaakt. Alle acties voor een weergave worden gegroepeerd onder die weergave.

**Handelingen**

Wanneer u op een handeling klikt, wordt het element op de site gemarkeerd waarop deze handeling wordt toegepast. Elke VEC-actie die onder een Weergave wordt gemaakt, heeft de volgende pictogrammen, zoals hieronder wordt getoond: Informatie, Bewerken, Klonen, Verplaatsen en Verwijderen.

![Wijzigingen](/help/c-experiences/assets/modifications.png)

In de volgende tabel wordt elke actie beschreven:

| Pagina | Beschrijving |
| --- | --- |
| Informatie | Geeft de details van de handeling weer. |
| Bewerken | Hiermee kunt u de eigenschappen van de handeling rechtstreeks bewerken. |
| Klonen | Kloont de actie aan één of meerdere Weergaven die op [!UICONTROL Modifications] paneel of aan één of meerdere Weergaven bestaan die u hebt doorzocht en aan in VEC genavigeerd. De handeling hoeft niet noodzakelijkerwijs in het deelvenster [!UICONTROL Modifications] te staan.<br>**Opmerking**: Nadat een kloonverrichting wordt gemaakt, moet u aan de Mening in VEC via navigeren  [!UICONTROL Browse] om te zien of de gekloonde actie een geldige verrichting was. Als de actie niet op de Mening kan worden toegepast, zult u een fout zien. |
| Verplaatsen | Hiermee wordt de handeling verplaatst naar een gebeurtenis Pagina laden of een andere weergave die al bestaat in het deelvenster Wijzigingen.<br>[!UICONTROL Page Load Event] - alle handelingen die overeenkomen met de gebeurtenis load van de pagina worden toegepast op de eerste pagina die wordt geladen van uw webtoepassing.<br>**** NoteAfter een bewegingsverrichting wordt gemaakt, moet u aan de Mening in VEC via Browse navigeren om te zien of de beweging een geldige verrichting was. Als de handeling niet kan worden toegepast op de weergave, wordt een fout weergegeven |
| Verwijderen | Hiermee verwijdert u de handeling. |

>[!NOTE]
>
>U kunt vele acties uitvoeren alvorens de pagina in VEC laadt, of zelfs als de pagina niet volledig kan laden. Handelingen die niet kunnen worden bewerkt voordat de site wordt geladen, worden uitgeschakeld in de gebruikersinterface.

**Voorbeeld 1**

Zie het bovenstaande voorbeeld waarin we een weergave Home hebben gemaakt. Ons doel is tweeledig voor deze visie:

1. Wijzig de knoppen Toevoegen aan winkelwagentje en Soortgelijk in een lichtere blauwe kleur. Dit moet in de modus &quot;Pagina laden&quot; staan, omdat de componenten van de koptekst veranderen.
1. Wijzig het label &quot;Nieuwste producten voor 2019&quot; in &quot;Hottest Products for 2019&quot; met de tekstkleur gewijzigd in paars.

Om deze doelstellingen uit te voeren, in VEC, klik [!UICONTROL Compose] en pas die veranderingen op de mening van het Huis toe.

![Voorbeeld 1](/help/c-experiences/assets/example1.png)

**Voorbeeld 2**

Raadpleeg het bovenstaande voorbeeld waarin we een PRODUCTS-PAGE-2-weergave hebben gemaakt. Ons doel is om het label Prijs te wijzigen in Verkoopprijs met de labelkleur rood.

1. Klik [!UICONTROL Browse], dan klik de [!UICONTROL Products] verbinding bij de kopbal.
1. Klik eenmaal [!UICONTROL Load More] om naar de tweede rij producten te gaan.
1. Klik op [!UICONTROL Compose].
1. Pas handelingen toe om het tekstlabel te wijzigen in Verkoopprijs en de kleur in rood.

![Voorbeeld 2](/help/c-experiences/assets/example2.png)

**Voorbeeld 3**

Tot slot kunnen, zoals eerder vermeld, weergaven in korreligheid worden gedefinieerd. Weergaven kunnen een status of zelfs een optie via een keuzerondje zijn. Eerder hebben we weergaven gemaakt als CHECKOUT-EXPRESS en CHECKOUT-NORMAL. Ons doel is de knopkleur te wijzigen in rood voor de CHECKOUT-EXPRESS-weergave.

1. Klik op [!UICONTROL Browse].
1. Voeg een paar producten toe aan het winkelwagentje.
1. Klik op het pictogram van het winkelwagentje in de rechterbovenhoek.
1. Klik op Uitchecken van uw bestelling.
1. Klik op het keuzerondje Expreslevering.
1. Klik op [!UICONTROL Compose].
1. Klik op de knop Betalen om de knop Bestelling voltooien te lezen en de kleur rood te wijzigen.

![Voorbeeld 3](/help/c-experiences/assets/example3.png)

>[!NOTE]
>
>De weergave UITCHECKUNNEN-EXPRESS wordt pas weergegeven in het deelvenster Wijzigen als u op het keuzerondje Uitdrukkelijke levering klikt. De reden hiervoor is dat de functie `triggerView()` wordt geactiveerd wanneer het keuzerondje Expreslevering is geselecteerd. Dit is alleen mogelijk wanneer VEC weet dat er een Weergave moet worden weergegeven in het wijzigingspaneel.

## Diep duiken in at.js en SPA

**Hoe kan ik meningen voor de recentste publieksgegevens terugwinnen die door acties na de aanvankelijke paginading op mijn SPA worden gehydrateerd?**

De typische workflow van at.js 2.x is wanneer uw site wordt geladen, worden al uw weergaven en handelingen in het cachegeheugen opgeslagen, zodat volgende gebruikersacties op uw site geen serveraanroepen activeren om aanbiedingen op te halen. Als u weergaven wilt ophalen afhankelijk van de meest actuele profielgegevens die mogelijk zijn bijgewerkt afhankelijk van de volgende gebruikershandelingen, kunt u `getOffers()` en `applyOffers()` aanroepen met de meest recente gebruikers- of profielgegevens die zijn doorgegeven.

Stel bijvoorbeeld dat u een telecombedrijf bent en dat u een SPA hebt die at.js 2.x gebruikt. Als bedrijf, wilt u de volgende doelstellingen bereiken:

* Voor een aangemelde of anonieme gebruiker, toon de recentste bedrijfsbevordering, zoals het tonen van een &quot;Eerste maand vrije&quot;heldenaanbieding op `http://www.telecom.com/home`.
* Voor een aangemelde gebruiker, toon een verbeteringsbevorderingsaanbieding voor gebruikers van wie contracten omhoog komen, zoals &quot;u verkiest voor een vrije telefoon!&quot; op `http://www.telecom.com/loggedIn/home`.

Nu, noemt uw ontwikkelaars meningen en roepen `triggerView()` op de volgende manier:

* Voor `http://www.telecom.com/home` is de weergavenaam &quot;Startpagina afgemeld&quot;
   * `triggerView(“Logged Out Home”)` wordt aangeroepen.
* Voor `http://www.telecom.com/loggedIn/home` is de weergavenaam &quot;Aangemeld thuis&quot;
   * `triggerView(“Logged In Home”)` wordt aangehaald op routeverandering.

Uw marketers voeren dan de volgende A/B-activiteiten door VEC uit:

* A/B activiteit met de &quot;Eerste Maand Vrije&quot;aanbieding voor publiek met de parameter &quot;`loggedIn= false`&quot;om in `http://www.telecom.com/home` worden getoond, waar de meningsnaam Startpagina Logged uit is.
* A/B activiteit met &quot;u komt voor een vrije telefoon in aanmerking!&quot; biedt het publiek met de parameter &quot;`loggedIn=true`&quot; aan om te worden getoond in `http://www.telecom.com/loggedIn/home`, waar de meningsnaam in Hero Aanbieding wordt geregistreerd.

Nu, laten wij deze gebruikersstroom overwegen:

1. Een anonieme aangemelde gebruiker landt op uw pagina.
1. Omdat u at.js 2.x gebruikt, gaat u in de parameter &quot;`loggedIn = false`&quot;op pagina-lading over om alle meningen terug te winnen huidig in actieve activiteiten die voor kwalificeren wanneer het publiek parameter &quot;`loggedIn = false`&quot;heeft.
1. at.js 2.x wint dan de Logged Out mening en de actie van het Huis terug om de &quot;Eerste Maand Vrije&quot;aanbieding te tonen en het op te slaan in geheim voorgeheugen.
1. Wanneer `triggerView(“Logged Out Home”)` wordt aangehaald, wordt de &quot;First Month Free&quot;aanbieding teruggewonnen van geheim voorgeheugen en de aanbieding wordt getoond zonder een servervraag.
1. De gebruiker klikt nu op Aanmelden en geeft zijn of haar referenties.
1. Aangezien uw website een SPA is, wordt de volledige pagina niet geladen en wordt de gebruiker doorgestuurd naar `http://www.telecom.com/loggedIn/home`.

Hier is het probleem. De gebruiker login en wij ontmoeten `triggerView(“Logged In Home”)` omdat wij deze code op routeverandering plaatsten. Dit vertelt at.js 2.x om de mening en de acties van geheim voorgeheugen terug te winnen, maar de enige mening die in geheim voorgeheugen bestaat is Logged Out Huis.

Dus hoe kunnen we dan onze aanmeldingsgegevens ophalen en de &quot;You are acceptable for a free phone&quot; weergeven? aanbieden? En aangezien alle verdere acties op uw plaats van een het programma geopend-in gebruikersperspectief zullen zijn, hoe kunt u ervoor zorgen alle verdere acties in gepersonaliseerde aanbiedingen voor het programma geopende gebruikers resulteren?

U kunt de nieuwe `getOffers()` en `applyOffers()` functies gebruiken die in at.js 2.x worden gesteund:

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

Geef de reactie van `getOffers()` aan `applyOffers()` door en nu zullen alle meningen en acties verbonden aan &quot;het programma geopende = waar&quot;zullen bijwerken het at.js geheime voorgeheugen.

Met andere woorden, 2.x in.js steunt een manier om meningen, acties, en aanbiedingen met de meest bijgewerkte publieksgegevens op een wijze op bestelling terug te winnen.

**Biedt at.js 2.x ondersteuning voor A4T voor toepassingen voor één pagina?**

Ja, at.js 2.x steunt A4T voor SPA via de `triggerView()` functie aangezien u Adobe Analytics en de Dienst van identiteitskaart van de Bezoeker van Experience Cloud hebt uitgevoerd. Zie het onderstaande diagram met stapsgewijze beschrijvingen.

![Doelstroom](/help/c-experiences/assets/atjs-spa-flow.png)

| Stap | Beschrijving |
| --- | --- |
| 1 | `triggerView()` wordt opgeroepen in de SPA om een weergave te renderen en acties toe te passen om visuele elementen die aan de weergave zijn gekoppeld, te wijzigen. |
| 2 | De gerichte inhoud voor de mening wordt gelezen van het geheime voorgeheugen. |
| 3 | Gerichte inhoud wordt zo snel mogelijk zichtbaar zonder flikkering van de standaardinhoud. |
| 4 | Het verzoek om een melding wordt verzonden naar de Target Profile Store om de bezoeker te tellen in de activiteit en de verhogingsmetriek. |
| 5 | Analytische gegevens die naar de Servers van de Inzameling van Gegevens worden verzonden. |
| 6 | De doelgegevens worden via de SDID aangepast aan de analysegegevens en worden verwerkt in de analytische rapportageopslag. De analysegegevens kunnen dan in zowel Analytics als Doel via A4T- rapporten worden bekeken. |

>[!NOTE]
>Als u geen berichten naar Adobe Analytics wilt verzenden voor het tellen van de indruk telkens wanneer een weergave wordt geactiveerd, geeft u `{page: false}` door aan de functie `triggerView()`, zodat het tellen van de indruk niet wordt opgeblazen wanneer een weergave meerdere keren wordt geactiveerd voor een component die constant opnieuw wordt gerenderd. Bijvoorbeeld:
>
>`adobe.target.triggerView(“PRODUCTS-PAGE-2”, {page:false})`

## Ondersteunde activiteiten

| Type activiteit | Ondersteund? |
| --- | --- |
| [A/B-test](/help/c-activities/t-test-ab/test-ab.md) | Ja |
| [Recommendations als ](/help/c-recommendations/recommendations-as-an-offer.md)<br>aanbieder van activiteiten op het gebied van A/B Test en Experience Targeting (XT) | Ja |
| [Automatisch toewijzen](/help/c-activities/automated-traffic-allocation/automated-traffic-allocation.md) | Ja |
| [Gericht op ervaring](/help/c-activities/t-experience-target/experience-target.md) | Ja |
| [Multivariatietest](/help/c-activities/c-multivariate-testing/multivariate-testing.md) | Nee |
| [Automatisch doel](/help/c-activities/auto-target/auto-target-to-optimize.md) | Nee |
| [Automated Personalization](/help/c-activities/t-automated-personalization/automated-personalization.md) | Nee |
| [Recommendations](/help/c-recommendations/recommendations.md) | Nee |

**Als wij bij .js 2.x installeerden en  `triggerView()` op onze plaatsen ten uitvoer gelegd, hoe stellen wij auto-Doel A/B activiteiten in werking omdat SPA VEC geen auto-Doel steunt?**

Als u Auto-Doel A/B activiteiten wilt gebruiken, kunt u al uw acties bewegen die op de Gebeurtenis van de Lading van de Pagina in VEC moeten worden uitgevoerd. Houd de cursor boven elke handeling en klik op de knop [!UICONTROL Move to Page Load Event]. Nadat dit, in de volgende stap wordt gedaan, kunt u auto-Doel voor de methode van de verkeerstoewijzing selecteren.

## Ondersteunde integratie

| Integratie | Ondersteund? |
| --- | --- |
| [Analyses voor doel (A4T)](/help/c-integrating-target-with-mac/a4t/a4t.md) | Ja |
| [Experience Cloud publiek](/help/c-integrating-target-with-mac/mmp.md) | Ja |
| [Klantkenmerken](/help/c-target/c-visitor-profile/working-with-customer-attributes.md) | Ja |
| [Fragmenten voor AEM](/help/c-experiences/c-manage-content/aem-experience-fragments.md) | Ja |

## Ondersteunde functies {#supported-features}

| Functie | Ondersteund? |
| --- | --- |
| [Werkruimten en eigenschappen](/help/administrating-target/c-user-management/property-channel/property-channel.md) | Ja |
| [QA-koppelingen](/help/c-activities/c-activity-qa/activity-qa.md) | Ja |
| [Form-based Experience Composer](/help/c-experiences/form-experience-composer.md) | Nee |
| [Aangepaste code](/help/c-experiences/c-visual-experience-composer/c-vec-code-editor/vec-code-editor.md) | Ja |
| [VEC-opties](/help/c-experiences/c-visual-experience-composer/viztarget-options.md) | Alles |
| [Klikken en bijhouden](/help/c-activities/r-success-metrics/click-tracking.md) | Ja |
| [Levering van meerdere activiteiten](/help/c-experiences/c-visual-experience-composer/multipage-activity.md) | Ja |

## De montages van de Levering van de pagina voor SPA VEC {#page-delivery-settings}

[!UICONTROL Page Delivery] de montages laten u regels vormen om te bepalen wanneer een activiteit van het Doel voor een publiek zou moeten kwalificeren en uitvoeren.

Als u vanuit de stap **[!UICONTROL Experiences]** toegang wilt tot de [!UICONTROL Page Delivery]-opties vanuit de workflow voor het maken van activiteiten met instructies in drie delen van de VEC, klikt u **[!UICONTROL Configure]** (het tandwielpictogram) > **[!UICONTROL Page Delivery]**.

![Dialoogvenster Opties voor paginaaflevering](/help/c-experiences/assets/page-delivery.png)

Bijvoorbeeld, zoals gedefinieerd door de [!UICONTROL Page Delivery] hierboven getoonde montages, kwalificeert een activiteit van het Doel en voert uit wanneer een bezoeker direct op `https://www.adobe.com` *of* wanneer een bezoeker op om het even welke URL landt die `https://www.adobe.com/products` bevat. Dit werkt perfect voor elke toepassing met meerdere pagina&#39;s waarin elke interactie met de pagina een pagina opnieuw laadt, waarvoor at.js de activiteiten ophaalt die in aanmerking komen voor de URL waarnaar de gebruiker navigeert.

Nochtans, omdat SPA verschillend werken, moeten de [!UICONTROL Page Delivery] montages op een bepaalde manier worden gevormd die alle acties om op de Mening toestaat worden toegepast zoals die in de SPA activiteit VEC wordt bepaald.

### Voorbeeld van gebruik

Overweeg dit voorbeeld use-case:

![SPA deelvenster VEC-wijzigingen](/help/c-experiences/assets/page-delivery-example.png)

De volgende wijzigingen zijn aangebracht:

* De achtergrondkleur is gewijzigd in de weergave Home, die zich onder de URL bevindt: [https://target.enablementadobe.com/react/demo/#/](https://target.enablementadobe.com/react/demo/#/).
* De knopkleur is gewijzigd in de weergave Producten, die zich onder de URL bevindt: [https://target.enablementadobe.com/react/demo/#/products](https://target.enablementadobe.com/react/demo/#/products).

Met het bovenstaande voorbeeld in mening, wat zou gebeuren wanneer wij [!UICONTROL Page Delivery] montages om slechts omvatten te vormen: [https://target.enablementadobe.com/react/demo/#/](https://target.enablementadobe.com/react/demo/#/) in een SPA met at.js 2.*x*?

![Dialoogvenster Pagina-aflevering](/help/c-experiences/assets/spa-page-delivery.png)

In de volgende afbeelding ziet u de aanvraag voor het laden van de doelstroom - pagina in at.js 2.*x*:

![Doelstroom - bij.js 2.0 Aanvraag voor laden van pagina](/help/c-experiences/assets/page-load-request.png)

**Gebruikersreis #1**

* Een gebruiker navigeert direct naar [https://target.enablementadobe.com/react/demo/#/](https://target.enablementadobe.com/react/demo/#/).
* te.js 2.*Hiermee* wordt een query naar Edge uitgevoerd om te kijken of er activiteiten nodig zijn voor de URL:  [https://target.enablementadobe.com/react/demo/#/](https://target.enablementadobe.com/react/demo/#/).
* In stap 6, keert de Rand van het Doel de acties voor de mening van het Huis en van Producten terug zodat zij binnen browser in het voorgeheugen worden opgeslagen.

**Resultaat**: De gebruiker ziet de groene achtergrondkleur in de weergave Home. Wanneer de gebruiker dan aan [https://target.enablementadobe.com/react/demo/#/products](https://target.enablementadobe.com/react/demo/#/products) navigeert, wordt de blauwe achtergrondkleur van de knoop gezien omdat de actie in het voorgeheugen onder browser onder de mening van Producten wordt in het voorgeheugen ondergebracht.

Opmerking: De gebruiker die naar [https://target.enablementadobe.com/react/demo/#/products](https://target.enablementadobe.com/react/demo/#/products) navigeert, heeft geen paginalading geactiveerd.

**Gebruikersreis #2**

* Een gebruiker navigeert direct naar [https://target.enablementadobe.com/react/demo/#/products](https://target.enablementadobe.com/react/demo/#/products).
* te.js 2.*Hiermee* wordt een query naar Edge uitgevoerd om te kijken of er activiteiten nodig zijn voor de URL:  [https://target.enablementadobe.com/react/demo/#/products](https://target.enablementadobe.com/react/demo/#/products).
* Er zijn geen activiteiten die zijn gekwalificeerd voor [https://target.enablementadobe.com/react/demo/#/products](https://target.enablementadobe.com/react/demo/#/products).
* Omdat er geen activiteiten gekwalificeerd zijn, zijn er geen acties en meningen om voor at.js 2 worden in het voorgeheugen onder te brengen.** xto trigger van.

**Resultaat**: Zelfs als u  `triggerView()` voor de Mening van Producten hebt bepaald en een actie aan de Mening van Producten door SPA VEC gemaakt, zult u niet de verwachte actie zien aangezien u geen regel creeerde die  [https://target.enablementadobe.com/react/demo/#/](https://target.enablementadobe.com/react/demo/#/products) producten in de montages van de Levering van de Pagina omvatte.

### Beste praktijken

U kunt zien dat het beheren van de gebruikersreis vrij moeilijk kan zijn aangezien de gebruikers op om het even welke URL van uw SPA kunnen landen en aan een andere pagina kunnen navigeren. Daarom is het beter om een regel van de Levering van de Pagina te specificeren die basis URL omvat zodat het uw volledige SPA omvat. Op deze manier hoeft u niet na te denken over alle verschillende reizen en paden die een gebruiker kan maken om naar een pagina te gaan waarop u een doelactiviteit voor A/B-test of -ervaring (XT) wilt weergeven.

Als u bijvoorbeeld het bovenstaande probleem wilt verhelpen, kunt u de basis-URL opgeven in de instellingen voor het leveren van pagina&#39;s als zodanig:

![Dialoogvenster Pagina-aflevering](/help/c-experiences/assets/conclusion.png)

Zo zorgt u ervoor dat de acties worden weergegeven wanneer een bezoeker op de SPA landt en naar de weergave Home of Pagina navigeert.

Nu, wanneer u een actie aan een Mening in SPA VEC toevoegt, zullen wij u het volgende pop-up bericht tonen om u eraan te herinneren om over de [!UICONTROL Page Delivery] regels te denken.

![Bericht over instellingen pagina](/help/c-experiences/assets/pop-up-message.png)

Dit bericht wordt weergegeven wanneer u de eerste actie toevoegt aan een Weergave voor elke nieuwe activiteit die u maakt. Dit bericht helpt ervoor zorgen dat iedereen in uw organisatie leert hoe te om deze [!UICONTROL Page Delivery] regels correct toe te passen.

## Trainingsvideo: VEC gebruiken voor SPA in Adobe Target

>[!VIDEO](https://video.tv.adobe.com/v/26249)

Zie [De Visual Experience Composer voor de Toepassing van de Enige Pagina (SPA VEC) in Adobe Target](https://helpx.adobe.com/target/kt/using/visual-experience-composer-for-single-page-applications-feature-video-use.html) voor meer informatie gebruiken.
