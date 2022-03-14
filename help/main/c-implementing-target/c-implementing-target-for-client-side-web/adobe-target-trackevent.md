---
keywords: adobe.target.trackEvent;trackEvent;trackevent;track event;at.js;functions;function;preventDefault;preventdefault;prevent default
description: Gebruik de functie adobe.target.trackEvent() voor de Adobe [!DNL Target] om.js JavaScript bibliotheek in werking te stellen om een verzoek in werking te stellen om gebruikersacties, zoals kliks en omzettingen op uw plaats te melden.
title: Hoe gebruik ik de functie adobe.target.trackEvent()?
feature: at.js
role: Developer
exl-id: 36005236-ce18-4845-b4fb-e52056018bc7
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '327'
ht-degree: 0%

---

# adobe.target.trackEvent(options)

Deze functie voert een verzoek in om gebruikersacties, zoals kliks en omzettingen te melden. Het levert geen activiteiten in de reactie.

Deze gebeurtenis-volgende mbox vraag kan dan worden gebruikt om metriek in activiteiten te bepalen. Zie voor meer informatie [Succeswaarden](/help/main/c-activities/r-success-metrics/success-metrics.md#reference_D011575C85DA48E989A244593D9B9924) en [Conversies bijhouden](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/implementing-target-without-a-tag-manager.md#task_E85D2F64FEB84201A594F2288FABF053).

Hier volgen de API-details:

| Sleutel | Type | Vereist | Beschrijving |
|--- |--- |--- |--- |
| mbox | String | Ja | Naam van vak <br>**Opmerking**: Als een trackEvent()-aanroep wordt geactiveerd met een naam van een box die al op de pagina is geactiveerd, wordt de SDID van trackEvent() opnieuw ingesteld en verschilt deze van de aanroepen van Target op de pagina. Als u echter een trackEvent()-aanroep met een andere naam mbox afvuurt, blijft de SDID van de trackEvent()-aanroep consistent met de aanroepen van Page Load Request/triggerView() op de pagina. |
| kiezer | String | Nee | CSS-kiezers die worden gebruikt om de HTML-elementen te zoeken. De gebeurtenislisteners worden aan gevonden elementen gekoppeld. |
| type | String | Nee | Vertegenwoordigt een geregistreerd gebeurtenistype. Het kunnen beide HTML bekende gebeurtenissen zijn zoals: klikken, mousedown, enz., evenals de gebeurtenissen van de douane HTML. |
| preventDefault | Boolean | Nee | Geeft aan of u wilt gebruiken `event.preventDefault()` in de gebeurtenislistener-callback. De standaardwaarde is false.<br>**Opmerking**: Alleen `form[submit]` en `a[click]` worden ondersteund. Andere scenario&#39;s worden niet gesteund wegens ingewikkeldheid en enorme hoeveelheid te steunen scenario&#39;s. |
| param | Object | Nee | Mbox-parameters. Een object van sleutelwaardeparen met de volgende structuur:<br>`{ "param1": "value1", "param2": "value2"}` |
| timeout | Getal | Nee | Time-out in milliseconden.<br>Indien niet opgegeven, wordt de standaardwaarde gebruikt:<br>`...timeoutInSeconds: 0.15...}` |
| succes | -functie | Nee | Een callback-functie die wordt gebruikt om aan te geven dat de gebeurtenis is gerapporteerd. |
| fout | -functie | Nee | Een callback-functie die wordt gebruikt om aan te geven dat de gebeurtenis niet kon worden gerapporteerd. |

## Voorbeeld

```javascript
<a href="https://asite.com">click me!</a> 
```

plus JavaScript-code die moet worden toegewezen `trackEvent`:

```javascript
<script> 
$('a').click(function(event){ 
  adobe.target.trackEvent({'mbox':'homePageHero'}) 
}); 
</script> 
```

Of:

```javascript
adobe.target.trackEvent({ 
    "mbox": "clicked-cta", 
    "params": { 
        "param1": "value1" 
    } 
});
```

>[!NOTE]
>
>Als de verplichte velden niet zijn ingesteld, wordt geen aanvraag uitgevoerd en wordt een fout gegenereerd.
