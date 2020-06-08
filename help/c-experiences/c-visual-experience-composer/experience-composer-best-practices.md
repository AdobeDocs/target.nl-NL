---
keywords: visual experience composer;visual experience composer best practices;visual experience composer limitations;visual experience composer caveats;vec best practices;vec
description: De volgende best practices kunnen u helpen uw ervaringen naar behoren te laten werken. Er zijn ook andere uiteinden en beperkingen die u van bewust zou moeten zijn wanneer het gebruiken van Visual Experience Composer (VEC).
title: Aanbevolen werkwijzen en beperkingen voor composer visuele ervaring
topic: Classic
uuid: 8d1d199b-b3d7-4edb-ba05-bd97372a0b9e
translation-type: tm+mt
source-git-commit: cf69c1d8472088d5f6a6b7250bedd1048cac5c10
workflow-type: tm+mt
source-wordcount: '2442'
ht-degree: 0%

---


# Aanbevolen werkwijzen en beperkingen voor composer visuele ervaring{#visual-experience-composer-best-practices-and-limitations}

De volgende best practices kunnen u helpen uw ervaringen naar behoren te laten werken. Er zijn ook andere uiteinden en beperkingen die u van bewust zou moeten zijn wanneer het gebruiken van Visual Experience Composer (VEC).

Door deze beste praktijken te volgen, zult u minder waarschijnlijk onverwachte problemen met de ervaringen ontmoeten u ontwerpt.

## Aanbevolen werkwijzen {#section_86CF28C99CFF40329E4CBAFE4DD78BB4}

**Voor mbox.js versie 57 en later, en voor at.js, plaats mbox.js of bij.js verwijzing bij de bovenkant van de`<head>`sectie van uw pagina.**

Als u ook de Bezoeker-API-service gebruikt, plaatst u het bezoeker-API-script boven mbox.js of at.js.

**Voor versies van mbox.js vóór versie 57 plaatst u de code mbox.js zo laag mogelijk in de`<head>`sectie van uw pagina.**

Plaats mbox.js aan het eind van de `<head>` sectie, zonder extra verklaringen na het. Anders worden alle script- of koppelingstags naar de `<body>` sectie verplaatst.

**U kunt de Enhanced Experience Composer inschakelen op accountniveau (ingeschakeld voor alle activiteiten die in de account zijn gemaakt) of op het niveau van de individuele activiteit.**

Om Verbeterde Composer van de Ervaring op het rekeningsniveau toe te laten, klik [!UICONTROL Setup > Preferences], dan knevel de schakelaar aan positie.

Om Verbeterde Composer van de Ervaring op het activiteitenniveau toe te laten terwijl het creëren van een activiteit in Visuele Composer van de Ervaring, klik [!UICONTROL Configure > URL], dan knevel de schakelaar aan positie aan.

**U kunt bepaalde IP adressen toestaan als de Verbeterde Composer van de Ervaring geen op veilige pagina&#39;s op uw plaats zal laden.**

De problemen die Verbeterde Visuele Composer van de Ervaring laden kunnen worden opgelost door de volgende IP adressen toe te staan. Deze IP-adressen zijn bestemd voor de Adobe-server die wordt gebruikt voor de Enhanced Experience Composer-proxy. Ze zijn alleen vereist voor het bewerken van activiteiten. Bezoekers van uw site hebben deze IP-adressen niet nodig.

Verenigde Staten: 52.55.99.45, 54.80.158.92 en 54.204.197.253

Europa, Midden-Oosten en Afrika (EMEA): 52.51.238.221, 52.210.1994.44 en 54.72.56.50

Azië-Stille Oceaan (APAC): 52.193.67.35, 54.199.198.109 en 54.199.241.57

**Gebruik unieke id&#39;s voor elementen op het hoogste niveau en andere elementen die geschikt kunnen zijn voor het testen of aanwijzen van kandidaten.**

Om het even welk onmiddellijk binnen het lichaamselement zou een unieke identiteitskaart moeten hebben. Als er nieuwe elementen in het lichaam worden geïnjecteerd en de code zich verplaatst, kunnen de bovenliggende elementen op zijn minst gemakkelijker worden herkend.

Voor Adobe Target zijn geen id&#39;s vereist, maar het gebruik van id&#39;s verhoogt de betrouwbaarheid van ervaringen die met de ervaringscomposer zijn gemaakt. Doel gebruikt CSS-kiezers om uw inhoud te wijzigen wanneer de ervaring wordt opgedaan. Wanneer u een ervaring uitgeeft, verankert de Visuele Composer van de Ervaring de selecteur aan de dichtstbijzijnde voorvader met een niet-krachteloze identiteitskaart attribuut aan het element dat van HTML wordt gewijzigd. Het is daarom niet aan te raden om een mechanisme te gebruiken, inclusief JavaScript-bibliotheken, waarmee HTML-id-kenmerken worden ingesteld of gewijzigd. Hoewel deze id&#39;s beschikbaar kunnen zijn voor de doelervaringscomposer voor het maken van activiteiten, is de id die werd gebruikt toen de ervaring werd gemaakt mogelijk niet beschikbaar wanneer de ervaring wordt uitgevoerd als JavaScript ID&#39;s wijzigt. Als er geen id beschikbaar is, mislukt de kiezer die aan de id is verankerd.

**Geef CSS-klassen een naam, zodat ze gemakkelijk kunnen worden herkend.**

Wanneer het uitgeven van CSS klassen in Visual Experience Composer, is het nuttig om de klassen gemakkelijk te maken zich door beschrijvende klassennamen te gebruiken gemakkelijk te identificeren. Zo kunt u ervoor zorgen dat u de juiste CSS-klassen bewerkt en dat de pagina&#39;s er naar behoren uitzien.

Gebruik de `!important` CSS-eigenschap niet wanneer u elementen verbergt of verwijdert.

Als de 1!Belangrijke1 CSS-eigenschap aanwezig is, worden wijzigingen die door target.js tijdens de levering worden aangebracht, overschreven door de CSS-regels van de site.

**Gebruik geen HTML-tabellen voor paginalay-outs.**

De Standaard en de Premium van het doel gebruiken JavaScript om een pagina te formatteren. Het is moeilijk om op tabellen gebaseerde lay-outs te wijzigen met JavaScript. Bovendien wordt op tabellen gebaseerde lay-outs mogelijk niet in alle browsers op dezelfde manier weergegeven. U bereikt de beste resultaten met CSS.

**Maak zo weinig mogelijk gebruik van iFrames.**

Het is een goede praktijk om het gebruik van iFrames te minimaliseren, om pagina- en testbeheer te vereenvoudigen. De visuele ervaringscomposer kan sommige acties binnen een iFrame toepassen, maar sommige acties, zoals het wijzigen van het formaat, werken niet correct. Het is moeilijk om pagina&#39;s met meerdere iFrames te beheren en de grootte ervan te wijzigen. Hierdoor kunnen het testen van iFrame-zware pagina&#39;s problemen veroorzaken.

**Poging om alle dynamische DOM-wijzigingen zo snel mogelijk na DOM gereed te maken.**

Als uw wijzigingen niet worden toegepast voordat de ervaringstoepassing door target.js wordt uitgevoerd, kan de levering van inhoud worden afgebroken. Dit gebeurt alleen wanneer de hiërarchie van een doelelement een DOM-wijziging bevat.

**Gebruik alleen onbewerkte tekst of een afbeeldingstag in uw ankerelementen.**

`<a>Anchor Text</a>`

OF

`<a href=""> <img src=""> </img> </a>`

**Vermijd blokelementen binnen een inline-element.**

Elementen op blokniveau mogen niet worden gebruikt binnen inline-elementen, zoals anker, bereik, enzovoort. Dit veroorzaakt inline elementen om hun hoogte en breedte te verliezen, zodat zou het bekledingshulpmiddel in Visuele Composer van de Ervaring niet kunnen werken zoals verwacht.

**Gebruik de basistag in uw website niet om URL&#39;s en koppelingen op te lossen.**

De visuele Composer van de Ervaring manipuleert de website achter de scènes, gebruikend een volmachtsserver die de verbindingen bijwerkte. Als u een basistag toevoegt, worden de URL&#39;s die door de proxyserver worden gebruikt, opnieuw door de browser opgelost en worden deze verbroken weergegeven.

**Als u HTML BEWERKEN gebruikt om de DOM-structuur te bewerken, kunnen kiezers worden verbroken.**

Als u bijvoorbeeld twee handelingen hebt uitgevoerd:

* Een klasse toegevoegd aan Element 1
* De HTML voor Element 1 is bewerkt

Elke verandering leidt tot een nieuw element in de Visuele Composer van de Ervaring. Omdat de tweede actie Element 1 wijzigt, als u Element 1 schrapt, heeft de tweede actie niet meer om het even wat te wijzigen, zodat werkt de verandering niet meer.

Met andere woorden, als u een element met tekst toevoegt, dan in een afzonderlijke actie bewerkt u dat element met verschillende tekst, toont de code redacteur beide acties als afzonderlijke elementen. Wanneer u het element hebt bewerkt, hebt u een nieuw element gemaakt dat het oorspronkelijke element wijzigt dat u hebt gemaakt en dat de bewerkte tekst bevat. Als u vervolgens het oorspronkelijke element verwijdert, kan de bewerkte tekst het bewerkte element niet vinden en wordt deze niet weergegeven. Het tweede element blijft in de lijst met elementen, maar heeft geen invloed op de pagina omdat het element dat wordt gewijzigd, niet meer bestaat.

Zie [Elementkiezers die worden gebruikt in de Visual Experience Composer](../../c-experiences/c-visual-experience-composer/vec-selectors.md#concept_4EB7663E255F439B8D24079D23479337) .

**Gebruik`<b>`en`<i>`labels wanneer u tekstelementen opmaakt met de RTF-editor.**

* Gebruik voor vette tekst `<b>` in plaats van `<strong>`.
* Gebruik voor cursieve tekst `<i>` in plaats van `<em>`.

`<strong>` en `<em>` -tags onverwachte resultaten kunnen veroorzaken.

**Wees voorzichtig wanneer u formuliervelden verwijdert.**

Bepaalde formuliervelden kunnen verplicht zijn voor verzending. Het verwijderen van deze formuliervelden kan gevolgen hebben voor verzendingen.

**Neem geen`mboxCreate`deel aan scripts.**

Omdat dit `mboxCreate` wordt gebruikt, wordt het niet aangeraden om deze `document.write``mboxCreate` in scripts op te nemen. Gebruik in plaats daarvan `mboxDefine` en `mboxUpdate` voor hetzelfde doel.

**Werk een HTML-fragment niet bij met behulp van Target Standard als hiervoor JavaScript-code vereist is voor initialisatie.**

Wanneer een handeling (HTML bewerken) wordt uitgevoerd op paginacomponenten (zoals Schuifregelaars, Carrousels enzovoort), kan de levering afgebroken lijken. Visual Experience Composer voert de actie uit nadat de paginacomponent door JavaScript is geconcretiseerd.

Wanneer de inhoud van de pagina echter aan bezoekers wordt afgeleverd, wordt de actie toegepast voordat de component wordt geïnstantieerd. Hierdoor kan de functionaliteit van deze component op het moment van levering al dan niet worden onderbroken. Functionaliteit is afhankelijk van de aard van het script dat op deze pagina wordt gebruikt om de component te definiëren.

Als u op levering test en het de eerste keer werkt, is het niet gewaarborgd dat het zal blijven werken. Er kan (of niet) een rasvoorwaarde zijn.

* Als er een rasvoorwaarde is, zal de levering periodiek werken.
* Als er geen rassenvoorwaarde is, zal het altijd werken.

Test de pagina meerdere keren om te controleren of de levering naar behoren werkt.

**Gebruik geen basistag op uw website om URL&#39;s en koppelingen op te lossen.**

Wanneer u de Enhanced Experience Composer gebruikt, wordt de website achter de schermen gemanipuleerd door een proxyserver die alle koppelings-URL&#39;s bijwerkt zodat deze in de proxy werken. Als u een basiscode toevoegt, worden al deze URL&#39;s opgelost door de browser zodat ze worden verbroken.

**Belangrijke tekst op de site die kan worden gebruikt als doel, moet worden opgeslagen in HTML-code binnen een element.**

U kunt de tekst Winkelwagentje bijvoorbeeld niet als doel instellen in de VEC als de code er als volgt uitziet:

```
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

In dit voorbeeld wordt het gehele ankerelement geselecteerd in de VEC. Dit heeft een negatief effect op andere elementen als het doel wordt uitgevoerd.

**Gebruik geen`top`of`self`variabelen in JavaScript-code.**

Wanneer de Enhanced Experience Composer is ingeschakeld, worden de waarde van de bovenste en de zelfvariabelen bijgewerkt om iframe busting uit te schakelen. Gebruik een koptekst met X-frame opties om iframe busting toe te voegen in plaats van aangepaste JavaScript-codes.

**Test altijd uw website als er parameters zijn toegevoegd bij het laden van de pagina.**

Als u bijvoorbeeld www.abc.com wilt openen, worden de volgende URL-parameters gebruikt:

`www.abc.com?mboxEdit=1&mboxDisable=1`

Deze parameters maken het bewerken in een iframe mogelijk.

Zorg ervoor dat uw website naar behoren wordt geladen nadat u dergelijke parameters hebt toegevoegd.

**Zorg ervoor dat de pagina wordt geopend zoals u in een iframe hebt verwacht.**

Schakel de technieken voor het opbouwen van iframe op uw website uit en controleer of deze wordt geopend zoals u had verwacht in een iframe op een dummypagina. Bijvoorbeeld:

```
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

## Caveats {#section_A0436B7B85BA467FA9DE13A9A40E6A6E}

Overweeg de volgende bedenkingen wanneer het gebruiken van de Visuele Composer van de Ervaring om uw activiteit te ontwerpen.

**De functie Verplaatsen ondersteunt geen Z-index.**

Omdat er geen Z-indexfunctionaliteit is, kan het verplaatste element niet boven op een ander element worden geplaatst. Zie [Beperkingen](../../c-experiences/c-visual-experience-composer/experience-composer-best-practices.md#section_F33C2EA27F2E417AA036BC199DD6C721) voor meer informatie.

**Het opnieuw rangschikken van elementen beïnvloedt klik het volgen.**

Als een element dat is gemarkeerd voor klikken bijhouden opnieuw wordt gerangschikt, worden de paden van de opnieuw gerangschikte elementen gewijzigd. Het resultaat is dat het element op de locatie waar het oorspronkelijke element zich bevond voordat het werd herschikt, het element is waarvan de klikken worden bijgehouden.

Dit komt voor omdat zowel de code om de activiteiteninhoud te leveren als de code om kliks te volgen in één stuk van code inbegrepen is die aan de pagina wordt geleverd. Als u naar een andere pagina bladert en instelt klikt op bijhouden, worden de code voor de activiteiteninhoud en de code voor het bijhouden van klikken naar die pagina verzonden. Als de pagina voor het bijhouden van klikken een vergelijkbare paginastructuur heeft als de pagina waarop de test wordt uitgevoerd, wordt de testinhoud mogelijk ook weergegeven op de pagina voor het bijhouden van klikken.

**Het invoegen van een element werkt mogelijk niet in een`<div>`mbox.**

Als een mbox een aanbieding bevat, kan het opnemen van een element als insertBefore en niet insertAfter verschijnen, als mbox verkeerd wordt uitgevoerd.

**Wanneer u zowel een bovenliggend element als een onderliggend element bewerkt, moet u eerst het bovenliggende element bewerken.**

Als u een afbeeldingsactie op een element omwisselt en de tekst of HTML op het bovenliggende element bewerkt, kunnen zich leveringsproblemen voordoen. De beste workflow is om het bovenliggende element te bewerken voordat de afbeelding op het onderliggende element wordt gewisseld.

**Kan geen pagina-element selecteren dat een box als onderliggend element bevat.**

Als uw pagina bijvoorbeeld het volgende bevat:

```
<div> 
  <div class="mboxDefault" > 
  </div>
  <script>mboxCreate('myMbox'); 
</div>`
```

De buitenste div zou niet in een ervaring moeten worden geselecteerd omdat mbox hardcoded in de pagina nog een vraag aan Doel maakt en een reactie ontvangt. Deze reactie beïnvloedt de reactie voorgenomen voor het grotere paginaelement.

**IPs van de volmacht kan in klantenmilieu worden geblokkeerd.**

Als u Uitgebreide Ervaren Composer op een niet levende plaats, zoals het opvoeren milieu gebruikt, zou u onderbrekingen en de toegang ontkende fouten kunnen zien als uw plaats RIPs blokkeert.

**Wanneer u meerdere pagina&#39;s toevoegt, worden zowel de rail als de paginalijn tegelijkertijd geopend. Dit vermindert uiteindelijk de breedte voor de Visuele Composer van de Ervaring om de plaats voor optimalisaties te tonen. Hierdoor kunnen herplaatsbare sites er anders uitzien dan u had verwacht in de beperkte ruimte.**

De oplossing is het samenvouwen van de ervarings- en paginalijn door op de linker chevron-pictogrammen bovenaan te klikken.

## Beperkingen {#section_F33C2EA27F2E417AA036BC199DD6C721}

**Functie Verplaatsen**

Een element kan niet worden verplaatst buiten een container die wordt gevolgd door een CSS-eigenschap.

**Alleen wisselvoorstellen zijn beschikbaar op vakjes.**

Handelingen zoals Klasse bewerken en opnieuw rangschikken zijn niet toegestaan in een kader. Mbox-inhoud wordt aangeboden door mbox.js.

**U moet niet hetzelfde element opnieuw rangschikken en verplaatsen.**

Als een element naar een andere plaats is verplaatst, en u de oudercontainer selecteert en probeert om de kindelementen opnieuw te rangschikken, wordt het verplaatste element niet beïnvloed en blijft waar het is. De herschikking wordt mogelijk niet naar wens weergegeven.

**Handeling Afbeelding wisselen werkt niet op een afbeelding in een carrousel.**

Als uw pagina bijvoorbeeld een carrousel met zes afbeeldingen bevat en u een afbeelding wilt wisselen met de tweede afbeelding van de carrousel, werkt de actie Afbeelding wisselen niet.

Als tussenoplossing kunt u de bovenliggende container selecteren en de handeling HTML bewerken gebruiken om de HTML van de carrousel te bewerken en de afbeeldingsbron van de gewenste afbeelding bij te werken.

**Afbeeldingen kunnen niet worden vergroot of verkleind in een box.**

Als u een afbeelding in een mbox-element omwisselt en u probeert de grootte van die afbeelding aan te passen aan de grootte van het mbox-element, is het wijzigen van de grootte niet toegestaan.

**Nadat u een afbeelding hebt gewisseld, kunt u de handeling Bewerken niet meer selecteren.**

Nadat u het beeld ruilt, kunt u niet Scene7 URL uitgeven.

**HTML-elementen met externe bron kunnen niet worden bewerkt.**

Bijvoorbeeld: video, audiotags, embed, iFrames, frames.

**Klik op Tekstspatiëring voor ankerelementen die andere elementen bevatten dan onbewerkte tekst of afbeeldingstags.**

Klik bijvoorbeeld op bijhouden werkt niet als het element JavaScript bevat.

**De pagina&#39;s moeten parameters URL voor de Visuele Composer van de Ervaring goedkeuren om te werken.**

Sommige sites verwijderen URL-parameters voor hun pagina&#39;s. Nochtans, vereist de Visuele Composer van de Ervaring die parameters.

**Tijdens het gebruik van een script als onderdeel van html, moeten alle variabelen en functies die van buiten worden benaderd, worden gedeclareerd onder vensternaamruimte.**

Het script wordt uitgevoerd binnen het bereik van target.js nadat de pagina is geladen. Daarom is elke variabele of functie die lokaal is gedeclareerd, niet toegankelijk van buiten het scriptblok.

*Onjuist:*

```
<script> 
  var myVar = 123; 
  function myFunc() { 
    // 
  } 
</script>`
```

*Juist:*

```
<script> 
  window.myVar = 123; 
  window.myFunc = function() { 
    // 
  }; 
</script>
```

**Wanneer u een afbeelding invoegt uit de inhoudsbibliotheek (Scene7) en de HTML bewerkt, wordt de afbeeldings-URL verbroken.**

Voeg een ankerelement in het div &#39;customHeaderMessage&#39; met een dummytekst toe:

```
<a href="#"> 
<span> Dummy text </span>
</a>
```

Selecteer dit div met de handeling Element invoegen om een afbeelding in te voegen als een sibling van dit dummy-tekstdiv.

Na het invoegen van de afbeelding ziet het er als volgt uit:

```
<a href="#">  
<span> Dummy text </span> 
<img src=""> This is inserted Image. </img> 
</a>
```

Verwijder het dummytekstbereik.

**De actie customCode in de Visuele Composer van de Ervaring werkt niet met Internet Explorer 8.**

Vanwege IE8-beperkingen bij het verwerken van scriptinhoud, biedt target.js geen ondersteuning voor dit probleem in IE8. Als tussenoplossing kan target.js de handeling customCode leveren als de pagina jQuery bevat en globaal beschikbaar wordt gemaakt voor het vensterobject. Zorg ervoor dat window.jQuery en window.jQuery.fn.prepend zijn gedefinieerd.

**Klik op Tekstspatiëring wordt alleen ondersteund op de pagina waarop ervaringen zijn gemaakt of op de omgeleide pagina.**

Hoewel de Browse wijze in Klik Spoor VEC beschikbaar is, kan het niet worden gebruikt om klik het volgen op een pagina toe te voegen.
