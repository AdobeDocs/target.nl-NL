---
keywords: adobe.target.getOffer;getOffer;getoffer;get offer;at.js;functions;function
description: Gebruik de functie adobe.target.getOffer() en de bijbehorende opties voor de Adobe [!DNL Target] at.js-bibliotheek om aanvragen voor een [!DNL Target] voorstel.
title: Hoe gebruik ik de functie adobe.target.getOffer()?
feature: at.js
role: Developer
exl-id: 3448fdaa-b5f6-465d-8858-1dfe214bd8c4
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '472'
ht-degree: 0%

---

# adobe.target.getOffer(options)

This function fires a request to get a Target offer.

Gebruik met `adobe.target.applyOffer()` om de reactie te verwerken of uw eigen succesafhandeling te gebruiken. De parameter options is verplicht en heeft de volgende structuur:

| Sleutel | Type | Required | Beschrijving |
|--- |--- |--- |--- |
| mbox | String | Yes | Naam van vak |
| param | Object | Nee | Mbox parameters. An object of key-value pairs that has the following structure:<br>`{ "param1": "value1", "param2": "value2"}` |
| succes | -functie | Ja | Callback die moet worden uitgevoerd wanneer wij een reactie van de server kregen. The success callback function will receive a single parameter that represents an array of offer objects. Hier volgt een voorbeeld van een geslaagde callback:<br>`function handleSuccess(response){......}`<br>Zie Reacties hieronder voor meer informatie. |
| fout | -functie | Ja | Callback om te worden uitgevoerd wanneer wij een fout hebben. Er zijn een paar gevallen die als onjuist worden beschouwd:<ul><li>HTTP-statuscode anders dan 200 OK</li><li>Response can not be parsed. We hebben bijvoorbeeld slecht JSON of HTML geconstrueerd in plaats van JSON.</li><li>De reactie bevat de &quot;fout&quot;sleutel. For example an exception was thrown on the edge a request could not be properly processed. Er kan een fout optreden als een box is geblokkeerd en er geen inhoud voor kan worden opgehaald, enzovoort. De functie callback van de fout zal twee parameters ontvangen: status en fout. Hier volgt een voorbeeld van een callback-fout: `function handleError(status, error){......}`</li></ul>Zie Reacties wegens fouten hieronder voor meer informatie. |
| timeout | Getal | Nee | Timeout in milliseconds. If not specified, the default timeout in at.js will be used.<br>The default timeout can be set from the [!DNL Target] UI under [!UICONTROL Administration > Implementation]. |

## Voorbeelden {#section_97C2D2E03E6549BEA7F4873E3F5E4A0D}

Parameters toevoegen met getOffer() en applyOffer() gebruiken voor succesafhandeling:

```javascript
adobe.target.getOffer({   
  "mbox": "target-global-mbox", 
  "params": { 
     "a": 1, 
     "b": 2 
  }, 
  "success": function(offer) {           
        adobe.target.applyOffer( {  
           "mbox": "target-global-mbox", 
           "offer": offer  
        } ); 
  },   
  "error": function(status, error) {           
      console.log('Error', status, error); 
  } 
});
```

Parameters en profielparameters toevoegen met getOffer() en applyOffer() gebruiken voor succesafhandeling:

```javascript
adobe.target.getOffer({   
  "mbox": "target-global-mbox", 
  "params": { 
     "a": 1, 
     "b": 2, 
     "profile.age": 27, 
     "profile.gender": "male" 
  }, 
  "success": function(offer) {           
        adobe.target.applyOffer( {  
           "mbox": "target-global-mbox", 
           "offer": offer  
        } ); 
  },   
  "error": function(status, error) {           
      console.log('Error', status, error); 
  } 
});
```

Aangepaste time-out en aangepaste succesafhandeling gebruiken met getOffer():

&quot;UW_OWN_CUSTOM_HANDLING_FUNCTION&quot; is een plaatsaanduiding voor een functie die de klant zou definiëren.

```javascript
adobe.target.getOffer({     
  "mbox": "target-global-mbox",   
  "success": function(offer) { 
    YOUR_OWN_CUSTOM_HANDLING_FUNCTION(offer);   
  }, 
  "error": function(status, error) {                 
    console.log('Error', status, error);   
  },   
  "timeout": 2000 
});
```

## Reacties {#section_CF9FD236EF794620BCBF84EB80160183}

The response parameter passed to the success callback will be an array of actions. Een handeling is een object met doorgaans de volgende indeling:

| Name | Type | Description |
|--- |--- |--- |
| action | String | Type actie dat op het geïdentificeerde element moet worden toegepast. |
| kiezer | Sting | Vertegenwoordigt een schuine-kantkiezer. |
| cssSelector | String | DOM native selector, used for element pre-hiding. |
| content | String | De inhoud die op het geïdentificeerde element moet worden toegepast. |

## Example

```javascript
{ 
    "sessionId": "1444512212156-384616", 
    "tntId": "1444512212156-384616.17_35", 
    "offers": [{ 
        "plugins": ["<script type=\"text/javascript\">\r\n/*mboxHighlight+ (1of2) v1 ==> Response Plugin*/\r\nwindow.ttMETA=(typeof(window.ttMETA)!='undefined')?window.ttMETA:[];window.ttMETA.push({'mbox':'target-global-mbox','campaign':'at: redirect ootb','experience':'Experience B','offer':'/at_redirect_ootb/experiences/1/pages/0/1442082890250'});window.ttMBX=function(x){var mbxList=[];for(i=0;i<ttMETA.length;i++){if(ttMETA[i].mbox==x.getName()){mbxList.push(ttMETA[i])}}return mbxList[x.getId()]}\r\n</script>"], 
        "actions": { 
            "content": [{ 
                "passMboxSession": false, 
                "selector": "body", 
                "action": "redirect", 
                "url": "https://example.com/04.html", 
                "includeAllUrlParameters": true 
            }] 
        } 
    }] 
}
```

## Foutreacties {#section_1ACCE79AF2CB4FA2AD1371EA06AF129F}

De parameters &quot;status&quot; en &quot;error&quot; die aan de callback worden doorgegeven, hebben de volgende indeling:

| Naam | Type | Beschrijving |
|--- |--- |--- |
| status | String | Represents the error status. Deze parameter kan de volgende waarden hebben:<ul><li>timeout: Geeft aan dat er een time-out voor de aanvraag is opgetreden.</li><li>parserror: Geeft aan dat de reactie niet kan worden geparseerd, bijvoorbeeld als er HTML- of onbewerkte tekst wordt ontvangen in plaats van JSON.</li><li>fout: Geeft een algemene fout aan als we HTTP-status hebben ontvangen die afwijkt van 200 OK</li></ul> |
| fout | String | Contains additional data like exception message or anything else that might be useful for troubleshooting. |
