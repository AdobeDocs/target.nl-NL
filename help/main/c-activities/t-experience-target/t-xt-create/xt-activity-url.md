---
keywords: Experience Target;xt;activity url;url
description: Leer hoe u de [!UICONTROL Activity URL] die de pagina bepaalt die in de test wordt gebruikt en die wanneer opent [!UICONTROL Experience Targeting] activiteit is ontworpen met [!DNL Adobe Target].
title: Wat is de [!UICONTROL Activity URL] In een [!UICONTROL Experience Targeting] (XT) Activiteit?
feature: Experience Targeting
exl-id: 8e3be814-6ad6-4ffa-be8d-68f0cb7857b5
source-git-commit: 24513d8cb39d38dcfbc74bf40961d5517cc90a4b
workflow-type: tm+mt
source-wordcount: '269'
ht-degree: 0%

---

# URL van activiteit in [!UICONTROL Experience Targeting] (XT) activiteiten

De [!UICONTROL Activity URL] Hiermee bepaalt u de pagina die wordt gebruikt in een [!DNL Adobe Target] [!UICONTROL Experience Targeting] (XT) activiteit. Dit is de pagina die wordt geopend in het dialoogvenster [!UICONTROL Visual Experience Composer] (VEC) of [!UICONTROL Form-Based Experience Composer] wanneer de activiteit is ontworpen.

1. Als dit wordt gevraagd [een XT-activiteit maken](/help/main/c-activities/t-experience-target/t-xt-create/xt-create.md), geeft u de activiteit-URL op. Typ de volledige URL (inclusief `https://`), klikt u vervolgens op **[!UICONTROL Create Activity]**.

   >[!NOTE]
   >
   >[!DNL Target] maakt geen onderscheid tussen URL-protocollen ( [!DNL https] en [!DNL http]). Dientengevolge, [!DNL `https://www.adobe.com`] en [!DNL `http://www.adobe.com`] beide komen overeen.
   >
   >De VEC of [Formuliergebaseerde Experience Composer](/help/main/c-experiences/form-experience-composer.md) Hiermee wordt de pagina geopend die is opgegeven in uw [Instellingen voor Visual Experience Composer](/help/main/administrating-target/visual-experience-composer-set-up.md). U kunt een andere pagina opgeven tijdens het maken van activiteiten.
   >
   >Als u een URL opgeeft voor een site die geen [[!DNL Target] at.js JavaScript-bibliotheek of [!DNL Adobe Experience Platform Web SDK]](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/overview.html){target=_blank}kunt u geen pagina-elementen selecteren.

1. (Voorwaardelijk) Om een andere pagina te tonen nadat VEC opent, klik **[!UICONTROL Configure]**, selecteert u **[!UICONTROL Page Delivery]** en geeft u vervolgens de URL op in het dialoogvenster [!UICONTROL URL] veld.

   ![Dialoogvenster Pagina-aflevering](/help/main/c-activities/t-experience-target/t-xt-create/assets/url-config-new.png)

   >[!NOTE]
   >
   >Als u de URL wijzigt nadat u wijzigingen in een pagina hebt aangebracht voor een of meer ervaringen, wordt de ervaring opnieuw ingesteld met de nieuwe pagina en gaan de aangebrachte wijzigingen verloren.

1. (Voorwaardelijk) Klik **[!UICONTROL Add Template Rule]** om meer pagina&#39;s of secties aan de activiteit toe te voegen.

   De extra regels kunnen op om het even welk van het volgende worden gebaseerd:

   * URL
   * Domein
   * Pad
   * Hash-fragment (#)
   * Query
   * mbox-parameter

   De extra regels kunnen tot aan de Activiteit URL met EN of OF worden aangesloten. Alle regels die u toevoegt, worden tegen elkaar geëvalueerd met EN.

1. Klikken **[!UICONTROL Save]** als u klaar bent.
