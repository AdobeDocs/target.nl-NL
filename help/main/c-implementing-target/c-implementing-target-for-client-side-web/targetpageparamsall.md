---
keywords: targetPageParamsAll;targetPageParameter;PageParamsAll;pageparamsall;page params;page parameters;at.js;function;function
description: Gebruik de functie targetPageParamsAll() voor de Adobe [!DNL Target] op.js JavaScript-bibliotheek om parameters toe te voegen aan alle vakken van buiten de aanvraagcode.
title: Hoe gebruik ik de functie targetPageParamsAll()?
feature: at.js
role: Developer
exl-id: 58fbb62e-30da-486f-b771-6452ad5e27e6
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '161'
ht-degree: 0%

---

# targetPageParamsAll()

Met deze methode kunt u parameters koppelen aan alle vakken van buiten de aanvraagcode.

Dit is zeer nuttig om de zelfde reeks parameters op veelvoudige mbox vraag te omvatten. De functie moet door de klant worden gedefinieerd. Het zou een serie van parameters moeten terugkeren die aan alle mbox verzoeken op de pagina zullen worden overgegaan. Deze functie kan worden gedefinieerd voordat at.js wordt geladen of in **[!UICONTROL Administration]** > **[!UICONTROL Implementation]** > **[!UICONTROL Edit]** > **[!UICONTROL Code Settings]** > **[!UICONTROL Library Header]**.

U kunt op de volgende manieren parameters doorgeven aan target-global-mbox met behulp van de functie targetPageParamsAll():

* Een door ampersand gescheiden lijst
* Een array
* Een JSON-object

## Voorbeelden

Door ampersand gescheiden lijst (waarden moeten URL-gecodeerd zijn):

```javascript
function targetPageParamsAll() { 
    return "param1=value1&param2=value2&p3=hello%20world"; 
}
```

Array (waarden hoeven niet via URL te worden gecodeerd):

```javascript
targetPageParamsAll = function() { 
     return ["a=1", "b=2", "c=hello world"]; 
};
```

JSON (waarden hoeven niet via URL te worden gecodeerd):

```javascript
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