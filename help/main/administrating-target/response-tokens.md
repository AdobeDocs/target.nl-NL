---
keywords: reactietokens;tokens;plug-ins;plug-ins;at.js;response;platform, web-sdk
description: Meer informatie over het gebruik van reactietokens in [!DNL Adobe Target] aan output-specifieke informatie voor het zuiveren en het integreren met derdehulpmiddelen.
title: Wat zijn reactietokens en hoe gebruik ik deze?
feature: Administration & Configuration
role: Admin
exl-id: d0c1e914-3172-466d-9721-fe0690abd30b
source-git-commit: 791274dc320912629b9425ef400d0008e0bb086b
workflow-type: tm+mt
source-wordcount: '1662'
ht-degree: 0%

---

# Reactietokens

Met respontokens kunt u automatisch specifieke informatie uitvoeren voor [!DNL Adobe Target] op de webpagina van uw merk. Deze informatie kan details over de activiteit, de aanbieding, de ervaring, het gebruikersprofiel, geo informatie, en meer omvatten. Deze details verstrekken extra reactiegegevens om met interne of derdehulpmiddelen te delen of voor het zuiveren te gebruiken.

De tekenen van de reactie laten u kiezen welke variabelen (in zeer belangrijke waardeparen) te gebruiken en dan hen toe te laten om als deel van a worden verzonden [!DNL Target] reactie. U laat een variabele toe gebruikend de schakelaar en de variabele wordt verzonden met [!DNL Target] reacties, die in netwerkvraag kunnen worden bevestigd. Reactietokens werken ook in [!UICONTROL Preview] -modus.

Een belangrijk verschil tussen insteekmodules en reactietokens is dat insteekmodules JavaScript leveren aan de pagina die wordt uitgevoerd bij levering. Responstkens leveren echter een object op dat vervolgens kan worden gelezen en verwerkt met behulp van gebeurtenislisteners. De responstoken-aanpak is veiliger en maakt de ontwikkeling en het onderhoud van integratie van derden eenvoudiger.

>[!NOTE]
>
>Responstokens zijn beschikbaar in versie 1.1 of hoger van at.js.

| Doel-SDK | Voorgestelde acties |
|--- |--- |
| [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/aep-web-sdk.html){target=_blank} | Zorg ervoor dat u versie 2.6.0 of later van SDK van het Web van het Platform gebruikt. Voor informatie over het downloaden van de recentste versie van Platform Web SDK, zie [De SDK installeren](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/installing-the-sdk.html){target=_blank} in de *Overzicht van Platform Web SDK* hulplijn. Voor informatie over nieuwe functionaliteit in elke versie van het Web SDK van het Platform, zie [Opmerkingen bij de release](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html) in de *Overzicht van Platform Web SDK* hulplijn. |
| [at.js](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/at-js/how-atjs-works.html){target=_blank} | Zorg ervoor dat u at.js versie 1.1 of later gebruikt. Voor informatie over het downloaden van de nieuwste versie van at.js raadpleegt u [Downloaden om.js](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/deploy-at-js/implement-target-without-a-tag-manager.html?lang=en){target=_blank}. For information about new functionality in each version of at.js, see [at.js Version Details](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html){target=_blank}.<br>Klanten die at.js gebruiken, worden aangeraden om reactietokens te gebruiken en zich van plug-ins af te verplaatsen. Sommige plug-ins die afhankelijk zijn van interne methoden die in mbox.js (nu afgekeurd) bestaan, maar niet in at.js, worden geleverd, maar mislukken. |

## Reactietokens gebruiken {#section_A9E141DDCBA84308926E68D05FD2AC62}

1. Zorg ervoor dat u Platform Web SDK versie 2.6.0 (of later) of versie 1.1 (of later) gebruikt.

   Voor meer informatie:

   * **Platform Web SDK**: Zie [De SDK installeren](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/installing-the-sdk.html) in de *Overzicht van Platform Web SDK* hulplijn.
   * **at.js**: Zie [Downloaden om.js](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/deploy-at-js/implement-target-without-a-tag-manager.html){target=_blank}.

1. In [!DNL Target], klikt u op **[!UICONTROL Administration]** > **[!UICONTROL Response Tokens]**.

   ![response_tokens-new image](assets/response_tokens-new.png)

1. De gewenste reactietokens activeren, zoals `activity.id` en `offer.id`.

   De volgende parameters zijn standaard beschikbaar:

   | Type | Parameter | Notities |
   |--- |--- |--- |
   | Ingebouwde profielen | `profile.activeActivities` | Hiermee wordt een array van de `activityIds` de bezoeker is gekwalificeerd voor. Dit neemt toe naarmate gebruikers gekwalificeerd zijn. Bijvoorbeeld op een pagina met twee [!DNL Target] verzoeken om twee verschillende activiteiten te verrichten, omvat het tweede verzoek beide activiteiten. |
   |  | `profile.isFirstSession` | Retourneert &quot;true&quot; of &quot;false&quot;. |
   |  | `profile.isNewSession` | Retourneert &quot;true&quot; of &quot;false&quot;. |
   |  | `profile.daysSinceLastVisit` | Geeft als resultaat het aantal dagen sinds het laatste bezoek van de bezoeker. |
   |  | `profile.tntId` | Retourneert de tntID van de bezoeker |
   |  | `profile.marketingCloudVisitorId` | Retourneert de bezoeker-id van het Experience Cloud van de bezoeker. |
   |  | `profile.thirdPartyId` | Retourneert de id van de derde partij van de bezoeker. |
   |  | `profile.categoryAffinity` | Geeft de favoriete categorie van de bezoeker. |
   |  | `profile.categoryAffinities` | Retourneert een array van de bovenste 5 categorieën van de bezoeker als tekenreeksen. |
   | Activiteit | `activity.name`<br>`activity.id`<br>`experience.name`<br>`experience.id`<br>`offer.name`<br>`offer.id` | Details van de huidige activiteit.<br> Merk op dat de waarden voor aanbiedingsparameters op het ervaringsniveau worden geëvalueerd. |
   | Geo | `geo.country`<br>`geo.state`<br>`geo.city`<br>`geo.zip`<br>`geo.dma`<br>`geo.domainName`<br>`geo.ispName`<br>`geo.connectionSpeed`<br>`geo.mobileCarrier` | Zie [Geo](/help/main/c-target/c-audiences/c-target-rules/geo.md) voor meer informatie over het gebruik van geo - gerichte toepassingen in activiteiten . |
   | Methode voor verkeerstoewijzing<br>(Van toepassing op [!UICONTROL Auto-Target] en [!UICONTROL Automated Personalization] alleen activiteiten.) | `experience.trafficAllocationId` | Keert 0 terug als een bezoeker een ervaring van het zijn in &quot;controle&quot;verkeer en 1 ontving als een bezoeker een ervaring van de &quot;gerichte&quot;verkeersdistributie ontving. |
   |  | `experience.trafficAllocationType` | Retourneer &quot;besturingselement&quot; of &quot;gericht&quot;. |

   Kenmerken van gebruikersprofielen en Klantkenmerken worden ook in de lijst weergegeven.

   >[!NOTE]
   >
   >Parameters met speciale tekens worden niet in de lijst weergegeven. Alleen alfanumerieke tekens en onderstrepingstekens worden ondersteund.

1. (Voorwaardelijk) Een profielparameter gebruiken als reactietoken, maar de parameter is niet doorgegeven via een [!DNL Target] en heeft dus niet in de [!DNL Target] UI, kunt u gebruiken [!UICONTROL Add Response Token] om het profiel aan de gebruikersinterface toe te voegen.

   Klikken **[!UICONTROL Add Response Token]**, geef de naam van het token op en klik vervolgens op **[!UICONTROL Activate]**.

   ![response_token_image maken](assets/response_token_create.png)

1. Maak een activiteit.

## Luisteren naar reacties en reactietokens lezen

Het proces dat u gebruikt om te luisteren naar [!DNL Target] reacties en leestekens voor reacties verschillen afhankelijk van of u een [!DNL Platform Web SDK] of at.js-implementatie.

### ![Adobe Experience Platform Web SDK-badge](/help/main/assets/platform.png) [!DNL Platform Web SDK] de klasse Handle-object gebruiken {#platform-web-sdk}

Gebruik de Object Handle-klasse, die een metagegevensobject en een gegevensobject bevat om naar te luisteren [!DNL Target] reacties en lees de reactietokens.

In het volgende reactievoorbeeld wordt een [!DNL Platform Web SDK] de manager van de douanegebeurtenis direct aan de pagina van de HTML (de lijst verklaart voorwerpen die in de code worden gebruikt):

| Object | Informatie |
| --- | --- |
| Type - Personalisatie.Besluit | Of de beslissing door de [!DNL Target] of Offer decisioning provider. |
| DecisionProvider - TGT | TGT-[!DNL Target]. [!DNL Target] Hiermee geeft u de metagegevens en waarden van het reactietoken op de pagina op. |
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

### ![at.js badge](/help/main/assets/atjs.png) at.js gebruiken, aangepaste gebeurtenissen

Gebruiken [at.js, aangepaste gebeurtenissen](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/functions-overview/atjs-custom-events.html?lang=en){target=_blank} om te luisteren naar [!DNL Target] reactietokens lezen en erop reageren.

Het volgende codevoorbeeld voegt een [!DNL at.js] aangepaste gebeurtenishandler rechtstreeks naar de pagina HTML:

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

De tokens van de reactie kunnen slechts door gebruikers met worden geactiveerd of worden gedeactiveerd [!DNL Target] [!UICONTROL Administrator] rol.

**Wat gebeurt er als ik werk? [!DNL Platform Web SDK] 2.6.0 (of eerder)?**

U hebt geen toegang tot reactietokens.

**Wat gebeurt er als ik om 1.js 1.0 (of vroeger) loop?**

U ziet de reactietokens, maar at.js kan hen niet gebruiken.

**Kan ik beide hebben [!DNL Target Classic] insteekmodules en reactietokens die tegelijkertijd actief zijn?**

Plugins en reactietokens zijn parallel beschikbaar, maar de plug-ins worden in de toekomst vervangen.

**Zijn reactietokens die door allen worden geleverd [!DNL Target] reacties of alleen via [!DNL Target] reacties die een activiteit leveren?**

Reactietokens worden alleen geleverd via [!DNL Target] reacties die een activiteit leveren.

**Mijn [!DNL Target Classic] opgenomen JavaScript. Hoe repliceer ik zijn functionaliteit gebruikend reactietokens?**

Bij het migreren naar reactietokens moet dit type JavaScript in uw codebase of oplossing voor tagbeheer worden bewaard. U kunt deze code activeren met [!DNL Platform Web SDK] of [!DNL at.js] aangepaste gebeurtenissen en geef de waarden van de reactietoken door aan uw JavaScript-functies.

**Waarom wordt mijn profiel/parameter van Attributen van de Klant niet getoond in de lijst van reactietokens?**

[!DNL Target] worden parameters gewoonlijk om de 15 minuten vernieuwd. Deze vernieuwing is afhankelijk van de actie van de gebruiker en de gegevens worden alleen vernieuwd wanneer u de pagina voor reactietokens weergeeft. Als de parameters niet worden weergegeven in de lijst met responstoken, [!DNL Target] heeft de gegevens nog niet vernieuwd.

Als uw parameter behalve alfanumerieke tekens of andere symbolen dan onderstrepingstekens iets anders bevat, wordt de parameter niet in de lijst weergegeven. Momenteel worden alleen alfanumerieke tekens en onderstrepingstekens ondersteund.

**Levert het reactietoken nog inhoud als het een geschrapt profielmanuscript of een profielparameter gebruikt?**

De tokens van de reactie halen informatie uit gebruikersprofielen en leveren dan die informatie. Als u een profielscript of parameter verwijdert, betekent dit niet dat de gegevens uit de gebruikersprofielen zijn verwijderd. De gebruikersprofielen beschikken nog steeds over gegevens die overeenkomen met het profielscript. Het reactietoken gaat door met het leveren van de inhoud. Voor gebruikers die de informatie niet in hun profielen hebben opgeslagen, of voor nieuwe bezoekers, wordt dat token niet geleverd omdat de gegevens niet aanwezig zijn in hun profielen.

[!DNL Target] schakelt het token niet automatisch uit. Als u een profielscript verwijdert en de token niet meer wilt leveren, moet u de token zelf uitschakelen.

**Ik heb mijn profielmanuscript anders genoemd, maar waarom is het teken dat dat manuscript gebruikt nog actief met de oude naam?**

Zoals hierboven vermeld, werken responstokens aan de profielgegevens die zijn opgeslagen voor gebruikers. Ook al hebt u de naam van uw profielscript gewijzigd, gebruikers die uw website hebben bezocht, hebben de oude profielscriptwaarde opgeslagen in hun profielen. De token blijft de oude waarde ophalen die al in de gebruikersprofielen is opgeslagen. Als u nu inhoud op de nieuwe naam wilt leveren, moet u van het vorige token en knevel op het nieuwe token schakelen.

**Als mijn kenmerken zijn gewijzigd, wanneer worden ze dan uit de lijst verwijderd?**

[!DNL Target] vernieuwt kenmerken regelmatig. Om het even welk attribuut dat niet wordt van een knevel voorzien wordt verwijderd tijdens volgende verfrist zich. Als u echter een kenmerk hebt dat is ingeschakeld en verwijderd, wordt dat script pas verwijderd uit de lijst met kenmerken nadat u het hebt uitgeschakeld. U hebt bijvoorbeeld een profielscript verwijderd dat als token is gebruikt. [!DNL Target] Hiermee verwijdert u alleen de in- en uitschakelkenmerken uit de lijst wanneer deze worden verwijderd of hernoemd.

## Gegevens verzenden naar Googles Analytics

In de volgende secties wordt beschreven hoe u kunt verzenden [!DNL Target] gegevens aan Googles Analytics. Gegevens die door responstokens worden verzonden, kunnen ook naar andere integratie van derden worden verzonden.

### ![AEP-badge](/help/main/assets/platform.png) Gegevens verzenden naar Googles Analytics via Platform Web SDK

Googles Analytics kunnen gegevens via Versie 2.6.0 van SDK van het Web van het Platform (of recenter) worden verzonden door de volgende code in de pagina van de HTML toe te voegen.

>[!NOTE]
>
>Zorg ervoor dat het sleutelwaardepaar van het reactietoken zich onder de `alloy("sendEvent"` object.

```
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
   
   
   ga('send', 'event', { 
   eventCategory: "target", 
   eventAction: experienceNames, 
   eventLabel: activityNames 
   }); 
   
   
   });
</script>
```

### ![at.js badge](/help/main/assets/atjs.png) Gegevens naar Googles Analytics verzenden via at.js {#section_04AA830826D94D4EBEC741B7C4F86156}

Googles Analytics kunnen via at.js gegevens worden verzonden door de volgende code op de pagina HTML toe te voegen:

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

### ![at.js badge](/help/main/assets/atjs.png) Googles Analytics en foutopsporing

Met de volgende code kunt u fouten opsporen met behulp van Googles Analytics:

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

Het equivalent van de ttMeta-plug-in voor foutopsporingsdoeleinden kan worden gemaakt door de volgende code toe te voegen aan de HTML-pagina:

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

## ![at.js](/help/main/assets/atjs.png) Trainingsvideo: respontokens en aangepaste gebeurtenissen at.js {#section_3AA0A6C8DBD94A528337A2525E3E05D5}

In de volgende video wordt uitgelegd hoe u responstokens en aangepaste gebeurtenissen at.js kunt gebruiken om profielgegevens te delen van [!DNL Target] naar systemen van derden.

>[!NOTE]
>
>De [!DNL Target] [!UICONTROL Administration] menu-interface (voorheen [!UICONTROL Setup]) is opnieuw ontworpen om betere prestaties te bieden, de vereiste onderhoudstijd bij het vrijgeven van nieuwe functies te verminderen en de gebruikerservaring in het hele product te verbeteren. De informatie in de volgende video is correct, maar de opties bevinden zich op een iets andere locatie.
>
>In de video wordt gesproken over `option.name` en `option.id`, die zijn vervangen door `offer.name` en `offer.id`, respectievelijk.

>[!VIDEO](https://video.tv.adobe.com/v/23253/)
