---
keywords: aanbevelingen;aanbevelingen activiteit;criteria;algoritme
description: Leer hoe u de criteria (regels die bepalen welke producten of inhoud moet worden aanbevolen) voor gebruik in uw Adobe selecteert [!DNL Target] Recommendations-activiteit.
title: Hoe selecteer ik criteria voor een Recommendations-activiteit?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="See what's included in Target Premium."
feature: Recommendations
exl-id: 119227ec-88c3-4de9-b2cf-f7d5fa2e98f6
source-git-commit: bde5506033fbca1577fad1cda1af203702fc4bb3
workflow-type: tm+mt
source-wordcount: '383'
ht-degree: 0%

---

# Criteria selecteren

Selecteer [criteria](/help/main/c-recommendations/c-algorithms/algorithms.md) om te gebruiken in uw [!DNL Adobe Target Recommendations] activiteit. Criteria zijn regels die bepalen welke producten moeten worden aanbevolen op basis van een vooraf bepaalde reeks gedragingen van bezoekers.

U kunt veelvoudige aanbevelingstypes tegen elkaar testen door meer dan één criteria toe te voegen.

Als u meerdere criteria selecteert, wordt het verkeer gelijkmatig over de geselecteerde criteria verdeeld. Als u bijvoorbeeld twee criteria hebt geselecteerd en uw activiteit is ontworpen om standaardinhoud weer te geven voor 20% van de deelnemers aan de activiteit, dan zal 40% van de deelnemers aan de activiteit de aanbevelingen zien die door elke criteria worden gecontroleerd. Er is geen optie om de percentages voor elke criteria te wijzigen.

* Als u naar bestaande criteria wilt zoeken (bijvoorbeeld als er veel kaarten met criteria worden weergegeven), typt u in het zoekveld totdat de gewenste criteria worden weergegeven, selecteert u de criteria en klikt u op **[!UICONTROL Done]**.

   Sommige criteria worden verstrekt [!DNL Recommendations]. U en uw team kunnen ook uw eigen aangepaste criteria maken.

* Als u nieuwe criteria wilt maken, klikt u op **[!UICONTROL Create Criteria]** > **[!UICONTROL Create Criteria]** en vult vervolgens de informatie voor de nieuwe criteria in. Voor informatie over het creëren van nieuwe criteria, zie [Nieuwe criteria maken](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md#task_8A9CB465F28D44899F69F38AD27352FE).

**Criteria selecteren:**

1. while [nieuwe aanbeveling](/help/main/c-recommendations/t-create-recs-activity/create-recs-activity.md#task_6874328773C64C44A73F0A130AD3F96F)in de **[!UICONTROL Select Criteria]** een of meer criteria zoeken en selecteren.

   ![Selectiecriteria, dialoogvenster](/help/main/c-recommendations/t-create-recs-activity/assets/filters.png)

   U kunt de [!UICONTROL Industry Type] filter, [!UICONTROL Page Type] filter, en [!UICONTROL Compatible] Schakel het selectievakje in om de lijst met criteria te filteren. Met deze opties kunt u de gewenste criteria vinden.

   * **Type industrie:** Het industrietype wordt gebruikt om te helpen categoriseren [!DNL Recommendations] criteria. Als u de standaardindustrie verticaal wilt wijzigen, klikt u op **[!UICONTROL Recommendations]** > **[!UICONTROL Settings]** en selecteer uw gewenste standaard **[!UICONTROL Industry Vertical]** instellen.
   * **Paginatype:** Met het paginatype kunt u uw aanbevelingen indelen. Er zijn ook ingebouwde criteria die voor elk paginatype kunnen worden gekozen.
   * **Compatibel met:** Alleen die criteria weergeven waarbij de geselecteerde pagina de vereiste gegevens doorgeeft. Niet alle criteria worden op elke pagina correct uitgevoerd. De pagina of het kader moet worden doorgegeven `entity.id` of `entity.categoryId` voor het huidige item/de huidige categorie-aanbevelingen compatibel te maken. Over het algemeen is het beter alleen compatibele criteria te laten zien. Als u echter incompatibele criteria voor de activiteit wilt gebruiken, wist u de optie **[!UICONTROL Compatible]** selectievakje. Deze optie kan in uw montages worden onbruikbaar gemaakt of worden toegelaten: **[!UICONTROL Recommendations]** > **[!UICONTROL Settings]**.

1. Klikken **[!UICONTROL Next]** om de [Ontwerp selecteren](/help/main/c-recommendations/c-design-overview/design-overview.md) in.
