---
keywords: aanbevelingen ontwerp;ontwerp maken;ontwerp kopiëren
description: Leer hoe te om een  [!DNL Target Recommendations]  ontwerp tot stand te brengen gebruikend een standaardontwerp of door een douaneontwerp te creëren om de lay-out van uw pagina het best te passen.
title: Hoe maak ik een ontwerp in aanbevelingen?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=nl-NL#premium newtab=true" tooltip="Kijk wat er in Target Premium is opgenomen."
feature: Recommendations
exl-id: 0f10ee9d-7210-4e02-9342-e4f85cf46e8c
source-git-commit: 02ffe8da6cdf96039218656b9690fa719a77910c
workflow-type: tm+mt
source-wordcount: '979'
ht-degree: 0%

---

# Een ontwerp maken

Een ontwerp bepaalt hoe de aanbevelingen op een pagina verschijnen.

U kunt een [!UICONTROL Recommendations] -ontwerp maken met behulp van een standaardontwerp of door een aangepast ontwerp te maken. In het scherm **[!UICONTROL Recommendations > Designs]** worden zowel de standaardontwerpkaarten als alle ontwerpen weergegeven die in uw account zijn gemaakt.

Houd rekening met de volgende informatie wanneer u met ontwerpen werkt:

* U kunt een ontwerp met aanbevelingen maken door een standaardontwerp te gebruiken of u kunt een aangepast ontwerp maken.
* U kunt een standaardontwerp niet bewerken of verwijderen.
* U kunt een aangepast ontwerp bewerken, kopiëren of verwijderen.
* Als u een ontwerp wilt maken dat is gebaseerd op een standaardontwerp, moet u eerst het ontwerp kopiëren en vervolgens de kopie bewerken.

Deze illustratie toont het standaard 1 x 4 ontwerp:

![&#x200B; 1 x 4 standaardontwerp &#x200B;](/help/main/c-recommendations/c-design-overview/assets/default-design.png)

In deze afbeelding ziet u een aangepast ontwerp:

![&#x200B; Het ontwerp van de Douane &#x200B;](/help/main/c-recommendations/c-design-overview/assets/custom-design.png)

U kunt een ontwerp maken tijdens het proces voor het maken van activiteiten vanuit [!UICONTROL Visual Experience Composer] (VEC) of vanuit de ontwerpbibliotheek buiten het maken van activiteiten. In de volgende secties wordt aangenomen dat u ontwerpen maakt vanuit de bibliotheek, maar dat de stappen op elkaar lijken.

## Ontwerpen maken

U kunt een ontwerp tot stand brengen dat op een standaardontwerp wordt gebaseerd of u kunt een douaneontwerp tot stand brengen.

### Een ontwerp maken op basis van een standaardontwerp

1. Klik op **[!UICONTROL Recommendations]** > **[!UICONTROL Designs]** om de [!UICONTROL Designs] -bibliotheek weer te geven.


1. Klik het Meer pictogram van Acties ( ![&#x200B; Meer pictogram van Acties &#x200B;](/help/main/assets/icons/MoreSmallList.svg)) voor het ontwerp u wilt tot stand brengen, dan klik **[!UICONTROL Copy]**.

   Het dialoogvenster [!UICONTROL Create Design] wordt weergegeven.

1. Typ een **[!UICONTROL &#x200B; Name]** en een optionele voorvertoningsafbeelding die op de ontwerpkaart moeten worden weergegeven.

   Wanneer u een standaardontwerp gebruikt, worden de ontwerpnaam en de optie Kopiëren weergegeven in het veld **[!UICONTROL Content Name]** . U kunt de naam bewerken. U kunt ook een afbeelding selecteren die u op de ontwerpkaart wilt weergeven.

1. (Voorwaardelijk) Bewerk het ontwerp **[!UICONTROL Code]** naar wens.

   De ontwerpen van de aanbeveling gebruiken de open-source ontwerptaal van de Snelheid. De informatie over Snelheid kan in [&#x200B; https://velocity.apache.org &#x200B;](https://velocity.apache.org) worden gevonden en in [&#x200B; past een ontwerp aan gebruikend Snelheid &#x200B;](/help/main/c-recommendations/c-design-overview/customizing-a-template.md).

   Een ontwerp kan HTML of niet-HTML zijn. HTML-ontwerpen worden standaard voorzien van een tag `<div>` , zodat muisklik kan worden gevolgd in een webomgeving. Niet-HTML-ontwerpen zijn bedoeld voor omgevingen die geen webomgeving zijn waar klik-tracking niet mogelijk is. Sleep de schakeloptie [!UICONTROL HTML Design] naar de uitstand om niet-HTML-code te gebruiken.

   >[!NOTE]
   >
   >Het maximumaantal entiteiten waarnaar in een ontwerp kan worden verwezen, hard-gecodeerd of via lussen, is 99.

1. Klik op **[!UICONTROL Create]**.

### Een aangepast ontwerp maken

1. Klik op **[!UICONTROL Recommendations]** > **[!UICONTROL Designs]** om de [!UICONTROL Designs] -bibliotheek weer te geven.

1. Klik op **[!UICONTROL Create Design]**.

   Als u uw nieuw douaneontwerp op een bestaand ontwerp wilt baseren, klik het [!UICONTROL More Actions] pictogram ( ![&#x200B; Meer pictogram van Acties &#x200B;](/help/main/assets/icons/MoreSmallList.svg) ) voor het ontwerp u wilt creëren, dan klik [!UICONTROL Copy]. U kunt de kopie vervolgens bewerken om een nieuw aangepast ontwerp te maken.

1. Voeg een **[!UICONTROL Name]** en een optionele voorvertoningsafbeelding toe.

1. (Voorwaardelijk) Bewerk het ontwerp **[!UICONTROL Code]** naar wens.

   Raadpleeg de informatie in stap 4 voor meer informatie.

1. Klik op **[!UICONTROL Create]**.

## Een ontwerp bewerken, kopiëren of verwijderen

U kunt een standaardontwerp niet bewerken of kopiëren. U kunt alleen standaardontwerpen kopiëren.

Klik het [!UICONTROL More Actions] pictogram ( ![&#x200B; Meer pictogram van Acties &#x200B;](/help/main/assets/icons/MoreSmallList.svg)) voor het ontwerp u wilt uitgeven of schrappen, dan het aangewezen pictogram klikken: [!UICONTROL Edit], [!UICONTROL Copy], of [!UICONTROL Delete].

U kunt een bestaand ontwerp kopiëren om een dubbel ontwerp tot stand te brengen dat u dan kunt wijzigen. Met dit proces kunt u een vergelijkbaar ontwerp maken met minder moeite.

Houd er rekening mee dat ontwerpen beschikbaar zijn voor de gehele account. Zorg ervoor dat u rekening houdt met het gebruik in verschillende accounts voordat u een ontwerp verwijdert. Verwijderde ontwerpen kunnen niet worden hersteld.

## JSON-voorbeeld {#section_75BFB2537CFF4FBD9B560F59EB32C8DD}

Het volgende voorbeeld toont hoe de reacties JSON kunnen zijn teruggekeerd wanneer het vormen van een activiteit via de [&#x200B; vorm-gebaseerde redacteur &#x200B;](/help/main/c-experiences/form-experience-composer.md).

1. Maak een ontwerp vanuit [!UICONTROL Design library] of vanuit de formuliergebaseerde workflow. Als u een ontwerp probeert te maken in de [!UICONTROL Visual Experience Composer] (VEC)-workflow, kunt u alleen een HTML-ontwerp maken dat in een `<div>` is opgenomen voor kliktraceringsdoeleinden.

1. Zorg ervoor dat de optie &quot;HTML Design&quot; is uitgeschakeld:

   ![&#x200B; html_design_toggle beeld &#x200B;](assets/html_design_toggle.png)

1. De volgende code is een voorbeeld van wat u in uw ontwerp kunt plakken:

   ```javascript
       #* 
       * "Return a simple list of recommended entity ids"   
       *#
   
       {   
         "notes":{   
         "purpose": "Return a simple list of recommended entity ids",   
         "use-case": "Use this approach if you prefer to do a real-time lookup of entity attribute details (such as inventory, price, rating) from another system (such as a CMS, PIM or ecommerce platform)",   
         "version": "01"   
         },   
         "recommendedItems": {   
           "key": "$key.id",   
           "slot-01": "$entity1.id",   
           "slot-02": "$entity2.id",   
           "slot-03": "$entity3.id",   
           "slot-04": "$entity4.id",   
           "slot-05": "$entity5.id",   
           "slot-06": "$entity6.id",   
           "slot-07": "$entity7.id",   
           "slot-08": "$entity8.id",   
           "slot-09": "$entity9.id",   
           "slot-10": "$entity10.id"   
         }   
       }  
   ```

1. Stel een op formulieren gebaseerde [!DNL Recommendations] activiteit in die dit ontwerp gebruikt.

   1. Navigeer naar de pagina **[!UICONTROL Activities]** .
   1. Klik op **[!UICONTROL Create Activity]** > **[!UICONTROL Recommendations]** .
   1. Selecteer onder **[!UICONTROL Choose Experience Composer]** de optie **[!UICONTROL Form]** en klik vervolgens op **[!UICONTROL Next]** .
   1. Voer onder locatie de tekst in: &quot;Sample_Recs_Response&quot;
   1. Klik onder **[!UICONTROL Default Content]** op de pijl-omlaag en klik vervolgens op **[!UICONTROL Add Recommendation]** .
   1. Kies een paginatype. Hiermee bepaalt u de eerste filtering van het volgende scherm.
   1. Selecteer een Criteria-kaart en klik op **[!UICONTROL Next]** .
   1. Selecteer het ontwerp dat u in de vorige stap hebt gemaakt en klik op **[!UICONTROL Next]** .
   1. Voltooi het installatieproces.
   1. Klik op de pijl-rechts naast **[!UICONTROL Inactive]** en selecteer vervolgens **[!UICONTROL Activate]** .

1. Nadat uw activiteit opstelling en geactiveerd is, kunt u opstelling een steekproefverzoek om de schone reactie JSON terug te krijgen.

   Vanaf het moment dat u uw activiteit opslaat, moet [!DNL Target] een model maken ter ondersteuning van de geselecteerde configuratie met criteria. Afhankelijk van een aantal factoren kan dit proces enige tijd duren. De resultaten worden weergegeven zodra het model is opgebouwd.

   Bijvoorbeeld:

   ```
   https://[YOUR_CLIENT_CODE].tt.omtrdc.net/m2/YOUR_CLIENT_CODE/ubox/raw?mbox=[YOUR_MBOX_NAME]&mboxContentType=text/html&mboxXDomain=disabled&entity.id=[ENTITY_ID]&mboxHost=rawbox_sample&at_property=[AT_PROPERTY_TOKEN]&mboxNoRedirect=true&mboxPC=1234-4321&mboxSession=9876-7000
   ```

   waar

   | Parameter | Waarde |
   |--- |--- |
   | `[YOUR_CLIENT_CODE]` | Doelclientcode (beschikbaar op /help/target/products.html#recsSettings > Recommendations API Token > Client Code). |
   | `[YOUR_MBOX_NAME]` | De naam die u hebt geselecteerd in de sectie &quot;locaties&quot; van de op formulieren gebaseerde aanbevelingen, in dit geval Sample_Recs_Response. |
   | `[ENTITY_ID` | De `entity.id` van een item in uw catalogus. |
   | `[AT_PROPERTY_TOKEN]` | (Optioneel) Voeg toe als u een eigenschap (onderdeel van Enterprise-machtigingen) hebt geselecteerd tijdens het instellen van de activiteit. |

Nadat het algoritme is uitgevoerd en u resultaten hebt, moet uw reactie er ongeveer als volgt uitzien:

![&#x200B; json_recommended beeld &#x200B;](assets/json_recommendation.png){width="575px"}

## Extra tips en trucs voor JSON-objecten {#section_C305673C68944749969DB239E3221DC2}

U kunt ook een eenvoudige lijst met door komma&#39;s gescheiden items terugsturen door een ontwerp in te stellen met de volgende syntaxis:

```
entity1.id, $entity2.id, $entity3.id, $entity4.id, $entity5.id, 
```

U kunt ook aanvullende informatie in de reactie verzenden. Het volgende codedossier is een complexer voorbeeld dat veel meer dan entiteitsidentiteitskaart met hun bijbehorende groeven (orde) terugkeert. In dit ontwerpvoorbeeld worden ook de activiteitsgegevens, [!UICONTROL Target Profile] details (zoals van toepassing) en andere `entity.attributes` die aan de geretourneerde items zijn gekoppeld, geretourneerd.

```javascript
    {   
     "adobeRecommendations": {   
      "notes": {   
       "purpose": "Return a list of entity ids with their associated entity.attributes",   
       "use-case": "Use this approach to avoid looking up attribute details after receiving a response from Target",   
       "version": "01"   
      },   
      "recommendedItems": {   
       "slot-01": "$entity1.id",   
       "slot-02": "$entity2.id",   
       "slot-03": "$entity3.id",   
       "slot-04": "$entity4.id",   
       "slot-05": "$entity5.id",   
       "slot-06": "$entity6.id",   
       "slot-07": "$entity7.id",   
       "slot-08": "$entity8.id",   
       "slot-09": "$entity9.id",   
       "slot-10": "$entity10.id"   
      },   
      "activityDetails": {   
       "mbox.name": "email-mbox",   
       "campaign.name": "\${campaign.name}",   
       "campaign.id": "\${campaign.id}",   
       "campaign.recipe.name": "\${campaign.recipe.name}",   
       "campaign.recipe.id": "\${campaign.recipe.id}",   
       "offer.name": "\${offer.name}",   
       "offer.id": "\${offer.id}",   
       "criteria.title": "$criteria.title",   
       "algorithm.name": "$algorithm.name",   
       "algorithm.dayCount": "$algorithm.dayCount"   
      },   
      "visitorProfile": {   
       "profile.favorite-category": "\${profile.favorite-category}",   
       "profile.test": "\${profile.test}",   
       "user.endpoint.lastPurchasedEntity": "\${user.endpoint.lastPurchasedEntity}",   
       "user.endpoint.lastViewedEntity": "\${user.endpoint.lastViewedEntity}",   
       "user.endpoint.mostViewedEntity": "\${user.endpoint.mostViewedEntity}",   
       "user.endpoint.categoryAffinity": "\${user.endpoint.categoryAffinity}",   
       "profile.geolocation.city": "\${profile.geolocation.city}",   
       "profile.geolocation.dma": "\${profile.geolocation.dma}",   
       "profile.geolocation.state": "\${profile.geolocation.state}",   
       "profile.geolocation.country": "\${profile.geolocation.country}",   
       "profile.sessionCount": "\${profile.sessionCount}",   
       "profile.averageDaysBetweenVisits": "\${profile.averageDaysBetweenVisits}",   
       "profile.browserTime": "\${profile.browserTime}",   
       "user.activeActivities": "\${user.activeActivities}",   
       "user.pcId": "\${user.pcId}",   
       "user.isFirstSession": "\${user.isFirstSession}",   
       "user.isNewSession": "\${user.isNewSession}",   
       "user.header": "\${user.header}",   
       "user.parameter": "\${user.parameter}"   
      },   
      "recKey": {   
       "recKeyDetails": {   
        "id": "$key.id",   
        "name": "$key.name",   
        "category": "$key.category",   
        "pageUrl": "$key.pageUrl",   
        "thumbnailUrl": "$key.thumbnailUrl"   
       }   
      },   
      "recDetailedResults": {   
       "recEntity1Details": {   
        "id": "$entity1.id",   
        "name": "$entity1.name",   
        "category": "$entity1.category",   
        "pageUrl": "$entity1.pageUrl",   
        "thumbnailUrl": "$entity1.thumbnailUrl"   
       },   
       "recEntity2Details": {   
        "id": "$entity2.id",   
        "name": "$entity2.name",   
        "category": "$entity2.category",   
        "pageUrl": "$entity2.pageUrl",   
        "thumbnailUrl": "$entity2.thumbnailUrl"   
       },   
       "recEntity3Details": {   
        "id": "$entity3.id",   
        "name": "$entity3.name",   
        "category": "$entity3.category",   
        "pageUrl": "$entity3.pageUrl",   
        "thumbnailUrl": "$entity3.thumbnailUrl"   
       },   
       "recEntity4Details": {   
        "id": "$entity4.id",   
        "name": "$entity4.name",   
        "category": "$entity4.category",   
        "pageUrl": "$entity4.pageUrl",   
        "thumbnailUrl": "$entity4.thumbnailUrl"   
       },   
       "recEntity5Details": {   
        "id": "$entity5.id",   
        "name": "$entity5.name",   
        "category": "$entity5.category",   
        "pageUrl": "$entity5.pageUrl",   
        "thumbnailUrl": "$entity5.thumbnailUrl"   
       },   
       "recEntity6Details": {   
        "id": "$entity6.id",   
        "name": "$entity6.name",   
        "category": "$entity6.category",   
        "pageUrl": "$entity6.pageUrl",   
        "thumbnailUrl": "$entity6.thumbnailUrl"   
       },   
       "recEntity7Details": {   
        "id": "$entity7.id",   
        "name": "$entity7.name",   
        "category": "$entity7.category",   
        "pageUrl": "$entity7.pageUrl",   
        "thumbnailUrl": "$entity7.thumbnailUrl"   
       },   
       "recEntity8Details": {   
        "id": "$entity8.id",   
        "name": "$entity8.name",   
        "category": "$entity8.category",   
        "pageUrl": "$entity8.pageUrl",   
        "thumbnailUrl": "$entity8.thumbnailUrl"   
       },   
       "recEntity9Details": {   
        "id": "$entity9.id",   
        "name": "$entity9.name",   
        "category": "$entity9.category",   
        "pageUrl": "$entity9.pageUrl",   
        "thumbnailUrl": "$entity9.thumbnailUrl"   
       },   
       "recEntity10Details": {   
        "id": "$entity10.id",   
        "name": "$entity10.name",   
        "category": "$entity10.category",   
        "pageUrl": "$entity10.pageUrl",   
        "thumbnailUrl": "$entity10.thumbnailUrl"   
       }   
      }   
     }   
    }  
```

## De video van de opleiding: Creeer douaneontwerpen in Aanbevelingen (3 :20) ![&#x200B; de badge van het Overzicht &#x200B;](/help/main/assets/overview.png)

Deze video bevat de volgende informatie:

* Een aangepast ontwerp maken
* Begrijp hoe u in uw ontwerpen naar weergavevariabelen kunt verwijzen

>[!VIDEO](https://video.tv.adobe.com/v/27687)
