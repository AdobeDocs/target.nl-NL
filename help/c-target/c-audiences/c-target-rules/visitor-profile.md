---
keywords: visitor profile;target visitor profile
description: Maak een publiek in Adobe Target om bezoekers aan te wijzen die aan specifieke profielparameters voldoen.
title: Opties voor bezoekersprofiel in Adobe Target-doelgroepen
feature: audiences
uuid: 462c80f4-bd5f-4dce-b02b-21b2c33c5bf6
translation-type: tm+mt
source-git-commit: 6922b80c88cbd2947c3bfd0cc9d8409ff5dcdcd0
workflow-type: tm+mt
source-wordcount: '211'
ht-degree: 0%

---


# Bezoekerprofiel{#visitor-profile}

Maak een publiek voor doelbezoekers die voldoen aan specifieke profielparameters.

1. Klik in de [!DNL Target] interface op **[!UICONTROL Audiences]** > **[!UICONTROL Create Audience]**.
1. Noem het publiek.
1. Klik op **[!UICONTROL Add Rule]** > **[!UICONTROL Visitor Profile]**.

   ![](assets/target_visitor_profile.png)

1. Klik **[!UICONTROL Select]** en selecteer een van de volgende opties:

   Bezoekerprofielparameters worden doorgegeven via het mbox (profiel). U kunt nieuwe of terugkerende bezoekers richten, of alle gebruikers omvatten.

   * Nieuwe bezoeker
   * Bezoeker terugsturen
   * In andere tests
   * Niet in andere tests
   * Eerste pagina van sessie
   * Niet eerste pagina van sessie
   * Categorie-affiniteit

   Er wordt een bezoekersprofiel gemaakt in het lokale Edge-geheugen voor elke nieuwe box-aanroep `mboxPC`. Na 30 minuten inactiviteit, wordt het profiel bewaard aan het gegevensbestand van het Doel en is toegankelijk van andere randen.

   Wanneer een sitebezoeker zich halverwege de sessie aanmeldt en een profiel krijgt, `3rdpartyId``3rdPartyId` zijn alle eerder geladen profielkenmerken die aan de site zijn gekoppeld, direct beschikbaar.

   U kunt aangepaste profielparameters en `user.` parameters als doel instellen. Kies de parameter die u wilt gebruiken om uw activiteit als doel in te stellen. Als de gewenste parameter niet verschijnt, is de parameter niet in brand gestoken door een mbox.

1. (Optioneel) Klik op aanvullende regels voor het publiek **[!UICONTROL Add Rule]** en stel deze in.
1. Klik op **[!UICONTROL Save]**.

## Trainingsvideo: Badge ![Overzicht publiek maken](/help/assets/overview.png)

Deze video bevat informatie over het gebruik van publiekscategorieën.

* Soorten publiek maken
* Doelcategorieën definiëren

>[!VIDEO](https://video.tv.adobe.com/v/17392)
