---
keywords: Targeting
description: De Activiteit URL bepaalt de pagina die in de Ervaring wordt gebruikt richtend activiteit, en die in Adobe Target Visual Experience Composer (VEC) of op vorm-Gebaseerde Composer van de Ervaring opent wanneer de activiteit wordt ontworpen.
title: URL van activiteit
feature: xt
uuid: 970de8ba-ab60-4339-866b-27889bec67f9
translation-type: tm+mt
source-git-commit: b2f80c89ecceb6f88a176db7a90e71a162a24641
workflow-type: tm+mt
source-wordcount: '265'
ht-degree: 0%

---


# URL van activiteit{#activity-url}

De Activiteit URL bepaalt de pagina die in de Ervaring het richten (XT) activiteit wordt gebruikt, en die in de Visuele Composer van de Ervaring (VEC) of op vorm-Gebaseerde Composer van de Ervaring opent wanneer de activiteit wordt ontworpen.

1. Geef de activiteit-URL op wanneer hierom wordt gevraagd tijdens het [maken van een XT-activiteit](/help/c-activities/t-experience-target/t-xt-create/xt-create.md). Typ de volledige URL (inclusief `https://`) en klik op **[!UICONTROL Create Activity]**.

   >[!NOTE]
   >
   >[!DNL Target] maakt geen onderscheid tussen URL-protocollen ( [!DNL https] en [!DNL http]). Hierdoor komen [!DNL `https://www.adobe.com`] en [!DNL `http://www.adobe.com`] beide overeen.
   >
   >Door gebrek, opent VEC of op vorm-Gebaseerde Composer van de Ervaring de pagina die in uw montages [van Composer van de](/help/administrating-target/visual-experience-composer-set-up.md)Visuele Ervaring wordt gespecificeerd. U kunt een andere pagina opgeven tijdens het maken van activiteiten.
   >
   >Als u een URL opgeeft voor een site die de standaard JavaScript-doelcode niet bevat, kunt u geen pagina-elementen selecteren.

1. (Voorwaardelijk) Als u een andere pagina wilt weergeven nadat de VEC is geopend, klikt u op **[!UICONTROL Configure]**, selecteert u **[!UICONTROL Page Delivery]** en geeft u de URL op in het [!UICONTROL URL] veld.

   ![Dialoogvenster Pagina-aflevering](/help/c-activities/t-experience-target/t-xt-create/assets/url-config-new.png)

   >[!NOTE]
   >
   >Als u de URL wijzigt nadat u wijzigingen in een pagina hebt aangebracht voor een of meer ervaringen, wordt de ervaring opnieuw ingesteld met de nieuwe pagina en gaan de aangebrachte wijzigingen verloren.

1. (Voorwaardelijk) Klik **[!UICONTROL Add Template Rule]** om meer pagina&#39;s of secties aan de activiteit toe te voegen.

   De extra regels kunnen op om het even welke volgend worden gebaseerd:

   * URL
   * Domein
   * Pad
   * Hash-fragment (#)
   * Query
   * mbox-parameter

   De extra regels kunnen tot aan de Activiteit URL met EN of OF worden aangesloten. Alle regels die u toevoegt, worden tegen elkaar geëvalueerd met EN.

1. Klik **[!UICONTROL Save]** wanneer u klaar bent.