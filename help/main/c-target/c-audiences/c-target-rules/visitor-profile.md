---
keywords: bezoekersprofiel;doelbezoekersprofiel
description: Leer hoe te om publiek in  [!DNL Adobe Target]  tot stand te brengen om bezoekers te richten die specifieke profielparameters zoals nieuwe of terugkerende bezoeker, categorievijnheid, en meer ontmoeten.
title: Kan ik bezoekers richten die aan specifieke profielparameters voldoen?
feature: Audiences
exl-id: aca45b80-660d-4b8e-a0d7-84627b8fd77b
source-git-commit: 293b2869957c2781be8272cfd0cc9f82d8e4f0f0
workflow-type: tm+mt
source-wordcount: '221'
ht-degree: 0%

---

# Bezoekerprofiel

Maak een publiek in [!DNL Adobe Target] om bezoekers aan te wijzen die aan specifieke profielparameters voldoen.

1. Klik in de interface [!DNL Target] op **[!UICONTROL Audiences]** > **[!UICONTROL Create Audience]** .
1. Geef een naam op voor het publiek en voeg een optionele beschrijving toe.
1. Sleep **[!UICONTROL Visitor Profile]** naar het deelvenster van de publieksbuilder.

1. Klik op **[!UICONTROL Select]** en selecteer een van de volgende opties:

   ![&#x200B; target_bezoeker_profile beeld &#x200B;](assets/target_visitor_profile.png)

   Bezoekerprofielparameters worden doorgegeven via het mbox (profiel). U kunt nieuwe of terugkerende bezoekers richten, of alle gebruikers omvatten.

   * [!UICONTROL New Visitor]
   * [!UICONTROL Returning Visitor]
   * [!UICONTROL In Other Tests]
   * [!UICONTROL Not In Other Tests]
   * [!UICONTROL First Page of Session]
   * [!UICONTROL Not First Page of Session]
   * [!UICONTROL Category Affinity]

   Er wordt een bezoekersprofiel gemaakt in het lokale Edge-geheugen voor elke nieuwe mappenaanroep `mboxPC` . Na 30 minuten inactiviteit, wordt het profiel bewaard aan het [!DNL Target] gegevensbestand en is toegankelijk van andere randen.

   Wanneer een sitebezoeker zich halverwege de sessie aanmeldt en een `3rdpartyId` krijgt, zijn alle eerder geladen profielkenmerken die aan `3rdPartyId` zijn gekoppeld, direct beschikbaar.

   U kunt aangepaste profielparameters en `user.` -parameters als doel instellen. Kies de parameter die u wilt gebruiken om uw activiteit als doel in te stellen. Als de gewenste parameter niet wordt weergegeven, is de parameter niet geactiveerd door een mbox.

1. (Optioneel) Stel aanvullende regels voor het publiek in.
1. Klik op **[!UICONTROL Done]**.

## De video van de opleiding: Creërend publiek ![&#x200B; badge van het Overzicht &#x200B;](/help/main/assets/overview.png)

Deze video bevat informatie over het gebruik van publiekscategorieën.

* Soorten publiek maken
* Categorieën publiek definiëren

>[!VIDEO](https://video.tv.adobe.com/v/17392)
