---
keywords: verzameling;gericht
description: Leer hoe te om inzamelingen van producten of punten in  [!DNL Target Recommendations] te gebruiken.
title: Hoe gebruik ik verzamelingen in aanbevelingen?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=nl-NL#premium newtab=true" tooltip="Kijk wat er in Target Premium is opgenomen."
feature: Recommendations
exl-id: e62f501b-3521-4456-9ea1-e4b8a2b478c6
source-git-commit: be9cb6da17f125c127d64ed8f9002987188fdf3d
workflow-type: tm+mt
source-wordcount: '716'
ht-degree: 0%

---

# Verzamelingen

Een verzameling is een reeks producten of items die in aanmerking komen voor een aanbeveling. Een verzameling wordt gedefinieerd door de voorwaarden op te geven waaraan items moeten voldoen om deel uit te maken van de verzameling.

Een verzameling is doorgaans een set van vergelijkbare of verwante items, zoals één productverzameling. U kunt echter de objecten groeperen in een categorie die voor uw bedrijf zinvol is, zoals producten in een bepaald prijsbereik of een bepaalde kleur, of objecten die in een bepaald geografisch gebied interessant kunnen zijn.

Gebruik verzamelingen om uw producten in logische emmers te ordenen. Als sommige items bijvoorbeeld beschikbaar zijn in een bepaalde regio, maar niet in een andere regio, kunt u een verzameling maken waarin items worden uitgesloten die niet beschikbaar zijn in de regio van de bezoeker. U kunt ook verzamelingen gebruiken om seizoensgebonden items te ordenen, of andere organisatorische parameters die van toepassing zijn op uw bedrijf.

[&#x200B; Van de Steun aanbevelingen &#x200B;](/help/main/c-recommendations/c-algorithms/backup-recs.md) die voor elke criteria binnen de aanbeveling worden geproduceerd gebruiken ook deze inzameling, zodat slechts zijn de punten in de inzameling inbegrepen in de reserveaanbeveling. Met inzamelingen, kunt u zeker zijn dat slechts de producten die steek houden om in een plaats te tonen worden getoond.

De inzamelingen worden herbouwd of bijgewerkt telkens als elke criteria loopt.

U kunt uw items groeperen in catalogi en vervolgens voor elke verzameling afzonderlijke aanbevelingen maken.

Met inclusiecriteria kunt u vergelijkbare dingen doen als een verzameling, maar deze moeten altijd worden ingesteld wanneer u een activiteit maakt. Met verzamelingen kunt u één keer een set items maken en deze gebruiken wanneer dat nodig is, zonder dat u de set opnieuw hoeft in te stellen.

Wanneer u een [!DNL Recommendations] -activiteit maakt of bewerkt, wordt de naam van de verzameling weergegeven naast het label [!UICONTROL Criteria] in het activiteitendiagram.

>[!NOTE]
>
>* De regels van de inzameling zijn op aanbeveling punten van toepassing die na de criteria in werking worden gesteld. Zij beïnvloeden slechts de Aanbevelingen van de Entiteit (ERs) in de output, niet de sleutel.
>
>* Verzamelingen worden niet toegepast wanneer u de [!UICONTROL Recently Viewed Items] aanbeveling-toets gebruikt.

## Een verzameling maken {#task_1256DFF6842141FCAADD9E1428EF7F08}

Maak een verzameling om de producten of inhoud te ordenen die u wilt weergeven in uw aanbevelingen.

1. Klik op **[!UICONTROL Recommendations]** > **[!UICONTROL Collections]** om de lijst met bestaande verzamelingen weer te geven.

   Op de pagina [!UICONTROL Collections] wordt een lijst met uw bestaande verzamelingen weergegeven. U maakt nieuwe verzamelingen door op de knop [!UICONTROL Create Collection] te klikken. U kunt, bestaande inzamelingen ook uitgeven kopiëren en schrappen door het Meer pictogram van Acties ( ![&#x200B; Meer pictogram van Acties &#x200B;](/help/main/assets/icons/MoreSmallList.svg)) naast de gewenste inzameling te klikken en dan door de gewenste optie te klikken.

   Het &quot;Aantal Punten&quot;voor elke inzameling op de [!UICONTROL Collections] lijstmening wordt gemeld is het aantal producten die de regels voor die inzameling aanpassen binnen de gevormde standaardgroep van Aanbevelingen [&#128279;](/help/main/administrating-target/hosts.md) (milieu). Zie [&#x200B; Montages &#x200B;](https://experienceleague.adobe.com/docs/target-dev/developer/recommendations.html?lang=nl-NL){target=_blank} om de standaardgastheergroep te veranderen.

1. Klik op **[!UICONTROL Create Collection]**.

1. Typ een **[!UICONTROL Name]** voor de verzameling.

   U kunt ook een optionele **[!UICONTROL Description]** invoeren.

1. (Voorwaardelijk) kies een [&#x200B; milieu &#x200B;](/help/main/administrating-target/environments.md) van de **[!UICONTROL Environment]** filter terwijl het creëren van (of het bijwerken) een inzameling om de inhoud van de inzameling in dat milieu voor te vertonen. Standaard worden de resultaten van de standaardhostgroep weergegeven.

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

Klik ( ![&#x200B; Meer pictogram van Acties &#x200B;](/help/main/assets/icons/MoreSmallList.svg)) naast de gewenste inzameling in de lijst, dan klik het aangewezen pictogram: [!UICONTROL Edit], [!UICONTROL Copy], of [!DNL Delete].

U kunt een bestaande verzameling kopiëren om een dubbele verzameling te maken die u vervolgens kunt wijzigen. Zo kunt u een vergelijkbare verzameling maken met minder moeite.

Houd er rekening mee dat verzamelingen beschikbaar zijn voor de gehele account. Zorg ervoor dat u hiermee rekening houdt voordat u een verzameling verwijdert. Verwijderde verzamelingen kunnen niet worden hersteld.

## Een verzameling gebruiken in een [!DNL Recommendations] -activiteit

1. Maak een verzameling met een van de bovenstaande methoden.

1. Klik **[!UICONTROL Activities]** en [&#x200B; creeer een nieuwe activiteit van Aanbevelingen &#x200B;](/help/main/c-recommendations/t-create-recs-activity/create-recs-activity.md) of geef een bestaande activiteit uit.

1. Nadat u criteria en een ontwerp hebt geselecteerd, wordt de pagina [!UICONTROL Options] weergegeven op de plaats waar u de gewenste verzameling hebt geselecteerd.

1. (Voorwaardelijk) Als u een bestaande verzamelingsinstelling wilt wijzigen, klikt u op de pagina **[!UICONTROL Experiences]** (stap 1 van de geleide workflow met drie delen) op de locatie waar u de aanbevelingen hebt geplaatst, klikt u op **[!UICONTROL Change Collection]** en selecteert u de gewenste verzameling.
