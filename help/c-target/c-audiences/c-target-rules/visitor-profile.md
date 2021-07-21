---
keywords: bezoekersprofiel;doelbezoekersprofiel
description: Leer hoe u een publiek kunt maken in [!DNL Adobe Target] om bezoekers aan te wijzen die voldoen aan specifieke profielparameters, zoals nieuwe of geretourneerde bezoeker, categorie affiniteit en meer.
title: Kan ik bezoekers richten die aan specifieke profielparameters voldoen?
feature: Soorten publiek
exl-id: aca45b80-660d-4b8e-a0d7-84627b8fd77b
source-git-commit: b46966a8dbb2ff6d2efbfb8f126783f750c2f08c
workflow-type: tm+mt
source-wordcount: '219'
ht-degree: 0%

---

# Bezoekerprofiel

Maak publiek in [!DNL Adobe Target] om bezoekers aan te wijzen die aan specifieke profielparameters voldoen.

1. Klik in de interface [!DNL Target] op **[!UICONTROL Audiences]** > **[!UICONTROL Create Audience]**.
1. Geef een naam op voor het publiek en voeg een optionele beschrijving toe.
1. Sleep **[!UICONTROL Visitor Profile]** in de ruit van de publieksbouwer.

1. Klik op **[!UICONTROL Select]** en selecteer een van de volgende opties:

   ![](assets/target_visitor_profile.png)

   Bezoekerprofielparameters worden doorgegeven via het mbox (profiel). U kunt nieuwe of terugkerende bezoekers richten, of alle gebruikers omvatten.

   * [!UICONTROL New Visitor]
   * [!UICONTROL Returning Visitor]
   * [!UICONTROL In Other Tests]
   * [!UICONTROL Not In Other Tests]
   * [!UICONTROL First Page of Session]
   * [!UICONTROL Not First Page of Session]
   * [!UICONTROL Category Affinity]

   Er wordt een bezoekersprofiel gemaakt in het lokale Edge-geheugen voor elke mbox-aanroep met nieuw `mboxPC`. Na 30 minuten inactiviteit, wordt het profiel bewaard aan [!DNL Target] gegevensbestand en is toegankelijk van andere randen.

   Wanneer een sitebezoeker zich halverwege de sessie aanmeldt en een `3rdpartyId` krijgt, zijn alle eerder geladen profielkenmerken die zijn gekoppeld aan `3rdPartyId`, direct beschikbaar.

   U kunt parameters van het douaneprofiel en `user.` parameters richten. Kies de parameter die u wilt gebruiken om uw activiteit als doel in te stellen. Als de gewenste parameter niet wordt weergegeven, is de parameter niet geactiveerd door een mbox.

1. (Optioneel) Stel aanvullende regels voor het publiek in.
1. Klik op **[!UICONTROL Done]**.

## Trainingsvideo: Soorten publiek maken ![Overzichtsbadge](/help/assets/overview.png)

Deze video bevat informatie over het gebruik van publiekscategorieën.

* Soorten publiek maken
* Doelcategorieën definiëren

>[!VIDEO](https://video.tv.adobe.com/v/17392)
