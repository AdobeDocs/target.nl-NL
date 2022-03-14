---
keywords: recommendations;recommendations activity;criteria;algorithm
description: Leer hoe u de criteria (regels die bepalen welke producten of inhoud moet worden aanbevolen) voor gebruik in uw Adobe selecteert [!DNL Target] Recommendations-activiteit.
title: Hoe selecteer ik criteria voor een Recommendations-activiteit?
feature: Recommendations
exl-id: 119227ec-88c3-4de9-b2cf-f7d5fa2e98f6
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '384'
ht-degree: 0%

---

# ![PREMIUM](/help/main/assets/premium.png) Criteria selecteren

Selecteer [criteria](/help/main/c-recommendations/c-algorithms/algorithms.md) om te gebruiken in uw [!DNL Adobe Target Recommendations] activiteit. Criteria zijn regels die bepalen welke producten moeten worden aanbevolen op basis van een vooraf bepaalde reeks gedragingen van bezoekers.

You can test multiple recommendation types against each other by adding more than one criteria.

Als u meerdere criteria selecteert, wordt het verkeer gelijkmatig over de geselecteerde criteria verdeeld. Als u bijvoorbeeld twee criteria hebt geselecteerd en uw activiteit is ontworpen om standaardinhoud weer te geven voor 20% van de deelnemers aan de activiteit, dan zal 40% van de deelnemers aan de activiteit de aanbevelingen zien die door elke criteria worden gecontroleerd. Er is geen optie om de percentages voor elke criteria te wijzigen.

* To search for an existing criteria (for example, if many criteria cards display), type in the search field until the desired criteria appears, then select the criteria and click **[!UICONTROL Done]**.

   Sommige criteria worden verstrekt [!DNL Recommendations]. U en uw team kunnen ook uw eigen aangepaste criteria maken.

* Als u nieuwe criteria wilt maken, klikt u op **[!UICONTROL Create Criteria]** > **[!UICONTROL Create Criteria]** en vult vervolgens de informatie voor de nieuwe criteria in. Voor informatie over het creëren van nieuwe criteria, zie [Nieuwe criteria maken](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md#task_8A9CB465F28D44899F69F38AD27352FE).

**Criteria selecteren:**

1. while [nieuwe aanbeveling](/help/main/c-recommendations/t-create-recs-activity/create-recs-activity.md#task_6874328773C64C44A73F0A130AD3F96F)in de **[!UICONTROL Select Criteria]** een of meer criteria zoeken en selecteren.

   ![Select Criteria dialog box](/help/main/c-recommendations/t-create-recs-activity/assets/filters.png)

   You can use the [!UICONTROL Industry Type] filter, [!UICONTROL Page Type] filter, and [!UICONTROL Compatible] checkbox to filter the list of criteria. These options help you locate the desired criteria.

   * **Industry Type:** The industry type is used to help categorize [!DNL Recommendations] criteria. Als u de standaardindustrie verticaal wilt wijzigen, klikt u op **[!UICONTROL Recommendations]** > **[!UICONTROL Settings]** en selecteer uw gewenste standaard **[!UICONTROL Industry Vertical]** instellen.
   * **Paginatype:** Met het paginatype kunt u uw aanbevelingen indelen. Er zijn ook ingebouwde criteria die voor elk paginatype kunnen worden gekozen.
   * **Compatible:** Show only those criteria where the selected page passes the required data. Niet alle criteria worden op elke pagina correct uitgevoerd. De pagina of het kader moet worden doorgegeven `entity.id` of `entity.categoryId` voor het huidige item/de huidige categorie-aanbevelingen compatibel te maken. In general, it is best to show only compatible criteria. Als u echter incompatibele criteria voor de activiteit wilt gebruiken, wist u de optie **[!UICONTROL Compatible]** selectievakje. Deze optie kan in uw montages worden onbruikbaar gemaakt of worden toegelaten: **[!UICONTROL Recommendations]** > **[!UICONTROL Settings]**.

1. Klikken **[!UICONTROL Next]** om de [Ontwerp selecteren](/help/main/c-recommendations/c-design-overview/design-overview.md) in.
