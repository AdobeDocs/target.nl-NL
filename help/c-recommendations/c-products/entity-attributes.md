---
keywords: entity;entity attributes;pass information to Recommendations;behavioral data;data counter;define relative URL;display inventory level;define price;define profit margin;custom attributes
description: Gebruik entiteitskenmerken om product- of inhoudsgegevens door te geven aan Adobe Target Recommendations.
title: Entiteitskenmerken
feature: entities
translation-type: tm+mt
source-git-commit: 6704ac2ec73361ad95e110e9182485537d0de642
workflow-type: tm+mt
source-wordcount: '1016'
ht-degree: 0%

---


# ![Kenmerken ](/help/assets/premium.png) PREMIUMEntity{#entity-attributes}

Gebruik entiteitskenmerken om product- of inhoudsinformatie door te geven aan [!DNL Adobe Target Recommendations].

[!DNL Recommendations] verzendt de  `productId` of  `productPurchasedId` (waarnaar wordt verwezen  `entity.id` in de code) die wordt gebruikt in de algoritmen.

>[!NOTE]
>
>* `entity.id` moet overeenkomen met de pagina die naar de pagina voor bevestiging van de bestelling is  `productPurchasedId` verzonden en met de pagina&#39;s die in Adobe Analytics-productrapporten zijn  `productId` gebruikt.
   >
   >
* Waarden van opgegeven entiteitskenmerken verlopen na 61 dagen. Dit betekent dat u ervoor moet zorgen dat de recentste waarde van elk entiteitattribuut aan Doel Recommendations minstens eens per maand voor elk punt in uw catalogus wordt overgegaan.


De meeste vooraf gedefinieerde parameters accepteren slechts één waarde, waarbij nieuwe waarden oude waarden overschrijven. De parameter `categoryId` kan een komma-afgebakende lijst van waarden voor elke categorie goedkeuren die dat product bevat. Nieuwe `categoryId`-waarden overschrijven bestaande waarden niet, maar worden toegevoegd tijdens het bijwerken van de entiteit (limiet van 250 tekens).

Over het algemeen ziet het informatievenster voor de weergave er als in het volgende voorbeeld uit als u at.js 1 gebruikt.** xwith  `mboxCreate`.

>[!NOTE]
>
>* Als u at.js 2 gebruikt.*x*,  `mboxCreate` (zoals in het volgende voorbeeld wordt gebruikt) wordt niet meer ondersteund. Product- of inhoudsgegevens doorgeven aan Recommendations met behulp van at.js 2.*x*, gebruik  [targetPageParams](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetpageparams.md). Voor een voorbeeld van dit, zie [Plan en voer Recommendations](/help/c-recommendations/plan-implement.md) uit.

>



Alle kenmerken van de entiteitsparameter zijn hoofdlettergevoelig.

```javascript
<div class="mboxDefault"></div><script language="JavaScript1.2"> 
 
mboxCreate('productPage', 
 
'entity.id=67833', 
 
'entity.name=GIANTS VS ROCKIES 5/12', 
 
'entity.categoryId=BASEBALL, GIANTS, SF BAY AREA', 
 
'entity.pageUrl=/help/baseball/giants-tix/giantsvrockies5.12.2000-67833', 
 
'entity.venue=AT&T PARK', 
 
'entity.secondary=ROCKIES', 
 
'entity.thumbnailUrl=/help/baseball/giants-tix/giants-136px.gif', 
 
'entity.message=FAMILY SPECIAL', 
 
'entity.value=15.99', 
 
'entity.inventory=1' 
 
); 
 
</script>
```

>[!NOTE]
>
>Relatieve URL&#39;s hebben de voorkeur voor `pageUrl` en `thumbnailUrl` in plaats van absolute URL&#39;s, omdat aanbevelingen gegevens ontvangen die worden verzonden vanuit alle omgevingen op uw site. Als u relatieve URL&#39;s gebruikt, worden hardcodeerde koppelingen naar een testserver of ontwikkelingsserver vermeden.

Als het selectievakje op een productpagina staat, kunt u zowel de product-id als de categorie-id opnemen. Het geselecteerde algoritme bepaalt welke weergaven worden weergegeven. De product-id wordt gebruikt voor affiniteitsalgoritmen en de categorie-id wordt gebruikt voor categoriealgoritmen.

## Beschikbare variabelen

In de volgende lijst worden de beschikbare variabelen beschreven.

### entity.id

Alleen randwaarde.

Deze vereiste parameter identificeert het product. Deze alfanumerieke id moet hetzelfde zijn voor alle [!DNL Adobe Experience Cloud]-producten die worden gebruikt, inclusief [!DNL Analytics], zodat de verschillende producten het item kunnen herkennen en gegevens erover kunnen delen.

`entity.id` waarden mogen geen slashes, ampersands, vraagtekens, percentagesymbolen, komma&#39;s of andere leestekens bevatten die URL-codering vereisen wanneer deze worden doorgegeven in een REST API-aanroep. Afbreekstreepjes en onderstrepingstekens zijn toegestaan. Het opnemen van ongeldige interpunctie in een `entity.id` waarde veroorzaakt sommige [!DNL Recommendations] functionaliteit om te ontbreken.

Voorbeeld: `'entity.id=67833'`

### entity.name

Alleen één waarde.

De productnaam die op de Website wordt getoond wanneer het product wordt geadviseerd.

Voorbeeld: `'entity.name=Giants& vs& Rockies& 5/12'`

### entity.categoryId

Ondersteunt meerdere waarden (door komma&#39;s gescheiden lijst).

Categorie van de huidige pagina. Dit kan meerdere categorieën omvatten, zoals een subsectie over cardigans (d.w.z. vrouwen, vrouwen:zweet, vrouwen:zweet:verzorgers). Meerdere categorieën moeten worden gescheiden door komma&#39;s.

`categoryId` is beperkt tot 250 tekens.

>[!NOTE]
>
>Om een aanbeveling te tonen die op een categorie in een [!UICONTROL Category] pagina wordt gebaseerd, slechts kan één `categoryId` in mbox worden overgegaan die wordt gebruikt om die bepaalde aanbeveling te tonen. De waarde van `categoryId` moet exact overeenkomen met de waarde van `entity.categoryId` die op de pagina [!UICONTROL Product Detail] is doorgegeven.

Voorbeelden:

* Voorbeeld van productdetailpagina: vrouwen, vrouwen:truien, vrouwen:sweaters:cardigans
* Voorbeeld van categorie Paginanummers: vrouwen:truien
* Voorbeeld van paginakaartjes voor categorieën: vrouwen:sweaters:cardigans

Voor op categorieën gebaseerde aanbevelingen wordt een komma gebruikt om de categoriewaarde te scheiden. Waarden die door komma&#39;s worden gescheiden, worden categorieën. U kunt ook subcategorieën definiëren door een ander scheidingsteken, zoals een dubbele punt (:), te gebruiken om subcategorieën binnen de categoriewaarde te scheiden.

In de volgende code is de categorie Vrouwen bijvoorbeeld onderverdeeld in verschillende subcategorieën:

```javascript
mboxCreate('mboxName', 'entity.id=343942-32', 'entity.categoryId= Womens, Womens:Outerwear, Womens:Outerwear:Jackets, Womens:Outerwear:Jackets:Parka, Womens:Outerwear:Jackets:Caban’, 'entity.thumbnailUrl=...', 'entity.message=...', );
```

Voor de levering mbox, wordt de langste kenmerknaam gebruikt voor de sleutel. Als er een tijd is, wordt het laatste kenmerk gebruikt. In het bovenstaande voorbeeld is de categorietoets Womens:Buitendgoedkleding:Jackets:Caban.

### entity.brand

Alleen één waarde.

Hiermee geeft u de merknaam van een item weer.

Voorbeeld: `'entity.brand=brandxyz'`

### entity.pageUrl

Alleen één waarde.

Definieert de relatieve URL van de pagina waarop het item kan worden aangeschaft.

Voorbeeld: `'entity.pageUrl=baseball/giants-tix/giantsvrockies5.12.2000-67833'`

### entity.thumbnailUrl

Alleen één waarde.

Definieert de relatieve URL ten opzichte van de miniatuurafbeelding die bij het item wordt weergegeven.

Voorbeeld: `'entity.thumbnailUrl=baseball/giants-tix/giants-136px.gif'`

### entity.message

Alleen één waarde.

Een bericht over het product dat in de aanbeveling wordt getoond, zoals &quot;bij verkoop&quot; of &quot;klaring&quot;. Het bericht is doorgaans uitgebreider dan de productnaam. Gebruik deze optie om aanvullende informatie te definiëren die met het product in de sjabloon moet worden weergegeven.

Voorbeeld: `'entity.message=Family&nbsp;special'`

### entity.inventory

Alleen één waarde. Vereist een geheel getal of een lange waarde.

Hiermee geeft u het voorraadniveau van het item weer.

Voorbeeld: `'entity.inventory=1'`

**Lege verwerking van inventariskenmerken:** Voor levering geldt dat als u een regel, verzamelingsregel of criteria hebt die zijn ingesteld op  `entity.inventory` > 0 of  `entity.inventory` = 0 en het product een voorraad heeft die niet is ingesteld, dit  [!DNL Target] wordt geëvalueerd op TRUE en dat er ook producten in worden opgenomen waarvoor de voorraad niet is ingesteld. Dit is standaard gedaan, zodat producten met een voorraad die niet is ingesteld, in de resultaten van de aanbeveling worden weergegeven.

En als u een globale uitsluitingsregel hebt met `entity.inventory` = 0 en `entity.inventory` niet is ingesteld, evalueert [!DNL Target] deze regel als WAAR en sluit het product uit.

**Bekend probleem:** Productzoekopdracht is inconsistent met levering voor niet-ingestelde voorraadwaardekenmerken. Voor een regel met `entity.inventory` = 0 geeft productzoekopdracht bijvoorbeeld geen producten weer waarvoor de inventariswaarde niet is ingesteld.

### entity.value

Alleen één waarde.

Hiermee definieert u de prijs of waarde van het item.

Voorbeeld: `'entity.value=15.99'`

### entity.margin

Alleen één waarde.

De winstmarge of andere waarde van de post.

Voorbeeld: `'entity.margin=1.00'`

### entiteit.*aangepast*

Ondersteunt multivalue (JSON-array).

Definieer maximaal 100 aangepaste variabelen die aanvullende informatie over het item bevatten. U kunt elke ongebruikte kenmerknaam opgeven voor elk aangepast kenmerk. U kunt bijvoorbeeld een aangepast kenmerk met de naam `entity.genre` maken om een boek of film te definiëren. Of een verkoper van vervoerbewijzen kan kenmerken maken voor een plaats van een evenement voor een tweede uitvoerder, zoals een bezoekend team in een sportevenement of een openingsactie in een concert.

Beperkingen:

* U kunt vooraf gedefinieerde namen van entiteitskenmerken niet gebruiken voor aangepaste entiteitskenmerken.
* Het attribuut entity.environment wordt gereserveerd door het systeem en kan niet voor de attributen van de douaneentiteit worden gebruikt. Pogingen om entiteit.environment door te geven met targetPageParams, feed of API worden genegeerd.

Voorbeelden:

`'entity.venue=AT&T&nbsp;Park'`

`'entity.secondary=Rockies'`

Aangepaste entiteitskenmerken ondersteunen meerdere waarden. Zie [Aangepaste entiteitskenmerken](/help/c-recommendations/c-products/custom-entity-attributes.md#limits) voor teken- en waardelimieten.

Voorbeeld: `'entity.secondary=["band1",&nbsp;"band2"]'`

>[!NOTE]
>
>Aangepaste entiteitskenmerken van meerdere waarden vereisen geldige JSON-arrays. Zie Aangepaste entiteitskenmerken voor correcte syntaxisinformatie.

### entity.event.detailsOnly

Alleen één waarde.

Gebruikt om een mbox vraag te verhinderen gedragstellers van gegevens voor een algoritme te verhogen.

Voorbeeld: `'entity.event.detailsOnly=true'`

In de onderstaande voorbeelden worden de catalogus en gedragsgegevens bijgewerkt met de eerste aanroep van het mbox. De tweede mbox-aanroep werkt alleen de catalogus bij.

```javascript
mboxCreate('myMbox', 'profile.geo.city = new york', 'profile.geo.state = new york',  'entity.id = 'entity.inventory = 4' )
mboxCreate('myMbox',  'profile.geo.city = new york', 'profile.geo.state = new york',  'entity.id = 123', 'entity.inventory = 4' 'entity.event.detailsOnly=true' )
```

## Verwante onderwerpen:

* [Kenmerken Aangepaste entiteit](/help/c-recommendations/c-products/custom-entity-attributes.md#concept_E5CF39BCAC8140309A73828706288322)
