---
keywords: collection;Targeting
description: Een verzameling is een reeks producten of objecten in Adobe Target die in aanmerking komen voor een aanbeveling.
title: Verzamelingen in Adobe Target
feature: entities
translation-type: tm+mt
source-git-commit: 968d36d65016e51290f6bf754f69c91fd8f68405
workflow-type: tm+mt
source-wordcount: '839'
ht-degree: 0%

---


# ![](/help/assets/premium.png) PREMIUMCollections  {#collections}

Een verzameling is een reeks producten of items die in aanmerking komen voor een aanbeveling. Een verzameling wordt gedefinieerd door de voorwaarden op te geven waaraan items moeten voldoen om deel uit te maken van de verzameling.

Een verzameling is doorgaans een set van vergelijkbare of verwante items, zoals één productverzameling. U kunt echter de objecten groeperen in een categorie die voor uw bedrijf zinvol is, zoals producten in een bepaald prijsbereik of een bepaalde kleur, of objecten die in een bepaald geografisch gebied interessant kunnen zijn.

Gebruik verzamelingen om uw producten in logische emmers te ordenen. Als sommige items bijvoorbeeld beschikbaar zijn in een bepaalde regio, maar niet in een andere regio, kunt u een verzameling maken waarin items worden uitgesloten die niet beschikbaar zijn in de regio van de bezoeker. U kunt ook verzamelingen gebruiken om seizoensgebonden items te ordenen, of andere organisatorische parameters die van toepassing zijn op uw bedrijf.

De [back-upaanbevelingen](/help/c-recommendations/c-algorithms/backup-recs.md) die voor elke criteria in de aanbeveling worden gegenereerd, gebruiken deze verzameling ook. Alleen items in de verzameling worden dus opgenomen in de back-upaanbeveling. Met inzamelingen, kunt u zeker zijn dat slechts de producten die steek houden om in een plaats te tonen worden getoond.

De inzamelingen worden herbouwd of bijgewerkt telkens als elke criteria loopt.

U kunt uw items groeperen in catalogi en vervolgens voor elke verzameling afzonderlijke aanbevelingen maken.

Met inclusiecriteria kunt u vergelijkbare dingen doen als een verzameling, maar deze moeten altijd worden ingesteld wanneer u een activiteit maakt. Met verzamelingen kunt u één keer een set items maken en deze gebruiken wanneer dat nodig is, zonder dat u de set opnieuw hoeft in te stellen.

Wanneer u een [!DNL Recommendations] activiteit creeert of uitgeeft, verschijnt de inzamelingsnaam naast het [!UICONTROL Criteria] etiket op het activiteitendiagram.

>[!NOTE]
>
>Verzamelingen worden niet toegepast wanneer u de [!UICONTROL Recently Viewed Items]-aanbevelingen gebruikt.

## Een verzameling maken {#task_1256DFF6842141FCAADD9E1428EF7F08}

Maak een verzameling om de producten of inhoud te ordenen die u wilt weergeven in uw aanbevelingen.

1. Klik **[!UICONTROL Recommendations]** > **[!UICONTROL Collections]** om de lijst van bestaande inzamelingen te tonen.

   ![Verzamelingslijst](assets/collections_list.png)

   De [!UICONTROL Collections] pagina toont een lijst van uw bestaande inzamelingen. U maakt nieuwe verzamelingen door op de knop [!UICONTROL Create Collection] te klikken. U kunt ook bestaande verzamelingen bewerken, kopiëren en verwijderen door de muisaanwijzer boven de gewenste verzameling te plaatsen en op het gewenste pictogram te klikken.

   ![Aanwijspictogrammen: bewerken, kopiëren en verwijderen](/help/c-recommendations/c-products/assets/hover-icons.png)

   Het &quot;Aantal Punten&quot;voor elke inzameling op [!UICONTROL Collections] lijstmening wordt gemeld is het aantal producten die de regels voor die inzameling binnen het gevormde gebrek Recommendations [gastheergroep](/help/administrating-target/hosts.md) (milieu) aanpassen. Zie [Instellingen](/help/c-recommendations/plan-implement.md#concept_C1E1E2351413468692D6C21145EF0B84) om de standaardhostgroep te wijzigen.

1. Klik op **[!UICONTROL Create Collection]**.

1. (Voorwaardelijk) Kies een milieu van het **[!UICONTROL Environment]** filter terwijl het creëren van (of het bijwerken van) een inzameling om de inhoud van de inzameling in die milieu te voorproef. Standaard worden de resultaten van de standaardhostgroep weergegeven.

   ![Verzameling maken](/help/c-recommendations/c-products/assets/CreateCollection.png)

1. Typ een **[!UICONTROL Name]** voor de verzameling.

   U kunt ook een optionele **[!UICONTROL Description]** invoeren.

1. Plaats de regels die worden gebruikt om de inzameling te bouwen.

   Uw verzameling kan bijvoorbeeld rond een product-id of een categorie, marge of een andere parameter in de lijst worden gemaakt.

   U kunt regels toevoegen om meerdere parameters te gebruiken om een verzameling te definiëren. De veelvoudige regels worden aangesloten bij een exploitant AND. De verzameling kan alleen worden toegepast als alle opgegeven regels overeenkomen.

1. Klik op **[!UICONTROL Save]**.

## Een verzameling maken met Geavanceerd zoeken

U kunt ook verzamelingen maken met Geavanceerd zoeken op de pagina [Cataloguszoekopdracht](/help/c-recommendations/c-products/catalog-search.md#save-as) ([!UICONTROL Recommendations] > [!UICONTROL Catalog Search] > [!UICONTROL Advanced Search]).

![Opslaan als dialoogvenster](/help/c-recommendations/c-products/assets/save-as.png)

Nadat u een zoekopdracht hebt gemaakt met &#39;id > contains&#39;, kunt u bijvoorbeeld op [!UICONTROL Save As] > [!UICONTROL Collection] klikken.

>[!IMPORTANT]
>
>De functie Geavanceerd zoeken is niet hoofdlettergevoelig. producten die op het tijdstip van levering worden geretourneerd, zijn echter gebaseerd op hoofdlettergevoelige zoekopdrachten. Deze wanverhouding kan tot verwarring leiden. Zorg ervoor dat u rekening houdt met hoofdlettergevoeligheid wanneer u verzamelingen maakt op basis van resultaten met de functie Geavanceerd zoeken. Als u bijvoorbeeld zoekt naar &#39;Vakantie&#39;, worden in de eerste zoekopdracht resultaten weergegeven die &#39;Vakantie&#39; en &#39;Vakantie&#39; bevatten. Als u vervolgens een catalogus maakt met de bedoeling producten met &quot;vakantie&quot; terug te sturen, worden alleen producten met &quot;vakantie&quot; geretourneerd. Producten met &quot;Vakantie&quot; worden niet geretourneerd.

## Een verzameling bewerken, kopiëren of verwijderen

Houd de muisaanwijzer boven de gewenste verzameling in de lijst en klik op het juiste pictogram: bewerken, kopiëren of verwijderen.

![Pictogrammen voor het aanwijzen van een verzameling](/help/c-recommendations/c-products/assets/hover-collections.png)

U kunt een bestaande verzameling kopiëren om een dubbele verzameling te maken die u vervolgens kunt wijzigen. Hierdoor kunt u een vergelijkbare uitsluiting maken met minder moeite.

Houd er rekening mee dat verzamelingen beschikbaar zijn voor de gehele account. Zorg ervoor dat u hiermee rekening houdt voordat u een verzameling verwijdert. Verwijderde verzamelingen kunnen niet worden hersteld.

## Een verzameling in een Recommendations-activiteit gebruiken

1. Maak een verzameling met een van de bovenstaande methoden.

1. Klik op **[!UICONTROL Activities]** en [om een nieuwe Recommendations](/help/c-recommendations/t-create-recs-activity/create-recs-activity.md)-activiteit te maken of een bestaande activiteit te bewerken.

1. Nadat u een criterium en een ontwerp hebt geselecteerd, wordt de pagina [!UICONTROL Options] weergegeven als u de gewenste verzameling selecteert.

   ![Verzamelingsoptie kiezen](/help/c-recommendations/c-products/assets/choose-collection.png)

1. (Voorwaardelijk) om een bestaande inzameling te veranderen die, op **[!UICONTROL Experiences]** pagina (stap 2 van de driedelige geleide werkschema) plaatst, klik een plaats waar u aanbevelingen plaatste, **[!UICONTROL Change Collection]** klikt, dan de gewenste inzameling selecteert.

   ![Verzameling wijzigen, optie](/help/c-recommendations/c-products/assets/change-collection.png)

## Trainingsvideo: Verzamelingen en uitsluitingen maken in Recommendations (7:05) ![Zelfstudie-badge](/help/assets/tutorial.png)

Deze video bevat de volgende informatie:

* Een verzameling maken
* Een uitsluiting maken

>[!VIDEO](https://video.tv.adobe.com/v/27689)