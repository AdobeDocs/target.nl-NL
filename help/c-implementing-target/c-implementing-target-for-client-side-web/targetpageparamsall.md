---
keywords: targetPageParamsAll;targetpageparamsall;PageParamsAll;pageparamsall;page params;page parameters;at.js;functions;function
description: Informatie over de targetPageParamsAll() functie voor de Adobe Target at.js JavaScript bibliotheek.
title: targetPageParamsAll()
feature: client-side
subtopic: Getting Started
topic: Standard
translation-type: tm+mt
source-git-commit: 8789d750e9e0245d88d54a8d3fe342e5b2e616fc
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 0%

---


# targetPageParamsAll()

Met deze methode kunt u parameters koppelen aan alle vakken van buiten de aanvraagcode.

Dit is zeer nuttig om de zelfde reeks parameters op veelvoudige mbox vraag te omvatten. De functie moet door de klant worden gedefinieerd. Het zou een serie van parameters moeten terugkeren die aan alle mbox verzoeken op de pagina zullen worden overgegaan. Deze functie kan worden gedefinieerd voordat om.js wordt geladen of in **[!UICONTROL Administration]** > **[!UICONTROL Implementation]** > **[!UICONTROL Edit]** > **[!UICONTROL Code Settings]** > **[!UICONTROL Library Header]**.

U kunt op de volgende manieren parameters doorgeven aan target-global-mbox met behulp van de functie targetPageParamsAll():

* Een door ampersand gescheiden lijst
* Een array
* Een JSON-object

## Voorbeelden

Door ampersand gescheiden lijst (waarden moeten URL-gecodeerd zijn):

```
function targetPageParamsAll() { 
    return "param1=value1&param2=value2&p3=hello%20world"; 
}
```

Array (waarden hoeven niet via URL te worden gecodeerd):

```
targetPageParamsAll = function() { 
     return ["a=1", "b=2", "c=hello world"]; 
};
```

JSON (waarden hoeven niet via URL te worden gecodeerd):

```
targetPageParamsAll = function() { 
  return { 
    "a": 1, 
    "b": 2, 
    "profile": { 
        "age": 26, 
        "country": { 
          "city": "San Francisco" 
        } 
      } 
  }; 
};
```
