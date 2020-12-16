---
keywords: activity url;url;different url
description: De URL van de Activiteit bepaalt de pagina die in de test wordt gebruikt en die opent wanneer de test wordt ontworpen.
title: URL van activiteit
feature: ab
translation-type: tm+mt
source-git-commit: 968d36d65016e51290f6bf754f69c91fd8f68405
workflow-type: tm+mt
source-wordcount: '267'
ht-degree: 0%

---


# Activiteit-URL{#activity-url}

De URL van de Activiteit bepaalt de pagina die in de test wordt gebruikt en die opent wanneer de test wordt ontworpen.

Geef de activiteit-URL op wanneer hierom wordt gevraagd tijdens het maken van activiteiten. Typ de volledige URL (inclusief `https://`) en klik vervolgens op **[!UICONTROL Create]**.

>[!NOTE]
>
>[!DNL Target] maakt geen onderscheid tussen URL-protocollen ( [!DNL https] en  [!DNL http]). Als gevolg hiervan komen [!DNL `http://www.adobe.com`] en [!DNL `https://www.adobe.com`] beide overeen.

## Een andere URL opgeven

Standaard wordt in de [!UICONTROL Visual Experience Composer] de pagina geopend die is opgegeven in de instellingen voor [Visual Experience Composer](/help/administrating-target/visual-experience-composer-set-up.md)
. U kunt een andere pagina opgeven tijdens het maken van activiteiten.

Als u een andere pagina wilt weergeven nadat [!UICONTROL Visual Experience Composer] is geopend, klikt u op het tandwielpictogram **[!UICONTROL Configure]** en selecteert u **[!UICONTROL Page Delivery]**. Voer de URL in het veld Activiteit-URL in.

![Dialoogvenster Pagina-aflevering](/help/c-activities/t-test-ab/t-test-create-ab/assets/url-config-new.png)

Klik **[!UICONTROL Add Template Rule]** om meer pagina&#39;s of secties aan de activiteit toe te voegen.

De extra regels kunnen op om het even welke volgend worden gebaseerd:

* URL
* Domein
* Pad
* Hash-fragment (#)
* Query
* mbox-parameter

De extra regels kunnen met EN of OF aan de Activiteit URL worden aangesloten. Alle regels die u toevoegt, worden tegen elkaar geëvalueerd met EN.

Klik **[!UICONTROL Save]** wanneer u klaar bent.

>[!NOTE]
>
>Als u een URL hebt ingevoerd voor een site die niet de standaard JavaScript-code [!DNL Target] bevat, kunt u geen pagina-elementen selecteren.

Standaard staan de [!UICONTROL Visual Experience Composer] geen wijzigingen toe in elementen die JavaScript bevatten, zoals draaiende banners. U kunt **[!UICONTROL Render using JavaScript]** van een knevel voorzien als u die elementen wilt kunnen veranderen gebruikend [!UICONTROL Visual Experience Composer].

>[!NOTE]
>
>Als u de URL wijzigt nadat u wijzigingen in een pagina hebt aangebracht voor een of meer ervaringen, wordt de ervaring opnieuw ingesteld met de nieuwe pagina en gaan de aangebrachte wijzigingen verloren.
