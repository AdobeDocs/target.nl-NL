---
keywords: bezoekersprofiel;doelbezoekersprofiel
description: Leer hoe u in Adobe Target doelgroepen kunt maken voor bezoekers die voldoen aan specifieke profielparameters, zoals nieuwe of geretourneerde bezoeker, categorie affiniteit en meer.
title: Kan ik bezoekers richten die aan specifieke profielparameters voldoen?
feature: Audiences
translation-type: tm+mt
source-git-commit: bb27f6e540998f7dbe7642551f7a5013f2fd25b4
workflow-type: tm+mt
source-wordcount: '231'
ht-degree: 0%

---


# Bezoekerprofiel{#visitor-profile}

Maak een publiek voor doelbezoekers die voldoen aan specifieke profielparameters.

1. Klik in de interface [!DNL Target] op **[!UICONTROL Audiences]** > **[!UICONTROL Create Audience]**.
1. Noem het publiek.
1. Klik op **[!UICONTROL Add Rule]** > **[!UICONTROL Visitor Profile]**.

   ![](assets/target_visitor_profile.png)

1. Klik op **[!UICONTROL Select]** en selecteer een van de volgende opties:

   Bezoekerprofielparameters worden doorgegeven via het mbox (profiel). U kunt nieuwe of terugkerende bezoekers richten, of alle gebruikers omvatten.

   * Nieuwe bezoeker
   * Bezoeker terugsturen
   * In andere tests
   * Niet in andere tests
   * Eerste pagina van sessie
   * Niet eerste pagina van sessie
   * Categorie-affiniteit

   Er wordt een bezoekersprofiel gemaakt in het lokale Edge-geheugen voor elke mbox-aanroep met nieuw `mboxPC`. Na 30 minuten inactiviteit, wordt het profiel bewaard aan het gegevensbestand van het Doel en is toegankelijk van andere randen.

   Wanneer een sitebezoeker zich halverwege de sessie aanmeldt en een `3rdpartyId` krijgt, zijn alle eerder geladen profielkenmerken die zijn gekoppeld aan `3rdPartyId`, direct beschikbaar.

   U kunt parameters van het douaneprofiel en `user.` parameters richten. Kies de parameter die u wilt gebruiken om uw activiteit als doel in te stellen. Als de gewenste parameter niet verschijnt, is de parameter niet in brand gestoken door een mbox.

1. (Optioneel) Klik op **[!UICONTROL Add Rule]** en stel aanvullende regels in voor het publiek.
1. Klik op **[!UICONTROL Save]**.

## Trainingsvideo: Soorten publiek maken ![Overzichtsbadge](/help/assets/overview.png)

Deze video bevat informatie over het gebruik van publiekscategorieën.

* Soorten publiek maken
* Doelcategorieën definiëren

>[!VIDEO](https://video.tv.adobe.com/v/17392)
