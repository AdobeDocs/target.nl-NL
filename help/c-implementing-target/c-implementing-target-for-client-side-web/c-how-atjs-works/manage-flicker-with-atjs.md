---
keywords: flicker;at.js;implementation;asynchronously;asynchronous;synchronously;synchronous
description: Informatie over hoe de JavaScript-bibliotheek Adobe Target at.js flikkering voorkomt tijdens het laden van de pagina of de toepassing.
title: Hoe Adobe Target at.js flikkering beheert
feature: client-side
topic: Standard
uuid: 65f67c4a-a931-4e0d-80d9-29ab67b62573
translation-type: tm+mt
source-git-commit: 95450abc32be19d04b791af3c62673e9411ab53c
workflow-type: tm+mt
source-wordcount: '655'
ht-degree: 0%

---


# Hoe at.js flikkering beheert{#how-at-js-manages-flicker}

Informatie over hoe de JavaScript-bibliotheek Doel op.js flikkering voorkomt tijdens het laden van de pagina of toepassing.

Er wordt geflikkerd als de standaardinhoud tijdelijk aan bezoekers wordt weergegeven voordat deze wordt vervangen door de inhoud van de activiteit. flikkering is ongewenst, omdat dit verwarrend kan zijn voor bezoekers.

## Een automatisch gemaakte globale mbox gebruiken {#section_C502170D551C4F52AAFD8E82C41BB63A}

Als u de instelling [Automatisch globale mazelbox](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-understanding-global-mbox/understanding-global-mbox.md#concept_76AC0EC995A048238F3220F53773DB13) maken inschakelt bij het configureren van at.js, wordt tijdens het laden van de pagina met .js de flikkering beheerd door de instelling voor dekking te wijzigen. Wanneer at.js wordt geladen, wordt de dekkingsinstelling van het `<body>` element gewijzigd in &quot;0&quot;, waardoor de pagina aanvankelijk onzichtbaar wordt voor bezoekers. Nadat een reactie van Doel wordt ontvangen-of als een fout met het verzoek van het Doel wordt ontdekt-at.js stelt opaciteit aan &quot;1&quot;terug. Zo weet u zeker dat de bezoeker de pagina alleen ziet nadat de inhoud van uw activiteiten is toegepast.

Als u de instelling inschakelt tijdens het configureren van at.js, stelt at.js de dekking van de HTML BODY-stijl in op 0. Nadat een reactie van Doel is ontvangen, stelt at.js de dekking van het HTML-BODY terug naar 1.

Dekking ingesteld op 0 houdt de pagina-inhoud verborgen om flikkering te voorkomen, maar de browser geeft de pagina nog steeds weer en laadt alle benodigde elementen, zoals CSS, afbeeldingen, enz.

Als dekking 0 niet werkt in uw implementatie, kunt u flikkering ook beheren door deze aan te passen `bodyHiddenStyle` en in te stellen op `body {visibility:hidden !important}`. U kunt de hoofdtekst van de waarde gebruiken `{opacity:0 !important}` of `body {visibility:hidden !important}`, afhankelijk van wat het beste werkt voor uw specifieke omstandigheid.

De volgende illustratie toont het Lichaam van de Huid en toont de vraag van het Lichaam in allebei at.js 1.*x* en at.js 2.x.

**at.js 2.x**

![Doelstroom: om.js pagina laden verzoek](/help/c-implementing-target/c-implementing-target-for-client-side-web/assets/atjs-20-flow-page-load-request.png)

**te.js 1.*x***

![](assets/target-flow2.png)

Zie `bodyHiddenStyle` targetGlobalSettings() [voor meer informatie over de](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetgobalsettings.md)overschrijving.

## flikkering beheren bij asynchroon laden bij .js

Het asynchroon laden van at.js is een goede manier om te voorkomen dat de browser de rendering blokkeert. deze techniek kan echter tot flikkering op de webpagina leiden .

U kunt flikkering voorkomen door een vooraf verborgen fragment te gebruiken dat zichtbaar zal zijn nadat de relevante HTML-elementen zijn aangepast door [!DNL Target].

at.js kan asynchroon worden geladen, direct ingesloten op de pagina of via een tagbeheer (Adobe Launch, Dynamic Tag Manager (DTM), enz.).

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

Standaard wordt in het fragment het hele HTML-vak verborgen. In sommige gevallen is het verstandig alleen bepaalde HTML-elementen vooraf te verbergen en niet de hele pagina. U kunt dit bereiken door de stijlparameter aan te passen. Het kan worden vervangen door iets dat slechts bepaalde gebieden van de pagina vooraf verbergt.

U hebt bijvoorbeeld twee gebieden die worden aangeduid met ID&#39;s container-1 en container-2, en de stijl kan vervolgens worden vervangen door:

```
#container-1, #container-2 {opacity: 0 !important}
```

In plaats van de standaardinstelling:

```
body {opacity: 0 !important}
```

## Flicker beheren in at.js 2.x voor triggerView()

Als u `triggerView()` doelgerichte inhoud in uw SPA weergeeft, vindt u flikkerbeheer in het vak. Dit betekent dat vooraf verborgen logica niet handmatig hoeft te worden toegevoegd. In plaats daarvan verbergt at at.js 2.x de locatie waar de weergave moet worden weergegeven voordat de doelinhoud wordt toegepast.

## Flicker beheren met getOffer() en applyOffer()

Omdat zowel `getOffer()` `applyOffer()` als API&#39;s van laag niveau zijn, is er geen ingebouwde flikkerbesturing. U kunt een kiezer of HTML-element als een optie doorgeven om, in dit geval, de activiteiteninhoud aan dit specifieke element `applyOffer()``applyOffer()` toe te voegen. u moet er echter voor zorgen dat het element op de juiste wijze vooraf is verborgen voordat u het element aanroept `getOffer()` en `applyOffer()`.

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

Als u een regionale mbox-implementatie gebruikt, kunt u uw pagina gebruiken `mboxCreate()` met een vergelijkbare indeling als de volgende voorbeeldcode:

```
<div class="mboxDefault">
Some default content
</div>
<script>
mboxCreate('some-mbox');
</script>
```

Als uw pagina&#39;s correct zijn ingericht, beheert at.js flikkering door de CSS &quot;zicht&quot;bezit van het element met de mboxDefault klasse geschikt te schakelen.