---
keywords: adobe.target.sendNotifications;sendNotifications;send meldingen;send meldingen;notifications;at.js;functies;function
description: Gebruik adobe.target.sendNotifications() voor at.js om meldingen te verzenden naar de [!DNL Target] rand als een ervaring wordt weergegeven zonder gebruik te maken van applyOffer(s). (js.2.1 +)
title: Hoe gebruik ik de functie adobe.target.sendNotifications()?
feature: at.js
role: Developer
exl-id: 71b7167d-729c-4d43-8f54-f43619e14f32
source-git-commit: c196b7e41101978ee029f93d5cd71c9b2d5b99f1
workflow-type: tm+mt
source-wordcount: '634'
ht-degree: 0%

---

# adobe.target.sendNotifications(options)

Deze functie verzendt een bericht naar de rand van het Doel wanneer een ervaring zonder het gebruiken wordt teruggegeven `adobe.target.applyOffer()` of `adobe.target.applyOffers()`.

>[!NOTE]
>
>Deze functie is geïntroduceerd in at.js 2.1.0 en zal voor om het even welke versies boven 2.1.0 beschikbaar zijn.

| Sleutel | Type | Vereist? | Beschrijving |
| --- | --- | --- | --- |
| consumerId | String | Nee | De standaardwaarde is het globale mbox van de cliënt als niet verstrekt. Deze sleutel wordt gebruikt om extra gegevens ID te produceren die voor integratie A4T wordt gebruikt. |
| Verzoek | Object | Ja | Zie onderstaande tabel Verzoeken. |
| timeout | Getal | Nee | Verzoek time-out. Als deze niet is opgegeven, wordt de standaardtime-out at.js gebruikt. |

## Verzoek

| Veldnaam | Type | Vereist? | Beperking | Beschrijving |
| --- | --- | --- | --- | --- |
| Verzoek > meldingen | Array van objecten | Ja |  | Meldingen voor de weergegeven inhoud, geklikte kiezers en/of bezochte weergaven of vakken. |
| Verzoek > meldingen > adres | Object | Nee |  |  |
| Verzoek > meldingen > adres > URL | String | Nee |  | URL vanwaar het bericht is gestart. |
| Verzoek > meldingen > adres > referencesUrl | String | Nee |  | De verwijzings-URL waarvan het bericht is gestart. |
| Verzoek > meldingen > parameters | String | Nee | De volgende namen zijn niet toegestaan voor parameters:<ul><li>orderId</li><li>orderTotal</li><li>productPurchasedIds</li></ul>Overweeg het volgende:<ul><li>Maximaal 50 parameterlimiet.</li><li>Parameternaam mag niet leeg zijn.</li><li>Parameternaam max. lengte 128.</li><li>Parameternaam mag niet beginnen met &quot;profiel&quot;.</li><li>Parameterwaarde lengte max. 5000.</li></ul> |  |
| Verzoek > meldingen > profileParameters | String | Nee | De volgende namen zijn niet toegestaan voor parameters:<ul><li>orderId</li><li>orderTotal</li><li>productPurchasedIds</li></ul>Overweeg het volgende:<ul><li>Maximaal 50 parameterlimiet.</li><li>Parameternaam mag niet leeg zijn.</li><li>Parameternaam max. lengte 128.</li><li>Parameternaam mag niet beginnen met &quot;profiel&quot;.</li><li>Parameterwaarde lengte max. 5000.</li></ul> |  |
| Verzoek > meldingen > Bestelling | Object | Nee |  | Object dat de orderdetails beschrijft. |
| Verzoek > meldingen > Bestelling > Id | String | Nee | `<=` 250 tekens. | Order-id. |
| Verzoek > meldingen > Bestelling > Totaal | String | Nee | `>=` 0 | Totaal bestellen. |
| Verzoek > meldingen > bestelling > purchaseProductIds | Array van tekenreeks | Nee | <ul><li>Geen lege waarden toegestaan.</li><li>Elke product-id heeft een maximale lengte van 50.</li><li>De product-id&#39;s, gescheiden door komma&#39;s en samengevoegd, mogen niet langer zijn dan 250.</li></ul> | Product-id&#39;s bestellen. |
| Verzoek > meldingen > product | Object | Nee |  |  |
| Verzoek > meldingen > product > id | String | Nee | `<=` 128 tekens; mag niet leeg zijn. | Product-id. |
| Verzoek > meldingen > product > rubriek-ID | String | Nee | `<=` 128 tekens; mag niet leeg zijn. | Categorie-id. |
| Verzoek > meldingen > ID | String | Ja | `<=` 200 tekens. | De bericht-id wordt als reactie gegeven en geeft aan dat het bericht is verwerkt. |
| Verzoek > meldingen > impositie-id | String | Nee | `<= 128` tekens. | Met de ID Impression wordt het huidige bericht gekoppeld aan een eerder bericht of wordt het verzoek uitgevoerd. Als beide overeenkomen, wekken de tweede en andere volgende verzoeken geen nieuwe indruk op de activiteit of ervaring. |
| Verzoek > meldingen > type | String | Ja | &quot;click&quot; of &quot;display&quot; wordt ondersteund. | Meldingstype. |
| Verzoek > meldingen > tijdstempel | Getal`<int64>` | Ja |  | Tijdstempel van het bericht in milliseconden die zijn verstreken sinds het tijdperk van UNIX. |
| Verzoek > meldingen > tokens | Array van tekenreeks | Ja |  | Een lijst met tokens voor weergegeven inhoud of geklikte kiezers, op basis van het type melding. |
| Verzoek > meldingen > mbox | Object | Nee |  | Meldingen voor de box. |
| Request > notifications > mbox > name | String | Nee | Geen lege waarden toegestaan.<br>Toegestane tekens: Zie de opmerking bij deze tabel. | mbox name. |
| Request > notifications > mbox > state | String | Nee |  | mbox state token. |
| Verzoek > meldingen > Weergave | Object | Nee |  |  |
| Verzoek > meldingen > Weergave > ID | Geheel `<int64>` | Nee |  | Id weergeven. De id die aan de weergave is toegewezen toen de weergave werd gemaakt via de weergave-API. |
| Verzoek > meldingen > Weergave > Naam | String | Nee | `<= 128` tekens. | Naam van weergave. |
| Request > notifications > view > key | String | Nee | `<=` 512 tekens. | Weergavesleutel. De sleutel die is ingesteld met de weergave via de API. |
| Verzoek > meldingen > Weergave > Status | String | Nee |  | Statustoken weergeven. |

**Opmerking**: De volgende tekens zijn *niet* toegestaan voor `Request > notifications > mbox > name`:

```
- '-, ./=`:;&!@#$%^&*()+|?~[]{}'
```

## sendNotifications() aanroep na renderen van vooraf ingestelde selectievakjes

```javascript
function createTokens(options) {
  return options.map(e => e.eventToken);
}

function createNotification(mbox, type, tokens) {
  const id = 11111; // here we should use a random ID like UUID
  const timestamp = Date.now();
  const { name, state, parameters, profileParameters, order, product } = mbox;
  const result = {
    id,
    type,
    timestamp,
    parameters,
    profileParameters,
    order,
    product
  };

  result.mbox = { name, state };
  result.tokens = tokens;

  return result;
}

adobe.target.getOffers({
  request: {
    prefetch: {
      mboxes: [
        {
          index: 0,
          name: "a1-serverside-ab"
        }
      ]
    }
  }
})
.then(response => {
  const mboxes = response.prefetch.mboxes;
  const notifications = mboxes.map(mbox => {
    const type = "display";
    const tokens = createTokens(mbox.options);

    return createNotification(mbox, type, tokens);
  });
  
  adobe.target.sendNotifications({
    request: { notifications }
  });
})
```

>[!NOTE]
>
>Als u Adobe Analytics gebruikt, `getOffers()` alleen met prefetch en `sendNotifications()`, moet het analyseverzoek na `sendNotifications()` wordt uitgevoerd. Het doel hiervan is ervoor te zorgen dat de SDID die wordt gegenereerd door `sendNotifications()` komt overeen met de SDID die naar Analytics en Target is verzonden.