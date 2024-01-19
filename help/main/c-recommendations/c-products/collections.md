---
keywords: verzameling;gericht
description: Leer hoe u verzamelingen in Adobe kunt gebruiken [!DNL Target] Recommendations. Een verzameling is een reeks producten of items die in aanmerking komen voor een aanbeveling.
title: Hoe gebruik ik verzamelingen in Recommendations-activiteiten?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Zie wat er in Target Premium is opgenomen."
feature: Recommendations
exl-id: e62f501b-3521-4456-9ea1-e4b8a2b478c6
source-git-commit: fe1e97710e7692ba7724103853ed7438c3f361b1
workflow-type: tm+mt
source-wordcount: '862'
ht-degree: 0%

---

# Verzamelingen

Een verzameling is een reeks producten of items die in aanmerking komen voor een aanbeveling. Een verzameling wordt gedefinieerd door de voorwaarden op te geven waaraan items moeten voldoen om deel uit te maken van de verzameling.

Een verzameling is doorgaans een set van vergelijkbare of verwante items, zoals één productverzameling. U kunt echter de objecten groeperen in een categorie die voor uw bedrijf zinvol is, zoals producten in een bepaald prijsbereik of een bepaalde kleur, of objecten die in een bepaald geografisch gebied interessant kunnen zijn.

Gebruik verzamelingen om uw producten in logische emmers te ordenen. Als sommige items bijvoorbeeld beschikbaar zijn in een bepaalde regio, maar niet in een andere regio, kunt u een verzameling maken waarin items worden uitgesloten die niet beschikbaar zijn in de regio van de bezoeker. U kunt ook verzamelingen gebruiken om seizoensgebonden items te ordenen, of andere organisatorische parameters die van toepassing zijn op uw bedrijf.

De [aanbevelingen voor back-up](/help/main/c-recommendations/c-algorithms/backup-recs.md) die voor elke criteria binnen de aanbeveling worden geproduceerd gebruikt ook deze inzameling, zodat slechts de punten in de inzameling in de reserveaanbeveling worden opgenomen. Met inzamelingen, kunt u zeker zijn dat slechts de producten die steek houden om in een plaats te tonen worden getoond.

De inzamelingen worden herbouwd of bijgewerkt telkens als elke criteria loopt.

U kunt uw items groeperen in catalogi en vervolgens voor elke verzameling afzonderlijke aanbevelingen maken.

Met inclusiecriteria kunt u vergelijkbare dingen doen als een verzameling, maar deze moeten altijd worden ingesteld wanneer u een activiteit maakt. Met verzamelingen kunt u één keer een set items maken en deze gebruiken wanneer dat nodig is, zonder dat u de set opnieuw hoeft in te stellen.

Wanneer u een [!DNL Recommendations] activiteit, verschijnt de inzamelingsnaam naast [!UICONTROL Criteria] label op het activiteitendiagram.

>[!NOTE]
>
>Verzamelingen worden niet toegepast bij gebruik van de [!UICONTROL Recently Viewed Items] aanbevelingen.

## Een verzameling maken {#task_1256DFF6842141FCAADD9E1428EF7F08}

Maak een verzameling om de producten of inhoud te ordenen die u wilt weergeven in uw aanbevelingen.

1. Klikken **[!UICONTROL Recommendations]** > **[!UICONTROL Collections]** om de lijst met bestaande verzamelingen weer te geven.

   ![Verzamelingslijst](assets/collections_list.png)

   De [!UICONTROL Collections] wordt een lijst met uw bestaande verzamelingen weergegeven. U maakt nieuwe verzamelingen door op de knop [!UICONTROL Create Collection] knop. U kunt ook bestaande verzamelingen bewerken, kopiëren en verwijderen door de muisaanwijzer boven de gewenste verzameling te plaatsen en op het gewenste pictogram te klikken.

   ![Pictogrammen voor aanwijzen: bewerken, kopiëren en verwijderen](/help/main/c-recommendations/c-products/assets/hover-icons.png)

   Het &quot;aantal items&quot; dat voor elke verzameling op het [!UICONTROL Collections] lijstmening is het aantal producten die de regels voor die inzameling binnen gevormde gebrek Recommendations aanpassen [hostgroep](/help/main/administrating-target/hosts.md) (milieu). Zie [Instellingen](https://experienceleague.adobe.com/docs/target-dev/developer/recommendations.html){target=_blank} om de standaardgastheergroep te veranderen.

1. Klik op **[!UICONTROL Create Collection]**.

1. (Voorwaardelijk) Kies een omgeving in het menu **[!UICONTROL Environment]** filter tijdens het maken (of bijwerken) van een verzameling om de inhoud van de verzameling in die omgeving voor te vertonen. Standaard worden de resultaten van de standaardhostgroep weergegeven.

   ![Verzameling maken](/help/main/c-recommendations/c-products/assets/CreateCollection.png)

1. Typ a **[!UICONTROL Name]** voor de verzameling.

   U kunt ook een optionele **[!UICONTROL Description]**.

1. Plaats de regels die worden gebruikt om de inzameling te bouwen.

   Uw verzameling kan bijvoorbeeld rond een product-id of een categorie, marge of een andere parameter in de lijst worden gemaakt.

   U kunt regels toevoegen om meerdere parameters te gebruiken om een verzameling te definiëren. De veelvoudige regels worden aangesloten bij een exploitant AND. De verzameling kan alleen worden toegepast als alle opgegeven regels overeenkomen.

1. Klik op **[!UICONTROL Save]**.

## Een verzameling maken met Geavanceerd zoeken

U kunt ook verzamelingen maken met Geavanceerd zoeken op het tabblad [Catalogus zoeken](/help/main/c-recommendations/c-products/catalog-search.md#save-as) pagina ([!UICONTROL Recommendations] > [!UICONTROL Catalog Search] > [!UICONTROL Advanced Search]).

![Opslaan als dialoogvenster](/help/main/c-recommendations/c-products/assets/save-as.png)

Nadat u een zoekopdracht hebt gemaakt met &#39;id > contains&#39;, kunt u bijvoorbeeld op [!UICONTROL Save As] > [!UICONTROL Collection].

>[!IMPORTANT]
>
>De functie Geavanceerd zoeken is niet hoofdlettergevoelig. Producten die op het moment van levering worden geretourneerd, zijn echter gebaseerd op hoofdlettergevoelige zoekopdrachten. Deze wanverhouding kan tot verwarring leiden. Zorg ervoor dat u rekening houdt met hoofdlettergevoeligheid wanneer u verzamelingen maakt op basis van resultaten met de functie Geavanceerd zoeken. Als u bijvoorbeeld zoekt naar &#39;Vakantie&#39;, worden in de eerste zoekopdracht resultaten weergegeven die &#39;Vakantie&#39; en &#39;Vakantie&#39; bevatten. Als u vervolgens een catalogus maakt met de intentie om producten met &quot;vakantie&quot; te retourneren, worden alleen producten met &quot;vakantie&quot; geretourneerd. Producten met &quot;Vakantie&quot; worden niet geretourneerd.

## Een verzameling bewerken, kopiëren of verwijderen

Houd de muisaanwijzer boven de gewenste verzameling in de lijst en klik op het juiste pictogram: bewerken, kopiëren of verwijderen.

![Pictogrammen voor het aanwijzen van een verzameling](/help/main/c-recommendations/c-products/assets/hover-collections.png)

U kunt een bestaande verzameling kopiëren om een dubbele verzameling te maken die u vervolgens kunt wijzigen. Hierdoor kunt u een vergelijkbare uitsluiting maken met minder moeite.

Houd er rekening mee dat verzamelingen beschikbaar zijn voor de gehele account. Zorg ervoor dat u hiermee rekening houdt voordat u een verzameling verwijdert. Verwijderde verzamelingen kunnen niet worden hersteld.

## Een verzameling in een Recommendations-activiteit gebruiken

1. Maak een verzameling met een van de bovenstaande methoden.

1. Klikken **[!UICONTROL Activities]** en [een nieuwe Recommendations maken](/help/main/c-recommendations/t-create-recs-activity/create-recs-activity.md) of een bestaande activiteit bewerken.

1. Nadat u een criterium en een ontwerp hebt geselecteerd, [!UICONTROL Options] worden weergegeven als u de gewenste verzameling hebt geselecteerd.

   ![Verzamelingsoptie kiezen](/help/main/c-recommendations/c-products/assets/choose-collection.png)

1. (Voorwaardelijk) Om een bestaande inzameling te veranderen die, op **[!UICONTROL Experiences]** pagina (stap 2 van de driedelige geleide workflow), klik op een locatie waar u aanbevelingen hebt gedaan en klik op **[!UICONTROL Change Collection]** Selecteer vervolgens de gewenste verzameling.

   ![Verzameling wijzigen, optie](/help/main/c-recommendations/c-products/assets/change-collection.png)

## Trainingsvideo: Verzamelingen en uitsluitingen maken in Recommendations (7:05) ![Zelfstudie-badge](/help/main/assets/tutorial.png)

Deze video bevat de volgende informatie:

* Een verzameling maken
* Een uitsluiting maken

>[!VIDEO](https://video.tv.adobe.com/v/27689)
