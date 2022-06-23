---
keywords: flikkering;at.js;implementatie;asynchroon;asynchroon;synchroon
description: Meer informatie over .js en Adobe [!DNL Target] voorkomt dat er tijdens het laden van de pagina of de app flikkering optreedt (standaardinhoud wordt tijdelijk weergegeven voordat deze wordt vervangen door activiteit-inhoud).
title: Hoe beheert at.js Flicker?
feature: at.js
role: Developer
exl-id: f6c26973-e046-42ed-91db-95c8a4210a9d
source-git-commit: b1e8ea2370fc15f4bfcd960ab2960cafe2db92b8
workflow-type: tm+mt
source-wordcount: '691'
ht-degree: 0%

---

# Hoe at.js flikkering beheert

Informatie over hoe de JavaScript-bibliotheek Doel op.js flikkering voorkomt tijdens het laden van de pagina of toepassing.

Er wordt geflikkerd als de standaardinhoud tijdelijk aan bezoekers wordt weergegeven voordat deze wordt vervangen door de inhoud van de activiteit. flikkering is ongewenst, omdat dit verwarrend kan zijn voor bezoekers.

## Een automatisch gemaakte globale mbox gebruiken {#section_C502170D551C4F52AAFD8E82C41BB63A}

Als u de optie [Globale box automatisch maken](https://developer.adobe.com/target/implement/client-side/atjs/global-mbox/global-mbox-overview/) Als u instelt bij het configureren van at.js, beheert at.js flikkering door de instelling voor dekking te wijzigen terwijl de pagina wordt geladen. Wanneer at.js laadt, wijzigt dit de dekkingsinstelling van het gereedschap `<body>` element aan &quot;0&quot;, waardoor de pagina aanvankelijk onzichtbaar wordt voor bezoekers. Nadat een reactie van Doel wordt ontvangen-of als een fout met het verzoek van het Doel wordt ontdekt-at.js stelt opaciteit aan &quot;1&quot;terug. Zo weet u zeker dat de bezoeker de pagina alleen ziet nadat de inhoud van uw activiteiten is toegepast.

Als u de instelling inschakelt tijdens het configureren van at.js, stelt at.js de dekking van de HTML BODY-stijl in op 0. Nadat een reactie van Doel wordt ontvangen, stelt at.js HTML BODY opaciteit aan 1 terug.

Dekking ingesteld op 0 houdt de pagina-inhoud verborgen om flikkering te voorkomen, maar de browser geeft de pagina nog steeds weer en laadt alle benodigde elementen, zoals CSS, afbeeldingen, enz.

Als dekking 0 niet werkt in uw implementatie, kunt u flikkering ook beheren door `bodyHiddenStyle` en stel deze in op `body {visibility:hidden !important}`. U kunt de hoofdtekst van beide waarden gebruiken `{opacity:0 !important}` of `body {visibility:hidden !important}`, afhankelijk van wat het beste werkt voor uw specifieke omstandigheid.

De volgende illustratie toont het Lichaam van de Huid en toont de vraag van het Lichaam in allebei at.js 1.*x* en at.js 2.x.

**at.js 2.x**

![Doelstroom: om.js pagina laden verzoek](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/assets/atjs-20-flow-page-load-request.png)

**te.js 1.*x***

![](assets/target-flow2.png)

Voor meer informatie over de `bodyHiddenStyle` override, zie [targetGlobalSettings()](https://developer.adobe.com/target/implement/client-side/atjs/atjs-functions/targetglobalsettings/).

## flikkering beheren bij asynchroon laden bij .js

Het asynchroon laden van at.js is een goede manier om te voorkomen dat de browser de rendering blokkeert. deze techniek kan echter tot flikkering op de webpagina leiden .

U kunt flikkering voorkomen door een vooraf verborgen fragment te gebruiken dat zichtbaar zal zijn nadat de relevante HTML-elementen zijn gepersonaliseerd door [!DNL Target].

at.js kan asynchroon worden geladen, rechtstreeks ingesloten op de pagina of via een tagbeheer (bijvoorbeeld [!DNL Adobe Experience Platform Launch]).

Als at.js op de pagina is ingesloten, moet het fragment worden toegevoegd voordat u at.js laadt. Als u at.js laadt via een tagmanager die ook asynchroon wordt geladen, moet u het fragment toevoegen voordat u het tagbeheer laadt. Als de tagmanager synchroon wordt geladen, kan het script vóór at.js worden opgenomen in de tagmanager.

Het vooraf verborgen codefragment ziet er als volgt uit:

```
;(function(win, doc, style, timeout) {
  var STYLE_ID = 'at-body-style';

  function getParent() {
    return doc.getElementsByTagName('head')[0];
  }

  function addStyle(parent, id, def) {
    if (!parent) {
      return;
    }

    var style = doc.createElement('style');
    style.id = id;
    style.innerHTML = def;
    parent.appendChild(style);
  }

  function removeStyle(parent, id) {
    if (!parent) {
      return;
    }

    var style = doc.getElementById(id);

    if (!style) {
      return;
    }

    parent.removeChild(style);
  }

  addStyle(getParent(), STYLE_ID, style);
  setTimeout(function() {
    removeStyle(getParent(), STYLE_ID);
  }, timeout);
}(window, document, "body {opacity: 0 !important}", 3000));
```

Standaard wordt in het fragment de hele HTML-BODY verborgen. In sommige gevallen is het verstandig alleen bepaalde HTML-elementen vooraf te verbergen en niet de hele pagina. U kunt dit bereiken door de stijlparameter aan te passen. Deze kan worden vervangen door iets dat alleen bepaalde gebieden op de pagina vooraf verbergt.

U hebt bijvoorbeeld twee gebieden die worden aangeduid met ID&#39;s container-1 en container-2, en de stijl kan vervolgens worden vervangen door:

```
#container-1, #container-2 {opacity: 0 !important}
```

In plaats van de standaardinstelling:

```
body {opacity: 0 !important}
```

## Flicker beheren in at.js 2.x voor triggerView()

DOM-voorverbergen is alleen van toepassing op het laden van de eerste pagina. Voor SPA wordt het DOM bijgewerkt wanneer `triggerView()` wordt aangeroepen. Er kan een korte flikkering optreden tussen het moment dat de SPA inhoud rendert naar de DOM en het moment dat updates at.js worden uitgevoerd [!DNL Target] voorstellen.  Als u flikkering wilt minimaliseren, `triggerView` Als u inhoud voor het laden van pagina&#39;s wilt wijzigen, moet &#39;triggerView&#39; worden aangeroepen zodra de pagina is gerenderd.

## Flicker beheren met getOffer() en applyOffer()

Omdat beide `getOffer()` en `applyOffer()` Bij API&#39;s op laag niveau is er geen ingebouwde flikkerbesturing. U kunt een kiezer of HTML-element als optie aan `applyOffer()`in dit geval `applyOffer()` voegt de inhoud van de activiteit aan dit bepaalde element toe; nochtans, moet u ervoor zorgen het element behoorlijk vóór het aanhalen wordt verborgen `getOffer()` en `applyOffer()`.

```
document.documentElement.style.opacity = "0";
 
adobe.target.getOffer({
    mbox: 'target-global-mbox',
    success: function(offer) {
        adobe.target.applyOffer({
            mbox: 'target-global-mbox',
            offer: offer
        });
 
        document.documentElement.style.opacity = "1";
    },
    error: function() {
        document.documentElement.style.opacity = "1";        
    }
});
```

## Een regionale box met mboxCreate() gebruiken in at.js 1.x (niet ondersteund in at.js 2.x)

Als u een regionale mbox-implementatie gebruikt, kunt u `mboxCreate()` met de pagina die u hebt ingericht, lijkt op de volgende voorbeeldcode:

```
<div class="mboxDefault">
Some default content
</div>
<script>
mboxCreate('some-mbox');
</script>
```

Als uw pagina&#39;s correct zijn ingericht, beheert at.js flikkering door de CSS &quot;zicht&quot;bezit van het element met de mboxDefault klasse geschikt te schakelen.
