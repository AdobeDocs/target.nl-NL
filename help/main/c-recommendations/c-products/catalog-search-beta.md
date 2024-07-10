---
keywords: cataloguszoekopdracht;catalogus;zoeken;uitsluiten;verzameling;filter;aanbevelingen
description: Leer hoe u de [!DNL Recommendations] [!UICONTROL Catalog Search] als u producten of inhoud wilt zoeken, verwijdert u onder andere items uit de catalogus.
title: Hoe gebruik ik de [!DNL Recommendations] [!UICONTROL Catalog Search]?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Zie wat er in Target Premium is opgenomen."
feature: Recommendations
hide: true
hidefromtoc: true
exl-id: 6b0175b1-0eee-498d-8a08-513cf6695114
source-git-commit: 16a7c11e8b9b1a08b1e467519f997d0b05e47529
workflow-type: tm+mt
source-wordcount: '539'
ht-degree: 0%

---

# [!UICONTROL Catalog Search]

De [!UICONTROL Catalog Search] pagina in [!DNL Adobe Recommendations] helpt u de producten of inhoud in uw catalogus te vinden. De eenvoudigste taak die u op deze pagina kunt uitvoeren, is het zoeken naar een item. Bovendien kunt u de omgeving wijzigen, facetten filteren, kolommen in de tabel wijzigen, nieuwe zoekfacetten toevoegen en nog veel meer.

De catalogi verwijzen naar uw volledige productreeks (entiteiten). Uw catalogus kan vele inzamelingen bevatten, een manier om uw producten in logische emmers te organiseren.

## Toegang [!UICONTROL Catalog Search]

Als u toegang wilt krijgen tot [!UICONTROL Catalog Search] pagina, klikt u **[!UICONTROL Recommendations]** > **[!UICONTROL Catalog Search]**.

![Pagina Zoeken in catalogus](/help/main/c-recommendations/c-products/assets/catalog-search-new.png)

## Een eenvoudige zoekopdracht uitvoeren

1. Typ een zoekterm in het dialoogvenster **[!UICONTROL Search In]** veld.

1. (Optioneel) U kunt uw zoekopdracht verfijnen door een zoekoptie te selecteren in het optiemenu dat wordt weergegeven wanneer u op de pijl omlaag klikt in het dialoogvenster [!UICONTROL Search In] veld.

   Zoekopties zijn onder andere:

   * ID
   * Naam
   * Bericht

1. Blader door de items in de zoekresultaten om miniaturen en andere productinformatie weer te geven.

   >[!NOTE]
   >
   > Wanneer u een cataloguszoekopdracht uitvoert op een aangepast kenmerk met een numerieke waarde, wordt het aangepaste kenmerk in de resultaten behandeld als een tekenreeks in plaats van een numerieke waarde.
   >
   >Er is momenteel geen functionaliteit beschikbaar waarmee u het type van een kenmerk kunt wijzigen. Als u een wijziging wilt aanbrengen, [een klantenprobleem openen](/help/main/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C) het verwijzen naar de kenmerken waarvoor het type moet worden gewijzigd van tekenreeks in numeriek.

   U kunt filters ook gebruiken om de gewenste producten te vinden. Als u bijvoorbeeld op de knop **[!UICONTROL Show Filters]** icon ( ![Pictogram Filters tonen](/help/main/c-recommendations/c-products/assets/icon-show-filters.png) ), de [!UICONTROL Collections] facet, selecteert u vervolgens een of meer verzamelingen, alle producten die tot de geselecteerde verzamelingen in de catalogusweergave behoren.

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

De index van de catalogus wordt automatisch gemaakt wanneer u de eerste feed uploadt en wordt vernieuwd op basis van de [gespecificeerd schema](/help/main/c-recommendations/c-products/feeds.md#steps).

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

[Omgevingen](/help/main/administrating-target/environments.md) kunt u uw sites en pre-productieomgevingen ordenen voor eenvoudig beheer en gescheiden rapportering.

1. Klik op het pictogram Filters tonen ( ![Pictogram Filters tonen](/help/main/c-recommendations/c-products/assets/icon-show-filters.png) ).

1. Selecteer de gewenste omgeving in het menu **[!UICONTROL Environment]** vervolgkeuzelijst.

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

U kunt de actieve kolommen tijdelijk wijzigen in het dialoogvenster [!UICONTROL Catalog Search] pagina.

1. Klik op de knop **[!UICONTROL Customize Table]** icon (  ![Pictogram Tabel aanpassen](/help/main/c-recommendations/c-products/assets/icon-customize-table.png) ).

1. Schakel de kolommen in of uit die u wilt weergeven of verbergen.

Wijzigingen die u aanbrengt, gelden alleen voor de huidige sessie.
