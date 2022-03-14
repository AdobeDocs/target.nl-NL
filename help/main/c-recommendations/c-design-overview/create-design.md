---
keywords: aanbevelingen ontwerp;ontwerp maken;ontwerp kopiëren
description: Leer hoe u een Adobe maakt [!DNL Target] Recommendations-ontwerp met een standaardontwerp of door een aangepast ontwerp te maken dat het beste aansluit bij de lay-out van uw pagina.
title: Hoe maak ik een ontwerp in Recommendations?
feature: Recommendations
exl-id: 0f10ee9d-7210-4e02-9342-e4f85cf46e8c
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '971'
ht-degree: 0%

---

# ![PREMIUM](/help/main/assets/premium.png) Een ontwerp maken

Een ontwerp bepaalt hoe de aanbevelingen op een pagina verschijnen.

U kunt een [!UICONTROL Recommendations] ontwerpen met een standaardontwerp of door een aangepast ontwerp te maken. De **[!UICONTROL Recommendations > Designs]** worden zowel standaardontwerpkaarten als ontwerpen weergegeven die in uw account zijn gemaakt.

Houd rekening met de volgende informatie wanneer u met ontwerpen werkt:

* U kunt een ontwerp met aanbevelingen maken door een standaardontwerp te gebruiken of u kunt een aangepast ontwerp maken.
* U kunt een standaardontwerp niet bewerken of verwijderen.
* U kunt een aangepast ontwerp bewerken, kopiëren of verwijderen.
* Als u een ontwerp wilt maken dat is gebaseerd op een standaardontwerp, moet u eerst het ontwerp kopiëren en vervolgens de kopie bewerken.

Deze illustratie toont het standaard 1 x 4 ontwerp:

![1 x 4 standaardontwerp](/help/main/c-recommendations/c-design-overview/assets/default-design.png)

In deze afbeelding ziet u een aangepast ontwerp:

![Aangepast ontwerp](/help/main/c-recommendations/c-design-overview/assets/custom-design.png)

U kunt een ontwerp tijdens het activiteit-creatie proces van binnen Visuele Composer van de Ervaring (VEC) of van de ontwerpbibliotheek buiten de activiteitenverwezenlijking tot stand brengen. In de volgende secties wordt aangenomen dat u ontwerpen maakt vanuit de bibliotheek, maar dat de stappen op elkaar lijken.

## Ontwerpen maken

U kunt een ontwerp tot stand brengen dat op een standaardontwerp wordt gebaseerd of u kunt een douaneontwerp tot stand brengen.

### Een ontwerp maken op basis van een standaardontwerp

1. Klikken **[!UICONTROL Recommendations]** > **[!UICONTROL Designs]** om de [!UICONTROL Designs] bibliotheek.

   ![Ontwerpbibliotheek](/help/main/c-recommendations/c-design-overview/assets/design-library.png)

1. Plaats de muis boven de kaart voor het ontwerp dat u wilt maken en klik vervolgens op de knop **[!UICONTROL Copy]** pictogram.

   ![](assets/Card_CopyDesign.png)

   De [!UICONTROL Create Design] wordt weergegeven.

   ![](assets/createDesign.png)

1. In de **[!UICONTROL Information]** deelvenster, een **[!UICONTROL Content Name]** en optionele voorvertoningsafbeelding die op de ontwerpkaart wordt weergegeven.

   Wanneer u een standaardontwerp gebruikt, worden de ontwerpnaam en de optie Kopiëren weergegeven in het dialoogvenster **[!UICONTROL Content Name]** veld. U kunt de naam bewerken. U kunt ook een afbeelding selecteren die u op de ontwerpkaart wilt weergeven.

1. (Voorwaardelijk) Bewerk het ontwerp **[!UICONTROL Code]**, naar wens.

   De ontwerpen van de aanbeveling gebruiken de open-source ontwerptaal van de Snelheid. Informatie over snelheid vindt u op [https://velocity.apache.org](https://velocity.apache.org) en in [Een ontwerp aanpassen met Snelheid](/help/main/c-recommendations/c-design-overview/customizing-a-template.md).

   Een ontwerp kan HTML of niet-HTML zijn. Standaard worden HTML-ontwerpen omwikkeld met een `<div>` tag om klikken en bijhouden toe te staan in een webomgeving. Niet-HTML-ontwerpen zijn bedoeld voor omgevingen die geen webomgeving zijn en waar het bijhouden van klikken niet mogelijk is. Schuif de [!UICONTROL HTML Design] Schakel over naar de uitstand om niet-HTML code te gebruiken.

   >[!NOTE]
   >
   >Het maximumaantal entiteiten waarnaar in een ontwerp kan worden verwezen, hard-gecodeerd of via lussen, is 99.

1. Klik op **[!UICONTROL Save]**.

### Een aangepast ontwerp maken

1. Klikken **[!UICONTROL Recommendations]** > **[!UICONTROL Designs]** om de [!UICONTROL Designs] bibliotheek.

1. Klik op **[!UICONTROL Create Design]**.

   Als u het nieuwe aangepaste ontwerp wilt baseren op een bestaand ontwerp, plaatst u de muis boven het gewenste ontwerp en klikt u op de knop [!UICONTROL Copy] pictogram. U kunt de kopie vervolgens bewerken om een nieuw aangepast ontwerp te maken.

1. Voeg een **[!UICONTROL Content Name]** en optionele voorvertoning.

1. (Voorwaardelijk) Bewerk het ontwerp **[!UICONTROL Code]**, naar wens.

   Raadpleeg de informatie in stap 4 voor meer informatie.

1. Klik op **[!UICONTROL Save]**.

## Een ontwerp bewerken, kopiëren of verwijderen

Het is niet mogelijk een standaardontwerp te bewerken of te kopiëren. u kunt alleen standaardontwerpen kopiëren.

Houd de muisaanwijzer boven het gewenste ontwerp in de [!UICONTROL Design] en klik vervolgens op het juiste pictogram: bewerken, kopiëren of verwijderen.

![Pictogrammen voor aanwijzen van een ontwerp](/help/main/c-recommendations/c-design-overview/assets/hover-icons-design.png)

U kunt een bestaand ontwerp kopiëren om een dubbel ontwerp tot stand te brengen dat u dan kunt wijzigen. Zo kunt u een vergelijkbaar ontwerp maken met minder moeite.

Houd er rekening mee dat ontwerpen beschikbaar zijn voor de gehele account. Zorg ervoor dat u hiermee rekening houdt voordat u een ontwerp verwijdert. Verwijderde ontwerpen kunnen niet worden hersteld.

## JSON-voorbeeld {#section_75BFB2537CFF4FBD9B560F59EB32C8DD}

In het volgende voorbeeld ziet u hoe JSON-reacties kunnen worden geretourneerd wanneer een activiteit wordt geconfigureerd via de formuliereditor.

1. Maak een ontwerp vanuit de ontwerpbibliotheek of vanuit de formuliergebaseerde workflow. Als u dit binnen het Visueel Composer van de Ervaring (VEC) werkschema probeert te doen kunt u om het even wat buiten een ontwerp van HTML tot stand brengen, dat in een `<div>` voor trackingdoeleinden.

1. Zorg ervoor dat de optie &quot;HTML-ontwerp&quot; is uitgeschakeld:

   ![](assets/html_design_toggle.png)

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

1. Een formuliergebaseerd instellen [!DNL Recommendations] activiteit die dit ontwerp gebruikt.

   1. Ga naar de **[!UICONTROL Activities]** pagina.
   1. Klik op **[!UICONTROL Create Activity]** > **[!UICONTROL Recommendations]**.
   1. Onder **[!UICONTROL Choose Experience Composer]**, selecteert u **[!UICONTROL Form]** en klik vervolgens op **[!UICONTROL Next]**.
   1. Voer de tekst in onder Locatie: &quot;Sample_Recs_Response&quot;
   1. Onder **[!UICONTROL Default Content]** klikt u op de pijl omlaag en vervolgens klikt u op **[!UICONTROL Add Recommendation]**.
   1. Kies een paginatype. Hiermee bepaalt u de eerste filtering van het volgende scherm.
   1. Selecteer een Criteria-kaart en klik vervolgens op **[!UICONTROL Next]**.
   1. Selecteer het ontwerp dat u in de vorige stap hebt gemaakt en klik op **[!UICONTROL Next]**.
   1. Voltooi het installatieproces.
   1. Klik op de pijl-rechts naast **[!UICONTROL Inactive]** selecteert u vervolgens **[!UICONTROL Activate]**.

1. Nadat uw activiteit opstelling en geactiveerd is, kunt u opstelling een steekproefverzoek om de schone reactie JSON terug te krijgen.

   Vanaf het moment dat u uw activiteit opslaat, [!DNL Target] moet een model bouwen ter ondersteuning van de configuratie van de geselecteerde criteria. Afhankelijk van een aantal factoren kan dit enige tijd duren. De resultaten worden weergegeven zodra het model is opgebouwd.

   Bijvoorbeeld:

   ```
   https://[YOUR_CLIENT_CODE].tt.omtrdc.net/m2/YOUR_CLIENT_CODE/ubox/raw?mbox=[YOUR_MBOX_NAME]&mboxContentType=text/html&mboxXDomain=disabled&entity.id=[ENTITY_ID]&mboxHost=rawbox_sample&at_property=[AT_PROPERTY_TOKEN]&mboxNoRedirect=true&mboxPC=1234-4321&mboxSession=9876-7000
   ```

   waar

   | Parameter | Waarde |
   |--- |--- |
   | `[YOUR_CLIENT_CODE]` | Doelclientcode (beschikbaar op /help/target/products.html#recsSettings > Recommendations API Token > Clientcode. |
   | `[YOUR_MBOX_NAME]` | De naam die u hebt geselecteerd in de sectie &quot;locations&quot; van de op formulieren gebaseerde Recommendations, in dit geval Sample_Recs_Response. |
   | `[ENTITY_ID` | De `entity.id` van een item in uw catalogus. |
   | `[AT_PROPERTY_TOKEN]` | (Optioneel) Voeg toe als u een eigenschap (onderdeel van Enterprise-machtigingen) hebt geselecteerd tijdens het instellen van de activiteit. |

Nadat het algoritme is uitgevoerd en u resultaten hebt, moet uw reactie er ongeveer als volgt uitzien:

![](assets/json_recommendation.png){width=&quot;575px&quot;}

## Extra tips en trucs voor JSON-objecten {#section_C305673C68944749969DB239E3221DC2}

U kunt ook gewoon een eenvoudige door komma&#39;s gescheiden lijst met items terugsturen door een ontwerp in te stellen met de volgende syntaxis:

```
entity1.id, $entity2.id, $entity3.id, $entity4.id, $entity5.id, 
```

U kunt ook aanvullende informatie in de reactie verzenden. Het volgende codedossier is een complexer voorbeeld dat veel meer dan entiteitsidentiteitskaart met hun bijbehorende groeven (orde) terugkeert. In dit ontwerpvoorbeeld worden ook activiteitsdetails, details van het doelprofiel (zoals van toepassing) en andere gegevens geretourneerd `entity.attributes` gekoppeld aan de geretourneerde items.

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

## Trainingsvideo: Aangepaste ontwerpen maken in Recommendations (3:20) ![Overzicht badge](/help/main/assets/overview.png)

Deze video bevat de volgende informatie:

* Een aangepast ontwerp maken
* Begrijp hoe u in uw ontwerpen naar weergavevariabelen kunt verwijzen

>[!VIDEO](https://video.tv.adobe.com/v/27687)
