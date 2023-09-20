---
keywords: activiteit-URL;url;verschillende URL
description: Leer hoe te om Activiteit URL te specificeren die de pagina bepaalt die in de test wordt gebruikt en die wanneer de test wordt ontworpen gebruikend [!DNL Adobe Target].
title: Wat is de activiteit URL in een activiteit A/B?
feature: A/B Tests
exl-id: 7482ae10-fb7e-42ba-9ea0-97b82ed85bff
source-git-commit: 6bca763d24649349dbc7cdf6e5f2dbc4ac0a480d
workflow-type: tm+mt
source-wordcount: '291'
ht-degree: 0%

---

# URL van activiteit

De activiteit URL bepaalt de pagina die in de test wordt gebruikt en die opent wanneer de test gebruikend Adobe Target wordt ontworpen.

Geef de activiteit-URL op wanneer hierom wordt gevraagd tijdens het maken van activiteiten. Typ de volledige URL (inclusief `https://`), klikt u vervolgens op **[!UICONTROL Create]**.

>[!NOTE]
>
>[!DNL Target] maakt geen onderscheid tussen URL-protocollen ( [!DNL https] en [!DNL http]). Dientengevolge, [!DNL `http://www.adobe.com`] en [!DNL `https://www.adobe.com`] beide komen overeen.

## Een andere URL opgeven

Standaard worden de [!UICONTROL Visual Experience Composer] Hiermee wordt de pagina geopend die is opgegeven in uw [Instellingen voor Visual Experience Composer](/help/main/administrating-target/visual-experience-composer-set-up.md). U kunt een andere pagina opgeven tijdens het maken van activiteiten.

1. Een andere pagina weergeven na de [!UICONTROL Visual Experience Composer] opent, op de **[!UICONTROL Experiences]** pagina, klikt u op de **[!UICONTROL Configure]** tandwielpictogram, selecteer vervolgens **[!UICONTROL Page Delivery]**.

1. Geef de URL op in het dialoogvenster **[!UICONTROL URL]** veld.

   ![Dialoogvenster Pagina-aflevering](/help/main/c-activities/t-test-ab/t-test-create-ab/assets/url-config-new.png)

1. (Voorwaardelijk) Klik **[!UICONTROL Add Template Rule]** om meer pagina&#39;s of secties aan de activiteit toe te voegen.

   De extra regels kunnen op om het even welk van het volgende worden gebaseerd:

   * URL
   * Domein
   * Pad
   * Hash-fragment (#)
   * Query
   * mbox-parameter

   De extra regels kunnen tot aan de Activiteit URL met EN of OF worden aangesloten. Alle regels die u toevoegt, worden tegen elkaar geëvalueerd met EN.

1. Klikken **[!UICONTROL Save]** als u klaar bent.

Als u een URL hebt ingevoerd voor een site die geen [!DNL Target] Standaard JavaScript-code. U kunt geen pagina-elementen selecteren.

Standaard worden de [!UICONTROL Visual Experience Composer] staat geen wijzigingen toe in elementen die JavaScript bevatten, zoals draaiende banners. U kunt schakelen **[!UICONTROL Render using JavaScript]** als u die elementen wilt kunnen veranderen gebruikend [!UICONTROL Visual Experience Composer].

>[!NOTE]
>
>Als u de URL wijzigt nadat u wijzigingen in een pagina hebt aangebracht voor een of meer ervaringen, wordt de ervaring opnieuw ingesteld met de nieuwe pagina en gaan de aangebrachte wijzigingen verloren.
