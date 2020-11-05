---
keywords: criteria sequence;multiple criteria;algorithms;criteria;recommendations criteria;sequence;limit number of items returned
description: Gebruik reeksen van maximaal vijf criteria om meer controle uit te oefenen over de items die in uw Adobe Target Recommendations-activiteiten worden weergegeven.
title: Criteria-reeksen maken
feature: criteria
uuid: 9a5ca86b-fc79-4c24-b86f-e333b0c63088
translation-type: tm+mt
source-git-commit: 95450abc32be19d04b791af3c62673e9411ab53c
workflow-type: tm+mt
source-wordcount: '719'
ht-degree: 0%

---


# ![PREMIUM](/help/assets/premium.png) : Criteria maken

Gebruik reeksen van maximaal vijf criteria om meer controle uit te oefenen over de items die in uw [!UICONTROL Recommendations] activiteiten worden weergegeven.

>[!NOTE]
>
>Criteria sequenties kunnen niet worden gebruikt met [!UICONTROL Recommendations] activiteiten die vóór de release van oktober 2016 zijn gecreëerd [!DNL Target Premium].

Als u een reeks criteria wilt maken, moet u eerst de criteria maken die u in de reeks wilt opnemen. Zie [Criteria](/help/c-recommendations/c-algorithms/create-new-algorithm.md) maken voor meer informatie.

Door een criteria opeenvolging te gebruiken, kunt u extra gerichte aanbevelingen verstrekken, in plaats van het gebruiken van generischere reserveaanbevelingen, wanneer een criteria niet genoeg resultaten terugkeren om uw ontwerp te vullen. Typisch, zal een criteria opeenvolging van specifieker richten te werk gaan, die minder resultaten zou kunnen terugkeren, aan meer algemeen richten, die gewoonlijk meer resultaten terugkeert.

Afhankelijk van het paginatype kunnen de volgorde van de criteria variëren, zoals in de volgende voorbeelden wordt getoond:

| Paginatype | Mogelijke volgorde van volgreeksen |
| --- | --- |
| Productpagina | <ol><li>Gebaseerd op huidig item, van hetzelfde merk</li><li>Gebaseerd op huidige item, van alle merken</li><li>Gebaseerd op gelijkenis van inhoud</li><li>Gebaseerd op topverkopers</li><li>Gebaseerd op de meeste weergegeven items op de hele site</li></ol> |
| Homepage | <ol><li>Gebaseerd op laatste aankoop van bezoeker </li><li>Gebaseerd op het favoriete object van de bezoeker</li><li>Gebaseerd op de favoriete rubriek van de bezoeker</li><li>Gebaseerd op topverkopers</li><li>Gebaseerd op de meest bekeken website</li></ol> |

## Een reeks criteria maken

U maakt maatreeksen op basis van het [!UICONTROL Create Criteria Sequence] scherm.

Er zijn meerdere manieren om het [!UICONTROL Create Criteria Sequence] scherm te bereiken. Sommige schermopties variëren afhankelijk van de manier waarop u het scherm bereikt.

* Klik in het scherm **[!UICONTROL Recommendations]** > **[!UICONTROL Criteria]** Bibliotheek op **[!UICONTROL Create Criteria]** > **[!UICONTROL Create Criteria Sequence]**. De criteria die u hier maakt, worden automatisch beschikbaar gesteld voor alle [!UICONTROL Recommendations] activiteiten.
* Wanneer u een [!UICONTROL Recommendations] activiteit creeert, van het Uitgezochte scherm van Criteria, klik **[!UICONTROL Create New]** > **[!UICONTROL Create Criteria Sequence]**. U kunt de nieuwe reeks criteria opslaan voor gebruik met andere [!UICONTROL Recommendations] activiteiten.
* Als u een [!UICONTROL Recommendations] activiteit bewerkt, klikt u in een [!UICONTROL Recommendations Location] vak op de pagina en selecteert u **[!UICONTROL Change Criteria]**. Klik in het [!UICONTROL Select Criteria] scherm op **[!UICONTROL Create New]** > **[!UICONTROL Create Criteria Sequence]**. U kunt de nieuwe criteria opslaan voor gebruik met andere [!UICONTROL Recommendations] activiteiten.

In de volgende stappen wordt ervan uitgegaan dat u het [!UICONTROL Create Criteria Sequence] scherm opent met de eerste methode: het scherm **[!UICONTROL Recommendations]** > **[!UICONTROL Criteria]** Bibliotheek.

1. Klik op **[!UICONTROL Recommendations]** > **[!UICONTROL Criteria]**.

1. Klik op **[!UICONTROL Create Criteria]** > **[!UICONTROL Create Criteria Sequence]**.

   ![](assets/CreateCriteriaSequence.png)

1. Vul de gegevens in in de sectie [Basisinformatie](/help/c-recommendations/c-algorithms/create-new-algorithm.md#info) .

1. Klik in de **[!UICONTROL Criteria Sequence]** sectie op **[!UICONTROL Add Criteria]**.

   De volgordevolgorde bepaalt de volgorde waarin een ontwerp wordt gevuld. Als Criteria 1 niet genoeg aanbevelingen heeft om uw ontwerp te vullen, zullen de resterende groeven met Criteria 2 worden gevuld, etc.

   ![Criteria toevoegen](/help/c-recommendations/c-algorithms/assets/add-criteria.png)

1. Selecteer een criterium op het [!UICONTROL Select Criteria] scherm en klik op **[!UICONTROL Add]**.

   U kunt het vakje van het Onderzoek en de filterdrop-down gebruiken om de gewenste criteria te vinden.

   ![Criteria selecteren](/help/c-recommendations/c-algorithms/assets/select-criteria.png)

1. (Optioneel) Sleep de **[!UICONTROL Limit the number of items returned]** schakeloptie naar de positie &quot;Aan&quot; en geef het aantal items op (tussen 1 en 50).

   ![Het aantal geretourneerde items beperken](/help/c-recommendations/c-algorithms/assets/limit-number.png)

   Houd rekening met de volgende gebruiksgevallen om u te helpen de waarde van de [!UICONTROL Limit the number of items returned] optie te begrijpen:

   * **Hoofdlettergebruik 1**: U wilt een combinatie van verschillende soorten punten in één enkele raadsdienblad hebben. U wilt bijvoorbeeld een combinatie van bovenkleding (jassen) en toppen (overhemden, T-shirts) weergeven. Om dit te bereiken, gebruik een Inzameling voor de activiteit die alle potentiële producttypes omvat u in om het even welke groeven in uw ontwerp wilt. Stel vervolgens de eerste criteria in met een statisch filter dat de criteria beperkt tot het opnemen van alleen bovenkleding, en stel de tweede criteria in met een statisch filter dat de criteria beperkt tot alleen bovenkanten. Ten slotte kunt u beide criteria toevoegen aan een reeks criteria en de eerste criteria beperken tot twee sleuven.

      De aanbevolen lade kan er op uw site als volgt uitzien:

      ![Aanbevolen productvak](/help/c-recommendations/c-algorithms/assets/featured-products.png)

   * **Hoofdlettergebruik 2**: U wilt een combinatie van zowel alternatieve items als aanvullende items. Stel één criterium in om een weergegeven/weergegeven algoritme te gebruiken en gebruik een dynamisch filter dat de aanbevolen items beperkt tot de categorie van het huidige item. Stel de tweede criteria in om een weergegeven/gekocht algoritme te gebruiken en gebruik een dynamisch filter dat alleen aanbevolen items bevat die niet overeenkomen met de categorie van het huidige item. Ten slotte kunt u beide criteria toevoegen aan een reeks en de eerste criteria beperken tot twee sleuven.

1. Voeg aanvullende criteria aan uw reeks toe. U kunt maximaal vijf criteria toevoegen aan een reeks.

1. Schakel opties voor [Back-up van inhoud in](/help/c-recommendations/c-algorithms/create-new-algorithm.md#content).

1. Klik op **[!UICONTROL Save]**.

   De opeenvolging van criteria zal in de lijst van Criteria verschijnen.

   Zie [Criteria](/help/c-recommendations/c-algorithms/algorithms.md)voor meer informatie over de opties van de aanbevolen logica.

## Trainingsvideo: Criteria maken in Recommendations (12:33) - ![Zelfstudie](/help/assets/tutorial.png)

Deze video bevat de volgende informatie:

* Criteria maken
* Criteria-reeksen maken
* Aangepaste criteria uploaden

>[!VIDEO](https://video.tv.adobe.com/v/27694?quality=12)
