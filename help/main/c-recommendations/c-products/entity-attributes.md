---
keywords: entiteit;entiteitskenmerken;informatie doorgeven aan Recommendations;gedraggegevens;gegevensteller;relatieve URL definiëren;inventarisniveau weergeven;prijs definiëren;winstmarge definiëren;aangepaste kenmerken
description: Leer hoe u entiteitskenmerken kunt gebruiken om product- of inhoudsgegevens door te geven aan [!DNL Target] Recommendations.
title: Hoe gebruik ik entiteitskenmerken?
feature: Recommendations
exl-id: 4ed5fad3-b8b6-4675-a741-9f85cf73fcf1
source-git-commit: b1e8ea2370fc15f4bfcd960ab2960cafe2db92b8
workflow-type: tm+mt
source-wordcount: '1084'
ht-degree: 0%

---

# ![PREMIUM](/help/main/assets/premium.png) Entiteitskenmerken

Entiteitskenmerken gebruiken om product- of inhoudsinformatie door te geven aan [!DNL Adobe Target Recommendations].

Entiteiten verwijzen naar de items die u wilt aanbevelen. De entiteiten kunnen producten, inhoud (artikelen, diashows, beelden, films, en televisieprogramma&#39;s), baanaanbiedingen, restaurants, etc. omvatten.

[!DNL Recommendations] verzendt de `productId` of `productPurchasedId` (wordt `entity.id` in de code) die wordt gebruikt in de algoritmen.

Overweeg het volgende:

* `entity.id` moet overeenkomen met `productPurchasedId` die naar de pagina van de orderbevestiging en de `productId` gebruikt in [!DNL Adobe Analytics] productrapporten.
* Kenmerkwaarden voor entiteiten die u doorgeeft [!DNL Recommendations] verlopen na 61 dagen. Adobe raadt aan dat u de laatste waarde van elk entiteitskenmerk doorgeeft aan [!DNL Recommendations] ten minste één keer per maand voor elk item in de catalogus.

De meeste vooraf gedefinieerde parameters accepteren slechts één waarde, waarbij nieuwe waarden oude waarden overschrijven. De `categoryId` kan een door komma&#39;s gescheiden lijst met waarden accepteren voor elke categorie die dat product bevat. Nieuw `categoryId` Waarden overschrijven bestaande waarden niet, maar worden toegevoegd tijdens het bijwerken van de entiteit (limiet van 250 tekens).

In het algemeen ziet het informatievenster voor de weergave er als in het volgende voorbeeld uit als u at.js 1 gebruikt.*x* with `mboxCreate`. Alle attributen van de entiteitparameter zijn case-sensitive.

>[!NOTE]
>
>Als u at.js 2 gebruikt.*x*, `mboxCreate` (zoals in het volgende voorbeeld wordt gebruikt) wordt niet meer ondersteund. Product- of inhoudsgegevens doorgeven aan [!DNL Recommendations] met behulp van at.js 2.*x*, gebruik [targetPageParams](https://developer.adobe.com/target/implement/client-side/atjs/atjs-functions/targetpageparams/). Zie voor een voorbeeld [Recommendations plannen en implementeren](https://developer.adobe.com/target/implement/recommendations/).

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
>Relatieve URL&#39;s hebben de voorkeur voor `pageUrl` en `thumbnailUrl` in plaats van absolute URL&#39;s, omdat aanbevelingen gegevens ontvangen die worden verzonden vanuit alle omgevingen op uw site. Als u relatieve URL&#39;s gebruikt, vermijdt u hardcodeerde koppelingen naar een testserver of ontwikkelingsserver.

Als het selectievakje op een productpagina staat, kunt u zowel de product-id als de categorie-id opnemen. Het geselecteerde algoritme bepaalt welke weergaven worden weergegeven. De product-id wordt gebruikt voor affiniteitsalgoritmen en de categorie-id wordt gebruikt voor categoriealgoritmen.

## Beschikbare variabelen

In de volgende lijst worden de beschikbare variabelen beschreven.

### entity.id

Alleen randwaarde.

Deze vereiste parameter identificeert het product. Deze alfanumerieke id moet overal hetzelfde zijn [!DNL Adobe Experience Cloud] producten die worden gebruikt, waaronder [!DNL Analytics], zodat de verschillende producten het item herkennen en er gegevens over uitwisselen.

De `entity.id` waarden moeten *niet* bevatten schuine strepen, ampersands, vraagtekens, percentagesymbolen, komma&#39;s of andere leestekens die URL-codering vereisen wanneer deze worden doorgegeven in een REST API-aanroep. Afbreekstreepjes en onderstrepingstekens zijn toegestaan. Ongeldige interpunctie opnemen in een `entity.id` waarde veroorzaakt sommige [!DNL Recommendations] functionaliteit om te mislukken.

Voorbeeld: `'entity.id=67833'`

### entity.name

Alleen één waarde.

De productnaam die op de Website wordt getoond wanneer het product wordt geadviseerd.

Voorbeeld: `'entity.name=Giants& vs& Rockies& 5/12'`

### entity.categoryId

Ondersteunt meerdere waarden (door komma&#39;s gescheiden lijst).

Categorie van de huidige pagina. De entiteit.categoryID kan meerdere categorieën bevatten, zoals een subsectie over cardigans (bijvoorbeeld vrouwen, vrouwen:zweet, vrouwen):sweaters:cardigans). Meerdere categorieën moeten worden gescheiden door komma&#39;s.

De `categoryId` waarde is beperkt tot 250 tekens.

>[!NOTE]
>
>Een aanbeveling weergeven op basis van een categorie in een [!UICONTROL Category] pagina, slechts één `categoryId` kan in mbox worden overgegaan die wordt gebruikt om die bepaalde aanbeveling te tonen. De waarde van de `categoryId` moet exact overeenkomen met de waarde van `entity.categoryId` doorgegeven aan de [!UICONTROL Product Detail] pagina.

Voorbeelden:

* Voorbeeld van productdetailpagina: vrouwen, vrouwen:truien, vrouwen:sweaters:cardigans
* Voorbeeld van categorie Paginanummers: vrouwen:truien
* Voorbeeld van paginakaartjes voor categorieën: vrouwen:sweaters:cardigans

Voor op categorieën gebaseerde aanbevelingen wordt de categoriewaarde met een komma van elkaar gescheiden. Waarden die door komma&#39;s worden gescheiden, worden categorieën. U kunt ook subcategorieën definiëren door een ander scheidingsteken, zoals een dubbele punt (:), te gebruiken om subcategorieën binnen de categoriewaarde te scheiden.

In de volgende code is de categorie Vrouwen bijvoorbeeld onderverdeeld in verschillende subcategorieën:

```javascript
mboxCreate('mboxName', 'entity.id=343942-32', 'entity.categoryId= Womens, Womens:Outerwear, Womens:Outerwear:Jackets, Womens:Outerwear:Jackets:Parka, Womens:Outerwear:Jackets:Caban’, 'entity.thumbnailUrl=...', 'entity.message=...', );
```

Voor de levering mbox, wordt de langste kenmerknaam gebruikt voor de sleutel. Als er een tijd is, wordt het laatste kenmerk gebruikt. In het bovenstaande voorbeeld is de categorietoets Womens:Outerwear:Jasjes:Caban.

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

Een bericht over het product dat in de aanbeveling wordt getoond, zoals &quot;bij verkoop&quot; of &quot;klaring&quot;. Het bericht is doorgaans uitgebreider dan de productnaam. Gebruik entity.message om aanvullende informatie te definiëren die met het product in de sjabloon moet worden weergegeven.

Voorbeeld: `'entity.message=Family&nbsp;special'`

### entity.inventory

Alleen één waarde. Vereist een geheel getal of een lange waarde.

Hiermee geeft u het voorraadniveau van het item weer.

Voorbeeld: `'entity.inventory=1'`

**Afhandeling van lege inventariskenmerken:** Voor levering, als u een inclusieregel, inzamelingsregel, of criteria hebt die met plaatsen `entity.inventory` > 0 of `entity.inventory` = 0 en de voorraad van het product niet is vastgesteld; [!DNL Target] evalueert deze waarde aan WAAR en omvat producten waar de inventaris niet wordt geplaatst. Dit heeft tot gevolg dat producten met een voorraad die niet is ingesteld, in de resultaten van aanbevelingen worden weergegeven.

Op dezelfde manier als u een globale uitsluitingsregel hebt met `entity.inventory` = 0 en `entity.inventory` niet is ingesteld, [!DNL Target] evalueert deze regel om WAAR te zijn en sluit het product uit.

**Bekend probleem:** Het zoeken naar producten is inconsistent met de levering voor de attributen van de inventariswaarde die niet worden geplaatst. Bijvoorbeeld voor een regel met `entity.inventory` = 0, wordt in Productzoekopdracht geen producten weergegeven waarvoor de inventariswaarde niet is ingesteld.

### entity.value

Alleen één waarde.

Hiermee definieert u de prijs of waarde van het item.

Voorbeeld: `'entity.value=15.99'`

entiteit.value ondersteunt alleen decimale notatie (bijvoorbeeld 15.99). De komma-indeling (15,99) wordt niet ondersteund.

### entity.margin

Alleen één waarde.

De winstmarge of andere waarde van de post.

Voorbeeld: `'entity.margin=1.00'`

### entiteit.*aangepast*

Ondersteunt multivalue (JSON-array).

Definieer maximaal 100 aangepaste variabelen die aanvullende informatie over het item bevatten. U kunt elke ongebruikte kenmerknaam opgeven voor elk aangepast kenmerk. U kunt bijvoorbeeld een aangepast kenmerk maken met de naam `entity.genre` om een boek of een film te definiëren. Een verkoper van vervoerbewijzen kan kenmerken voor een gebeurtenisplaats voor een secundaire uitvoerder, zoals een bezoekend team in een sportevenement of een openingsactie in een concert tot stand brengen.

Beperkingen:

* U kunt vooraf gedefinieerde namen van entiteitskenmerken niet gebruiken voor aangepaste entiteitskenmerken.
* Het attribuut entity.environment wordt gereserveerd door het systeem en kan niet voor de attributen van de douaneentiteit worden gebruikt. Pogingen om entiteit.environment door te geven met targetPageParams, feed of API worden genegeerd.

Voorbeelden:

`'entity.venue=AT&T&nbsp;Park'`

`'entity.secondary=Rockies'`

Aangepaste entiteitskenmerken ondersteunen meerdere waarden. Zie [Aangepaste entiteitskenmerken](/help/main/c-recommendations/c-products/custom-entity-attributes.md#limits) voor teken- en waardelimieten.

Voorbeeld: `'entity.secondary=["band1",&nbsp;"band2"]'`

Aangepaste entiteitskenmerken van meerdere waarden vereisen geldige JSON-arrays. Voor correcte syntaxisinformatie raadpleegt u [Kenmerken Aangepaste entiteit](/help/main/c-recommendations/c-products/custom-entity-attributes.md).

### entity.event.detailsOnly

Alleen één waarde.

Gebruikt om een mbox vraag te verhinderen gedragstellers van gegevens voor een algoritme te verhogen.

Voorbeeld: `'entity.event.detailsOnly=true'`

In de onderstaande voorbeelden werkt de eerste mbox-aanroep de catalogus en gedragsgegevens bij. De tweede mbox-aanroep werkt alleen de catalogus bij.

```javascript
mboxCreate('myMbox', 'profile.geo.city = new york', 'profile.geo.state = new york',  'entity.id = 'entity.inventory = 4' )
mboxCreate('myMbox',  'profile.geo.city = new york', 'profile.geo.state = new york',  'entity.id = 123', 'entity.inventory = 4' 'entity.event.detailsOnly=true' )
```

>[!MORELIKETHIS]
>
>* [Kenmerken Aangepaste entiteit](/help/main/c-recommendations/c-products/custom-entity-attributes.md#concept_E5CF39BCAC8140309A73828706288322)

