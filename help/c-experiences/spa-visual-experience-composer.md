---
keywords: spa vec;react;angular;react.js;spa visual experience composer;spa experience composer options;single page apps;single-page-app;spa;mobile experience options;target view
description: De visuele Composer van de Ervaring (VEC) voor Enige Pagina Apps (SPAs) in Adobe Target laat marketers toe om tests tot stand te brengen en inhoud op SPAs op een wijze te personaliseren doe-het-zelf zonder ononderbroken ontwikkelingsgebiedsdelen. De VEC kan worden gebruikt om activiteiten op populaire kaders, zoals React en Angular tot stand te brengen.
title: Single Page App (SPA) Visual Experience Composer
topic: Standard
uuid: 4dcd6d9c-b2e3-4759-a2e0-3696c572faba
translation-type: tm+mt
source-git-commit: 3edb13b196240bb1918fc66edcc653936e32d3ef
workflow-type: tm+mt
source-wordcount: '3648'
ht-degree: 0%

---


# Single Page App (SPA) Visual Experience Composer {#single-page-app-spa-visual-experience-composer}

In [!DNL Adobe Target], geeft [!UICONTROL Visual Experience Composer] (VEC) marketers een doe-het-zelf vermogen om activiteiten tot stand te brengen en ervaringen te personaliseren die dynamisch op traditionele Toepassingen van de Multi-Pagina via Adobe Target globale mbox kunnen worden geleverd. Nochtans, baseert dit zich op het terugwinnen van aanbiedingen op pagina-lading of verdere servervraag, die latentie, zoals aangetoond in het hieronder diagram introduceert. Deze benadering werkt niet goed met de Toepassingen van de Enige Pagina (SPAs) omdat het de gebruikerservaring en toepassingsprestaties degradeert.

![Traditionele levenscyclus vs. SPA-levenscyclus](/help/c-experiences/assets/trad-vs-spa.png)

Met de recentste versie, introduceren wij nu VEC voor SPAs. VEC voor SPAs laat marketers toe om tests tot stand te brengen en inhoud op SPAs op een doe-het-zelfmanier zonder ononderbroken ontwikkelingsgebiedsdelen te personaliseren. De VEC kan worden gebruikt om [A/B Test](/help/c-activities/t-test-ab/test-ab.md) en [Ervaring gerichte](/help/c-activities/t-experience-target/experience-target.md) (XT) activiteiten op populaire kaders, zoals React en Hoekig tot stand te brengen.

## Adobe Target Views and Single Page Applications

Adobe Target VEC voor SPAs haalt voordeel uit een nieuw concept genoemd Bekijken: een logische groep van visuele elementen die samen omhoog een ervaring van het KUUROORD maken. Een KUUROORD kan daarom als transitioning door meningen, in plaats van URLs worden beschouwd, die op gebruikersinteractie wordt gebaseerd. Een weergave kan doorgaans een hele site of gegroepeerde visuele elementen binnen een site vertegenwoordigen.

Als u meer wilt weten over de weergaven, navigeert u naar deze hypothetische online e-commercesite die u in Reageren hebt geïmplementeerd en verkent u enkele voorbeeldweergaven. Klik op de onderstaande koppelingen om deze site te openen in een nieuw browsertabblad.

**Koppeling:[Home Site](https://target.enablementadobe.com/react/demo/#/)**

![thuissite](/help/c-experiences/assets/home.png)

Wanneer we naar de thuissite navigeren, kunnen we meteen een hoofdafbeelding zien die een paasverkoop bevordert en de nieuwste producten die op de site worden verkocht. In dit geval, kan een Mening als volledige homesite worden gedefinieerd. Dit is handig om op te merken, aangezien we hier meer over zullen doen in de sectie Adobe Target-weergaven implementeren hieronder.

**Koppeling:[Productsite](https://target.enablementadobe.com/react/demo/#/products)**

![productsite](/help/c-experiences/assets/product-site.png)

Aangezien wij meer in de producten geïnteresseerd raken, besluiten wij om de verbinding van Producten te klikken. Net als op de thuissite kan de hele productsite worden gedefinieerd als een weergave. We kunnen deze weergave &#39;producten&#39; noemen, net als de padnaam in `https://target.enablementadobe.com/react/demo/#/products`.

![productsite 2](/help/c-experiences/assets/product-site-2.png)

In het begin van deze sectie definieerden we Weergaven als de gehele site of zelfs als een groep visuele elementen op de site. Zoals hierboven wordt getoond, kunnen de vier producten die op de plaats worden getoond ook als Mening worden gegroepeerd en worden beschouwd. Als we deze weergave een naam willen geven, kunnen we deze &quot;producten&quot; noemen.

![productsite 3](/help/c-experiences/assets/product-site-3.png)

We besluiten op de knop Meer laden te klikken om meer producten op de site te verkennen. De URL van de website verandert in dit geval niet. Maar een weergave hier kan alleen de tweede rij producten weergeven die hierboven wordt weergegeven. De weergavenaam kan &#39;PRODUCTS-PAGE-2&#39; worden genoemd.

**Koppeling:[Afhandeling](https://target.enablementadobe.com/react/demo/#/checkout)**

![uitcheckpagina](/help/c-experiences/assets/checkout.png)

Omdat we bepaalde producten op de site leuk vonden, besloten we een paar te kopen. Nu krijgen we op de uitchecksite enkele opties om normale levering of expreslevering te kiezen. Omdat een weergave elke groep visuele elementen op een site kan zijn, kunnen we deze &quot;Voorkeuren voor levering weergeven&quot; noemen.

Bovendien kan het concept van de standpunten veel verder worden uitgebreid. Als marketers de inhoud op de site willen aanpassen, afhankelijk van de geselecteerde leveringsvoorkeur, kan een Weergave worden gemaakt voor elke leveringsvoorkeur. In dit geval, wanneer wij Normale Levering selecteren, kan de Mening &quot;Normale Levering&quot;worden genoemd. Als Express Delivery is geselecteerd, kan de weergave de naam &quot;Express Delivery&quot; hebben.

Marktdeelnemers kunnen nu een A/B-test uitvoeren om te zien of het wijzigen van de kleur van blauw in rood wanneer Express Delivery is geselecteerd, conversies kan stimuleren in plaats van de knopkleur blauw te houden voor beide leveringsopties.

## Adobe Target-weergaven implementeren

Nu wij hebben behandeld wat de Weergaven van Adobe Target zijn, kunnen wij hefboomwerking dit concept in Target aan machtigen marktleiders om tests A/B en XT op SPAs via VEC in werking te stellen. Hiervoor is een eenmalige ontwikkelaarsinstelling vereist. Laten we de stappen doorlopen om dit in te stellen.

1. Installeer om 0.js 2.x.

   Eerst moeten we installeren op .js 2.x. Deze versie van at.js werd ontwikkeld met SPAs in mening. Eerdere versies van at.js en mbox.js ondersteunen geen Adobe Target Views en VEC voor SPA.

   ![Dialoogvenster Implementatiedetails](/help/c-experiences/assets/imp-200.png)

   Download het bestand at.js 2.x via de gebruikersinterface van Adobe Target in [!UICONTROL Administration > Implementation]. at.js 2.x kan ook worden geïmplementeerd via [Adobe Launch](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/cmp-implementing-target-using-adobe-launch.md). De Adobe Target Extensions zijn momenteel echter niet up-to-date en worden wel ondersteund.

1. Implementeer de nieuwste functie van at.js 2.x: [triggerView()](/help/c-implementing-target/c-implementing-target-for-client-side-web/adobe-target-triggerview-atjs-2.md) op uw sites.

   Na het bepalen van de Weergaven van uw SPA waar u een A/B of XT test wilt in werking stellen, voer de `triggerView()` functie van at.js 2.x met de Bekijken uit binnen als parameter worden overgegaan. Dit staat marketers toe om VEC te gebruiken om de tests A/B en XT voor die Gedefinieerde Kijken te ontwerpen en in werking te stellen. Als de `triggerView()` functie niet voor die Meningen wordt bepaald, zal VEC niet de Meningen ontdekken en zo kunnen de verkopers VEC niet gebruiken om A/B en XT tests te ontwerpen en in werking te stellen.

   **`adobe.target.triggerView(viewName, options)`**

   | Parameter | Type | Vereist? | Validatie | Beschrijving |
   | --- | --- | --- | --- | --- |
   | viewName | String | Ja | 1. Geen navolgende spaties.<br>2. Kan niet leeg zijn.<br>3. De weergavenaam moet uniek zijn voor alle pagina&#39;s.<br>4. **Waarschuwing**: De weergavenaam mag niet beginnen of eindigen met &#39;`/`&#39;. De reden hiervoor is dat de klant doorgaans de weergavenaam uit het URL-pad haalt. Voor ons zijn &quot;thuis&quot; en &quot;`/home`&quot; anders.<br>5. **Waarschuwing**: Dezelfde weergave mag niet meerdere keren achter elkaar worden geactiveerd met de `{page: true}` optie. | Geef een willekeurige naam door als een type tekenreeks dat u de weergave wilt vertegenwoordigen. Deze naam van Mening toont in het [!UICONTROL Modifications] paneel van VEC voor marketers om acties tot stand te brengen en hun activiteiten A/B en XT in werking te stellen. |
   | opties | Object | Nee |  |  |
   | opties > pagina | Boolean | Nee |  | **TRUE**: De standaardwaarde van de pagina is true. Wanneer `page=true`, zullen de berichten naar de servers van de Rand voor het verhogen van immentatietelling worden verzonden.<br>**FALSE **: Wanneer`page=false`worden geen meldingen verzonden voor het verhogen van het aantal impressies. Dit zou moeten worden gebruikt wanneer u een component op een pagina met een aanbieding slechts opnieuw wilt teruggeven. |

   Nu ga door één of ander voorbeeld gebruiksgevallen op hoe te om de `triggerView()` functie in Reageren voor onze hypothetische e-commerce SPA aan te halen:

   **Koppeling:[Home Site](https://target.enablementadobe.com/react/demo/#/)**

   ![home-response-1](/help/c-experiences/assets/react1.png)

   Als marketers, als wij A/B tests op de volledige homesite willen in werking stellen, dan zouden wij de mening &quot;huis&quot;kunnen noemen die uit URL kan worden gehaald:

   ```
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

   **Koppeling:[Productsite](https://target.enablementadobe.com/react/demo/#/products)**

   Laten we nu een voorbeeld bekijken dat wat gecompliceerder is. Als marketers willen we bijvoorbeeld de tweede rij van de producten personaliseren door de kleur van het prijslabel te wijzigen in rood nadat een gebruiker op de knop Meer laden heeft geklikt.

   ![producten reageren](/help/c-experiences/assets/react4.png)

   ```
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

   **Koppeling:[Afhandeling](https://target.enablementadobe.com/react/demo/#/checkout)**

   ![uitchecken reageren](/help/c-experiences/assets/react6.png)

   Als marketers de inhoud op de site willen aanpassen, afhankelijk van de geselecteerde leveringsvoorkeur, kan een Weergave worden gemaakt voor elke leveringsvoorkeur. In dit geval, wanneer wij Normale Levering selecteren, kan de Mening &quot;Normale Levering&quot;worden genoemd. Als Express Delivery is geselecteerd, kan de weergave de naam &quot;Express Delivery&quot; hebben.

   Marketers willen nu een A/B-test uitvoeren om te zien of het wijzigen van de kleur van blauw in rood wanneer de optie Uitdrukkelijke levering is ingeschakeld, conversies kan stimuleren in plaats van de knopkleur blauw te houden voor beide leveringsopties.

   ```
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

   Wanneer `adobe.target.triggerView()` op uw KUUROORD met de namen van de Mening binnen als parameters worden overgegaan, zal VEC deze meningen kunnen ontdekken en gebruikers toestaan om acties en wijzigingen voor hun A/B of XT activiteiten tot stand te brengen.

   >[!NOTE]
   >
   >VEC voor SPAs is werkelijk het zelfde VEC dat u op regelmatige Web-pagina&#39;s gebruikt, maar sommige extra mogelijkheden zijn beschikbaar wanneer u één enkele paginaapp met `triggerView()` uitgevoerd opent.

Er zijn twee belangrijke verbeteringen aan het paneel van [Aanpassingen](/help/c-experiences/c-visual-experience-composer/c-vec-code-editor/vec-code-editor.md) en Acties voor VEC die VEC toestaan om goed met SPAs te werken.

**Deelvenster Wijzigingen**

In het [!UICONTROL Modifications] deelvenster, zoals hieronder weergegeven, worden de acties vastgelegd die voor een bepaalde weergave zijn gemaakt. Alle acties voor een weergave worden gegroepeerd onder die weergave.

**Handelingen**

Wanneer u op een handeling klikt, wordt het element op de site gemarkeerd waarop deze handeling wordt toegepast. Elke VEC-actie die onder een Weergave wordt gemaakt, heeft de volgende pictogrammen, zoals hieronder wordt getoond: Informatie, Bewerken, Klonen, Verplaatsen en Verwijderen.

![Wijzigingen](/help/c-experiences/assets/modifications.png)

In de volgende tabel wordt elke actie beschreven:

| Pagina | Beschrijving |
| --- | --- |
| Informatie | Geeft de details van de handeling weer. |
| Bewerken | Hiermee kunt u de eigenschappen van de handeling rechtstreeks bewerken. |
| Klonen | Kloont de actie aan één of meerdere Weergaven die op het [!UICONTROL Modifications] paneel bestaan of aan één of meerdere Weergaven die u hebt doorzocht en aan in VEC genavigeerd. De handeling hoeft niet noodzakelijkerwijs in het [!UICONTROL Modifications] deelvenster te bestaan.<br>**Opmerking **: Nadat een kloonverrichting wordt gemaakt, moet u aan de Mening in VEC via navigeren[!UICONTROL Browse]om te zien of de gekloonde actie een geldige verrichting was. Als de actie niet op de Mening kan worden toegepast, zult u een fout zien. |
| Verplaatsen | Hiermee wordt de handeling verplaatst naar een gebeurtenis Pagina laden of een andere weergave die al bestaat in het deelvenster Wijzigingen.<br>[!UICONTROL Page Load Event] - alle handelingen die overeenkomen met de gebeurtenis load van de pagina worden toegepast op de eerste pagina die wordt geladen van uw webtoepassing.<br>**Nota **nadat een bewegingsverrichting wordt gemaakt, moet u aan de Mening in VEC via Browse navigeren om te zien of de beweging een geldige verrichting was. Als de handeling niet kan worden toegepast op de weergave, wordt een fout weergegeven |
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

1. Klik [!UICONTROL Browse]en klik vervolgens op de [!UICONTROL Products] koppeling in de koptekst.
1. Klik [!UICONTROL Load More] eenmaal om naar de tweede rij producten te gaan.
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
>De weergave UITCHECKUNNEN-EXPRESS wordt pas weergegeven in het deelvenster Wijzigen als u op het keuzerondje Uitdrukkelijke levering klikt. De reden hiervoor is dat de `triggerView()` functie wordt geactiveerd wanneer het keuzerondje Expreslevering is geselecteerd. Dit is alleen mogelijk wanneer VEC weet dat er een Weergave moet worden weergegeven in het deelvenster Wijzigen.

## Diep duiken in at.js en SPAs

**Hoe kan ik meningen voor de recentste publieksgegevens terugwinnen die door acties na de aanvankelijke paginading op mijn SPA worden gehydrateerd?**

De typische workflow van at.js 2.x is wanneer uw site wordt geladen, worden al uw weergaven en handelingen in het cachegeheugen opgeslagen, zodat volgende gebruikersacties op uw site geen serveraanroepen activeren om aanbiedingen op te halen. Als u weergaven wilt ophalen op basis van de meest recente profielgegevens die mogelijk zijn bijgewerkt, afhankelijk van de volgende gebruikershandelingen, kunt u bellen `getOffers()` en de meest recente gebruikers- of profielgegevens `applyOffers()` laten doorgeven.

Bijvoorbeeld, ben u een telecombedrijf en u hebt een KUUROORD die at.js 2.x gebruikt. Als bedrijf, wilt u de volgende doelstellingen bereiken:

* Voor een aangemelde of anonieme gebruiker, toon de recentste bedrijfbevordering, zoals het tonen van een &quot;Eerste maand vrije&quot;heldenaanbieding op `http://www.telecom.com/home`.
* Voor een aangemelde gebruiker, toon een verbeteringsbevorderingsaanbieding voor gebruikers van wie contracten omhoog komen, zoals &quot;u verkiest voor een vrije telefoon!&quot; op `http://www.telecom.com/loggedIn/home`.

Nu, noemt uw ontwikkelaars meningen en roepen `triggerView()` op de volgende manier:

* Voor `http://www.telecom.com/home` de weergavenaam is &quot;Startpagina Afgemeld&quot;
   * `triggerView(“Logged Out Home”)` wordt aangeroepen.
* Voor `http://www.telecom.com/loggedIn/home` de weergavenaam is &quot;Aangemeld thuis&quot;
   * `triggerView(“Logged In Home”)` wordt aangehaald op routeverandering.

Uw marketers voeren dan de volgende A/B-activiteiten door VEC uit:

* A/B activiteit met de &quot;Eerste Maand Vrije&quot;aanbieding voor publiek met de parameter &quot;`loggedIn= false`&quot;dat in moet worden getoond `http://www.telecom.com/home`, waar de meningsnaam Startpagina Logged uit is.
* A/B activiteit met &quot;u komt voor een vrije telefoon in aanmerking!&quot; biedt het publiek aan met de parameter &quot;`loggedIn=true`&quot; die moet worden getoond in `http://www.telecom.com/loggedIn/home`, waar de weergavenaam is geregistreerd in hoofdaanbieding.

Nu, laten wij deze gebruikersstroom overwegen:

1. Een anonieme aangemelde gebruiker landt op uw pagina.
1. Omdat u at.js 2.x gebruikt, gaat u in de parameter &quot;`loggedIn = false`&quot;op pagina-lading over om alle meningen terug te winnen aanwezig in actieve activiteiten die voor kwalificeren wanneer het publiek parameter &quot;`loggedIn = false`&quot;heeft.
1. at.js 2.x wint dan de Logged Out mening en de actie van het Huis terug om de &quot;Eerste Maand Vrije&quot;aanbieding te tonen en het op te slaan in geheim voorgeheugen.
1. Wanneer `triggerView(“Logged Out Home”)` wordt aangehaald, wordt de &quot;Eerste Maand Vrije&quot;aanbieding teruggewonnen van geheim voorgeheugen en de aanbieding zonder een servervraag getoond.
1. De gebruiker klikt nu op Aanmelden en geeft zijn of haar referenties.
1. Omdat uw website een KUUROORD is, leidt u geen volledige paginading en in plaats daarvan leidt uw gebruiker aan `http://www.telecom.com/loggedIn/home`.

Hier is het probleem. De gebruiker login en wij ontmoeten `triggerView(“Logged In Home”)` omdat wij deze code op routeverandering plaatsten. Dit vertelt at.js 2.x om de mening en de acties van geheim voorgeheugen terug te winnen, maar de enige mening die in geheim voorgeheugen bestaat is Logged Out Huis.

Dus hoe kunnen we dan onze aanmeldingsgegevens ophalen en de &quot;You are acceptable for a free phone&quot; weergeven? aanbieden? En aangezien alle verdere acties op uw plaats van een het programma geopend-in gebruikersperspectief zullen zijn, hoe kunt u ervoor zorgen alle verdere acties in gepersonaliseerde aanbiedingen voor het programma geopende gebruikers resulteren?

U kunt de nieuwe `getOffers()` en `applyOffers()` functies gebruiken die in at.js 2.x worden gesteund:

```
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

Geef de reactie van `getOffers()` aan `applyOffers()` en nu door alle meningen en acties verbonden aan &quot;het programma geopend = waar&quot;zal het at.js geheime voorgeheugen bijwerken.

Met andere woorden, 2.x in.js steunt een manier om meningen, acties, en aanbiedingen met de meest bijgewerkte publieksgegevens op een wijze op bestelling terug te winnen.

**Biedt at.js 2.x ondersteuning voor A4T voor toepassingen voor één pagina?**

Ja, in.js 2.x wordt A4T voor SPA ondersteund via de `triggerView()` functie, aangezien u Adobe Analytics en de Experience Cloud Visitor ID Service hebt geïmplementeerd. Zie het onderstaande diagram met stapsgewijze beschrijvingen.

![Target Flow](/help/c-experiences/assets/atjs-spa-flow.png)

| Stap | Beschrijving |
| --- | --- |
| 1 | `triggerView()` wordt geroepen in het KUUROORD om een mening terug te geven en acties toe te passen om visuele elementen te wijzigen verbonden aan de mening. |
| 2 | De gerichte inhoud voor de mening wordt gelezen van het geheime voorgeheugen. |
| 3 | Gerichte inhoud wordt zo snel mogelijk zichtbaar zonder flikkering van de standaardinhoud. |
| 4 | Aanvraag voor meldingen wordt verzonden naar de Target Profile Store om de bezoeker te tellen bij de activiteiten en incrementele metingen. |
| 5 | Analytics-gegevens verzonden naar gegevensverzamelingsservers. |
| 6 | Target-gegevens worden gekoppeld aan Analytics-gegevens via de SDID en worden verwerkt in de Analytics-rapportageopslag. Analytics-gegevens kunnen vervolgens zowel in Analytics als in Target worden bekeken via A4T-rapporten. |

>[!NOTE]
>Als u geen berichten naar Adobe Analytics wilt verzenden om elke keer dat een weergave wordt geactiveerd, de indruk te tellen, geeft u de `{page: false}` `triggerView()` functie door zodat het tellen van de indruk niet wordt opgeblazen wanneer een weergave meerdere keren wordt geactiveerd voor een component die voortdurend opnieuw wordt gerenderd. Bijvoorbeeld:
>
>`adobe.target.triggerView(“PRODUCTS-PAGE-2”, {page:false})`

## Ondersteunde activiteiten

| Type activiteit | Ondersteund? |
| --- | --- |
| [A/B-test](/help/c-activities/t-test-ab/test-ab.md) | Ja |
| [Aanbevelingen als een](/help/c-recommendations/recommendations-as-an-offer.md)<br>aanbod voor activiteiten op het gebied van A/B Test en Experience Targeting (XT) | Ja |
| [Automatisch toewijzen](/help/c-activities/automated-traffic-allocation/automated-traffic-allocation.md) | Ja |
| [Gericht op ervaring](/help/c-activities/t-experience-target/experience-target.md) | Ja |
| [Multivariatietest](/help/c-activities/c-multivariate-testing/multivariate-testing.md) | Nee |
| [Auto-Target](/help/c-activities/auto-target-to-optimize.md) | Nee |
| [Geautomatiseerde personalisatie](/help/c-activities/t-automated-personalization/automated-personalization.md) | Nee |
| [Aanbevelingen](/help/c-recommendations/recommendations.md) | Nee |

**Als wij bij .js 2.x installeerden en`triggerView()`op onze plaatsen uitvoerden, hoe stellen wij auto-Target A/B activiteiten in werking omdat SPA VEC auto-Target niet steunt?**

Als u Auto-Target A/B activiteiten wilt gebruiken, kunt u al uw acties bewegen die op de Gebeurtenis van het Lading van de Pagina in VEC worden uitgevoerd. Houd de muisaanwijzer boven elke actie en klik op de [!UICONTROL Move to Page Load Event] knop. Nadat dit, in de volgende stap wordt gedaan, kunt u auto-Target voor de methode van de verkeerstoewijzing selecteren.

## Ondersteunde integratie

| Integratie | Ondersteund? |
| --- | --- |
| [Analytics voor Target (A4T)](/help/c-integrating-target-with-mac/a4t/a4t.md) | Ja |
| [Experience Cloud-publiek](/help/c-integrating-target-with-mac/mmp.md) | Ja |
| [Klantkenmerken](/help/c-target/c-visitor-profile/working-with-customer-attributes.md) | Ja |
| [AEM-ervaringsfragmenten](/help/c-experiences/c-manage-content/aem-experience-fragments.md) | Ja |

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

[!UICONTROL Page Delivery] Met instellingen kunt u regels configureren om te bepalen wanneer een Target-activiteit in aanmerking moet komen en moet worden uitgevoerd voor een publiek.

Als u vanuit de [!UICONTROL Page Delivery] stap toegang wilt tot de **[!UICONTROL Experiences]** opties vanuit de workflow voor het maken van activiteiten met instructies in drie delen van de VEC, klikt u op **[!UICONTROL Configure]** (het tandwielpictogram) > **[!UICONTROL Page Delivery]**.

![Dialoogvenster Opties voor paginaaflevering](/help/c-experiences/assets/page-delivery.png)

Bijvoorbeeld, zoals gedefinieerd door de bovenstaande [!UICONTROL Page Delivery] instellingen, kwalificeert en voert een Target-activiteit uit wanneer een bezoeker rechtstreeks landt op `https://www.adobe.com` of *wanneer een bezoeker landt op een URL die deze bevat* `https://www.adobe.com/products`. Dit werkt perfect voor elke toepassing met meerdere pagina&#39;s waarin elke interactie met de pagina een pagina opnieuw laadt, waarvoor at.js de activiteiten ophaalt die in aanmerking komen voor de URL waarnaar de gebruiker navigeert.

Nochtans, omdat SPAs verschillend werkt, moeten de [!UICONTROL Page Delivery] montages op een manier worden gevormd die alle acties toestaat om op de Weergaven worden toegepast zoals die in de activiteit van het KUUROORD VEC worden bepaald.

### Voorbeeld van gebruik

Overweeg dit voorbeeld use-case:

![Deelvenster SPA VEC-wijzigingen](/help/c-experiences/assets/page-delivery-example.png)

De volgende wijzigingen zijn aangebracht:

* De achtergrondkleur is gewijzigd in de weergave Home, die zich onder de URL bevindt: [https://target.enablementadobe.com/react/demo/#/](https://target.enablementadobe.com/react/demo/#/).
* De knopkleur is gewijzigd in de weergave Producten, die zich onder de URL bevindt: [https://target.enablementadobe.com/react/demo/#/products](https://target.enablementadobe.com/react/demo/#/products).

Met het bovenstaande voorbeeld in mening, wat zou gebeuren wanneer wij montages vormen om slechts omvatten: [!UICONTROL Page Delivery] [https://target.enablementadobe.com/react/demo/#/](https://target.enablementadobe.com/react/demo/#/) in een SPA met at.js 2.*x*?

![Dialoogvenster Pagina-aflevering](/help/c-experiences/assets/spa-page-delivery.png)

In het volgende voorbeeld ziet u de aanvraag Target Flow - Page Load in at.js 2.*x*:

![Target Flow - at.js 2.0 Aanvraag voor laden van pagina&#39;s](/help/c-experiences/assets/page-load-request.png)

**Gebruikersreis #1**

* Een gebruiker navigeert rechtstreeks naar [https://target.enablementadobe.com/react/demo/#/](https://target.enablementadobe.com/react/demo/#/).
* te.js 2.*x* maakt een vraag aan Edge om te zien of moet om het even welke activiteit voor URL uitvoeren: [https://target.enablementadobe.com/react/demo/#/](https://target.enablementadobe.com/react/demo/#/).
* In stap 6 retourneert de Target Edge de acties voor de weergave Home en Products, zodat deze in de browser in de cache worden opgeslagen.

**Resultaat**: De gebruiker ziet de groene achtergrondkleur in de weergave Home. Wanneer de gebruiker dan naar [https://target.enablementadobe.com/react/demo/#/products](https://target.enablementadobe.com/react/demo/#/products)navigeert, wordt de blauwe achtergrondkleur van de knop weergegeven omdat de actie in de browser onder de weergave Producten in de cache wordt geplaatst.

Opmerking: De gebruiker die naar [https://target.enablementadobe.com/react/demo/#/products](https://target.enablementadobe.com/react/demo/#/products) navigeert, heeft geen pagina geladen.

**Gebruikersreis #2**

* Een gebruiker navigeert rechtstreeks naar [https://target.enablementadobe.com/react/demo/#/products](https://target.enablementadobe.com/react/demo/#/products).
* te.js 2.*x* maakt een vraag aan Edge om te zien of moet om het even welke activiteit voor URL uitvoeren: [https://target.enablementadobe.com/react/demo/#/products](https://target.enablementadobe.com/react/demo/#/products).
* Er zijn geen activiteiten die gekwalificeerd zijn voor [https://target.enablementadobe.com/react/demo/#/products](https://target.enablementadobe.com/react/demo/#/products).
* Omdat er geen activiteiten gekwalificeerd zijn, zijn er geen acties en meningen om voor at.js 2 worden in het voorgeheugen onder te brengen.*x* om te activeren.

**Resultaat**: Zelfs als u `triggerView()` voor de Mening van Producten hebt bepaald en een actie aan de Mening van Producten door het KUUROORD VEC gemaakt, zult u niet de verwachte actie zien aangezien u geen regel creeerde die [https://target.enablementadobe.com/react/demo/#/products](https://target.enablementadobe.com/react/demo/#/products) in de montages van de Levering van de Pagina omvatte.

### Beste praktijken

U kunt zien dat het beheren van de gebruikersreis vrij moeilijk kan zijn aangezien de gebruikers op om het even welke URL van uw KUUROORD kunnen landen en aan een andere pagina navigeren. Daarom is het best om een regel van de Levering van de Pagina te specificeren die basis URL omvat zodat het uw volledige KUUROORD omvat. Op deze manier hoeft u niet na te denken over alle verschillende reizen en paden die een gebruiker kan maken om naar een pagina te gaan waarop u een doelactiviteit voor A/B-test of -ervaring (XT) wilt weergeven.

Als u bijvoorbeeld het bovenstaande probleem wilt verhelpen, kunt u de basis-URL opgeven in de instellingen voor het leveren van pagina&#39;s als zodanig:

![Dialoogvenster Pagina-aflevering](/help/c-experiences/assets/conclusion.png)

Dit zorgt ervoor dat wanneer een bezoeker op het KUUROORD landt en naar of het Huis of de Mening van de Pagina navigeert de toegepaste acties zullen zien.

Nu, wanneer u een actie aan een Mening in het KUUROORD VEC toevoegt, zullen wij u het volgende pop-up bericht tonen om u eraan te herinneren om over de [!UICONTROL Page Delivery] regels te denken.

![Bericht over instellingen pagina](/help/c-experiences/assets/pop-up-message.png)

Dit bericht wordt weergegeven wanneer u de eerste actie toevoegt aan een Weergave voor elke nieuwe activiteit die u maakt. Dit bericht helpt ervoor te zorgen dat iedereen in uw organisatie leert hoe te om deze [!UICONTROL Page Delivery] regels correct toe te passen.

## Trainingsvideo: Het gebruiken van VEC voor SPAs in Adobe Target

>[!VIDEO](https://video.tv.adobe.com/v/26249)

Zie het [Gebruiken van de Visuele Composer van de Ervaring voor Enige Toepassing van de Pagina (SPA VEC) in Adobe Target](https://helpx.adobe.com/target/kt/using/visual-experience-composer-for-single-page-applications-feature-video-use.html) voor meer informatie.
