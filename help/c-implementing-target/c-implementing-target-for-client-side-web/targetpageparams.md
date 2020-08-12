---
keywords: targetPageParams;targetpageparams;pageParams;pageparams;page params;page parameters;at.js;functions;function
description: Informatie over de targetPageParams() functie voor de Adobe Target at.js JavaScript bibliotheek.
title: Informatie over de targetPageParams() functie voor de Adobe Target at.js JavaScript bibliotheek.
feature: null
subtopic: Getting Started
topic: Standard
translation-type: tm+mt
source-git-commit: a51addc6155f2681f01f2329b25d72327de36701
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 0%

---


# targetPageParams() {#reference_B235C9F6DA79449ABE3E23F914FEABAE}

Met deze methode kunt u parameters aan de globale mbox koppelen van buiten de aanvraagcode.

Deze functie is zeer nuttig om de zelfde reeks parameters op veelvoudige mbox vraag te omvatten. De functie moet door de klant worden gedefinieerd. Het zou een serie van parameters moeten terugkeren die slechts tot het globale mbox verzoek zullen worden overgegaan. Deze functie kan worden gedefinieerd voordat om.js wordt geladen of in **[!UICONTROL Administration]** > **[!UICONTROL Implementation]** > **[!UICONTROL Edit]** > **[!UICONTROL Library Header]**.

U kunt parameters op de volgende manieren doorgeven aan target-global-mbox met behulp van de `targetPageParams()` functie:

* Een door ampersand gescheiden lijst
* Een array
* Een JSON-object

## Voorbeelden

Door ampersand gescheiden lijst (waarden moeten URL-gecodeerd zijn):

```
function targetPageParams() { 
    return "param1=value1&param2=value2&p3=hello%20world"; 
}
```

Array (waarden hoeven niet via URL te worden gecodeerd):

```
targetPageParams = function() { 
     return ["a=1", "b=2", "c=hello world"]; 
};
```

JSON (waarden hoeven niet via URL te worden gecodeerd):

```
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
