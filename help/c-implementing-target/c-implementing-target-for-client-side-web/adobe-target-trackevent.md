---
keywords: adobe.target.trackEvent;trackEvent;trackevent;track event;at.js;functions;function;preventDefault;preventdefault;prevent default
description: Informatie over de functie adobe.target.trackEvent(options) voor de JavaScript-bibliotheek van Adobe Target at.js.
title: adobe.target.trackEvent(options)
feature: client-side
subtopic: Getting Started
topic: Standard
translation-type: tm+mt
source-git-commit: 95450abc32be19d04b791af3c62673e9411ab53c
workflow-type: tm+mt
source-wordcount: '298'
ht-degree: 0%

---


# adobe.target.trackEvent(options)

Deze functie voert een verzoek in om gebruikersacties, zoals kliks en omzettingen te melden. Het levert geen activiteiten in de reactie.

Deze gebeurtenis-volgende mbox vraag kan dan worden gebruikt om metriek in activiteiten te bepalen. Voor meer informatie, zie de Metriek [van het](/help/c-activities/r-success-metrics/success-metrics.md#reference_D011575C85DA48E989A244593D9B9924) Succes en de Omzettingen [van het](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/implementing-target-without-a-tag-manager.md#task_E85D2F64FEB84201A594F2288FABF053)Spoor.

Hier volgen de API-details:

| Sleutel | Type | Vereist | Beschrijving |
|--- |--- |--- |--- |
| mbox | String | Ja | Mbox <br>**nameNote**: Als een trackEvent()-aanroep wordt geactiveerd met een naam van een box die al op de pagina is geactiveerd, wordt de SDID van trackEvent() opnieuw ingesteld en verschilt deze van de aanroepen van Target op de pagina. Als u echter een trackEvent()-aanroep met een andere naam mbox afvuurt, blijft de SDID van de trackEvent()-aanroep consistent met de aanroepen van Page Load Request/triggerView() op de pagina. |
| kiezer | String | Nee | CSS-kiezers die worden gebruikt om de HTML-elementen te zoeken. De gebeurtenislisteners worden aan gevonden elementen gekoppeld. |
| type | String | Nee | Vertegenwoordigt een geregistreerd gebeurtenistype. Dit kunnen beide bekende HTML-gebeurtenissen zijn, zoals: klikken, mousedown, enz., evenals de gebeurtenissen van douaneHTML. |
| preventDefault | Boolean | Nee | Geeft aan of moet worden gebruikt `event.preventDefault()` in de callback van de gebeurtenislistener. De standaardwaarde is false.<br>**Opmerking**: Alleen `form[submit] and `[klikken]wordt ondersteund. Andere scenario&#39;s worden niet gesteund wegens ingewikkeldheid en enorme hoeveelheid te steunen scenario&#39;s. |
| param | Object | Nee | Mbox-parameters. Een object van sleutelwaardeparen met de volgende structuur:<br>`{ "param1": "value1", "param2": "value2"}` |
| timeout | Getal | Nee | Time-out in milliseconden.<br>Indien niet opgegeven, wordt de standaardwaarde gebruikt:<br>`...timeoutInSeconds: 0.15...}` |
| succes | -functie | Nee | Een callback-functie die wordt gebruikt om aan te geven dat de gebeurtenis is gerapporteerd. |
| fout | -functie | Nee | Een callback-functie die wordt gebruikt om aan te geven dat de gebeurtenis niet kon worden gerapporteerd. |

## Voorbeeld

```
<a href="https://asite.com">click me!</a> 
```

plus JavaScript-code die moet worden toegewezen `trackEvent`:

```
<script> 
$('a').click(function(event){ 
  adobe.target.trackEvent({'mbox':'homePageHero'}) 
}); 
</script> 
```

Of:

```
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