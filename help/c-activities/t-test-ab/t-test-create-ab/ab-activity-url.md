---
keywords: Overview and Reference
description: De URL van de Activiteit bepaalt de pagina die in de test wordt gebruikt en die opent wanneer de test wordt ontworpen.
title: URL van activiteit
feature: ab
topic: Standard
uuid: 65489969-d548-4286-858f-8420120317c0
translation-type: tm+mt
source-git-commit: b2f80c89ecceb6f88a176db7a90e71a162a24641
workflow-type: tm+mt
source-wordcount: '267'
ht-degree: 0%

---


# URL van activiteit{#activity-url}

De URL van de Activiteit bepaalt de pagina die in de test wordt gebruikt en die opent wanneer de test wordt ontworpen.

Geef de activiteit-URL op wanneer hierom wordt gevraagd tijdens het maken van activiteiten. Typ de volledige URL (inclusief `https://`) en klik op **[!UICONTROL Create]**.

>[!NOTE]
>
>[!DNL Target] maakt geen onderscheid tussen URL-protocollen ( [!DNL https] en [!DNL http]). Hierdoor komen [!DNL `http://www.adobe.com`] en [!DNL `https://www.adobe.com`] beide overeen.

## Een andere URL opgeven

Door gebrek, [!UICONTROL Visual Experience Composer] opent de pagina die in uw montages [van Composer van de](/help/administrating-target/visual-experience-composer-set-up.md)Visuele Ervaring wordt gespecificeerd. U kunt een andere pagina opgeven tijdens het maken van activiteiten.

Als u een andere pagina wilt weergeven nadat de pagina is [!UICONTROL Visual Experience Composer] geopend, klikt u op het tandwielpictogram en selecteert u **[!UICONTROL Configure]** **[!UICONTROL Page Delivery]**. Voer de URL in het veld Activiteit-URL in.

![Dialoogvenster Pagina-aflevering](/help/c-activities/t-test-ab/t-test-create-ab/assets/url-config-new.png)

Klik **[!UICONTROL Add Template Rule]** om meer pagina&#39;s of secties aan de activiteit toe te voegen.

De extra regels kunnen op om het even welke volgend worden gebaseerd:

* URL
* Domein
* Pad
* Hash-fragment (#)
* Query
* mbox-parameter

De extra regels kunnen tot aan de Activiteit URL met EN of OF worden aangesloten. Alle regels die u toevoegt, worden tegen elkaar geëvalueerd met EN.

Klik **[!UICONTROL Save]** wanneer u klaar bent.

>[!NOTE]
>
>Als u een URL hebt ingevoerd voor een site die niet de [!DNL Target] standaard JavaScript-code bevat, kunt u geen pagina-elementen selecteren.

Standaard staan wijzigingen in elementen die JavaScript bevatten, zoals draaiende banners, [!UICONTROL Visual Experience Composer] niet toe. U kunt schakelen **[!UICONTROL Render using JavaScript]** als u die elementen wilt kunnen veranderen gebruikend [!UICONTROL Visual Experience Composer].

>[!NOTE]
>
>Als u de URL wijzigt nadat u wijzigingen in een pagina hebt aangebracht voor een of meer ervaringen, wordt de ervaring opnieuw ingesteld met de nieuwe pagina en gaan de aangebrachte wijzigingen verloren.
