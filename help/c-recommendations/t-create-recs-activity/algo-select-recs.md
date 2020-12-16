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


# ![](/help/assets/premium.png) PREMIUMSelecteer criteria{#select-criteria}

Selecteer de [criteria](/help/c-recommendations/c-algorithms/algorithms.md) om in uw [!DNL Adobe Target Recommendations] activiteit te gebruiken. Criteria zijn regels die bepalen welke producten moeten worden aanbevolen op basis van een vooraf bepaalde reeks gedragingen van bezoekers.

U kunt veelvoudige aanbevelingstypes tegen elkaar testen door meer dan één criteria toe te voegen.

Als u meerdere criteria selecteert, wordt het verkeer gelijkmatig over de geselecteerde criteria verdeeld. Als u bijvoorbeeld twee criteria hebt geselecteerd en uw activiteit is ontworpen om standaardinhoud weer te geven voor 20% van de deelnemers aan de activiteit, dan zal 40% van de deelnemers aan de activiteit de aanbevelingen zien die door elke criteria worden gecontroleerd. Er is geen optie om de percentages voor elke criteria te wijzigen.

* Als u naar bestaande criteria wilt zoeken (bijvoorbeeld als er veel kaarten met criteria worden weergegeven), typt u in het zoekveld totdat de gewenste criteria worden weergegeven, selecteert u de criteria en klikt u op **[!UICONTROL Done]**.

   Bij [!DNL Recommendations] worden enkele criteria geleverd. U en uw team kunnen ook uw eigen aangepaste criteria maken.

* Als u nieuwe criteria wilt maken, klikt u op **[!UICONTROL Create Criteria]** > **[!UICONTROL Create Criteria]** en vult u vervolgens de gegevens voor de nieuwe criteria in. Zie [Nieuwe criteria maken](/help/c-recommendations/c-algorithms/create-new-algorithm.md#task_8A9CB465F28D44899F69F38AD27352FE) voor informatie over het maken van nieuwe criteria.

**Criteria selecteren:**

1. Zoek en selecteer een of meer criteria terwijl [een nieuwe aanbeveling](/help/c-recommendations/t-create-recs-activity/create-recs-activity.md#task_6874328773C64C44A73F0A130AD3F96F) maakt in het dialoogvenster **[!UICONTROL Select Criteria]**.

   ![Selectiecriteria, dialoogvenster](/help/c-recommendations/t-create-recs-activity/assets/filters.png)

   U kunt het filter [!UICONTROL Industry Type], het filter [!UICONTROL Page Type], en [!UICONTROL Compatible] checkbox gebruiken om de lijst van criteria te filtreren. Met deze opties kunt u de gewenste criteria vinden.

   * **Type bedrijfstak:** het industrietype wordt gebruikt helpen  [!DNL Recommendations] criteria categoriseren. Als u de standaard verticale instellingen wilt wijzigen, klikt u op **[!UICONTROL Recommendations]** > **[!UICONTROL Settings]** en selecteert u de gewenste standaardinstelling **[!UICONTROL Industry Vertical]**.
   * **Paginatype:** Met het paginatype kunt u uw aanbevelingen indelen. Er zijn ook ingebouwde criteria die voor elk paginatype kunnen worden gekozen.
   * **Compatibel:alleen de criteria** tonen waarbij de geselecteerde pagina de vereiste gegevens doorgeeft. Niet alle criteria worden op elke pagina correct uitgevoerd. De pagina of het kader moet `entity.id` of `entity.categoryId` voor de huidige punt/huidige categorieconflicten overgaan om compatibel te zijn. Over het algemeen is het beter alleen compatibele criteria te laten zien. Als u echter incompatibele criteria voor de activiteit beschikbaar wilt maken, schakelt u het selectievakje **[!UICONTROL Compatible]** uit. Deze optie kan in uw montages worden onbruikbaar gemaakt of worden toegelaten: **[!UICONTROL Recommendations]** > **[!UICONTROL Settings]**.

1. Klik **[!UICONTROL Next]** om [Select Design](/help/c-recommendations/c-design-overview/design-overview.md) dialoogdoos te tonen.
