---
keywords: Meervoudige tests;activiteit-URL
description: Leer hoe te om de activiteit URL te specificeren die de pagina bepaalt die in de test wordt gebruikt en die opent wanneer de [!UICONTROL Multivariate Test] activiteit gebruikend  [!DNL Adobe Target] wordt ontworpen.
title: Wat is de activiteit-URL in een [!UICONTROL Multivariate Test] (MVT) activiteit?
feature: Multivariate Tests
exl-id: 336169ae-7c8b-4fd5-9b1c-0bd3e9524425
source-git-commit: 8f9c0ea65197fd639d463628e54db79db993c2da
workflow-type: tm+mt
source-wordcount: '269'
ht-degree: 0%

---

# URL van activiteit

De activiteit-URL bepaalt de pagina die in [!UICONTROL Multivariate Test] (MVT) wordt gebruikt, en die opent wanneer de test in [!DNL Adobe Target] wordt ontworpen.

1. Wanneer ertoe aangezet tijdens [&#x200B; activiteitenverwezenlijking &#x200B;](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/create-multivariate-test.md), specificeer de activiteit URL. Typ de volledige URL (inclusief `https://`) en klik vervolgens op **[!UICONTROL Create]** .

   >[!NOTE]
   >
   >[!DNL Target] maakt geen onderscheid tussen URL-protocollen ( [!DNL https] en [!DNL http] ). Hierdoor komen [!DNL `https://www.adobe.com`] en [!DNL `http://www.adobe.com`] beide overeen.

   Door gebrek, opent [!UICONTROL Visual Experience Composer] (VEC) de pagina die in uw [&#x200B; Visuele montages van Composer van de Ervaring wordt gespecificeerd &#x200B;](/help/main/administrating-target/visual-experience-composer-set-up.md). U kunt een andere pagina opgeven tijdens het maken van activiteiten.

1. (Voorwaardelijk) Als u een andere pagina wilt weergeven nadat de VEC is geopend, klikt u op het pictogram **[!UICONTROL Configure]** en selecteert u **[!UICONTROL Page Delivery]** . Geef vervolgens de URL op.

1. (Voorwaardelijk) Klik **[!UICONTROL Add Rule]** om meer pagina&#39;s of secties aan de activiteit toe te voegen.

   De extra regels kunnen op om het even welk van het volgende worden gebaseerd:

   * [!UICONTROL &#x200B; URL]
   * [!UICONTROL Domain]
   * [!UICONTROL Path]
   * [!UICONTROL Hash (#) Fragment]
   * [!UICONTROL Query]
   * [!UICONTROL Custom]

   De extra regels kunnen aan de activiteit URL met EN of OF worden aangesloten. Alle regels die u toevoegt worden tegen elkaar geëvalueerd met EN.

   Klik op **[!UICONTROL Save]** wanneer u klaar bent.

>[!NOTE]
>
>Als u een URL hebt ingevoerd voor een site die de JavaScript-code van [!DNL Target] niet bevat, kunt u geen pagina-elementen selecteren.
>
>Standaard staat de VEC geen wijzigingen toe in elementen die JavaScript bevatten, zoals draaiende banners. U kunt **[!UICONTROL Render using JavaScript]** uitschakelen als u deze elementen wilt kunnen wijzigen met de [!UICONTROL Visual Experience Composer] .

>[!NOTE]
>
>Als u de URL wijzigt nadat u wijzigingen in een pagina hebt aangebracht voor een of meer ervaringen, wordt de ervaring opnieuw ingesteld met de nieuwe pagina en gaan de aangebrachte wijzigingen verloren.
