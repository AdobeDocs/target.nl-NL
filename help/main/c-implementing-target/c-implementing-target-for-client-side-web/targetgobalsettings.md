---
keywords: server;targetGlobalSettings;targetGlobalsettings;globalSettings;globalSettings;global settings;at.js;function;clientCode;clientDomain;serverDomain;serverDomain;cookieDomain;cookieDomain;crossDomain;crossdomain;timeout;globalMboxAutoCreate;bezoekerApiTimeout;defaultContentHiddenStyle defaultContentVisibleStyle;bodyHiddenStyle;bodyHidingEnabled;imsOrgId;secureOnly;overrideMboxEdgeServer;overrideMboxEdgeServerTimeout;optoutEnabled;optout;opt out;kiezersPollingTimeout;dataProviders;Hybrid Personalization;deviceIdLifetime
description: Gebruik de targetGlobalSettings() functie voor de Adobe [!DNL Target] at.js JavaScript-bibliotheek om instellingen te overschrijven in plaats van de [!DNL Target] UI- of REST-API's.
title: Hoe gebruik ik de functie targetGlobalSettings()?
feature: at.js
role: Developer
exl-id: 14080cf6-6a15-4829-b95d-62c068898564
source-git-commit: c196b7e41101978ee029f93d5cd71c9b2d5b99f1
workflow-type: tm+mt
source-wordcount: '2371'
ht-degree: 0%

---

# targetGlobalSettings()

U kunt instellingen in de bibliotheek at.js overschrijven met `targetGlobalSettings()`in plaats van de instellingen in het dialoogvenster [!DNL Target] Standaard/Premium-gebruikersinterface of met REST-API&#39;s.

## Instellingen {#section_42C759AE9B524A43B8659018677224B8}

U kunt de volgende instellingen overschrijven:

### bodyHiddenStyle

* **Type**: String
* **Standaardwaarde**: body {-dekking: 0 }
* **Beschrijving**: Wordt alleen gebruikt wanneer `globalMboxAutocreate === true` om de kans op flikkering te minimaliseren.

   Zie voor meer informatie [Hoe at.js flikkering beheert](https://developer.adobe.com/target/implement/client-side/atjs/how-atjs-works/manage-flicker-with-atjs/).

### bodyHidingEnabled

* **Type**: Boolean
* **Standaardwaarde**: true
* **Beschrijving**: Wordt gebruikt om flikkering te besturen wanneer `target-global-mbox` wordt gebruikt om aanbiedingen te leveren die in de Visuele Composer van de Ervaring worden gecreeerd, die ook als visuele aanbiedingen wordt bekend.

### clientCode

* **Type**: String
* **Standaardwaarde**: Waarde ingesteld via UI.
* **Beschrijving**: Vertegenwoordigt de clientcode.

### cookieDomain

* **Type**: String
* **Standaardwaarde**: Indien mogelijk ingesteld op het bovenste domein.
* **Beschrijving**: Vertegenwoordigt het domein dat wordt gebruikt bij het opslaan van cookies.

### crossDomain

* **Type**: String
* **Standaardwaarde**: Waarde ingesteld via UI.
* **Beschrijving**: Geeft aan of interdomeintracering is ingeschakeld. De toegestane waarden zijn: uitgeschakeld, ingeschakeld of alleen x.

### cspScriptNonce

* **Type**: Zie [Beveiligingsbeleid voor inhoud](#content-security) hieronder.
* **Standaardwaarde**: Zie [Beveiligingsbeleid voor inhoud](#content-security) hieronder.
* **Beschrijving**: Zie [Beveiligingsbeleid voor inhoud](#content-security) hieronder.

### cspStyleNonce

* **Type**: Zie [Beveiligingsbeleid voor inhoud](#content-security) hieronder.
* **Standaardwaarde**: Zie [Beveiligingsbeleid voor inhoud](#content-security) hieronder.
* **Beschrijving**: Zie [Beveiligingsbeleid voor inhoud](#content-security) hieronder.

### dataProviders

* **Type**: Zie [Gegevensleveranciers](#data-providers) hieronder.
* **Standaardwaarde**: Zie [Gegevensleveranciers](#data-providers) hieronder.
* **Beschrijving**: Zie [Gegevensleveranciers](#data-providers) hieronder.

### determinoningMethod {#on-device-decisioning}

* **Type**: String
* **Standaardwaarde**: serverzijde
* **Overige waarden**: op apparaat, hybride
* **Beschrijving**: Zie de onderstaande beslissingsmethoden.

   **beslissingsmethoden**

   Bij apparaatbeslissingen introduceert Target een nieuwe instelling genaamd [!UICONTROL Decisioning Method] dat dicteert hoe at.js uw ervaringen levert. De `decisioningMethod` heeft drie waarden: alleen aan de serverzijde, alleen op het apparaat en hybride. Wanneer `decisioningMethod` is ingesteld in `targetGlobalSettings()`, fungeert het als standaardbeslissingsmethode voor iedereen [!DNL Target] besluiten.

   **[!UICONTROL Server-side only]**:

   [!UICONTROL Server-side only] is de standaardbepalingsmethode die uit de doos wordt geplaatst wanneer at.js 2.5+ wordt uitgevoerd en op uw Web-eigenschappen opgesteld.

   Gebruiken [!UICONTROL server-side only] als de standaardconfiguratie betekent dat alle beslissingen worden genomen over de [!DNL Target] edge network, wat een blokkerende servervraag impliceert. Deze aanpak kan incrementele latentie introduceren, maar biedt ook aanzienlijke voordelen, zoals de mogelijkheid om de mogelijkheden van Target voor machinaal leren toe te passen, zoals [Recommendations](/help/main/c-recommendations/recommendations.md), [Automated Personalization](/help/main/c-activities/t-automated-personalization/automated-personalization.md) (AP), en [Automatisch doel](/help/main/c-activities/auto-target/auto-target-to-optimize.md) activiteiten.

   Bovendien kan het verbeteren van uw gepersonaliseerde ervaringen door het gebruikersprofiel van Target te gebruiken, dat over zittingen en kanalen wordt voortgeduurd, krachtige resultaten voor uw zaken verstrekken.

   Tot slot: [!UICONTROL server-side only] Hiermee kunt u de Adobe Experience Cloud gebruiken en het publiek precies afstemmen waarop u zich kunt richten via de segmenten Audience Manager en Adobe Analytics.

   **[!UICONTROL On-device only]**:

   [!UICONTROL On-Device only] is de besluitvormingsmethode die in at.js 2.5+ moet worden geplaatst wanneer de op-apparatenbeslissing slechts door uw Web-pagina&#39;s zou moeten worden gebruikt.

   De besluitvorming op het apparaat kan uw ervaringen en verpersoonlijkingsactiviteiten bij het opblazen van snelle snelheid leveren omdat de besluiten van een caching regelartefact worden gemaakt dat al uw activiteiten bevat die voor op-apparaat besluitvorming kwalificeren.

   Zie de sectie met ondersteunde functies voor meer informatie over welke activiteiten in aanmerking komen voor beslissingen op het apparaat.

   Deze beslissingsmethode moet alleen worden gebruikt als de prestaties van essentieel belang zijn voor alle pagina&#39;s waarvoor beslissingen nodig zijn [!DNL Target]. Houd er bovendien rekening mee dat wanneer deze beslissingsmethode wordt geselecteerd, uw [!DNL Target] activiteiten die niet in aanmerking komen voor beslissingen op het apparaat worden niet uitgevoerd of uitgevoerd. De bibliotheek at.js 2.5+ wordt gevormd om het caching regelartefact slechts te zoeken om besluiten te nemen.

   **Hybride**:

   [!UICONTROL Hybrid] is de besluitvormingsmethode die in at.js 2.5+ moet worden geplaatst wanneer zowel op-apparatenbesluit als activiteiten die een netwerkvraag aan het netwerk van de Rand van Adobe Target vereisen moeten worden uitgevoerd.

   Wanneer u zowel op apparaat beslissingsactiviteiten als server-zijactiviteiten beheert, kan het een beetje gecompliceerd en vervelend zijn wanneer het denken over hoe te om en voorziening op te stellen [!DNL Target] op uw pagina&#39;s. met hybride als beslissingsmethode, [!DNL Target] weet wanneer het een servervraag aan het netwerk van Adobe Target Edge voor activiteiten moet maken die server-zijuitvoering vereisen, en ook wanneer om slechts op-apparatenbesluiten uit te voeren.

   Het Artefact van JSON-regels bevat metagegevens om at.js te informeren of een box een serveractiviteit heeft die wordt uitgevoerd of een beslissingsactiviteit op het apparaat. Deze beslissingsmethode zorgt ervoor dat activiteiten die u snel wilt laten uitvoeren, worden uitgevoerd via apparaatbeslissingen en voor activiteiten die krachtigere, door ML gestuurde personalisatie vereisen, worden deze activiteiten uitgevoerd via het Adobe Target Edge-netwerk.

### defaultContentHiddenStyle

* **Type**: String
* **Standaardwaarde**: zichtbaarheid: verborgen
* **Beschrijving**: Wordt alleen gebruikt voor omsluitende kaders die gebruikmaken van DIV met klassenaam &quot;mboxDefault&quot; en die via `mboxCreate()`, `mboxUpdate()`, of `mboxDefine()` om standaardinhoud te verbergen.

### defaultContentVisibleStyle

* **Type**: String
* **Standaardwaarde**: zichtbaarheid: visible
* **Beschrijving**: Wordt alleen gebruikt voor omsluitende kaders die gebruikmaken van DIV met klassenaam &quot;mboxDefault&quot; en die via `mboxCreate()`, `mboxUpdate()`, of `mboxDefine()` om het toegepaste voorstel als om het even welke of standaardinhoud te onthullen.

### deviceIdLifetime

* **Type**: Getal
* **Standaardwaarde**: 63244800000 ms = 2 jaar
* **Beschrijving**: Tijd `deviceId` blijft in cookies bestaan.

>[!NOTE]
>
>De instelling deviceIdLifetime kan worden overschreven in at.js versie 2.3.1 of hoger.

### enabled

* **Type**: Boolean
* **Standaardwaarde**: true
* **Beschrijving**: Indien ingeschakeld, wordt een [!DNL Target] verzoek om ervaringen op te halen en DOM-manipulatie om de ervaringen te renderen wordt automatisch uitgevoerd. Bovendien [!DNL Target] de vraag kan manueel via worden uitgevoerd `getOffer(s)` / `applyOffer(s)`.

   Indien uitgeschakeld, [!DNL Target] aanvragen worden niet automatisch of handmatig uitgevoerd.

### globalMboxAutoCreate

* **Type**: Getal
* **Standaardwaarde**: Waarde ingesteld via UI.
* **Beschrijving**: Geeft aan of het algemene mbox-verzoek moet worden geactiveerd.

### imsOrgId

* **Type**: Sting
* **Standaardwaarde**: true
* **Beschrijving**: Vertegenwoordigt de IMS ORG-ID.

### optinEnabled

* **Type**: Boolean
* **Standaardwaarde**: false
* **Beschrijving**: [!DNL Target] biedt ondersteuning voor aanmeldingsfunctionaliteit via [!DNL Adobe Experience Platform] om u te helpen uw toestemmingsbeheerstrategie steunen. De opt-in functionaliteit laat klanten controleren hoe en wanneer [!DNL Target] -tag wordt geactiveerd. Er is ook een optie via [!DNL Adobe Experience Platform] om de [!DNL Target] tag. De mogelijkheid om Opt-In te gebruiken in het dialoogvenster [!DNL Target] at.js-bibliotheek toevoegen `optinEnabled=true` instellen. In [!DNL Adobe Experience Platform] u moet &quot;toelaten&quot;van selecteren [!UICONTROL GDPR Opt-In] vervolgkeuzelijst in de installatieweergave van de extensie. Zie de [Adobe Experience Platform-documentatie](https://developer.adobe.com/target/implement/client-side/atjs/how-to-deployatjs/implement-target-using-adobe-launch/) voor meer informatie . Zie voor meer informatie over deze instelling in verband met privacy- en gegevensbeschermingsvoorschriften, waaronder de algemene gegevensbeschermingsverordening van de Europese Unie (GDPR) en de California Consumer Privacy Act (CCPA) [Regels inzake privacy en gegevensbescherming](https://developer.adobe.com/target/before-implement/privacy/cmp-privacy-and-general-data-protection-regulation/).

### optoutEnabled

* **Type**: Boolean
* **Standaardwaarde**: false
* **Beschrijving**: Geeft aan of Target de bezoeker-API moet aanroepen `isOptedOut()` functie. Dit maakt deel uit van de functie voor apparaatgrafiek.

### overrideMboxEdgeServer

* **Type**: Boolean
* **Standaardwaarde**: true (waar, vanaf at.js versie 1.6.2)
* **Beschrijving**: Geeft aan of we moeten gebruiken `<clientCode>.tt.omtrdc.net` domein of `mboxedge<clusterNumber>.tt.omtrdc.net` domein.

   Als deze waarde waar is, `mboxedge<clusterNumber>.tt.omtrdc.net` domein wordt opgeslagen in een cookie. Werken momenteel niet met [CNAME](https://developer.adobe.com/target/before-implement/implement-cname-support-in-target/) bij gebruik van at.js-versies vóór at.js 1.8.2 en at.js 2.3.1. Als dit voor u een probleem is, kunt u [bijwerken om.js](https://developer.adobe.com/target/implement/client-side/atjs/target-atjs-versions/) naar een nieuwere, ondersteunde versie.

### overrideMboxEdgeServerTimeout

* **Type**: Getal
* **Standaardwaarde**: 1860000 => 31 minuten
* **Beschrijving**: Geeft de cookielevensduur aan die de `mboxedge<clusterNumber>.tt.omtrdc.net` waarde.

### pageLoadEnabled

* **Type**: Boolean
* **Standaardwaarde**: true
* **Beschrijving**: Als deze optie is ingeschakeld, haalt u automatisch ervaringen op die bij het laden van de pagina moeten worden geretourneerd.

### secureOnly

* **Type**: Boolean
* **Standaardwaarde**: false
* **Beschrijving**: Geeft aan of at.js alleen HTTPS mag gebruiken of mag schakelen tussen HTTP en HTTPS op basis van het paginaprotocol. Wanneer ingesteld op true, stelt secureOnly ook de kenmerken Secure en SameSite in op het cookie van de box.

### selectorsPollingTimeout

* **Type**: Getal
* **Standaardwaarde**: 5000 ms = 5 s
* **Beschrijving**: In at.js 0.9.6, [!DNL Target] geïntroduceerd deze nieuwe instelling die kan worden overschreven via `targetGlobalSettings`.

   De `selectorsPollingTimeout` het plaatsen vertegenwoordigt hoe lang de cliënt bereid is om op alle die elementen te wachten door selecteurs worden geïdentificeerd om op de pagina te verschijnen.

   De activiteiten die via Visual Experience Composer (VEC) worden gecreeerd hebben aanbiedingen die selecteurs bevatten.

### serverDomain

* **Type**: String
* **Standaardwaarde**: Waarde ingesteld via UI.
* **Beschrijving**: Vertegenwoordigt de doelEdge-server.

### serverState

* **Type**: Zie [Hybride personalisatie](#server-state) hieronder.
* **Standaardwaarde**: Zie [Hybride personalisatie](#server-state) hieronder.
* **Beschrijving**: Zie [Hybride personalisatie](#server-state) hieronder.

### telemetryEnabled {#telemetry}

* **Type**: Boolean
* **Standaardwaarde**: true
* **Beschrijving**: Indien ingeschakeld, [!DNL Adobe] verzamelt het gebruik van SDK-functies en telemetriegegevens voor prestaties. Persoonlijke gegevens worden niet verzameld.

### timeout

* **Type**: Getal
* **Standaardwaarde**: Waarde ingesteld via UI.
* **Beschrijving**: Vertegenwoordigt de [!DNL Target] time-out randverzoek.

### viewsEnabled

* **Type**: Boolean
* **Standaardwaarde**: true
* **Beschrijving**: Als deze optie is ingeschakeld, haalt u automatisch de weergaven op die bij het laden van de pagina moeten worden geretourneerd. Weergaven worden ondersteund in at.js 2.*x* alleen.

### bezoekerApiTimeout

* **Type**: Getal
* **Standaardwaarde**: 2000 ms = 2 s
* **Beschrijving**: Vertegenwoordigt de [!UICONTROL Visitor API] time-out verzoek.

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
>Gegevensleveranciers vereisen [!DNL at.js] 1.3 of hoger.

De volgende video&#39;s bevatten meer informatie:

| Video | Beschrijving |
|--- |--- |
| [Gegevensleveranciers gebruiken in Adobe Target](https://helpx.adobe.com/target/kt/using/dataProviders-atjs-feature-video-use.html) | Gegevensleveranciers zijn een mogelijkheid waarmee u gegevens van derden eenvoudig aan Doel kunt doorgeven. Een derde partij zou een weerdienst, een DMP, of zelfs uw eigen Webdienst kunnen zijn. Vervolgens kunt u deze gegevens gebruiken om een publiek te maken, inhoud te benoemen en het profiel van de bezoeker te verrijken. |
| [Gegevensleveranciers implementeren in Adobe Target](https://helpx.adobe.com/target/kt/using/dataProviders-atjs-technical-video-implement.html) | Implementatiedetails en voorbeelden van het gebruik van de functie Adobe Target DataProviders om gegevens van externe gegevensleveranciers op te halen en door te geven in de aanvraag van het Doel. |

De `window.targetGlobalSettings.dataProviders` het plaatsen is een serie van gegevensleveranciers.

Elke gegevensaanbieder heeft de volgende structuur:

| Sleutel | Type | Beschrijving |
|--- |--- |--- |
| name | String | Naam van de provider. |
| versie | String | Providerversie. Deze sleutel zal voor leveranciersevolutie worden gebruikt. |
| timeout | Getal | Geeft de time-out van de provider aan als dit een netwerkaanvraag is.  Deze toets is optioneel. |
| provider | -functie | De functie die de logica voor het ophalen van providergegevens bevat.<br>De functie heeft één vereiste parameter: `callback`. De callback-parameter is een functie die alleen moet worden aangeroepen wanneer de gegevens zijn opgehaald of er een fout optreedt.<br>Callback verwacht twee parameters:<ul><li>fout: Geeft aan of er een fout is opgetreden. Als alles OK is, moet deze parameter op null worden ingesteld.</li><li>param: Een JSON-object dat de parameters vertegenwoordigt die in een doelverzoek worden verzonden.</li></ul> |

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

After at.js-processen `window.targetGlobalSettings.dataProviders`bevat het verzoek Doel een nieuwe parameter: `t1=1`.

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

After at.js-processen `window.targetGlobalSettings.dataProviders`bevat het verzoek van Doel aanvullende parameters: `t1=1`, `t2=2` en `t3=3`.

In het volgende voorbeeld worden gegevensproviders gebruikt om weergegevens in API te verzamelen en te verzenden als parameters in een aanvraag van het Doel. Het doelverzoek bevat aanvullende parameters, zoals `country` en `weatherCondition`.

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

Houd rekening met het volgende wanneer u met de `dataProviders` instellen:

* Als de gegevensleveranciers `window.targetGlobalSettings.dataProviders` asynchroon zijn, worden ze parallel uitgevoerd. De visitor-API-aanvraag wordt uitgevoerd parallel aan de functies die zijn toegevoegd aan `window.targetGlobalSettings.dataProviders` om een minimale wachttijd toe te staan.
* at.js zal niet proberen om de gegevens in het voorgeheugen onder te brengen. Als de gegevensleverancier gegevens slechts één keer haalt, zou de gegevensleverancier ervoor moeten zorgen dat de gegevens in het voorgeheugen wordt opgeslagen en, wanneer de leveranciersfunctie wordt aangehaald, de geheim voorgeheugengegevens voor de tweede aanroeping dienen.

## Beveiligingsbeleid voor inhoud {#content-security}

at.js 2.3.0+ steunt het plaatsen van de nonces van het Veiligheidsbeleid van de Inhoud op SCRIPT en STYLE markeringen die aan pagina DOM worden toegevoegd wanneer het toepassen van geleverde aanbiedingen van het Doel.

De SCRIPT- en STYLE-nonces moeten worden ingesteld in `targetGlobalSettings.cspScriptNonce` en `targetGlobalSettings.cspStyleNonce` voorafgaand aan het laden van 2.3.0+ te.js. Zie een voorbeeld hieronder:

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

Na `cspScriptNonce` en `cspStyleNonce` de instellingen worden opgegeven, stelt at.js 2.3.0+ deze als nonce-kenmerken in op alle SCRIPT- en STYLE-tags die het aan de DOM toevoegt wanneer het doel wordt toegepast.

## Hybride personalisatie {#server-state}

`serverState` is een instelling die beschikbaar is in at.js v2.2+ en die kan worden gebruikt om de paginaprestaties te optimaliseren wanneer een hybride integratie van Target wordt geïmplementeerd. Hybride integratie betekent dat u zowel at.js v2.2+ op de client-kant als de levering-API of een doel-SDK op de server-kant gebruikt om ervaringen te bieden. `serverState` geeft at.js v2.2+ de capaciteit om ervaringen direct van inhoud toe te passen die op de server wordt gehaald en aan de cliënt als deel van de pagina teruggegeven wordt.

### Voorwaarden

U moet een hybride integratie hebben van [!DNL Target].

* **Server-kant**: U moet de nieuwe [bezorgings-API](https://developers.adobetarget.com/api/delivery-api/) of [Doel-SDK&#39;s](https://developers.adobetarget.com/api/delivery-api/#section/SDKs).
* **Client-kant**: U moet [at.js versie 2.2 of hoger](https://developer.adobe.com/target/implement/client-side/atjs/target-atjs-versions/).

### Codevoorbeelden

Voor een beter begrip van hoe dit werkt, zie hieronder de codevoorbeelden die u op uw server zou hebben. De code gaat ervan uit dat u de [Doel Node.js SDK](https://github.com/adobe/target-nodejs-sdk).

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

Een monster `serverState` JSON-object voor weergaveprefetch ziet er als volgt uit:

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

Nadat de pagina in de browser is geladen, past at.js alle [!DNL Target] voorstellen van `serverState` onmiddellijk, zonder enige netwerkvraag tegen [!DNL Target] rand. Bovendien prehidt at.js alleen de DOM-elementen waarvoor [!DNL Target] aanbiedingen zijn beschikbaar op de server-kant van de inhoud die is opgehaald, en beïnvloeden zo de prestaties bij het laden van pagina&#39;s en de gebruikerservaring positief.

### Belangrijke opmerkingen

Houd rekening met het volgende wanneer u `serverState`:

* Op dit moment biedt at.js v2.2 alleen ondersteuning voor het aanbieden van ervaringen via serverState voor:

   * VEC-gemaakte activiteiten die worden uitgevoerd bij het laden van de pagina.
   * Vooraf opgehaalde weergaven.

      Bij SPA [!DNL Target] Weergaven en `triggerView()` in de API van at.js, in.js v2.2 geheime voorgeheugens de inhoud voor alle meningen die op de server worden vooraf ingesteld en past deze toe zodra elke Mening via wordt teweeggebracht `triggerView()`, opnieuw zonder om het even welke extra inhoud-haalt vraag aan Doel te vuren.

   * **Opmerking**: Op dit moment worden selectievakjes die op de server worden opgehaald, niet ondersteund in `serverState`.

* Bij toepassen `serverState `aanbiedingen, waarbij at.js `pageLoadEnabled` en `viewsEnabled` instellingen, zoals aanbiedingen voor het laden van pagina&#39;s, worden niet toegepast als de `pageLoadEnabled` instellen is false.

   Als u deze instellingen wilt inschakelen, schakelt u de schakeloptie in **[!UICONTROL Administration]> [!UICONTROL Implementation] > [!UICONTROL Edit] >[!UICONTROL Page Load Enabled]**.

   ![Instellingen voor Laden van pagina](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/assets/page-load-enabled-setting.png)

* Als u `serverState` en gebruiken `<script>` -tags in de geretourneerde inhoud, controleer of de HTML-inhoud `<\/script>` in plaats van `</script>`. Als u `</script>`, wordt de browser geïnterpreteerd `</script>` als het einde van een inline SCRIPT en kan de HTML-pagina worden verbroken.

### Aanvullende bronnen

Meer informatie over `serverState` werkt, controleer de volgende middelen:

* [Voorbeeldcode](https://github.com/Adobe-Marketing-Cloud/target-node-client-samples/tree/master/advanced-atjs-integration-serverstate).
* [Toepassing van één pagina (SPA), voorbeeldtoepassing met `serverState`](https://github.com/Adobe-Marketing-Cloud/target-node-client-samples/tree/master/react-shopping-cart-demo).
