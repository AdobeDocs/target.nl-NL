---
keywords: spa vec;response;angular;response.js;spa visual experience composer;spa experience composer opties;single page apps;single-page-app;spa;mobile experience opties;target view
description: Leer hoe te om het KUUROORD VEC in Adobe  [!DNL Target]  te gebruiken om tests tot stand te brengen en inhoud op SPAs op een doe-het-zelf wijze zonder ononderbroken ontwikkelingsgebiedsdelen te personaliseren.
title: Hoe gebruik ik Composer van de Ervaring van de Enige Pagina App Visuele (SPA VEC)?
feature: Visual Experience Composer (VEC)
exl-id: fd3dcfaa-e5c6-45a1-8229-9c206562e5b0
source-git-commit: 2fc704a1779414a370ffd00ef5442fce36e7a5dd
workflow-type: tm+mt
source-wordcount: '3569'
ht-degree: 0%

---

# Single Page App (SPA) Visual Experience Composer

In [!DNL Adobe Target] biedt [!UICONTROL Visual Experience Composer] (VEC) marketers de mogelijkheid om zelf activiteiten te maken en ervaringen aan te passen die dynamisch kunnen worden aangeboden in traditionele toepassingen voor meerdere pagina&#39;s via Adobe Target global mbox. Nochtans, baseert dit zich op het terugwinnen van aanbiedingen op pagina-lading of verdere servervraag, die latentie, zoals aangetoond in het hieronder diagram introduceert. Deze benadering werkt niet goed met de Toepassingen van de Enige Pagina (SPAs) omdat het de gebruikerservaring en toepassingsprestaties degradeert.

![&#x200B; Traditionele levenscyclus vs. Levenscyclus van het KUUROORD &#x200B;](/help/main/c-experiences/assets/trad-vs-spa.png)

Met de recentste versie, introduceren wij nu VEC voor SPAs. VEC voor SPAs laat marketers toe om tests tot stand te brengen en inhoud op SPAs op een doe-het-zelfmanier zonder ononderbroken ontwikkelingsgebiedsdelen te personaliseren. VEC kan worden gebruikt om [&#x200B; te creëren A/B Test &#x200B;](/help/main/c-activities/t-test-ab/test-ab.md) en [&#x200B; Ervaring richtend &#x200B;](/help/main/c-activities/t-experience-target/experience-target.md) (XT) activiteiten op populaire kaders, zoals Reageren en Angular.

## Adobe [!DNL Target] Weergaven en toepassingen voor één pagina

Adobe Target VEC voor SPAs haalt voordeel uit een nieuw concept genoemd Bekijken: een logische groep visuele elementen die samen omhoog een ervaring van het KUUROORD maken. Een KUUROORD kan daarom als transitioning door meningen, in plaats van URLs worden beschouwd, die op gebruikersinteractie wordt gebaseerd. Een weergave kan doorgaans een hele site of gegroepeerde visuele elementen binnen een site vertegenwoordigen.

Als u meer wilt weten over de weergaven, navigeert u naar deze hypothetische online e-commercesite die u in Reageren hebt geïmplementeerd en verkent u enkele voorbeeldweergaven. Klik op de onderstaande koppelingen om deze site te openen in een nieuw browsertabblad.

**Verbinding: [&#x200B; Plaats van het Huis &#x200B;](https://experienceleague.adobe.com/developer/ashop-react-demo/at-js/?lang=nl-NL#/)**

![&#x200B; homesite &#x200B;](/help/main/c-experiences/assets/home.png)

Wanneer we naar de thuissite navigeren, kunnen we meteen een hoofdafbeelding zien die een paasverkoop bevordert en de nieuwste producten die op de site worden verkocht. In dit geval, kan een Mening als volledige homesite worden gedefinieerd. Dit is handig om op te merken, aangezien we hier meer over zullen doen in de sectie Adobe Target-weergaven implementeren hieronder.

**Verbinding: [&#x200B; Plaats van het Product &#x200B;](https://experienceleague.adobe.com/developer/ashop-react-demo/at-js/?lang=nl-NL#/products)**

![&#x200B; productplaats &#x200B;](/help/main/c-experiences/assets/product-site.png)

Aangezien wij meer in de producten geïnteresseerd raken, besluiten wij om de verbinding van Producten te klikken. Net als op de thuissite kan de hele productsite worden gedefinieerd als een weergave. Deze weergave kan net als de padnaam in `https://experienceleague.adobe.com/developer/ashop-react-demo/at-js/?lang=nl-NL#/products` &#39;producten&#39; worden genoemd.

![&#x200B; productplaats 2 &#x200B;](/help/main/c-experiences/assets/product-site-2.png)

In het begin van deze sectie definieerden we Weergaven als de gehele site of zelfs als een groep visuele elementen op de site. Zoals hierboven wordt getoond, kunnen de vier producten die op de plaats worden getoond ook als Mening worden gegroepeerd en worden beschouwd. Als we deze weergave een naam willen geven, kunnen we deze &quot;producten&quot; noemen.

![&#x200B; productplaats 3 &#x200B;](/help/main/c-experiences/assets/product-site-3.png)

We besluiten op de knop Meer laden te klikken om meer producten op de site te verkennen. De URL van de website verandert in dit geval niet. Maar een weergave hier kan alleen de tweede rij producten weergeven die hierboven wordt weergegeven. De weergavenaam kan &#39;PRODUCTS-PAGE-2&#39; worden genoemd.

**Verbinding: [&#x200B; Controle &#x200B;](https://experienceleague.adobe.com/developer/ashop-react-demo/at-js/?lang=nl-NL#/checkout)**

![&#x200B; controle-uit pagina &#x200B;](/help/main/c-experiences/assets/checkout.png)

Omdat we bepaalde producten op de site leuk vonden, besloten we een paar te kopen. Nu krijgen we op de uitchecksite enkele opties om normale levering of expreslevering te kiezen. Omdat een weergave elke groep visuele elementen op een site kan zijn, kunnen we deze &quot;Voorkeuren voor levering weergeven&quot; noemen.

Bovendien kan het concept van de standpunten veel verder worden uitgebreid. Als marketers de inhoud op de site willen aanpassen, afhankelijk van de geselecteerde leveringsvoorkeur, kan een Weergave worden gemaakt voor elke leveringsvoorkeur. In dit geval, wanneer wij Normale Levering selecteren, kan de Mening &quot;Normale Levering&quot;worden genoemd. Als Express Delivery is geselecteerd, kan de weergave de naam &quot;Express Delivery&quot; hebben.

Marktdeelnemers kunnen nu een A/B-test uitvoeren om te zien of het wijzigen van de kleur van blauw in rood wanneer Express Delivery is geselecteerd, conversies kan stimuleren in plaats van de knopkleur blauw te houden voor beide leveringsopties.

## Adobe [!DNL Target] -weergaven implementeren

Nu wij hebben behandeld wat de Weergaven van Adobe Target zijn, kunnen wij hefboomwerking dit concept in Doel om marktleiders in staat te stellen om tests A/B en XT op SPAs via VEC in werking te stellen. Hiervoor is een eenmalige ontwikkelaarsinstelling vereist. Laten we de stappen doorlopen om dit in te stellen.

1. Installeer om 2.js.

   Eerst moeten we installeren op .js 2.x. Deze versie van at.js werd ontwikkeld met SPAs in mening. Eerdere versies van at.js en bieden geen ondersteuning voor Adobe Target Views en VEC for SPA.

   ![&#x200B; de dialoogdoos van de Details van de Implementatie &#x200B;](/help/main/c-experiences/assets/imp-200.png)

   Download het bestand at.js 2.x via de gebruikersinterface van Adobe Target in [!UICONTROL Administration > Implementation] . at.js 2.x kan ook via markeringen in [&#x200B; Adobe Experience Platform &#x200B;](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/deploy-at-js/implement-target-using-adobe-launch.html?lang=nl-NL){target=_blank} worden opgesteld. De Adobe Target-extensies zijn momenteel echter niet up-to-date en worden wel ondersteund.

1. Implementeer de nieuwste functie van at.js 2.x: [&#x200B; triggerView () &#x200B;](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/functions-overview/adobe-target-triggerview-atjs-2.html?lang=nl-NL){target=_blank} op uw plaatsen.

   Na het bepalen van de Weergaven van uw SPA waar u een A/B of XT test wilt in werking stellen, voer de functie van at.js 2.x `triggerView()` met de Bekijken uit die binnen als parameter worden overgegaan. Dit staat marketers toe om VEC te gebruiken om de tests A/B en XT voor die Gedefinieerde Kijken te ontwerpen en in werking te stellen. Als de `triggerView()` functie niet voor die Kijken wordt bepaald, zal VEC niet de Kijken ontdekken en zo kunnen de verkopers VEC niet gebruiken om A/B en XT tests te ontwerpen en in werking te stellen.

   **`adobe.target.triggerView(viewName, options)`**

   | Parameter | Type | Vereist? | Validatie | Beschrijving |
   | --- | --- | --- | --- | --- |
   | viewName | String | Ja | &#x200B;1. Geen navolgende spaties.<br> 2. Kan niet leeg zijn.<br> 3. De weergavenaam moet uniek zijn voor alle pagina&#39;s.<br> 4. **Waarschuwing**: De naam van de mening zou niet met &quot;`/`&quot;moeten beginnen of eindigen. De reden hiervoor is dat de klant doorgaans de weergavenaam uit het URL-pad haalt. Voor ons zijn &#39;home&#39; en &#39;`/home`&#39; anders.<br> 5. **Waarschuwing**: De zelfde mening zou niet opeenvolgend veelvoudige tijden met de `{page: true}` optie moeten worden teweeggebracht. | Geef een willekeurige naam door als een type tekenreeks dat u de weergave wilt vertegenwoordigen. Deze weergavenaam wordt in het deelvenster [!UICONTROL Modifications] van de VEC weergegeven, zodat marketers handelingen kunnen maken en hun A/B- en XT-activiteiten kunnen uitvoeren. |
   | opties | Object | Nee |  |  |
   | opties > pagina | Boolean | Nee |  | **WAAR**: De standaardwaarde van pagina is waar. Wanneer `page=true` , zullen de berichten naar de servers van Edge voor het verhogen van immentatietelling worden verzonden.<br>**VALS**: Wanneer `page=false`, zullen de berichten niet voor het verhogen van beeldtelling worden verzonden. Dit zou moeten worden gebruikt wanneer u een component op een pagina met een aanbieding slechts opnieuw wilt teruggeven. |

   Nu ga door één of ander voorbeeld gebruiksgevallen op hoe te om de `triggerView()` functie in React voor onze hypothetische e-commerce SPA aan te halen:

   **Verbinding: [&#x200B; Plaats van het Huis &#x200B;](https://experienceleague.adobe.com/developer/ashop-react-demo/at-js/?lang=nl-NL#/)**

   ![&#x200B; huis-reactie-1 &#x200B;](/help/main/c-experiences/assets/react1.png)

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

   **Verbinding: [&#x200B; Plaats van Producten &#x200B;](https://experienceleague.adobe.com/developer/ashop-react-demo/at-js/?lang=nl-NL#/products)**

   Laten we nu eens kijken naar een voorbeeld dat wat gecompliceerder is. Laten we bijvoorbeeld als marketers de tweede rij van de producten personaliseren door de kleur van het prijslabel te wijzigen in rood nadat een gebruiker op de knop Meer laden heeft geklikt.

   ![&#x200B; reacties producten &#x200B;](/help/main/c-experiences/assets/react4.png)

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
       var page = this.state.page + 1; // assuming page number is derived from component's state
       this.setState({page: page});
       targetView('PRODUCTS-PAGE-' + page);
     }
   }
   ```

   **Verbinding: [&#x200B; Controle &#x200B;](https://experienceleague.adobe.com/developer/ashop-react-demo/at-js/?lang=nl-NL#/checkout)**

   ![&#x200B; reactie controle &#x200B;](/help/main/c-experiences/assets/react6.png)

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

   Wanneer `adobe.target.triggerView()` op uw SPA met de namen van de Mening wordt uitgevoerd die als parameters worden overgegaan, zal VEC deze meningen kunnen ontdekken en gebruikers toestaan om acties en wijzigingen voor hun A/B of XT activiteiten tot stand te brengen.

   >[!NOTE]
   >
   >VEC voor SPAs is werkelijk het zelfde VEC dat u op regelmatige Web-pagina&#39;s gebruikt, maar sommige extra mogelijkheden zijn beschikbaar wanneer u één enkele paginaapp opent met `triggerView()` uitgevoerd.

Er zijn twee belangrijke verbeteringen aan het [&#x200B; paneel van Veranderingen &#x200B;](/help/main/c-experiences/c-visual-experience-composer/c-vec-code-editor/vec-code-editor.md) en Acties voor VEC die VEC toestaan om goed met SPAs te werken.

**het Comité van Wijzigingen**

In het deelvenster [!UICONTROL Modifications] worden, zoals hieronder wordt weergegeven, de acties vastgelegd die voor een bepaalde weergave zijn gemaakt. Alle acties voor een weergave worden gegroepeerd onder die weergave.

**Acties**

Wanneer u op een handeling klikt, wordt het element op de site gemarkeerd waarop deze handeling wordt toegepast. Elke VEC-actie die onder een Weergave wordt gemaakt, heeft de volgende pictogrammen, zoals hieronder wordt weergegeven: Informatie, Bewerken, Klonen, Verplaatsen en Verwijderen.

![&#x200B; Wijzigingen &#x200B;](/help/main/c-experiences/assets/modifications.png)

In de volgende tabel wordt elke actie beschreven:

| Pagina | Beschrijving |
| --- | --- |
| Informatie | Geeft de details van de handeling weer. |
| Bewerken | Hiermee kunt u de eigenschappen van de handeling rechtstreeks bewerken. |
| Klonen | Kloont de actie aan één of meerdere Weergaven die op het [!UICONTROL Modifications] paneel of aan één of meerdere Weergaven bestaan die u hebt doorzocht en aan in VEC genavigeerd. De handeling hoeft niet noodzakelijkerwijs in het deelvenster [!UICONTROL Modifications] te staan.<br>**Nota**: Nadat een kloonverrichting wordt gemaakt, moet u aan de Mening in VEC via [!UICONTROL Browse] navigeren om te zien of de gekloonde actie een geldige verrichting was. Als de actie niet op de Mening kan worden toegepast, zult u een fout zien. |
| Verplaatsen | Hiermee wordt de handeling verplaatst naar een gebeurtenis Pagina laden of een andere weergave die al bestaat in het deelvenster Wijzigingen.<br>[!UICONTROL Page Load Event] - alle handelingen die overeenkomen met de gebeurtenis load van de pagina worden toegepast op het eerste laden van de pagina van de webtoepassing.<br>**Nota** nadat een bewegingsverrichting wordt gemaakt, moet u aan de Mening in VEC via doorbladeren navigeren om te zien of de beweging een geldige verrichting was. Als de handeling niet kan worden toegepast op de weergave, wordt een fout weergegeven |
| Verwijderen | Hiermee verwijdert u de handeling. |

>[!NOTE]
>
>U kunt vele acties uitvoeren alvorens de pagina in VEC laadt, of zelfs als de pagina niet volledig kan laden. Handelingen die niet kunnen worden bewerkt voordat de site wordt geladen, worden uitgeschakeld in de gebruikersinterface.

**Voorbeeld 1**

Laten we het bovenstaande voorbeeld gebruiken waarin we een weergave Home hebben gemaakt. Ons doel is tweeledig voor deze visie:

1. Wijzig de knoppen Toevoegen aan winkelwagentje en Soortgelijk in een lichtblauwe kleur. Dit moet in de modus &quot;Pagina laden&quot; staan, omdat de componenten van de koptekst veranderen.
1. Wijzig het label &quot;Nieuwste producten voor 2019&quot; in &quot;Hottest Products for 2019&quot; met de tekstkleur gewijzigd in paars.

Om deze doelstellingen uit te voeren, in VEC, klik [!UICONTROL Compose] en pas die veranderingen op de mening van het Huis toe.

![&#x200B; Voorbeeld 1 &#x200B;](/help/main/c-experiences/assets/example1.png)

**Voorbeeld 2**

Laten we het voorbeeld hierboven gebruiken waarin we een PRODUCTS-PAGE-2-weergave hebben gemaakt. Ons doel is om het label Prijs te wijzigen in Verkoopprijs met de labelkleur rood.

1. Klik op [!UICONTROL Browse] en klik vervolgens op de koppeling [!UICONTROL Products] in de koptekst.
1. Klik één keer op [!UICONTROL Load More] om naar de tweede rij producten te gaan.
1. Klik op [!UICONTROL Compose].
1. Pas handelingen toe om het tekstlabel te wijzigen in Verkoopprijs en de kleur in rood.

![&#x200B; Voorbeeld 2 &#x200B;](/help/main/c-experiences/assets/example2.png)

**Voorbeeld 3**

Tot slot kunnen, zoals eerder vermeld, weergaven in korreligheid worden gedefinieerd. Weergaven kunnen een status of zelfs een optie via een keuzerondje zijn. Eerder hebben we weergaven gemaakt als CHECKOUT-EXPRESS en CHECKOUT-NORMAL. Ons doel is de knopkleur te wijzigen in rood voor de CHECKOUT-EXPRESS-weergave.

1. Klik op [!UICONTROL Browse].
1. Voeg een paar producten toe aan het winkelwagentje.
1. Klik op het winkelwagentje in de rechterbovenhoek.
1. Klik op Uitchecken van uw bestelling.
1. Klik op het keuzerondje Expreslevering.
1. Klik op [!UICONTROL Compose].
1. Klik op de knop Betalen om de knop Volgorde voltooien te lezen en de kleur rood te wijzigen.

![&#x200B; Voorbeeld 3 &#x200B;](/help/main/c-experiences/assets/example3.png)

>[!NOTE]
>
>De weergave UITCHECKUNNEN-EXPRESS wordt pas weergegeven in het deelvenster Wijzigen als u op het keuzerondje Uitdrukkelijke levering klikt. De reden hiervoor is dat de functie `triggerView()` wordt geactiveerd wanneer het keuzerondje Expreslevering is geselecteerd. Dit is alleen mogelijk wanneer VEC weet dat er een Weergave moet worden weergegeven in het deelvenster Wijzigen.

## Diep duiken in at.js en SPAs

**Hoe kan ik meningen voor de recentste publieksgegevens terugwinnen die door acties na de aanvankelijke paginalading op mijn KUUROORD worden gehydrateerd?**

De typische workflow van at.js 2.x is wanneer uw site wordt geladen, worden al uw weergaven en handelingen in het cachegeheugen opgeslagen, zodat volgende gebruikersacties op uw site geen serveraanroepen activeren om aanbiedingen op te halen. Als u de weergaven wilt ophalen op basis van de meest recente profielgegevens die mogelijk zijn bijgewerkt, afhankelijk van volgende gebruikershandelingen, kunt u `getOffers()` en `applyOffers()` aanroepen met de meest recente gebruikers- of profielgegevens die zijn doorgegeven.

Bijvoorbeeld, ben u een telecombedrijf en u hebt een KUUROORD die at.js 2.x gebruikt. Als bedrijf, wilt u de volgende doelstellingen bereiken:

* Voor een aangemelde of anonieme gebruiker geeft u de meest recente bevordering van het bedrijf weer, zoals een &quot;First month free&quot; hoofdaanbieding op `http://www.telecom.com/home` .
* Voor een aangemelde gebruiker, toon een verbeteringsbevorderingsaanbieding voor gebruikers van wie contracten omhoog komen, zoals &quot;u verkiest voor een vrije telefoon!&quot; op `http://www.telecom.com/loggedIn/home` .

De ontwikkelaars noemen nu weergaven en roepen `triggerView()` op de volgende manier aan:

* Voor `http://www.telecom.com/home` is de weergavenaam &quot;Startpagina afgemeld&quot;
   * `triggerView("Logged Out Home")` wordt aangeroepen.
* Voor `http://www.telecom.com/loggedIn/home` is de weergavenaam &quot;Aangemeld bij homepage&quot;
   * `triggerView("Logged In Home")` wordt aangeroepen bij routewijziging.

Uw marketers voeren dan de volgende A/B-activiteiten door VEC uit:

* A/B activiteit met de &quot;Eerste Maand Vrije&quot;aanbieding voor publiek met de parameter &quot;`loggedIn= false`&quot;dat in `http://www.telecom.com/home` moet worden getoond, waar de meningsnaam Startpagina Logged uit is.
* A/B activiteit met &quot;u komt voor een vrije telefoon in aanmerking!&quot; biedt aan publiek met de parameter &quot;`loggedIn=true`&quot; aan om in `http://www.telecom.com/loggedIn/home` te worden getoond, waar de meningsnaam in Heropaanbod wordt geregistreerd.

Nu, laten wij deze gebruikersstroom overwegen:

1. Een anonieme aangemelde gebruiker landt op uw pagina.
1. Omdat u at.js 2.x gebruikt, gaat u in de parameter &quot;`loggedIn = false`&quot;op pagina-lading over om alle meningen terug te winnen huidig in actieve activiteiten die voor kwalificeren wanneer het publiek parameter &quot; `loggedIn = false`&quot;heeft.
1. at.js 2.x wint dan de Logged Out mening en de actie van het Huis terug om de &quot;Eerste Maand Vrije&quot;aanbieding te tonen en het op te slaan in geheim voorgeheugen.
1. Wanneer `triggerView("Logged Out Home")` wordt aangehaald, wordt de &quot;Eerste Maand Vrije&quot;aanbieding teruggewonnen van geheim voorgeheugen en de aanbieding wordt getoond zonder een servervraag.
1. De gebruiker klikt nu op Aanmelden en geeft zijn of haar referenties.
1. Omdat uw website een SPA is, laadt u geen volledige pagina en leidt u in plaats daarvan uw gebruiker naar `http://www.telecom.com/loggedIn/home`.

Hier is het probleem. De gebruiker meldt zich aan en wij ontmoeten `triggerView("Logged In Home")` omdat wij deze code op routeverandering plaatsten. Dit vertelt at.js 2.x om de mening en de acties van geheim voorgeheugen terug te winnen, maar de enige mening die in geheim voorgeheugen bestaat is Logged Out Huis.

Dus hoe kunnen we dan onze aanmeldingsgegevens ophalen en de &quot;You are acceptable for a free phone&quot; weergeven? aanbieden? En aangezien alle verdere acties op uw plaats van een het programma geopend-in gebruikersperspectief zullen zijn, hoe kunt u ervoor zorgen alle verdere acties in gepersonaliseerde aanbiedingen voor het programma geopende gebruikers resulteren?

U kunt de nieuwe `getOffers()` - en `applyOffers()` -functies gebruiken die worden ondersteund in at.js 2.x:

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

Geef het antwoord van `getOffers()` aan `applyOffers()` door en nu werken alle weergaven en acties die zijn gekoppeld aan &quot;logIn = true&quot; de cache at.js bij.

Met andere woorden, 2.x in.js steunt een manier om meningen, acties, en aanbiedingen met de meest bijgewerkte publieksgegevens op een wijze op bestelling terug te winnen.

**steunt at.js 2.x A4T voor Enige Toepassingen van de Pagina?**

Ja, in.js 2.x wordt A4T voor SPA ondersteund via de functie `triggerView()` , aangezien u Adobe Analytics en de Experience Cloud Visitor ID Service hebt geïmplementeerd. Zie het onderstaande diagram met stapsgewijze beschrijvingen.

![&#x200B; Stroom van het Doel &#x200B;](/help/main/c-experiences/assets/atjs-spa-flow.png)

| Stap | Beschrijving |
| --- | --- |
| 1 | `triggerView()` wordt geroepen in het KUUROORD om een mening terug te geven en acties toe te passen om visuele elementen verbonden aan de mening te wijzigen. |
| 2 | De gerichte inhoud voor de mening wordt gelezen van het geheime voorgeheugen. |
| 3 | Gerichte inhoud wordt zo snel mogelijk zichtbaar zonder flikkering van de standaardinhoud. |
| 4 | Het verzoek om een melding wordt verzonden naar de Target Profile Store om de bezoeker te tellen in de activiteit en de verhogingsmetriek. |
| 5 | Analytische gegevens die naar de Servers van de Inzameling van Gegevens worden verzonden. |
| 6 | De doelgegevens worden via de SDID aangepast aan de analysegegevens en worden verwerkt in de analytische rapportageopslag. De analysegegevens kunnen dan in zowel Analytics als Doel via A4T- rapporten worden bekeken. |

>[!NOTE]
>Als u geen berichten naar Adobe Analytics wilt verzenden voor het tellen van de indruk telkens wanneer een mening wordt teweeggebracht, ga `{page: false}` aan de `triggerView()` functie in zodat de indruk tellend niet wordt opgeblazen wanneer een mening veelvoudige tijden voor een component wordt teweeggebracht die constant opnieuw teruggeeft. Bijvoorbeeld:
>
>`adobe.target.triggerView("PRODUCTS-PAGE-2", {page:false})`

## Ondersteunde activiteiten

| Type activiteit | Ondersteund? |
| --- | --- |
| [&#x200B; Test A/B &#x200B;](/help/main/c-activities/t-test-ab/test-ab.md) | Ja |
| [&#x200B; Aanbevelingen als aanbieding &#x200B;](/help/main/c-recommendations/recommendations-as-an-offer.md)<br> in de Test van A/B en Ervaring die (XT) activiteiten richten | Ja |
| [&#x200B; automatisch-toewijst &#x200B;](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md) | Ja |
| [&#x200B; Ervaring richtend &#x200B;](/help/main/c-activities/t-experience-target/experience-target.md) | Ja |
| [&#x200B; Multivariate Test &#x200B;](/help/main/c-activities/c-multivariate-testing/multivariate-testing.md) | Nee |
| [&#x200B; auto-Doel &#x200B;](/help/main/c-activities/auto-target/auto-target-to-optimize.md) | Nee |
| [&#x200B; Automated Personalization &#x200B;](/help/main/c-activities/t-automated-personalization/automated-personalization.md) | Nee |
| [&#x200B; Aanbevelingen &#x200B;](/help/main/c-recommendations/recommendations.md) | Nee |

**als wij bij.js 2.x installeerden en `triggerView()` op onze plaatsen ten uitvoer legden, hoe wij auto-Doel A/B activiteiten in werking stellen omdat het KUUROORD VEC auto-Doel niet steunt?**

Als u Auto-Doel A/B activiteiten wilt gebruiken, kunt u al uw acties bewegen die op de Gebeurtenis van de Lading van de Pagina in VEC moeten worden uitgevoerd. Houd de cursor boven elke handeling en klik op de knop [!UICONTROL Move to Page Load Event] . Nadat dit, in de volgende stap wordt gedaan, kunt u auto-Doel voor de methode van de verkeerstoewijzing selecteren.

## Ondersteunde integratie

| Integratie | Ondersteund? |
| --- | --- |
| [&#x200B; Analytics voor Doel (A4T) &#x200B;](/help/main/c-integrating-target-with-mac/a4t/a4t.md) | Ja |
| [&#x200B; publiek van Experience Cloud &#x200B;](/help/main/c-integrating-target-with-mac/mmp.md) | Ja |
| [&#x200B; Attributen van de Klant &#x200B;](https://experienceleague.adobe.com/docs/target-dev/developer/implementation/methods/customer-attributes.html?lang=nl-NL){target=_blank} | Ja |
| [&#x200B; de Fragmenten van de Ervaring van AEM &#x200B;](/help/main/c-experiences/c-manage-content/aem-experience-fragments.md) | Ja |

## Ondersteunde functies {#supported-features}

| Functie | Ondersteund? |
| --- | --- |
| [&#x200B; Werkruimten en Eigenschappen &#x200B;](/help/main/administrating-target/c-user-management/property-channel/property-channel.md) | Ja |
| [&#x200B; Verbindingen QA &#x200B;](/help/main/c-activities/c-activity-qa/activity-qa.md) | Ja |
| [&#x200B; Op vorm-gebaseerde Composer van de Ervaring &#x200B;](/help/main/c-experiences/form-experience-composer.md) | Nee |
| [&#x200B; de Code van de Douane &#x200B;](/help/main/c-experiences/c-visual-experience-composer/c-vec-code-editor/vec-code-editor.md) | Ja |
| [&#x200B; opties VEC &#x200B;](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md) | Alles |
| [&#x200B; klik-volgt &#x200B;](/help/main/c-activities/r-success-metrics/click-tracking.md) | Ja |
| [&#x200B; multi-activity levering &#x200B;](/help/main/c-experiences/c-visual-experience-composer/multipage-activity.md) | Ja |

## De montages van de Levering van de pagina voor SPA VEC {#page-delivery-settings}

Met instellingen van [!UICONTROL Page Delivery] kunt u regels configureren om te bepalen wanneer een doelactiviteit moet worden gekwalificeerd en uitgevoerd voor een publiek.

Als u vanuit de [!UICONTROL Page Delivery] stap toegang wilt tot de **[!UICONTROL Experiences]** -opties vanuit de workflow voor het maken van activiteiten met instructies in drie delen van de VEC, klikt u op **[!UICONTROL Configure]** (het tandwielpictogram) > **[!UICONTROL Page Delivery]** .

![&#x200B; de optiesdialoogdoos van de Levering van de Pagina &#x200B;](/help/main/c-experiences/assets/page-delivery.png)

Bijvoorbeeld, zoals die door de [!UICONTROL Page Delivery] hierboven getoonde montages wordt bepaald, kwalificeert een activiteit van het Doel en voert uit wanneer een bezoeker direct op `https://www.adobe.com` *of* wanneer een bezoeker op om het even welke URL landt die `https://www.adobe.com/products` bevat. Dit werkt perfect voor elke toepassing met meerdere pagina&#39;s waarin elke interactie met de pagina een pagina opnieuw laadt, waarvoor at.js de activiteiten ophaalt die in aanmerking komen voor de URL waarnaar de gebruiker navigeert.

Nochtans, omdat SPAs verschillend werkt, moeten de [!UICONTROL Page Delivery] montages op een manier worden gevormd die alle acties toestaat om op de Weergaven worden toegepast zoals die in de activiteit van het KUUROORD VEC worden bepaald.

### Voorbeeld van gebruik

Overweeg dit voorbeeld use-case:

![&#x200B; het paneel van Wijzigingen van SPA VEC &#x200B;](/help/main/c-experiences/assets/page-delivery-example.png)

De volgende wijzigingen zijn aangebracht:

* Veranderde achtergrondkleur in de mening van het Huis, die onder URL wordt gevestigd: [&#x200B; https://experienceleague.adobe.com/developer/ashop-react-demo/at-js/?lang=nl-NL#/ &#x200B;](https://experienceleague.adobe.com/developer/ashop-react-demo/at-js/?lang=nl-NL#/).
* Veranderde knoopkleur in de mening van Producten, die onder URL wordt gevestigd: [&#x200B; https://experienceleague.adobe.com/developer/ashop-react-demo/at-js/?lang=nl-NL#/products &#x200B;](https://experienceleague.adobe.com/developer/ashop-react-demo/at-js/?lang=nl-NL#/products).

Met het voorbeeld hierboven in mening, wat zou gebeuren wanneer wij [!UICONTROL Page Delivery] montages vormen om slechts te omvatten: [&#x200B; https://experienceleague.adobe.com/developer/ashop-react-demo/at-js/?lang=nl-NL#/ &#x200B;](https://experienceleague.adobe.com/developer/ashop-react-demo/at-js/?lang=nl-NL#/) in een KUUROORD met at.js 2.*x*?

![&#x200B; de dialoogdoos van de Levering van de Pagina &#x200B;](/help/main/c-experiences/assets/spa-page-delivery.png)

In de volgende afbeelding ziet u de aanvraag voor het laden van de doelstroom - pagina in at.js 2.*x*:

![&#x200B; Stroom van het Doel - bij.js 2.0 het Verzoek van de Lading van de Pagina &#x200B;](/help/main/c-experiences/assets/page-load-request.png)

**Reis van de Gebruiker #1**

* Een gebruiker navigeert direct aan [&#x200B; https://experienceleague.adobe.com/developer/ashop-react-demo/at-js/?lang=nl-NL#/ &#x200B;](https://experienceleague.adobe.com/developer/ashop-react-demo/at-js/?lang=nl-NL#/).
* te.js 2.*x* maakt een vraag aan Edge om te zien of moet om het even welke activiteit voor URL uitvoeren: [&#x200B; https://experienceleague.adobe.com/developer/ashop-react-demo/at-js/?lang=nl-NL#/ &#x200B;](https://experienceleague.adobe.com/developer/ashop-react-demo/at-js/?lang=nl-NL#/).
* In stap 6, keert het Doel Edge de acties voor de mening van het Huis en van Producten terug zodat zij binnen browser in het voorgeheugen ondergebracht zijn.

**Resultaat**: De gebruiker ziet de groene achtergrondkleur in de mening van het Huis. Wanneer de gebruiker dan aan [&#x200B; https://experienceleague.adobe.com/developer/ashop-react-demo/at-js/?lang=nl-NL#/products &#x200B;](https://experienceleague.adobe.com/developer/ashop-react-demo/at-js/?lang=nl-NL#/products) navigeert, wordt de blauwe achtergrondkleur van de knoop gezien omdat de actie in browser onder de mening van Producten in het voorgeheugen onder wordt gebracht.

Nota: De gebruiker die aan [&#x200B; https://experienceleague.adobe.com/developer/ashop-react-demo/at-js/?lang=nl-NL#/products &#x200B;](https://experienceleague.adobe.com/developer/ashop-react-demo/at-js/?lang=nl-NL#/products) navigeert bracht geen paginading teweeg.

**Reis van de Gebruiker #2**

* Een gebruiker navigeert direct aan [&#x200B; https://experienceleague.adobe.com/developer/ashop-react-demo/at-js/?lang=nl-NL#/products &#x200B;](https://experienceleague.adobe.com/developer/ashop-react-demo/at-js/?lang=nl-NL#/products).
* te.js 2.*x* maakt een vraag aan Edge om te zien of moet om het even welke activiteit voor URL uitvoeren: [&#x200B; https://experienceleague.adobe.com/developer/ashop-react-demo/at-js/?lang=nl-NL#/products &#x200B;](https://experienceleague.adobe.com/developer/ashop-react-demo/at-js/?lang=nl-NL#/products).
* Er zijn geen activiteiten die voor [&#x200B; https://experienceleague.adobe.com/developer/ashop-react-demo/at-js/?lang=nl-NL#/products &#x200B;](https://experienceleague.adobe.com/developer/ashop-react-demo/at-js/?lang=nl-NL#/products) worden gekwalificeerd.
* Omdat er geen activiteiten gekwalificeerd zijn, zijn er geen acties en meningen om voor at.js 2 worden in het voorgeheugen onder te brengen.*x* aan trekker van.

**Resultaat**: Zelfs als u `triggerView()` voor de Mening van Producten hebt bepaald en een actie aan de Mening van Producten door het KUUROORD VEC gemaakt, zult u niet de verwachte actie zien aangezien u geen regel creeerde die [&#x200B; https://experienceleague.adobe.com/developer/ashop-react-demo/at-js/?lang=nl-NL#/products &#x200B;](https://experienceleague.adobe.com/developer/ashop-react-demo/at-js/?lang=nl-NL#/products) in de montages van de Levering van de Pagina omvatte.

### Beste praktijken

U kunt zien dat het beheren van de gebruikersreis vrij moeilijk kan zijn aangezien de gebruikers op om het even welke URL van uw KUUROORD kunnen landen en aan een andere pagina navigeren. Daarom is het best om een regel van de Levering van de Pagina te specificeren die basis URL omvat zodat het uw volledige KUUROORD omvat. Op deze manier, te hoeven u niet om over alle verschillende reizen en wegen te denken die een gebruiker zou kunnen nemen om aan een pagina te krijgen waarop u een A/B Test of een Gerichte (XT) activiteit van de Ervaring wilt tonen.

Als u bijvoorbeeld het bovenstaande probleem wilt verhelpen, kunnen we de basis-URL opgeven in de instellingen voor het leveren van pagina&#39;s als zodanig:

![&#x200B; de dialoogdoos van de Levering van de Pagina &#x200B;](/help/main/c-experiences/assets/conclusion.png)

Dit zorgt ervoor dat wanneer een bezoeker op het KUUROORD landt en naar of het Huis of de Mening van de Pagina navigeert de toegepaste acties zullen zien.

Nu, wanneer u een actie aan een Mening in het KUUROORD VEC toevoegt, zullen wij u het volgende pop-up bericht tonen om u eraan te herinneren om over de [!UICONTROL Page Delivery] regels te denken.

![&#x200B; het bericht van de Montages van de Levering van de Pagina &#x200B;](/help/main/c-experiences/assets/pop-up-message.png)

Dit bericht wordt weergegeven wanneer u de eerste actie toevoegt aan een Weergave voor elke nieuwe activiteit die u maakt. Dit bericht helpt ervoor te zorgen dat iedereen in uw organisatie leert hoe te om deze [!UICONTROL Page Delivery] regels correct toe te passen.

## Trainingsvideo: VEC gebruiken voor SPA&#39;s in Adobe Target

>[!VIDEO](https://video.tv.adobe.com/v/26249)

Zie [&#x200B; Gebruikend de Visuele Composer van de Ervaring voor Enige Toepassing van de Pagina (SPA VEC) in Adobe Target &#x200B;](https://helpx.adobe.com/target/kt/using/visual-experience-composer-for-single-page-applications-feature-video-use.html) voor meer informatie.
