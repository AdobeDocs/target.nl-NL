---
keywords: activiteit-URL;url;verschillende URL
description: Ontdek hoe u [!UICONTROL Activity URL] kunt instellen om testpagina's te definiëren en een nauwkeurig testontwerp te garanderen.
title: Wat is de activiteit URL in een activiteit A/B?
feature: A/B Tests
hide: true
hidefromtoc: true
source-git-commit: 6e9d18b8347d8ae68be699640c4cde91bdec762c
workflow-type: tm+mt
source-wordcount: '225'
ht-degree: 0%

---

# URL van activiteit

De activiteit-URL bepaalt de pagina die in de test wordt gebruikt en die wordt geopend wanneer de test wordt ontworpen gebruikend [!DNL Adobe Target].

Geef de activiteit-URL op wanneer hierom wordt gevraagd tijdens het maken van activiteiten. Typ de volledige URL (inclusief `https://`) en klik vervolgens op **[!UICONTROL Create]** .

>[!NOTE]
>
>[!DNL Target] maakt geen onderscheid tussen URL-protocollen ( [!DNL https] en [!DNL http] ). Hierdoor komen [!DNL `http://www.adobe.com`] en [!DNL `https://www.adobe.com`] beide overeen.

## Een andere URL opgeven

Door gebrek, opent [!UICONTROL Visual Experience Composer] de pagina die in uw [ Visuele montages van Composer van de Ervaring ](/help/main/administrating-target/visual-experience-composer-set-up.md) wordt gespecificeerd. U kunt een andere pagina opgeven tijdens het maken van activiteiten.

1. Als u een andere pagina wilt weergeven nadat de pagina [!UICONTROL Visual Experience Composer] is geopend, klikt u op de **[!UICONTROL Experiences]** pagina **[!UICONTROL Configure]** boven aan de pagina en selecteert u vervolgens **[!UICONTROL Page Delivery]** .

1. Geef de URL op in het veld **[!UICONTROL URL]** .

1. (Voorwaardelijk) Klik **[!UICONTROL Add Rule]** om meer pagina&#39;s of secties aan de activiteit toe te voegen.

   De extra regels kunnen op om het even welk van het volgende worden gebaseerd:

   * URL
   * Domein
   * Pad
   * Hash-fragment (#)
   * Query
   * mbox-parameter

   De extra regels kunnen aan de activiteit URL met EN of OF worden aangesloten. Alle regels die u toevoegt, worden tegen elkaar geëvalueerd met EN.

1. Klik op **[!UICONTROL Save]** wanneer u klaar bent.

<!-- If you entered a URL for a site that does not include the [!DNL Target]s JavaScript code, you cannot select page elements.

By default, the [!UICONTROL Visual Experience Composer] does not allow changes to elements containing JavaScript, such as rotating banners. You can toggle off **[!UICONTROL Render using JavaScript]** if you want to be able to alter those elements using the [!UICONTROL Visual Experience Composer].-->

>[!NOTE]
>
>Als u de URL wijzigt nadat u wijzigingen in een pagina hebt aangebracht voor een of meer ervaringen, wordt de ervaring opnieuw ingesteld met de nieuwe pagina en gaan de aangebrachte wijzigingen verloren.