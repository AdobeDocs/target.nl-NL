---
keywords: activiteit-URL;url;verschillende URL
description: Leer hoe te om Activiteit URL te specificeren die de pagina bepaalt die in de test wordt gebruikt en die opent wanneer de test gebruikend  [!DNL Adobe Target] wordt ontworpen.
title: Wat is de activiteit URL in een activiteit A/B?
feature: A/B Tests
exl-id: 7482ae10-fb7e-42ba-9ea0-97b82ed85bff
source-git-commit: eb7e892a85fa3952ffc22172085d421756d0dfb5
workflow-type: tm+mt
source-wordcount: '291'
ht-degree: 0%

---

# URL van activiteit

De activiteit URL bepaalt de pagina die in de test wordt gebruikt en die opent wanneer de test gebruikend Adobe Target wordt ontworpen.

Geef de activiteit-URL op wanneer hierom wordt gevraagd tijdens het maken van activiteiten. Typ de volledige URL (inclusief `https://`) en klik vervolgens op **[!UICONTROL Create]** .

>[!NOTE]
>
>[!DNL Target] maakt geen onderscheid tussen URL-protocollen ( [!DNL https] en [!DNL http] ). Hierdoor komen [!DNL `http://www.adobe.com`] en [!DNL `https://www.adobe.com`] beide overeen.

## Een andere URL opgeven

Door gebrek, opent [!UICONTROL Visual Experience Composer] de pagina die in uw [&#x200B; Visuele montages van Composer van de Ervaring &#x200B;](/help/main/administrating-target/visual-experience-composer-set-up.md) wordt gespecificeerd. U kunt een andere pagina opgeven tijdens het maken van activiteiten.

1. Als u een andere pagina wilt weergeven nadat [!UICONTROL Visual Experience Composer] is geopend, klikt u op de **[!UICONTROL Experiences]** -pagina op het tandwielpictogram **[!UICONTROL Configure]** en selecteert u vervolgens **[!UICONTROL Page Delivery]** .

1. Geef de URL op in het veld **[!UICONTROL URL]** .

   ![&#x200B; de dialoogdoos van de Levering van de Pagina &#x200B;](/help/main/c-activities/t-test-ab/t-test-create-ab/assets/url-config-new.png)

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

Als u een URL hebt ingevoerd voor een site die de [!DNL Target] standaard JavaScript-code niet bevat, kunt u geen pagina-elementen selecteren.

Standaard staan in [!UICONTROL Visual Experience Composer] geen wijzigingen toe in elementen die JavaScript bevatten, zoals roterende banners. U kunt **[!UICONTROL Render using JavaScript]** uitschakelen als u deze elementen wilt kunnen wijzigen met de [!UICONTROL Visual Experience Composer] .

>[!NOTE]
>
>Als u de URL wijzigt nadat u wijzigingen in een pagina hebt aangebracht voor een of meer ervaringen, wordt de ervaring opnieuw ingesteld met de nieuwe pagina en gaan de aangebrachte wijzigingen verloren.
