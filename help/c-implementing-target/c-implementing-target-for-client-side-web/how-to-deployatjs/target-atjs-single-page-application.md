---
keywords: single page application implementation;implement single page application;spa;at.js 2.x;at.js;single page application;single page app;spa;SPAs
description: Informatie die Adobe Target in.js 2.x moet gebruiken voor de implementatie van Single Page Applications (SPAs).
title: Toepassing van één pagina in Adobe Target
topic: standard
uuid: 5887ec53-e5b1-40f9-b469-33685f5c6cd6
translation-type: tm+mt
source-git-commit: 7a2e5ae6a02c63f06fc49f5d040b74656f0f3262

---


# Toepassing van één pagina{#single-page-application-implementation}

Traditionele websites werkten aan navigatiemodellen &quot;van pagina tot pagina&quot;, ook wel bekend als Toepassingen van meerdere pagina&#39;s, waarbij websiteontwerpen nauw gekoppeld waren aan URL&#39;s en overgangen van de ene webpagina naar de andere een pagina moesten laden. Moderne webtoepassingen, zoals Single Page Applications (SPAs), maken in plaats daarvan gebruik van een model dat snel gebruik van de rendering van de gebruikersinterface van de browser voorstelt. Deze is vaak onafhankelijk van het opnieuw laden van de pagina. Deze ervaringen worden vaak veroorzaakt door klanteninteractie, zoals scrolls, kliks, en curseurbewegingen. Naarmate de paradigma&#39;s van het moderne web zijn geëvolueerd, werkt de relevantie van traditionele generieke gebeurtenissen, zoals page-load, om personalisatie en experimenten te implementeren, niet meer.

![Traditionele levenscyclus van pagina&#39;s versus levenscyclus van SPA](/help/c-experiences/assets/trad-vs-spa.png)

at.js 2.x verstrekt rijke eigenschappen die uw zaken uitrusten om verpersoonlijking op volgende-generatie, cliënt-zijtechnologieën uit te voeren. Deze versie is gericht op het verbeteren van at.js om harmonieuze interactie met SPAs te hebben.

Hier volgen enkele voordelen van het gebruik van at.js 2.x die niet beschikbaar zijn in eerdere versies:

* De capaciteit om alle aanbiedingen op pagina-lading in het voorgeheugen onder te brengen om veelvoudige servervraag aan één enkele servervraag te verminderen.
* Verbeter de ervaringen van uw eindgebruikers op uw site aanzienlijk, omdat aanbiedingen direct via de cache worden weergegeven zonder vertraging die door traditionele serveraanroepen wordt geïntroduceerd.
* Een eenvoudige één-lijn van code en éénmalige ontwikkelaarsopstelling om uw marketers toe te laten om A/B en Ervaring te creëren die (XT) activiteiten richten via VEC op uw SPA.

## Adobe Target Views and Single Page Applications

Het doel VEC van Adobe voor SPAs haalt voordeel uit een nieuw concept genoemd Bekijken: een logische groep van visuele elementen die samen omhoog een ervaring van het KUUROORD maken. Een KUUROORD kan daarom als transitioning door meningen, in plaats van URLs worden beschouwd, die op gebruikersinteractie wordt gebaseerd. Een weergave kan doorgaans een hele site of gegroepeerde visuele elementen binnen een site vertegenwoordigen.

Als u meer wilt weten over de weergaven, navigeert u naar deze hypothetische online e-commercesite die u in Reageren hebt geïmplementeerd en verkent u enkele voorbeeldweergaven. Klik op de onderstaande koppelingen om deze site te openen in een nieuw browsertabblad.

**Koppeling:[Homesite](https://target.enablementadobe.com/react/demo/#/)**

![thuissite](/help/c-experiences/assets/home.png)

Wanneer we naar de thuissite gaan, zien we meteen een hoofdafbeelding die een paasverkoop bevordert en de nieuwste producten die op de site worden verkocht. In dit geval, kan een Mening als volledige homesite worden gedefinieerd. Dit is handig om op te merken, aangezien we dit verder zullen uitvouwen in de sectie Adobe Target Views hieronder implementeren.

**Koppeling:[Productsite](https://target.enablementadobe.com/react/demo/#/products)**

![productsite](/help/c-experiences/assets/product-site.png)

Aangezien wij meer in de producten worden geinteresseerd die de zaken verkopen, besluiten wij om de verbinding van Producten te klikken. Net als op de thuissite kan de hele productsite worden gedefinieerd als een weergave. We kunnen deze weergave &#39;producten&#39; noemen, net als de padnaam in `https://target.enablementadobe.com/react/demo/#/products)`.

![productsite 2](/help/c-experiences/assets/product-site-2.png)

In het begin van deze sectie definieerden we Weergaven als de gehele site of zelfs als een groep visuele elementen op de site. Zoals hierboven wordt getoond, kunnen de vier producten die op de plaats worden getoond ook als Mening worden gegroepeerd en worden beschouwd. Als we deze weergave een naam willen geven, kunnen we het een product noemen.

![productsite 3](/help/c-experiences/assets/product-site-3.png)

We besluiten op de knop Meer laden te klikken om meer producten op de site te verkennen. De URL van de website verandert in dit geval niet. Maar een weergave hier kan alleen de tweede rij producten weergeven die hierboven wordt weergegeven. De weergavenaam kan &#39;PRODUCTS-PAGE-2&#39; worden genoemd.

**Koppeling:[Afhandeling](https://target.enablementadobe.com/react/demo/#/checkout)**

![uitcheckpagina](/help/c-experiences/assets/checkout.png)

Omdat we bepaalde producten op de site leuk vonden, besloten we een paar te kopen. Nu krijgen we op de uitchecksite enkele opties om normale levering of expreslevering te kiezen. Omdat een weergave elke groep visuele elementen op een site kan zijn, kunnen we deze &quot;Voorkeuren voor levering weergeven&quot; noemen.

Bovendien kan het concept van de standpunten veel verder worden uitgebreid. Als marketers de inhoud op de site willen aanpassen, afhankelijk van de geselecteerde leveringsvoorkeur, kan een Weergave worden gemaakt voor elke leveringsvoorkeur. In dit geval, wanneer wij Normale Levering selecteren, kan de Mening &quot;Normale Levering worden genoemd.&quot; Als Expreslevering is geselecteerd, kan de weergave de naam &quot;Expreslevering&quot; hebben.

Marktdeelnemers kunnen nu een A/B-test uitvoeren om te zien of het wijzigen van de kleur van blauw in rood wanneer Express Delivery is geselecteerd, conversies kan stimuleren in plaats van de knopkleur blauw te houden voor beide leveringsopties.

## Adobe-doelweergaven implementeren

Nu wij hebben behandeld wat de Weergaven van het Doel van Adobe zijn, kunnen wij hefboomwerking dit concept in Doel aan makend marketers om tests A/B en XT op SPAs via VEC in werking te stellen. Hiervoor is een eenmalige ontwikkelaarsinstelling vereist. Laten we de stappen doorlopen om dit in te stellen.

1. Installeer om 0.js 2.x.

   Eerst moeten we installeren op .js 2.x. Deze versie van at.js werd ontwikkeld met SPAs in mening. Eerdere versies van at.js en mbox.js bieden geen ondersteuning voor Adobe Target Views en VEC for SPAs.

   Download bestand.js 2.x via de gebruikersinterface van Adobe Target in [!UICONTROL Setup > Implementatie]. at.js 2.x kan ook worden geïmplementeerd via Adobe Launch. De Adobe Target-extensies zijn momenteel echter niet up-to-date en worden wel ondersteund.

1. Implementeer de nieuwste functie van .js 2.x `triggerView()` op uw sites.

   Na het bepalen van de Weergaven van uw SPA waar u een A/B of XT test wilt in werking stellen, voer de `triggerView()` functie van at.js 2.x met de Bekijken uit binnen als parameter worden overgegaan. Dit staat marketers toe om VEC te gebruiken om de tests A/B en XT voor die Gedefinieerde Kijken te ontwerpen en in werking te stellen. Als de `triggerView()` functie niet voor die Meningen wordt bepaald, zal VEC niet de Meningen ontdekken en zo kunnen de verkopers VEC niet gebruiken om A/B en XT tests te ontwerpen en in werking te stellen.

   **`adobe.target.triggerView(viewName, options)`**

   | Parameter | Type | Vereist? | Validatie | Beschrijving |
   | --- | --- | --- | --- | --- |
   | viewName | String | Ja | 1. Geen navolgende spaties.<br>2. Kan niet leeg zijn.<br>3. De weergavenaam moet uniek zijn voor alle pagina&#39;s.<br>4. **Waarschuwing**: De weergavenaam mag niet beginnen of eindigen met &#39;`/`&#39;. De reden hiervoor is dat de klant doorgaans de weergavenaam uit het URL-pad haalt. Voor ons zijn &quot;thuis&quot; en &quot;`/home`&quot; anders.<br>5. **Waarschuwing**: Dezelfde weergave mag niet meerdere keren achter elkaar worden geactiveerd met de `{page: true}` optie. | Geef een willekeurige naam door als een type tekenreeks dat u de weergave wilt vertegenwoordigen. Deze naam van Mening toont in het paneel van [!UICONTROL Wijzigingen] van VEC voor marketers om acties tot stand te brengen en hun activiteiten A/B en XT in werking te stellen. |
   | opties | Object | Nee |  |  |
   | opties > pagina | Boolean | Nee |  | **TRUE**: De standaardwaarde van de pagina is true. Wanneer `page=true`, zullen de berichten naar de servers van de Rand voor het verhogen van immentatietelling worden verzonden.<br>**FALSE **: Wanneer`page=false`worden geen meldingen verzonden voor het verhogen van het aantal impressies. Dit zou moeten worden gebruikt wanneer u een component op een pagina met een aanbieding slechts opnieuw wilt teruggeven. |

   Nu ga door één of ander voorbeeld gebruiksgevallen op hoe te om de `triggerView()` functie in Reageren voor onze hypothetische e-commerce SPA aan te halen:

   **Koppeling:[Homesite](https://target.enablementadobe.com/react/demo/#/)**

   ![home-response-1](/help/c-experiences/assets/react1.png)

   Als marketers, als wij A/B tests op de volledige homesite willen in werking stellen, dan zouden wij de mening &quot;huis&quot;kunnen willen noemen:

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

**Koppeling: Site voor[producten](https://target.enablementadobe.com/react/demo/#/products)**

Laten we nu een voorbeeld bekijken dat wat gecompliceerder is. Als marketers willen we bijvoorbeeld de tweede rij van de producten aanpassen door de labelkleur &quot;Prijs&quot; in rood te wijzigen nadat een gebruiker op de knop Meer laden heeft geklikt.

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

Als marketers de inhoud op de site willen aanpassen, afhankelijk van de geselecteerde leveringsvoorkeur, kan een Weergave worden gemaakt voor elke leveringsvoorkeur. In dit geval, wanneer wij Normale Levering selecteren, kan de Mening &quot;Normale Levering worden genoemd.&quot; Als Expreslevering is geselecteerd, kan de weergave de naam &quot;Expreslevering&quot; hebben.

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

## at.js 2.x systeemdiagrammen

De volgende diagrammen helpen u het werkschema van at.js 2.x met Meningen begrijpen en hoe dit de integratie van het KUUROORD verbetert. Voor een betere inleiding van de concepten die in at.js 2.x worden gebruikt, zie de implementatie [van de Toepassing van de](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/target-atjs-single-page-application.md)Enige Pagina.

![Doelstroom met at.js 2.x](/help/c-implementing-target/c-implementing-target-for-client-side-web/assets/system-diagram-atjs-20.png)

| Stap | Details |
| --- | --- |
| 1 | De vraag keert terug [!DNL Experience Cloud ID] als de gebruiker voor authentiek wordt verklaard; een andere vraag synchroniseert de klant identiteitskaart |
| 2 | De bibliotheek at.js wordt synchroon geladen en de hoofdtekst van het document verborgen.<br>at.js kan ook asynchroon worden geladen met een optie die fragment verbergt dat op de pagina is geïmplementeerd. |
| 3 | Er wordt een aanvraag voor het laden van een pagina ingediend, inclusief alle geconfigureerde parameters (MCID, SDID en klant-id). |
| 4 | Profielscripts worden uitgevoerd en vervolgens toegevoegd aan de profielenwinkel. De winkel vraagt om gekwalificeerd publiek uit de Audience Library (bijvoorbeeld een publiek dat wordt gedeeld via Adobe Analytics, Audience Management, enz.).<br>Klantkenmerken worden in een batchproces naar de profielopslag verzonden. |
| 5 | Op basis van URL-aanvraagparameters en -profielgegevens [!DNL Target] bepaalt u welke activiteiten en ervaringen u wilt retourneren aan de bezoeker voor de huidige pagina en de toekomstige weergaven. |
| 6 | Gerichte inhoud wordt teruggestuurd naar de pagina, waarbij eventueel ook profielwaarden voor extra personalisatie worden opgenomen.<br>Gerichte inhoud op de huidige pagina wordt zo snel mogelijk zichtbaar zonder flikkering van de standaardinhoud.<br>Gerichte inhoud voor meningen die als resultaat aan gebruikersacties in een KUUROORD worden getoond die in browser in het voorgeheugen wordt opgeslagen zodat kan het onmiddellijk zonder een extra servervraag worden toegepast wanneer de meningen door `triggerView()`. worden teweeggebracht. |
| 7 | De analysegegevens worden verzonden naar de servers van de Inzameling van Gegevens. |
| 8 | De gerichte gegevens worden aangepast aan de analysegegevens via SDID en worden verwerkt in de analytische rapporteringsopslag.<br>De analysegegevens kunnen dan in zowel Analytics als Doel via Analytics voor de rapporten van het Doel (A4T) worden bekeken. |

Nu, waar `triggerView()` op uw SPA wordt uitgevoerd, worden de Meningen en de acties teruggewonnen van geheim voorgeheugen en aan de gebruiker zonder een servervraag getoond. `triggerView()` doet ook een verzoek om meldingen aan de [!DNL Target] achterzijde om het aantal beeldpunten te verhogen en te registreren.

![Doelstroom bij.js 2.x triggerView](/help/c-implementing-target/c-implementing-target-for-client-side-web/assets/atjs-20-triggerview.png)

| Stap | Details |
| --- | --- |
| 1 | `triggerView()` wordt geroepen in het KUUROORD om de Mening terug te geven en acties toe te passen om visuele elementen te wijzigen. |
| 2 | De gerichte inhoud voor de mening wordt gelezen van het geheime voorgeheugen. |
| 3 | Gerichte inhoud wordt zo snel mogelijk zichtbaar zonder flikkering van de standaardinhoud. |
| 4 | Aanvraag voor meldingen wordt naar de [!DNL Target] profielenwinkel verzonden om de bezoeker te tellen in de activiteit en incrementele metingen. |
| 5 | Analytische gegevens die naar de Servers van de Inzameling van Gegevens worden verzonden. |
| 6 | De doelgegevens worden via de SDID aangepast aan de analysegegevens en worden verwerkt in de analytische rapportageopslag. De analysegegevens kunnen dan in zowel Analytics als Doel via A4T- rapporten worden bekeken. |

## Single Page App Visual Experience Composer

Nadat u klaar bent met het installeren van at.js 2.x en het toevoegen `triggerView()` aan uw plaats, gebruik VEC om A/B en XT activiteiten in werking te stellen. Voor meer informatie, zie [Enige Pagina App (SPA) Visuele Composer](/help/c-experiences/spa-visual-experience-composer.md)van de Ervaring.

>[!NOTE]
>
>VEC voor SPAs is werkelijk het zelfde VEC dat u op regelmatige Web-pagina&#39;s gebruikt, maar sommige extra mogelijkheden zijn beschikbaar wanneer u één enkele paginaapp met `triggerView()` uitgevoerd opent.

## Gebruik TriggerView om ervoor te zorgen dat A4T correct met at.js 2.x en SPAs werkt {#triggerview}

Om ervoor te zorgen dat [Analytics voor Doel](/help/c-integrating-target-with-mac/a4t/a4t.md) (A4T) correct met at.js 2.x werkt, ben zeker om zelfde SDID in het verzoek van het Doel en in het verzoek van Analytics te verzenden.

Als beste praktijken met betrekking tot SPAs:

* Gebruik aangepaste gebeurtenissen om te melden dat er iets interessants in de toepassing gebeurt
* Een aangepaste gebeurtenis activeren voordat de weergave begint met renderen
* Een aangepaste gebeurtenis activeren wanneer de weergave is voltooid

at.js 2.x heeft een nieuwe API-functie [triggerView()](/help/c-implementing-target/c-implementing-target-for-client-side-web/adobe-target-triggerview-atjs-2.md) toegevoegd. Gebruik deze optie `triggerView()` om at.js te laten weten dat een weergave begint met renderen.

Een voorbeeld bekijken om te zien hoe u aangepaste gebeurtenissen, in.js 2.x en Analytics kunt combineren. In dit voorbeeld wordt ervan uitgegaan dat de HTML-pagina de Bezoeker-API bevat, gevolgd door at.js 2.x, gevolgd door AppMeasurement.

Laten we aannemen dat de volgende aangepaste gebeurtenissen bestaan:

* `at-view-start` - Wanneer de weergave begint met renderen
* `at-view-end` - Wanneer de weergave is voltooid, wordt rendering voltooid

Om ervoor te zorgen dat A4T met at.js 2.x werkt,

De manager van het meningsbegin zou iets als dit moeten kijken:

```
document.addEventListener("at-view-start", function(e) {
  var visitor = Visitor.getInstance("<your Adobe Org ID>");
  
  visitor.resetState();
  adobe.target.triggerView("<view name>");
});
```

De manager van het meningseind zou iets als dit moeten kijken:

```
document.addEventListener("at-view-end", function(e) {
  // s - is the AppMeasurement tracker object
  s.t();
});
```

>[!NOTE]
>
>U moet de gebeurtenissen `at-view-start` en `at-view-end` gebeurtenissen in brand steken. Deze gebeurtenissen maken geen deel uit van aangepaste gebeurtenissen at.js.

Hoewel in deze voorbeelden JavaScript-code wordt gebruikt, kan dit alles worden vereenvoudigd als u tagbeheer gebruikt, zoals [Adobe Launch](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/cmp-implementing-target-using-adobe-launch.md).

Als de voorafgaande stappen worden gevolgd zou u een robuuste oplossing A4T voor SPAs moeten hebben.

## Best practices implementeren

met API&#39;s van het type at.js 2.x kunt u uw [!DNL Target] implementatie op verschillende manieren aanpassen, maar het is belangrijk dat u de juiste volgorde van bewerkingen tijdens dit proces volgt.

De volgende informatie beschrijft de volgorde van bewerkingen die u moet uitvoeren wanneer u voor het eerst een toepassing voor één pagina in een browser laadt en voor elke weergavewijziging die daarna plaatsvindt.

### Volgorde van bewerkingen voor het laden van de eerste pagina

| Stap | Handeling | Details |
| --- | --- | --- |
| 1 | Bezoeker-API JS laden | Deze bibliotheek is verantwoordelijk voor het toewijzen van een ECID aan de bezoeker. Deze id wordt later gebruikt door andere [!DNL Adobe] oplossingen op de webpagina. |
| 2 | Laden bij.js 2.x | at.js 2.x laadt alle noodzakelijke APIs die u gebruikt om [!DNL Target] verzoeken en meningen uit te voeren. |
| 3 | Uitvoeren van [!DNL Target] verzoek | Als u een gegevenslaag hebt, adviseren wij dat u kritieke gegevens laadt die worden vereist om naar te verzenden [!DNL Target] alvorens een [!DNL Target] verzoek uit te voeren. Hiermee kunt u alle gegevens verzenden die u wilt gebruiken `targetPageParams` voor het opgeven van doelen. U moet ervoor zorgen dat u in deze API-aanroep een verzoek indient voor uitvoering > pageLoad en prefetch > weergaven. als u hebt ingesteld `pageLoadEnabled` en `viewsEnabled`, worden beide opties > pageLoad en prefetch > weergaven automatisch uitgevoerd met Stap 2. anders moet u de `getOffers()` API gebruiken om deze aanvraag in te dienen. |
| 4 | Bellen `triggerView()` | Omdat het [!DNL Target] verzoek u in Stap 3 in werking stelde ervaringen voor zowel de uitvoering van de Lading van de Pagina als Mening kon terugkeren, zorg ervoor dat `triggerView()` wordt geroepen nadat het [!DNL Target] verzoek is teruggekeerd en beëindigt het toepassen van de aanbiedingen aan geheime voorgeheugen. U moet deze stap slechts eenmaal per weergave uitvoeren. |
| 5 | Roep het [!DNL Analytics] paginaweergavebaken aan | Dit baken verzendt SDID verbonden aan Stap 3 en 4 naar [!DNL Analytics] voor gegevens het stitching. |
| 6 | Aanvullende oproep `triggerView({"page": false})` | Dit is een facultatieve stap voor het kader van het KUUROORD dat bepaalde componenten op de pagina zonder een meningsverandering kon potentieel opnieuw teruggeven. In dergelijke gevallen, is het belangrijk dat u deze API aanhaalt om ervoor te zorgen dat de [!DNL Target] ervaringen opnieuw worden toegepast nadat het kader van het KUUROORD de componenten opnieuw heeft teruggegeven. U kunt deze stap zo vaak uitvoeren aangezien u wilt ervoor zorgen dat de [!DNL Target] ervaringen in uw meningen van het KUUROORD blijven. |

### De orde van verrichtingen voor de meningsverandering van het KUUROORD (geen volledig paginaherladen)

| Stap | Handeling | Details |
| --- | --- | --- |
| 1 | Bellen `visitor.resetState()` | Deze API zorgt ervoor dat de SDID opnieuw wordt gegenereerd voor de nieuwe weergave terwijl deze wordt geladen. |
| 2 | Cache bijwerken door de `getOffers()` API aan te roepen | Dit is een optionele stap als deze gezichtswijziging de huidige bezoeker kan kwalificeren voor meer [!DNL Target] activiteiten of hen van activiteiten kan diskwalificeren. Op dit punt kunt u er ook voor kiezen om aanvullende gegevens te verzenden [!DNL Target] voor het mogelijk maken van verdere doelmogelijkheden. |
| 3 | Bellen `triggerView()` | Als u Stap 2 hebt uitgevoerd, dan moet u op het [!DNL Target] verzoek wachten en de aanbiedingen op geheim voorgeheugen toepassen alvorens deze stap uit te voeren. U moet deze stap slechts eenmaal per weergave uitvoeren. |
| 4 | Bellen `triggerView()` | Als u Stap 2 niet hebt uitgevoerd, kunt u deze stap uitvoeren zodra u Stap 1 voltooit. Als u Stap 2 en Stap 3 hebt uitgevoerd, dan zou u deze stap moeten overslaan. U moet deze stap slechts eenmaal per weergave uitvoeren. |
| 5 | Roep het [!DNL Analytics] paginaweergavebaken aan | Dit baken verzendt SDID verbonden aan Stap 2, 3, en 4 naar [!DNL Analytics] voor gegevens het stitching. |
| 6 | Aanvullende oproep `triggerView({"page": false})` | Dit is een facultatieve stap voor het kader van het KUUROORD dat bepaalde componenten op de pagina zonder een meningsverandering kon potentieel opnieuw teruggeven. In dergelijke gevallen, is het belangrijk dat u deze API aanhaalt om ervoor te zorgen dat de [!DNL Target] ervaringen opnieuw worden toegepast nadat het kader van het KUUROORD de componenten opnieuw heeft teruggegeven. U kunt deze stap zo vaak uitvoeren aangezien u wilt ervoor zorgen dat de [!DNL Target] ervaringen in uw meningen van het KUUROORD blijven. |

## Trainingsvideo&#39;s

De volgende video&#39;s bevatten meer informatie:

### Begrijpen hoe at.js 2.x de badge van het ![Overzicht werkt](/help/assets/overview.png)

>[!VIDEO](https://video.tv.adobe.com/v/26250)

Zie [Begrijpen hoe at.js 2.x voor meer informatie werkt](https://helpx.adobe.com/target/kt/using/atjs20-diagram-technical-video-understand.html) .

### Implementeer at.js 2.x in een badge van het ![Leerprogramma van het KUUROORD](/help/assets/tutorial.png)

>[!VIDEO](https://video.tv.adobe.com/v/26248)

Zie Adobe Target&#39;s at.js 2.x [implementeren in een Single Page Application (SPA)](https://helpx.adobe.com/target/kt/using/atjs2-single-page-application-technical-video-implement.html) voor meer informatie.

### De VEC voor SPA&#39;s gebruiken in de badge voor ![zelfstudie van Adobe Target](/help/assets/tutorial.png)

>[!VIDEO](https://video.tv.adobe.com/v/26249)

Zie [het Gebruiken van Composer van de Visuele Ervaring voor Enige Toepassing van de Pagina (SPA VEC) in het Doel](https://helpx.adobe.com/target/kt/using/visual-experience-composer-for-single-page-applications-feature-video-use.html) van Adobe voor meer informatie.
