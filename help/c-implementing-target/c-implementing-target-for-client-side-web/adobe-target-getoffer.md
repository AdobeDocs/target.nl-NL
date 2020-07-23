---
keywords: adobe.target.getOffer;getOffer;getoffer;get offer;at.js;functions;function
description: Informatie over de functie adobe.target.getOffer(options) voor de Adobe Target at.js JavaScript-bibliotheek.
title: Informatie over de functie adobe.target.getOffer(options) voor de Adobe Target at.js JavaScript-bibliotheek.
subtopic: Getting Started
topic: Standard
translation-type: tm+mt
source-git-commit: 3edb13b196240bb1918fc66edcc653936e32d3ef
workflow-type: tm+mt
source-wordcount: '464'
ht-degree: 0%

---


# adobe.target.getOffer(options)

Deze functie activeert een aanvraag om een Target-aanbieding te krijgen.

Met gebruiken `adobe.target.applyOffer()` om de reactie te verwerken of uw eigen succesafhandeling te gebruiken. De parameter options is verplicht en heeft de volgende structuur:

| Sleutel | Type | Vereist | Beschrijving |
|--- |--- |--- |--- |
| mbox | String | Ja | Naam van vak |
| param | Object | Nee | Mbox-parameters. Een object van sleutelwaardeparen met de volgende structuur:<br>`{ "param1": "value1", "param2": "value2"}` |
| succes | -functie | Ja | Callback die moet worden uitgevoerd wanneer wij een reactie van de server kregen. De succesvolle callback functie zal één enkele parameter ontvangen die een serie van aanbiedingsvoorwerpen vertegenwoordigt. Hier volgt een voorbeeld van een geslaagde callback:<br>`function handleSuccess(response){......}`<br>Zie Reacties hieronder voor meer informatie. |
| fout | -functie | Ja | Callback om te worden uitgevoerd wanneer wij een fout hebben. Er zijn een paar gevallen die als onjuist worden beschouwd:<ul><li>HTTP-statuscode anders dan 200 OK</li><li>De reactie kan niet worden geparseerd. We hebben bijvoorbeeld slecht opgebouwde JSON of HTML in plaats van JSON.</li><li>De reactie bevat de &quot;fout&quot;sleutel. Er is bijvoorbeeld een uitzondering op de rand gegenereerd die niet correct kan worden verwerkt. Er kan een fout optreden als een box is geblokkeerd en er geen inhoud voor kan worden opgehaald, enzovoort. De functie callback van de fout zal twee parameters ontvangen: status en fout. Hier volgt een voorbeeld van een callback-fout: `function handleError(status, error){......}`</li></ul>Zie Reacties wegens fouten hieronder voor meer informatie. |
| timeout | Getal | Nee | Time-out in milliseconden. Als deze niet wordt opgegeven, wordt de standaardtime-out in at.js gebruikt.<br>De standaardtime-out kan worden ingesteld vanuit de [!DNL Target] gebruikersinterface onder [!UICONTROL Administration > Implementation]. |

## Voorbeelden {#section_97C2D2E03E6549BEA7F4873E3F5E4A0D}

Parameters toevoegen met getOffer() en applyOffer() gebruiken voor succesafhandeling:

```
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

```
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

```
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

De responsparameter die aan de succescallback wordt doorgegeven, is een array met handelingen. Een handeling is een object met doorgaans de volgende indeling:

| Naam | Type | Beschrijving |
|--- |--- |--- |
| action | String | Type actie dat op het geïdentificeerde element moet worden toegepast. |
| kiezer | Sting | Vertegenwoordigt een schuine-kantkiezer. |
| cssSelector | String | Native DOM-kiezer, wordt gebruikt voor het vooraf verbergen van elementen. |
| content | String | De inhoud die op het geïdentificeerde element moet worden toegepast. |

## Voorbeeld

```
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
| status | String | Geeft de foutstatus aan. Deze parameter kan de volgende waarden hebben:<ul><li>timeout: Geeft aan dat er een time-out voor de aanvraag is opgetreden.</li><li>parserror: Geeft aan dat de reactie niet kan worden geparseerd, bijvoorbeeld als er HTML of onbewerkte tekst wordt ontvangen in plaats van JSON.</li><li>fout: Geeft een algemene fout aan als we HTTP-status hebben ontvangen die afwijkt van 200 OK</li></ul> |
| fout | String | Bevat extra gegevens zoals uitzonderingsbericht of iets anders die voor het oplossen van problemen nuttig zouden kunnen zijn. |