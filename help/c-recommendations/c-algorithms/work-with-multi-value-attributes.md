---
keywords: multi-value;attributes;recommendations;multi-value;multivalue;multi-value
description: Leer hoe u met een veld met meerdere waarden in Adobe Target Recommendations werkt met speciale operatoren voor meerdere waarden, bijvoorbeeld wanneer u films met meerdere acteurs aanbeveelt.
title: Kan ik multiwaardekenmerken gebruiken in Recommendations?
feature: Recommendations
translation-type: tm+mt
source-git-commit: bb27f6e540998f7dbe7642551f7a5013f2fd25b4
workflow-type: tm+mt
source-wordcount: '455'
ht-degree: 0%

---


# Werken met kenmerken van meerdere waarden

Soms wilt u wellicht werken met een veld met meerdere waarden. Neem de volgende voorbeelden:

* U biedt films aan gebruikers aan. Een bepaalde film heeft meerdere acteurs.
* Je verkoopt tickets aan concerten. Een bepaalde gebruiker heeft meerdere favoriete banden.
* Je verkoopt kleding. Een shirt is verkrijgbaar in verschillende formaten.

Om aanbevelingen in deze scenario&#39;s te behandelen, kunt u multi-waardegegevens tot [!DNL Target Recommendations] overgaan en speciale multi-waardeexploitanten gebruiken.

Om [!DNL Recommendations] toe te staan om multi-waardegegevens te identificeren, zou het als serie JSON, zoals in de hieronder codesteekproeven moeten worden verzonden.

## Een parameter met meerdere waarden doorgeven in JavaScript

```
function targetPageParams() { 
  return { 
    'entity.id':                   '123', 
    'entity.categoryId':            '["A", "A:B", "A:B:C", "A:B:C:D"]',        
    'entity.MultiValueAttribute':   '["X", "Y", "Z"]', 
    'entity.event.detailsOnly':     'true', 
    'excludedIds":                  '[123, 3232, 2323, 4344]', 
    'orderId":                      '123456', 
    'orderTotal":                   '195.32', 
    'productPurchaseId":            '[001,002,003]' 
  }; 
}
```

Zie [Meerwaardekenmerken implementeren](/help/c-recommendations/c-products/custom-entity-attributes.md#section_80FEFE49E8AF415D99B739AA3CBA2A14) in *Aangepaste entiteitskenmerken* voor meer informatie.

## Een kenmerk van een entiteit met meerdere waarden doorgeven in een CSV-bestand

```
## RECSRecommendations Upload File,,,,,,,,,,,,,,,,,,,
## RECS''## RECS'' indicates a Recommendations pre-process header. Please do not remove these lines.,,,,,,,,,,,,,,,,,,,
## RECS,,,,,,,,,,,,,,,,,,,
## RECSUse this file to upload product display information to Recommendations. Each product has its own row. Each line must contain 19 values and if not all are filled a space should be left.,,,,,,,,,,,,,,,,,,,
## RECSThe last 100 columns (entity.custom1 - entity.custom100) are custom. The name 'customN' can be replaced with a custom name such as 'onSale' or 'brand'.,,,,,,,,,,,,,,,,,,,
## RECSIf the products already exist in Recommendations then changes uploaded here will override the data in Recommendations. Any new attributes entered here will be added to the product''s entry in Recommendations.,,,,,,,,,,,,,,,,,,,
## RECSentity.id ,entity.name,entity. categoryId ,entity. message ,entity.thumbnailUrl ,entity.value ,entity.pageUrl ,entity.inventory ,entity.margin ,entity.custom1 ,entity.custom2 ,entity.custom3 ,entity.custom4,entity.custom5,entity.custom6,entity.custom7,entity.custom8,entity.custom9,entity.custom10,
1,Sample Product 1,category1,Save 10%,http://sample.store/products/images/product1_th.jpg,325,http://sample.store/products/product_detail.jsp?productId=1,1000,48,a,"[ ""v1"", ""v2"" ]",, , , , , , , ,
2,Sample Product 2,category1,Save 10%,http://sample.store/products/images/product2_th.jpg,369,http://sample.store/products/product_detail.jsp?productId=2,1000,52,a,"[ ""v1"", ""v2"" ]",, , , , , , , ,
3,Sample Product 3,category1,Save 10%,http://sample.store/products/images/product3_th.jpg,479,http://sample.store/products/product_detail.jsp?productId=3,1000,78,a,"[ ""v1"", ""v2"" ]",,,,,,,,,
4,Sample Product 4,category1,Save 10%,http://sample.store/products/images/product4_th.jpg,409,http://sample.store/products/product_detail.jsp?productId=4,1000,66,a,"[ ""v1"", ""v2"" ]",,,,,,,,,
5,Sample Product 5,category1,Save 10%,http://sample.store/products/images/product5_th.jpg,325,http://sample.store/products/product_detail.jsp?productId=5,1000,45,a,"[ ""v1"", ""v2"" ]",,,,,,,,, 
```

Wanneer een entiteitskenmerk, profielkenmerk of mbox-parameter wordt opgegeven als een meerwaarde volgens de bovenstaande indeling, geeft [!DNL Recommendations] automatisch aan dat het veld een meerwaarde is.

De volgende operatoren zijn beschikbaar voor gebruik met multi-value entiteit-, profiel- en mbox-kenmerken:

* [!UICONTROL is contained in list]
* [!UICONTROL is not contained in list]

## Werken met kenmerken van meerdere waarden in integratieregels

>[!NOTE]
>
>Ondersteuning voor dynamische overeenkomst met kenmerken van meerdere waarden is momenteel alleen beschikbaar op basis van criteria bij het gebruik van een profielkenmerk dat overeenkomt met of parameterkenmerk dat overeenkomt met de regel bij het vergelijken van één waarde aan de linkerkant naar een meerwaarde aan de rechterkant. Attributen met meerdere waarden worden momenteel niet ondersteund in promoties, overeenkomsten tussen entiteitskenmerken of voor lijsten aan de linkerkant van insluitingsregels.

### Voorbeeld: Onlangs gevolgde objecten uitsluiten

Stel dat u wilt voorkomen dat films die zich in de laatste tien gecontroleerde films van de gebruiker bevinden, worden aanbevolen. Schrijf eerst een profielscript met de naam `user.lastWatchedMovies` om de laatste tien bekeken films als een JSON-array bij te houden. Dan, kunt u de punten uitsluiten door de volgende inclusieregel te gebruiken:

```
`Profile Attribute Matching`
`id - is not contained in list - user.lastWatchedMovies`
```

JSON API-representatie van de insluitingsregel:

```
{
    "attribute": "id",
    "operation": "isNotContainedInList",
    "source": {
        "name": "user.lastWatchedMovies",
        "type": "PROFILE"
    }
} 
```

### Voorbeeld: Aanbevolen objecten uit de favorieten van de gebruiker

Stel dat u alleen tickets aan concerten wilt aanbevelen als de band die wordt afgespeeld een van de favoriete banden van de gebruiker is. Eerst, zorg ervoor dat u een profielvariabele genoemd `profile.favoriteBands` hebt die de favoriete banden van de gebruiker bevat. Zorg er vervolgens voor dat uw catalogus een kenmerk `entity.artistPerforming` bevat dat de artiest bevat die in het concert uitvoert. Vervolgens kunt u de volgende inclusieregel gebruiken:

```
`Profile Attribute Matching`
`artistPerforming - is contained in list - profile.favoriteBands`
```

JSON API-representatie van de insluitingsregel:

```
{
    "attribute": "artistPerforming",
    "operation": "isContainedInList",
    "source": {
        "name": "profile.favoriteBands",
        "type": "PROFILE"
    }
}
```

### Voorbeeld: API maken van criteria voor het aanbevelen van items uit de favorieten van een gebruiker

U kunt criteria maken met filterregels voor meerdere waarden, zoals alle criteria, via Adobe I/O API&#39;s. Een voorbeeld-API-aanroep om een criterium te maken waarbij het entiteitskenmerk `id` in de parameterlijst mbox `favorites` is opgenomen, wordt hier gegeven:

```
curl -X POST \
  https://<serverhost>/api/recs/<client>/criteria/item \
  -H 'Accept: application/vnd.adobe.target.v1+json' \
  -H 'Accept-Encoding: gzip, deflate' \
  -H 'Cache-Control: no-cache' \
  -H 'Connection: keep-alive' \
  -H 'Content-Type: application/json' \
  -H 'User-Agent: <from API client>' \
  -H 'X-Target-user-email: <email address>' \
  -H 'cache-control: no-cache' \
  -d '{
    "name": "viewed criteria",
    "criteriaTitle": "test title",
    "type": "VIEWED_CF",
    "key": "CURRENT",
    "daysCount": "TWO_WEEKS",
    "aggregation": "NONE",
    "backupDisabled": false,
    "partialDesignAllowed": true,
    "configuration": {
        "inclusionRules": [
            {
                "attribute": "id",
                "operation": "isContainedInList",
                "source": {
                    "name": "mbox.favorites",
                    "type": "MBOX"
                }
            }
        ]
    }
}'
```

Dit zou in combinatie met JavaScript op de pagina worden doorgegeven om de favoriete inhoud door te geven:

```
<!-- pass in the value of mbox parameter “favorites” as JSON array -->
<script type="text/javascript">
   mboxCreate('myMbox','entity.id=<key>','favorites=["a","b","c"]');
</script>
```
