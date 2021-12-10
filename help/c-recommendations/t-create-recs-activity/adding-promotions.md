---
keywords: promoties;promoties vooraf;promoties;promotietype;lijst met items;promoten op kenmerk;een verzameling promoten
description: Leer hoe je gepromoveerde objecten kunt toevoegen en de plaatsing ervan in je Adobe kunt regelen [!DNL Target] Recommendations-ontwerpen. U kunt statische en dynamische promoties toevoegen.
title: Hoe voeg ik promoties toe in Recommendations-ontwerpen?
feature: Recommendations
exl-id: bd5e5e12-a712-4c4c-9cf8-6b0f4834067b
source-git-commit: 0d8d04091968923c7d343692140279c026d579f4
workflow-type: tm+mt
source-wordcount: '627'
ht-degree: 0%

---

# ![PREMIUM](/help/assets/premium.png) Promoties toevoegen

Aanbevolen objecten toevoegen en de plaatsing ervan in uw [!DNL Adobe Target Recommendations] ontwerpen. U kunt statische en dynamische promoties toevoegen.

>[!IMPORTANT]
>
>Statische en dynamische uitsluitingsregels zijn krachtige functies die u kunnen helpen bij uw marketinginspanningen. Voor gedetailleerde informatie, voorbeelden, en gebruiksscenario&#39;s, zie [Regels voor dynamische en statische integratie gebruiken](/help/c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md#concept_4CB5C0FA705D4E449BD0B37B3D987F9F).

Wanneer u een [!DNL Recommendations] activiteit, je hebt de mogelijkheid om gepromoveerde objecten op te nemen in je [!DNL Recommendations] ontwerp. De bevorderingen gebruiken beschikbare groeven in een ontwerp en nemen belangrijkheid over criteria resultaten en reserveaanbevelingen. Als uw ontwerp bijvoorbeeld zes sleuven heeft en u er twee gebruikt voor speciale acties, zijn er vier sleuven beschikbaar voor aanbevolen items op basis van criteria.

Aanbiedingen worden gededupliceerd ten opzichte van objecten die worden aanbevolen op basis van de criteria voor je activiteit. Een bepaald object wordt dus niet twee keer weergegeven in één aanbevolen lade.

U kunt specifieke objecten promoten, objecten dynamisch promoten, objecten promoten op basis van kenmerken of verzamelingen promoten.

![[!UICONTROL Front Promotion] en [!UICONTROL Back Promotion] opties in [!DNL Target] UI](assets/add_promotion_toggles.png)

>[!NOTE]
>
>Met promoties wijzigt u de CSV-structuur en -uitvoer. Deze wijzigingen kunnen van invloed zijn op externe processen waarbij CSV wordt gebruikt, zoals e-mail.

1. Op de **[!UICONTROL Options]** pagina, klikt u op de knop **[!UICONTROL Front Promotion]** of **[!UICONTROL Back Promotion]** schakelen.

   In de volgende afbeelding ziet u de [!UICONTROL Front Promotion] schakelen in de positie &quot;Aan&quot;.

   ![Voorste-promotieopties toevoegen](/help/c-recommendations/t-create-recs-activity/assets/add_promotion_front.png)

   U kunt promoties invoegen voor *en* na de resultaten van uw criteria.

1. Stel het aantal sleuven voor ontwerpen in dat moet worden gebruikt voor gepromoveerde items.

   Afhankelijk van uw [!DNL Recommendations] ontwerp. Elke sleuf die u gebruikt, is niet beschikbaar voor aanbevelingen die op basis van uw criteria worden geretourneerd.

1. Stel een begin- en einddatum in voor je gepromoveerde objecten.

   Als je geen begindatum instelt, begint de aanbieding direct. Als u geen einddatum instelt, loopt de bevordering voor onbepaalde tijd.

1. Selecteer een **[!UICONTROL Promotion Type]**.

   * Selecteren **[!UICONTROL List of items]** en voert u de `entity.id` waarden, gescheiden door komma&#39;s, van de specifieke items die u wilt promoten.

   * Selecteren **[!UICONTROL Promote by attribute]** en voeg regels toe om de kenmerken te definiëren van de items die u wilt promoten.

      Als u [!UICONTROL Promote by Attribute]kunt u dynamische overeenkomsten maken. Zie voor meer informatie [Regels voor dynamische en statische integratie gebruiken](/help/c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md#concept_4CB5C0FA705D4E449BD0B37B3D987F9F).

   * Selecteren **[!UICONTROL Promote a collection]** en kiest u de verzameling objecten die u wilt promoten.

      U kunt nieuwe verzamelingen maken die u voor promoties wilt gebruiken. Zie [Een verzameling maken](/help/c-recommendations/c-products/collections.md#task_1256DFF6842141FCAADD9E1428EF7F08) voor meer informatie .
   Als u **[!UICONTROL List of Items]** als de **[!UICONTROL Promotion Type]**, kunt u **[!UICONTROL Randomize Item Order]** selectievakje, indien gewenst.

   De standaardsorteervolgorde voor [!UICONTROL List of Items] is gebaseerd op de volgorde die u hebt ingevoerd in het dialoogvenster [!DNL Target] UI of API. Als uw lijst meer items bevat dan het aantal sleuven dat u instelt voor speciale acties, worden de [!UICONTROL Randomize Item Order] Hiermee maakt u de gepromoveerde objecten die in uw ontwerp worden weergegeven willekeurig. Als u deze optie kiest, wordt [!DNL Target] willekeurig selecteren van de objecten die voor promoties in de template zijn ingeschakeld, uit de hele reeks voor speciale acties bij elke treffer.

   Als uw entiteiten geen `entity.value` -kenmerk (je verkoopt bijvoorbeeld geen producten) kunt u een numerieke waarde in de `entity.value` kenmerk, zoals de publicatiedatum. In dit geval kunnen gepromoveerde objecten op basis van de meest recente publicatiedatum in aflopende volgorde worden gepromoot. De `entity.value` het kenmerk is van het type double; tekenreeksen worden niet geaccepteerd.

   Als u **[!UICONTROL Promote by Attribute]** of **[!UICONTROL Promote a Collection]** is de optie om de volgorde willekeurig te maken niet van toepassing.

   Wanneer u specifieke objecten promoot met de [!UICONTROL Promote by Attribute] of [!UICONTROL Promote a Collection] opties, de standaardvolgorde waarin items worden weergegeven, is gebaseerd op de `entity.value` in aflopende numerieke volgorde.

   In de volgende tabel worden de verschillen tussen deze opties weergegeven:

   | Type aanbieding | Standaardsortering | Back-upsortering | Dynamisch filteren, optie |
   | --- | --- | --- | --- |
   | [!UICONTROL List of Items] | De volgorde die is ingevoerd in de doelgebruikersinterface/API | Willekeurig (indien geselecteerd via UI/API) | Nee |
   | [!UICONTROL Promote by Attribute] | `entity.value` (aflopende volgorde) | Geen randomisatie | Ja |
   | [!UICONTROL Promote a Collection] | `entity.value` (aflopende volgorde) | Geen randomisatie | Nee |

1. Klik op **[!UICONTROL Save]**.

Promoties worden toegepast op alle ervaringen in de activiteit.
