---
keywords: recommendations design;create design;copy design
description: Een ontwerp bepaalt hoe de aanbevelingen op een pagina verschijnen.
title: Een ontwerp maken
feature: designs
uuid: 812258e0-8d28-4ef3-b745-45ed694fcabe
translation-type: tm+mt
source-git-commit: 3cf1f4fa56f86c106dccdc2c97c080c17c3982b4
workflow-type: tm+mt
source-wordcount: '613'
ht-degree: 1%

---


# ![PREMIUM](/help/assets/premium.png) Een ontwerp maken {#create-a-design}

Een ontwerp bepaalt hoe de aanbevelingen op een pagina verschijnen.

U kunt een [!UICONTROL Recommendations] ontwerp tot stand brengen gebruikend een standaardontwerp of door een douaneontwerp te creëren. In het **[!UICONTROL Recommendations > Designs]** scherm worden zowel de standaardontwerpkaarten als de ontwerpen weergegeven die u hebt gemaakt. De standaardontwerpen kunnen niet worden bewerkt of verwijderd.

1. Plaats de muisaanwijzer op het **[!UICONTROL Recommendations > Designs]** scherm op de kaart voor het ontwerp dat u wilt maken.

   ![](assets/Card_CopyDesign.png)

1. Als u een bestaand ontwerp wilt kopiëren en bewerken, klikt u op het **[!UICONTROL Copy]** pictogram.

   of

   Klik op het **[!UICONTROL Create Design]** **[!UICONTROL Recommendations > Designs]** scherm om een aangepast ontwerp te maken.

   ![](assets/createDesign.png)

1. Voeg een **[!UICONTROL Content Name]**.

   Wanneer u een standaardontwerp gebruikt, worden de ontwerpnaam en de optie Kopiëren in het **[!UICONTROL Content Name]** veld weergegeven. U kunt de naam bewerken. 1. (Optioneel) Klik om een afbeelding te selecteren die u op de ontwerpkaart wilt weergeven.
1. Bewerk het ontwerp **[!UICONTROL Code]**.

   De ontwerpen van de aanbeveling gebruiken de open-source ontwerptaal van de Snelheid. Informatie over snelheid vindt u op [https://velocity.apache.org](https://velocity.apache.org).

   Een ontwerp kan HTML of niet-HTML zijn. HTML-ontwerpen worden standaard voorzien van een <div> tag om klikken en bijhouden toe te staan in een webomgeving. Niet-HTML-ontwerpen zijn bedoeld voor omgevingen die geen webomgeving zijn waar klik-tracking niet mogelijk is.

   >[!NOTE]
   >
   >Het maximumaantal entiteiten waarnaar in een ontwerp kan worden verwezen, is 99, ofwel hardcoded ofwel via lussen.

1. Klik op **[!UICONTROL Save]**.

## JSON-voorbeeld {#section_75BFB2537CFF4FBD9B560F59EB32C8DD}

In het volgende voorbeeld ziet u hoe u JSON-reacties kunt retourneren tijdens het configureren van een activiteit via de formuliereditor.

1. Maak een ontwerp vanuit de ontwerpbibliotheek of vanuit de formuliergebaseerde workflow. Als u dit binnen de Visueel Composer van de Ervaring (VEC) werkschema probeert te doen kunt u geen ander dan een ontwerp van HTML tot stand brengen, dat in een `<div>` voor klikvolgende doeleinden verpakt is.
1. Zorg ervoor dat de optie &quot;HTML-ontwerp&quot; is uitgeschakeld:

   ![](assets/html_design_toggle.png)

1. De volgende code is een voorbeeld hieronder van wat u in uw ontwerp kunt plakken:

   ```
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

1. Stel een Recommendations-activiteit op basis van formulieren in die dit ontwerp gebruikt.

   1. Navigeer naar de pagina Activiteiten.
   1. Klik op **[!UICONTROL Create Activity]**.
   1. Selecteer **[!UICONTROL Recommendations]**.
   1. Selecteer onder **[!UICONTROL Choose Experience Composer]** de optie **[!UICONTROL Form]**.

   1. Voer de tekst in onder Locatie: &quot;Sample_Recs_Response&quot;
   1. Klik onder **[!UICONTROL Default Content]** op de pijl omlaag en klik vervolgens op **[!UICONTROL Add Recommendation]**.
   1. Kies een paginatype. Hiermee bepaalt u de eerste filtering van het volgende scherm.
   1. Selecteer een Criteria-kaart en klik op **[!UICONTROL Next]**.
   1. Selecteer het ontwerp dat u in de vorige stap hebt gemaakt en klik op **[!UICONTROL Save]**.
   1. Voltooi het installatieproces.
   1. Klik op de pijl-rechts naast **[!UICONTROL Inactive]** en selecteer **[!UICONTROL Activate]**.

1. Nadat uw activiteit opstelling en geactiveerd is, kunt u opstelling een steekproefverzoek om de schone reactie JSON terug te krijgen.

   Vanaf het moment dat u uw activiteit opslaat, zal het Doel een model moeten bouwen om de geselecteerde criteria configuratie te steunen. Afhankelijk van een aantal factoren kan dit enige tijd duren. De resultaten worden weergegeven zodra het model is opgebouwd.

   Bijvoorbeeld:

   ```
   https://[YOUR_CLIENT_CODE].tt.omtrdc.net/m2/YOUR_CLIENT_CODE/ubox/raw?mbox=[YOUR_MBOX_NAME]&mboxContentType=text/html&mboxXDomain=disabled&entity.id=[ENTITY_ID]&mboxHost=rawbox_sample&at_property=[AT_PROPERTY_TOKEN]&mboxNoRedirect=true&mboxPC=1234-4321&mboxSession=9876-7000
   ```

   waar

| Parameter | Waarde |
|--- |--- |
| `[YOUR_CLIENT_CODE]` | Doelclientcode (beschikbaar op ../target/products.html#recsSettings > Recommendations API Token > Clientcode. |
| `[YOUR_MBOX_NAME]` | De naam die u hebt geselecteerd in de sectie &quot;locations&quot; van de op formulieren gebaseerde Recommendations, in dit geval Sample_Recs_Response. |
| `[ENTITY_ID`] | De `entity.id` waarde van een item in uw catalogus. |
| `[AT_PROPERTY_TOKEN]` | (Optioneel) Voeg toe als u een eigenschap (onderdeel van Enterprise-machtigingen) hebt geselecteerd tijdens het instellen van de activiteit. |

Nadat het algoritme is uitgevoerd en u resultaten hebt, moet uw reactie er ongeveer als volgt uitzien:

![](assets/json_recommendation.png){width=&quot;575px&quot;}

## Extra tips en trucs voor JSON-objecten {#section_C305673C68944749969DB239E3221DC2}

U kunt ook gewoon een eenvoudige door komma&#39;s gescheiden lijst met items terugsturen door een ontwerp in te stellen met de volgende syntaxis:

```
entity1.id, $entity2.id, $entity3.id, $entity4.id, $entity5.id, 
```

U kunt ook aanvullende informatie in de reactie verzenden. Het volgende codedossier is een complexer voorbeeld dat veel meer dan entiteitsidentiteitskaart met hun bijbehorende groeven (orde) terugkeert. In dit ontwerpvoorbeeld worden ook de activiteitsdetails, de gegevens van het doelprofiel (zoals van toepassing) en andere gegevens `entity.attributes` die aan de geretourneerde items zijn gekoppeld, geretourneerd.

```
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

## Trainingsvideo: Aangepaste ontwerpen maken in Recommendations (3:20) - ![overzichtsbadge](/help/assets/overview.png)

Deze video bevat de volgende informatie:

* Een aangepast ontwerp maken
* Begrijp hoe u in uw ontwerpen naar weergavevariabelen kunt verwijzen

>[!VIDEO](https://video.tv.adobe.com/v/27687)
