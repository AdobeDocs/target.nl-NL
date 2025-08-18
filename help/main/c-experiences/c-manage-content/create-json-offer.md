---
keywords: json-aanbieding;create json-aanbieding
description: Leer hoe u JSON-aanbiedingen maakt voor gebruik in de [!UICONTROL Form-Based Experience Composer] .
title: Hoe maak ik JSON-aanbiedingen?
feature: Experiences and Offers
exl-id: 793665a4-4cd6-458f-8225-ba23e503a115
source-git-commit: e8201198dc6ac36e803153d5c6b345a30716204a
workflow-type: tm+mt
source-wordcount: '425'
ht-degree: 0%

---

# JSON-aanbiedingen maken

Maak JSON-aanbiedingen in de [!UICONTROL Offer Library] in [!DNL Adobe Target] voor gebruik in de [!UICONTROL Form-Based Experience Composer] .

JSON-aanbiedingen kunnen worden gebruikt in op formulieren gebaseerde activiteiten om gebruiksgevallen mogelijk te maken waarbij [!DNL Target] -beslissingen vereist zijn voor het verzenden van een aanbieding in JSON-indeling voor gebruik in SPA-framework of serverintegratie.

## JSON-overwegingen

Houd rekening met de volgende informatie terwijl u met JSON werkt:

* JSON-aanbiedingen zijn momenteel alleen beschikbaar voor [!UICONTROL A/B Test]-, [!UICONTROL Automated Personalization] (AP)- en [!UICONTROL Experience Targeting] (XT)-activiteiten.
* De aanbiedingen JSON kunnen in [ vorm-gebaseerde activiteiten ](/help/main/c-experiences/form-experience-composer.md) slechts worden gebruikt.
* De aanbiedingen JSON kunnen direct worden teruggewonnen wanneer u de [ Zijde APIs van de Server en Mobiele Node.js, Java, .NET, en Python SDKs ](https://experienceleague.adobe.com/nl/docs/target-dev/developer/server-side/server-side-overview){target=_blank} gebruikt.
* In browser, kunnen de aanbiedingen JSON slechts via at.js 1.2.3 (of recenter) worden teruggewonnen en [ getOffer () gebruiken ](https://experienceleague.adobe.com/nl/docs/target-dev/developer/client-side/at-js-implementation/functions-overview/adobe-target-getoffer){target=_blank} door acties te filtreren gebruikend de `setJson` actie.
* JSON-aanbiedingen worden geleverd als native JSON-objecten in plaats van als tekenreeksen. Consumenten van deze objecten hoeven objecten niet langer als tekenreeksen te verwerken en deze in JSON-objecten om te zetten.
* JSON-aanbiedingen worden niet automatisch toegepast in tegenstelling tot andere aanbiedingen (zoals HTML-aanbiedingen) omdat JSON-aanbiedingen niet-visuele aanbiedingen zijn. De ontwikkelaars moeten code schrijven om de aanbieding uitdrukkelijk te krijgen gebruikend [ getOffer () ](https://experienceleague.adobe.com/nl/docs/target-dev/developer/client-side/at-js-implementation/functions-overview/adobe-target-getoffer){target=_blank}.

## Een JSON-aanbieding maken {#section_BB9C72D59DEA4EFB97A906AE7569AD7A}

1. Klik op **[!UICONTROL Offers]** > **[!UICONTROL Code Offers]** .
1. Klik op **[!UICONTROL Create Offer]** > **[!UICONTROL JSON Offer]** .
1. Typ een naam voor het voorstel.
1. (Voorwaardelijk) als u de rekening van de a [[!DNL Target]  Premium ](/help/main/c-intro/intro.md#premium) hebt, kies de gewenste [ werkruimte ](/help/main/administrating-target/c-user-management/property-channel/property-channel.md#workspace).
1. (Voorwaardelijk) Kies de gewenste profielkenmerken.
1. Typ of plak de JSON-code in het vak **[!UICONTROL Code]** .
1. Klik op **[!UICONTROL Create]**.

## JSON-voorbeeld {#section_A54F7BB2B55D4B7ABCD5002E0C72D8C9}

De aanbiedingen JSON worden gesteund slechts in activiteiten die worden gecreeerd gebruikend [ vorm-Gebaseerde Composer van de Ervaring ](/help/main/c-experiences/form-experience-composer.md). De enige manier om JSON-aanbiedingen te kunnen gebruiken is momenteel via directe API/SDK-aanroepen.

Hier volgt een voorbeeld:

![ creeer JSON de dialoogdoos van de aanbieding ](/help/main/c-experiences/c-manage-content/assets/json-example.png)

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

Als u het JSON-aanbod wilt extraheren, doorloopt u de handelingen en zoekt u de handeling met de handeling `setJson` en doorloopt u vervolgens de inhoudarray.

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

Voor meer informatie, zie [ de Attributen van het Profiel in real time CDP van het Aandeel met  [!DNL Target]](/help/main/c-integrating-target-with-mac/integrating-with-rtcdp.md#rtcdp-profile-attributes).

## Aanbiedingen filteren door het type JSON-aanbieding {#section_52533555BCE6420C8A95EB4EB8907BDE}

U kunt de [!UICONTROL Offers] bibliotheek door het aanbiedingstype van JSON filtreren door het **[!UICONTROL Show filters]** pictogram ( ![ tonen het pictogram van Filters ](/help/main/assets/icons/Filter.svg)) te klikken, dan door **[!UICONTROL JSON Offers]** checkbox te selecteren.
