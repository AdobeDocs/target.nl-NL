---
keywords: promotions;front promotions;back promotions;promotions type
description: Voeg gepromoveerde objecten toe en controleer de plaatsing ervan in Adobe Target Recommendations-ontwerpen. U kunt statische en dynamische promoties toevoegen.
title: Aanbiedingen toevoegen in Adobe Target Recommendations-ontwerpen.
feature: recs creation
uuid: 732bf2c2-0cc7-4d5d-9919-9fe668344d39
translation-type: tm+mt
source-git-commit: 95450abc32be19d04b791af3c62673e9411ab53c
workflow-type: tm+mt
source-wordcount: '447'
ht-degree: 0%

---


# ![PREMIUM](/help/assets/premium.png) promoties toevoegen{#add-promotions}

Voeg gepromoveerde objecten toe en controleer de plaatsing ervan in Recommendations-ontwerpen. U kunt statische en dynamische promoties toevoegen.

>[!IMPORTANT]
>
>Statische en dynamische uitsluitingsregels zijn krachtige functies die u kunnen helpen bij uw marketinginspanningen. Voor gedetailleerde informatie, voorbeelden, en gebruik-case scenario&#39;s, zie de Dynamische en Statische Regels [van de Insluiting van het](/help/c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md#concept_4CB5C0FA705D4E449BD0B37B3D987F9F)Gebruik.

Wanneer u een [!DNL Recommendations] activiteit maakt, kunt u gepromoveerde objecten in uw [!DNL Recommendations] ontwerp opnemen. De bevorderingen gebruiken beschikbare groeven in een ontwerp en nemen belangrijkheid over criteria resultaten en reserveaanbevelingen. Als uw ontwerp bijvoorbeeld zes sleuven heeft en u er twee gebruikt voor speciale acties, zijn er vier sleuven beschikbaar voor aanbevolen items op basis van criteria.

Aanbiedingen worden gededupliceerd ten opzichte van objecten die worden aanbevolen op basis van de criteria voor je activiteit. Een bepaald object wordt dus niet twee keer weergegeven in één aanbevolen lade.

U kunt specifieke objecten promoten, objecten dynamisch promoten, objecten promoten op basis van kenmerken of verzamelingen promoten.

![](assets/add_promotion_toggles.png)

>[!NOTE]
>
>Met promoties wijzigt u de CSV-structuur en -uitvoer. Deze wijzigingen kunnen van invloed zijn op externe processen waarbij CSV wordt gebruikt, zoals e-mail.

1. Klik op de **[!UICONTROL Options]** pagina op de **[!UICONTROL Front Promotion]** of **[!UICONTROL Back Promotion]** schakeloptie.

   In de volgende afbeelding ziet u de [!UICONTROL Front Promotion] schakeloptie op de positie &quot;Aan&quot;.

   ![Voorste-promotieopties toevoegen](/help/c-recommendations/t-create-recs-activity/assets/add_promotion_front.png)

   Je kunt promoties invoegen voor *en na de resultaten van* je criteria.
1. Stel het aantal sleuven voor ontwerpen in dat moet worden gebruikt voor gepromoveerde items.

   Afhankelijk van uw [!DNL Recommendations] ontwerp kunt u maximaal 20 sleuven gebruiken. Elke sleuf die u gebruikt, is niet beschikbaar voor aanbevelingen die op basis van uw criteria worden geretourneerd.

1. Stel een begin- en einddatum in voor je gepromoveerde objecten.

   Als je geen begindatum instelt, begint de aanbieding direct. Als u geen einddatum instelt, loopt de bevordering voor onbepaalde tijd.

1. Selecteer een **[!UICONTROL Promotion Type]**.

   * Selecteer **[!UICONTROL List of items]** en voer de `entity.id` waarden in, gescheiden door komma&#39;s, van de specifieke items die u wilt promoten.

      Als uw lijst meer items bevat dan het aantal sleuven dat u instelt voor speciale acties, kunt u het **[!UICONTROL Randomize Item Order]** selectievakje inschakelen om de gepromoveerde items te variëren die in uw ontwerp worden weergegeven. Als u deze optie kiest, wordt het aantal objecten dat voor speciale acties in de sjabloon is ingeschakeld, willekeurig geselecteerd in de hele set voor speciale acties voor elk bezoek.

   * Selecteer **[!UICONTROL Promote by attribute]** en voeg regels toe om de kenmerken te definiëren van de items die u wilt promoten.

      Als u Promote by Attribute selecteert, kunt u dynamische gelijken tot stand brengen. Zie Dynamische en statische [insluitingsregels](/help/c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md#concept_4CB5C0FA705D4E449BD0B37B3D987F9F)gebruiken voor meer informatie.

   * Selecteer **[!UICONTROL Promote a collection]** en kies de verzameling objecten die u wilt promoten. U kunt nieuwe verzamelingen maken die u voor promoties wilt gebruiken. Zie [Een verzameling](/help/c-recommendations/c-products/collections.md#task_1256DFF6842141FCAADD9E1428EF7F08) maken voor meer informatie.

1. Klik op **[!UICONTROL Save.]**.

Promoties worden toegepast op alle ervaringen in de activiteit.
