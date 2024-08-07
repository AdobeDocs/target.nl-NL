---
keywords: verzameling;gericht
description: Leer hoe u verzamelingen van producten of objecten kunt gebruiken in [!DNL Target Recommendations].
title: Hoe gebruik ik verzamelingen in Recommendations-activiteiten?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Zie wat er in Target Premium is opgenomen."
feature: Recommendations
hide: true
hidefromtoc: true
source-git-commit: 31cf23a52c331eabad0e5f6423eeeca84df87625
workflow-type: tm+mt
source-wordcount: '707'
ht-degree: 0%

---

# Verzamelingen

Een verzameling is een reeks producten of items die in aanmerking komen voor een aanbeveling. Een verzameling wordt gedefinieerd door de voorwaarden op te geven waaraan items moeten voldoen om deel uit te maken van de verzameling.

Een verzameling is doorgaans een set van vergelijkbare of verwante items, zoals één productverzameling. U kunt echter de objecten groeperen in een categorie die voor uw bedrijf zinvol is, zoals producten in een bepaald prijsbereik of een bepaalde kleur, of objecten die in een bepaald geografisch gebied interessant kunnen zijn.

Gebruik verzamelingen om uw producten in logische emmers te ordenen. Als sommige items bijvoorbeeld beschikbaar zijn in een bepaalde regio, maar niet in een andere regio, kunt u een verzameling maken waarin items worden uitgesloten die niet beschikbaar zijn in de regio van de bezoeker. U kunt ook verzamelingen gebruiken om seizoensgebonden items te ordenen, of andere organisatorische parameters die van toepassing zijn op uw bedrijf.

[Aanbevelingen voor back-up](/help/main/c-recommendations/c-algorithms/backup-recs.md) Deze verzameling wordt ook gebruikt voor alle criteria in de aanbeveling, zodat alleen de items in de verzameling worden opgenomen in de back-upaanbeveling. Met inzamelingen, kunt u zeker zijn dat slechts de producten die steek houden om in een plaats te tonen worden getoond.

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

   ![Verzamelingslijst](assets/collections-list.png)

   De [!UICONTROL Collections] wordt een lijst met uw bestaande verzamelingen weergegeven. U maakt nieuwe verzamelingen door op de knop [!UICONTROL Create Collection] knop. U kunt bestaande verzamelingen ook bewerken, kopiëren en verwijderen door op het pictogram met de ellips naast de gewenste verzameling te klikken en vervolgens op de gewenste optie te klikken.

   Het &quot;aantal items&quot; dat voor elke verzameling op het [!UICONTROL Collections] lijstmening is het aantal producten die de regels voor die inzameling binnen gevormde gebrek Recommendations aanpassen [hostgroep](/help/main/administrating-target/hosts.md) (milieu). Zie [Instellingen](https://experienceleague.adobe.com/docs/target-dev/developer/recommendations.html){target=_blank} om de standaardgastheergroep te veranderen.

1. Klik op **[!UICONTROL Create Collection]**.

   ![Verzameling maken](/help/main/c-recommendations/c-products/assets/create-collection.png)

1. Typ a **[!UICONTROL Name]** voor de verzameling.

   U kunt ook een optionele **[!UICONTROL Description]**.

1. (Voorwaardelijk) Kies een [milieu](/help/main/administrating-target/environments.md) van de **[!UICONTROL Environment]** filter tijdens het maken (of bijwerken) van een verzameling om de inhoud van de verzameling in die omgeving voor te vertonen. Standaard worden de resultaten van de standaardhostgroep weergegeven.

1. Plaats de regels die worden gebruikt om de inzameling te bouwen.

   Uw verzameling kan bijvoorbeeld rond een product-id of een categorie, marge of een andere parameter in de lijst worden gemaakt.

   U kunt regels toevoegen om meerdere parameters te gebruiken om een verzameling te definiëren. De veelvoudige regels worden aangesloten bij een exploitant AND. De verzameling kan alleen worden toegepast als alle opgegeven regels overeenkomen.

1. Klik op **[!UICONTROL Create]**.

<!-- ## Create a collection using [!UICONTROL Advanced Search]

You can also create collections using [!UICONTROL Advanced Search] on the [Catalog Search](/help/main/c-recommendations/c-products/catalog-search.md#save-as) page ([!UICONTROL Recommendations] > [!UICONTROL Catalog Search] > [!UICONTROL Advanced Search]). 

![Save as dialog](/help/main/c-recommendations/c-products/assets/save-as.png)

After creating a search using "id > contains," for example, you can then click [!UICONTROL Save As] > [!UICONTROL Collection].

>[!IMPORTANT]
>
>The [!UICONTROL Advanced Search] functionality is case-insensitive; however, products returned at the time of delivery are based on case-sensitive search. This mismatch might lead to confusion. Ensure that you consider case-sensitivity when you create collections based on results using the [!UICONTROL Advanced Search] functionality. For example, if you perform a search for "Holiday," that initial search lists results containing "Holiday" and "holiday." If you then create a catalog with the intent to return products containing "holiday," only products containing "holiday" are returned. Products containing "Holiday" are not returned. -->

## Een verzameling bewerken, kopiëren of verwijderen

Klik op de knop **weglatingsteken** klikt u op het betreffende pictogram naast de gewenste verzameling in de lijst: bewerken, kopiëren of verwijderen.

![Pictogrammen voor aanwijzen: bewerken, kopiëren en verwijderen](/help/main/c-recommendations/c-products/assets/hover-icons-new.png)

U kunt een bestaande verzameling kopiëren om een dubbele verzameling te maken die u vervolgens kunt wijzigen. Zo kunt u een vergelijkbare verzameling maken met minder moeite.

Houd er rekening mee dat verzamelingen beschikbaar zijn voor de gehele account. Zorg ervoor dat u hiermee rekening houdt voordat u een verzameling verwijdert. Verwijderde verzamelingen kunnen niet worden hersteld.

## Een verzameling in een [!DNL Recommendations] activiteit

1. Maak een verzameling met een van de bovenstaande methoden.

1. Klikken **[!UICONTROL Activities]** en [een nieuwe Recommendations maken](/help/main/c-recommendations/t-create-recs-activity/create-recs-activity.md) of een bestaande activiteit bewerken.

1. Nadat u een criterium en een ontwerp hebt geselecteerd, [!UICONTROL Options] De pagina wordt weergegeven waar u de gewenste verzameling selecteert.

   ![Verzamelingsoptie kiezen](/help/main/c-recommendations/c-products/assets/choose-collection.png)

1. (Voorwaardelijk) Om een bestaande inzameling te veranderen die, op **[!UICONTROL Experiences]** pagina (stap 2 van de driedelige geleide workflow), klik op een locatie waar u aanbevelingen hebt gedaan en klik op **[!UICONTROL Change Collection]** Selecteer vervolgens de gewenste verzameling.

   ![Verzameling wijzigen, optie](/help/main/c-recommendations/c-products/assets/change-collection.png)