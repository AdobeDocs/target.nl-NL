---
keywords: Gericht op ervaring;Bezig met landen van pagina testen
description: 'Een elementkiezer is een CSS-expressie waarmee een of meer elementen kunnen worden geïdentificeerd. Leer hoe u elementkiezers in de Adobe kunt gebruiken [!DNL Target] Visual Experience Composer (VEC). '
title: Kan ik de Kiezers van het Element in Visual Experience Composer (VEC) gebruiken?
feature: Visual Experience Composer (VEC)
exl-id: f4ddb30a-f599-4fe5-861c-2deeeb9a70dd
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '422'
ht-degree: 0%

---

# Elementkiezers die worden gebruikt in de composer voor visuele ervaring

Een elementkiezer is een CSS-expressie waarmee een of meer elementen kunnen worden geïdentificeerd.

U vindt basisinformatie over CSS-kiezers in het dialoogvenster [Kiezers](https://developer.mozilla.org/en-US/docs/Web/Guide/CSS/Getting_started/Selectors) document over het Mozilla Developer Network (MDN).

U kunt instellen of u in uw accountvoorkeuren een elementklasse- of element-id wilt gebruiken. Klikken **[!UICONTROL Administration > Visual Experience Composer]** en kiest u de gewenste CSS-kiezers.

![](assets/css_selectors.png)

>[!NOTE]
>
>De Klassen van het element zijn beschikbaar als selecteurs in de Test A/B, Automated Personalization, en Multivariate van de Test activiteiten.

Voor informatie over wanneer CSS-kiezers moeten worden gebruikt en wanneer unieke id&#39;s moeten worden gebruikt, raadpleegt u [Aanbevolen werkwijzen en beperkingen voor composer visuele ervaring](/help/main/c-experiences/c-visual-experience-composer/experience-composer-best-practices.md#concept_E284B3F704C04406B174D9050A2528A6).

## Hoe Adobe [!DNL Target] Genereert een kiezer voor een element {#section_D89D954BCBFB486CA081BE183776A475}

Doel gebruikt een eenvoudig algoritme om een kiezer te maken. Hier volgt een korte uitleg van de generatielogica:

1. Als een element bijvoorbeeld een id heeft `id="container"`De kiezer voor het element is `#container`.

   Bijvoorbeeld:

   ```html
   <div class="wrapper">
     <div id="container"> <!-- Selector is computed for this element -->
       <ul class="navigation">
         <li class="item active"> Home </li>
         <li class="item"> Men </li>
         <li class="item"> Women </li>
         <li class="item"> Kids </li>
       </ul>
     </div>
   </div>
   ```

1. Als een element een klassenkenmerk bevat, probeert Target de eerste klasse van alle klassen die zich op het element bevinden, te benutten.

   Het doel probeert het bovenliggende element te parseren totdat het het `<HTML>` -element of een element met een id. Wanneer een element een id bevat en de kiezer op het onderliggende element wordt berekend, levert de id van dit element een bijdrage aan de kiezer.

   Bijvoorbeeld:

   ```html
   <div class="wrapper">
     <div id="container"> <!-- id is present here. It contributes to selector -->
       <ul class="navigation">
         <li class="item active"> Home </li> <!-- Selector is computed for this element -->
         <li class="item"> Men </li>
         <li class="item"> Women </li>
         <li class="item"> Kids </li>
       </ul>
     </div>
   </div>
   ```

   In dit voorbeeld:

   Kiezer: `#container` > `ul.navigation:eq(0)` > `li.item:eq(0)` (&quot; > &quot; geeft het directe onderliggende item aan.)

   `eq` vertelt de index er een element is dat &quot;tagName=UL&quot;heeft en de eerste klasse is `navigation`. Daarom `index` is 0. Zie de [Kiezers](https://developer.mozilla.org/en-US/docs/Web/Guide/CSS/Getting_started/Selectors) artikel in MDN voor meer informatie.

1. Als een element geen klasse bevat, gebruikt Target `tagName` voor het element en doorloopt het bovenliggende element totdat een van de `<HTML>` -element of een element met een id is gevonden.

   Bijvoorbeeld:

   ```html
   <div class="wrapper">
     <div id="container"> <!-- id is present here. It contributes to selector -->
       <ul class="navigation">
         <li> Home </li>
         <li> Men </li>
         <li class="active"> Women </li>
         <li> Kids </li><!-- Selector is computed for this element -->
       </ul>
     </div>
   </div>
   ```

   Kiezer: `#container` > `ul.navigation(0)` > `li:nth-of-type(4)`

   Meer informatie over [nth-of-type op de webpagina CSS-trucs](https://css-tricks.com/almanac/selectors/n/nth-of-type/).

In het bovenstaande proces:

* U kunt elke CSS-kiezer gebruiken zolang deze een element in het DOM op unieke wijze identificeert.
* De bovenstaande benadering wordt door Target gebruikt. Het doel verplicht u niet om deze benadering te gebruiken. U kunt elke kiezer toevoegen zolang punt #1 waar is.
* U kunt elk willekeurig kenmerk in de kiezer gebruiken. Dit document gebruikt alleen een klassenaam als voorbeeld.
