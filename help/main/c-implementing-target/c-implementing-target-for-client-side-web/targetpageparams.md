---
keywords: targetPageParams;targetPageParams;pageParams;pageparams;pageParams;pageParameters;at.js;functies;function
description: Gebruik de targetPageParams() functie voor de Adobe [!DNL Target] op.js JavaScript-bibliotheek om parameters van buiten de aanvraagcode toe te voegen aan het globale vak.
title: Hoe gebruik ik de functie targetPageParams()?
feature: at.js
role: Developer
exl-id: 0772b400-626c-45d8-a4b5-a12691978cf3
source-git-commit: c196b7e41101978ee029f93d5cd71c9b2d5b99f1
workflow-type: tm+mt
source-wordcount: '162'
ht-degree: 0%

---

# targetPageParams()

Met deze methode kunt u parameters aan de globale mbox koppelen van buiten de aanvraagcode.

Deze functie is zeer nuttig om de zelfde reeks parameters op veelvoudige mbox vraag te omvatten. De functie moet door de klant worden gedefinieerd. Het zou een serie van parameters moeten terugkeren die slechts tot het globale mbox verzoek zullen worden overgegaan. Deze functie kan worden gedefinieerd voordat at.js wordt geladen of in **[!UICONTROL Administration]** > **[!UICONTROL Implementation]** > **[!UICONTROL Edit]** > **[!UICONTROL Library Header]**.

U kunt parameters aan target-global-mbox overgaan gebruikend `targetPageParams()` op een van de volgende manieren te werken:

* Een door ampersand gescheiden lijst
* Een array
* Een JSON-object

## Voorbeelden

Door ampersand gescheiden lijst (waarden moeten URL-gecodeerd zijn):

```javascript
function targetPageParams() { 
    return "param1=value1&param2=value2&p3=hello%20world"; 
}
```

Array (waarden hoeven niet via URL te worden gecodeerd):

```javascript
targetPageParams = function() { 
     return ["a=1", "b=2", "c=hello world"]; 
};
```

JSON (waarden hoeven niet via URL te worden gecodeerd):

```javascript
targetPageParams = function() { 
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
