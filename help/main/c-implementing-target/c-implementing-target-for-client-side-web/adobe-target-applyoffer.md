---
keywords: adobe.target.applyOffer;applyOffer;applyAanbieding;apply aanbieding;at.js;functies;function
description: Gebruik de functie adobe.target.applyOffer() voor de Adobe [!DNL Target] JavaScript-bibliotheek at.js om de inhoud van het antwoord toe te passen.
title: Hoe gebruik ik de functie adobe.target.applyOffer()?
feature: at.js
role: Developer
exl-id: d230d48f-0d6c-4f55-96a0-681dd31e8d16
source-git-commit: c196b7e41101978ee029f93d5cd71c9b2d5b99f1
workflow-type: tm+mt
source-wordcount: '174'
ht-degree: 0%

---

# adobe.target.applyOffer(options)

Deze functie is bedoeld om de inhoud van de reactie toe te passen met [!DNL Adobe Target].

>[!NOTE]
>
>`applyOffer` vereist `mbox` parameter. Als er geen naam van het selectievakje is opgegeven, treedt er een fout op.

De parameter options is verplicht en heeft de volgende structuur:

| Sleutel | Type | Vereist | Beschrijving |
|--- |--- |--- |--- |
| mbox | String | Ja | Naam van vak<br>Met at.js 1.3.0 (en later) dwingt het Doel af dat de mbox sleutel wordt gebruikt. Deze sleutel is in het verleden vereist, maar Doel dwingt nu zijn gebruik af om ervoor te zorgen dat Doel juiste bevestiging heeft en klanten correct de functie gebruiken. |
| kiezer | Tekenreeks of DOM-element | Nee | HTML-element of CSS-kiezer die wordt gebruikt om het HTML-element aan te duiden waar Target de aanbiedingsinhoud moet plaatsen. Als de selecteur niet wordt verstrekt, veronderstelt het Doel dat het element van de HTML HTML HEAD zou moeten gebruiken. |
| Voorstel | Array | Ja | Een array die op het element moet worden toegepast. |

## Voorbeeld {#section_D8D6A17B73DE4542937CDB687193A5CC}

In het volgende voorbeeld wordt getoond hoe u `getOffer` en `applyOffer` samen:

```javascript
adobe.target.getOffer({   
  "mbox": "mbox",   
  "success": function(offers) {           
        adobe.target.applyOffer( {  
           "mbox": "mbox", 
           "offer": offers  
        } ); 
  },   
  "error": function(status, error) {           
      if (console && console.log) { 
        console.log(status); 
        console.log(error); 
      } 
  }, 
 "timeout": 5000 
}); 
```
