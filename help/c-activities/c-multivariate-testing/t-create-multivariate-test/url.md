---
keywords: Multivariate Tests;activity url
description: De URL van de Activiteit bepaalt de pagina die in Adobe Target Multivariate Test (MVT) wordt gebruikt, en die opent wanneer de test in Adobe Target wordt ontworpen.
title: URL van activiteit
feature: Multivariate Tests
translation-type: tm+mt
source-git-commit: 4adade56529fb95e4400e06d04d3c6c69e120edc
workflow-type: tm+mt
source-wordcount: '269'
ht-degree: 0%

---


# Activiteit-URL{#activity-url}

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

De extra regels kunnen met EN of OF aan de Activiteit URL worden aangesloten. Alle regels die u toevoegt, worden tegen elkaar geëvalueerd met EN.

Klik **[!UICONTROL Save]** wanneer u klaar bent.

>[!NOTE]
>
>Als u een URL hebt ingevoerd voor een site die niet de standaard JavaScript-doelcode bevat, kunt u geen pagina-elementen selecteren.

Standaard staat de VEC geen wijzigingen toe in elementen die JavaScript bevatten, zoals draaiende banners. U kunt **[!UICONTROL Render using JavaScript]** van een knevel voorzien als u die elementen wilt kunnen veranderen gebruikend [!UICONTROL Visual Experience Composer].

>[!NOTE]
>
>Als u de URL wijzigt nadat u wijzigingen in een pagina hebt aangebracht voor een of meer ervaringen, wordt de ervaring opnieuw ingesteld met de nieuwe pagina en gaan de aangebrachte wijzigingen verloren.