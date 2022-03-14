---
keywords: mboxCreate;mboxcreate;mbox create;at.js;functions;function
description: Gebruik de functie mboxCreate() voor de Adobe [!DNL Target] in.js JavaScript-bibliotheek om aanbiedingen toe te passen op de dichtstbijzijnde DIV met de naam van de klasse mboxDefault. (om 1.js)
title: Hoe gebruik ik de functie mboxCreate()?
feature: at.js
role: Developer
exl-id: 821ad97a-345a-4e56-9be6-ab1c7d3a651d
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '205'
ht-degree: 0%

---

# mboxCreate(mbox,params) - at.js 1.x

Voert een verzoek uit en past de aanbieding op dichtstbijzijnde div met mboxDefault klassennaam toe.

>[!NOTE]
>
>Deze functie is beschikbaar voor at.js versies 1.*x* alleen. Deze functie is vervangen door de release van at.js 2.x. Deze functie retourneert standaardinhoud als deze wordt gebruikt met at.js 2.x.

Deze functie is ingebouwd in [!DNL at.js] vooral om de overgang van [!DNL mbox.js] (nu afgekeurd) naar [!DNL at.js]. Een nieuwer alternatief voor `mboxCreate()` is `adobe.target.getOffer()`/ `adobe.target.applyOffer()` of de Angular.

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

* [Foutopsporing](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/c-target-debugging-atjs/target-debugging-atjs.md#concept_CAE591DA8C404C22917584ECD4F7494F) is iets anders.
* Vermijd aanbiedingscode die synchrone, blokkerende vraag vereist.

   Bijvoorbeeld, aanbiedingen die variabelen plaatsen JavaScript die door plaatscode of andere dozen worden gebruikt die later op de pagina komen.

* Zorg ervoor dat u een `<div class="mboxDefault"></div>`voordat wordt aangeroepen `mboxCreate()`, omdat [!DNL at.js] Hiermee voegt u er geen toe.

* Leeg, bovenaan pagina `mboxCreate()` functies worden niet aanbevolen als een globale mbox.

   De automatisch gemaakte globale mbox in [!DNL at.js] is een betere optie omdat het van `<head>` en kan inhoud eerder retourneren.
