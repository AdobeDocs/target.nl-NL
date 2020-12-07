---
keywords: Recommendations
description: De scenario's in dit onderwerp tonen hoe de veranderingen die aan uw pagina worden aangebracht de capaciteit van het Doel beïnvloeden om een ervaring te tonen.
title: Paginawijzigingsscenario's
feature: vec
translation-type: tm+mt
source-git-commit: 6704ac2ec73361ad95e110e9182485537d0de642
workflow-type: tm+mt
source-wordcount: '520'
ht-degree: 0%

---


# Paginawijzigingsscenario&#39;s {#page-modification-scenarios}

De scenario&#39;s in dit onderwerp tonen hoe de veranderingen die aan uw pagina worden aangebracht de capaciteit van het Doel beïnvloeden om een ervaring te tonen.

De doelkiezer bepaalt waar een ervaring moet worden weergegeven. Als een pagina buiten Doel wordt gewijzigd, kunnen de veranderingen de capaciteit van Doel beïnvloeden om de ervaring te tonen.

Wanneer u de kiezer gebruikt, komt de unieke klasse niet overeen met de id. De kiezer werkt altijd met een unieke klasse. Als er geen klasse aan het element is toegewezen, berekent de kiezer het aantal vorige zusterobjecten met dezelfde tagnaam.

>[!NOTE]
>
>Hoewel deze scenario&#39;s lijstpunten als voorbeelden gebruiken, zijn de concepten op om het even welk element van toepassing.

## Scenario: Een element invoegen met een andere klassenaam voor het geselecteerde element {#section_298F661F72384F6AB957D5885A99D822}

In dit voorbeeld wordt een nieuw element ingevoegd als een element op hetzelfde niveau als het element in de doelkiezer.

Het is mogelijk dat de eerste klasse die aanwezig is op het element, wordt toegevoegd door JavaScript. In dat geval mislukt de levering en wordt de actie niet toegepast.

**Ingevoegd element:**

```html
<li class="kids-section">Kids</li>
```

**Geselecteerd:**

`<li class="women-section">Women</li>`

Kiezer: `#wrap > ul.nav:eq(0) > li.women-section:eq(0)`

**Resultaat:**

De kiezer werkt zoals u had verwacht, omdat dit geen invloed `li.women-section:eq(0)` heeft.

Voor:

```html
<div id="wrap">
     <ul class="nav">
        <li class="men-section"> Men</li> <li class="women-section">Women</li>
     </ul> 
</div>
```

Na:

```html
<div id="wrap">
    <ul class="nav">
        <li class="kids-section">Kids</li>
        <li class="men-section"> Men</li>       <li class="women-section">Women</li>
    </ul> 
</div>
```

## Scenario: Een element invoegen met dezelfde klassenaam als het geselecteerde element {#section_0969B88C2F154E648D9969C8C85EF55A}

In dit scenario wordt geprobeerd een lijst in te voegen wanneer een item in een lijst is geselecteerd.

**Ingevoegd element:**

```html
<ul class="nav"> 
   <li class="item"> Sale </li> 
   <li> class="item"> Offers </li> 
</ul>
```

**Geselecteerd**

`<li class="women-section">Women</li>`

Kiezer: `#wrap > ul.nav:eq(0) > li.women-section:eq(0)`

**Resultaat:**

De kiezer werkt niet, omdat er een dynamisch toegevoegd element `ul.nav:eq(0)` is. Het element is niet beschikbaar en de handeling wordt niet toegepast. Wanneer een vergelijkbaar lijstitem met dezelfde klasse dynamisch of handmatig wordt toegevoegd nadat een activiteit is gemaakt, wordt een nieuw element op de eerste positie gemaakt. Hierdoor wordt de kiezer verbroken.

Voor:

```html
<div id="wrap">
    <ul class="nav">
        <li class="men-section"> Men</li>       <li class="women-section">Women</li>
    </ul> 
</div>
```

Na (geprobeerd):

```html
<div id="wrap">
     <ul class="nav">
        <li class="item"> Sale</li>
        <li> class="item"> Offers</li>
     </ul>
     <ul class="nav">
       <li class="men-section"> Men</li>
       <li class="women-section">Women</li>
    </ul>
</div>
```

## Scenario: Een element invoegen na het geselecteerde element {#section_15B07B84BEE94ED39D85BBBE0733E170}

In dit scenario wordt een lijstitem ingevoegd na het geselecteerde element.

**Ingevoegd element:**

```html
<ul class="nav"> 
   <li class="men-section"> Men Clothes</li> 
   <li class="women-section"> Women Clothes</li> 
</ul>
```

**Geselecteerd:**

`<li class="women-section">Women Shoes</li>`

Kiezer: `#wrap > ul.nav:eq(0) > li.women-section:eq(0)`

**Resultaat:**

In dit geval werkt het invoegen van een lijst na de lijst die eindigt met het geselecteerde lijstitem zoals u had verwacht. Het nieuwe element wordt toegevoegd op dezelfde positie als het geselecteerde element ten opzichte van het bovenliggende element.

Voor:

```html
<div id="wrap">
    <ul class="nav">
        <li class="men">Men Shoes </li>       <li class="women">Women Shoes</li>
    </ul>
</div>
```

Na:

```html
<div id="wrap">
    <ul class="nav">
        <li class="men">Men Shoes </li>
        <li class="women">Women Shoes</li>
    </ul>
      <ul class="nav">
        <li class="men-section">Men Clothes</li>
        <li class="women-section"> Women Clothes</li>
    </ul>
</div>
```

## Scenario: Het element verwijderen dat direct voorafgaat aan een ander element {#section_F193674F04F84AA593EAA1137C880EBA}

In dit scenario wordt het lijstitem verwijderd voordat het geselecteerde element wordt verwijderd.

**Verwijderd element:**

```html
<li class="men-section"> Men </li>
```

**Geselecteerd:**

`<li class="women-section">Women</li>`

Kiezer: `#wrap > ul.nav:eq(0) > li.women-section:eq(0)`

**Resultaat:**

Het element is verwijderd omdat de klasse van het geselecteerde item niet is gewijzigd.

Voor:

```html
<div id="wrap">
    <ul class="nav">
        <li class="men-section">Men</li>
        <li class="women-section">Women</li>
    </ul>
</div>
```

Na:

```html
<div id="wrap">
    <ul class="nav">
        <li class="women-section">Women</li>
    </ul>
</div>
```

## Scenario: Het element direct na een ander element verwijderen {#section_F83B51BE54924FB58679D512DAF1EBB2}

In dit scenario wordt het lijstitem nadat het geselecteerde element is verwijderd.

**Verwijderd element:**

```html
<li class="kids-section">Kids</li>
```

**Geselecteerd:**

`<li class="women-section">Women</li>`

Kiezer: `#wrap > ul.nav:eq(0) > li.women-section:eq(0)`

**Resultaat:**

Het element is verwijderd omdat de klasse van het geselecteerde item niet is gewijzigd. Het verwijderde element bevat een unieke klasse binnen de bovenliggende substructuur.

Voor:

```html
<div id="wrap">
    <ul class="nav">
        <li class="men-section">Men</li>
        <li class="women-section">Women</li>
        <li class="kids-section">Women</li>
    </ul>
</div>
```

Na:

```html
<div id="wrap">
    <ul class="nav">
        <li class="men-section">Men</li>
        <li class="women-section">Women</li>
    </ul>
</div>
```

## Scenario: Het geselecteerde element verwijderen {#section_1989CF1E2C344CC5963084ED83C18F9C}

In dit scenario wordt het geselecteerde lijstitem verwijderd.

**Verwijderd element:**

```html
<li class="women-shoes">Women</li>
```

**Geselecteerd:**

`<li class="women-shoes">Women</li>`

Kiezer: `#wrap > ul.nav:eq(0) > li.women-section:eq(0)`

**Resultaat:**

Het element is verwijderd.

Voor:

```html
<div id="wrap">
    <ul class="nav">
        <li class="men-section">Men</li>
        <li class="women-shoes">Women</li>
    </ul>
</div>
```

Na

```html
<div id="wrap">
    <ul class="nav">
       <li class="men-section">Men</li>
    </ul>
</div>
```

## Scenario: De naam van de klasse van het geselecteerde element wijzigen {#section_79D244C588BA452DB8E433D82B7F63EA}

In dit scenario wordt de klasse van het geselecteerde lijstitem gewijzigd.

**Gewijzigd element:**

```html
<li class="women-section">Women</li>
```

**Geselecteerd:**

`<li class="women-section">Women</li>`

Kiezer: `#wrap > ul.nav:eq(0) > li.women-section:eq(0)`

**Resultaat:**

De naam van de elementklasse kan niet worden gewijzigd omdat `class` deze niet is gevonden.

Voor:

```html
<div id="wrap">
    <ul class="nav">
        <li class="men-section">Men</li>
        <li class="women-section">Women</li>
    </ul>
</div>
```

Na (geprobeerd):

```html
<div id="wrap">
    <ul class="nav">
        <li class="men-section">Men</li>
        <li class="women-shoes">Women</li>
    </ul>
</div>
```
