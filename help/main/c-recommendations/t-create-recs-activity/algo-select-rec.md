---
keywords: aanbevelingen;aanbevelingen activiteit;criteria;algoritme
description: Leer hoe te om de criteria (regels te selecteren die welke producten of inhoud om) bepalen te gebruiken in uw Adobe  [!DNL Target]  activiteit van Aanbevelingen.
title: Hoe selecteer ik Criteria voor een activiteit van Aanbevelingen?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=nl-NL#premium newtab=true" tooltip="Kijk wat er in Target Premium is opgenomen."
feature: Recommendations
exl-id: 119227ec-88c3-4de9-b2cf-f7d5fa2e98f6
source-git-commit: 02ffe8da6cdf96039218656b9690fa719a77910c
workflow-type: tm+mt
source-wordcount: '391'
ht-degree: 0%

---

# Criteria selecteren

Selecteer de [&#x200B; criteria &#x200B;](/help/main/c-recommendations/c-algorithms/algorithms.md) in uw [!DNL Adobe Target Recommendations] activiteit te gebruiken. Criteria zijn regels die bepalen welke producten moeten worden aanbevolen op basis van een vooraf bepaalde reeks gedragingen van bezoekers.

U kunt veelvoudige aanbevelingstypes tegen elkaar testen door meer dan één criteria toe te voegen.

Als u meerdere criteria selecteert, wordt het verkeer gelijkmatig over de geselecteerde criteria verdeeld. Als u bijvoorbeeld twee criteria hebt geselecteerd en uw activiteit is ontworpen om standaardinhoud weer te geven voor 20% van de deelnemers aan de activiteit, dan zal 40% van de deelnemers aan de activiteit de aanbevelingen zien die door elke criteria worden gecontroleerd. Er is geen optie om de percentages voor elke criteria te wijzigen.

* Als u naar bestaande criteria wilt zoeken (bijvoorbeeld als er veel kaarten met criteria worden weergegeven), typt u in het zoekveld totdat de gewenste criteria worden weergegeven, selecteert u de criteria en klikt u op **[!UICONTROL Done]** .

  Sommige criteria worden geleverd bij [!DNL Recommendations] . U en uw team kunnen ook uw eigen aangepaste criteria maken.

* Als u nieuwe criteria wilt maken, klikt u op **[!UICONTROL Create Criteria]** > **[!UICONTROL Create Criteria]** en vult u de gegevens voor de nieuwe criteria in. Voor informatie over het creëren van nieuwe criteria, zie [&#x200B; een Nieuwe Criteria &#x200B;](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md#task_8A9CB465F28D44899F69F38AD27352FE) creëren.

**om criteria te selecteren:**

1. Terwijl [&#x200B; creërend een nieuwe aanbeveling &#x200B;](/help/main/c-recommendations/t-create-recs-activity/create-recs-activity.md#task_6874328773C64C44A73F0A130AD3F96F), in het **[!UICONTROL Select Criteria]** dialoogvakje, bepaal de plaats en selecteer van één of meerdere criteria.

   U kunt het selectievakje [!UICONTROL Industry Type] filter, [!UICONTROL Page Type] filter en [!UICONTROL Compatible] gebruiken om de lijst met criteria te filteren. Met deze opties kunt u de gewenste criteria vinden.

   * **Type van Industrie:** het industrietype wordt gebruikt helpen [!DNL Recommendations] criteria categoriseren. Als u de standaard verticale instellingen wilt wijzigen, klikt u op **[!UICONTROL Recommendations]** > **[!UICONTROL Settings]** en selecteert u de gewenste standaardinstelling **[!UICONTROL Industry Vertical]** .
   * **Type van Pagina:** het paginatype helpt u uw aanbevelingen categoriseren. Er zijn ook ingebouwde criteria die voor elk paginatype kunnen worden gekozen.
   * **Compatibel:** toon slechts die criteria waar de geselecteerde pagina de vereiste gegevens overgaat. Niet alle criteria worden op elke pagina correct uitgevoerd. De pagina of het kader moet `entity.id` of `entity.categoryId` doorgeven om de huidige aanbevelingen voor het item of de huidige categorie compatibel te maken. Over het algemeen is het beter alleen compatibele criteria te laten zien. Als u echter incompatibele criteria voor de activiteit wilt gebruiken, schakelt u het selectievakje **[!UICONTROL Compatible]** uit. U kunt deze optie uitschakelen of inschakelen in de volgende instellingen: **[!UICONTROL Recommendations]** > **[!UICONTROL Settings]** .

1. Klik **[!UICONTROL Next]** om het [&#x200B; Uitgezochte de dialoogvakje van het Ontwerp &#x200B;](/help/main/c-recommendations/c-design-overview/design-overview.md) te tonen.
