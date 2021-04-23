---
keywords: Meervoudige tests;activiteit-URL
description: Leer hoe te om Activiteit URL te specificeren die de pagina bepaalt die in de test wordt gebruikt en die opent wanneer de Multivariate activiteit van de Test gebruikend Adobe Target wordt ontworpen.
title: Wat is de activiteit URL in een Multivariate (MVT) activiteit?
feature: Meervoudige tests
exl-id: 336169ae-7c8b-4fd5-9b1c-0bd3e9524425
translation-type: tm+mt
source-git-commit: a92e88b46c72971d5d3c752593d651d8290b674e
workflow-type: tm+mt
source-wordcount: '286'
ht-degree: 0%

---

# URL van activiteit

De activiteit URL bepaalt de pagina die in [!UICONTROL Multivariate Test] (MVT) wordt gebruikt, en die opent wanneer de test in [!DNL Adobe Target] wordt ontworpen.

Geef bij de aanwijzing tijdens [activity creation](/help/c-activities/c-multivariate-testing/t-create-multivariate-test/create-multivariate-test.md) de activiteit-URL op. Typ de volledige URL (inclusief `https://`) en klik vervolgens op **[!UICONTROL Next]**.

>[!NOTE]
>
>[!DNL Target] maakt geen onderscheid tussen URL-protocollen ( [!DNL https] en  [!DNL http]). Als gevolg hiervan komen [!DNL `https://www.adobe.com`] en [!DNL `http://www.adobe.com`] beide overeen.

Door gebrek, [!UICONTROL Visual Experience Composer] (VEC) opent de pagina die in uw [montages van Composer van de Visuele Ervaring ](/help/administrating-target/visual-experience-composer-set-up.md) wordt gespecificeerd. U kunt een andere pagina opgeven tijdens het maken van activiteiten.

Als u een andere pagina wilt weergeven nadat de VEC is geopend, klikt u op het pictogram **[!UICONTROL Configure]** en selecteert u **[!UICONTROL Page Delivery]**. Geef vervolgens de URL op.

![Dialoogvenster Pagina-aflevering](/help/c-activities/c-multivariate-testing/t-create-multivariate-test/assets/url-config.png)

Klik **[!UICONTROL Add Template Rule]** om meer pagina&#39;s of secties aan de activiteit toe te voegen.

De extra regels kunnen op om het even welke volgend worden gebaseerd:

* URL
* Domein
* Pad
* Hash-fragment (#)
* Query
* Parameter

De extra regels kunnen tot aan de Activiteit URL met EN of OF worden aangesloten. Alle regels die u toevoegt, worden tegen elkaar geëvalueerd met EN.

Klik **[!UICONTROL Save]** wanneer u klaar bent.

>[!NOTE]
>
>Als u een URL hebt ingevoerd voor een site die niet de standaard JavaScript-doelcode bevat, kunt u geen pagina-elementen selecteren.

Standaard staat de VEC geen wijzigingen toe in elementen die JavaScript bevatten, zoals draaiende banners. U kunt **[!UICONTROL Render using JavaScript]** van een knevel voorzien als u die elementen wilt kunnen veranderen gebruikend [!UICONTROL Visual Experience Composer].

>[!NOTE]
>
>Als u de URL wijzigt nadat u wijzigingen in een pagina hebt aangebracht voor een of meer ervaringen, wordt de ervaring opnieuw ingesteld met de nieuwe pagina en gaan de aangebrachte wijzigingen verloren.
