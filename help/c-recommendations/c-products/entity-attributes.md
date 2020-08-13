---
keywords: entity;entity attributes;pass information to Recommendations;behavioral data;data counter;define relative URL;display inventory level;define price;define profit margin;custom attributes
description: Gebruik entiteitskenmerken om product- of inhoudsgegevens door te geven aan Recommendations.
title: Entiteitskenmerken
feature: entities
uuid: 27672881-a79c-4271-9a61-defddb9a5249
translation-type: tm+mt
source-git-commit: 3cf1f4fa56f86c106dccdc2c97c080c17c3982b4
workflow-type: tm+mt
source-wordcount: '1006'
ht-degree: 0%

---


# ![PREMIUM](/help/assets/premium.png) -entiteitskenmerken{#entity-attributes}

Gebruik entiteitskenmerken om product- of inhoudsgegevens door te geven aan Recommendations.

## Beschikbare variabelen

In de volgende lijst worden de beschikbare variabelen beschreven.

### `entity.id`

Alleen randwaarde.

Deze vereiste parameter identificeert het product. Deze alfanumerieke id moet voor alle gebruikte [!DNL Adobe Experience Cloud] producten gelijk zijn, inclusief [!DNL Analytics], zodat de verschillende producten het item herkennen en er gegevens over uitwisselen.

`entity.id` waarden mogen geen slashes, ampersands, vraagtekens, percentagesymbolen, komma&#39;s of andere leestekens bevatten die URL-codering vereisen wanneer deze worden doorgegeven in een REST API-aanroep. Afbreekstreepjes en onderstrepingstekens zijn toegestaan. Het opnemen van ongeldige leestekens in een `entity.id` waarde leidt tot een fout [!DNL Recommendations] in de functionaliteit.

Voorbeeld: `'entity.id=67833'`

### `entity.name`

Alleen één waarde.

De productnaam die op de Website wordt getoond wanneer het product wordt geadviseerd.

Voorbeeld: `'entity.name=Giants& vs& Rockies& 5/12'`

### `entity.categoryId`

Ondersteunt meerdere waarden (door komma&#39;s gescheiden lijst).

Categorie van de huidige pagina. Dit kan meerdere categorieën omvatten, zoals een subsectie over cardigans (d.w.z. vrouwen, vrouwen:zweet, vrouwen:zweet:verzorgers). Meerdere categorieën moeten worden gescheiden door komma&#39;s.

`categoryId` is beperkt tot 250 tekens.

>[!NOTE]
>
>Als u een aanbeveling wilt weergeven die is gebaseerd op een categorie op een [!UICONTROL Category] pagina, `categoryId` kan slechts één aanbeveling worden doorgegeven in het vak waarin die specifieke aanbeveling wordt weergegeven. De waarde van de pagina `categoryId` moet exact overeenkomen met de waarde van `entity.categoryId` die op de [!UICONTROL Product Detail] pagina is doorgegeven.

Voorbeelden:

* Voorbeeld van productdetailpagina: vrouwen, vrouwen:truien, vrouwen:sweaters:cardigans
* Voorbeeld van categorie Paginanummers: vrouwen:truien
* Voorbeeld van paginakaartjes voor categorieën: vrouwen:sweaters:cardigans

Voor op categorieën gebaseerde aanbevelingen wordt een komma gebruikt om de categoriewaarde te scheiden. Waarden die door komma&#39;s worden gescheiden, worden categorieën. U kunt ook subcategorieën definiëren door een ander scheidingsteken, zoals een dubbele punt (:), te gebruiken om subcategorieën binnen de categoriewaarde te scheiden.

In de volgende code is de categorie Vrouwen bijvoorbeeld onderverdeeld in verschillende subcategorieën:

```
mboxCreate('mboxName', 'entity.id=343942-32', 'entity.categoryId= Womens, Womens:Outerwear, Womens:Outerwear:Jackets, Womens:Outerwear:Jackets:Parka, Womens:Outerwear:Jackets:Caban’, 'entity.thumbnailUrl=...', 'entity.message=...', );
```

Voor de levering mbox, wordt de langste kenmerknaam gebruikt voor de sleutel. Als er een tijd is, wordt het laatste kenmerk gebruikt. In het bovenstaande voorbeeld is de categorietoets Womens:Buitendgoedkleding:Jackets:Caban.

### `entity.brand`

Alleen één waarde.

Hiermee geeft u de merknaam van een item weer.

Voorbeeld: `'entity.brand=brandxyz'`

### `entity.pageUrl`

Alleen één waarde.

Definieert de relatieve URL van de pagina waarop het item kan worden aangeschaft.

Voorbeeld: `'entity.pageUrl=baseball/giants-tix/giantsvrockies5.12.2000-67833'`

### `entity.thumbnailUrl`

Alleen één waarde.

Definieert de relatieve URL ten opzichte van de miniatuurafbeelding die bij het item wordt weergegeven.

Voorbeeld: `'entity.thumbnailUrl=baseball/giants-tix/giants-136px.gif'`

### `entity.message`

Alleen één waarde.

Een bericht over het product dat in de aanbeveling wordt getoond, zoals &quot;bij verkoop&quot; of &quot;klaring&quot;. Het bericht is doorgaans uitgebreider dan de productnaam. Gebruik deze optie om aanvullende informatie te definiëren die met het product in de sjabloon moet worden weergegeven.

Voorbeeld: `'entity.message=Family&nbsp;special'`

### `entity.inventory`

Alleen één waarde. Vereist een geheel getal of een lange waarde.

Hiermee geeft u het voorraadniveau van het item weer.

Voorbeeld: `'entity.inventory=1'`

**Afhandeling van lege inventariskenmerken:** Voor levering, als u een inclusieregel, inzamelingsregel, of criteria die met `entity.inventory` > 0 of `entity.inventory` = 0 plaatst hebt en het product voorraad niet plaatste, [!DNL Target] evalueert dit aan WAAR en omvat producten waar de inventaris niet wordt geplaatst. Dit is standaard gedaan, zodat producten met een voorraad die niet is ingesteld, in de resultaten van de aanbeveling worden weergegeven.

Op dezelfde manier als u een globale uitsluitingsregel met `entity.inventory` = 0 hebt en niet `entity.inventory` wordt geplaatst, [!DNL Target] evalueert deze regel om WAAR te zijn en sluit het product uit.

**Bekend probleem:** Productzoekopdracht is inconsistent met levering voor niet-ingestelde voorraadwaardekenmerken. Voor een regel met `entity.inventory` = 0 geeft productzoekopdracht bijvoorbeeld geen producten weer waarvan de inventariswaarde niet is ingesteld.

### `entity.value`

Alleen één waarde.

Hiermee definieert u de prijs of waarde van het item.

Voorbeeld: `'entity.value=15.99'`

### `entity.margin`

Alleen één waarde.

De winstmarge of andere waarde van de post.

Voorbeeld: `'entity.margin=1.00'`

### `entity.<custom>`

Ondersteunt multivalue (JSON-array).

Definieer maximaal 100 aangepaste variabelen die aanvullende informatie over het item bevatten. U kunt elke ongebruikte kenmerknaam opgeven voor elk aangepast kenmerk. U kunt bijvoorbeeld een aangepast kenmerk maken dat wordt aangeroepen `entity.genre` om een boek of film te definiëren. Of een verkoper van vervoerbewijzen kan kenmerken maken voor een plaats van een evenement voor een tweede uitvoerder, zoals een bezoekend team in een sportevenement of een openingsactie in een concert.

Beperkingen:

* U kunt vooraf gedefinieerde namen van entiteitskenmerken niet gebruiken voor aangepaste entiteitskenmerken.
* Het attribuut entity.environment wordt gereserveerd door het systeem en kan niet voor de attributen van de douaneentiteit worden gebruikt. Pogingen om entiteit.environment door te geven met targetPageParams, feed of API worden genegeerd.

Voorbeelden:

`'entity.venue=AT&T&nbsp;Park'`

`'entity.secondary=Rockies'`

Aangepaste entiteitskenmerken ondersteunen meerdere waarden. Zie Kenmerken [van](/help/c-recommendations/c-products/custom-entity-attributes.md#limits) aangepaste entiteiten voor teken- en waardelimieten.

Voorbeeld: `'entity.secondary=["band1",&nbsp;"band2"]'`

>[!NOTE]
>
>Aangepaste entiteitskenmerken van meerdere waarden vereisen geldige JSON-arrays. Zie Aangepaste entiteitskenmerken voor correcte syntaxisinformatie.

### `entity.event.detailsOnly`

Alleen één waarde.

Gebruikt om een mbox vraag te verhinderen gedragstellers van gegevens voor een algoritme te verhogen.

Voorbeeld: `'entity.event.detailsOnly=true'`

In de onderstaande voorbeelden worden de catalogus en gedragsgegevens bijgewerkt met de eerste aanroep van het mbox. De tweede mbox-aanroep werkt alleen de catalogus bij.

```
mboxCreate('myMbox', 'profile.geo.city = new york', 'profile.geo.state = new york',  'entity.id = 'entity.inventory = 4' )
mboxCreate('myMbox',  'profile.geo.city = new york', 'profile.geo.state = new york',  'entity.id = 123', 'entity.inventory = 4' 'entity.event.detailsOnly=true' )
```

## Entiteitskenmerken gebruiken

>[!NOTE]
>
>Waarden van opgegeven entiteitskenmerken verlopen na 61 dagen. Dit betekent dat u ervoor moet zorgen dat de recentste waarde van elk entiteitattribuut aan Doel Recommendations minstens eens per maand voor elk punt in uw catalogus wordt overgegaan.

Recommendations verzendt de code `productId` of `productPurchasedId` (wordt `entity.id` in de code genoemd) die in de algoritmen wordt gebruikt.

>[!NOTE]
>
>`entity.id` moet overeenkomen met de pagina `productPurchasedId` die naar de pagina voor bevestiging van de bestelling is verzonden en met de pagina&#39;s die in Adobe Analytics-productrapporten worden `productId` gebruikt).

De meeste vooraf gedefinieerde parameters accepteren slechts één waarde, waarbij nieuwe waarden oude waarden overschrijven. De `categoryId` parameter kan een door komma&#39;s gescheiden lijst met waarden accepteren voor elke categorie die dat product bevat. Nieuwe `categoryId` waarden overschrijven bestaande waarden niet, maar worden toegevoegd tijdens het bijwerken van een entiteit (limiet van 250 tekens).

Over het algemeen ziet het informatievenster voor de weergave er als in het volgende voorbeeld uit als u at.js 1 gebruikt.*x* met `mboxCreate`.

>[!NOTE]
>
>Als u at.js 2 gebruikt.*x*, `mboxCreate` (zoals in het volgende voorbeeld wordt gebruikt) wordt niet meer ondersteund. Product- of inhoudsgegevens doorgeven aan Recommendations met behulp van at.js 2.*x*, gebruik [targetPageParams](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetpageparams.md). Zie Recommendations [](/help/c-recommendations/plan-implement.md)plannen en implementeren voor een voorbeeld hiervan.

>[!NOTE]
>
>Alle kenmerken van de entiteitsparameter zijn hoofdlettergevoelig.

```
<div class="mboxDefault"></div><script language="JavaScript1.2"> 
 
mboxCreate('productPage', 
 
'entity.id=67833', 
 
'entity.name=GIANTS VS ROCKIES 5/12', 
 
'entity.categoryId=BASEBALL, GIANTS, SF BAY AREA', 
 
'entity.pageUrl=../baseball/giants-tix/giantsvrockies5.12.2000-67833', 
 
'entity.venue=AT&T PARK', 
 
'entity.secondary=ROCKIES', 
 
'entity.thumbnailUrl=../baseball/giants-tix/giants-136px.gif', 
 
'entity.message=FAMILY SPECIAL', 
 
'entity.value=15.99', 
 
'entity.inventory=1' 
 
); 
 
</script>
```

>[!NOTE]
>
>Relatieve URL&#39;s hebben de voorkeur voor `pageUrl` en `thumbnailUrl` niet voor absolute URL&#39;s, omdat aanbevelingen gegevens ontvangen die worden verzonden vanuit alle omgevingen op uw site. Als u relatieve URL&#39;s gebruikt, vermijdt u hardcodeerde koppelingen naar een testserver of ontwikkelingsserver.

Als het selectievakje op een productpagina staat, kunt u zowel de product-id als de categorie-id opnemen. Het geselecteerde algoritme bepaalt welke weergaven worden weergegeven. De product-id wordt gebruikt voor affiniteitsalgoritmen en de categorie-id wordt gebruikt voor categoriealgoritmen.

## Verwante onderwerpen:

* [Kenmerken Aangepaste entiteit](../../c-recommendations/c-products/custom-entity-attributes.md#concept_E5CF39BCAC8140309A73828706288322)
