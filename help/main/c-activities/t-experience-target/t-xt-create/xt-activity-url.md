---
keywords: Experience Targeting;xt;activity url;url
description: Leer hoe u de Activiteit-URL opgeeft die de pagina bepaalt die wordt gebruikt in de test en die wordt geopend wanneer de Experience Targeting-activiteit is ontworpen met Adobe Target.
title: Wat is de activiteit URL in een ervaring richtend (XT) activiteit?
feature: Experience Targeting
exl-id: 8e3be814-6ad6-4ffa-be8d-68f0cb7857b5
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '271'
ht-degree: 0%

---

# Activiteits-URL in Experience Targeting-activiteiten (XT)

De [!UICONTROL Activity URL] Hiermee bepaalt u de pagina die wordt gebruikt in het dialoogvenster [!DNL Adobe Target] [!UICONTROL Experience Targeting] (XT) en dat wordt geopend in de [!UICONTROL Visual Experience Composer] (VEC) of [!UICONTROL Form-Based Experience Composer] wanneer de activiteit is ontworpen.

1. Als dit wordt gevraagd [een XT-activiteit maken](/help/main/c-activities/t-experience-target/t-xt-create/xt-create.md), geeft u de activiteit-URL op. Typ de volledige URL (inclusief `https://`), klikt u vervolgens op **[!UICONTROL Create Activity]**.

   >[!NOTE]
   >
   >[!DNL Target] maakt geen onderscheid tussen URL-protocollen ( [!DNL https] en [!DNL http]). Dientengevolge [!DNL `https://www.adobe.com`] en [!DNL `http://www.adobe.com`] beide komen overeen.
   >
   >Standaard wordt met de VEC of Form-Based Experience Composer de pagina geopend die is opgegeven in uw [Instellingen voor Visual Experience Composer](/help/main/administrating-target/visual-experience-composer-set-up.md). U kunt een andere pagina opgeven tijdens het maken van activiteiten.
   >
   >Als u een URL opgeeft voor een site die niet de standaard JavaScript-doelcode bevat, kunt u geen pagina-elementen selecteren.

1. (Voorwaardelijk) Als u een andere pagina wilt weergeven nadat de VEC is geopend, klikt u op **[!UICONTROL Configure]**, selecteert u **[!UICONTROL Page Delivery]** en geeft u de URL op in het dialoogvenster [!UICONTROL URL] veld.

   ![Dialoogvenster Pagina-aflevering](/help/main/c-activities/t-experience-target/t-xt-create/assets/url-config-new.png)

   >[!NOTE]
   >
   >Als u de URL wijzigt nadat u wijzigingen in een pagina hebt aangebracht voor een of meer ervaringen, wordt de ervaring opnieuw ingesteld met de nieuwe pagina en gaan de aangebrachte wijzigingen verloren.

1. (Voorwaardelijk) Klik **[!UICONTROL Add Template Rule]** om meer pagina&#39;s of secties aan de activiteit toe te voegen.

   De extra regels kunnen op om het even welke volgend worden gebaseerd:

   * URL
   * Domein
   * Pad
   * Hash-fragment (#)
   * Query
   * mbox-parameter

   De extra regels kunnen tot aan de Activiteit URL met EN of OF worden aangesloten. Alle regels die u toevoegt, worden tegen elkaar geëvalueerd met EN.

1. Klikken **[!UICONTROL Save]** als u klaar bent.
