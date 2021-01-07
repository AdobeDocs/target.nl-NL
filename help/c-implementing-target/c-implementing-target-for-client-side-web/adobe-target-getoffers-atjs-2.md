---
keywords: adobe.target.getOffers;getOffers;getoffers;get offers;at.js;functions;function
description: Informatie over de functie adobe.target.getOffers(options) voor de Adobe Target at.js JavaScript-bibliotheek.
title: adobe.target.getOffers(options) - at.js 2.x
feature: at.js
translation-type: tm+mt
source-git-commit: 6bb75e3b818a71af323614d9150e50e3e9f611b7
workflow-type: tm+mt
source-wordcount: '1219'
ht-degree: 0%

---


# adobe.target.getOffers(options) - at.js 2.x

Deze functie laat u veelvoudige aanbiedingen terugwinnen door in veelvoudige dozen over te gaan. Bovendien kunnen meerdere aanbiedingen worden opgehaald voor alle weergaven in actieve activiteiten.

>[!NOTE]
>
>Deze functie is geïntroduceerd met at.js 2.x. Deze functie is niet beschikbaar voor versie 1 van at.js.*x*.

| Sleutel | Type | Vereist? | Beschrijving |
| --- | --- | --- | --- |
| consumerId | String | Nee | De standaardwaarde is het globale mbox van de cliënt als niet verstrekt. Deze sleutel wordt gebruikt om extra gegevens ID te produceren die voor integratie A4T wordt gebruikt. Deze sleutel is een unieke tekenreeks per bezoeker. |
| verzoek | Object | Ja | Zie onderstaande tabel Verzoeken. |
| timeout | Getal | Nee | time-out verzoek. Als deze niet is opgegeven, wordt de standaardtime-out at.js gebruikt. |

## Verzoek

>[!NOTE]
>
>Raadpleeg de [Delivery API documentatie](http://developers.adobetarget.com/api/delivery-api/#tag/Delivery-API) voor informatie over de acceptabele typen voor alle hieronder vermelde velden.

| Veldnaam | Vereist? | Beperkingen | Beschrijving |
| --- | --- | --- | --- |
| request > id | Nee |  | Een van `tntId`, `thirdPartyId` of `marketingCloudVisitorId` is vereist. |
| Request > id > thirdPartyId | Nee | Maximale grootte = 128 |  |  |
| Verzoek > ExperienceCloud | Nee |  |  |
| Request > ExperienceCloud > Analytics | Nee |  | Adobe Analytics-integratie |
| Request > ExperienceCloud > Analytics > logging | Nee | Het volgende moet op pagina worden geïmplementeerd:<ul><li>Bezoekersidentiteitsservice</li><li>Appmeasurement.js</li></ul> | De volgende waarden worden ondersteund:<br>**client_side**: Wanneer gespecificeerd, zal een analytische lading aan de bezoeker worden teruggegeven die zou moeten worden gebruikt om naar Adobe Analytics via de Invoeging API van Gegevens te verzenden.<br>**server_kant**: Dit is de standaardwaarde waar het doel en de achtergrond van Analytics SDID zullen gebruiken om de vraag voor rapporteringsdoeleinden samen te binden. |
| Verzoek > prefetch | Nee |  |  |
| Verzoek > Prefetch > views | Nee | Maximumaantal 50<br>Naam niet leeg<br>Naam lengte `<=` 128<br>Waarde lengte `<=` 5000<br>Naam mag niet beginnen met &quot;profiel&quot;<br>Niet-toegestane namen: &quot;orderId&quot;, &quot;orderTotal&quot;, &quot;productPurchasedId&quot; | Geef parameters door die moeten worden gebruikt om relevante weergaven in actieve activiteiten op te halen. |
| Request > prefetch > views > profileParameters | Nee | Maximumaantal 50<br>Naam niet leeg<br>Naam lengte `<=` 128<br>Waarde lengte `<=` 5000<br>Naam mag niet beginnen met &quot;profiel&quot; | Geef profielparameters door die moeten worden gebruikt om relevante weergaven in actieve activiteiten op te halen. |
| Request > prefetch > views > product | Nee |  |  |
| Request > prefetch > views > product -> id | Nee | Niet leeg<br>maximumgrootte = 128 | Geef de product-id&#39;s door die moeten worden gebruikt om relevante weergaven in actieve activiteiten op te halen. |
| Request > prefetch > views > product > categoryId | Nee | Niet leeg<br>maximumgrootte = 128 | Geef de id&#39;s van de productcategorie door die moeten worden gebruikt om relevante weergaven in activiteiten op te halen. |
| Request > prefetch > views > order | Nee |  |  |
| Request > prefetch > views > order > id | Nee | Maximumlengte = 250 | Geef dit door zodat id&#39;s kunnen worden gebruikt om relevante weergaven in actieve activiteiten op te halen. |
| Verzoek > Prefetch > views > order > total | Nee | Totaal `>=` 0 | Geef de totalen door die moeten worden gebruikt om relevante weergaven in actieve activiteiten op te halen. |
| Request > prefetch > views > order > purchaseProductIds | Nee | Geen lege waarden<br>Maximale lengte van elke waarde 50<br>Gecatactiveerd en gescheiden door komma<br>Totale lengte van product-id&#39;s `<=` 250 | Geef de aangeschafte product-id&#39;s door die moeten worden gebruikt om relevante weergaven in actieve activiteiten op te halen. |
| Verzoek > Uitvoeren | Nee |  |  |
| Verzoek > Uitvoeren > pageLoad | Nee |  |  |
| Request > execute > pageLoad > parameters | Nee | Maximum aantal 50<br>Naam niet leeg<br>Naam lengte `<=` 128<br>Waarde lengte `<=` 5000<br>Naam mag niet beginnen met &quot;profiel.&quot;<br>Namen niet toegestaan: &quot;orderId&quot;, &quot;orderTotal&quot;, &quot;productPurchasedId&quot; | Haal aanbiedingen met de opgegeven parameters op wanneer de pagina wordt geladen. |
| Verzoek > execute > pageLoad > profileParameters | Nee | Maximum aantal 50<br>Naam niet leeg<br>Naam lengte `<=` 128<br>Waarde lengte `<=`256<br>Naam mag niet beginnen met &quot;profiel.&quot; | Haal aanbiedingen met de opgegeven profielparameters op wanneer de pagina wordt geladen. |
| Verzoek > execute > pageLoad > product | Nee |  |  |
| Verzoek > execute > pageLoad > product -> id | Nee | Niet leeg<br>Maximale grootte = 128 | Ontvang voorstellen met gespecificeerde product IDs wanneer de pagina laadt. |
| Request > execute > pageLoad > product > categoryId | Nee | Niet leeg<br>Maximale grootte = 128 | Ontvang voorstellen met gespecificeerde productcategorie IDs wanneer de pagina laadt. |
| Verzoek > execute > pageLoad > order | Nee |  |  |
| Verzoek > execute > pageLoad > order > id | Nee | Maximumlengte = 250 | Ontvang voorstellen met gespecificeerde orde IDs wanneer de pagina laadt. |
| Verzoek > execute > pageLoad > order > total | Nee | `>=` 0 | Ontvang voorstellen met gespecificeerde ordetotalen wanneer de pagina laadt. |
| Verzoek > execute > pageLoad > order > purchaseProductIds | Nee | Geen lege waarden<br>Maximale lengte van elke waarde 50<br>Gecatactiveerd en gescheiden door komma<br>Totale lengte van product-id&#39;s `<=` 250 | Ontvang voorstellen met gespecificeerde gekochte product IDs wanneer de pagina laadt. |
| Verzoek > Uitvoeren > Selecties | Nee | Maximale grootte = 50<br>Geen null-elementen |  |
| Request > execute > mboxes>mbox | Ja | Niet leeg<br>Geen &#39;-geklikt&#39; achtervoegsel<br>Maximale grootte = 250<br>Toegestane tekens: `'-, ._\/=:;&!@#$%^&*()_+|?~[]{}'` | Naam van de box. |
| Request > execute > boxes>mbox>index | Ja | Niet null<br>Unique<br>`>=` 0 | De index vertegenwoordigt niet de volgorde waarin de vakken worden verwerkt. Net als in een webpagina met verschillende regionale vakken kan de volgorde waarin ze worden verwerkt niet worden opgegeven. |
| Request > execute > boxes > mbox > parameters | Nee | Maximum aantal = 50<br>Naam niet leeg<br>Naam lengte `<=` 128<br>Waarde lengte `<=` 5000<br>Naam mag niet beginnen met &quot;profiel.&quot;<br>Namen niet toegestaan: &quot;orderId&quot;, &quot;orderTotal&quot;, &quot;productPurchasedId&quot; | Hiermee worden voorstellen voor een bepaalde mbox met de opgegeven parameters opgehaald. |
| Verzoek > execute > mboxes>mbox>profileParameters | Nee | Maximum aantal = 50<br>Naam niet leeg<br>Naam lengte `<=` 128<br>Waarde lengte `<=`256<br>Naam mag niet beginnen met &quot;profiel.&quot; | Hiermee worden aanbiedingen voor een bepaalde box met de opgegeven profielparameters opgehaald. |
| Request > execute > mboxes>mbox > product | Nee |  |  |
| Request > execute > boxes > mbox > product > id | Nee | Niet leeg<br>Maximale grootte = 128 | Wis voorstellen voor een bepaalde doos met gespecificeerde product IDs. |
| Verzoek > Uitvoeren > Selectievakje > Product > Categorie-id | Nee | Niet leeg<br>Maximale grootte = 128 | Wis voorstellen voor een bepaalde doos met gespecificeerde productcategorie IDs. |
| Request > execute > boxes > mbox > order | Nee |  |  |
| Request > execute > boxes>mbox > order > id | Nee | Maximumlengte = 250 | Haal voorstellen voor een bepaalde mbox met de gespecificeerde orde IDs op. |
| Verzoek > Uitvoeren > Vakken > Postvak > Volgorde > Totaal | Nee | `>=` 0 | Wis voorstellen voor een bepaalde mbox met de gespecificeerde orde totalen. |
| Verzoek > execute > boxes > mbox > order > purchaseProductIds | Nee | Geen blanco waarden<br>Maximumlengte van elke waarde = 50<br>Geconcentreerd en gescheiden door komma<br>Product ids totale lengte `<=` 250 | Wis voorstellen voor een bepaalde doos met de gespecificeerde orde gekochte product IDs. |

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

**Reactie**:

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

De nuttige lading kan dan aan Adobe Analytics via [de Invoeging API van Gegevens](https://helpx.adobe.com/analytics/kb/data-insertion-api-post-method-adobe-analytics.html) door:sturen.

## Gegevens uit meerdere vakken ophalen en renderen via getOffers() en applyOffers() {#multiple}

met at.js 2.x kunt u meerdere vakken ophalen via de `getOffers()`-API. U kunt ook gegevens ophalen voor meerdere vakken en vervolgens `applyOffers()` gebruiken om de gegevens te renderen op verschillende locaties die door een CSS-kiezer worden geïdentificeerd.

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

Veronderstel dat u drie containers hebt die u via inhoud wilt wijzigen die van [!DNL Target] wordt ontvangen. U kunt één aanvraag maken voor drie vakken waarin elke box inhoud bevat die in de desbetreffende container moet worden gerenderd.

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

In de sectie `request > prefetch > mboxes` zijn er drie verschillende vakjes. Als het verzoek met succes werd voltooid, ontvangt u de reactie voor elke mbox van `response > prefetch > mboxes`. Nadat u de reacties hebt en de locaties die u voor rendering wilt gebruiken, kunt u `applyOffers()` aanroepen om de inhoud te renderen die u hebt opgehaald uit [!DNL Target]. In dit voorbeeld hebben we de volgende afbeelding:

* mbox1 > CSS selector #container1
* mbox2 > CSS selector #container2
* mbox3 > CSS selector #container3

In dit voorbeeld wordt de telvariabele gebruikt om de CSS-kiezers samen te stellen. In een real-life scenario kunt u een verschillende afbeelding gebruiken tussen de CSS-kiezer en de box.

In dit voorbeeld wordt `prefetch > mboxes` gebruikt, maar u kunt `execute > mboxes` ook gebruiken. Zorg ervoor dat als u prefetch in `getOffers()` gebruikt, u ook prefetch in `applyOffers()` aanroeping zou moeten gebruiken.

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
