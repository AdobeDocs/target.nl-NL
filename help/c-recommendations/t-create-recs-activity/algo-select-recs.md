---
keywords: recommendations;recommendations activity;criteria;algorithm
description: Selecteer de criteria die je wilt gebruiken in je Adobe Target Recommendations-activiteit.
title: Criteria selecteren
feature: recs creation
translation-type: tm+mt
source-git-commit: 968d36d65016e51290f6bf754f69c91fd8f68405
workflow-type: tm+mt
source-wordcount: '361'
ht-degree: 0%

---


# ![PREMIUM](/help/assets/premium.png) -selectiecriteria{#select-criteria}

Selecteer de [criteria](/help/c-recommendations/c-algorithms/algorithms.md) die u in uw [!DNL Adobe Target Recommendations] activiteit wilt gebruiken. Criteria zijn regels die bepalen welke producten moeten worden aanbevolen op basis van een vooraf bepaalde reeks gedragingen van bezoekers.

U kunt veelvoudige aanbevelingstypes tegen elkaar testen door meer dan één criteria toe te voegen.

Als u meerdere criteria selecteert, wordt het verkeer gelijkmatig over de geselecteerde criteria verdeeld. Als u bijvoorbeeld twee criteria hebt geselecteerd en uw activiteit is ontworpen om standaardinhoud weer te geven voor 20% van de deelnemers aan de activiteit, dan zal 40% van de deelnemers aan de activiteit de aanbevelingen zien die door elke criteria worden gecontroleerd. Er is geen optie om de percentages voor elke criteria te wijzigen.

* Als u naar bestaande criteria wilt zoeken (bijvoorbeeld als er veel kaarten met criteria worden weergegeven), typt u in het zoekveld totdat de gewenste criteria worden weergegeven, selecteert u de criteria en klikt u **[!UICONTROL Done]**.

   Er worden enkele criteria verstrekt [!DNL Recommendations]. U en uw team kunnen ook uw eigen aangepaste criteria maken.

* Als u nieuwe criteria wilt maken, klikt u op **[!UICONTROL Create Criteria]** > **[!UICONTROL Create Criteria]** en vult u de gegevens voor de nieuwe criteria in. Zie [Nieuwe criteria](/help/c-recommendations/c-algorithms/create-new-algorithm.md#task_8A9CB465F28D44899F69F38AD27352FE)maken voor meer informatie over het maken van nieuwe criteria.

**Criteria selecteren:**

1. Zoek en selecteer een of meer criteria tijdens het [maken van een nieuwe aanbeveling](/help/c-recommendations/t-create-recs-activity/create-recs-activity.md#task_6874328773C64C44A73F0A130AD3F96F)in het **[!UICONTROL Select Criteria]** dialoogvenster.

   ![Selectiecriteria, dialoogvenster](/help/c-recommendations/t-create-recs-activity/assets/filters.png)

   U kunt het [!UICONTROL Industry Type] filter, het [!UICONTROL Page Type] filter, en het [!UICONTROL Compatible] controlevakje gebruiken om de lijst van criteria te filtreren. Met deze opties kunt u de gewenste criteria vinden.

   * **Type industrie:** Het industrietype wordt gebruikt om te helpen [!DNL Recommendations] criteria categoriseren. Als u de standaard verticale instellingen wilt wijzigen, klikt u op **[!UICONTROL Recommendations]** > **[!UICONTROL Settings]** en selecteert u de gewenste standaardinstelling **[!UICONTROL Industry Vertical]** .
   * **Paginatype:** Met het paginatype kunt u uw aanbevelingen indelen. Er zijn ook ingebouwde criteria die voor elk paginatype kunnen worden gekozen.
   * **Compatibel met:** Alleen die criteria weergeven waarbij de geselecteerde pagina de vereiste gegevens doorgeeft. Niet alle criteria worden op elke pagina correct uitgevoerd. De pagina of het kader moet worden doorgegeven `entity.id` `entity.categoryId` of de huidige aanbevelingen voor het item of de huidige categorie moeten compatibel zijn. Over het algemeen is het beter alleen compatibele criteria te laten zien. Als u echter incompatibele criteria voor de activiteit wilt gebruiken, schakelt u het **[!UICONTROL Compatible]** selectievakje uit. Deze optie kan in uw montages worden onbruikbaar gemaakt of worden toegelaten: **[!UICONTROL Recommendations]** > **[!UICONTROL Settings]**.

1. Klik **[!UICONTROL Next]** om het dialoogvenster [Ontwerp](/help/c-recommendations/c-design-overview/design-overview.md) selecteren weer te geven.
