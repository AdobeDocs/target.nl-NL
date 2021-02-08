---
keywords: server;targetGlobalSettings;targetGlobalsettings;globalSettings;globalSettings;global settings;at.js;function;clientCode;clientDomain;serverDomain;serverDomain;cookieDomain;cookieDomain;crossDomain;crossdomain;timeout;globalMboxAutoCreate;bezoekerApiTimeout;defaultContentHiddenStyle defaultContentVisibleStyle;bodyHiddenStyle;bodyHidingEnabled;imsOrgId;secureOnly;overrideMboxEdgeServer;overrideMboxEdgeServerTimeout;optoutEnabled;optout;opt out;kiezersPollingTimeout;dataProviders;Hybrid Personalization;deviceIdLifetime
description: Gebruik de targetGlobalSettings() functie voor de Adobe Target at.js JavaScript bibliotheek om instellingen te overschrijven in plaats van de doel-UI of REST API's te gebruiken.
title: Hoe gebruik ik de functie targetGlobalSettings()?
feature: at.js
role: Developer
translation-type: tm+mt
source-git-commit: bb27f6e540998f7dbe7642551f7a5013f2fd25b4
workflow-type: tm+mt
source-wordcount: '1736'
ht-degree: 0%

---


# targetGlobalSettings()

U kunt instellingen in de bibliotheek at.js overschrijven met behulp van `targetGlobalSettings()` in plaats van de instellingen te configureren in de [!DNL Target] Standard/Premium-interface of door REST API&#39;s te gebruiken.

Er zijn gebruiksgevallen, vooral wanneer at.js via [!DNL Dynamic Tag Management] (DTM) wordt geleverd wanneer u enkele montages zou willen met voeten treden.

## Instellingen {#section_42C759AE9B524A43B8659018677224B8}

U kunt de volgende instellingen overschrijven:

### bodyHiddenStyle

* **Type**: String
* **Standaardwaarde**: body {-dekking: 0 }
* **Omschrijving**: Wordt alleen gebruikt wanneer  `globalMboxAutocreate === true` de kans op flikkering tot een minimum wordt beperkt.

   Zie [How at.js Manages Flicker](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/manage-flicker-with-atjs.md) voor meer informatie.

### bodyHidingEnabled

* **Type**: Boolean
* **Standaardwaarde**: true
* **Omschrijving**: Gebruikt om flikkering te controleren wanneer  `target-global-mbox` wordt gebruikt om aanbiedingen te leveren die in de Visuele Composer van de Ervaring worden gecreeerd, die ook als visuele aanbiedingen wordt bekend.

### clientCode

* **Type**: String
* **Standaardwaarde**: Waarde ingesteld via UI.
* **Omschrijving**: Vertegenwoordigt de clientcode.

### cookieDomain

* **Type**: String
* **Standaardwaarde**: Indien mogelijk ingesteld op het bovenste domein.
* **Omschrijving**: Vertegenwoordigt het domein dat wordt gebruikt bij het opslaan van cookies.

### crossDomain

* **Type**: String
* **Standaardwaarde**: Waarde ingesteld via UI.
* **Omschrijving**: Geeft aan of interdomeintracering is ingeschakeld. De toegestane waarden zijn: uitgeschakeld, ingeschakeld of alleen x.

### cspScriptNonce

* **Type**: Zie  [het ](#content-security) beleid voor inhoudsbeveiliging hieronder.
* **Standaardwaarde**: Zie  [het ](#content-security) beleid voor inhoudsbeveiliging hieronder.
* **Omschrijving**: Zie  [het ](#content-security) beleid voor inhoudsbeveiliging hieronder.

### cspStyleNonce

* **Type**: Zie  [het ](#content-security) beleid voor inhoudsbeveiliging hieronder.
* **Standaardwaarde**: Zie  [het ](#content-security) beleid voor inhoudsbeveiliging hieronder.
* **Omschrijving**: Zie  [het ](#content-security) beleid voor inhoudsbeveiliging hieronder.

### dataProviders

* **Type**: Zie  [hieronder ](#data-providers) Gegevensproviders.
* **Standaardwaarde**: Zie  [hieronder ](#data-providers) Gegevensproviders.
* **Omschrijving**: Zie  [hieronder ](#data-providers) Gegevensproviders.

### defaultContentHiddenStyle

* **Type**: String
* **Standaardwaarde**: zichtbaarheid: verborgen
* **Omschrijving**: Wordt alleen gebruikt voor omvattende vakken die gebruikmaken van DIV met klassenaam &quot;mboxDefault&quot; en die worden uitgevoerd via  `mboxCreate()`,  `mboxUpdate()`of  `mboxDefine()` om standaardinhoud te verbergen.

### defaultContentVisibleStyle

* **Type**: String
* **Standaardwaarde**: zichtbaarheid: visible
* **Omschrijving**: Wordt alleen gebruikt voor wrapping-vakken die gebruikmaken van DIV met klassenaam &quot;mboxDefault&quot; en die worden uitgevoerd via  `mboxCreate()`,  `mboxUpdate()`of  `mboxDefine()` om de toegepaste aanbieding weer te geven als er inhoud of standaardinhoud is.

### deviceIdLifetime

* **Type**: Getal
* **Standaardwaarde**: 63244800000 ms = 2 jaar
* **Omschrijving**: De hoeveelheid tijd  `deviceId` wordt in cookies aangehouden.

>[!NOTE]
>
>De instelling deviceIdLifetime kan worden overschreven in at.js versie 2.3.1 of hoger.

### enabled

* **Type**: Boolean
* **Standaardwaarde**: true
* **Omschrijving**: Wanneer toegelaten, wordt een  [!DNL Target] verzoek om ervaringen en DOM manipulatie terug te winnen om de ervaringen terug te geven automatisch uitgevoerd. Daarnaast kunnen [!DNL Target] aanroepen handmatig worden uitgevoerd via `getOffer(s)` / `applyOffer(s)`.

   Als [!DNL Target]-verzoeken zijn uitgeschakeld, worden deze niet automatisch of handmatig uitgevoerd.

### globalMboxAutoCreate

* **Type**: Getal
* **Standaardwaarde**: Waarde ingesteld via UI.
* **Omschrijving**: Geeft aan of het algemene mbox-verzoek moet worden geactiveerd.

### imsOrgId

* **Type**: Sting
* **Standaardwaarde**: true
* **Omschrijving**: Vertegenwoordigt de IMS ORG-ID.

### optoutEnabled

* **Type**: Boolean
* **Standaardwaarde**: false
* **Omschrijving**: Geeft aan of Target de API- `isOptedOut()` functie voor bezoekers moet aanroepen. Dit maakt deel uit van de functie voor apparaatgrafiek.

### overrideMboxEdgeServer

* **Type**: Boolean
* **Standaardwaarde**: true (waar, vanaf at.js versie 1.6.2)
* **Omschrijving**: Geeft aan of we  `<clientCode>.tt.omtrdc.net` domein of  `mboxedge<clusterNumber>.tt.omtrdc.net` domein moeten gebruiken.

   Als deze waarde true is, wordt het `mboxedge<clusterNumber>.tt.omtrdc.net`-domein opgeslagen in een cookie. Werkt momenteel niet met [CNAME](/help/c-implementing-target/c-considerations-before-you-implement-target/implement-cname-support-in-target.md) bij het gebruiken van at.js versies vóór at.js 1.8.2 en at.js 2.3.1. Als dit voor u een probleem is, kunt u [het bijwerken om .js](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md) tot een nieuwere, ondersteunde versie overwegen.

### overrideMboxEdgeServerTimeout

* **Type**: Getal
* **Standaardwaarde**: 1860000 => 31 minuten
* **Omschrijving**: Geeft de cookielevensduur aan die de  `mboxedge<clusterNumber>.tt.omtrdc.net` waarde bevat.

### pageLoadEnabled

* **Type**: Boolean
* **Standaardwaarde**: true
* **Omschrijving**: Als deze optie is ingeschakeld, haalt u automatisch ervaringen op die bij het laden van de pagina moeten worden geretourneerd.

### secureOnly

* **Type**: Boolean
* **Standaardwaarde**: false
* **Omschrijving**: Geeft aan of at.js alleen HTTPS mag gebruiken of mag schakelen tussen HTTP en HTTPS op basis van het paginaprotocol.

### selectorsPollingTimeout

* **Type**: Getal
* **Standaardwaarde**: 5000 ms = 5 s
* **Omschrijving**: In 0.js 0.9.6  [!DNL Target] introduceerde deze nieuwe instelling die via kan worden overschreven  `targetGlobalSettings`.

   De instelling `selectorsPollingTimeout` geeft aan hoelang de client bereid is te wachten totdat alle elementen die door kiezers zijn geïdentificeerd, op de pagina worden weergegeven.

   De activiteiten die via Visual Experience Composer (VEC) worden gecreeerd hebben aanbiedingen die selecteurs bevatten.

### serverDomain

* **Type**: String
* **Standaardwaarde**: Waarde ingesteld via UI.
* **Omschrijving**: Vertegenwoordigt de doelEdge-server.

### serverState

* **Type**: Zie  [Hybride ](#server-state) personalisatie hieronder.
* **Standaardwaarde**: Zie  [Hybride ](#server-state) personalisatie hieronder.
* **Omschrijving**: Zie  [Hybride ](#server-state) personalisatie hieronder.

### timeout

* **Type**: Getal
* **Standaardwaarde**: Waarde ingesteld via UI.
* **Omschrijving**: Geeft de time-out voor de  [!DNL Target] randaanvraag aan.

### viewsEnabled

* **Type**: Boolean
* **Standaardwaarde**: true
* **Omschrijving**: Als deze optie is ingeschakeld, haalt u automatisch de weergaven op die moeten worden geretourneerd tijdens het laden van de pagina. Weergaven worden ondersteund in at.js 2.** Alleen.

### bezoekerApiTimeout

* **Type**: Getal
* **Standaardwaarde**: 2000 ms = 2 s
* **Omschrijving**: Geeft de time-out van het  [!UICONTROL Visitor API] verzoek aan.

## Gebruik {#section_9AD6FA3690364F7480C872CB55567FB0}

Deze functie kan worden gedefinieerd voordat at.js wordt geladen of in **[!UICONTROL Administration]** > **[!UICONTROL Implementation]** > **[!UICONTROL Edit at.js Settings]** > **[!UICONTROL Code Settings]** > **[!UICONTROL Library Header]**.

In het veld Bibliotheekkoptekst kunt u JavaScript in vrije vorm invoeren. De aanpassingscode moet er ongeveer als volgt uitzien:

```javascript
window.targetGlobalSettings = {  
   timeout: 200, // using custom timeout  
   visitorApiTimeout: 500, // using custom API timeout  
   enabled: document.location.href.indexOf('https://www.adobe.com') >= 0 // enabled ONLY on adobe.com  
};
```

## Gegevensleveranciers {#data-providers}

Met deze instelling kunnen klanten gegevens verzamelen van gegevensleveranciers van derden, zoals Demandbase, BlueKai en aangepaste services, en de gegevens doorgeven aan Target als mbox-parameters in het algemene mbox-verzoek. Het steunt de inzameling van gegevens van veelvoudige leveranciers via async en synchronisatieverzoeken. Op deze manier kunt u flikkering van de standaardpagina-inhoud eenvoudig beheren en onafhankelijke time-outs opnemen voor elke provider om de invloed op de paginaprestaties te beperken

>[!NOTE]
>
>Voor gegevensleveranciers is [!DNL at.js] 1.3 of hoger vereist.

De volgende video&#39;s bevatten meer informatie:

| Video | Beschrijving |
|--- |--- |
| [Gegevensleveranciers gebruiken in Adobe Target](https://helpx.adobe.com/target/kt/using/dataProviders-atjs-feature-video-use.html) | Gegevensleveranciers zijn een mogelijkheid waarmee u gegevens van derden eenvoudig aan Doel kunt doorgeven. Een derde partij zou een weerdienst, een DMP, of zelfs uw eigen Webdienst kunnen zijn. Vervolgens kunt u deze gegevens gebruiken om een publiek te maken, inhoud te benoemen en het profiel van de bezoeker te verrijken. |
| [Gegevensleveranciers implementeren in Adobe Target](https://helpx.adobe.com/target/kt/using/dataProviders-atjs-technical-video-implement.html) | Implementatiedetails en voorbeelden van het gebruik van de functie Adobe Target DataProviders om gegevens van externe gegevensleveranciers op te halen en door te geven in de aanvraag van het Doel. |

De instelling `window.targetGlobalSettings.dataProviders` is een array van gegevensproviders.

Elke gegevensaanbieder heeft de volgende structuur:

| Sleutel | Type | Beschrijving |
|--- |--- |--- |
| name | String | Naam van de provider. |
| versie | String | Providerversie. Deze sleutel zal voor leveranciersevolutie worden gebruikt. |
| timeout | Getal | Geeft de time-out van de provider aan als dit een netwerkaanvraag is.  Deze toets is optioneel. |
| provider | -functie | De functie die de logica voor het ophalen van providergegevens bevat.<br>De functie heeft één vereiste parameter:  `callback`. De callback-parameter is een functie die alleen moet worden aangeroepen wanneer de gegevens zijn opgehaald of er een fout optreedt.<br>Callback verwacht twee parameters:<ul><li>fout: Geeft aan of er een fout is opgetreden. Als alles OK is, moet deze parameter op null worden ingesteld.</li><li>param: Een JSON-object dat de parameters vertegenwoordigt die in een doelverzoek worden verzonden.</li></ul> |

In het volgende voorbeeld wordt getoond waar de gegevensaanbieder de synchronisatie uitvoert:

```javascript
var syncDataProvider = { 
  name: "simpleDataProvider", 
  version: "1.0.0", 
  provider: function(callback) { 
    callback(null, {t1: 1}); 
  } 
}; 
  
window.targetGlobalSettings = { 
  dataProviders: [ 
    syncDataProvider 
  ] 
};
```

Na processen at.js `window.targetGlobalSettings.dataProviders`, zal het verzoek van het Doel een nieuwe parameter bevatten: `t1=1`.

Het volgende is een voorbeeld als de parameters die u aan het verzoek van het Doel wilt toevoegen van de derdedienst, zoals Bluekai, Demandbase, enzovoort worden gehaald:

```javascript
var blueKaiDataProvider = { 
   name: "blueKai", 
   version: "1.0.0", 
   provider: function(callback) { 
      // simulating network request 
     setTimeout(function() { 
       callback(null, {t1: 1, t2: 2, t3: 3}); 
     }, 1000); 
   } 
} 
  
window.targetGlobalSettings = { 
   dataProviders: [ 
      blueKaiDataProvider 
   ] 
};
```

Na processen at.js `window.targetGlobalSettings.dataProviders`, zal het verzoek van het Doel extra parameters bevatten: `t1=1`, `t2=2` en `t3=3`.

In het volgende voorbeeld worden gegevensproviders gebruikt om weergegevens in API te verzamelen en te verzenden als parameters in een aanvraag van het Doel. Het verzoek van het Doel zal extra params, zoals `country` en `weatherCondition` hebben.

```javascript
var weatherProvider = { 
      name: "weather-api", 
      version: "1.0.0", 
      timeout: 2000, 
      provider: function(callback) { 
        var API_KEY = "caa84fc6f5dc77b6372d2570458b8699"; 
        var lat = 44.426767399999996; 
        var lon = 26.1025384; 
        var url = "//api.openweathermap.org/data/2.5/weather?lang=en"; 
        var data = { 
          lat: lat, 
          lon: lon, 
          appId: API_KEY 
        } 
 
        $.ajax({ 
          type: "GET", 
                url: url, 
          dataType: "json", 
          data: data, 
          success: function(data) { 
            console.log("Weather data", data); 
            callback(null, { 
              country: data.sys.country, 
              weatherCondition: data.weather[0].main 
            }); 
          }, 
          error: function(err) { 
            console.log("Error", err); 
            callback(err); 
          } 
        });         
      } 
    }; 
 
    window.targetGlobalSettings = { 
      dataProviders: [weatherProvider] 
    };
```

Houd rekening met het volgende wanneer u met de instelling `dataProviders` werkt:

* Als de gegevensproviders die aan `window.targetGlobalSettings.dataProviders` zijn toegevoegd, asynchroon zijn, worden ze parallel uitgevoerd. Het verzoek voor de bezoeker-API wordt parallel met de functies uitgevoerd die aan `window.targetGlobalSettings.dataProviders` zijn toegevoegd, zodat er minimaal een wachttijd is.
* at.js zal niet proberen om de gegevens in het voorgeheugen onder te brengen. Als de gegevensleverancier gegevens slechts één keer haalt, zou de gegevensleverancier ervoor moeten zorgen dat de gegevens in het voorgeheugen wordt opgeslagen en, wanneer de leveranciersfunctie wordt aangehaald, de geheim voorgeheugengegevens voor de tweede aanroeping dienen.

## Inhoudbeveiligingsbeleid {#content-security}

at.js 2.3.0+ steunt het plaatsen van de nonces van het Veiligheidsbeleid van de Inhoud op SCRIPT en STYLE markeringen die aan pagina DOM worden toegevoegd wanneer het toepassen van geleverde aanbiedingen van het Doel.

De SCRIPT- en STYLE-nonces moeten dienovereenkomstig worden ingesteld in `targetGlobalSettings.cspScriptNonce` en `targetGlobalSettings.cspStyleNonce`, voorafgaand aan het laden van at.js 2.3.0+. Zie een voorbeeld hieronder:

```javascript
...
<head>
 <script nonce="<script_nonce_value>">
window.targetGlobalSettings = {
  cspScriptNonce: "<csp_script_nonce_value>",
  cspStyleNonce: "<csp_style_nonce_value>"
};
 </script>
 <script nonce="<script_nonce_value>" src="at.js"></script>
...
</head>
...
```

Nadat `cspScriptNonce` en `cspStyleNonce` montages worden gespecificeerd, plaatst at.js 2.3.0+ deze als nonce attributen op alle markeringen SCRIPT en STYLE die het aan DOM wanneer het toepassen van de aanbiedingen van het Doel toevoegt.

## Hybride personalisatie {#server-state}

`serverState` is een instelling die beschikbaar is in at.js v2.2+ en die kan worden gebruikt om de paginaprestaties te optimaliseren wanneer een hybride integratie van Target wordt geïmplementeerd. Hybride integratie betekent dat u zowel at.js v2.2+ op de client-kant als de levering-API of een doel-SDK op de server-kant gebruikt om ervaringen te bieden. `serverState` geeft at.js v2.2+ de capaciteit om ervaringen direct van inhoud toe te passen die op de server wordt gehaald en aan de cliënt als deel van de pagina teruggegeven wordt.

### Voorwaarden

U moet een hybride integratie van [!DNL Target] hebben.

* **Server-kant**: U moet de nieuwe  [levering ](https://developers.adobetarget.com/api/delivery-api/) API of  [Doel SDKs](https://developers.adobetarget.com/api/delivery-api/#section/SDKs) gebruiken.
* **Client**: U moet  [at.js versie 2.2 of later](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md) gebruiken.

### Codevoorbeelden

Voor een beter begrip van hoe dit werkt, zie hieronder de codevoorbeelden die u op uw server zou hebben. In de code wordt aangenomen dat u de SDK [Target Node.js](https://github.com/adobe/target-nodejs-sdk) gebruikt.

```javascript
// First, we fetch the offers via Target Node.js SDK API, as usual
const targetResponse = await targetClient.getOffers(options);
// A successfull response will contain Target Delivery API request and response objects, which we need to set as serverState
const serverState = {
  request: targetResponse.request,
  response: targetResponse.response
};
// Finally, we should set window.targetGlobalSettings.serverState in the returned page, by replacing it in a page template, for example
const PAGE_TEMPLATE = `
<!doctype html>
<html>
<head>
  ...
  <script>
    window.targetGlobalSettings = {
      overrideMboxEdgeServer: true,
      serverState: ${JSON.stringify(serverState, null, " ")}
    };
  </script>
  <script src="at.js"></script>
</head>
...
</html>
`;
// Return PAGE_TEMPLATE to the client ...
```

Een voorbeeld van een JSON-object `serverState` voor de weergaveprefetch ziet er als volgt uit:

```
{
 "request": {
  "requestId": "076ace1cd3624048bae1ced1f9e0c536",
  "id": {
   "tntId": "08210e2d751a44779b8313e2d2692b96.21_27"
  },
  "context": {
   "channel": "web",
   "timeOffsetInMinutes": 0
  },
  "experienceCloud": {
   "analytics": {
    "logging": "server_side",
    "supplementalDataId": "7D3AA246CC99FD7F-1B3DD2E75595498E"
   }
  },
  "prefetch": {
   "views": [
    {
     "address": {
      "url": "my.testsite.com/"
     }
    }
   ]
  }
 },
 "response": {
  "status": 200,
  "requestId": "076ace1cd3624048bae1ced1f9e0c536",
  "id": {
   "tntId": "08210e2d751a44779b8313e2d2692b96.21_27"
  },
  "client": "testclient",
  "edgeHost": "mboxedge21.tt.omtrdc.net",
  "prefetch": {
   "views": [
    {
     "name": "home",
     "key": "home",
     "options": [
      {
       "type": "actions",
       "content": [
        {
         "type": "setHtml",
         "selector": "#app > DIV.app-container:eq(0) > DIV.page-container:eq(0) > DIV:nth-of-type(2) > SECTION.section:eq(0) > DIV.container:eq(1) > DIV.heading:eq(0) > H1.title:eq(0)",
         "cssSelector": "#app > DIV:nth-of-type(1) > DIV:nth-of-type(1) > DIV:nth-of-type(2) > SECTION:nth-of-type(1) > DIV:nth-of-type(2) > DIV:nth-of-type(1) > H1:nth-of-type(1)",
         "content": "<span style=\"color:#FF0000;\">Latest</span> Products for 2020"
        }
       ],
       "eventToken": "t0FRvoWosOqHmYL5G18QCZNWHtnQtQrJfmRrQugEa2qCnQ9Y9OaLL2gsdrWQTvE54PwSz67rmXWmSnkXpSSS2Q==",
       "responseTokens": {
        "profile.memberlevel": "0",
        "geo.city": "dublin",
        "activity.id": "302740",
        "experience.name": "Experience B",
        "geo.country": "ireland"
       }
      }
     ],
     "state": "J+W1Fq18hxliDDJonTPfV0S+mzxapAO3d14M43EsM9f12A6QaqL+E3XKkRFlmq9U"
    }
   ]
  }
 }
}
```

Nadat de pagina in browser wordt geladen, past at.js alle [!DNL Target] aanbiedingen van `serverState` onmiddellijk toe, zonder netwerkvraag tegen [!DNL Target] rand te vuren. Bovendien prehidt at.js alleen de DOM-elementen waarvoor [!DNL Target] aanbiedingen beschikbaar zijn op de server-kant van de opgehaalde inhoud. Dit heeft een positief effect op de prestaties bij het laden van pagina&#39;s en de gebruikerservaring.

### Belangrijke opmerkingen

Houd rekening met het volgende wanneer u `serverState` gebruikt:

* Op dit moment biedt at.js v2.2 alleen ondersteuning voor het aanbieden van ervaringen via serverState voor:

   * VEC-gemaakte activiteiten die worden uitgevoerd bij het laden van de pagina.
   * Vooraf opgehaalde weergaven.

      Als SPA [!DNL Target] Weergaven en `triggerView()` in de API at.js gebruikt, plaatst at.js v2.2 de inhoud voor alle weergaven die op de server zijn voorafgegaan in cache en past deze toe zodra elke Weergave via `triggerView()` wordt geactiveerd, opnieuw zonder dat aanvullende aanroepen voor het ophalen van inhoud naar Target worden afgevuurd.

   * **Opmerking**: Op dit moment worden selectievakjes die op de server worden opgehaald, niet ondersteund in  `serverState`.

* Wanneer u `serverState `aanbiedingen toepast, houdt at.js rekening met de instellingen `pageLoadEnabled` en `viewsEnabled`. Aanbiedingen voor het laden van pagina worden bijvoorbeeld niet toegepast als de instelling `pageLoadEnabled` onwaar is.

   Als u deze instellingen wilt inschakelen, schakelt u de schakeloptie **[!UICONTROL Administration]> [!UICONTROL Implementation] > [!UICONTROL Edit] >[!UICONTROL Page Load Enabled]** in.

   ![Instellingen voor Laden van pagina](/help/c-implementing-target/c-implementing-target-for-client-side-web/assets/page-load-enabled-setting.png)

* Als u `serverState` gebruikt en `<script>` markeringen in de teruggekeerde inhoud gebruikt, zorg ervoor dat uw inhoud van HTML `<\/script>` in plaats van `</script>` gebruikt. Als u `</script>` gebruikt, interpreteert de browser `</script>` als het eind op een gealigneerd SCRIPT en het zou de HTML- pagina kunnen breken.

### Aanvullende bronnen

Als u meer wilt weten over de werking van `serverState`, bekijkt u de volgende bronnen:

* [Voorbeeldcode](https://github.com/Adobe-Marketing-Cloud/target-node-client-samples/tree/master/advanced-atjs-integration-serverstate).
* [Toepassing van één pagina (SPA) voorbeeldtoepassing met  `serverState`](https://github.com/Adobe-Marketing-Cloud/target-node-client-samples/tree/master/react-shopping-cart-demo).
