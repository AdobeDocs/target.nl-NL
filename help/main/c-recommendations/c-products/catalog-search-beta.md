---
keywords: cataloguszoekopdracht;catalogus;zoeken;uitsluiten;verzameling;filter;aanbevelingen
description: Leer hoe u de [!DNL Recommendations] [!UICONTROL Catalog Search] om producten of inhoud te zoeken, verzamelingen of uitsluitingen te maken, items uit uw catalogus te verwijderen en nog veel meer.
title: Hoe gebruik ik de [!DNL Recommendations] [!UICONTROL Catalog Search]?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Zie wat er in Target Premium is opgenomen."
feature: Recommendations
hide: true
hidefromtoc: true
source-git-commit: c2d553a9f292ff9942fe973c17040e003db8c60d
workflow-type: tm+mt
source-wordcount: '980'
ht-degree: 0%

---

# [!UICONTROL Catalog Search]

De [!UICONTROL Catalog Search] pagina in [!DNL Adobe Recommendations] helpt u de producten of inhoud in uw catalogus te vinden. De eenvoudigste taak die u op deze pagina kunt uitvoeren, is het zoeken naar een item. Bovendien kunt u het milieu veranderen, onderzoeksresultaten aan inzamelingen of uitsluitingen bewaren, filterfacetten toevoegen, kolommen in de lijst wijzigen, nieuwe onderzoeksfacetten toevoegen, en meer.

De catalogi verwijzen naar uw volledige productreeks (entiteiten). Uw catalogus kan vele inzamelingen bevatten, een manier om uw producten in logische emmers te organiseren.

## Toegang [!UICONTROL Catalog Search]

Als u toegang wilt krijgen tot [!UICONTROL Catalog Search] pagina, klikt u **[!UICONTROL Recommendations]** > **[!UICONTROL Catalog Search]**.

![Pagina Zoeken in catalogus](/help/main/c-recommendations/c-products/assets/catalog-search-new.png)

## Zoeken naar een object

U kunt een eenvoudige zoekopdracht of een geavanceerde zoekopdracht gebruiken om items in uw catalogus te zoeken.

### Een eenvoudige zoekopdracht uitvoeren

1. Typ een zoekterm in het dialoogvenster **[!UICONTROL Search In]** veld.

1. (Optioneel) U kunt uw zoekopdracht verfijnen door een zoekoptie te selecteren in het optiemenu dat wordt weergegeven wanneer u op de pijl omlaag klikt in het dialoogvenster [!UICONTROL Search In] veld.

   Zoekopties zijn onder andere:

   * ALL - Zoekt over alle andere onderzoekscriteria, gebruikend OF logica.
   * Naam
   * Merk
   * Categorie
   * ID
   * Bericht

1. U kunt nu door de items in de zoekresultaten bladeren om miniaturen en andere productinformatie weer te geven.

   In de volgende afbeelding ziet u de resultaten van de optie Alles voor &quot;fiets&quot;.

   ![Catalogus zoeken naar fiets](/help/main/c-recommendations/c-products/assets/bike-results.png)

   Het aantal dat naast &quot;Producten&quot;toont is het aantal producten die de onderzoekstermijn aanpassen, van het totaal beschikbaar in het gespecificeerde milieu.

   U kunt de functie voor automatisch aanvullen zoeken gebruiken. In de volgende afbeelding retourneert het typen van &quot;bik&quot; alle producten die het woord &quot;cycle&quot; bevatten.

   ![Zoekopdracht automatisch voltooid](/help/main/c-recommendations/c-products/assets/bike-results-2.png)

   >[!NOTE]
   >
   >Wanneer u een cataloguszoekopdracht uitvoert op een aangepast kenmerk met een numerieke waarde, wordt het aangepaste kenmerk in de resultaten behandeld als een tekenreeks in plaats van een numerieke waarde.
   >
   >Er is momenteel geen functionaliteit beschikbaar waarmee u het type van een kenmerk kunt wijzigen. Als u een wijziging wilt aanbrengen, [een klantenprobleem openen](/help/main/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C) het verwijzen naar de kenmerken waarvoor het type moet worden gewijzigd van tekenreeks in numeriek.

1. U kunt filters ook gebruiken om het gewenste product te vinden. In het volgende voorbeeld, door uit te breiden [!UICONTROL Collections] facet en selecteer &quot;Extra&#39;s maken&quot;, alle fietsgereedschappen in uw catalogusscherm.

   ![Teken-gereedschappen](/help/main/c-recommendations/c-products/assets/bike-results-3.png)

1. U kunt verder zoeken in de resultatenlijst door een zoekterm in te voeren, bijvoorbeeld &#39;keten&#39;.

   ![Zoeken naar keten](/help/main/c-recommendations/c-products/assets/bike-results-4.png)

### Een geavanceerde zoekopdracht uitvoeren {#advanced-search}

U kunt [!UICONTROL Advanced Search] om uw zoekresultaten verder te verfijnen of om uw zoekresultaten op te slaan als een [collectie](/help/main/c-recommendations/c-products/collections.md) of [uitsluiting](/help/main/c-recommendations/c-products/exclusions.md).

1. Klik op de knop **[!UICONTROL Advanced Search]** koppeling.

   ![Geavanceerde zoekpagina](/help/main/c-recommendations/c-products/assets/advances-search.png)

1. Gebruik de vervolgkeuzelijsten om de parameter, de operator en de waarden voor uw zoekopdracht op te geven.

1. (Optioneel) Klik op **[!UICONTROL Add Rule]** om een extra zoekregel toe te voegen.

   Elke extra onderzoeksregel wordt aangesloten bij de exploitant AND.

1. Klik op **[!UICONTROL Search]**.

1. (Optioneel) Klik op **[!UICONTROL Save As]** en klik vervolgens op **[!UICONTROL Collection]** of **[!UICONTROL Exclusion]**.

   ![Opslaan als opties](/help/main/c-recommendations/c-products/assets/save-as.png)

   Zie voor meer informatie [Een verzameling of uitsluiting maken op basis van Geavanceerd zoeken](#save-as) hieronder.

## Details van een object bekijken

U kunt de details van een afzonderlijk item, zoals de id, de naam, het bericht, de categorie en meer, weergeven door de details ervan weer te geven.

1. Klik op een item in de zoekresultaten om de details weer te geven.

   ![Productgegevens](/help/main/c-recommendations/c-products/assets/bike-results-5.png)

## Een item uit de catalogus verwijderen

1. Klik op een item in de zoekresultaten om de details weer te geven.

1. Klik op **[!UICONTROL Remove from Catalog]**.

1. Bevestig dat u het item wilt verwijderen.

Alle informatie over dat item wordt verwijderd uit de catalogusindex. Het item wordt alleen in de catalogus opgenomen als het opnieuw wordt toegevoegd aan een gegevensfeed. Een verwijderd item moet afzonderlijk van feeds worden verwijderd.

## De catalogus vernieuwen

De index van de catalogus wordt automatisch gemaakt wanneer u de eerste feed uploadt en wordt vernieuwd op basis van de [gespecificeerd schema](/help/main/c-recommendations/c-products/feeds.md#steps).

De catalogus wordt automatisch vernieuwd wanneer updates worden ontvangen via feed-bestanden, API- of mbox-updates. Updates worden meestal binnen een uur voltooid. Als er updates worden uitgevoerd, wordt de tijd weergegeven waarop de meest recente update is gestart. Als er geen updates worden uitgevoerd, wordt de tijd weergegeven waarop de meest recente update is gestart en voltooid.

## Een verzameling of uitsluiting maken op basis van Geavanceerd zoeken {#save-as}

U kunt [verzamelingen](/help/main/c-recommendations/c-products/collections.md) of [uitsluitingen](/help/main/c-recommendations/c-products/exclusions.md) gebruiken [!UICONTROL Advanced Search] op de [!UICONTROL Catalog Search] pagina ([!UICONTROL Recommendations] > [!UICONTROL Catalog Search] > [!UICONTROL Advanced Search]).

1. Een [geavanceerd zoeken](#advanced-search).

1. Klikken **[!UICONTROL Save As]** en klik vervolgens op **[!UICONTROL Collection]** of **[!UICONTROL Exclusion]**.

   ![Opslaan als opties](/help/main/c-recommendations/c-products/assets/save-as.png)

   >[!IMPORTANT]
   >
   >De [!UICONTROL Advanced Search] de functionaliteit is case-insensitive; nochtans, zijn de producten die op het tijdstip van levering zijn teruggekeerd gebaseerd op case-sensitive onderzoek. Deze wanverhouding kan tot verwarring leiden. Zorg ervoor dat u rekening houdt met hoofdlettergevoeligheid wanneer u verzamelingen of uitsluitingen maakt op basis van resultaten met de [!UICONTROL Advanced Search] functionaliteit. Als u bijvoorbeeld zoekt naar &#39;Vakantie&#39;, worden in de eerste zoekopdracht resultaten weergegeven die &#39;Vakantie&#39; en &#39;Vakantie&#39; bevatten. Als u vervolgens een catalogus maakt met de intentie om producten met &quot;vakantie&quot; te retourneren, worden alleen producten met &quot;vakantie&quot; geretourneerd. Producten met &quot;Vakantie&quot; worden niet geretourneerd. Uitsluitingen worden op vergelijkbare wijze behandeld.

## De omgeving wijzigen

[Omgevingen](/help/main/administrating-target/environments.md) kunt u uw sites en pre-productieomgevingen ordenen voor eenvoudig beheer en gescheiden rapportering.

1. Klik op de koppeling Omgeving.

   ![Omgevingslink](/help/main/c-recommendations/c-products/assets/environment.png)

1. Selecteer de gewenste omgeving.

## De pagina Catalogus zoeken (filters en kolommen) wijzigen

U kunt de beschikbare filters en kolommen tijdelijk wijzigen in het dialoogvenster [!UICONTROL Catalog Search] pagina voor de huidige sessie.

### Filters wijzigen

U kunt extra filterfacetten aan toevoegen [!UICONTROL Catalog Search] pagina.

1. In de **[!UICONTROL Filters]** deelvenster, klikt u op **[!UICONTROL Modify]**.

   ![Filters wijzigen, koppeling](/help/main/c-recommendations/c-products/assets/modify-filters.png)

1. Selecteer de gewenste zoekfacetten (ID, naam, bericht, enz.) en klik op **[!UICONTROL Save]**.

   ![Filters toevoegen](/help/main/c-recommendations/c-products/assets/add-filters.png)

Houd er rekening mee dat de extra filterfacetten alleen beschikbaar zijn in de huidige sessie.

### Kolommen wijzigen

U kunt de actieve kolommen tijdelijk wijzigen in het dialoogvenster [!UICONTROL Catalog Search] pagina.

1. Klik op de knop **[!UICONTROL Columns]** koppeling.

   ![Kolomopties](/help/main/c-recommendations/c-products/assets/columns.png)

1. (Voorwaardelijk) U kunt de volgorde van actieve kolommen wijzigen door de kolommen in het deelvenster **[!UICONTROL Active Columns]** in de gewenste volgorde.

1. (Voorwaardelijk) Sleep items vanuit de **[!UICONTROL Active Columns]** aan de **[!UICONTROL Inactive Columns]** (en omgekeerd) naar wens.

   U kunt ook op het verwijderpictogram ( x ) klikken naast de kolom die u van de actieve naar de niet-actieve sectie wilt verplaatsen.

Wijzigingen die u aanbrengt, gelden alleen voor de huidige sessie.