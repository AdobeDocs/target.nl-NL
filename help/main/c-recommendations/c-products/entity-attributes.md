---
keywords: entiteit;entiteitskenmerken;geef informatie door aan Aanbevelingen;gedragsgegevens;gegevensteller;definieer relatieve URL;geef voorraadniveau weer;definieer prijs;definieer winstmarge;eigen kenmerken
description: Leer hoe te om entiteitattributen te gebruiken om product of inhoudsinformatie tot  [!DNL Target]  Aanbevelingen over te gaan.
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=nl-NL#premium newtab=true" tooltip="Kijk wat er in Target Premium is opgenomen."
title: Hoe gebruik ik entiteitskenmerken?
feature: Recommendations
exl-id: 4ed5fad3-b8b6-4675-a741-9f85cf73fcf1
source-git-commit: b6697eee5925cb8fa3b2fa2e107af0c617d30f94
workflow-type: tm+mt
source-wordcount: '1078'
ht-degree: 0%

---

# Entiteitskenmerken

Gebruik entiteitskenmerken om product- of inhoudsinformatie door te geven aan [!DNL Adobe Target Recommendations] .

Entiteiten verwijzen naar de items die u wilt aanbevelen. De entiteiten kunnen producten, inhoud (artikelen, diashows, beelden, films, en televisieprogramma&#39;s), baanaanbiedingen, restaurants, etc. omvatten.

[!DNL Recommendations] verzendt `productId` of `productPurchasedId` (in de code `entity.id` genoemd) die in de algoritmen wordt gebruikt.

Overweeg het volgende:

* `entity.id` moet overeenkomen met de `productPurchasedId` die naar de pagina voor bevestiging van de bestelling is verzonden en de `productId` die in [!DNL Adobe Analytics] -productrapporten wordt gebruikt.
* Waarden van entiteitskenmerken die u doorgeeft aan [!DNL Recommendations] verlopen na 61 dagen. Adobe raadt aan dat u de laatste waarde van elk entiteitskenmerk ten minste één keer per maand doorgeeft aan [!DNL Recommendations] voor elk item in de catalogus.

De meeste vooraf gedefinieerde parameters accepteren slechts één waarde, waarbij nieuwe waarden oude waarden overschrijven. De parameter `categoryId` kan een door komma&#39;s gescheiden lijst met waarden accepteren voor elke categorie die dat product bevat. Nieuwe `categoryId` -waarden overschrijven geen bestaande waarden, maar worden toegevoegd tijdens het bijwerken van een entiteit (limiet van 250 tekens).

In het algemeen ziet het informatievenster voor de weergave er als in het volgende voorbeeld uit als u at.js 1 gebruikt.*x* met `mboxCreate`. Alle attributen van de entiteitparameter zijn case-sensitive.

>[!NOTE]
>
>Als u at.js 2 gebruikt.*x*, `mboxCreate` (zoals die in het volgende voorbeeld wordt gebruikt) wordt niet meer gesteund. Product- of inhoudsgegevens doorgeven aan [!DNL Recommendations] met behulp van at.js 2.*x*, gebruik [&#x200B; targetPageParams &#x200B;](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/functions-overview/targetpageparams.html?lang=nl-NL){target=_blank}. Voor een voorbeeld, zie [&#x200B; Plan en voer Aanbevelingen &#x200B;](https://experienceleague.adobe.com/docs/target-dev/developer/recommendations.html?lang=nl-NL){target=_blank} uit.

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

Deze vereiste parameter identificeert het product. Deze alfanumerieke id moet hetzelfde zijn voor alle gebruikte [!DNL Adobe Experience Cloud] producten, inclusief [!DNL Analytics] , zodat de verschillende producten het item herkennen en er gegevens over kunnen delen.

De `entity.id` waarden moeten ** geen ruimten, schuine strepen, ampersands, vraagtekens, percentagesymbolen, komma&#39;s, of andere leestekens bevatten die URL het coderen wanneer overgegaan in een REST API vraag vereisen. Afbreekstreepjes en onderstrepingstekens zijn toegestaan. Het opnemen van ongeldige interpunctie in een `entity.id` -waarde leidt tot een fout in de [!DNL Recommendations] -functionaliteit.

Voorbeeld: `'entity.id=67833'`

### entity.name

Alleen één waarde.

De productnaam die op de Website wordt getoond wanneer het product wordt geadviseerd.

Voorbeeld: `'entity.name=Giants& vs& Rockies& 5/12'`

### entity.categoryId

Ondersteunt meerdere waarden (door komma&#39;s gescheiden lijst).

Categorie van de huidige pagina. De entity.categoryID kan meerdere categorieën bevatten, zoals een subsectie voor cardigans (bijvoorbeeld `womens` , `womens:sweaters` , `womens:sweaters:cardigans` ). Meerdere categorieën moeten worden gescheiden door komma&#39;s.

De waarde `categoryId` mag maximaal 250 tekens bevatten.

>[!NOTE]
>
>Als u een aanbeveling wilt weergeven op basis van een categorie op een [!UICONTROL Category] -pagina, kan slechts één `categoryId` worden doorgegeven in het mbox dat wordt gebruikt om die specifieke aanbeveling weer te geven. De waarde van de `categoryId` moet exact overeenkomen met de waarde van `entity.categoryId` die op de [!UICONTROL Product Detail] -pagina is doorgegeven.

Voorbeelden:

* Voorbeeld van productdetailpagina: `womens`, `womens:sweaters`, `womens:sweaters:cardigans`
* Voorbeeld van categorie Paginacooters: `womens:sweaters`
* Voorbeeld van paginakaartjes voor categorieën: `womens:sweaters:cardigans`

Voor op categorieën gebaseerde aanbevelingen wordt de categoriewaarde met een komma van elkaar gescheiden. Waarden die door komma&#39;s worden gescheiden, worden categorieën. U kunt ook subcategorieën definiëren door een ander scheidingsteken, zoals een dubbele punt (:), te gebruiken om subcategorieën binnen de categoriewaarde te scheiden.

In de volgende code is de categorie Vrouwen bijvoorbeeld onderverdeeld in verschillende subcategorieën:

```javascript
mboxCreate('mboxName', 'entity.id=343942-32', 'entity.categoryId= Womens, Womens:Outerwear, Womens:Outerwear:Jackets, Womens:Outerwear:Jackets:Parka, Womens:Outerwear:Jackets:Caban', 'entity.thumbnailUrl=...', 'entity.message=...', );
```

Voor de levering mbox, wordt de langste kenmerknaam gebruikt voor de sleutel. Als er een tijd is, wordt het laatste kenmerk gebruikt. In het bovenstaande voorbeeld is de categorietoets `Womens:Outerwear:Jackets:Caban` .

### entity.brand

Alleen één waarde.

Geeft de merknaam van een item weer.

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

**de Lege Behandeling van de Attributen van de Inventaris:** voor levering, als u een inclusieregel, inzamelingsregel, of criteria die met `entity.inventory` > 0 of `entity.inventory` = 0 hebt plaatsen en het product inventaris niet heeft, [!DNL Target] evalueert deze waarde aan WAAR en omvat producten waar de inventaris niet wordt geplaatst. Dit heeft tot gevolg dat producten met een voorraad die niet is ingesteld, in de resultaten van aanbevelingen worden weergegeven.

En als u een algemene uitsluitingsregel hebt met `entity.inventory` = 0 en `entity.inventory` niet is ingesteld, evalueert [!DNL Target] deze regel als TRUE en wordt het product uitgesloten.

**Bekende kwestie:** het Onderzoek van het Product is inconsistent met levering voor de attributen van de inventariswaarde die niet worden geplaatst. Voor een regel met `entity.inventory` = 0 geeft productzoekopdracht bijvoorbeeld geen producten weer waarvoor de inventariswaarde niet is ingesteld.

### entity.value

Alleen één waarde.

Hiermee definieert u de prijs of waarde van het item.

Voorbeeld: `'entity.value=15.99'`

entiteit.value ondersteunt alleen decimale notatie (bijvoorbeeld 15.99). De komma-indeling (15,99) wordt niet ondersteund.

### entity.margin

Alleen één waarde.

De winstmarge of andere waarde van de post.

Voorbeeld: `'entity.margin=1.00'`

### entiteit.*douane*

Ondersteunt multivalue (JSON-array).

Definieer maximaal 100 aangepaste variabelen die aanvullende informatie over het item bevatten. U kunt elke ongebruikte kenmerknaam opgeven voor elk aangepast kenmerk. U kunt bijvoorbeeld een aangepast kenmerk met de naam `entity.genre` maken om een boek of film te definiëren. Een verkoper van vervoerbewijzen kan kenmerken voor een gebeurtenisplaats voor een secundaire uitvoerder, zoals een bezoekend team in een sportevenement of een openingsactie in een concert tot stand brengen.

Beperkingen:

* U kunt vooraf gedefinieerde namen van entiteitskenmerken niet gebruiken voor aangepaste entiteitskenmerken.
* Het attribuut entity.environment wordt gereserveerd door het systeem en kan niet voor de attributen van de douaneentiteit worden gebruikt. Pogingen om entiteit.environment door te geven met targetPageParams, feed of API worden genegeerd.

Voorbeelden:

`'entity.venue=AT&T&nbsp;Park'`

`'entity.secondary=Rockies'`

Aangepaste entiteitskenmerken ondersteunen meerdere waarden. Zie [&#x200B; de entiteitattributen van de Douane &#x200B;](/help/main/c-recommendations/c-products/custom-entity-attributes.md#limits) voor karakter en waardegrenzen.

Voorbeeld: `'entity.secondary=["band1",&nbsp;"band2"]'`

Aangepaste entiteitskenmerken van meerdere waarden vereisen geldige JSON-arrays. Voor correcte syntaxisinformatie, zie {de Attributen van de Entiteit van 0} Douane [.](/help/main/c-recommendations/c-products/custom-entity-attributes.md)

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
>* [&#x200B; de Attributen van de Entiteit van de Douane &#x200B;](/help/main/c-recommendations/c-products/custom-entity-attributes.md#concept_E5CF39BCAC8140309A73828706288322)
