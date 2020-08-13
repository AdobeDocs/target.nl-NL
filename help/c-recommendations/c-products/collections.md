---
keywords: collection;Targeting
description: Een verzameling is een reeks producten of objecten in Adobe Target die in aanmerking komen voor een aanbeveling.
title: Verzamelingen in Adobe Target
feature: entities
uuid: aa1afdcf-e51c-4e44-a229-3c21fc9d0514
translation-type: tm+mt
source-git-commit: 3cf1f4fa56f86c106dccdc2c97c080c17c3982b4
workflow-type: tm+mt
source-wordcount: '617'
ht-degree: 0%

---


# ![PREMIUM](/help/assets/premium.png) Collections {#collections}

Een verzameling is een reeks producten of items die in aanmerking komen voor een aanbeveling.

Een verzameling is doorgaans een set van vergelijkbare of verwante items, zoals één productverzameling. U kunt echter de objecten groeperen in een categorie die voor uw bedrijf zinvol is, zoals producten met een bepaalde prijs of kleur, of items die in een bepaald geografisch gebied interessant kunnen zijn.

Gebruik verzamelingen om uw producten in logische emmers te ordenen. Als sommige items bijvoorbeeld beschikbaar zijn in een bepaald gebied maar niet in een ander gebied, wilt u wellicht een verzameling maken waarin items worden uitgesloten die niet beschikbaar zijn in het gebied van de bezoeker. U kunt ook verzamelingen gebruiken om seizoensgebonden items te ordenen, of andere organisatorische parameters die van toepassing zijn op uw bedrijf.

De [reserveaanbevelingen](/help/c-recommendations/c-algorithms/backup-recs.md) die voor elke criteria binnen de aanbeveling worden geproduceerd gebruiken ook deze inzameling, zodat worden slechts punten in de inzameling inbegrepen in de reserveaanbeveling. Met inzamelingen, kunt u zeker zijn dat slechts de producten die steek houden om in een plaats te tonen worden getoond.

De inzamelingen worden herbouwd of bijgewerkt telkens als elke criteria loopt.

U kunt uw items groeperen in catalogi en vervolgens voor elke verzameling afzonderlijke aanbevelingen maken.

Met inclusiecriteria kunt u vergelijkbare dingen doen als een verzameling, maar deze moeten altijd worden ingesteld wanneer u een activiteit maakt. Met verzamelingen kunt u één keer een set items maken en deze gebruiken wanneer dat nodig is, zonder dat u de set opnieuw hoeft in te stellen.

Wanneer u een [!DNL Recommendations] activiteit creeert of uitgeeft, verschijnt de inzamelingsnaam naast het [!UICONTROL Criteria] etiket op het activiteitendiagram.

>[!NOTE]
>
>Verzamelingen worden niet toegepast wanneer u de [!UICONTROL Recently Viewed Items] aanbevolen toets gebruikt.

## Een verzameling maken {#task_1256DFF6842141FCAADD9E1428EF7F08}

Maak een verzameling om de producten te ordenen die u in uw aanbevelingen wilt weergeven.

1. Klik **[!UICONTROL Recommendations]** > **[!UICONTROL Collections]** om de lijst met bestaande verzamelingen weer te geven.

   ![Verzamelingslijst](assets/collections_list.png)

   Het &quot;Aantal Punten&quot;voor elke inzameling op de [!UICONTROL Collections] lijstmening wordt gemeld is het aantal producten die de regels voor die inzameling binnen de gevormde standaardRecommendations [gastheergroep](/help/administrating-target/hosts.md) (milieu) aanpassen die. Zie [Instellingen](../../c-recommendations/plan-implement.md#concept_C1E1E2351413468692D6C21145EF0B84) om de standaardhostgroep te wijzigen.

1. Klik op **[!UICONTROL Create Collection]**.

1. (Voorwaardelijk) Kies een omgeving van het **[!UICONTROL Environment]** filter wanneer u een verzameling maakt (of bijwerkt) om een voorvertoning van de inhoud van de verzameling in die omgeving weer te geven. Standaard worden de resultaten van de standaardhostgroep weergegeven.

   ![Verzameling maken](/help/c-recommendations/c-products/assets/CreateCollection.png)

1. Typ een waarde **[!UICONTROL Name]** voor de verzameling.

   U kunt ook een optioneel veld invoeren **[!UICONTROL Description]**.

1. Plaats de regels die worden gebruikt om de inzameling te bouwen.

   Uw verzameling kan bijvoorbeeld rond een product-id of een categorie, marge of een andere parameter in de lijst worden gemaakt.

   U kunt regels toevoegen om meerdere parameters te gebruiken om een verzameling te definiëren. De veelvoudige regels worden aangesloten bij EN. De verzameling kan alleen worden toegepast als alle opgegeven regels overeenkomen.

1. Klik op **[!UICONTROL Save]**.

## Een verzameling maken met Geavanceerd zoeken

U kunt ook verzamelingen maken met Geavanceerd zoeken op de pagina [Catalog Search](/help/c-recommendations/c-products/catalog-search.md) ([!UICONTROL Recommendations] > [!UICONTROL Catalog Search] > [!UICONTROL Advanced Search]).

![Opslaan als dialoogvenster](/help/c-recommendations/c-products/assets/save-as-dialog.png)

Nadat u een zoekopdracht hebt gemaakt met &#39;id > contains&#39;, kunt u bijvoorbeeld op [!UICONTROL Save As] > [!UICONTROL Collection]klikken.

>[!IMPORTANT]
>
>De functie Geavanceerd zoeken is niet hoofdlettergevoelig. producten die op het tijdstip van levering worden geretourneerd, zijn echter gebaseerd op hoofdlettergevoelige zoekopdrachten. Deze wanverhouding kan tot verwarring leiden. Zorg ervoor dat u rekening houdt met hoofdlettergevoeligheid wanneer u verzamelingen maakt op basis van resultaten met de functie Geavanceerd zoeken. Als u bijvoorbeeld zoekt naar &#39;Vakantie&#39;, worden in de eerste zoekopdracht resultaten weergegeven die &#39;Vakantie&#39; en &#39;Vakantie&#39; bevatten. Als u vervolgens een catalogus maakt met de bedoeling producten met &quot;vakantie&quot; terug te sturen, worden alleen producten met &quot;vakantie&quot; geretourneerd. Producten met &quot;Vakantie&quot; worden niet geretourneerd.

## Trainingsvideo: Verzamelingen en uitsluitingen maken in Recommendations (7:05) - ![Zelfstudie](/help/assets/tutorial.png)

Deze video bevat de volgende informatie:

* Een verzameling maken
* Een uitsluiting maken

>[!VIDEO](https://video.tv.adobe.com/v/27689)