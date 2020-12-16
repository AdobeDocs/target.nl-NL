---
keywords: global mbox parameters;targetPageParams;query string;array;json;dtm;dynamic tag management
description: De JavaScript targetPageParams functie wordt gebruikt om parameters tot globale mbox over te gaan. Dit is nodig in elk scenario waarin aanvullende informatie over doelgerichtheid/context aan Adobe Target wordt doorgegeven.
title: Parameters doorgeven aan een globale box
feature: null
translation-type: tm+mt
source-git-commit: 5c7ab4af3d4290ef8fa53ed51ed1c2e8336e02f9
workflow-type: tm+mt
source-wordcount: '381'
ht-degree: 0%

---


# Parameters doorgeven aan een globale box{#pass-parameters-to-a-global-mbox}

De functie JavaScript `targetPageParams` wordt gebruikt om parameters tot globale mbox in &lt;a1 door te geven/>. [!DNL Adobe Target] Dit is nodig in elk scenario waarbij extra informatie over gericht/context moet worden doorgegeven aan [!DNL Target].

In een [!DNL Recommendations]-activiteit gebruikt u bijvoorbeeld de parameters om het huidige product of de huidige categorie te vertegenwoordigen die wordt weergegeven.

De code die de JavaScript-functie moet aanroepen, moet vóór het globale vakje op de pagina komen, ongeacht of het globale vakje als onderdeel van at.js is geactiveerd of handmatig in de paginacode is opgenomen.

>[!NOTE]
>
>Als u parameters aan alle dozen op de pagina, niet alleen aan globale mbox wilt toevoegen, gebruik [targetPageParamsAll ()](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetpageparamsall.md) functie.

U kunt parameters aan `target-global-mbox` overgaan gebruikend de `targetPageParams()` functie op om het even welke volgende manieren:

* Een array
* Een JSON-object
* Een door ampersand gescheiden lijst

Gebruik deze drie methoden om te controleren of de parameters correct worden doorgegeven. Mogelijk kunt u ook controleren of parameters worden doorgegeven met de [Adobe Experience Cloud Debugger](https://experienceleague.adobe.com/docs/debugger/using/experience-cloud-debugger.html).

U moet de JavaScript-functie definiëren voordat u het globale vakje aan de pagina toevoegt. De naam moet `targetPageParams` zijn.

## Tekenreeks query

```
p1=v1&p2=v2&p3=hello%20world
```

* Naam: `targetPageParams`
* Retourwaarde: a &quot;&amp;&quot; gescheiden parameters, met URL gecodeerde parameterwaarden.

   Voorbeeld:

   In dit voorbeeld heeft p3 de waarde `hello world`, die URL-gecodeerd is.

Hieronder ziet u hoe de code voor de pagina eruit kan zien:

```
<html> 
  <head> 
    <title>Title here..</title> 
    <script type="text/javascript"> 
        function targetPageParams() { 
           
<b>return "p1=v1&p2=v2&p3=hello%20world"</b>; 
        } 
    </script> 
    <script src="mbox.js" type="text/javascript"></script> 
  </head> 
  <body>Body here... 
  </body> 
</html>
```

In dit voorbeeld worden de volgende gegevens naar de mbox-rand verzonden:

* p1=v1
* p2=v2
* p3=hello wereld

## Array

```
<!--window.-->targetPageParams = function() { 
  return ["a=1", "b=2", "c=hello world"]; 
}; 
```

Waarden hoeven niet via URL te worden gecodeerd. Als een waarde bijvoorbeeld een spatie bevat, is het niet nodig de spatie te coderen.

In dit voorbeeld worden de volgende gegevens naar de mbox-rand verzonden:

* a=1
* b=2
* c=hello wereld

## JSON

JSON is een krachtige manier om parameters door te geven. Doel gebruikt de JSON-objectsleutels om gecompliceerde structuren samen te voegen tot eenvoudige parameters.

```
<!--window.-->targetPageParams = function() { 
  return { 
    "a": 1, 
    "b": 2, 
    "profile": { 
                  "memberStatus": Gold, 
                  "country": { 
                                "city": "San Francisco" 
                            } 
              } 
  }; 
}; 
```

Waarden hoeven niet via URL te worden gecodeerd. &quot;San Francisco&quot; vereist bijvoorbeeld niet dat de ruimte wordt gecodeerd. Een ruimte volstaat.

In dit voorbeeld worden de volgende gegevens naar de mbox-rand verzonden:

* a=1
* b=2
* `profile.memberStatus`=Goud
* `profile.country.city`=San Francisco