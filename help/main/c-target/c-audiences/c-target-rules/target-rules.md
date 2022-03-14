---
keywords: gericht;doelcategorieën;doelvoorwaarden;doelmanager;aangepaste profielparameters;bezoekersprofiel;profiel;aangepaste gebruikersparameters;doelregels
description: Leer hoe u categorieën (zoals Browser, Geo, Netwerk, Besturingssysteem, Bezoekersprofiel) kunt gebruiken om inhoud als doel in te stellen.
title: Wat zijn de categorieën voor het publiek?
feature: Audiences
exl-id: 37d6435d-4139-47c5-a871-6595e089d052
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '374'
ht-degree: 0%

---

# Categorieën voor soorten publiek

U kunt zich richten op een van de verschillende categoriekenmerken met [!DNL Adobe Target]. Om het richten regels (of groepen) voor elk attribuut tot stand te brengen, sleep en laat vallen de gewenste attributen in de ruit van de Bouwer van de Publiek.

![Attributen voor publiek](/help/main/c-target/c-audiences/assets/attributes.png)

Als een bepaalde categorie is geselecteerd, kunt u een of meer doelvoorwaarden toepassen. In de categorie Geo definieert u bijvoorbeeld een regel als City=San Francisco. Als u meerdere waarden toevoegt, wordt een OR-voorwaarde gemaakt. De bezoeker moet slechts één van de waarden aanpassen om aan de het richten voorwaarde te voldoen. Voor EN-voorwaarden op dezelfde parameter maakt u een aangepast expressiedoel.

Nadat u een regel hebt gemaakt, klikt u op **[!UICONTROL Done]**. Een samenvatting van de regelvertoningen naast de het richten verbinding voor het niveau u richt.

U kunt een regel verder verfijnen door meer voorwaarden toe te voegen of door extra regels te maken in andere categorieën. U kunt bijvoorbeeld alleen Firefox-gebruikers uit San Francisco als doel instellen die vanuit Google toegang hebben tot uw site. Stel de [!UICONTROL Geo] voor gebruikers uit San Francisco, de [!UICONTROL Browser] categorie voor doelgebruikers met Firefox en de [!UICONTROL Traffic Sources] categorie voor doelgebruikers die afkomstig zijn van [!UICONTROL From Google]. De regels die over categorieën worden gecreeerd worden gecombineerd met de exploitant AND.

Om complexe het richten regels tot stand te brengen die OF verrichtingen over categorieën omvatten, creeer een uitdrukkingsdoel.

U kunt ook aangepaste profielparameters en `user.` parameters. Bij het toevoegen van een publiek, sleept u en zet u een toets neer **[!UICONTROL Visitor Profile]** Kies vervolgens de parameter die u wilt gebruiken om uw activiteit als doel in te stellen. Als de gewenste parameter niet wordt weergegeven, is de parameter niet geactiveerd door een mbox.

Gebruik het zoekvak om te zoeken in uw [!UICONTROL Audiences] lijst. U kunt zoeken naar een willekeurig deel van een publieksnaam of u kunt een specifieke tekenreeks tussen aanhalingstekens plaatsen.

U kunt de [!UICONTROL Audience] lijst op publieksnaam of op de datum waarop deze voor het laatst is gewijzigd. Als u op naam of datum wilt sorteren, klikt u op de kolomkop en selecteert u deze om het publiek in oplopende of aflopende volgorde weer te geven.

## Trainingsvideo: Soorten publiek maken ![Zelfstudie-badge](/help/main/assets/tutorial.png)

Deze video bevat informatie over het gebruik van publiekscategorieën.

* Soorten publiek maken
* Doelcategorieën definiëren

>[!VIDEO](https://video.tv.adobe.com/v/17392)
