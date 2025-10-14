---
keywords: cataloguszoekopdracht;catalogus;zoeken;uitsluiten;verzameling;filter;aanbevelingen
description: Leer hoe te om  [!DNL Recommendations] [!UICONTROL Catalog Search] te gebruiken om van producten of inhoud de plaats te bepalen, punten uit uw catalogus te verwijderen, en meer.
title: Hoe gebruik ik  [!DNL Recommendations] [!UICONTROL Catalog Search]?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=nl-NL#premium newtab=true" tooltip="Kijk wat er in Target Premium is opgenomen."
feature: Recommendations
exl-id: 925fea97-e2c5-4883-84e3-fd357a8ee8d9
source-git-commit: 02ffe8da6cdf96039218656b9690fa719a77910c
workflow-type: tm+mt
source-wordcount: '508'
ht-degree: 0%

---

# [!UICONTROL Catalog Search]

Met de pagina [!UICONTROL Catalog Search] in [!DNL Adobe Recommendations] kunt u de producten of inhoud in uw catalogus vinden. De eenvoudigste taak die u op deze pagina kunt uitvoeren, is het zoeken naar een item. Bovendien kunt u de omgeving wijzigen, facetten filteren, kolommen in de tabel wijzigen, nieuwe zoekfacetten toevoegen en nog veel meer.

De catalogi verwijzen naar uw volledige productreeks (entiteiten). Uw catalogus kan vele inzamelingen bevatten, een manier om uw producten in logische emmers te organiseren.

## Toegang [!UICONTROL Catalog Search]

1. Klik op [!UICONTROL Catalog Search] > **[!UICONTROL Recommendations]** om de pagina **[!UICONTROL Catalog Search]** te openen.

1. (Facultatief) om filters op uw onderzoek toe te passen, klik het **[!UICONTROL Show Filters]** pictogram ( ![&#x200B; toon het pictogram van Filters &#x200B;](/help/main/assets/icons/Filter.svg)). U kunt filteren op [!UICONTROL Environment] , [!UICONTROL Collections] , [!UICONTROL Category] , [!UICONTROL Brand] , [!UICONTROL Inventory] en [!UICONTROL Value] .

## Een eenvoudige zoekopdracht uitvoeren

1. Typ een zoekterm in het veld **[!UICONTROL Search In]** .

1. (Optioneel) U kunt uw zoekopdracht verfijnen door een zoekoptie te selecteren in het optiemenu dat wordt weergegeven wanneer u op de pijl omlaag klikt in het veld [!UICONTROL Search In] .

   Zoekopties zijn onder andere:

   * ID
   * Naam
   * Bericht

1. Blader door de items in de zoekresultaten om miniaturen en andere productinformatie weer te geven.

   >[!NOTE]
   >
   > Wanneer u een cataloguszoekopdracht uitvoert op een aangepast kenmerk met een numerieke waarde, wordt het aangepaste kenmerk in de resultaten behandeld als een tekenreeks in plaats van een numerieke waarde.
   >
   >Er is momenteel geen functionaliteit beschikbaar waarmee u het type van een kenmerk kunt wijzigen. Om een verandering aan te brengen, [&#x200B; open een klantenkwestie &#x200B;](/help/main/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C) van verwijzingen voorzien van de attributen die het type vereisen dat van koord in numeriek wordt veranderd.

<!-- ### Perform an advanced search {#advanced-search}

You can use [!UICONTROL Advanced Search] to further refine your search results or to save your search results as a [collection](/help/main/c-recommendations/c-products/collections.md) or [exclusion](/help/main/c-recommendations/c-products/exclusions.md).

1. Click the **[!UICONTROL Advanced Search]** link.

   ![Advanced Search page](/help/main/c-recommendations/c-products/assets/advances-search.png)

1. Use the drop-down lists to specify the parameter, operator, and values for your search.

1. (Optional) Click **[!UICONTROL Add Rule]** to add an additional search rule.

   Each additional search rule is joined with the AND operator.

1. Click **[!UICONTROL Search]**.

1. (Optional) Click **[!UICONTROL Save As]**, then click **[!UICONTROL Collection]** or **[!UICONTROL Exclusion]**.

   ![Save as options](/help/main/c-recommendations/c-products/assets/save-as.png)

   For more information, see [Create a collection or exclusion based on Advanced Search](#save-as) below.-->

## Details van een object bekijken

U kunt de details van een afzonderlijk item, zoals de id, de naam, het bericht, de categorie en meer, weergeven door de details ervan weer te geven.

1. Klik op een item in de zoekresultaten om de details weer te geven.

## Een item uit de catalogus verwijderen

1. Klik op een item in de zoekresultaten om de details weer te geven.

1. Klik op **[!UICONTROL Remove from Catalog]**.

1. Bevestig dat u het item wilt verwijderen.

Alle informatie over dat item wordt verwijderd uit de catalogusindex. Het item wordt alleen in de catalogus opgenomen als het opnieuw wordt toegevoegd aan een gegevensfeed. Een verwijderd item moet afzonderlijk van feeds worden verwijderd.

## De catalogus vernieuwen

De index van uw catalogus wordt automatisch gecreeerd wanneer u uw eerste voer uploadt, en volgens het [&#x200B; gespecificeerde programma &#x200B;](/help/main/c-recommendations/c-products/feeds.md#steps) verfrist.

De catalogus wordt automatisch vernieuwd wanneer updates worden ontvangen via feed-bestanden, API- of mbox-updates. Updates worden meestal binnen een uur voltooid. Als er updates worden uitgevoerd, wordt de tijd weergegeven waarop de meest recente update is gestart. Als er geen updates worden uitgevoerd, wordt de tijd weergegeven waarop de meest recente update is gestart en voltooid.

<!-- ## Create a collection or exclusion based on Advanced Search {#save-as}

You can create [collections](/help/main/c-recommendations/c-products/collections.md) or [exclusions](/help/main/c-recommendations/c-products/exclusions.md) using [!UICONTROL Advanced Search] on the [!UICONTROL Catalog Search] page ([!UICONTROL Recommendations] > [!UICONTROL Catalog Search] > [!UICONTROL Advanced Search]).

1. Perform an [advanced search](#advanced-search).

1. Click **[!UICONTROL Save As]**, then click **[!UICONTROL Collection]** or **[!UICONTROL Exclusion]**.

   ![Save as options](/help/main/c-recommendations/c-products/assets/save-as.png)

   >[!IMPORTANT]
   >
   >The [!UICONTROL Advanced Search] functionality is case-insensitive; however, products returned at the time of delivery are based on case-sensitive search. This mismatch might lead to confusion. Ensure that you consider case-sensitivity when you create collections or exclusions based on results using the [!UICONTROL Advanced Search] functionality. For example, if you perform a search for "Holiday," that initial search lists results containing "Holiday" and "holiday." If you then create a catalog with the intent to return products containing "holiday," only products containing "holiday" are returned. Products containing "Holiday" are not returned. Exclusions are handled in a similar fashion.-->

## De omgeving wijzigen

[&#x200B; Milieu&#39;s &#x200B;](/help/main/administrating-target/environments.md) laten u uw plaatsen en pre-productiemilieu&#39;s voor gemakkelijk beheer en gescheiden rapportering organiseren.

1. Klik het pictogram van Filters van de Show ( ![&#x200B; toon het pictogram van Filters &#x200B;](/help/main/assets/icons/Filter.svg)).

1. Selecteer de gewenste omgeving in de vervolgkeuzelijst **[!UICONTROL Environment]** .

<!-- ## Modify the Catalog Search page (filters and columns)

You can temporarily modify the available filters and columns on the [!UICONTROL Catalog Search] page for the current session.

### Modify filters

You can add additional filter facets to the [!UICONTROL Catalog Search] page.

1. In the **[!UICONTROL Filters]** panel, click **[!UICONTROL Modify]**.

   ![Modify filters link](/help/main/c-recommendations/c-products/assets/modify-filters.png)

1. Select the desired search facets (ID, name, message, etc.), then click **[!UICONTROL Save]**.

   ![Add filters](/help/main/c-recommendations/c-products/assets/add-filters.png)

Keep in mind that the additional filter facets are available in the current session only.-->

## Kolommen wijzigen

U kunt de actieve kolommen op de [!UICONTROL Catalog Search] pagina wijzigen.

1. Klik het **[!UICONTROL Customize Table]** pictogram ( ![&#x200B; pas het pictogram van de Lijst &#x200B;](/help/main/assets/icons/ColumnSetting.svg) aan).

1. Schakel de kolommen in of uit die u wilt weergeven of verbergen.

Wijzigingen die u aanbrengt, blijven tijdens de verschillende sessies behouden.
