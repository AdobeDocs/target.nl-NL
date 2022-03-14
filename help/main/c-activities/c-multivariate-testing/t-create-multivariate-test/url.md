---
keywords: Meervoudige tests;activiteit-URL
description: Leer hoe te om Activiteit URL te specificeren die de pagina bepaalt die in de test wordt gebruikt en die opent wanneer de Multivariate activiteit van de Test gebruikend Adobe Target wordt ontworpen.
title: Wat is de activiteit URL in een Multivariate (MVT) activiteit?
feature: Multivariate Tests
exl-id: 336169ae-7c8b-4fd5-9b1c-0bd3e9524425
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '284'
ht-degree: 0%

---

# URL van activiteit

De activiteit-URL bepaalt de pagina die in [!UICONTROL Multivariate Test] (MVT) en die wordt geopend wanneer de test is ontworpen in [!DNL Adobe Target].

Wanneer dit wordt gevraagd tijdens [activiteit creëren](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/create-multivariate-test.md), geeft u de activiteit-URL op. Typ de volledige URL (inclusief `https://`), klikt u vervolgens op **[!UICONTROL Next]**.

>[!NOTE]
>
>[!DNL Target] maakt geen onderscheid tussen URL-protocollen ( [!DNL https] en [!DNL http]). Dientengevolge [!DNL `https://www.adobe.com`] en [!DNL `http://www.adobe.com`] beide komen overeen.

Standaard worden de [!UICONTROL Visual Experience Composer] (VEC) opent de pagina die in uw [Instellingen voor Visual Experience Composer](/help/main/administrating-target/visual-experience-composer-set-up.md). U kunt een andere pagina opgeven tijdens het maken van activiteiten.

Als u een andere pagina wilt weergeven nadat de VEC is geopend, klikt u op de knop **[!UICONTROL Configure]** pictogram, dan selecteren **[!UICONTROL Page Delivery]** en geeft u vervolgens de URL op.

![Dialoogvenster Pagina-aflevering](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/assets/url-config.png)

Klikken **[!UICONTROL Add Template Rule]** om meer pagina&#39;s of secties aan de activiteit toe te voegen.

De extra regels kunnen op om het even welke volgend worden gebaseerd:

* URL
* Domein
* Pad
* Hash-fragment (#)
* Query
* Parameter

De extra regels kunnen tot aan de Activiteit URL met EN of OF worden aangesloten. Alle regels die u toevoegt, worden tegen elkaar geëvalueerd met EN.

Klikken **[!UICONTROL Save]** als u klaar bent.

>[!NOTE]
>
>Als u een URL hebt ingevoerd voor een site die niet de standaard JavaScript-doelcode bevat, kunt u geen pagina-elementen selecteren.

Standaard staat de VEC geen wijzigingen toe in elementen die JavaScript bevatten, zoals draaiende banners. U kunt schakelen **[!UICONTROL Render using JavaScript]** als u die elementen wilt kunnen veranderen gebruikend [!UICONTROL Visual Experience Composer].

>[!NOTE]
>
>Als u de URL wijzigt nadat u wijzigingen in een pagina hebt aangebracht voor een of meer ervaringen, wordt de ervaring opnieuw ingesteld met de nieuwe pagina en gaan de aangebrachte wijzigingen verloren.
