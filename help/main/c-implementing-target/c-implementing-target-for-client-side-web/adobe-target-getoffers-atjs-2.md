---
keywords: adobe.target.getOffers;getOffers;getoffers;get aanbiedingen;at.js;functies;function
description: Gebruik de functie adobe.target.getOffers() en de bijbehorende opties voor de Adobe [!DNL Target] at.js-bibliotheek om aanvragen in te dienen voor het ophalen van meerdere [!DNL Target] voorstellen. (om 2.x.js)
title: Hoe gebruik ik de functie adobe.target.getOffers()?
feature: at.js
role: Developer
exl-id: ed5f06c8-d837-4ea1-a857-c6c46424aa1f
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '1314'
ht-degree: 0%

---

# adobe.target.getOffers() - at.js 2.x

Deze functie laat u veelvoudige aanbiedingen terugwinnen door in veelvoudige dozen over te gaan. Bovendien kunnen meerdere aanbiedingen worden opgehaald voor alle weergaven in actieve activiteiten.

>[!NOTE]
>
>Deze functie is geïntroduceerd met at.js 2.x. Deze functie is niet beschikbaar voor versie 1 van at.js.*x*.

| Sleutel | Type | Vereist? | Beschrijving |
| --- | --- | --- | --- |
| `consumerId` | String | Nee | De standaardwaarde is het globale mbox van de cliënt als niet verstrekt. Deze sleutel wordt gebruikt om de supplementaire gegevens ID (SDID) te produceren die voor integratie A4T wordt gebruikt.<br>Wanneer u `getOffers()`, produceert elke vraag een nieuwe SDID. Als er meerdere box-aanvragen op dezelfde pagina staan en u wilt de SDID behouden (zodat deze overeenkomt met de SDID van de target-global-mbox en de Adobe Analytics SDID), gebruikt u de `consumerId` parameter.<br>Indien `getOffers()` omvat drie vakken (genaamd &quot;mbox1&quot;, &quot;mbox2&quot; en &quot;mbox3&quot;): `consumerId: "mbox1, mbox2, mbox3"` in de `getOffers()` vraag. |
| `decisioningMethod` | String | Nee | &quot;server-side&quot;, &quot;on-device&quot;, &quot;hybride&quot; |
| `request` | Object | Ja | Zie onderstaande tabel Verzoeken. |
| `timeout` | Getal | Nee | Verzoek time-out. Als deze niet is opgegeven, wordt de standaardtime-out at.js gebruikt. |

## Verzoek

>[!NOTE]
>
>Raadpleeg de [Leverings-API-documentatie](https://developers.adobetarget.com/api/delivery-api/#tag/Delivery-API) voor informatie over de acceptabele typen voor alle onderstaande velden.

| Veldnaam | Vereist? | Beperkingen | Beschrijving |
| --- | --- | --- | --- |
| request > id | Nee |  | Eén van `tntId`, `thirdPartyId`, of `marketingCloudVisitorId` is vereist. |
| Request > id > thirdPartyId | Nee | Maximale grootte = 128. |  |  |
| Verzoek > ExperienceCloud | Nee |  |  |
| Request > ExperienceCloud > Analytics | Nee |  | Adobe Analytics-integratie |
| Request > ExperienceCloud > Analytics > logging | Nee | Het volgende moet op pagina worden geïmplementeerd:<ul><li>Bezoekersidentiteitsservice</li><li>Appmeasurement.js</li></ul> | De volgende waarden worden ondersteund:<br>**client_side**: Wanneer gespecificeerd, zal een analytische lading aan de bezoeker worden teruggegeven die zou moeten worden gebruikt om naar Adobe Analytics via de Invoeging API van Gegevens te verzenden.<br>**server_side**: Dit is de standaardwaarde waar het doel en de achtergrond van Analytics SDID zullen gebruiken om de vraag voor rapporteringsdoeleinden samen te binden. |
| Verzoek > prefetch | Nee |  |  |
| Verzoek > Prefetch > views | Nee | Maximaal aantal 50.<br>Naam niet leeg.<br>Naam lengte `<=` 128.<br>Waarde lengte `<=` 5000.<br>De naam mag niet beginnen met &quot;profiel&quot;.<br>Namen niet toegestaan: &quot;orderId&quot;, &quot;orderTotal&quot;, &quot;productPurchasedId&quot;. | Geef parameters door die moeten worden gebruikt om relevante weergaven in actieve activiteiten op te halen. |
| Request > prefetch > views > profileParameters | Nee | Maximumaantal 50.<br>Naam niet leeg.<br>Naam lengte `<=` 128.<br>Waarde lengte `<=` 5000.<br>Accepteert alleen tekenreekswaarden.<br>De naam mag niet beginnen met &quot;profiel&quot;. | Geef profielparameters door die moeten worden gebruikt om relevante weergaven in actieve activiteiten op te halen. |
| Request > prefetch > views > product | Nee |  |  |
| Request > prefetch > views > product -> id | Nee | Niet leeg.<br>maximale grootte = 128. | Geef de product-id&#39;s door die moeten worden gebruikt om relevante weergaven in actieve activiteiten op te halen. |
| Request > prefetch > views > product > categoryId | Nee | Niet leeg.<br>maximale grootte = 128. | Geef de id&#39;s van de productcategorie door die moeten worden gebruikt om relevante weergaven in activiteiten op te halen. |
| Request > prefetch > views > order | Nee |  |  |
| Request > prefetch > views > order > id | Nee | Maximumlengte = 250. | Geef dit door zodat id&#39;s kunnen worden gebruikt om relevante weergaven in actieve activiteiten op te halen. |
| Verzoek > Prefetch > views > order > total | Nee | Totaal `>=` 0. | Geef de totalen door die moeten worden gebruikt om relevante weergaven in actieve activiteiten op te halen. |
| Request > prefetch > views > order > purchaseProductIds | Nee | Geen lege waarden.<br>Maximale lengte van elke waarde 50.<br>Samengevoegd en gescheiden door komma&#39;s.<br>Totale lengte product-id&#39;s `<=` 250. | Geef de aangeschafte product-id&#39;s door die moeten worden gebruikt om relevante weergaven in actieve activiteiten op te halen. |
| Verzoek > Uitvoeren | Nee |  |  |
| Verzoek > Uitvoeren > pageLoad | Nee |  |  |
| Request > execute > pageLoad > parameters | Nee | Maximaal aantal 50.<br>Naam niet leeg.<br>Naam lengte `<=` 128.<br>Waarde lengte `<=` 5000.<br>Accepteert alleen tekenreekswaarden.<br>De naam mag niet beginnen met &quot;profiel&quot;.<br>Namen niet toegestaan: &quot;orderId&quot;, &quot;orderTotal&quot;, &quot;productPurchasedId&quot;. | Haal aanbiedingen met de opgegeven parameters op wanneer de pagina wordt geladen. |
| Verzoek > execute > pageLoad > profileParameters | Nee | Maximaal aantal 50.<br>Naam niet leeg.<br>Naam lengte `<=` 128.<br>Waarde lengte `<=`256<br>De naam mag niet beginnen met &quot;profiel&quot;.<br>Accepteert alleen tekenreekswaarden. | Haal aanbiedingen met de opgegeven profielparameters op wanneer de pagina wordt geladen. |
| Verzoek > execute > pageLoad > product | Nee |  |  |
| Verzoek > execute > pageLoad > product -> id | Nee | Niet leeg.<br>Maximale grootte = 128. | Ontvang voorstellen met gespecificeerde product IDs wanneer de pagina laadt. |
| Request > execute > pageLoad > product > categoryId | Nee | Niet leeg.<br>Maximale grootte = 128. | Ontvang voorstellen met gespecificeerde productcategorie IDs wanneer de pagina laadt. |
| Verzoek > execute > pageLoad > order | Nee |  |  |
| Verzoek > execute > pageLoad > order > id | Nee | Maximumlengte = 250. | Ontvang voorstellen met gespecificeerde orde IDs wanneer de pagina laadt. |
| Verzoek > execute > pageLoad > order > total | Nee | `>=` 0. | Ontvang voorstellen met gespecificeerde ordetotalen wanneer de pagina laadt. |
| Verzoek > execute > pageLoad > order > purchaseProductIds | Nee | Geen lege waarden.<br>Maximale lengte van elke waarde 50.<br>Samengevoegd en gescheiden door komma&#39;s.<br>Totale lengte product-id&#39;s `<=` 250. | Ontvang voorstellen met gespecificeerde gekochte product IDs wanneer de pagina laadt. |
| Verzoek > Uitvoeren > Selecties | Nee | Maximale grootte = 50.<br>Geen null-elementen. |  |
| Request > execute > mboxes>mbox | Ja | Niet leeg.<br>Geen achtervoegsel &#39;-geklikt&#39;.<br>Maximale grootte = 250.<br>Toegestane tekens: `'-, ._\/=:;&!@#$%^&*()_+|?~[]{}'` | Naam van de box. |
| Request > execute > boxes>mbox>index | Ja | Niet null.<br>Uniek.<br>`>=` 0. | De index vertegenwoordigt niet de volgorde waarin de vakken worden verwerkt. Net als in een webpagina met verschillende regionale vakken kan de volgorde waarin ze worden verwerkt niet worden opgegeven. |
| Request > execute > boxes > mbox > parameters | Nee | Maximum aantal = 50.<br>Naam niet leeg.<br>Naam lengte `<=` 128.<br>Accepteert alleen tekenreekswaarden.<br>Waarde lengte `<=` 5000.<br>De naam mag niet beginnen met &#39;profiel&#39;.<br>Namen niet toegestaan: &quot;orderId&quot;, &quot;orderTotal&quot;, &quot;productPurchasedId&quot;. | Hiermee worden voorstellen voor een bepaalde mbox met de opgegeven parameters opgehaald. |
| Verzoek > execute > mboxes>mbox>profileParameters | Nee | Maximum aantal = 50.<br>Naam niet leeg.<br>Naam lengte `<=` 128.<br>Accepteert alleen tekenreekswaarden.<br>Waarde lengte `<=`256<br>De naam mag niet beginnen met &#39;profiel&#39;. | Hiermee worden aanbiedingen voor een bepaalde box met de opgegeven profielparameters opgehaald. |
| Request > execute > mboxes>mbox > product | Nee |  |  |
| Request > execute > boxes > mbox > product > id | Nee | Niet leeg.<br>Maximale grootte = 128. | Wis voorstellen voor een bepaalde doos met gespecificeerde product IDs. |
| Verzoek > Uitvoeren > Selectievakje > Product > Categorie-id | Nee | Niet leeg.<br>Maximale grootte = 128. | Wis voorstellen voor een bepaalde doos met gespecificeerde productcategorie IDs. |
| Request > execute > boxes > mbox > order | Nee |  |  |
| Request > execute > boxes>mbox > order > id | Nee | Maximumlengte = 250. | Haal voorstellen voor een bepaalde mbox met de gespecificeerde orde IDs op. |
| Verzoek > Uitvoeren > Vakken > Postvak > Volgorde > Totaal | Nee | `>=` 0. | Wis voorstellen voor een bepaalde mbox met de gespecificeerde orde totalen. |
| Verzoek > execute > boxes > mbox > order > purchaseProductIds | Nee | Geen lege waarden.<br>De maximumlengte van elke waarde = 50.<br>Samengevoegd en gescheiden door komma&#39;s.<br>Productids totale lengte `<=` 250. | Wis voorstellen voor een bepaalde doos met de gespecificeerde orde gekochte product IDs. |

## getOffers() aanroepen voor alle weergaven

```javascript
adobe.target.getOffers({
    request: {
      prefetch: {
        views: [{}]
    }
  }
});
```

## getOffers() aanroepen om een apparaatbeslissing te maken

```javascript
adobe.target.getOffers({ 

  decisioningMethod:"on-device", 
  request: { 
    execute: { 
      mboxes: [ 
        { 
          index: 0, 
          name: "homepage" 
        } 
      ] 
    } 
 } 
}); 
```

## Roep getOffers() aan om de nieuwste weergaven op te halen met de doorgegeven parameters en profielparameters

```javascript
adobe.target.getOffers({
  request: {
    "prefetch": {
      "views": [
        {
          "parameters": {
            "ad": "1"
          },
          "profileParameters": {
            "age": 23
          }
        }
      ]
    }
  }
});
```

## Roep getOffers() aan om vakken met doorgegeven parameters en profielparameters op te halen.

```javascript
adobe.target.getOffers({
  request: {
    execute: {
      mboxes: [
        {
          index: 0,
          name: "first-mbox"
        },
        {
          index: 1,
          name: "second-mbox",
          parameters: {
            a: 1
          },
          profileParameters: {
            b: 2
          }
        }
      ]
    }
  }
});
```

## Roep getOffers() aan om de payload van de analyse van de client op te halen

```javascript
adobe.target.getOffers({
      request: {
        experienceCloud: {
          analytics: {
            logging: "client_side"
          }
        },
        prefetch: {
          mboxes: [{
            index: 0,
            name: "a1-serverside-xt"
          }]
        }
      }
    })
    .then(console.log)
```

**Antwoord**:

```javascript
{
  "prefetch": {
    "mboxes": [{
      "index": 0,
      "name": "a1-serverside-xt",
      "options": [{
        "content": "<img src=\"http://s7d2.scene7.com/is/image/TargetAdobeTargetMobile/L4242-xt-usa?tm=1490025518668&fit=constrain&hei=491&wid=980&fmt=png-alpha\"/>",
        "type": "html",
        "eventToken": "n/K05qdH0MxsiyH4gX05/2qipfsIHvVzTQxHolz2IpSCnQ9Y9OaLL2gsdrWQTvE54PwSz67rmXWmSnkXpSSS2Q==",
        "responseTokens": {
          "profile.memberlevel": "0",
          "geo.city": "bucharest",
          "activity.id": "167169",
          "experience.name": "USA Experience",
          "geo.country": "romania"
        }
      }],
      "analytics": {
        "payload": {
          "pe": "tnt",
          "tnta": "167169:0:0|0|100,167169:0:0|2|100,167169:0:0|1|100"
        }
      }
    }]
  }
}
```

De lading kan vervolgens via de [API voor gegevensinvoer](https://helpx.adobe.com/analytics/kb/data-insertion-api-post-method-adobe-analytics.html).

## Gegevens ophalen en renderen vanuit meerdere vakken via getOffers() en applyOffers() {#multiple}

Met at.js 2.x kunt u meerdere vakken ophalen via de `getOffers()` API. U kunt ook gegevens ophalen voor meerdere vakken en deze vervolgens gebruiken `applyOffers()` om de gegevens te renderen op verschillende locaties die door een CSS-kiezer worden geïdentificeerd.

In het volgende voorbeeld ziet u een eenvoudige HTML-pagina waarop at.js 2.x is geïmplementeerd:

```html
<!DOCTYPE html>
<html>
<head>
  <meta charset="utf-8">
  <title>at.js 2.x, multiple selectors and multiple mboxes</title>
  <script src="at.js"></script>
</head>
<body>
  <div id="container1">Default content 1</div>
  
  <div id="container2">Default content 2</div>

  <div id="container3">Default content 3</div>
</body>
</html>
```

Veronderstel dat u drie containers hebt die u via inhoud wilt wijzigen die van wordt ontvangen [!DNL Target]. U kunt één aanvraag maken voor drie vakken waarin elke box inhoud bevat die in de desbetreffende container moet worden gerenderd.

De aanvraag- en rendercode kunnen er als volgt uitzien:

```javascript
adobe.target.getOffers({
  request: {
    prefetch: {
      mboxes: [
        {
          index: 0,
          name: "mbox1"
        },
        {
          index: 1,
          name: "mbox2"
        },
        {
          index: 2,
          name: "mbox3"
        }
      ]
    }
  }
})
.then(response => {
  // get all mboxes from response
  const mboxes = response.prefetch.mboxes;
  let count = 1;

  mboxes.forEach(el => {
    adobe.target.applyOffers({
      selector: "#container" + count,
      response: {
        prefetch: {
          mboxes: [el]
        }
      }
    });

    count += 1;
  });
});
```

In de `request > prefetch > mboxes` -sectie, zijn er drie verschillende vakken. Als de aanvraag succesvol is voltooid, ontvangt u de reactie voor elke box van `response > prefetch > mboxes`. Nadat u de reacties hebt en de locaties die u voor rendering wilt gebruiken, kunt u een activering uitvoeren `applyOffers()` om de opgehaalde inhoud te renderen [!DNL Target]. In dit voorbeeld hebben we de volgende afbeelding:

* mbox1 > CSS selector #container1
* mbox2 > CSS selector #container2
* mbox3 > CSS selector #container3

In dit voorbeeld wordt de telvariabele gebruikt om de CSS-kiezers samen te stellen. In een real-life scenario kunt u een verschillende afbeelding gebruiken tussen de CSS-kiezer en de box.

In dit voorbeeld wordt `prefetch > mboxes`, maar u kunt ook `execute > mboxes`. Controleer of u de voorinstelling `getOffers()`moet u ook de prefetch in het dialoogvenster `applyOffers()` oproepen.

## Roep getOffers() aan om een pageLoad uit te voeren

In het volgende voorbeeld wordt getoond hoe u een pageLoad kunt uitvoeren met getOffers() met at.js 2.*x*

```javascript
adobe.target.getOffers({
    request: {
        execute: {
            pageLoad: {
                parameters: {}
            }
        }
    }
});
```