---
keywords: composer voor visuele ervaring;visuele ervaring composer tips en trucs;visuele ervaring composer beperkingen;visuele ervaring composer beveats;vec best practices;vec
description: Leer de beste praktijken om uw ervaringen te laten werken zoals verwacht wanneer het gebruiken van [!UICONTROL Visual Experience Composer] (VEC).
title: Wat zijn [!UICONTROL Visual Experience Composer] aanbevolen procedures en beperkingen?
feature: Visual Experience Composer (VEC)
exl-id: cf51bfec-d7fa-4ec1-a5dc-35edefefd3e4
source-git-commit: 8c62a0e976ce075d07e1f80018c7ad7fac240eea
workflow-type: tm+mt
source-wordcount: '2435'
ht-degree: 0%

---

# [!UICONTROL Visual Experience Composer] aanbevolen procedures en beperkingen

Volg de aanbevolen procedures bij het gebruik van [!DNL Adobe Target] [!UICONTROL Visual Experience Composer] (VEC) om ervoor te zorgen dat uw ervaringen naar behoren werken. Houd rekening met belangrijke tips en beperkingen om de prestaties te maximaliseren en veelvoorkomende problemen te voorkomen.

## Aanbevolen procedures {#section_86CF28C99CFF40329E4CBAFE4DD78BB4}

Hieronder vindt u de aanbevolen procedures voor het gebruik van de VEC:

### Plaats de verwijzing at.js bij de bovenkant van de `<head>` sectie van uw pagina.

+++Zie details
Als u ook [!UICONTROL Visitor API Service] gebruikt, plaatst u het API-script voor bezoekers boven at.js.

+++

### U kunt [!UICONTROL Enhanced Experience Composer] inschakelen op accountniveau (ingeschakeld voor alle activiteiten die in de account zijn gemaakt) of op het niveau van de individuele activiteit.

+++Zie details
Als u [!UICONTROL Enhanced Experience Composer] op accountniveau wilt inschakelen, klikt u op [!UICONTROL [!UICONTROL Administration] > [!UICONTROL Visual Experience Composer]] en schakelt u de [!UICONTROL Enable Enhanced Experience Composer] -schakelaar in op de Aan-positie.

Als u [!UICONTROL Enhanced Experience Composer] op activiteitsniveau wilt inschakelen terwijl u een activiteit maakt in de [!UICONTROL Visual Experience Composer] , klikt u op [!UICONTROL Configure > [!UICONTROL Page Delivery]] en schakelt u vervolgens de [!UICONTROL Enable Enhanced Experience Composer] -schakelaar in op de Aan-positie.

+++

### U kunt bepaalde IP-adressen lijsten van gewenste personen als [!UICONTROL Enhanced Experience Composer] niet wordt geladen op beveiligde pagina&#39;s op uw site.

+++Zie details
Problemen bij het laden van de [!UICONTROL Enhanced Experience Composer] kunnen worden opgelost door de volgende IP-adressen te voegend op lijst van gewenste personen. Deze IP-adressen zijn bedoeld voor [!DNL Adobe] -servers die worden gebruikt voor de [!UICONTROL Enhanced Experience Composer] -proxy. Ze zijn alleen vereist voor het bewerken van activiteiten. Bezoekers van uw site hebben deze op de lijst met gewenste personen staan IP-adressen niet nodig.

Voor meer informatie, zie [&#x200B; EEG geen interne QA URL laden die niet op openbare IP &#x200B;](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/troubleshooting-issues-related-to-the-enhanced-experience-composer-eec.md) in *kwesties van het Oplossen van problemen met betrekking tot de Verbeterde Composer van de Ervaring* toegankelijk is.

+++

### Gebruik unieke id&#39;s voor elementen op het hoogste niveau en andere elementen die geschikt kunnen zijn voor het testen of aanwijzen van kandidaten.

+++Details
Om het even welk onmiddellijk binnen het lichaamselement zou een unieke identiteitskaart moeten hebben. Als er nieuwe elementen in het lichaam worden geïnjecteerd en de code zich verplaatst, kunnen de bovenliggende elementen op zijn minst gemakkelijker worden herkend.

[!DNL Target] vereist geen id&#39;s, maar het gebruik van id&#39;s verhoogt de betrouwbaarheid van ervaringen die met de ervaringscomposer zijn gemaakt. [!DNL Target] gebruikt CSS-kiezers om uw inhoud te wijzigen wanneer de ervaring wordt opgeleverd. Wanneer u een ervaring bewerkt, verankert [!UICONTROL Visual Experience Composer] de kiezer aan de dichtstbijzijnde voorouder met een niet-null-id-kenmerk voor het HTML-element dat wordt gewijzigd. Het is daarom niet aan te raden een mechanisme te gebruiken, waaronder JavaScript-bibliotheken, waarmee HTML-id-kenmerken worden ingesteld of gewijzigd. Hoewel deze id&#39;s beschikbaar kunnen zijn voor de [!DNL Target] Experience-composer voor het maken van activiteiten, is de id die werd gebruikt toen de ervaring werd gemaakt mogelijk niet beschikbaar wanneer JavaScript id&#39;s wijzigt. Als er geen id beschikbaar is, mislukt de kiezer die aan de id is verankerd.

+++

### Geef CSS-klassen een naam, zodat ze gemakkelijk kunnen worden herkend.

+++Details
Wanneer u CSS-klassen bewerkt in de [!DNL Visual Experience Composer] , is het handig om de klassen eenvoudig te identificeren door beschrijvende klassennamen te gebruiken. Zo kunt u ervoor zorgen dat u de juiste CSS-klassen bewerkt en dat de pagina&#39;s er naar behoren uitzien.

Gebruik de CSS-eigenschap `!important` niet wanneer u elementen verbergt of verwijdert.

Als de CSS-eigenschap `!important` aanwezig is, worden wijzigingen die door `target.js` tijdens de levering worden aangebracht, overschreven door de CSS-regels van de site.

+++

### Gebruik geen HTML-tabellen voor paginalay-outs.

+++Details
[!DNL Target] gebruikt JavaScript om een pagina op te maken. Het is moeilijk om op tabellen gebaseerde lay-outs te wijzigen met JavaScript. Bovendien wordt op tabellen gebaseerde lay-outs mogelijk niet in alle browsers op dezelfde manier weergegeven. U bereikt de beste resultaten met CSS.

+++

### Maak zo weinig mogelijk gebruik van iFrames.

+++Details
Het is een goede praktijk om het gebruik van iFrames te minimaliseren, om pagina- en testbeheer te vereenvoudigen. Visual Experience Composer kan sommige acties binnen een iFrame toepassen, maar sommige acties, zoals het wijzigen van het formaat, werken niet correct. Het is moeilijk om pagina&#39;s met meerdere iFrames te beheren en de grootte ervan te wijzigen. Hierdoor kunnen het testen van iFrame-zware pagina&#39;s problemen veroorzaken.

+++

### Poging om alle dynamische DOM-wijzigingen zo snel mogelijk na DOM gereed te maken.

+++Details
Als uw wijzigingen niet worden toegepast voordat `target.js` de ervaringstoepassing uitvoert, kan de levering van de inhoud worden afgebroken. Dit gebeurt alleen wanneer de hiërarchie van een doelelement een DOM-wijziging bevat.

+++

### Gebruik alleen onbewerkte tekst of een afbeeldingstag in uw ankerelementen.

+++Details
`<a>Anchor Text</a>`

OF

`<a href=""> <img src=""> </img> </a>`

+++

### Vermijd blokelementen binnen een inline-element.

+++Details
Elementen op blokniveau mogen niet worden gebruikt binnen inline-elementen, zoals anker, bereik, enzovoort. Hierdoor gaan inline-elementen hun hoogte en breedte verliezen, zodat het overlaygereedschap in de [!UICONTROL Visual Experience Composer] mogelijk niet naar behoren werkt.

+++

### Gebruik de basistag in uw website niet om URL&#39;s en koppelingen op te lossen.

+++Details
VEC manipuleert de website achter de scènes, gebruikend een volmachtsserver die de verbindingen bijwerkt. Als u een basistag toevoegt, worden de URL&#39;s die door de proxyserver worden gebruikt, opnieuw door de browser opgelost en worden deze verbroken weergegeven.

+++

### Als u de DOM-structuur manipuleert met EDIT HTML, kunnen kiezers worden verbroken.

+++Details
Als u bijvoorbeeld twee handelingen hebt uitgevoerd:

* Een klasse toegevoegd aan Element 1
* HTML for Element 1 bewerkt

Elke verandering leidt tot een nieuw element in VEC. Omdat de tweede actie Element 1 wijzigt, als u Element 1 schrapt, heeft de tweede actie niet meer om het even wat te wijzigen, zodat werkt de verandering niet meer.

Met andere woorden, als u een element met tekst toevoegt, dan in een afzonderlijke actie bewerkt u dat element met verschillende tekst, toont de code redacteur beide acties als afzonderlijke elementen. Wanneer u het element hebt bewerkt, hebt u een nieuw element gemaakt dat het oorspronkelijke element wijzigt dat u hebt gemaakt en dat de bewerkte tekst bevat. Als u vervolgens het oorspronkelijke element verwijdert, kan de bewerkte tekst het bewerkte element niet vinden en wordt deze niet weergegeven. Het tweede element blijft in de lijst met elementen, maar heeft geen invloed op de pagina omdat het element dat wordt gewijzigd, niet meer bestaat.

Zie [&#x200B; die Selectors van het Element in [!UICONTROL Visual Experience Composer]](/help/main/c-experiences/c-visual-experience-composer/vec-selectors.md#concept_4EB7663E255F439B8D24079D23479337) worden gebruikt.

+++

### Gebruik de labels `<b>` en `<i>` wanneer u tekstelementen opmaakt met de RTF-editor.

+++Details
* Gebruik `<b>` in plaats van `<strong>` voor vette tekst.
* Gebruik `<i>` in plaats van `<em>` voor cursieve tekst.

`<strong>` - en `<em>` -tags kunnen leiden tot onverwachte resultaten.

+++

### Wees voorzichtig wanneer u formuliervelden verwijdert.

+++Details
Bepaalde formuliervelden kunnen verplicht zijn voor verzending. Het verwijderen van deze formuliervelden kan gevolgen hebben voor verzendingen.

+++

### Neem `mboxCreate` niet op in scripts.

+++Details
Omdat `mboxCreate` `document.write` gebruikt, wordt het niet aanbevolen `mboxCreate` in scripts op te nemen. Gebruik in plaats daarvan `mboxDefine` en `mboxUpdate` voor hetzelfde doel.

+++

### Werk een HTML-fragment niet bij met [!DNL Target] als hiervoor JavaScript-code vereist is.


+++Details
Wanneer een handeling (HTML bewerken) wordt uitgevoerd op paginacomponenten (zoals schuifregelaars, carrousels enzovoort), kan de aflevering verbroken lijken. VEC voert de actie uit nadat de paginacomponent door JavaScript is geconcretiseerd.

Wanneer de inhoud van de pagina echter aan bezoekers wordt afgeleverd, wordt de actie toegepast voordat de component wordt geïnstantieerd. Hierdoor kan de functionaliteit van deze component op het moment van levering al dan niet worden onderbroken. Functionaliteit is afhankelijk van de aard van het script dat op deze pagina wordt gebruikt om de component te definiëren.

Als u op levering test en het de eerste keer werkt, is het niet gewaarborgd dat het zal blijven werken. Er kan (of niet) een rasvoorwaarde zijn.

* Als er een rasvoorwaarde is, werkt de levering periodiek.
* Als er geen rasvoorwaarde is, werkt de levering altijd.

Test de pagina meerdere keren om te controleren of de levering naar behoren werkt.

+++

### Gebruik geen basistag op uw website om URL&#39;s en koppelingen op te lossen.

+++Details
Wanneer u [!UICONTROL Enhanced Experience Composer] gebruikt, wordt de website achter de scènes gemanipuleerd door een volmachtsserver die alle verbinding URLs bijwerkt om hen te maken in de volmacht werken. Als u een basiscode toevoegt, worden al deze URL&#39;s opgelost door de browser, zodat ze verbroken lijken.

+++

### Belangrijke tekst op de site die kan worden gebruikt als doel, moet in HTML-code binnen een element worden bewaard.

+++Details
U kunt de tekst Winkelwagentje bijvoorbeeld niet als doel instellen in de VEC als de code er als volgt uitziet:

```html
<a href="https://www.botanicchoice.com/shop.axd/Cart"> 
   <img alt="Shopping Cart"src="/images/ico-cart.gif"></img> 
   Shopping Cart: 
   <span id="HeaderCartQtyTotal">
      0 
  </span> 
  Items 
  <span id="HeaderCartPriceTotal"></span> 
</a>
```

In dit voorbeeld wordt het gehele ankerelement geselecteerd in de VEC, wat andere elementen nadelig beïnvloedt als het richten wordt uitgevoerd.

+++

### Gebruik `top` - of `self` -variabelen niet in JavaScript-code.

+++Details
Wanneer [!UICONTROL Enhanced Experience Composer] is ingeschakeld, worden de waarde van de bovenste en de zelfvariabelen bijgewerkt om het busten van iframe uit te schakelen. Gebruik een koptekst met X-frame opties om iframe-opwindingen toe te voegen in plaats van aangepaste JavaScript-codes.

+++

### Test altijd uw website als er parameters zijn toegevoegd bij het laden van de pagina.

+++Details
Als u bijvoorbeeld `www.abc.com` wilt openen, worden de volgende URL-parameters gebruikt:

`www.abc.com?mboxEdit=1&mboxDisable=1`

Deze parameters maken het bewerken in een iframe mogelijk.

Zorg ervoor dat uw website naar behoren wordt geladen nadat u dergelijke parameters hebt toegevoegd.

+++

### Zorg ervoor dat de pagina wordt geopend zoals u in een iframe hebt verwacht.

+++Details
Schakel iframe-opbouwtechnieken op uw website uit en controleer of de website wordt geopend zoals u had verwacht in een iframe op een dummypagina. Bijvoorbeeld:

```html
<!DOCTYPE 
<html> 
<html> 
<head> 
  <meta charset="utf-8"> 
  <meta name="viewport" content="width=device-width"> 
  <title>JS Bin</title> 
</head> 
<body> 
  <iframe src="https://www.homedepot.com"</iframe> 
</body> 
</html>
```

+++

## Caveats {#section_A0436B7B85BA467FA9DE13A9A40E6A6E}

Houd rekening met het volgende wanneer u [!UICONTROL Visual Experience Composer] gebruikt om uw activiteit te ontwerpen.

### De functie [!UICONTROL Move] biedt geen ondersteuning voor Z-index.

+++Details
Omdat er geen Z-indexfunctionaliteit is, kan het verplaatste element niet boven op een ander element worden geplaatst. Zie [&#x200B; Beperkingen &#x200B;](/help/main/c-experiences/c-visual-experience-composer/experience-composer-best-practices.md#section_F33C2EA27F2E417AA036BC199DD6C721) voor meer details.

+++

### Het opnieuw rangschikken van elementen beïnvloedt klik het volgen.

+++Details
Als een element dat is gemarkeerd voor klikken bijhouden opnieuw wordt gerangschikt, worden de paden van de opnieuw gerangschikte elementen gewijzigd. Het resultaat is dat het element op de locatie waar het oorspronkelijke element zich bevond voordat het werd herschikt, het element is waarvan de klikken worden bijgehouden.

Dit komt voor omdat zowel de code om de activiteiteninhoud te leveren als de code om kliks te volgen in één stuk van code inbegrepen is die aan de pagina wordt geleverd. Als u naar een andere pagina bladert en instelt klikt op bijhouden, worden de code voor de activiteiteninhoud en de code voor het bijhouden van klikken naar die pagina verzonden. Als de pagina voor het bijhouden van klikken een vergelijkbare paginastructuur heeft als de pagina waarop de test wordt uitgevoerd, wordt de testinhoud mogelijk ook weergegeven op de pagina voor het bijhouden van klikken.

+++

### Het invoegen van een element werkt mogelijk niet in een `<div>` -vak.

+++Details
Als een mbox een aanbieding bevat, kan het opnemen van een element verschijnen als `insertBefore` en niet `insertAfter`, als mbox verkeerd wordt uitgevoerd.

+++

### Wanneer u zowel een bovenliggend element als een onderliggend element bewerkt, moet u eerst het bovenliggende element bewerken.

+++Details
Als u een afbeeldingsactie op een element omwisselt en vervolgens de tekst of HTML op het bovenliggende element bewerkt, kunnen zich leveringsproblemen voordoen. De beste workflow is om het bovenliggende element te bewerken voordat de afbeelding op het onderliggende element wordt gewisseld.

+++

### Kan geen pagina-element selecteren dat een box als onderliggend element bevat.

+++Details
Als uw pagina bijvoorbeeld het volgende bevat:

```html
<div> 
  <div class="mboxDefault" > 
  </div>
  <script>mboxCreate('myMbox'); 
</div>`
```

De buitenste div moet tijdens een bewerking niet worden geselecteerd omdat de in de pagina gecodeerde mbox nog steeds een aanroep naar [!DNL Target] maakt en een reactie ontvangt. Deze reactie beïnvloedt de reactie voorgenomen voor het grotere paginaelement.

+++

### IPs van de volmacht zou in klantenmilieu kunnen worden geblokkeerd.

+++Details
Als u [!UICONTROL Enhanced Experienced Composer] gebruikt op een niet live site, zoals een testomgeving, ziet u mogelijk time-outs en toegangsontzegde fouten als uw site RIP&#39;s blokkeert.

+++

## Beperkingen {#section_F33C2EA27F2E417AA036BC199DD6C721}

Houd rekening met de volgende beperkingen wanneer u met de VEC werkt:

### VEC-compatibiliteit met [!DNL Chrome] beleidswijzigingen voor extensies verwerken. {#ext}

+++Details
Wegens bijgewerkt [&#x200B; V3 Manifest beleid in Google Chrome &#x200B;](https://developer.chrome.com/docs/extensions/develop/migrate/what-is-mv3){target=_blank}, kunnen de uitbreidingen originele DOM niet meer wijzigen alvorens het door browser wordt ontleed. Dientengevolge, zouden bepaalde veiligheidsmanuscripten-zoals iframe-het bouwen implementaties-pagina&#39;s van het laden in VEC kunnen blokkeren.

Om de compatibiliteit te garanderen, moeten deze scripts voorwaardelijk worden uitgeschakeld wanneer de pagina in het iframe [!DNL Target] wordt geladen. Dit proces kan veilig worden uitgevoerd door te controleren op de aanwezigheid van het `window.adobeVecExtension` -object, dat door [!DNL Target] tijdens het laden met VEC wordt geïnjecteerd.

De volgende codefragmenten zijn voorbeelden van iFrame-bosting code die tot Web-pagina kan leiden die niet in VEC laadt:

`window.top.location = window.self.location;`

`top.location.href = self.location.href;`

Met een eenvoudige controle kunt u controleren of een webpagina is ingesloten in [!DNL Target] . Een codefragment moet er als volgt uitzien:

```
if(!window.adobeVecExtension) {
    // additional security logic
}
```

+++

### U kunt een element niet buiten een container plaatsen, gevolgd door een CSS-eigenschap.

+++Details
Een element kan niet worden verplaatst buiten een container die wordt gevolgd door een CSS-eigenschap.

+++

### U kunt het [!UICONTROL Button] -element niet selecteren voor herschikking.

+++Details
[!UICONTROL Button] -elementen kunnen niet rechtstreeks worden geselecteerd voor herschikking. Plaats knoppen in een grotere container om herschikking in te schakelen.

+++

### Alleen wisselvoorstellen zijn beschikbaar op vakjes.

+++Details
Handelingen als [!UICONTROL Edit Class] en [!UICONTROL Rearrange] zijn niet toegestaan binnen een box.

+++

### U moet niet hetzelfde element opnieuw rangschikken en verplaatsen.

+++Details
Als een element naar een andere plaats is verplaatst, en u de oudercontainer selecteert en probeert om de kindelementen opnieuw te rangschikken, wordt het verplaatste element niet beïnvloed en blijft waar het is. De herschikking wordt mogelijk niet naar wens weergegeven.

+++

### De handeling [!UICONTROL Change Image] werkt niet op een afbeelding in een carrousel.

+++Details
Als uw pagina bijvoorbeeld een carrousel met zes afbeeldingen bevat en u een afbeelding wilt omwisselen met de tweede afbeelding van de carrousel, werkt de handeling [!UICONTROL Change Image] niet.

Als tussenoplossing kunt u de bovenliggende container selecteren en de handeling [!UICONTROL Edit HTML] gebruiken om de HTML van de carrousel te bewerken en de afbeeldingsbron van de gewenste afbeelding bij te werken.

+++

### Afbeeldingen kunnen niet worden vergroot of verkleind in een box.

+++Details
Als u een afbeelding in een mbox-element omwisselt en u probeert de grootte van die afbeelding aan te passen aan de grootte van het mbox-element, is het wijzigen van de grootte niet toegestaan.

+++

### Nadat u een afbeelding hebt gewisseld, kunt u de handeling [!UICONTROL Edit] niet meer selecteren.

+++Details
Nadat u het beeld ruilt, kunt u niet Scene7 URL uitgeven.

+++

### HTML-elementen met een externe bron kunnen niet worden bewerkt.

+++Details
Bijvoorbeeld: video, audiotags, embed, iFrames, frames.

+++

### Klik op Tekstspatiëring voor ankerelementen die andere elementen bevatten dan onbewerkte tekst of afbeeldingstags.

+++Details
Klik bijvoorbeeld op bijhouden als het element JavaScript bevat.

+++

### De pagina&#39;s moeten URL parameters voor VEC goedkeuren om te werken.

+++Details
Sommige sites verwijderen URL-parameters voor hun pagina&#39;s. De VEC vereist deze parameters echter.

+++

### Wanneer u een script gebruikt als onderdeel van HTML, moeten alle variabelen en functies die van buiten worden benaderd, worden gedeclareerd onder de vensternaamruimte.

+++Details
Het script wordt uitgevoerd binnen het bereik van `target.js` nadat de pagina is geladen. Daarom is elke variabele of functie die lokaal is gedeclareerd, niet toegankelijk van buiten het scriptblok.

*Onjuist:*

```html
<script> 
  var myVar = 123; 
  function myFunc() { 
    // 
  } 
</script>`
```

*Correct:*

```html
<script> 
  window.myVar = 123; 
  window.myFunc = function() { 
    // 
  }; 
</script>
```

+++

### Wanneer u een afbeelding invoegt uit de [!UICONTROL Content] -bibliotheek (Scene7) en de HTML bewerkt, wordt de URL van de afbeelding verbroken.

+++Details
Voeg een ankerelement in het div &#39;customHeaderMessage&#39; met een dummytekst toe:

```html
<a href="#"> 
<span> Dummy text </span>
</a>
```

Selecteer dit div-element met de handeling [!UICONTROL Insert Element] om een afbeelding in te voegen als een sibling van dit dummy-tekstdiv.

Na het invoegen van de afbeelding ziet het er als volgt uit:

```html
<a href="#">  
<span> Dummy text </span> 
<img src=""> This is inserted Image. </img> 
</a>
```

Verwijder het dummytekstbereik.

+++

### De handeling `customCode` in de VEC werkt niet met [!DNL Internet Explorer] 8.

+++Details
Vanwege IE8-beperkingen bij het verwerken van scriptinhoud, biedt `target.js` geen ondersteuning voor dit probleem in IE8. Als tussenoplossing kan `target.js` de handeling `customCode` afleveren als de pagina jQuery bevat en algemeen beschikbaar wordt gemaakt voor het vensterobject. Zorg ervoor dat `window.jQuery` en `window.jQuery.fn.prepend` zijn gedefinieerd.

+++

### Klik op Tekstspatiëring wordt alleen ondersteund op de pagina waarop ervaringen zijn gemaakt of op de omgeleide pagina.

+++Details
Hoewel de modus [!UICONTROL Browse] beschikbaar is voor klikken op bijhouden in de VEC, kan de modus [!UICONTROL Browse] niet worden gebruikt voor het toevoegen van klikken op bijhouden op een pagina.

+++
