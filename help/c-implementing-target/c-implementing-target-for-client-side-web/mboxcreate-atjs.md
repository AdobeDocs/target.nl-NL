---
keywords: mboxCreate;mboxcreate;mbox create;at.js;functions;function
description: Gebruik de functie mboxCreate() voor de JavaScript-bibliotheek Adobe Target at.js om aanbiedingen toe te passen op de dichtstbijzijnde DIV met de naam van de mboxDefault-klasse. (om 1.js)
title: Hoe gebruik ik de functie mboxCreate()?
feature: at.js
role: Developer
translation-type: tm+mt
source-git-commit: bb27f6e540998f7dbe7642551f7a5013f2fd25b4
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# mboxCreate(mbox,params) - at.js 1.x {#reference_E68805FE86C64792B2066DB17B253D74}

Voert een verzoek uit en past de aanbieding op dichtstbijzijnde div met mboxDefault klassennaam toe.

>[!NOTE]
>
>Deze functie is beschikbaar voor at.js versies 1.** Alleen. Deze functie is vervangen door de release van at.js 2.x. Deze functie retourneert standaardinhoud als deze wordt gebruikt met at.js 2.x.

Deze functie is vooral ingebouwd in [!DNL at.js] om de overgang van [!DNL mbox.js] naar [!DNL at.js] te vergemakkelijken. Een nieuwer alternatief voor `mboxCreate()` is `adobe.target.getOffer()`/ `adobe.target.applyOffer()` of de hoekige instructie.

## Voorbeeld

```javascript
<div class="mboxDefault"> 
  default content to replace by offer 
</div> 
<script> 
  mboxCreate('mboxName','param1=value1','param2=value2'); 
</script>
```

## Notities

`mboxCreate()` gebruikt nu het &quot;json&quot;eindpunt in plaats van het &quot;standaard&quot;eindpunt en brand asynchroon. Daarom:

* [](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-target-debugging-atjs/target-debugging-atjs.md#concept_CAE591DA8C404C22917584ECD4F7494F) Debuggingatie is iets anders.
* Vermijd aanbiedingscode die synchrone, blokkerende vraag vereist.

   Bijvoorbeeld, aanbiedingen die variabelen plaatsen JavaScript die door plaatscode of andere dozen worden gebruikt die later op de pagina komen.

* Zorg ervoor dat u een `<div class="mboxDefault"></div>`hebt voordat u `mboxCreate()` aanroept, omdat [!DNL at.js] er geen voor u toevoegt.

* Lege functies van boven aan pagina `mboxCreate()` worden niet aanbevolen als een globale box.

   Het automatisch gemaakte globale mbox in [!DNL at.js] is een betere optie omdat het van `<head>` in brand steekt en inhoud kan vroeger terugkeren.