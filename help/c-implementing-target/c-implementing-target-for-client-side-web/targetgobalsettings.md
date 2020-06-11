---
keywords: serverstate;targetGlobalSettings;targetglobalsettings;globalSettings;globalsettings;global settings;at.js;functions;function;clientCode;clientcode;serverDomain;serverdomain;cookieDomain;cookiedomain;crossDomain;crossdomain;timeout;globalMboxAutoCreate;visitorApiTimeout;defaultContentHiddenStyle;defaultContentVisibleStyle;bodyHiddenStyle;bodyHidingEnabled;imsOrgId;secureOnly;overrideMboxEdgeServer;overrideMboxEdgeServerTimeout;optoutEnabled;optout;opt out;selectorsPollingTimeout;dataProviders;Hybrid Personalization;deviceIdLifetime
description: Informatie over de targetGlobalSettings() functie voor de Adobe Target op .js JavaScript bibliotheek.
title: Informatie over de targetGlobalSettings() functie voor de Adobe Target op .js JavaScript bibliotheek.
subtopic: Getting Started
topic: Standard
translation-type: tm+mt
source-git-commit: 7e602a3451c41ac1f3f2330bce6e763ded82b084
workflow-type: tm+mt
source-wordcount: '1627'
ht-degree: 0%

---


# targetGlobalSettings()

U kunt instellingen in de bibliotheek at.js overschrijven met behulp van `targetGlobalSettings()`, in plaats van de instellingen in de interface [!DNL Target] Standaard/Premium te configureren of met REST API&#39;s.

Er zijn gebruiksgevallen, vooral wanneer at.js via [!DNL Dynamic Tag Management] (DTM) wordt geleverd wanneer u enkele instellingen wilt overschrijven.

## Instellingen {#section_42C759AE9B524A43B8659018677224B8}

U kunt de volgende instellingen overschrijven:

### bodyHiddenStyle

* **Type**: String
* **Standaardwaarde**: body {-dekking: 0 }
* **Omschrijving**: Wordt alleen gebruikt wanneer `globalMboxAutocreate === true` de kans op flikkering tot een minimum wordt beperkt.

   Zie [How at.js Manages Flicker](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/manage-flicker-with-atjs.md)voor meer informatie.

### bodyHidingEnabled

* **Type**: Boolean
* **Standaardwaarde**: true
* **Omschrijving**: Gebruikt om flikkering te controleren wanneer `target-global-mbox` wordt gebruikt om aanbiedingen te leveren die in de Visuele Composer van de Ervaring worden gecreeerd, die ook als visuele aanbiedingen wordt bekend.

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

* **Type**: Zie [Beveiligingsbeleid](#content-security) voor inhoud hieronder.
* **Standaardwaarde**: Zie [Beveiligingsbeleid](#content-security) voor inhoud hieronder.
* **Omschrijving**: Zie [Beveiligingsbeleid](#content-security) voor inhoud hieronder.

### cspStyleNonce

* **Type**: Zie [Beveiligingsbeleid](#content-security) voor inhoud hieronder.
* **Standaardwaarde**: Zie [Beveiligingsbeleid](#content-security) voor inhoud hieronder.
* **Omschrijving**: Zie [Beveiligingsbeleid](#content-security) voor inhoud hieronder.

### dataProviders

* **Type**: Zie [Gegevensleveranciers](#data-providers) hieronder.
* **Standaardwaarde**: Zie [Gegevensleveranciers](#data-providers) hieronder.
* **Omschrijving**: Zie [Gegevensleveranciers](#data-providers) hieronder.

### defaultContentHiddenStyle

* **Type**: String
* **Standaardwaarde**: zichtbaarheid: verborgen
* **Omschrijving**: Wordt alleen gebruikt voor omvattende vakken die gebruikmaken van DIV met klassenaam &quot;mboxDefault&quot; en die worden uitgevoerd via `mboxCreate()`, `mboxUpdate()`of `mboxDefine()` om standaardinhoud te verbergen.

### defaultContentVisibleStyle

* **Type**: String
* **Standaardwaarde**: zichtbaarheid: visible
* **Omschrijving**: Wordt alleen gebruikt voor wrapping-vakken die gebruikmaken van DIV met klassenaam &quot;mboxDefault&quot; en die worden uitgevoerd via `mboxCreate()`, `mboxUpdate()`of `mboxDefine()` om toegepaste aanbieding weer te geven als deze bestaat of inhoud standaard bevat.

### deviceIdLifetime

* **Type**: Getal
* **Standaardwaarde**: 63244800000 ms = 2 jaar
* **Omschrijving**: De hoeveelheid tijd die in cookies `deviceId` wordt doorgebracht.

### enabled

* **Type**: Boolean
* **Standaardwaarde**: true
* **Omschrijving**: Wanneer toegelaten, wordt een [!DNL Target] verzoek om ervaringen en DOM manipulatie terug te winnen om de ervaringen terug te geven automatisch uitgevoerd. Voorts kunnen de [!DNL Target] vraag manueel via `getOffer(s)` / `applyOffer(s)`worden uitgevoerd.

   Wanneer deze optie is uitgeschakeld, worden [!DNL Target] aanvragen niet automatisch of handmatig uitgevoerd.

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
* **Omschrijving**: Geeft aan of we `<clientCode>.tt.omtrdc.net` domein of `mboxedge<clusterNumber>.tt.omtrdc.net` domein moeten gebruiken.

   Als deze waarde true is, wordt het `mboxedge<clusterNumber>.tt.omtrdc.net` domein opgeslagen in een cookie. Werken momenteel niet met [CNAME](/help/c-implementing-target/c-considerations-before-you-implement-target/implement-cname-support-in-target.md)

### overrideMboxEdgeServerTimeout

* **Type**: Getal
* **Standaardwaarde**: 1860000 => 31 minuten
* **Omschrijving**: Geeft de cookielevensduur aan die de `mboxedge<clusterNumber>.tt.omtrdc.net` waarde bevat.

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
* **Omschrijving**: In 0.js 0.9.6 [!DNL Target] introduceerde deze nieuwe instelling die via kan worden overschreven `targetGlobalSettings`.

   De `selectorsPollingTimeout` instelling geeft aan hoelang de client wil wachten totdat alle elementen die door kiezers zijn geïdentificeerd, op de pagina worden weergegeven.

   De activiteiten die via Visual Experience Composer (VEC) worden gecreeerd hebben aanbiedingen die selecteurs bevatten.

### serverDomain

* **Type**: String
* **Standaardwaarde**: Waarde ingesteld via UI.
* **Omschrijving**: Vertegenwoordigt de doelEdge-server.

### serverState

* **Type**: Zie [Hybride personalisatie](#server-state) hieronder.
* **Standaardwaarde**: Zie [Hybride personalisatie](#server-state) hieronder.
* **Omschrijving**: Zie [Hybride personalisatie](#server-state) hieronder.

### timeout

* **Type**: Getal
* **Standaardwaarde**: Waarde ingesteld via UI.
* **Omschrijving**: Geeft de time-out voor de [!DNL Target] randaanvraag aan.

### viewsEnabled

* **Type**: Boolean
* **Standaardwaarde**: true
* **Omschrijving**: Als deze optie is ingeschakeld, haalt u automatisch de weergaven op die bij het laden van de pagina moeten worden geretourneerd. Weergaven worden ondersteund in at.js 2.*alleen x* .

### bezoekerApiTimeout

* **Type**: Getal
* **Standaardwaarde**: 2000 ms = 2 s
* **Omschrijving**: Geeft de time-out van het [!UICONTROL Visitor API] verzoek aan.

## Gebruik {#section_9AD6FA3690364F7480C872CB55567FB0}

Deze functie kan worden gedefinieerd voordat om.js wordt geladen of in **[!UICONTROL Setup]** > **[!UICONTROL Implementation]** > **[!UICONTROL Edit at.js Settings]** > **[!UICONTROL Code Settings]** > **[!UICONTROL Library Header]**.

In het veld Bibliotheekkoptekst kunt u JavaScript in vrije vorm invoeren. De aanpassingscode moet er ongeveer als volgt uitzien:

```
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
| [Gegevensproviders gebruiken in Adobe Target](https://helpx.adobe.com/target/kt/using/dataProviders-atjs-feature-video-use.html) | Gegevensleveranciers zijn een mogelijkheid waarmee u gegevens van derden eenvoudig aan Doel kunt doorgeven. Een derde partij zou een weerdienst, een DMP, of zelfs uw eigen Webdienst kunnen zijn. Vervolgens kunt u deze gegevens gebruiken om een publiek te maken, inhoud te benoemen en het profiel van de bezoeker te verrijken. |
| [Gegevensleveranciers implementeren in Adobe Target](https://helpx.adobe.com/target/kt/using/dataProviders-atjs-technical-video-implement.html) | Implementatiedetails en voorbeelden van hoe u de functie dataProviders van Adobe Target kunt gebruiken om gegevens van externe gegevensleveranciers op te halen en door te geven in de aanvraag van Target. |

De `window.targetGlobalSettings.dataProviders` instelling is een array met gegevensproviders.

Elke gegevensaanbieder heeft de volgende structuur:

| Sleutel | Type | Beschrijving |
|--- |--- |--- |
| name | String | Naam van de provider. |
| versie | String | Providerversie. Deze sleutel zal voor leveranciersevolutie worden gebruikt. |
| timeout | Getal | Geeft de time-out van de provider aan als dit een netwerkaanvraag is.  Deze toets is optioneel. |
| provider | -functie | De functie die de logica voor het ophalen van providergegevens bevat.<br>De functie heeft één vereiste parameter: `callback`. De callback-parameter is een functie die alleen moet worden aangeroepen wanneer de gegevens zijn opgehaald of er een fout optreedt.<br>Callback verwacht twee parameters:<ul><li>fout: Geeft aan of er een fout is opgetreden. Als alles OK is, moet deze parameter op null worden ingesteld.</li><li>param: Een JSON-object dat de parameters vertegenwoordigt die in een doelverzoek worden verzonden.</li></ul> |

In het volgende voorbeeld wordt getoond waar de gegevensaanbieder de synchronisatie uitvoert:

```
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

```
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

In het volgende voorbeeld worden gegevensproviders gebruikt om weergegevens in API te verzamelen en te verzenden als parameters in een aanvraag van het Doel. Het verzoek van het Doel zal extra params, zoals `country` en `weatherCondition`. hebben

```
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

Houd rekening met het volgende wanneer u met de `dataProviders` instelling werkt:

* Als de gegevensleveranciers aan worden toegevoegd asynchroon `window.targetGlobalSettings.dataProviders` zijn, zullen zij parallel worden uitgevoerd. De aanvraag voor de Bezoeker-API wordt parallel met de toegevoegde functies uitgevoerd `window.targetGlobalSettings.dataProviders` om een minimale wachttijd mogelijk te maken.
* at.js zal niet proberen om de gegevens in het voorgeheugen onder te brengen. Als de gegevensleverancier gegevens slechts één keer haalt, zou de gegevensleverancier ervoor moeten zorgen dat de gegevens in het voorgeheugen wordt opgeslagen en, wanneer de leveranciersfunctie wordt aangehaald, de geheim voorgeheugengegevens voor de tweede aanroeping dienen.

## Beveiligingsbeleid voor inhoud {#content-security}

at.js 2.3.0+ steunt het plaatsen van de nonces van het Veiligheidsbeleid van de Inhoud op SCRIPT en STYLE markeringen die aan pagina DOM worden toegevoegd wanneer het toepassen van geleverde aanbiedingen van het Doel.

De SCRIPT- en STYLE-nonces moeten worden ingesteld in `targetGlobalSettings.cspScriptNonce` en `targetGlobalSettings.cspStyleNonce` overeenkomstig, voorafgaand aan het laden van at.js 2.3.0+. Zie een voorbeeld hieronder:

```
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

Nadat `cspScriptNonce` `cspStyleNonce` en de montages worden gespecificeerd, plaatst at.js 2.3.0+ deze als nonce attributen op alle markeringen SCRIPT en STYLE die het aan DOM toevoegt wanneer het toepassen van de aanbiedingen van het Doel.

## Hybride personalisatie {#server-state}

`serverState` is een instelling die beschikbaar is in at.js v2.2+ en die kan worden gebruikt om de paginaprestaties te optimaliseren wanneer een hybride integratie van Target wordt geïmplementeerd. Hybride integratie betekent dat u zowel at.js v2.2+ op de client-kant als de levering-API of een doel-SDK op de server-kant gebruikt om ervaringen te bieden. `serverState` geeft at.js v2.2+ de capaciteit om ervaringen direct van inhoud toe te passen die op de server wordt gehaald en aan de cliënt als deel van de pagina teruggegeven wordt.

### Voorwaarden

Je moet een hybride integratie hebben van [!DNL Target].

* **Server-kant**:  U moet de nieuwe [levering API](https://developers.adobetarget.com/api/delivery-api/) of [Doel SDKs](https://developers.adobetarget.com/api/delivery-api/#section/SDKs)gebruiken.
* **Client**: U moet [at.js versie 2.2 of later](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md)gebruiken.

### Codevoorbeelden

Voor een beter begrip van hoe dit werkt, zie hieronder de codevoorbeelden die u op uw server zou hebben. De code veronderstelt u de SDK [van Node.js van het](https://github.com/adobe/target-nodejs-sdk)Doel gebruikt.

```
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

Een voorbeeldobject `serverState` JSON voor weergaveprefetch ziet er als volgt uit:

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

Nadat de pagina in browser wordt geladen, past at.js alle [!DNL Target] aanbiedingen van `serverState` onmiddellijk toe, zonder enige netwerkvraag tegen de [!DNL Target] rand te vuren. Bovendien prehides at.js alleen de DOM-elementen waarvoor [!DNL Target] aanbiedingen beschikbaar zijn op de server-kant van de content die is opgehaald, waardoor de prestaties bij het laden van de pagina en de gebruikerservaring er positief door worden beïnvloed.

### Belangrijke opmerkingen

Houd rekening met het volgende wanneer u `serverState`:

* Op dit moment biedt at.js v2.2 alleen ondersteuning voor het aanbieden van ervaringen via serverState voor:

   * VEC-gemaakte activiteiten die worden uitgevoerd bij het laden van de pagina.
   * Vooraf opgehaalde weergaven.

      In het geval van SPAs die [!DNL Target] Weergaven en `triggerView()` in at.js API gebruiken, in.js v2.2 geheime voorgeheugens de inhoud voor alle Weergaven die op server-kant worden vooraf ingesteld en past deze toe zodra elke Mening via `triggerView()`, opnieuw wordt teweeggebracht zonder om het even welke extra inhoud-haalt vraag aan Doel te vuren.

   * **Opmerking**:  Op dit moment worden selectievakjes die op de server worden opgehaald, niet ondersteund in `serverState`.

* Bij het toepassen van `serverState `aanbiedingen houdt at.js rekening met `pageLoadEnabled` en `viewsEnabled` instellingen. Aanbiedingen voor laden van pagina worden bijvoorbeeld niet toegepast als de `pageLoadEnabled` instelling false is.

   U schakelt deze instellingen in door de schakeloptie in te schakelen in **[UICONTROL Setup > Implementation > Edit Settings > Page Load Enabled]**.

   ![Instellingen voor Laden van pagina](/help/c-implementing-target/c-implementing-target-for-client-side-web/assets/page-load-enabled-setting.png)

### Aanvullende bronnen

Raadpleeg de volgende bronnen voor meer informatie over hoe `serverState` werkt:

* [Voorbeeldcode](https://github.com/Adobe-Marketing-Cloud/target-node-client-samples/tree/master/advanced-atjs-integration-serverstate).
* [Voorbeeldtoepassing van één pagina (SPA) met `serverState`](https://github.com/Adobe-Marketing-Cloud/target-node-client-samples/tree/master/react-shopping-cart-demo).
