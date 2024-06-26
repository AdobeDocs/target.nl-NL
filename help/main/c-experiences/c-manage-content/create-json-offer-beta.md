---
keywords: json-aanbieding;create json-aanbieding
description: Leer hoe u JSON-aanbiedingen kunt maken voor gebruik in de [!UICONTROL Form-Based Experience Composer].
title: Hoe maak ik JSON-aanbiedingen?
feature: Experiences and Offers
hide: true
hidefromtoc: true
source-git-commit: 98613f43c5f135a6ce61a4b8dcc7f2b372df51e2
workflow-type: tm+mt
source-wordcount: '426'
ht-degree: 0%

---

# JSON-aanbiedingen maken

JSON-aanbiedingen maken in het dialoogvenster [!UICONTROL Offer Library] in [!DNL Adobe Target] voor gebruik in de [!UICONTROL Form-Based Experience Composer].

JSON-aanbiedingen kunnen worden gebruikt in formuliergebaseerde activiteiten om gebruiksituaties mogelijk te maken waarin [!DNL Target] Beslissing is vereist om een aanbod in JSON-indeling te verzenden voor gebruik in SPA framework of serverintegratie.

## JSON-overwegingen

Houd rekening met de volgende informatie terwijl u met JSON werkt:

* JSON-voorstellen zijn momenteel alleen beschikbaar voor [!UICONTROL A/B Test], [!UICONTROL Automated Personalization] (AP), en [!UICONTROL Experience Targeting] (XT) activiteiten.
* JSON-aanbiedingen kunnen worden gebruikt in [op formulieren gebaseerde activiteiten](/help/main/c-experiences/form-experience-composer.md) alleen.
* JSON-aanbiedingen kunnen rechtstreeks worden opgehaald wanneer u de [Server Side API&#39;s en Mobile Node.js, Java, .NET en Python SDK&#39;s](https://experienceleague.adobe.com/docs/target-dev/developer/server-side/server-side-overview.html){target=_blank}.
* In de browser kunnen JSON-aanbiedingen alleen worden opgehaald via at.js 1.2.3 (of hoger) en via [getOffer()](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/functions-overview/adobe-target-getoffer.html){target=_blank} door acties te filteren met de `setJson` handeling.
* JSON-aanbiedingen worden geleverd als native JSON-objecten in plaats van als tekenreeksen. Consumenten van deze objecten hoeven objecten niet langer als tekenreeksen te verwerken en deze in JSON-objecten om te zetten.
* JSON-aanbiedingen worden niet automatisch toegepast in tegenstelling tot andere aanbiedingen (zoals HTML-aanbiedingen), omdat JSON-aanbiedingen niet-visuele aanbiedingen zijn. Ontwikkelaars moeten code schrijven om de aanbieding expliciet op te halen met [getOffer()](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/functions-overview/adobe-target-getoffer.html){target=_blank}.

## Een JSON-aanbieding maken {#section_BB9C72D59DEA4EFB97A906AE7569AD7A}

1. Klikken **[!UICONTROL Offers]** > **[!UICONTROL Code Offers]**.

   ![Aanbiedingen > tabblad Codevoorstellen](/help/main/c-experiences/c-manage-content/assets/code-offers-tab-new.png)

1. Klikken **[!UICONTROL Create Offer]** > **[!UICONTROL JSON Offer]**.

   ![aanbiedingsafbeelding](assets/offer-json-new.png)

1. Typ een naam voor het voorstel.
1. (Voorwaardelijk) Als u een [[!DNL Target] Premium-account](/help/main/c-intro/intro.md#premium)kiest u de gewenste [werkruimte](/help/main/administrating-target/c-user-management/property-channel/property-channel.md#workspace).
1. (Voorwaardelijk) Kies de gewenste profielkenmerken.
1. Typ of plak uw JSON-code in het dialoogvenster **[!UICONTROL Code]** doos.
1. Klik op **[!UICONTROL Create]**.

## JSON-voorbeeld {#section_A54F7BB2B55D4B7ABCD5002E0C72D8C9}

JSON-aanbiedingen worden alleen ondersteund in activiteiten die zijn gemaakt met de [Formuliergebaseerde Experience Composer](/help/main/c-experiences/form-experience-composer.md). De enige manier om JSON-aanbiedingen te kunnen gebruiken is momenteel via directe API/SDK-aanroepen.

Hier volgt een voorbeeld:

```json
adobe.target.getOffer({ 
  mbox: "some-mbox", 
  success: function(actions) { 
    console.log('Success', actions); 
  }, 
  error: function(status, error) { 
    console.log('Error', status, error); 
  } 
});
```

De acties die aan succesvolle callback worden overgegaan zijn een serie van voorwerp. Ervan uitgaande dat u één JSON-aanbieding hebt, die de volgende inhoud heeft:

```json
{ 
  "demo": {"a": 1, "b": 2} 
}
```

De actiesarray heeft deze structuur:

```json
[ 
 { 
   action: "setJson", 
   content: [{ 
     "demo": {"a": 1, "b": 2} 
   }] 
 }  
]
```

Als u het JSON-aanbod wilt uitpakken, doorloopt u de handelingen en zoekt u de handeling met de `setJson` en doorloopt vervolgens de inhoudarray.

## Hoofdletters gebruiken {#section_85B07907B51A43239C8E3498EF58B1E5}

Stel dat de volgende JSON-aanbieding op uw webpagina wordt afgeleverd:

```json
{ 
    "_id": "5a65d24d8fafc966921e9169", 
    "index": 0, 
    "guid": "7c006504-c6f7-468d-a46f-f72531ea454c", 
    "isActive": true, 
    "balance": "$2,075.06", 
    "picture": "https://placehold.it/32x32", 
    "tags": [ 
      "esse", 
      "commodo", 
      "excepteur"
    ], 
    "friends": [ 
      { 
        "id": 0, 
        "name": "Carla Lyons" 
      }, 
      { 
        "id": 1, 
        "name": "Ollie Mooney" 
      } 
    ], 
    "greeting": "Hello, Stephenson Fernandez! You have 4 unread messages.", 
    "favoriteFruit": "strawberry" 
} 
  
```

De volgende code toont hoe te om tot het &quot;groet&quot;attribuut toegang te hebben:

```json
adobe.target.getOffer({   
  "mbox": "name_of_mbox", 
  "params": {}, 
  "success": function(offer) {           
        console.log(offer[0].content[0].greeting); 
  },   
  "error": function(status, error) {           
      console.log('Error', status, error); 
  } 
});
```

## JSON-aanbiedingsvoorbeeld met CDP-profielkenmerken in realtime

CDP-profielkenmerken in realtime kunnen worden gedeeld met [!DNL Target] voor gebruik in HTML- en JSON-aanbiedingen.

Zie voor meer informatie [CDP-profielkenmerken in realtime delen met [!DNL Target]](/help/main/c-integrating-target-with-mac/integrating-with-rtcdp.md#rtcdp-profile-attributes).

## Aanbiedingen filteren door het type JSON-aanbieding {#section_52533555BCE6420C8A95EB4EB8907BDE}

U kunt het filter [!UICONTROL Offers] bibliotheek van het aanbiedingstype JSON door op het **[!UICONTROL Show filters]** pictogram, dan door **[!UICONTROL JSON]** selectievakje.

![aanbieding-json-filter beeld](assets/offer-json-filter-new.png)