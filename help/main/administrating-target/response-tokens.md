---
keywords: reactietokens;tokens;plugins;plug-ins;at.js;response;platform web sdk;google analytics
description: Leer hoe te om reactietokens in  [!DNL Adobe Target]  aan output-specifieke informatie voor het zuiveren en het integreren met derdehulpmiddelen te gebruiken.
title: Wat zijn reactietokens en hoe gebruik ik deze?
feature: Administration & Configuration
role: Admin
exl-id: d0c1e914-3172-466d-9721-fe0690abd30b
source-git-commit: a1617f64f0633a87ea4c1f8e5104a1d177df04e2
workflow-type: tm+mt
source-wordcount: '1622'
ht-degree: 0%

---

# Reactietokens

Met responstokens kunt u automatisch specifieke informatie over [!DNL Adobe Target] naar de webpagina van uw merk uitvoeren. Deze informatie kan details over de activiteit, de aanbieding, de ervaring, het gebruikersprofiel, geo informatie, en meer omvatten. Deze details verstrekken extra reactiegegevens om met interne of derdehulpmiddelen te delen of voor het zuiveren te gebruiken.

Met responstokens kunt u kiezen welke variabelen (in sleutelwaardeparen) u wilt gebruiken en deze vervolgens inschakelen als onderdeel van een [!DNL Target] -reactie. U laat een variabele toe gebruikend de schakelaar en de variabele wordt verzonden met [!DNL Target] reacties, die in netwerkvraag kunnen worden bevestigd. Reactietokens werken ook in de modus [!UICONTROL Preview] .

Een belangrijk verschil tussen plug-ins en responstokens is dat plug-ins JavaScript leveren aan de pagina die wordt uitgevoerd na levering. Responstkens leveren echter een object op dat vervolgens kan worden gelezen en verwerkt met behulp van gebeurtenislisteners. De responstoken-aanpak is veiliger en maakt de ontwikkeling en het onderhoud van integratie van derden eenvoudiger.

{{permissions-update}}

>[!NOTE]
>
>Responstokens zijn beschikbaar in versie 1.1 of hoger van at.js.

| Doel SDK | Voorgestelde acties |
|--- |--- |
| [ SDK van het Web van Adobe Experience Platform ](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/aep-web-sdk.html){target=_blank} | Zorg ervoor dat u Platform Web SDK versie 2.6.0 of later gebruikt. Voor informatie over het downloaden van de recentste versie van het Web SDK van het Platform, zie [ SDK ](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/installing-the-sdk.html?lang=nl-NL){target=_blank} in de *overzicht van SDK van het Web van het Platform* gids installeren. Voor informatie over nieuwe functionaliteit in elke versie van het Web SDK van het Platform, zie [ de nota&#39;s van de Versie ](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=nl-NL) in de *overzicht van SDK van het Web van het Platform* gids. |
| [ at.js ](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/at-js/how-atjs-works.html?lang=nl-NL){target=_blank} | Zorg ervoor dat u at.js versie 1.1 of later gebruikt. Voor informatie over het downloaden van de recentste versie van at.js, zie [ Download at.js ](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/deploy-at-js/implement-target-without-a-tag-manager.html?lang=nl-NL){target=_blank}. Voor informatie over nieuwe functionaliteit in elke versie van at.js, zie [ at.js de Details van de Versie ](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html?lang=nl-NL){target=_blank}.<br> Klanten die at.js gebruiken worden aangemoedigd om reactietokens te gebruiken en zich van stop-ins weg te bewegen. Sommige plug-ins die afhankelijk zijn van interne methoden die in mbox.js (nu afgekeurd) bestaan, maar niet in at.js, worden geleverd, maar mislukken. |

## Reactietokens gebruiken {#section_A9E141DDCBA84308926E68D05FD2AC62}

1. Zorg ervoor dat u Platform Web SDK versie 2.6.0 (of later) of at.js versie 1.1 (of later) gebruikt.

   Voor meer informatie:

   * **SDK van het Web van het Platform**: Zie [ SDK ](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/installing-the-sdk.html?lang=nl-NL) in de *overzicht van SDK van het Platform van het Web* gids installeren.
   * **at.js**: Zie [ Download at.js ](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/deploy-at-js/implement-target-without-a-tag-manager.html?lang=nl-NL){target=_blank}.

1. Klik in [!DNL Target] op **[!UICONTROL Administration]** > **[!UICONTROL Response Tokens]** .

1. Activeer de gewenste reactietokens, zoals `activity.id` en `offer.id` .

   De volgende parameters zijn standaard beschikbaar:

   | Type | Parameter | Notities |
   |--- |--- |--- |
   | Ingebouwde profielen | `profile.activeActivities` | Retourneert een array van de `activityIds` waarvoor de bezoeker gekwalificeerd is. Dit neemt toe naarmate gebruikers gekwalificeerd zijn. Op een pagina met twee [!DNL Target] -aanvragen die twee verschillende activiteiten uitvoeren, omvat het tweede verzoek bijvoorbeeld beide activiteiten. |
   |  | `profile.isFirstSession` | Retourneert &quot;true&quot; of &quot;false&quot;. |
   |  | `profile.isNewSession` | Retourneert &quot;true&quot; of &quot;false&quot;. |
   |  | `profile.daysSinceLastVisit` | Geeft als resultaat het aantal dagen sinds het laatste bezoek van de bezoeker. |
   |  | `profile.tntId` | Retourneert de tntID van de bezoeker |
   |  | `profile.marketingCloudVisitorId` | Retourneert de Experience Cloud Visitor-id van de bezoeker. |
   |  | `profile.thirdPartyId` | Retourneert de id van de derde partij van de bezoeker. |
   |  | `profile.categoryAffinity` | Geeft de favoriete categorie van de bezoeker. |
   |  | `profile.categoryAffinities` | Retourneert een array van de bovenste 5 categorieën van de bezoeker als tekenreeksen. |
   | Activiteit | `activity.name`<br>`activity.id`<br>`experience.name`<br>`experience.id`<br>`offer.name`<br>`offer.id` | Details van de huidige activiteit.<br> Merk op dat de waarden voor aanbiedingsparameters op het ervaringsniveau worden geëvalueerd. |
   | Geo | `geo.country`<br>`geo.countryCode`<br>`geo.state`<br>`geo.city`<br>`geo.zip`<br>`geo.dma`<br>`geo.domainName`<br>`geo.ispName`<br>`geo.connectionSpeed`<br>`geo.mobileCarrier` | Zie [ Geo ](/help/main/c-target/c-audiences/c-target-rules/geo.md) voor meer informatie over het gebruiken van geo het richten in activiteiten. |
   | De Methode van de Toewijzing van het verkeer <br> (is op [!UICONTROL Auto-Target] en [!UICONTROL Automated Personalization] slechts activiteiten van toepassing.) | `experience.trafficAllocationId` | Keert 0 terug als een bezoeker een ervaring van het zijn in &quot;controle&quot;verkeer en 1 ontving als een bezoeker een ervaring van de &quot;gerichte&quot;verkeersdistributie ontving. |
   |  | `experience.trafficAllocationType` | Retourneer &quot;besturingselement&quot; of &quot;gericht&quot;. |

   Kenmerken van gebruikersprofielen en Klantkenmerken worden ook in de lijst weergegeven.

   >[!NOTE]
   >
   >Parameters met speciale tekens worden niet in de lijst weergegeven. Alleen alfanumerieke tekens en onderstrepingstekens worden ondersteund.

1. (Voorwaardelijk) om een profielparameter als reactietoken te gebruiken, maar de parameter is niet overgegaan door een [!DNL Target] verzoek en, zo, geladen niet in [!DNL Target] UI, kunt u de [!UICONTROL Add Response Token] knoop gebruiken om het profiel aan UI toe te voegen.

   Klik op **[!UICONTROL Add Response Token]** , geef de naam van het token op en klik op **[!UICONTROL Activate]** .

1. Maak een activiteit.

## Luisteren naar reacties en reactietokens lezen

Het proces dat u gebruikt om te luisteren naar [!DNL Target] reacties en om responstokens te lezen, hangt af van het feit of u een [!DNL Platform Web SDK] - of at.js-implementatie hebt.

### ![ ](/help/main/assets/platform.png) gebruiken van de de objecten van de Handle klasse van SDK van het Web van Adobe Experience Platform[!DNL Platform Web SDK] {#platform-web-sdk}

Gebruik de Object Handle-klasse, die een metagegevensobject en een gegevensobject bevat om te luisteren naar [!DNL Target] -reacties en de reactietokens te lezen.

In het volgende reactievoorbeeld wordt een [!DNL Platform Web SDK] aangepaste gebeurtenishandler rechtstreeks aan de HTML-pagina toegevoegd (in de tabel worden de objecten in de code uitgelegd):

| Object | Informatie |
| --- | --- |
| Type - Personalization.Decision | Of de beslissing is genomen door de [!DNL Target] - of Offer Decisioning-provider. |
| DecisionProvider - TGT | TGT-[!DNL Target]. [!DNL Target] bevat de metagegevens en waarden van het reactietoken voor de pagina. |
| Meta | Metagegevens die aan de pagina worden doorgegeven. |
| Gegevens | Waarden van de metagegevens die aan de pagina zijn doorgegeven. |

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

### ![ at.js badge ](/help/main/assets/atjs.png) at.js die douanegebeurtenissen gebruiken

Het gebruik [ at.js douanegebeurtenissen ](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/functions-overview/atjs-custom-events.html?lang=nl-NL){target=_blank} om op de [!DNL Target] reactie te luisteren en de reactietokens te lezen.

In het volgende codevoorbeeld wordt een [!DNL at.js] aangepaste gebeurtenishandler rechtstreeks aan de HTML-pagina toegevoegd:

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

Responstempels kunnen alleen worden geactiveerd of gedeactiveerd door gebruikers met de rol [!DNL Target] [!UICONTROL Administrator] .

**wat gebeurt als ik [!DNL Platform Web SDK] 2.6.0 (of vroeger) in werking stel?**

U hebt geen toegang tot reactietokens.

**wat gebeurt als ik bij.js 1.0 (of vroeger) loopt?**

U ziet de reactietokens, maar at.js kan hen niet gebruiken.

**kan ik zowel [!DNL Target Classic] insteekmodules als reactietokens tezelfdertijd actief hebben?**

Plugins en reactietokens zijn parallel beschikbaar, maar de plug-ins worden in de toekomst vervangen.

**zijn reactietokens die door alle [!DNL Target] reacties of slechts door [!DNL Target] reacties worden geleverd die een activiteit leveren?**

Reactietokens worden alleen geleverd via [!DNL Target] reacties die een activiteit leveren.

**Mijn [!DNL Target Classic] plug-in bevatte JavaScript. Hoe repliceer ik zijn functionaliteit gebruikend reactietokens?**

Wanneer u naar reactietokens migreert, moet dit type JavaScript in uw codebase of oplossing voor tagbeheer worden bewaard. U kunt deze code activeren met behulp van [!DNL Platform Web SDK] - of [!DNL at.js] -aangepaste gebeurtenissen en de waarden van de reactietoken doorgeven aan uw JavaScript-functies.

**waarom toont mijn profiel/de parameter van Attributen van de Klant niet in de lijst van reactietokens?**

In [!DNL Target] worden parameters gewoonlijk elke 15 minuten vernieuwd. Deze vernieuwing is afhankelijk van de actie van de gebruiker en de gegevens worden alleen vernieuwd wanneer u de pagina voor reactietokens weergeeft. Als de parameters niet worden weergegeven in de lijst met reactietoken, heeft [!DNL Target] de gegevens nog niet vernieuwd.

Als uw parameter behalve alfanumerieke tekens of andere symbolen dan onderstrepingstekens iets anders bevat, wordt de parameter niet in de lijst weergegeven. Momenteel worden alleen alfanumerieke tekens en onderstrepingstekens ondersteund.

**levert het reactietoken nog inhoud als het een geschrapt profielmanuscript of een profielparameter gebruikt?**

De tokens van de reactie halen informatie uit gebruikersprofielen en leveren dan die informatie. Als u een profielscript of parameter verwijdert, betekent dit niet dat de gegevens uit de gebruikersprofielen zijn verwijderd. De gebruikersprofielen beschikken nog steeds over gegevens die overeenkomen met het profielscript. Het reactietoken gaat door met het leveren van de inhoud. Voor gebruikers die de informatie niet in hun profielen hebben opgeslagen, of voor nieuwe bezoekers, wordt dat token niet geleverd omdat de gegevens niet aanwezig zijn in hun profielen.

[!DNL Target] schakelt het token niet automatisch uit. Als u een profielscript verwijdert en de token niet meer wilt leveren, moet u de token zelf uitschakelen.

**ik hernoemde mijn profielmanuscript, maar waarom is het teken dat dat manuscript gebruikt nog actief met de oude naam?**

Zoals hierboven vermeld, werken responstokens aan de profielgegevens die zijn opgeslagen voor gebruikers. Ook al hebt u de naam van uw profielscript gewijzigd, gebruikers die uw website hebben bezocht, hebben de oude profielscriptwaarde opgeslagen in hun profielen. De token blijft de oude waarde ophalen die al in de gebruikersprofielen is opgeslagen. Als u nu inhoud op de nieuwe naam wilt leveren, moet u van het vorige token en knevel op het nieuwe token schakelen.

**als mijn attributen zijn veranderd, wanneer worden zij verwijderd uit de lijst?**

[!DNL Target] vernieuwt kenmerken regelmatig. Om het even welk attribuut dat niet wordt van een knevel voorzien wordt verwijderd tijdens volgende verfrist zich. Als u echter een kenmerk hebt dat is ingeschakeld en verwijderd, wordt dat script pas verwijderd uit de lijst met kenmerken nadat u het hebt uitgeschakeld. U hebt bijvoorbeeld een profielscript verwijderd dat als token is gebruikt. [!DNL Target] verwijdert alleen de in- en uitschakelkenmerken uit de lijst wanneer deze worden verwijderd of hernoemd.

## Gegevens verzenden naar Google Analytics

In de volgende secties wordt beschreven hoe u [!DNL Target] -gegevens naar Google Analytics 4 kunt verzenden. Gegevens die door responstokens worden verzonden, kunnen ook naar andere integratie van derden worden verzonden.

### ![ AEP badge ](/help/main/assets/platform.png) die gegevens naar Google Analytics via het Web SDK van het Platform verzendt

Google Analytics kan via Platform Web SDK versie 2.6.0 (of hoger) gegevens worden verzonden door de volgende code toe te voegen in de HTML-pagina.

>[!NOTE]
>
>Zorg ervoor dat het sleutelwaardepaar van het reactietoken zich onder het `alloy("sendEvent"` -object bevindt.

```javascript
<script async src="https://www.googletagmanager.com/gtag/js?id=TAG_ID"></script>
<script type="text/javascript">
    alloy("sendEvent", {
 
 
    })
    .then(({ renderedPropositions, nonRenderedPropositions }) => {
        // concatenate all the propositions
        const propositions = [...renderedPropositions, ...nonRenderedPropositions];
        // extractResponseTokens() extract the meta from item -> meta
        const tokens = extractResponseTokens(propositions);
        const activityNames = [];
        const experienceNames = [];
        const uniqueTokens = distinct(tokens);
    
    
        uniqueTokens.forEach(token => {
            activityNames.push(token["activity.name"]);
            experienceNames.push(token["experience.name"]);
        });
 
        gtag('config', 'TAG_ID');
        gtag('event', 'action_name', {'eventCategory': 'target',
            'eventAction': experienceNames, 'eventLabel': activityNames
        });
    });
</script>
```

### ![ at.js badge ](/help/main/assets/atjs.png) verzendt gegevens naar Google Analytics via at.js {#section_04AA830826D94D4EBEC741B7C4F86156}

Google Analytics kan gegevens verzenden via at.js door de volgende code toe te voegen op de HTML-pagina:

```javascript
<script async src="https://www.googletagmanager.com/gtag/js?id=TAG_ID"></script>

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

        gtag('config', 'TAG_ID');
        gtag('event', 'action_name', {'eventCategory': 'target',
            'eventAction': experienceNames, 'eventLabel': activityNames
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

### ![ at.js badge ](/help/main/assets/atjs.png) Google Analytics en het zuiveren

Met de volgende code kunt u fouten opsporen met behulp van Google Analytics:

```javascript
<script async src="https://www.googletagmanager.com/gtag/js?id=TAG_ID"></script>
  
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
  
      gtag('config', 'TAG_ID');
      gtag('event', 'action_name', {'eventCategory': 'target',
          'eventAction': experienceNames, 'eventLabel': activityNames
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
        'OfferId': token["offer.id"], 
        'OfferName': token["offer.name"], 
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

## ![ at.js ](/help/main/assets/atjs.png) de Video van de Opleiding: De Tokens van de Reactie en de Gebeurtenissen van de Douane at.js {#section_3AA0A6C8DBD94A528337A2525E3E05D5}

In de volgende video wordt uitgelegd hoe u responstokens en aangepaste gebeurtenissen at.js kunt gebruiken om profielgegevens van [!DNL Target] naar systemen van derden te delen.

>[!NOTE]
>
>De gebruikersinterface van het [!DNL Target] [!UICONTROL Administration] menu (voorheen [!UICONTROL Setup] ) is opnieuw ontworpen om betere prestaties te bieden, de vereiste onderhoudstijd bij het vrijgeven van nieuwe functies te verminderen en de gebruikerservaring in het hele product te verbeteren. De informatie in de volgende video is correct, maar de opties bevinden zich op een iets andere locatie.
>
>De video bespreekt `option.name` en `option.id` , die zijn vervangen door respectievelijk `offer.name` en `offer.id` .

>[!VIDEO](https://video.tv.adobe.com/v/23253/)
