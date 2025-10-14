---
keywords: promoties;promoties vooraf;promoties;promotietype;lijst met items;promoten op kenmerk;een verzameling promoten
description: Leer hoe te om bevorderde punten toe te voegen en hun plaatsing in uw ontwerpen van de Aanbevelingen van Adobe te controleren  [!DNL Target] . U kunt statische en dynamische promoties toevoegen.
title: Hoe voeg ik promoties toe in ontwerpen met aanbevelingen?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=nl-NL#premium newtab=true" tooltip="Kijk wat er in Target Premium is opgenomen."
feature: Recommendations
exl-id: bd5e5e12-a712-4c4c-9cf8-6b0f4834067b
source-git-commit: 07062b7df75300bd7558a24da5121df454520e42
workflow-type: tm+mt
source-wordcount: '637'
ht-degree: 0%

---

# Promoties toevoegen

Voeg gepromoveerde items toe en controleer de plaatsing ervan in uw [!DNL Adobe Target Recommendations] -ontwerpen. U kunt statische en dynamische promoties toevoegen.

>[!IMPORTANT]
>
>Statische en dynamische uitsluitingsregels zijn krachtige functies die u kunnen helpen bij uw marketinginspanningen. Voor gedetailleerde informatie, voorbeelden, en gebruik-case scenario&#39;s, zie [&#x200B; Dynamische en statische opnemingsregels van het Gebruik &#x200B;](/help/main/c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md#concept_4CB5C0FA705D4E449BD0B37B3D987F9F).

Wanneer u een [!DNL Recommendations] -activiteit maakt, kunt u gepromoveerde items opnemen in uw [!DNL Recommendations] -ontwerp. De bevorderingen gebruiken beschikbare groeven in een ontwerp en nemen belangrijkheid over criteria resultaten en reserveaanbevelingen. Als uw ontwerp bijvoorbeeld zes sleuven heeft en u er twee gebruikt voor speciale acties, zijn er vier sleuven beschikbaar voor aanbevolen items op basis van criteria.

Aanbiedingen worden gededupliceerd ten opzichte van objecten die worden aanbevolen op basis van de criteria voor je activiteit. Een bepaald object wordt dus niet twee keer weergegeven in één aanbevolen lade.

U kunt specifieke objecten promoten, objecten dynamisch promoten, objecten promoten op basis van kenmerken of verzamelingen promoten.

![[!UICONTROL Front Promotion] en [!UICONTROL Back Promotion] opties in [!DNL Target] UI &#x200B;](assets/add_promotion_toggles.png)

>[!NOTE]
>
>Met promoties wijzigt u de CSV-structuur en -uitvoer. Deze wijzigingen kunnen van invloed zijn op externe processen waarbij CSV wordt gebruikt, zoals e-mail.

1. Klik op de pagina **[!UICONTROL Options]** op de schakeloptie **[!UICONTROL Front Promotion]** of **[!UICONTROL Back Promotion]** .

   In de volgende afbeelding ziet u de [!UICONTROL Front Promotion] -schakeloptie op de positie &quot;Aan&quot;.

   ![&#x200B; voeg de Voorste opties van de Bevordering &#x200B;](/help/main/c-recommendations/t-create-recs-activity/assets/add_promotion_front.png) toe

   U kunt bevorderingen zowel vóór *als* na uw criteria opnemen resultaten.

1. Stel het aantal sleuven voor ontwerpen in dat moet worden gebruikt voor gepromoveerde items.

   Afhankelijk van uw [!DNL Recommendations] -ontwerp kunt u maximaal 20 sleuven gebruiken. Elke sleuf die u gebruikt, is niet beschikbaar voor aanbevelingen die op basis van uw criteria worden geretourneerd.

1. Stel een begin- en einddatum in voor je gepromoveerde objecten.

   Als je geen begindatum instelt, begint de aanbieding direct. Als u geen einddatum instelt, loopt de bevordering voor onbepaalde tijd.

1. Selecteer een **[!UICONTROL Promotion Type]** .

   * Selecteer **[!UICONTROL List of items]** en voer de `entity.id` -waarden in, gescheiden door komma&#39;s, van de specifieke items die u wilt promoten.

   * Selecteer **[!UICONTROL Promote by attribute]** en voeg regels toe om de kenmerken te definiëren van de items die u wilt promoten.

     Als u [!UICONTROL Promote by Attribute] selecteert, kunt u dynamische overeenkomsten maken. Voor meer informatie, zie [&#x200B; Dynamische en statische opnemingsregels van het Gebruik &#x200B;](/help/main/c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md#concept_4CB5C0FA705D4E449BD0B37B3D987F9F).

   * Selecteer **[!UICONTROL Promote a collection]** en kies de verzameling items die u wilt promoten.

     U kunt nieuwe verzamelingen maken die u voor promoties wilt gebruiken. Zie [&#x200B; een inzameling &#x200B;](/help/main/c-recommendations/c-products/collections.md#task_1256DFF6842141FCAADD9E1428EF7F08) voor meer informatie creëren.

   Als u **[!UICONTROL List of Items]** als **[!UICONTROL Promotion Type]** kiest, kunt u desgewenst het selectievakje **[!UICONTROL Randomize Item Order]** inschakelen.

   De standaardsorteervolgorde voor [!UICONTROL List of Items] is gebaseerd op de volgorde die u hebt ingevoerd in de gebruikersinterface of API van [!DNL Target] . Als uw lijst meer items bevat dan het aantal sleuven dat u instelt voor speciale acties, worden met de optie [!UICONTROL Randomize Item Order] de geprezen items die in uw ontwerp worden weergegeven, willekeurig ingedeeld. Als u deze optie kiest, worden in [!DNL Target] willekeurig de items geselecteerd die zijn ingeschakeld voor promoties in de sjabloon, uit de gehele set met speciale acties op elke hit.

   Als uw entiteiten geen attribuut `entity.value` hebben (bijvoorbeeld wanneer u geen producten verkoopt), kunt u een numerieke waarde in het attribuut `entity.value` doorgeven, zoals de publicatiedatum. In dit geval kunnen gepromoveerde objecten op basis van de meest recente publicatiedatum in aflopende volgorde worden gepromoot. Het attribuut `entity.value` is van het type double; het accepteert geen tekenreeksen.

   Als u de optie **[!UICONTROL Promote by Attribute]** of **[!UICONTROL Promote a Collection]** hebt geselecteerd, is de optie om de volgorde te randomiseren niet van toepassing.

   Wanneer specifieke items worden bevorderd met de opties [!UICONTROL Promote by Attribute] of [!UICONTROL Promote a Collection] , wordt de standaardvolgorde waarin items worden weergegeven, gebaseerd op het kenmerk `entity.value` in aflopende numerieke volgorde.

   In de volgende tabel worden de verschillen tussen deze opties weergegeven:

   | Soort promotie | Standaardsortering | Back-upsortering | Dynamisch filteren, optie |
   | --- | --- | --- | --- |
   | [!UICONTROL List of Items] | De volgorde die is ingevoerd in de doelgebruikersinterface/API | Willekeurig (indien geselecteerd via UI/API) | Nee |
   | [!UICONTROL Promote by Attribute] | `entity.value` (aflopende volgorde) | Geen randomisatie | Ja |
   | [!UICONTROL Promote a Collection] | `entity.value` (aflopende volgorde) | Geen randomisatie | Nee |

1. Klik op **[!UICONTROL Save]**.

Promoties worden toegepast op alle ervaringen in de activiteit.
