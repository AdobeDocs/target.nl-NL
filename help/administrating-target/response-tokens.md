---
keywords: reactietokens;tokens;plug-ins;plug-ins;at.js;response
description: Leer hoe te om reactietokens in Adobe [!DNL Target] output-specifieke informatie te gebruiken in het zuiveren en het integreren met derdesystemen (zoals Clicktale).
title: Wat zijn reactietokens en hoe gebruik ik deze?
feature: Beheer en configuratie
role: Administrator
exl-id: d0c1e914-3172-466d-9721-fe0690abd30b
source-git-commit: d1579a56e46b806c3e4a0cb1748e5682b0900d11
workflow-type: tm+mt
source-wordcount: '1581'
ht-degree: 0%

---

# Reactietokens

Met responstokens kunt u automatisch specifieke informatie voor [!DNL Adobe Target] uitvoeren op de webpagina van uw merk. Deze informatie kan details over de activiteit, de aanbieding, de ervaring, het gebruikersprofiel, geo informatie, en meer omvatten. Deze details verstrekken extra reactiegegevens om met interne of derdehulpmiddelen te delen of voor het zuiveren te gebruiken.

De tekenen van de reactie laten u kiezen welke variabelen (in zeer belangrijke waardeparen) te gebruiken en dan hen toe te laten om als deel van een [!DNL Target] reactie worden verzonden. U laat een variabele toe gebruikend de schakelaar en de variabele wordt verzonden met [!DNL Target] reacties, die in netwerkvraag kunnen worden bevestigd. De tekenen van de reactie werken ook op [!UICONTROL Preview] wijze.

Een belangrijk verschil tussen insteekmodules en reactietokens is dat insteekmodules JavaScript leveren aan de pagina die wordt uitgevoerd bij levering. Responstkens leveren echter een object op dat vervolgens kan worden gelezen en verwerkt met behulp van gebeurtenislisteners. De responstoken-aanpak is veiliger en maakt de ontwikkeling en het onderhoud van integratie van derden eenvoudiger.

>[!NOTE]
>
>Responstkens zijn beschikbaar in [!DNL Adobe Experience Platform Web SDK] versie 2.5.0 of hoger (release gepland voor 1 juni 2021) en met versie 1.1 of hoger op at.js.

| Doel-SDK | Voorgestelde acties |
|--- |--- |
| [Adobe Experience Platform Web SDK](/help/c-implementing-target/c-implementing-target-for-client-side-web/aep-web-sdk.md) | Zorg ervoor dat u versie 2.5.0 of later van SDK van het Web van het Platform gebruikt. Voor informatie over het downloaden van de recentste versie van het Web SDK van het Platform, zie [SDK installeren](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/installing-the-sdk.html) in *Overzicht SDK van het Web SDK van het Platform* gids. Voor informatie over nieuwe functionaliteit in elke versie van het Web SDK van het Platform, zie [Nota&#39;s van de Versie](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html) in *Overzicht van SDK van het Web van het Platform* gids. |
| [at.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/how-atjs-works.md) | Zorg ervoor dat u at.js versie 1.1 of later gebruikt. Voor informatie over het downloaden van de recentste versie van at.js, zie [Download bij.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/implementing-target-without-a-tag-manager.md). Voor informatie over nieuwe functionaliteit in elke versie van at.js, zie [at.js de Details van de Versie](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md).<br>Klanten die at.js gebruiken, worden aangeraden om reactietokens te gebruiken en zich van plug-ins af te verplaatsen. Sommige plug-ins die afhankelijk zijn van interne methoden die in mbox.js bestaan, maar niet in at.js, worden geleverd, maar mislukken. Voor meer informatie, zie [at.js Beperkingen](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-target-atjs-implementation/target-atjs-limitations.md). |

## Reactietokens gebruiken {#section_A9E141DDCBA84308926E68D05FD2AC62}

1. Zorg ervoor dat u Platform Web SDK versie 2.5.0 (of later) of versie 1.1 (of later) gebruikt.

   Voor meer informatie:

   * **Platform Web SDK**: Zie  [Installeer ](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/installing-the-sdk.html) SDK in de  *Platform SDK* overviewguide.
   * **at.js**: Zie  [Downloaden om.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/implementing-target-without-a-tag-manager.md#concept_1E1F958F9CCC4E35AD97581EFAF659E2).

1. Klik in [!DNL Target] op **[!UICONTROL Administration]** > **[!UICONTROL Response Tokens]**.

   ![](assets/response_tokens-new.png)

1. Activeer de gewenste reactietokens, zoals `activity.id` en `option.id`.

   De volgende parameters zijn standaard beschikbaar:

   | Type | Parameter | Notities |
   |--- |--- |--- |
   | Ingebouwde profielen | `profile.activeActivities` | Retourneert een array van de `activityIds` waarvoor de bezoeker gekwalificeerd is. Dit neemt toe naarmate gebruikers gekwalificeerd zijn. Op een pagina met twee [!DNL Target] verzoeken die twee verschillende activiteiten leveren, omvat het tweede verzoek bijvoorbeeld beide activiteiten. |
   |  | `profile.isFirstSession` | Retourneert &quot;true&quot; of &quot;false&quot;. |
   |  | `profile.isNewSession` | Retourneert &quot;true&quot; of &quot;false&quot;. |
   |  | `profile.daysSinceLastVisit` | Geeft als resultaat het aantal dagen sinds het laatste bezoek van de bezoeker. |
   |  | `profile.tntId` | Retourneert de tntID van de bezoeker |
   |  | `profile.marketingCloudVisitorId` | Retourneert de Experience Cloud Bezoeker-id van de bezoeker. |
   |  | `profile.thirdPartyId` | Retourneert de id van de derde partij van de bezoeker. |
   |  | `profile.categoryAffinity` | Geeft de favoriete categorie van de bezoeker. |
   |  | `profile.categoryAffinities` | Retourneert een array van de bovenste 5 categorieën van de bezoeker als tekenreeksen. |
   | Activiteit | `activity.name`<br>`activity.id`<br>`experience.name`<br>`experience.id`<br>`option.name`<br>`option.id` | Details van de huidige activiteit. Merk op dat &quot;optie&quot;&quot;voorstel&quot;evenaart. |
   | Geo | `geo.country`<br>`geo.state`<br>`geo.city`<br>`geo.zip`<br>`geo.dma`<br>`geo.domainName`<br>`geo.ispName`<br>`geo.connectionSpeed`<br>`geo.mobileCarrier` | Zie [Geo](/help/c-target/c-audiences/c-target-rules/geo.md) voor meer informatie over het gebruiken van geo richten in activiteiten. |
   | Verkeerstoewijzingsmethode<br>(alleen van toepassing op [!UICONTROL Auto-Target]- en [!UICONTROL Automated Personalization]-activiteiten.) | `experience.trafficAllocationId` | Keert 0 terug als een bezoeker een ervaring van het zijn in &quot;controle&quot;verkeer en 1 ontving als een bezoeker een ervaring van de &quot;gerichte&quot;verkeersdistributie ontving. |
   |  | `experience.trafficAllocationType` | Retourneer &quot;besturingselement&quot; of &quot;gericht&quot;. |

   Kenmerken van gebruikersprofielen en Klantkenmerken worden ook in de lijst weergegeven.

   >[!NOTE]
   >
   >Parameters met speciale tekens worden niet in de lijst weergegeven. Alleen alfanumerieke tekens en onderstrepingstekens worden ondersteund.

1. (Voorwaardelijk) om een profielparameter als reactietoken te gebruiken, maar de parameter is niet overgegaan door een [!DNL Target] verzoek en, zo, heeft niet geladen in [!DNL Target] UI, kunt u [!UICONTROL Add Response Token] knoop gebruiken om het profiel aan UI toe te voegen.

   Klik **[!UICONTROL Add Response Token]**, verstrek de symbolische naam, dan klik **[!UICONTROL Activate]**.

   ![](assets/response_token_create.png)

1. Maak een activiteit.

## Luisteren naar reacties en reactietokens lezen

Het proces dat u gebruikt om te luisteren naar [!DNL Target] reacties en om reactietokens te lezen, is afhankelijk van het feit of u een [!DNL Platform Web SDK]- of at.js-implementatie hebt.

### ![Adobe Experience Platform Web SDK-](/help/assets/platform.png) [!DNL Platform Web SDK] badge met de Handle-objectklasse

Gebruik de klasse van het voorwerp van de Handle, die een meta- gegevensvoorwerp en een gegevensvoorwerp heeft om op [!DNL Target] reacties te luisteren en de reactietokens te lezen.

In het volgende codevoorbeeld wordt een aangepaste gebeurtenishandler [!DNL Platform Web SDK] rechtstreeks aan de HTML-pagina toegevoegd:

```html
<html>

<head>
 ...
 <script src="alloy.js"></script>
 <script>
  {
   "requestId": "4d0a7cfd-952c-408c-b3b8-438edc38250a",
   "handle": [{
    "type": "personalization:decisions",
    "payload": [{
     "id": "....",
     "scope": "__view__",
     "scopeDetails": {
      "decisionProvider": "TGT",
      "activity": {
       "id": "..."
      },
      "experience": {
       "id": "...."
      }
     },
     "items": [{
      "id": "123",
      "schema": "https://ns.adobe.com/personalization/dom-action",
      "meta": {
       "activity.id": "...",
       "activity.name": "...",
       "profile.foo": "...",
       "profile.bar": "..."
      },
      "data": {
       "id": "123",
       "type": "setHtml",
       "selector": "#foo",
       "prehidingSelector": "#foo",
       "content": "<div>Hello world</div>"
      }
     }]
    }]
   }]
  }
  });
 </script>
</head>

<body>
 ...
</body>

</html>
```

| Object | Informatie |
| --- | --- |
| Type - Personalisatie.Besluit | [!DNL Target] en hier worden de gegevens van de Offer decisioning doorgegeven. |
| DecisionProvider - TGT | TGT-[!DNL Target]. [!DNL Target] Hiermee geeft u de metagegevens en waarden van het reactietoken op de pagina op. |
| Meta | Metagegevens die worden doorgegeven aan de pagina. |
| Gegevens | Waarden van de metagegevens die aan de pagina zijn doorgegeven. |

### ![at.js ](/help/assets/atjs.png) badgeat.js die aangepaste gebeurtenissen gebruiken

Gebruik [at.js aangepaste gebeurtenissen](/help/c-implementing-target/c-implementing-target-for-client-side-web/atjs-custom-events.md) om te luisteren naar de [!DNL Target]-reactie en de reactietokens te lezen.

In het volgende codevoorbeeld wordt een aangepaste gebeurtenishandler [!DNL at.js] rechtstreeks aan de HTML-pagina toegevoegd:

```html
<html> 
  <head> 
    .... 
    <script src="at.js"></script> 
    <script> 
      document.addEventListener(adobe.target.event.REQUEST_SUCCEEDED, function(e) { 
        console.log("Request succeeded", e.detail); 
      }); 
    </script> 
  <head> 
  <body> 
  ... 
  </body> 
</html>
```

## Veelgestelde vragen over antwoordtoken {#section_3DD5F32C668246289CDF9B4CDE1F536D}

**Welke rol wordt vereist om reactietokens te activeren of te deactiveren?**

De tekenen van de reactie kunnen slechts door gebruikers met de [!DNL Target] [!UICONTROL Administrator] rol worden geactiveerd of worden gedeactiveerd.

**Wat gebeurt er als ik [!DNL Platform Web SDK] 2.5.0 (of eerder) in werking stel?

U hebt geen toegang tot reactietokens.

**Wat gebeurt er als ik om 1.js 1.0 (of vroeger) loop?**

U ziet de reactietokens, maar at.js kan hen niet gebruiken.

**Kan ik tegelijkertijd zowel  [!DNL Target Classic] insteekmodules als reactietokens actief hebben?**

Plug-ins en reactietokens zijn parallel beschikbaar; insteekmodules worden in de toekomst echter afgekeurd .

**Wordt de reactietokens geleverd door alle  [!DNL Target] reacties of slechts door  [!DNL Target] reacties leverend een activiteit?**

De tekenen van de reactie worden geleverd slechts door [!DNL Target] reacties leverend een activiteit.

**Mijn  [!DNL Target Classic] insteekmodule bevat JavaScript. Hoe repliceer ik zijn functionaliteit gebruikend reactietokens?**

Bij het migreren naar reactietokens moet dit type JavaScript in uw codebase of oplossing voor tagbeheer worden bewaard. U kunt deze code activeren met behulp van aangepaste gebeurtenissen [!DNL Platform Web SDK] of [!DNL at.js] en de waarden van de reactietoken doorgeven aan uw JavaScript-functies.

**Waarom wordt mijn profiel/parameter van Attributen van de Klant niet getoond in de lijst van reactietokens?**

[!DNL Target] worden parameters gewoonlijk om de 15 minuten vernieuwd. Deze vernieuwing is afhankelijk van de actie van de gebruiker en de gegevens worden alleen vernieuwd wanneer u de pagina voor reactietokens weergeeft. Als uw parameters niet in de lijst van het reactietoken tonen, [!DNL Target] heeft nog niet verfrist de gegevens.

Als uw parameter behalve alfanumerieke tekens of andere symbolen dan onderstrepingstekens iets anders bevat, wordt de parameter niet in de lijst weergegeven. Momenteel worden alleen alfanumerieke tekens en onderstrepingstekens ondersteund.

**Levert het reactietoken nog inhoud als het een geschrapt profielmanuscript of een profielparameter gebruikt?**

De tokens van de reactie halen informatie uit gebruikersprofielen en leveren dan die informatie. Als u een profielscript of parameter verwijdert, betekent dit niet dat de gegevens uit de gebruikersprofielen zijn verwijderd. De gebruikersprofielen beschikken nog steeds over gegevens die overeenkomen met het profielscript. Het reactietoken gaat door met het leveren van de inhoud. Voor gebruikers die de informatie niet in hun profielen hebben opgeslagen, of voor nieuwe bezoekers, wordt dat token niet geleverd omdat de gegevens niet aanwezig zijn in hun profielen.

[!DNL Target] schakelt het token niet automatisch uit. Als u een profielscript verwijdert en de token niet meer wilt leveren, moet u de token zelf uitschakelen.

**Ik heb mijn profielmanuscript anders genoemd, maar waarom is het teken dat dat manuscript gebruikt nog actief met de oude naam?**

Zoals hierboven vermeld, werken responstokens aan de profielgegevens die zijn opgeslagen voor gebruikers. Ook al hebt u de naam van uw profielscript gewijzigd, gebruikers die uw website hebben bezocht, hebben de oude profielscriptwaarde opgeslagen in hun profielen. De token blijft de oude waarde ophalen die al in de gebruikersprofielen is opgeslagen. Als u nu inhoud op de nieuwe naam wilt leveren, moet u van het vorige token en knevel op het nieuwe token schakelen.

**Als mijn kenmerken zijn gewijzigd, wanneer worden ze dan uit de lijst verwijderd?**

[!DNL Target] vernieuwt kenmerken regelmatig. Om het even welk attribuut dat niet wordt van een knevel voorzien wordt verwijderd tijdens volgende verfrist zich. Als u echter een kenmerk hebt dat is ingeschakeld en verwijderd, wordt dat script pas verwijderd uit de lijst met kenmerken nadat u het hebt uitgeschakeld. U hebt bijvoorbeeld een profielscript verwijderd dat als token is gebruikt. [!DNL Target] Hiermee verwijdert u alleen de in- en uitschakelkenmerken uit de lijst wanneer deze worden verwijderd of hernoemd.

## Gegevens verzenden naar Google Analytics

In de volgende secties wordt beschreven hoe u [!DNL Target]-gegevens naar Google Analytics verzendt:

### ![AEP ](/help/assets/platform.png) badgeSending data to Google Analytics via Platform Web SDK

Google Analytics kunnen via Platform Web SDK versie 2.5.0 (of later) gegevens worden verzonden door de volgende code in de HTML-pagina toe te voegen:

(Te ontvangen code)

### ![at.js ](/help/assets/atjs.png) badgeGegevens worden naar Google Analytics verzonden via at.js {#section_04AA830826D94D4EBEC741B7C4F86156}

Google Analytics kunnen via at.js gegevens worden verzonden door de volgende code toe te voegen in de HTML-pagina:

```javascript
<script type="text/javascript"> 
  (function(i, s, o, g, r, a, m) { 
    i['GoogleAnalyticsObject'] = r; 
    i[r] = i[r] || function() { 
      (i[r].q = i[r].q || []).push(arguments) 
    }, i[r].l = 1 * new Date(); 
    a = s.createElement(o), 
      m = s.getElementsByTagName(o)[0]; 
    a.async = 1; 
    a.src = g; 
    m.parentNode.insertBefore(a, m) 
  })(window, document, 'script', 'https://www.google-analytics.com/analytics.js', 'ga'); 
  ga('create', 'Google Client Id', 'auto'); 
</script> 
 
<script type="text/javascript"> 
  document.addEventListener(adobe.target.event.REQUEST_SUCCEEDED, function(e) { 
    var tokens = e.detail.responseTokens; 
 
    if (isEmpty(tokens)) { 
      return; 
    } 
 
    var activityNames = []; 
    var experienceNames = []; 
    var uniqueTokens = distinct(tokens); 
 
    uniqueTokens.forEach(function(token) { 
      activityNames.push(token["activity.name"]); 
      experienceNames.push(token["experience.name"]); 
    }); 
 
    ga('send', 'event', { 
      eventCategory: "target", 
      eventAction: experienceNames, 
      eventLabel: activityNames 
    }); 
  }); 
 
  function isEmpty(val) { 
    return (val === undefined || val == null || val.length <= 0) ? true : false; 
  } 
 
  function key(obj) { 
     return Object.keys(obj) 
    .map(function(k) { return k + "" + obj[k]; }) 
    .join(""); 
  } 
 
  function distinct(arr) { 
    var result = arr.reduce(function(acc, e) { 
      acc[key(e)] = e; 
      return acc; 
    }, {}); 
   
    return Object.keys(result) 
    .map(function(k) { return result[k]; }); 
  } 
</script>
```

## Foutopsporing

De volgende secties verstrekken informatie over het zuiveren reactietokens:

### ![at.js ](/help/assets/atjs.png) badgeGoogle Analytics en foutopsporing

Met de volgende code kunt u fouten opsporen met behulp van Google Analytics:

```javascript
<script type="text/javascript"> 
  (function(i, s, o, g, r, a, m) { 
    i['GoogleAnalyticsObject'] = r; 
    i[r] = i[r] || function() { 
      (i[r].q = i[r].q || []).push(arguments) 
    }, i[r].l = 1 * new Date(); 
    a = s.createElement(o), 
      m = s.getElementsByTagName(o)[0]; 
    a.async = 1; 
    a.src = g; 
    m.parentNode.insertBefore(a, m) 
  })(window, document, 'script', 'https://www.google-analytics.com/analytics.js', 'ga'); 
  ga('create', 'Google Client Id', 'auto'); 
</script> 
 
<script type="text/javascript"> 
  document.addEventListener(adobe.target.event.REQUEST_SUCCEEDED, function(e) { 
    var tokens = e.detail.responseTokens; 
 
    if (isEmpty(tokens)) { 
      return; 
    } 
 
    var activityNames = []; 
    var experienceNames = []; 
    var uniqueTokens = distinct(tokens); 
 
    uniqueTokens.forEach(function(token) { 
      activityNames.push(token["activity.name"]); 
      experienceNames.push(token["experience.name"]); 
    }); 
 
    ga('send', 'event', { 
      eventCategory: "target", 
      eventAction: experienceNames, 
      eventLabel: activityNames 
    }); 
  }); 
 
  function isEmpty(val) { 
    return (val === undefined || val == null || val.length <= 0) ? true : false; 
  } 
 
  function key(obj) { 
     return Object.keys(obj) 
    .map(function(k) { return k + "" + obj[k]; }) 
    .join(""); 
  } 
 
  function distinct(arr) { 
    var result = arr.reduce(function(acc, e) { 
      acc[key(e)] = e; 
      return acc; 
    }, {}); 
   
    return Object.keys(result) 
    .map(function(k) { return result[k]; }); 
  } 
```

### Foutopsporing met het equivalent van de ttMeta-plug-in

Het equivalent van de ttMeta-insteekmodule voor foutopsporingsdoeleinden kan worden gemaakt door de volgende code toe te voegen aan de HTML-pagina:

```javascript
<script type="text/javascript" > 
  document.addEventListener(adobe.target.event.REQUEST_SUCCEEDED, function (e) { 
    window.ttMETA= typeof(window.ttMETA)!="undefined" ? window.ttMETA : []; 
 
    var tokens=e.detail.responseTokens; 
 
    if (isEmpty(tokens)) { 
      return; 
    } 
     
    var uniqueTokens = distinct(tokens); 
 
    uniqueTokens.forEach(function(token) { 
      window.ttMETA.push({ 
        'CampaignName': token["activity.name"], 
        'CampaignId' : token["activity.id"], 
        'RecipeName': token["experience.name"], 
        'RecipeId': token["experience.id"], 
        'OfferId': token["option.id"], 
        'OfferName': token["option.name"], 
        'MboxName': e.detail.mbox}); 
      console.log(ttMETA); 
    }); 
  }); 
 
  function isEmpty(val){ 
    return (val === undefined || val == null || val.length <= 0) ? true : false; 
  } 
 
  function key(obj) { 
     return Object.keys(obj) 
    .map(function(k) { return k + "" + obj[k]; }) 
    .join(""); 
  } 
 
  function distinct(arr) { 
    var result = arr.reduce(function(acc, e) { 
      acc[key(e)] = e; 
      return acc; 
    }, {}); 
   
    return Object.keys(result) 
    .map(function(k) { return result[k]; }); 
  } 
</script>
```

## ![at.](/help/assets/atjs.png) jsTraining Video: Response Tokens en aangepaste gebeurtenissen at.js {#section_3AA0A6C8DBD94A528337A2525E3E05D5}

In de volgende video wordt uitgelegd hoe u responstokens en aangepaste gebeurtenissen at.js kunt gebruiken om profielgegevens te delen van [!DNL Target] naar systemen van derden.

>[!NOTE]
>
>De [!DNL Target] [!UICONTROL Administration] menu-interface (voorheen [!UICONTROL Setup]) is opnieuw ontworpen om betere prestaties te bieden, de vereiste onderhoudstijd bij het vrijgeven van nieuwe functies te verminderen en de gebruikerservaring in het hele product te verbeteren. De informatie in de volgende video is correct. de opties bevinden zich echter op een iets andere locatie .

>[!VIDEO](https://video.tv.adobe.com/v/23253/)
