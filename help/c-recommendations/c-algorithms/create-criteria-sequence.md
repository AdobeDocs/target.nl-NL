---
keywords: criteria opeenvolging;veelvoudige criteria;algoritmen;criteria;aanbevelingen criteria;opeenvolging;grens aantal teruggekeerde punten;groefniveaucontrole;groef
description: Gebruik reeksen van maximaal vijf criteria om meer controle uit te oefenen over de items die in uw Adobe Target Recommendations-activiteiten worden weergegeven.
title: Criteria-reeksen maken
feature: Recommendations
translation-type: tm+mt
source-git-commit: 48b94f967252f5ddb009597456edf0a43bc54ba6
workflow-type: tm+mt
source-wordcount: '758'
ht-degree: 0%

---


# ![Criteria ](/help/assets/premium.png) PREMIUMCreate-reeksen maken

Gebruik reeksen van maximaal vijf criteria om meer controle uit te oefenen over de items die in uw [!UICONTROL Recommendations]-activiteiten worden weergegeven. U kunt ook het aantal geretourneerde items beperken (dit wordt ook wel &#39;&#39;besturingselement voor sleufniveau&#39;&#39; genoemd).

>[!NOTE]
>
>Criteria-reeksen kunnen niet worden gebruikt met [!UICONTROL Recommendations]-activiteiten die vóór de release van oktober 2016 van [!DNL Target Premium] zijn gemaakt.

Als u een reeks criteria wilt maken, moet u eerst de criteria maken die u in de reeks wilt opnemen. Zie [Criteria maken](/help/c-recommendations/c-algorithms/create-new-algorithm.md) voor meer informatie.

Door een criteria opeenvolging te gebruiken, kunt u extra gerichte aanbevelingen verstrekken, in plaats van het gebruiken van generischere reserveaanbevelingen, wanneer een criteria niet genoeg resultaten terugkeren om uw ontwerp te vullen. Typisch, zal een criteria opeenvolging van specifieker richten te werk gaan, die minder resultaten zou kunnen terugkeren, aan meer algemeen richten, die gewoonlijk meer resultaten terugkeert.

Afhankelijk van het paginatype kunnen de volgorde van de criteria variëren, zoals in de volgende voorbeelden wordt getoond:

| Paginatype | Mogelijke volgorde van volgreeksen |
| --- | --- |
| Productpagina | <ol><li>Gebaseerd op huidig item, van hetzelfde merk</li><li>Gebaseerd op huidige item, van alle merken</li><li>Gebaseerd op gelijkenis van inhoud</li><li>Gebaseerd op topverkopers</li><li>Gebaseerd op de meeste weergegeven items op de hele site</li></ol> |
| Homepage | <ol><li>Gebaseerd op laatste aankoop van bezoeker </li><li>Gebaseerd op het favoriete object van de bezoeker</li><li>Gebaseerd op de favoriete rubriek van de bezoeker</li><li>Gebaseerd op topverkopers</li><li>Gebaseerd op de meest bekeken website</li></ol> |

## Een reeks criteria maken

U maakt reeksen criteria op basis van het scherm [!UICONTROL Create Criteria Sequence].

Er zijn meerdere manieren om het [!UICONTROL Create Criteria Sequence] scherm te bereiken. Sommige schermopties variëren afhankelijk van de manier waarop u het scherm bereikt.

* Klik op **[!UICONTROL Recommendations]** > **[!UICONTROL Criteria]** bibliotheekscherm op **[!UICONTROL Create Criteria]** > **[!UICONTROL Create Criteria Sequence]**. Criteria die u hier maakt, worden automatisch beschikbaar gesteld voor alle [!UICONTROL Recommendations]-activiteiten.
* Wanneer u een [!UICONTROL Recommendations] activiteit creeert, van het Uitgezochte scherm van Criteria, klik **[!UICONTROL Create New]** > **[!UICONTROL Create Criteria Sequence]**. U zult de optie hebben om uw nieuwe criteria opeenvolging voor gebruik met andere [!UICONTROL Recommendations] activiteiten te bewaren.
* Wanneer u een [!UICONTROL Recommendations] activiteit uitgeeft, klik in [!UICONTROL Recommendations Location] doos op uw pagina, dan uitgezocht **[!UICONTROL Change Criteria]**. Klik op [!UICONTROL Select Criteria] > **[!UICONTROL Create Criteria Sequence]** in het scherm **[!UICONTROL Create New]**. U hebt de optie om uw nieuwe criteria voor gebruik met andere [!UICONTROL Recommendations] activiteiten te bewaren.

In de volgende stappen wordt ervan uitgegaan dat u het scherm [!UICONTROL Create Criteria Sequence] opent met de eerste methode: het **[!UICONTROL Recommendations]** > **[!UICONTROL Criteria]** bibliotheekscherm.

1. Klik op **[!UICONTROL Recommendations]** > **[!UICONTROL Criteria]**.

1. Klik op **[!UICONTROL Create Criteria]** > **[!UICONTROL Create Criteria Sequence]**.

   ![](assets/CreateCriteriaSequence.png)

1. Vul de gegevens in de sectie [Basisinformatie](/help/c-recommendations/c-algorithms/create-new-algorithm.md#info) in.

1. Klik in de sectie **[!UICONTROL Criteria Sequence]** op **[!UICONTROL Add Criteria]**.

   De volgordevolgorde bepaalt de volgorde waarin een ontwerp wordt gevuld. Als Criteria 1 niet genoeg aanbevelingen heeft om uw ontwerp te vullen, zullen de resterende groeven met Criteria 2 worden gevuld, etc.

   ![Criteria toevoegen](/help/c-recommendations/c-algorithms/assets/add-criteria.png)

1. Selecteer een criterium in het scherm [!UICONTROL Select Criteria] en klik op **[!UICONTROL Add]**.

   U kunt het vakje van het Onderzoek en de filterdrop-down gebruiken om de gewenste criteria te vinden.

   ![Criteria selecteren](/help/c-recommendations/c-algorithms/assets/select-criteria.png)

1. (Optioneel) Schuif de **[!UICONTROL Limit the number of items returned]**-schakeloptie naar de positie &quot;aan&quot; en geef vervolgens het aantal items op (tussen 1 en 50).

   ![Het aantal geretourneerde items beperken](/help/c-recommendations/c-algorithms/assets/limit-number.png)

   Om u te helpen de waarde van de [!UICONTROL Limit the number of items returned] optie begrijpen (soms genoemd &quot;de controle van het groefniveau,&quot;) overweeg de volgende gebruiksgevallen:

   * **Hoofdlettergebruik 1**: U wilt een combinatie van verschillende soorten punten in één enkele raadsdienblad hebben. U wilt bijvoorbeeld een combinatie van bovenkleding (jassen) en toppen (overhemden, T-shirts) weergeven. Om dit te bereiken, gebruik een Inzameling voor de activiteit die alle potentiële producttypes omvat u in om het even welke groeven in uw ontwerp wilt. Stel vervolgens de eerste criteria in met een statisch filter dat de criteria beperkt tot het opnemen van alleen bovenkleding, en stel de tweede criteria in met een statisch filter dat de criteria beperkt tot alleen bovenkanten. Ten slotte kunt u beide criteria toevoegen aan een reeks criteria en de eerste criteria beperken tot twee sleuven.

      De aanbevolen lade kan er op uw site als volgt uitzien:

      ![Aanbevolen productvak](/help/c-recommendations/c-algorithms/assets/featured-products.png)

   * **Hoofdlettergebruik 2**: U wilt een combinatie van zowel alternatieve items als aanvullende items. Stel één criterium in om een weergegeven/weergegeven algoritme te gebruiken en gebruik een dynamisch filter dat de aanbevolen items beperkt tot de categorie van het huidige item. Stel de tweede criteria in om een weergegeven/gekocht algoritme te gebruiken en gebruik een dynamisch filter dat alleen aanbevolen items bevat die niet overeenkomen met de categorie van het huidige item. Ten slotte kunt u beide criteria toevoegen aan een reeks en de eerste criteria beperken tot twee sleuven.

1. Voeg aanvullende criteria aan uw reeks toe. U kunt maximaal vijf criteria toevoegen aan een reeks.

1. Schakel [Opties voor back-upinhoud](/help/c-recommendations/c-algorithms/create-new-algorithm.md#content) in.

1. Klik op **[!UICONTROL Save]**.

   De opeenvolging van criteria zal in de lijst van Criteria verschijnen.

   Zie [Criteria](/help/c-recommendations/c-algorithms/algorithms.md) voor meer informatie over de opties van de aanbevolen logica.

## Trainingsvideo: Criteria maken in Recommendations (12:33) ![Zelfstudie badge](/help/assets/tutorial.png)

Deze video bevat de volgende informatie:

* Criteria maken
* Criteria-reeksen maken
* Aangepaste criteria uploaden

>[!VIDEO](https://video.tv.adobe.com/v/27694?quality=12)
