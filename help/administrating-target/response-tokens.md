---
keywords: response tokens;tokens;plugins;plug-ins;at.js;response
description: Met responstokens kunt u automatisch Adobe Target-specifieke informatie (activiteitsgegevens, gebruikersprofielgegevens, geografische informatie enzovoort) uitvoeren voor gebruik bij foutopsporing of integratie met systemen van derden (zoals Clicktale).
title: Reactietokens in Adobe Target
feature: response tokens
translation-type: tm+mt
source-git-commit: c2769c0fcf7a05c10405ec855468c829aca785c0
workflow-type: tm+mt
source-wordcount: '1559'
ht-degree: 0%

---


# Reactietokens{#response-tokens}

Met responstokens kunt u automatisch informatie uitvoeren die specifiek is voor [!DNL Target] (activiteitsdetails, gebruikersprofielinformatie, geografische informatie enzovoort) en die u kunt gebruiken bij foutopsporing of integratie met systemen van derden (zoals Clicktale).

Met reactietokens kunt u kiezen welke variabelen u wilt gebruiken en deze vervolgens inschakelen als onderdeel van een doelreactie. Om dit te doen, laat u eenvoudig een variabele toe gebruikend de schakelaar en de variabele zal met de reacties van het Doel worden verzonden, die in netwerkvraag kunnen worden bevestigd. De tekenen van de reactie werken ook op [!UICONTROL Preview] wijze.

Een belangrijk verschil tussen insteekmodules en reactietokens is dat terwijl insteekmodules JavaScript leveren aan de pagina die wordt uitgevoerd bij levering, de reactietokens een object leveren dat vervolgens kan worden gelezen en bewerkt met behulp van gebeurtenislisteners. Zie aangepaste gebeurtenissen [](/help/c-implementing-target/c-implementing-target-for-client-side-web/atjs-custom-events.md) at.js en de voorbeelden verderop in dit artikel voor meer informatie. De aanpak van responstokens is veiliger en moet de ontwikkeling en het onderhoud van integratie van derden vergemakkelijken.

>[!NOTE]
>
>Responstempels zijn beschikbaar bij at.js 1.1 of hoger. Responstempels worden niet ondersteund met mbox.js.

| Doelbibliotheek in gebruik | Voorgestelde handelingen |
|--- |--- |
| at.js | Zorg ervoor dat u at.js versie 1.1 of later gebruikt. Voor informatie over het downloaden van de recentste versie van at.js, zie [Download bij.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/implementing-target-without-a-tag-manager.md). Voor informatie over nieuwe functionaliteit in elke versie van at.js, zie [bij.js de Details](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md)van de Versie.<br>Klanten die at.js gebruiken, worden aangeraden om reactietokens te gebruiken en zich van plug-ins af te verplaatsen. Bepaalde plug-ins die afhankelijk zijn van interne methoden die in mbox.js bestaan, maar niet in at.js, worden geleverd, maar mislukken. Zie [Beperkingen](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-target-atjs-implementation/target-atjs-limitations.md)in.js voor meer informatie. |
| mbox.js | Plugins worden ondersteund en geleverd bij het gebruik van mbox.js.<br>Klanten die mbox.js en plug-ins gebruiken, worden echter aangeraden om naar at.js en reactietokens te gaan. Voor informatie over de voordelen van het gebruiken van at.js over mbox.js, zie [bij.js Veelgestelde Vragen](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-target-atjs-faq/target-atjs-faq.md). Zie [Migreren naar at.js vanuit mbox.js voor informatie over migreren](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-target-atjs-implementation/target-migrate-atjs.md).<br>Na de veroudering van Klassiek Doel (November 2017), zou u de Zorg van de Cliënt kunnen moeten contacteren om bestaande stop- ins uit te geven of onbruikbaar te maken. Controleer de plug-ins voordat Target Classic is vervangen en schakel ongewenste plug-ins uit.<br>U kunt geen nieuwe plug-ins maken in Target Standard/Premium. Gebruik in plaats daarvan reactietokens.<br>Oude SiteCatalyst-plug-ins moeten worden uitgeschakeld en vervangen door [Adobe Analytics als de rapportbron voor Adobe Target](/help/c-integrating-target-with-mac/a4t/a4t.md) (A4T). De ttMeta-plug-in moet worden uitgeschakeld en vervangen door [Adobe Experience Cloud Debugger](https://chrome.google.com/webstore/detail/adobe-experience-cloud-de/ocdmogmohccmeicdhlhhgepeaijenapj). |

## Reactiepunten gebruiken {#section_A9E141DDCBA84308926E68D05FD2AC62}

1. Zorg ervoor dat u [!DNL at.js] versie 1.1 of hoger gebruikt.

   Zie [Downloaden op .js voor meer informatie](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/implementing-target-without-a-tag-manager.md#concept_1E1F958F9CCC4E35AD97581EFAF659E2).

1. Klik [!DNL Target]in **[!UICONTROL Administration]** > **[!UICONTROL Response Tokens]**.

   ![](assets/response_tokens-new.png)

1. Activeer de gewenste reactietokens, zoals `activity.id`, `option.id`enzovoort.

   De volgende parameters zijn standaard beschikbaar:

   | Type | Parameter | Notities |
   |--- |--- |--- |
   | Ingebouwde profielen | `profile.activeActivities` | Retourneert een array van de array waarvoor `activityIds` de bezoeker gekwalificeerd is. Dit neemt toe naarmate gebruikers gekwalificeerd zijn. Op een pagina met twee [!DNL Target] verzoeken die twee verschillende activiteiten uitvoeren, omvat het tweede verzoek bijvoorbeeld beide activiteiten. |
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
   | Verkeerstoewijzingsmethode<br>(alleen van toepassing op [!UICONTROL Auto-Target] en [!UICONTROL Automated Personalization] activiteiten.) | `experience.trafficAllocationId` | Keert 0 terug als een bezoeker een ervaring van het zijn in &quot;controle&quot;verkeer en 1 ontving als een bezoeker een ervaring van de &quot;gerichte&quot;verkeersdistributie ontving. |
   |  | `experience.trafficAllocationType` | Retourneer &quot;besturingselement&quot; of &quot;gericht&quot;. |

   Kenmerken van gebruikersprofielen en Klantkenmerken worden ook in de lijst weergegeven.

   >[!NOTE]
   >
   >Parameters met speciale tekens worden niet in de lijst weergegeven. Alleen alfanumerieke tekens en onderstrepingstekens worden ondersteund.

1. (Voorwaardelijk) als u een profielparameter als reactietoken wilt gebruiken, maar de parameter is niet overgegaan door een [!DNL Target] verzoek en, zo, heeft niet geladen in het Doel UI, kunt u de [!UICONTROL Add Response Token] knoop gebruiken om het profiel aan UI toe te voegen.

   Klik **[!UICONTROL Add Response Token]**, geef de naam van het token op en klik op **[!UICONTROL Activate]**.

   ![](assets/response_token_create.png)

1. Maak een activiteit.

Gebruik aangepaste gebeurtenissen [](/help/c-implementing-target/c-implementing-target-for-client-side-web/atjs-custom-events.md) at.js om te luisteren naar de [!DNL Target] reactie en de reactietokens te lezen.

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

De volgende instructies tonen hoe u een [!DNL at.js] aangepaste gebeurtenishandler kunt toevoegen met gebruik van Adobe Dynamic Tag Manager (DTM):

1. Meld u aan bij DTM.
1. Blader naar de juiste eigenschap.
1. Gereedschap Doel openen.

   Omdat DTM geen eigen ondersteuning biedt voor at.js, moet u de code-editor gebruiken.

1. Voeg in de code-editor de volgende code toe aan [!DNL at.js]:

   ```json
   document.addEventListener(adobe.target.event.REQUEST_SUCCEEDED, function(e) { 
     console.log("Request succeeded", e.detail); 
   });
   ```

U kunt het volgende fragment toevoegen aan de bibliotheekvoettekst [op de pagina](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/implementing-target-without-a-tag-manager.md#concept_2FA0456607D04F82B0539C5BF5309812) .js Setup als u wilt dat alles één bestand is.

```json
document.addEventListener(adobe.target.event.REQUEST_SUCCEEDED, function(e) { 
  console.log("Request succeeded", e.detail); 
});
```

## Veelgestelde vragen over responstoken {#section_3DD5F32C668246289CDF9B4CDE1F536D}

**Welke rol wordt vereist om reactietokens te activeren of te deactiveren?**

De tekenen van de reactie kunnen slechts door gebruikers met de rol van Admin van het Doel worden geactiveerd of worden gedeactiveerd.

**Wat zal er gebeuren als ik om 1.js 1.0 of lager rijd?**

U zult de reactietokens zien, maar at.js zal niet hen kunnen gebruiken.

**Wat gebeurt er als ik at.js 1.1 (of later) gebruik op sommige pagina&#39;s op mijn site maar mbox.js op andere pagina&#39;s?**

De tokens van de reactie zullen aan de Reacties van het [!DNL at.js] Doel, maar niet aan de [!DNL mbox.js] reacties worden geleverd.

**Kan ik tegelijkertijd zowel de Insteekmodules van het Doel Klassieke als reactietokens actief hebben?**

Plugins en reactietokens zijn parallel beschikbaar; insteekmodules worden in de toekomst echter afgekeurd .

**Wordt de reactietokens geleverd door alle [!DNL Target] reacties of slechts door [!DNL Target] reacties leverend een activiteit?**

Reactietokens worden alleen geleverd door middel van [!DNL Target] reacties die een activiteit leveren.

**Mijn doel-klassieke insteekmodule bevat JavaScript. Hoe repliceer ik zijn functionaliteit gebruikend reactietokens?**

Wanneer u naar reactietokens migreert, moet dit type JavaScript in uw codebase of oplossing voor tagbeheer worden bewaard. U kunt deze code activeren door [!DNL at.js] aangepaste gebeurtenissen te gebruiken en de waarden van de reactietoken door te geven aan uw JavaScript-functies.

**Waarom wordt mijn profiel/parameter van Attributen van de Klant niet getoond in de lijst van reactietokens?**

Het doel verfrist normaal om de 15 minuten parameters. Dit verfrist zich is afhankelijk van gebruikersactie en de gegevens worden verfrist slechts wanneer u de pagina van reactietokens bekijkt. Als uw parameters niet in de lijst van het reactietoken tonen, zou het kunnen omdat het Doel de gegevens nog niet heeft verfrist.

Als uw parameter behalve alfanumerieke tekens of andere symbolen dan onderstrepingstekens iets anders bevat, wordt de parameter niet in de lijst weergegeven. Momenteel worden alleen alfanumerieke tekens en onderstrepingstekens ondersteund.

**Als ik een reactietoken creeer gebruikend een profielmanuscript of een profielparameter en dan dat profielmanuscript of parameter schrapt, zal het reactietoken nog inhoud leveren?**

De tokens van de reactie halen informatie uit gebruikersprofielen en leveren dan die informatie. Als u een profielscript of parameter verwijdert, betekent dit niet dat de gegevens uit de gebruikersprofielen zijn verwijderd. De gebruikersprofielen hebben nog steeds gegevens die overeenkomen met het profielscript. Het reactietoken blijft de inhoud leveren. Voor gebruikers die de informatie niet in hun profielen hebben opgeslagen, of voor nieuwe bezoekers, zal dat token niet worden geleverd omdat de gegevens niet aanwezig zijn in hun profielen.

Doel schakelt het token niet automatisch uit. Als u een profielscript verwijdert en de token niet meer wilt leveren, moet u de token zelf uitschakelen.

**Ik heb mijn profielmanuscript anders genoemd, maar waarom is het teken dat dat manuscript gebruikt nog actief met de oude naam?**

Zoals hierboven vermeld, werken responstokens aan de profielgegevens die zijn opgeslagen voor gebruikers. Ook al hebt u de naam van uw profielscript gewijzigd, toch hebben de gebruikers die uw website hebben bezocht, de oude profielscriptwaarde opgeslagen in hun profielen en de token blijft de oude waarde ophalen die al is opgeslagen in de gebruikersprofielen. Als u nu inhoud op de nieuwe naam wilt leveren, moet u van het vorige token en knevel op het nieuwe token schakelen.

**Als mijn kenmerken zijn gewijzigd, wanneer worden ze dan uit de lijst verwijderd?**

Het doel vernieuwt kenmerken regelmatig. Om het even welk attribuut dat niet wordt van een knevel voorzien zal tijdens volgende verfrissen worden verwijderd. Als u echter een kenmerk hebt dat is ingeschakeld en verwijderd (bijvoorbeeld een profielscript dat als token is gebruikt), wordt dat script pas verwijderd uit de kenmerkenlijst als u het uitschakelt. Doel verwijdert alleen de in- en uitschakelkenmerken uit de lijst wanneer deze worden verwijderd of hernoemd.

## Gegevens naar Google Analytics verzenden via at.js {#section_04AA830826D94D4EBEC741B7C4F86156}

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

## Foutopsporing (vergelijkbaar met de ttMeta-plug-in) {#section_DB3392B6E80749C1BFB520732EDF3BCE}

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

## Trainingsvideo: Antwoordtokens en badge ![voor aangepaste gebeurtenissen bij.js](/help/assets/tutorial.png) {#section_3AA0A6C8DBD94A528337A2525E3E05D5}

Bekijk de volgende video om te leren hoe u responstokens en aangepaste gebeurtenissen at.js kunt gebruiken om profielgegevens van Target naar systemen van derden te delen.

>[!NOTE]
>
>De gebruikersinterface van het [!DNL Target] menu (voorheen [!UICONTROL Administration] [!UICONTROL Setup]) is opnieuw ontworpen om betere prestaties te bieden, de vereiste onderhoudstijd bij het vrijgeven van nieuwe functies te verminderen en de gebruikerservaring in het hele product te verbeteren. De informatie in de volgende video is over het algemeen correct. de opties kunnen zich echter op iets andere locaties bevinden . Bijgewerkte video&#39;s worden binnenkort gepost.

>[!VIDEO](https://video.tv.adobe.com/v/23253/)
