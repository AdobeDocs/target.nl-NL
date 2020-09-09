---
keywords: criteria sequence;multiple criteria;algorithms;criteria;recommendations criteria;sequence;
description: Gebruik reeksen van maximaal vijf criteria om meer controle uit te oefenen over de items die in uw Adobe Target Recommendations-activiteiten worden weergegeven.
title: Criteria-reeksen maken
feature: criteria
uuid: 9a5ca86b-fc79-4c24-b86f-e333b0c63088
translation-type: tm+mt
source-git-commit: a4479a26873f39a41782e78651802899512b87fe
workflow-type: tm+mt
source-wordcount: '1016'
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

## Open het scherm &#39;Create Criteria Sequence&#39;

Er zijn meerdere manieren om het [!UICONTROL Create Criteria Sequence] scherm te bereiken. Sommige schermopties variëren afhankelijk van de manier waarop u het scherm bereikt.

* Klik in het scherm **[!UICONTROL Recommendations]** > **[!UICONTROL Criteria]** Bibliotheek op **[!UICONTROL Create Criteria]** > **[!UICONTROL Create Criteria Sequence]**. De criteria die u hier maakt, worden automatisch beschikbaar gesteld voor alle [!UICONTROL Recommendations] activiteiten.
* Wanneer u een [!UICONTROL Recommendations] activiteit creeert, van het Uitgezochte scherm van Criteria, klik **[!UICONTROL Create New]** > **[!UICONTROL Create Criteria Sequence]**. U kunt de nieuwe reeks criteria opslaan voor gebruik met andere [!UICONTROL Recommendations] activiteiten.
* Als u een [!UICONTROL Recommendations] activiteit bewerkt, klikt u in een [!UICONTROL Recommendations Location] vak op de pagina en selecteert u **[!UICONTROL Change Criteria]**. Klik in het [!UICONTROL Select Criteria] scherm op **[!UICONTROL Create New]** > **[!UICONTROL Create Criteria Sequence]**. U kunt de nieuwe criteria opslaan voor gebruik met andere [!UICONTROL Recommendations] activiteiten.

In de volgende stappen wordt ervan uitgegaan dat u het [!UICONTROL Create Criteria Sequence] scherm opent met de eerste methode: het scherm **[!UICONTROL Recommendations]** > **[!UICONTROL Criteria]** Bibliotheek.

1. Klik op **[!UICONTROL Recommendations]** > **[!UICONTROL Criteria]**.

1. Klik op **[!UICONTROL Create Criteria]** > **[!UICONTROL Create Criteria Sequence]**.

   ![](assets/CreateCriteriaSequence.png)

## De sectie Informatie invullen

1. Typ een **[!UICONTROL Name]** voor de reeks.

   Dit is de &quot;interne&quot;naam die wordt gebruikt om de opeenvolging van criteria te beschrijven. Bezoekers van uw site krijgen deze naam niet te zien.

   ![Sectie met informatie over reeks criteria maken](/help/c-recommendations/c-algorithms/assets/criteria-sequence-info.png)

1. Typ een openbare-onder ogen ziet **[!UICONTROL Generic Display Title]** om op de pagina te verschijnen als de veelvoudige criteria in de opeenvolging worden gebruikt om het [!UICONTROL Recommendations] ontwerp te vullen.

   U wilt bijvoorbeeld &quot;Klanten die dit ook hebben bekeken&quot; vervangen. met &quot;Aanbevolen voor u&quot; als het ontwerp items kan bevatten die op meer dan één [!UICONTROL Recommendations] toets zijn gebaseerd.

1. Typ een korte reeks criteria. **[!UICONTROL Description]**

   De beschrijving zou u moeten helpen de opeenvolging van criteria identificeren en zou informatie over zijn doel kunnen omvatten.

1. Selecteer een **[!UICONTROL Industry Vertical]**.

   Uw standaard verticale [](/help/c-recommendations/c-algorithms/algorithms.md#section_936BCFCF234C49A2BEC1C38AAC2D71AF) industrie verschijnt automatisch.

1. Selecteer een **[!UICONTROL Page Type]**.

   U kunt meerdere paginatypen selecteren.

   Samen, worden de industrie verticale en paginatypes gebruikt om uw bewaarde opeenvolging van criteria te categoriseren, die het gemakkelijker maken om opeenvolgingen voor andere [!UICONTROL Recommendations] activiteiten opnieuw te gebruiken.

## Reeks maken {#sequence}

De volgordevolgorde bepaalt de volgorde waarin een ontwerp wordt gevuld. Als Criteria 1 niet genoeg aanbevelingen heeft om uw ontwerp te vullen, zullen de resterende groeven met Criteria 2 worden gevuld, etc.

1. Klik in de **[!UICONTROL Criteria Sequence]** sectie op **[!UICONTROL Add Criteria]**.

   ![Criteria toevoegen](/help/c-recommendations/c-algorithms/assets/add-criteria.png)

1. Selecteer een criterium op het [!UICONTROL Select Criteria] scherm.

   U kunt het vakje van het Onderzoek en de filterdrop-down gebruiken om de gewenste criteria te vinden.

   ![Criteria selecteren](/help/c-recommendations/c-algorithms/assets/select-criteria.png)

1. Klik op **[!UICONTROL Add]**.

1. (Optioneel) Sleep de **[!UICONTROL Limit the number of items returned]** schakeloptie naar de positie &quot;Aan&quot; en geef het aantal items op (tussen 1 en 50).

   ![Het aantal geretourneerde items beperken](/help/c-recommendations/c-algorithms/assets/limit-number.png)

   Houd rekening met de volgende gebruiksgevallen om u te helpen de waarde van de [!UICONTROL Limit the number of items returned] optie te begrijpen:

   * **Hoofdlettergebruik 1**: U wilt een combinatie van verschillende soorten punten in één enkele raadsdienblad hebben. U wilt bijvoorbeeld een combinatie van bovenkleding (jassen) en toppen (overhemden, T-shirts) weergeven. Om dit te bereiken, gebruik een Inzameling voor de activiteit die alle potentiële producttypes omvat u in om het even welke groeven in uw ontwerp wilt. Stel vervolgens de eerste criteria in met een statisch filter dat de criteria beperkt tot het opnemen van alleen bovenkleding, en stel de tweede criteria in met een statisch filter dat de criteria beperkt tot alleen bovenkanten. Ten slotte kunt u beide criteria toevoegen aan een reeks criteria en de eerste criteria beperken tot twee sleuven.

      De aanbevolen lade kan er op uw site als volgt uitzien:

      ![Aanbevolen productvak](/help/c-recommendations/c-algorithms/assets/featured-products.png)

   * **Hoofdlettergebruik 2**: U wilt een combinatie van zowel alternatieve items als aanvullende items. Stel één criterium in om een weergegeven/weergegeven algoritme te gebruiken en gebruik een dynamisch filter dat de aanbevolen items beperkt tot de categorie van het huidige item. Stel de tweede criteria in om een weergegeven/gekocht algoritme te gebruiken en gebruik een dynamisch filter dat alleen aanbevolen items bevat die niet overeenkomen met de categorie van het huidige item. Ten slotte kunt u beide criteria toevoegen aan een reeks en de eerste criteria beperken tot twee sleuven.

1. Voeg aanvullende criteria aan uw reeks toe. U kunt maximaal vijf criteria toevoegen aan een reeks.

## Back-upinhoud opgeven

Kies welke inhoud wordt teruggegeven wanneer er niet genoeg aanbevelingen beschikbaar zijn om het ontwerpmalplaatje te vullen.

Wanneer u een reeks criteria maakt, worden back-upaanbevelingen en renderinstellingen voor gedeeltelijk ontwerp genegeerd voor de afzonderlijke criteria waaruit de reeks bestaat. Als u back-upaanbevelingen en gedeeltelijke ontwerprendering wilt gebruiken, moet u deze voor de reeks inschakelen. Selecteer de juiste gereedschappen. Als u ervoor kiest om back-upaanbevelingen toe te staan, kunt u ook kiezen of u inclusieregels wilt toepassen op de back-ups.

![Instellingen voor back-upinhoud](/help/c-recommendations/c-algorithms/assets/backup-content-settings.png)

1. (Optioneel) Sleep de **[!UICONTROL Partial Design Rendering]** schakeloptie naar de positie &quot;aan&quot;.

   Er worden zoveel mogelijk sleuven ingevuld, maar in de ontwerpsjabloon kan lege ruimte voor de resterende sleuven zijn opgenomen.

1. (Optioneel) Sleep de **[!UICONTROL Backup Recommendations]** schakeloptie naar de positie &quot;aan&quot;.

   Vul eventueel resterende lege sleuven in het ontwerp met een willekeurige selectie van de meest bekeken producten van de hele site.

   Zie [Een back-upaanbeveling](/help/c-recommendations/c-algorithms/backup-recs.md)gebruiken voor meer informatie.

1. (Voorwaardelijk) Als u **[!UICONTROL Backup Recommendations]** in de vorige stap selecteerde, kunt u selecteren **[!UICONTROL Apply inclusion rules to backup recommendations]**.

   Zie Dynamische en statische insluitingsregels [](/help/c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md)gebruiken voor meer informatie.

1. Klik op **[!UICONTROL Save]**.

   De opeenvolging van criteria zal in de lijst van Criteria verschijnen.

   Zie [Criteria](../../c-recommendations/c-algorithms/algorithms.md)voor meer informatie over de opties van de aanbevolen logica.

## Trainingsvideo: Criteria maken in Recommendations (12:33) - ![Zelfstudie](/help/assets/tutorial.png)

Deze video bevat de volgende informatie:

* Criteria maken
* Criteria-reeksen maken
* Aangepaste criteria uploaden

>[!VIDEO](https://video.tv.adobe.com/v/27694?quality=12)
