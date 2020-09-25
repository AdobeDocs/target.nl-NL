---
keywords: adobe.target.applyOffers;applyOffers;applyoffers;apply offers;at.js;functions;function
description: Informatie over de functie adobe.target.applyOffers(options) voor de JavaScript-bibliotheek Adobe Target at.js.
title: adobe.target.applyOffers(options) - at.js 2.x
feature: client-side
subtopic: Getting Started
topic: Standard
translation-type: tm+mt
source-git-commit: 8789d750e9e0245d88d54a8d3fe342e5b2e616fc
workflow-type: tm+mt
source-wordcount: '791'
ht-degree: 0%

---


# adobe.target.applyOffers(options) - at.js 2.x

Met deze functie kunt u meerdere aanbiedingen toepassen die zijn opgehaald door `adobe.target.getOffers()`.

>[!NOTE]
>
>Deze functie is geïntroduceerd met at.js 2.x. Deze functie is niet beschikbaar voor versie 1 van at.js.*x*.

| Sleutel | Type | Vereist? | Beschrijving |
| --- | --- | --- | --- |
| kiezer | String | Nee | HTML-element of CSS-kiezer die wordt gebruikt om het HTML-element aan te duiden waar de aanbiedingsinhoud [!DNL Target] moet worden geplaatst. Als er geen kiezer is, wordt ervan [!DNL Target] uitgegaan dat het HTML-element dat moet worden gebruikt HTML HEAD is. |
| Antwoord | Object | Ja | Reactieobject van `getOffers()`.<br>Zie onderstaande tabel Verzoeken. |

## Antwoord

>[!NOTE]
>
>Raadpleeg de documentatie [van de](http://developers.adobetarget.com/api/delivery-api/#tag/Delivery-API) bezorgings-API voor informatie over de acceptabele typen voor alle onderstaande velden.

| Veldnaam | Beschrijving |
| --- | --- |
| response > prefetch > views > options > content | De inhoud van de optie &quot;option&quot; is niet goed gedefinieerd en hangt rechtstreeks af van het optietype/de sjabloonstructuur. |
| response > prefetch > views > options > type | Type optie. Geeft het type &quot;content&quot;-veld aan. Ondersteund type is handelingen. |
| response > prefetch > views > state | Een ondoorzichtig token voor weergavestatus dat moet worden doorgestuurd met een weergavemelding voor de weergave |
| response > prefetch > views > options > responseTokens | Bevat de kaart van `responseTokens` die zijn verzameld toen de huidige optie werd verwerkt. |
| response > prefetch > views > analytics > payload | Analyselading voor cliënt-zijintegratie die naar Analytics zou moeten worden verzonden nadat de mening is toegepast. |
| response > prefetch > views > trace | Het object met alle traceergegevens voor de aanroep van de prefetch per weergave.<br>Het spoorvoorwerp zal ook een versie voor het spoor omvatten.<br>Het spoorvoorwerp zal ook details van de huidige mening omvatten. |
| response > prefetch > views > options > eventToken | Gebeurtenislogbestanden worden per optie uitgevoerd. Voor elke toegepaste optie moet de respectievelijke gebeurtenistoken worden toegevoegd aan de lijst met meldingstokens. Een weergave bestaat uit meerdere opties. Als alle opties zijn toegepast en zichtbaar zijn, `eventTokens` moeten ze allemaal in de kennisgeving worden opgenomen. |
| response > prefetch > views > name | De voor mensen leesbare weergavenaam. |
| response > prefetch > views > metrics | Meldend metriek die zou moeten worden gecontroleerd en dan [!DNL Target] over op de hoogte brengen. Momenteel wordt alleen het klikken op metrisch ondersteund. Als er een klik op het element plaatsvindt, `eventTokens` moet de juiste informatie worden verzameld en moet een melding worden verzonden. |
| response > prefetch > views > key | De sleutel of vingerafdruk die de weergave identificeert. |
| response > prefetch > views > id | Id van de weergave. |
| response > notifications > id | Meldings-id. |
| reactie > meldingen > gebeurtenissen > type | Het type van het bericht, klik, of vertoning. |
| reactie > meldingen > gebeurtenissen > trace | Het spoor voor de berichtgebeurtenis. |
| reactie > meldingen > gebeurtenissen > token | Het token dat met de meldingsgebeurtenis is verzonden. |
| response > notifications > events > timestamp | De tijdstempel die met de meldingsgebeurtenis is verzonden. |
| response > notifications > events > errorCode | Als de melding is mislukt, geeft de code de oorzaak van de fout aan. |
| response > notifications > events | De gebeurtenissen die werden geregistreerd of er niet in geslaagd om voor het huidige bericht worden geregistreerd. |
| response > notifications | Geeft de geregistreerde of mislukte meldingen aan. |
| response > execute > boxes > mbox > trace | Het object met alle traceergegevens voor de afzonderlijke mbox-aanvraag. |
| response > execute > mboxes > mbox > responseTokens | Bevat kaart van `responseTokens` voor specifieke mbox verzoekuitvoering. |
| response > execute > boxes > mbox > option > content | De inhoud van de optie &quot;option&quot; is niet goed gedefinieerd en hangt rechtstreeks af van het optietype/de sjabloonstructuur. |
| response > execute > boxes > mbox > option > type | Type optie. Geeft het type &quot;content&quot;-veld aan. Ondersteunde typen zijn: html, redirect, JSON en dynamic. |
| response > execute > boxes > mbox > options | Reactieoptie. |
| response > execute > mboxes > metrics > eventToken | Token van gebeurtenis click. |
| response > execute > boxes > mbox > metrics > type | &quot;click&quot; |
| response > execute > boxes > mbox > metrics | Bevat een lijst met `clickThrough` metriek. |
| response > execute > boxes > mbox > mbox | De naam van de mbox. |
| response > execute > boxes > mbox >index | Geeft aan dat de reactie wordt gegeven voor mbox met deze index van de aanvraag. |
| response > execute > mboxen > mbox > analytics > payload | Analyselading voor cliënt-zijintegratie die naar Analytics zou moeten worden verzonden nadat mbox is toegepast. (Zie de sectie Campagnes die geschikt zijn voor A4T.) |
| response > execute > boxes | Lijst met uitvoerbare vakken. |
| response > execute > pageLoad > options > content | De inhoud van de optie &quot;option&quot; is niet goed gedefinieerd en hangt rechtstreeks af van het optietype/de sjabloonstructuur. |
| response > execute > pageLoad > options > type | Type optie. Geeft het type &quot;content&quot;-veld aan. Ondersteunde typen zijn: html, redirect, JSON, dynamic en actions. |
| response > execute > pageLoad > options | Opties die niet door meningen (doel-globaal-mbox + opties van activiteiten met meningen worden gegroepeerd die niet door meningen) worden gegroepeerd. |
| response > execute > pageLoad > metrics | Klik op Metriek die niet is ingesteld om tot een bepaalde weergave te behoren. |
| response > execute > pageLoad > trace | Het object met alle traceergegevens voor de pageLoad-aanvraag. |
| response > execute > pageLoad > analytics > payload | Analyselading voor client-side integratie die naar Analytics moet worden verzonden nadat de inhoud voor het laden van de pagina is toegepast. (Zie de sectie Campagnes die geschikt zijn voor A4T.) |

## Voorbeeld applyOffers()-aanroep

```
adobe.target.applyOffers({response:{
  "execute": {
    "pageLoad": {
      "options": [{
        "type": "html",
        "content": "page-load"
      },
      {
        "type": "actions",
        "content": [{
          "type": "setHtml",
          "content": "<h1>Container 1</h1>",
          "selector": "#container1",
          "cssSelector": "#container1"
        },
        {
          "type": "setHtml",
          "content": "<h3>Container 3</h3>",
          "selector": "#container3",
          "cssSelector": "#container3"
        }]
      }],
 
 
      "metrics": [{
        "type": "click",
        "selector": "#container1",
        "eventToken": "page-load-click-metric" 
      }]
    }
  }
}});
```

## Voorbeeld van aanroep van Promise-ketting met `getOffers()` en `applyOffers()`, omdat deze functies zijn gebaseerd op Promise

```
adobe.target.getOffers({...})
.then(response => adobe.target.applyOffers({ response: response }))
.then(() => console.log("Success"))
.catch(error => console.log("Error", error));
```
