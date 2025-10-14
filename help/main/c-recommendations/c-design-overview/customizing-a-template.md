---
keywords: aangepast ontwerp;snelheid;decimaal;komma;ontwerp aanpassen
description: Leer hoe te om de open-bron  [!DNL Velocity]  ontwerptaal te gebruiken om aanbevelingsontwerpen in  [!DNL Target]  Aanbevelingen aan te passen.
title: Hoe pas ik een ontwerp aan gebruikend snelheid?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=nl-NL#premium newtab=true" tooltip="Kijk wat er in Target Premium is opgenomen."
feature: Recommendations
exl-id: 035d7988-80d8-4080-bb0d-1d0e9f8856d1
source-git-commit: eba9e0b02ce74fea127d2cb2d08d04dcd2da2d76
workflow-type: tm+mt
source-wordcount: '1049'
ht-degree: 0%

---

# Een ontwerp aanpassen met [!DNL Velocity]

Gebruik de ontwerptaal open-source [!DNL Velocity] om aanbevelingsontwerpen aan te passen in [!DNL Adobe Target Recommendations] .

## [!DNL Velocity] overzicht {#section_C431ACA940BC4210954C7AEFF6D03EA5}

De informatie over [!DNL Velocity] kan in [&#x200B; https://velocity.apache.org &#x200B;](https://velocity.apache.org) worden gevonden.

Alle [!DNL Velocity] -logica, -syntaxis, enzovoort kunnen worden gebruikt voor een aanbevolen ontwerp. Dit betekent dat u *voor* lijnen, *kunt tot stand brengen als* verklaringen, en andere code gebruikend [!DNL Velocity] eerder dan JavaScript.

Entiteitskenmerken die naar [!DNL Recommendations] worden verzonden in de `productPage` mbox of de CSV-upload, kunnen in een ontwerp worden weergegeven, met uitzondering van &quot;multi-value&quot;-kenmerken. Elk type kenmerk kan worden verzonden, maar [!DNL Target] geeft geen kenmerken van het type &quot;multi-value&quot; door als een array die door een sjabloon kan worden herhaald (bijvoorbeeld `entityN.categoriesList` ).

Naar deze waarden wordt verwezen met de volgende syntaxis:

```
$entityN.variable
```

Namen van entiteitskenmerken moeten volgen op [!DNL Velocity] stenornotatie, die bestaat uit een voorloopteken *$* , gevolgd door een id voor [!DNL Velocity] Sjabloontaal (VTL). De VTL-id moet beginnen met een alfabetisch teken (a-z of A-Z).

Namen van kenmerken van snelheidsentiteiten zijn beperkt tot de volgende typen tekens:

* Alfabetisch (a-z, A-Z)
* Numeriek (0-9)
* Afbreekstreepje ( - )
* Onderstrepingsteken ( _ )

De volgende kenmerken zijn beschikbaar als [!DNL Velocity] -arrays. Als zodanig kunnen ze worden herhaald of via index naar ze worden verwezen.

* `entities`
* `entityN.categoriesList`

Bijvoorbeeld:

```
#foreach ($category in $entity1.categoriesList) 
<br/>$category 
#end
```

of

```
#if ($entities[0].categoriesList.size() >= 3 ) 
$entities[0].categoriesList[2] 
#end
```

Voor meer informatie over [!DNL Velocity] variabelen (attributen), zie [&#x200B; https://velocity.apache.org/engine/releases/velocity-1.7/user-guide.html#variables &#x200B;](https://velocity.apache.org/engine/releases/velocity-1.7/user-guide.html#variables).

Als u een profielscript in uw ontwerp gebruikt, moet $ voorafgaand aan de scriptnaam met een `\` (backslash) worden beschermd. Bijvoorbeeld:

`\${user.script_name}`

>[!NOTE]
>
>Het maximumaantal entiteiten waarnaar in een ontwerp kan worden verwezen, hard-gecodeerd of via lussen, is 99. De lengte van het sjabloonscript kan maximaal 65.000 tekens bevatten.

Als u bijvoorbeeld een ontwerp wilt dat iets dergelijks weergeeft:

![&#x200B; snelheid_example beeld &#x200B;](assets/velocity_example.png)

u kunt de volgende code gebruiken:

```
<table style="border:1px solid #CCCCCC;"> 
<tr> 
<td colspan="3" style="font-size: 130%; border-bottom:1px solid  
#CCCCCC;"> You May Also Like... </td> 
</tr> 
<tr> 
<td style="border-right:1px solid #CCCCCC;"> 
<div class="search_content_inner" style="border-bottom:0px;"> 
<div class="search_title"><a href="$entity1.pageUrl"  
style="color: rgb(112, 161, 0); font-weight: bold;"> 
$entity1.id</a></div> 
By $entity1.message <a href="?x14=brand;q14=$entity1.message"> 
(More)</a><br/> 
sku: $entity1.prodId<br/> Price: $$entity1.value 
<br/><br/> 
</div> 
</td> 
<td style="border-right:1px solid #CCCCCC; padding-left:10px;"> 
<div class="search_content_inner" style="border-bottom:0px;">  
<div class="search_title"><a href="$entity2.pageUrl"  
style="color: rgb(112, 161, 0); font-weight: bold;"> 
$entity2.id</a></div> 
By $entity2.message <a href="?x14=brand;q14=$entity2.message"> 
(More)</a><br/> 
sku: $entity2.prodId<br/> 
Price: $$entity2.value 
<br/><br/> 
</div> 
</td> 
<td style="padding-left:10px;"> 
<div class="search_content_inner" style="border-bottom:0px;"> 
<div class="search_title"><a href="$entity3.pageUrl"  
style="color: rgb(112, 161, 0); font-weight: bold;"> 
$entity3.id</a></div> 
By $entity3.message <a href="?x14=brand;q14=$entity3.message"> 
(More)</a><br/> 
sku: $entity3.prodId<br/> Price: $$entity3.value 
<br/><br/> 
</div> 
</td> 
</tr>  
</table>
```

>[!NOTE]
>
>Als u tekst wilt toevoegen na de waarde van een kenmerk vóór een tag die aangeeft dat de naam van het kenmerk is voltooid, kunt u dit doen met een formele notatie om de naam van het kenmerk in te sluiten. Bijvoorbeeld: `${entity1.thumbnailUrl}.gif` .

U kunt `algorithm.name` en `algorithm.dayCount` ook gebruiken als entiteitskenmerken in ontwerpen, zodat één ontwerp kan worden gebruikt om meerdere criteria te testen, en de naam van de criteria kan dynamisch in het ontwerp worden getoond. Dit toont de bezoeker die hij of zij kijkt naar &quot;topverkopers&quot; of &quot;mensen die dit bekeken hebben die dat gekocht hebben.&quot; U kunt deze kenmerken zelfs gebruiken om de `dayCount` weer te geven (aantal dagen dat gegevens in de criteria zijn gebruikt, zoals &#39;hoogste verkopers in de afgelopen 2 dagen&#39;, enzovoort.

## Werken met getallen in [!DNL Velocity] sjablonen

Standaard behandelen [!DNL Velocity] -sjablonen alle entiteitkenmerken als tekenreekswaarden. Mogelijk wilt u een entiteitskenmerk behandelen als een numerieke waarde om een wiskundige bewerking uit te voeren of deze te vergelijken met een andere numerieke waarde. Voer de volgende stappen uit om een entiteitskenmerk als een numerieke waarde te behandelen:

1. Declareer een dummyvariabele en initialiseer deze naar een willekeurig geheel getal of een dubbele waarde.
1. Zorg ervoor dat het entiteitskenmerk dat u wilt gebruiken, niet leeg is (vereist voor [!DNL Target Recommendations] &#39;-sjabloonparser om de sjabloon te valideren en op te slaan).
1. Geef het entiteitskenmerk door in de methode `parseInt` of `parseDouble` van de dummyvariabele die u in stap 1 hebt gemaakt om de tekenreeks om te zetten in een geheel getal of dubbele waarde.
1. Voer de wiskundige bewerking of vergelijking uit op de nieuwe numerieke waarde.

### Voorbeeld: Een kortingsprijs berekenen

Stel dat je de weergegeven prijs van een object met $0,99 wilt verlagen om een korting toe te passen. U kunt de volgende methode gebruiken om dit resultaat te bereiken:

```
#set( $double = 0.1 )

#if( $entity1.get('priceBeforeDiscount') != '' )
    #set( $discountedPrice = $double.parseDouble($entity1.get('priceBeforeDiscount')) - 0.99 )
    Item price: $$discountedPrice
#else
    Item price unavailable
#end
```

### Voorbeeld: Het aantal sterren kiezen dat moet worden weergegeven op basis van de waardering van een item

Stel dat u een geschikt aantal sterren wilt weergeven op basis van de numerieke gemiddelde klantbeoordeling van een item. U kunt de volgende methode gebruiken om dit resultaat te bereiken:

```
#set( $double = 0.1 )

#if( $entity1.get('rating') != '' )
    #set( $rating = $double.parseDouble($entity1.get('rating')) )
    #if( $rating >= 4.5 )
        <img src="5_stars.jpg">
    #elseif( $rating >= 3.5 )
        <img src="4_stars.jpg">
    #elseif( $rating >= 2.5 )
        <img src="3_stars.jpg">
    #elseif( $rating >= 1.5 )
        <img src="2_stars.jpg">
    #else
        <img src="1_star.jpg">
    #end
#else
    <img src="no_rating_default.jpg">
#end
```

### Voorbeeld: de tijd in uren en minuten berekenen op basis van de lengte van een item in minuten

Stel dat u de lengte van een film in minuten opslaat, maar de lengte in uren en minuten wilt weergeven. U kunt de volgende methode gebruiken om dit resultaat te bereiken:

```
#if( $entity1.get('length_minutes') )
#set( $Integer = 1 )
#set( $nbr = $Integer.parseInt($entity1.get('length_minutes')) )
#set( $hrs = $nbr / 60)
#set( $mins = $nbr % 60)
#end
```

## Een sleutelitem weergeven met aanbevolen producten {#section_7F8D8C0CCCB0403FB9904B32D9E5EDDE}

U kunt uw ontwerp aanpassen om uw belangrijkste punt naast andere geadviseerde producten te tonen. U kunt bijvoorbeeld het huidige item ter referentie naast de aanbevelingen weergeven.

Hiertoe maakt u in uw ontwerp een kolom waarin het kenmerk `$key` wordt gebruikt waarop u uw aanbeveling baseert in plaats van het kenmerk `$entity` . De code voor uw sleutelkolom kan er bijvoorbeeld als volgt uitzien:

```
<div class="at-table-column"> 
   <a href="$key.pageURL"> 
      <img src=$key.thumbnailUrl" class="at-thumbnail"/> 
      <br/><h3>$key.name</h3> 
      <br/><p class="at-light">$key.message</p> 
      <br/><p class="at-light">$key.value</p> 
   </a> 
</div>
```

Het resultaat is een ontwerp als het volgende, waarbij in één kolom het sleutelitem wordt weergegeven.

![&#x200B; rec_key beeld &#x200B;](assets/rec_key.png)

Wanneer u uw [!DNL Recommendations] activiteit creeert, als het belangrijkste punt uit het profiel van de bezoeker, zoals &quot;laatst gekocht voorwerp wordt genomen,&quot;[!DNL Target] toont een willekeurig product in [!UICONTROL Visual Experience Composer] (VEC). Dit komt omdat er geen profiel beschikbaar is terwijl u de activiteit ontwerpt. Wanneer bezoekers de pagina bekijken, zullen zij het verwachte belangrijkste punt zien.

## Vervangingen in een tekenreekswaarde uitvoeren {#section_01F8C993C79F42978ED00E39956FA8CA}

U kunt uw ontwerp wijzigen om waarden binnen een tekenreeks te vervangen. Zo vervangt u het decimaalteken dat in de Verenigde Staten wordt gebruikt door het komma-scheidingsteken dat in Europa en andere landen wordt gebruikt.

De volgende code toont één regel in een voorbeeld van een voorwaardelijke verkoopprijs:

```
<span class="price">$entity1.value.replace(".", ",") &euro;</span><br>
```

De volgende code is een volledig voorwaardelijk voorbeeld van een verkoopprijs:

```
<div class="price"> 
    #if($entity1.hasSalesprice==true) 
    <span class="old">Statt <s>$entity1.salesprice.replace(".", ",") &euro;</s></span><br> 
    <span style="font-size: 10px; float: left;">jetzt nur</span> $entity1.value.replace(".", ",") &euro;<br> #else 
    <span class="price">$entity1.value.replace(".", ",") &euro;</span><br> #end 
    <span style="font-weight:normal; font-size:10px;"> 
                                        $entity1.vatclassDisplay 
                                        <br/> 
                                        $entity1.delivery 
                                        <br> 
                                    </span>
```

## De sjabloongrootte aanpassen en blanco waarden controleren {#default}

Met behulp van een [!DNL Velocity] -script voor het dynamisch instellen van de grootte van de entiteitsweergave, past de volgende sjabloon een 1-op-veel-resultaat toe om te voorkomen dat lege HTML-elementen worden gemaakt wanneer er onvoldoende overeenkomende entiteiten worden geretourneerd van [!DNL Recommendations] . Dit script is het meest geschikt voor scenario&#39;s waarin back-upaanbevelingen geen nut hebben en [!UICONTROL Partial Template Rendering] is ingeschakeld.

Het volgende HTML-fragment vervangt het bestaande HTML-gedeelte in het standaardontwerp van 4 x 2 (de CSS is hier niet opgenomen omwille van de beknoptheid):

* Als er een vijfde entiteit bestaat, voegt het script een afsluitende div in en wordt een nieuwe rij geopend met `<div class="at-table-row">` .
* Met 4x2 zijn de maximale resultaten acht, maar deze kunnen voor kleinere of grotere lijsten worden aangepast door `$count <=8` aan te passen.
* Houd er rekening mee dat de logica de entiteiten op meerdere rijen niet in evenwicht brengt. Bijvoorbeeld, als er vijf of zes te tonen entiteiten zijn, zal het dynamisch niet drie op bovenkant en twee op de bodem (of drie op bovenkant en drie op de bodem) worden. In de bovenste rij worden vier items weergegeven voordat een tweede rij wordt gestart.

```
<div class="at-table">
  <div class="at-table-row">
    #set($count=1) 
    #foreach($e in $entities)  
        #if($e.id != "" && $count < $entities.size() && $count <=8) 
            #if($count==5) 
                </div>
                <div class="at-table-row">
            #end
            <div class="at-table-column">
                <a href="$e.pageUrl"><img src="$e.thumbnailUrl" class="at-thumbnail" />
                    <br/>
                    <h3>$e.name</h3>
                    <br/>
                    <p class="at-light">$e.message</p>
                    <br/>
                    <p class="at-light">$$e.value</p>
                </a>
            </div>
            #set($count = $count + 1) 
        #end 
    #end
  </div>
</div>
```
