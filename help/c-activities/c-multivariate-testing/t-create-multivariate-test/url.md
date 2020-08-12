---
keywords: Targeting
description: De URL van de Activiteit bepaalt de pagina die in de Multivariate Test (MVT) wordt gebruikt, en die opent wanneer de test in Adobe Target wordt ontworpen.
title: URL van activiteit
feature: null
uuid: ddc7330c-199a-4e38-b3d4-6786e3997783
translation-type: tm+mt
source-git-commit: a51addc6155f2681f01f2329b25d72327de36701
workflow-type: tm+mt
source-wordcount: '267'
ht-degree: 0%

---


# URL van activiteit{#activity-url}

De activiteit URL bepaalt de pagina die in [!UICONTROL Multivariate Test] (MVT) wordt gebruikt, en die opent wanneer de test binnen wordt ontworpen [!DNL Adobe Target].

Geef de activiteit-URL op wanneer dit wordt gevraagd tijdens het maken [van](/help/c-activities/c-multivariate-testing/t-create-multivariate-test/create-multivariate-test.md)activiteiten. Typ de volledige URL (inclusief `https://`) en klik op **[!UICONTROL Next]**.

>[!NOTE]
>
>[!DNL Target] maakt geen onderscheid tussen URL-protocollen ( [!DNL https] en [!DNL http]). Hierdoor komen [!DNL `https://www.adobe.com`] en [!DNL `http://www.adobe.com`] beide overeen.

Door gebrek, opent [!UICONTROL Visual Experience Composer] (VEC) de pagina die in uw montages [van Composer van de](/help/administrating-target/visual-experience-composer-set-up.md)Visuele Ervaring wordt gespecificeerd. U kunt een andere pagina opgeven tijdens het maken van activiteiten.

Als u een andere pagina wilt weergeven nadat de VEC is geopend, klikt u op het **[!UICONTROL Configure]** pictogram, selecteert u **[!UICONTROL Page Delivery]** en geeft u vervolgens de URL op.

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

Standaard staat de VEC geen wijzigingen toe in elementen die JavaScript bevatten, zoals draaiende banners. U kunt schakelen **[!UICONTROL Render using JavaScript]** als u die elementen wilt kunnen veranderen gebruikend [!UICONTROL Visual Experience Composer].

>[!NOTE]
>
>Als u de URL wijzigt nadat u wijzigingen in een pagina hebt aangebracht voor een of meer ervaringen, wordt de ervaring opnieuw ingesteld met de nieuwe pagina en gaan de aangebrachte wijzigingen verloren.