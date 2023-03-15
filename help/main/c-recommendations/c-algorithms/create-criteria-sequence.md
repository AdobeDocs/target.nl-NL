---
keywords: criteria opeenvolging;veelvoudige criteria;algoritmen;criteria;aanbevelingen criteria;opeenvolging;grens aantal teruggekeerde punten;groefniveaucontrole;groef
description: Leer hoe u reeksen van maximaal vijf criteria instelt om meer controle uit te oefenen over de items die in uw Adobe worden weergegeven [!DNL Target] Recommendations-activiteiten.
title: Hoe kan ik in Recommendations reeksen criteria maken?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="See what's included in Target Premium."
feature: Recommendations
exl-id: 5366c86c-7685-478b-a621-9b3f24296ab7
source-git-commit: bde5506033fbca1577fad1cda1af203702fc4bb3
workflow-type: tm+mt
source-wordcount: '766'
ht-degree: 0%

---

# Criteria-reeksen maken

Gebruik reeksen van maximaal vijf criteria om meer controle uit te oefenen over de items die in uw [!UICONTROL Recommendations] activiteiten. U kunt ook het aantal geretourneerde items beperken (dit wordt ook wel &#39;&#39;besturingselement voor sleufniveau&#39;&#39; genoemd).

>[!NOTE]
>
>Criteria-reeksen kunnen niet worden gebruikt met [!UICONTROL Recommendations] activiteiten die vóór de release van oktober 2016 zijn gecreëerd [!DNL Target Premium].

Als u een reeks criteria wilt maken, moet u eerst de criteria maken die u in de reeks wilt opnemen. Zie [Criteria maken](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md) voor meer informatie .

Door een criteria opeenvolging te gebruiken, kunt u extra gerichte aanbevelingen verstrekken, in plaats van het gebruiken van generischere reserveaanbevelingen, wanneer een criteria niet genoeg resultaten terugkeren om uw ontwerp te vullen. Typisch, zal een criteria opeenvolging van specifieker richten te werk gaan, die minder resultaten zou kunnen terugkeren, aan meer algemeen richten, die gewoonlijk meer resultaten terugkeert.

Afhankelijk van het paginatype kunnen de volgorde van de criteria variëren, zoals in de volgende voorbeelden wordt getoond:

| Paginatype | Mogelijke volgorde van volgreeksen |
| --- | --- |
| Productpagina | <ol><li>Gebaseerd op huidig item, van hetzelfde merk</li><li>Gebaseerd op huidige item, van alle merken</li><li>Gebaseerd op gelijkenis van inhoud</li><li>Gebaseerd op topverkopers</li><li>Gebaseerd op de meeste weergegeven items op de hele site</li></ol> |
| Homepage | <ol><li>Gebaseerd op laatste aankoop van bezoeker </li><li>Gebaseerd op het favoriete object van de bezoeker</li><li>Gebaseerd op de favoriete rubriek van de bezoeker</li><li>Gebaseerd op topverkopers</li><li>Gebaseerd op de meest bekeken website</li></ol> |

## Een reeks criteria maken

U maakt reeksen criteria op basis van de [!UICONTROL Create Criteria Sequence] scherm.

Er zijn meerdere manieren om de [!UICONTROL Create Criteria Sequence] scherm. Sommige schermopties variëren afhankelijk van de manier waarop u het scherm bereikt.

* Op de **[!UICONTROL Recommendations]** > **[!UICONTROL Criteria]** bibliotheekscherm, klik **[!UICONTROL Create Criteria]** > **[!UICONTROL Create Criteria Sequence]**. De criteria die u hier maakt, worden automatisch beschikbaar gesteld voor alle [!UICONTROL Recommendations] activiteiten.
* Wanneer u een [!UICONTROL Recommendations] activiteit, van het Uitgezochte scherm van Criteria, klik **[!UICONTROL Create New]** > **[!UICONTROL Create Criteria Sequence]**. U hebt de optie om uw nieuwe reeks criteria op te slaan voor gebruik met andere [!UICONTROL Recommendations] activiteiten.
* Wanneer u een [!UICONTROL Recommendations] activiteit, klik in [!UICONTROL Recommendations Location] op uw pagina en selecteer vervolgens **[!UICONTROL Change Criteria]**. Op de [!UICONTROL Select Criteria] scherm, klikken **[!UICONTROL Create New]** > **[!UICONTROL Create Criteria Sequence]**. U hebt de optie om uw nieuwe criteria op te slaan voor gebruik met andere [!UICONTROL Recommendations] activiteiten.

De volgende stappen veronderstellen u tot [!UICONTROL Create Criteria Sequence] scherm met de eerste methode: de **[!UICONTROL Recommendations]** > **[!UICONTROL Criteria]** bibliotheekscherm.

1. Klik op **[!UICONTROL Recommendations]** > **[!UICONTROL Criteria]**.

1. Klik op **[!UICONTROL Create Criteria]** > **[!UICONTROL Create Criteria Sequence]**.

   ![CreateCriteriaSequence-afbeelding](assets/CreateCriteriaSequence.png)

1. Vul de gegevens in in de [Basisinformatie](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md#info) sectie.

1. In de **[!UICONTROL Criteria Sequence]** sectie, klikt u op **[!UICONTROL Add Criteria]**.

   De volgordevolgorde bepaalt de volgorde waarin een ontwerp wordt gevuld. Als Criteria 1 niet genoeg aanbevelingen heeft om uw ontwerp te vullen, zullen de resterende groeven met Criteria 2 worden gevuld, etc.

   ![Criteria toevoegen](/help/main/c-recommendations/c-algorithms/assets/add-criteria.png)

1. Op de [!UICONTROL Select Criteria] scherm, selecteer criteria, dan klik **[!UICONTROL Add]**.

   U kunt het vakje van het Onderzoek en de filterdrop-down gebruiken om de gewenste criteria te vinden.

   ![Criteria selecteren](/help/main/c-recommendations/c-algorithms/assets/select-criteria.png)

1. (Optioneel) Schuif de schuifregelaar **[!UICONTROL Limit the number of items returned]** Schakel over naar de positie &quot;aan&quot; en geef vervolgens het aantal items op (tussen 1 en 50).

   ![Het aantal geretourneerde items beperken](/help/main/c-recommendations/c-algorithms/assets/limit-number.png)

   Om u te helpen de waarde van begrijpen [!UICONTROL Limit the number of items returned] (ook wel &quot;besturingselement voor sleufniveau&quot; genoemd) kunt u de volgende gebruiksgevallen overwegen:

   * **Hoofdlettergebruik 1**: U wilt een combinatie van verschillende soorten punten in één enkele raadsdienblad hebben. U wilt bijvoorbeeld een combinatie van bovenkleding (jassen) en toppen (overhemden, T-shirts) weergeven. Om dit te bereiken, gebruik een Inzameling voor de activiteit die alle potentiële producttypes omvat u in om het even welke groeven in uw ontwerp wilt. Stel vervolgens de eerste criteria in met een statisch filter dat de criteria beperkt tot het opnemen van alleen bovenkleding, en stel de tweede criteria in met een statisch filter dat de criteria beperkt tot alleen bovenkanten. Ten slotte kunt u beide criteria toevoegen aan een reeks criteria en de eerste criteria beperken tot twee sleuven.

      De aanbevolen lade kan er op uw site als volgt uitzien:

      ![Aanbevolen productvak](/help/main/c-recommendations/c-algorithms/assets/featured-products.png)

   * **Hoofdlettergebruik 2**: U wilt een combinatie van zowel alternatieve items als aanvullende items. Stel één criterium in om een weergegeven/weergegeven algoritme te gebruiken en gebruik een dynamisch filter dat de aanbevolen items beperkt tot de categorie van het huidige item. Stel de tweede criteria in om een weergegeven/gekocht algoritme te gebruiken en gebruik een dynamisch filter dat alleen aanbevolen items bevat die niet overeenkomen met de categorie van het huidige item. Ten slotte kunt u beide criteria toevoegen aan een reeks en de eerste criteria beperken tot twee sleuven.

1. Voeg aanvullende criteria aan uw reeks toe. U kunt maximaal vijf criteria toevoegen aan een reeks.

1. Inschakelen [Opties voor back-upinhoud](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md#content).

1. Klik op **[!UICONTROL Save]**.

   De opeenvolging van criteria zal in de lijst van Criteria verschijnen.

   Voor meer informatie over de opties van de aanbeveling logica, zie [Criteria](/help/main/c-recommendations/c-algorithms/algorithms.md).

## Trainingsvideo: Criteria maken in Recommendations (12:33) ![Zelfstudie-badge](/help/main/assets/tutorial.png)

Deze video bevat de volgende informatie:

* Criteria maken
* Criteria-reeksen maken
* Aangepaste criteria uploaden

>[!VIDEO](https://video.tv.adobe.com/v/27694?quality=12)
