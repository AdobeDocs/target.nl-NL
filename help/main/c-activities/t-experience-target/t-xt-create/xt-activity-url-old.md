---
keywords: Experience Target;xt;activity url;url
description: Leer hoe te om [!UICONTROL Activity URL] te specificeren die de pagina bepaalt die in de test wordt gebruikt en die opent wanneer de [!UICONTROL Experience Targeting] activiteit gebruikend  [!DNL Adobe Target] wordt ontworpen.
title: Wat is de [!UICONTROL Activity URL] in een [!UICONTROL Experience Targeting] (XT) activiteit?
feature: Experience Targeting
exl-id: 8e3be814-6ad6-4ffa-be8d-68f0cb7857b5
source-git-commit: 3a44c05bea24c622292dd0b774f88f0c93be1d88
workflow-type: tm+mt
source-wordcount: '263'
ht-degree: 0%

---

# URL van activiteit in [!UICONTROL Experience Targeting] (XT) activiteiten

De [!UICONTROL Activity URL] bepaalt de pagina die wordt gebruikt in een [!DNL Adobe Target] [!UICONTROL Experience Targeting] (XT) activiteit. Dit is de pagina die in [!UICONTROL Visual Experience Composer] (VEC) of [!UICONTROL Form-Based Experience Composer] wordt geopend wanneer de activiteit wordt ontworpen.

1. Wanneer ertoe aangezet terwijl [&#x200B; het creëren van een XT activiteit &#x200B;](/help/main/c-activities/t-experience-target/t-xt-create/xt-create.md), specificeer de activiteit URL. Typ de volledige URL (inclusief `https://`) en klik vervolgens op **[!UICONTROL Create Activity]** .

   >[!NOTE]
   >
   >[!DNL Target] maakt geen onderscheid tussen URL-protocollen ( [!DNL https] en [!DNL http] ). Hierdoor komen [!DNL `https://www.adobe.com`] en [!DNL `http://www.adobe.com`] beide overeen.
   >
   >Door gebrek, opent VEC of [&#x200B; vorm-Gebaseerde Composer van de Ervaring &#x200B;](/help/main/c-experiences/form-experience-composer.md) de pagina die in uw [&#x200B; Visuele montages van Composer van de Ervaring wordt gespecificeerd &#x200B;](/help/main/administrating-target/visual-experience-composer-set-up.md). U kunt een andere pagina opgeven tijdens het maken van activiteiten.
   >
   >Als u een URL voor een plaats specificeert die a [[!DNL Target]  at.js de bibliotheek van JavaScript of  [!DNL Adobe Experience Platform Web SDK] &#x200B;](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/overview.html?lang=nl-NL){target=_blank} niet omvat, kunt u geen pagina-elementen selecteren.

1. (Voorwaardelijk) Als u een andere pagina wilt weergeven nadat de VEC is geopend, klikt u op **[!UICONTROL Configure]** , selecteert u **[!UICONTROL Page Delivery]** en geeft u vervolgens de URL op in het veld [!UICONTROL URL] .

   ![&#x200B; de dialoogdoos van de Levering van de Pagina &#x200B;](/help/main/c-activities/t-experience-target/t-xt-create/assets/url-config-new.png)

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

1. Klik op **[!UICONTROL Save]** wanneer u klaar bent.
