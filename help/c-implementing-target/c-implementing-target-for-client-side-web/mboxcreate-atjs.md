---
keywords: mboxCreate;mboxcreate;mbox create;at.js;functions;function
description: Informatie over de functie mboxCreate(mbox,params) voor de Adobe Target at.js JavaScript-bibliotheek.
title: Informatie over de functie mboxCreate(mbox,params) voor de Adobe Target at.js JavaScript-bibliotheek.
feature: null
subtopic: Getting Started
topic: Standard
translation-type: tm+mt
source-git-commit: a51addc6155f2681f01f2329b25d72327de36701
workflow-type: tm+mt
source-wordcount: '193'
ht-degree: 0%

---


# mboxCreate(mbox,params) - at.js 1.x {#reference_E68805FE86C64792B2066DB17B253D74}

Voert een verzoek uit en past de aanbieding op dichtstbijzijnde div met mboxDefault klassennaam toe.

>[!NOTE]
>
>Deze functie is beschikbaar voor at.js versies 1.*alleen x* . Deze functie is vervangen door de release van at.js 2.x. Deze functie retourneert standaardinhoud als deze wordt gebruikt met at.js 2.x.

Deze functie is vooral ingebouwd [!DNL at.js] om de overgang van [!DNL mbox.js] naar [!DNL at.js]te vergemakkelijken. Een nieuwer alternatief voor `mboxCreate()` is `adobe.target.getOffer()`/ `adobe.target.applyOffer()` of de hoekrichtlijn.

## Voorbeeld

```
<div class="mboxDefault"> 
  default content to replace by offer 
</div> 
<script> 
  mboxCreate('mboxName','param1=value1','param2=value2'); 
</script>
```

## Notities

`mboxCreate()` gebruikt nu het &quot;json&quot;eindpunt in plaats van het &quot;standaard&quot;eindpunt en brand asynchroon. Daarom:

* [Foutopsporing](../../c-implementing-target/c-implementing-target-for-client-side-web/c-target-debugging-atjs/target-debugging-atjs.md#concept_CAE591DA8C404C22917584ECD4F7494F) is iets anders.
* Vermijd aanbiedingscode die synchrone, blokkerende vraag vereist.

   Bijvoorbeeld, aanbiedingen die variabelen plaatsen JavaScript die door plaatscode of andere dozen worden gebruikt die later op de pagina komen.

* Zorg ervoor dat u een sjabloon hebt `<div class="mboxDefault"></div>`voordat u een item aanroept `mboxCreate()`, omdat [!DNL at.js] u dit item niet toevoegt.

* Lege, paginagrote `mboxCreate()` functies worden niet aanbevolen als een globale box.

   De automatisch gemaakte globale mbox in [!DNL at.js] is een betere optie omdat deze vanaf de pagina wordt geactiveerd `<head>` en eerder inhoud kan retourneren.