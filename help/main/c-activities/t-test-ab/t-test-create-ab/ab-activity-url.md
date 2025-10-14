---
keywords: activiteit-URL;url;verschillende URL
description: Ontdek hoe u [!UICONTROL Activity URL] kunt instellen om testpagina's te definiëren en een nauwkeurig testontwerp te garanderen.
title: Wat is de activiteit URL in een activiteit A/B?
feature: A/B Tests
exl-id: 7f1b8364-790d-4767-bff3-4217ced1a77b
source-git-commit: 2f86c9ee89b4e1698180f6b3dc9df393733eb780
workflow-type: tm+mt
source-wordcount: '279'
ht-degree: 0%

---

# URL van activiteit

De activiteit-URL bepaalt de pagina die in de test wordt gebruikt en die wordt geopend wanneer de test wordt ontworpen gebruikend [!DNL Adobe Target].

Geef de activiteit-URL op wanneer hierom wordt gevraagd tijdens het maken van activiteiten. Typ de volledige URL (inclusief `https://`) en klik vervolgens op **[!UICONTROL Create]** .

>[!NOTE]
>
>[!DNL Target] maakt geen onderscheid tussen URL-protocollen ( [!DNL https] en [!DNL http] ). Hierdoor komen [!DNL `http://www.adobe.com`] en [!DNL `https://www.adobe.com`] beide overeen.

## Een andere URL opgeven

Door gebrek, opent [!UICONTROL Visual Experience Composer] de pagina die in uw [&#x200B; Visuele montages van Composer van de Ervaring &#x200B;](/help/main/administrating-target/visual-experience-composer-set-up.md) wordt gespecificeerd. U kunt een andere pagina opgeven tijdens het maken van activiteiten.

1. (Voorwaardelijk) Als u een andere pagina wilt weergeven nadat [!UICONTROL Visual Experience Composer] is geopend, klikt u op de **[!UICONTROL Experiences]** -pagina **[!UICONTROL Configure]** boven aan de pagina en selecteert u vervolgens **[!UICONTROL Page Delivery]** .

1. Geef de URL op in het veld **[!UICONTROL URL]** .

1. (Voorwaardelijk) Klik **[!UICONTROL Add Rule]** om meer pagina&#39;s of secties aan de activiteit toe te voegen.

   De extra regels kunnen op om het even welk van het volgende worden gebaseerd:

   * URL
   * Domein
   * Pad
   * Hash-fragment (#)
   * Query
   * mbox-parameter
   * Aangepast

   De extra regels kunnen aan de activiteit URL met EN of OF worden aangesloten. Alle regels die u toevoegt, worden tegen elkaar geëvalueerd met EN.

1. Klik op **[!UICONTROL Save]** wanneer u klaar bent.

   Als u een URL voor een plaats inging die niet de code van JavaScript van [!DNL Target] omvat, kunt u geen paginaelementen selecteren.

   Standaard staan in [!UICONTROL Visual Experience Composer] geen wijzigingen toe in elementen die JavaScript bevatten, zoals roterende banners. U kunt **[!UICONTROL Render using JavaScript]** uitschakelen als u deze elementen wilt kunnen wijzigen met de opdracht [!UICONTROL Visual Experience Composer] .—>

>[!NOTE]
>
>Als u de URL wijzigt nadat u wijzigingen in een pagina hebt aangebracht voor een of meer ervaringen, wordt de ervaring opnieuw ingesteld met de nieuwe pagina en gaan de aangebrachte wijzigingen verloren.
