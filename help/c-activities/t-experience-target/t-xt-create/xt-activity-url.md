---
keywords: Experience Targeting;xt;activity url;url
description: De Activiteit URL bepaalt de pagina die in de Ervaring van Adobe Target die activiteit richt wordt gebruikt, en die in Visual Experience Composer (VEC) of op vorm-Gebaseerde Composer van de Ervaring opent wanneer de activiteit wordt ontworpen.
title: URL van activiteit
feature: Experience Targeting
translation-type: tm+mt
source-git-commit: 48b94f967252f5ddb009597456edf0a43bc54ba6
workflow-type: tm+mt
source-wordcount: '266'
ht-degree: 0%

---


# Activiteits-URL in Experience Targeting-activiteiten (XT)

De [!UICONTROL Activity URL] bepaalt de pagina die in [!DNL Adobe Target] [!UICONTROL Experience Targeting] (XT) activiteit wordt gebruikt, en die in [!UICONTROL Visual Experience Composer] (VEC) of [!UICONTROL Form-Based Experience Composer] opent wanneer de activiteit wordt ontworpen.

1. Wanneer ertoe aangezet terwijl [het creëren van een XT activiteit](/help/c-activities/t-experience-target/t-xt-create/xt-create.md), specificeer de activiteit URL. Typ de volledige URL (inclusief `https://`) en klik vervolgens op **[!UICONTROL Create Activity]**.

   >[!NOTE]
   >
   >[!DNL Target] maakt geen onderscheid tussen URL-protocollen ( [!DNL https] en  [!DNL http]). Als gevolg hiervan komen [!DNL `https://www.adobe.com`] en [!DNL `http://www.adobe.com`] beide overeen.
   >
   >Door gebrek, opent VEC of op vorm-Gebaseerde Composer van de Ervaring de pagina die in uw [montages van Composer van de Visuele Ervaring ](/help/administrating-target/visual-experience-composer-set-up.md) wordt gespecificeerd. U kunt een andere pagina opgeven tijdens het maken van activiteiten.
   >
   >Als u een URL opgeeft voor een site die niet de standaard JavaScript-doelcode bevat, kunt u geen pagina-elementen selecteren.

1. (Voorwaardelijk) om een verschillende pagina te tonen nadat VEC opent, klik **[!UICONTROL Configure]**, selecteer **[!UICONTROL Page Delivery]**, en specificeer URL in het [!UICONTROL URL] gebied.

   ![Dialoogvenster Pagina-aflevering](/help/c-activities/t-experience-target/t-xt-create/assets/url-config-new.png)

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

   De extra regels kunnen met EN of OF aan de Activiteit URL worden aangesloten. Alle regels die u toevoegt, worden tegen elkaar geëvalueerd met EN.

1. Klik **[!UICONTROL Save]** wanneer u klaar bent.