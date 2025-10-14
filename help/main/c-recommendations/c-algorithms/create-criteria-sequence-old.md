---
keywords: criteria opeenvolging;veelvoudige criteria;algoritmen;criteria;aanbevelingen criteria;opeenvolging;grens aantal teruggekeerde punten;groefniveaucontrole;groef
description: Leer hoe te om opeenvolgingen van maximaal vijf criteria te plaatsen om grotere controle van de punten uit te oefenen die in uw activiteiten van de Aanbevelingen van Adobe  [!DNL Target]  verschijnen.
title: Hoe maak ik reeksen criteria in aanbevelingen?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=nl-NL#premium newtab=true" tooltip="Kijk wat er in Target Premium is opgenomen."
feature: Recommendations
exl-id: 5366c86c-7685-478b-a621-9b3f24296ab7
source-git-commit: 02ffe8da6cdf96039218656b9690fa719a77910c
workflow-type: tm+mt
source-wordcount: '786'
ht-degree: 0%

---

# Criteria-reeksen maken

Gebruik reeksen van maximaal vijf criteria om meer controle uit te oefenen over de items die in uw [!UICONTROL Recommendations] -activiteiten worden weergegeven. U kunt ook het aantal geretourneerde items beperken (dit wordt ook wel &#39;&#39;besturingselement voor sleufniveau&#39;&#39; genoemd).

>[!NOTE]
>
>Criteria-reeksen kunnen niet worden gebruikt met [!UICONTROL Recommendations] -activiteiten die zijn gemaakt vóór de release van oktober 2016 van [!DNL Target Premium] .

Als u een reeks criteria wilt maken, moet u eerst de criteria maken die u in de reeks wilt opnemen. Zie [&#x200B; criteria &#x200B;](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md) voor meer informatie creëren.

Door een criteria opeenvolging te gebruiken, kunt u extra gerichte aanbevelingen verstrekken, in plaats van het gebruiken van generischere reserveaanbevelingen, wanneer een criteria niet genoeg resultaten terugkeren om uw ontwerp te vullen. Typisch, zal een criteria opeenvolging van specifieker richten te werk gaan, die minder resultaten zou kunnen terugkeren, aan meer algemeen richten, die gewoonlijk meer resultaten terugkeert.

Afhankelijk van het paginatype kunnen de volgorde van de criteria variëren, zoals in de volgende voorbeelden wordt getoond:

| Paginatype | Mogelijke volgorde van reeksen |
| --- | --- |
| Productpagina | <ol><li>Gebaseerd op huidig item, van hetzelfde merk</li><li>Gebaseerd op huidige item, van alle merken</li><li>Gebaseerd op gelijkenis van inhoud</li><li>Gebaseerd op topverkopers</li><li>Gebaseerd op de meeste weergegeven items op de hele site</li></ol> |
| Homepage | <ol><li>Gebaseerd op laatste aankoop van bezoeker </li><li>Gebaseerd op het favoriete object van de bezoeker</li><li>Gebaseerd op favoriete rubriek van bezoeker</li><li>Gebaseerd op topverkopers</li><li>Gebaseerd op de meest bekeken website</li></ol> |

## Een reeks criteria maken

U maakt reeksen criteria op basis van het scherm [!UICONTROL Create Criteria Sequence] .

Er zijn meerdere manieren om het [!UICONTROL Create Criteria Sequence] -scherm te bereiken. Sommige schermopties variëren afhankelijk van de manier waarop u het scherm bereikt.

* Klik in het scherm **[!UICONTROL Recommendations]** > **[!UICONTROL Criteria]** Bibliotheek op **[!UICONTROL Create Criteria]** > **[!UICONTROL Create Criteria Sequence]** . De criteria die u hier maakt, worden automatisch beschikbaar gesteld voor alle [!UICONTROL Recommendations] -activiteiten.
* Wanneer u een [!UICONTROL Recommendations] -activiteit maakt, klikt u in het scherm Criteria selecteren op **[!UICONTROL Create New]** > **[!UICONTROL Create Criteria Sequence]** . U kunt de nieuwe reeks criteria opslaan voor gebruik met andere [!UICONTROL Recommendations] -activiteiten.
* Wanneer u een [!UICONTROL Recommendations] -activiteit bewerkt, klikt u in een [!UICONTROL Recommendations Location] -vak op de pagina en selecteert u vervolgens **[!UICONTROL Change Criteria]** . Klik in het [!UICONTROL Select Criteria] -scherm op **[!UICONTROL Create New]** > **[!UICONTROL Create Criteria Sequence]** . U kunt de nieuwe criteria opslaan voor gebruik met andere [!UICONTROL Recommendations] -activiteiten.

In de volgende stappen wordt ervan uitgegaan dat u het [!UICONTROL Create Criteria Sequence] -scherm opent via de eerste methode: het **[!UICONTROL Recommendations]** > **[!UICONTROL Criteria]** -bibliotheekscherm.

1. Klik op **[!UICONTROL Recommendations]** > **[!UICONTROL Criteria]** .

1. Klik op **[!UICONTROL Create Criteria]** > **[!UICONTROL Create Criteria Sequence]** .

   ![&#x200B; CreateCriteriaSequence beeld &#x200B;](assets/CreateCriteriaSequence.png)

1. Vul de informatie in de [&#x200B; Basisinformatie &#x200B;](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md#info) sectie in.

1. Klik in de sectie **[!UICONTROL Criteria Sequence]** op **[!UICONTROL Add Criteria]** .

   De volgordevolgorde bepaalt de volgorde waarin een ontwerp wordt gevuld. Als Criteria 1 niet genoeg aanbevelingen heeft om uw ontwerp te vullen, zullen de resterende groeven met Criteria 2 worden gevuld, etc.

   ![&#x200B; voegt Criteria &#x200B;](/help/main/c-recommendations/c-algorithms/assets/add-criteria.png) toe

1. Selecteer een criterium in het scherm [!UICONTROL Select Criteria] en klik op **[!UICONTROL Add]** .

   U kunt het vakje van het Onderzoek en de filterdrop-down gebruiken om de gewenste criteria te vinden.

   ![&#x200B; Uitgezochte criteria &#x200B;](/help/main/c-recommendations/c-algorithms/assets/select-criteria.png)

1. (Optioneel) Sleep de schakeloptie **[!UICONTROL Limit the number of items returned]** naar de positie &quot;aan&quot; en geef vervolgens het aantal items op (tussen 1 en 50).

   ![&#x200B; Beperk het aantal punten teruggekeerde knevel &#x200B;](/help/main/c-recommendations/c-algorithms/assets/limit-number.png)

   Houd rekening met de volgende gebruiksgevallen om u te helpen de waarde van de optie [!UICONTROL Limit the number of items returned] te begrijpen (ook wel &#39;&#39;besturingselement voor sleufniveau&#39;&#39; genoemd):

   * **Geval 1 van het Gebruik**: U wilt een mengeling van verschillende soorten punten in één enkele aanbevelingen laden hebben. U wilt bijvoorbeeld een combinatie van bovenkleding (jassen) en toppen (overhemden, T-shirts) weergeven. Om dit te bereiken, gebruik een Inzameling voor de activiteit die alle potentiële producttypes omvat u in om het even welke groeven in uw ontwerp wilt. Stel vervolgens de eerste criteria in met een statisch filter dat de criteria beperkt tot het opnemen van alleen bovenkleding, en stel de tweede criteria in met een statisch filter dat de criteria beperkt tot alleen bovenkanten. Ten slotte kunt u beide criteria toevoegen aan een reeks criteria en de eerste criteria beperken tot twee sleuven.

     De aanbevolen lade kan er op uw site als volgt uitzien:

     ![&#x200B; Aanbevolen de aanbevelingen van Producten het dienblad &#x200B;](/help/main/c-recommendations/c-algorithms/assets/featured-products.png)

   * **Geval 2 van het Gebruik**: U wilt een mengeling van zowel alternatieve punten als complementaire punten. Stel één criterium in om een weergegeven/weergegeven algoritme te gebruiken en gebruik een dynamisch filter dat de aanbevolen items beperkt tot de categorie van het huidige item. Stel de tweede criteria in om een weergegeven/gekocht algoritme te gebruiken en gebruik een dynamisch filter dat alleen aanbevolen items bevat die niet overeenkomen met de categorie van het huidige item. Ten slotte kunt u beide criteria toevoegen aan een reeks en de eerste criteria beperken tot twee sleuven.

1. Voeg aanvullende criteria aan uw reeks toe. U kunt maximaal vijf criteria toevoegen aan een reeks.

1. Laat [&#x200B; de opties van de ReserveInhoud &#x200B;](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md#content) toe.

1. Klik op **[!UICONTROL Save]**.

   De opeenvolging van criteria zal in de lijst van Criteria verschijnen.

   Voor meer informatie over de opties van de aanbeveling logica, zie [&#x200B; Criteria &#x200B;](/help/main/c-recommendations/c-algorithms/algorithms.md).

## De video van de opleiding: Creeer criteria in Aanbevelingen (12 :33) ![&#x200B; badge van het Leerprogramma &#x200B;](/help/main/assets/tutorial.png)

Deze video bevat de volgende informatie:

* Criteria maken
* Criteria-reeksen maken
* Aangepaste criteria uploaden

>[!VIDEO](https://video.tv.adobe.com/v/27694?quality=12)
