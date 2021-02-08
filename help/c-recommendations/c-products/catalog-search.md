---
keywords: cataloguszoekopdracht;catalogus;zoeken;uitsluiten;verzameling;filter
description: Leer hoe u met de zoekfunctie voor Recommendations-catalogi producten of inhoud kunt zoeken, verzamelingen of uitsluitingen kunt maken, items uit uw catalogus kunt verwijderen en nog veel meer.
title: Hoe gebruik ik de zoekfunctie van de Recommendations-catalogus?
feature: Recommendations
translation-type: tm+mt
source-git-commit: bb27f6e540998f7dbe7642551f7a5013f2fd25b4
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# ![](/help/assets/premium.png) PREMIUMCatalog Search

De [!UICONTROL Catalog Search] pagina in [!DNL Adobe Recommendations] helpt u van de producten of de inhoud in uw catalogus de plaats bepalen. De eenvoudigste taak die u op deze pagina kunt uitvoeren, is het zoeken naar een item. Daarnaast kunt u de omgeving wijzigen, zoekresultaten opslaan in verzamelingen of uitsluitingen, filterfacetten toevoegen en kolommen in de tabel wijzigen, nieuwe zoekfacetten toevoegen en nog veel meer.

De catalogi verwijzen naar uw volledige productreeks (entiteiten). Uw catalogus kan vele inzamelingen bevatten, een manier om uw producten in logische emmers te organiseren.

## Zoeken naar catalogus openen

Als u de pagina [!UICONTROL Catalog Search] wilt openen, klikt u op **[!UICONTROL Recommendations]** > **[!UICONTROL Catalog Search]**.

![Pagina Zoeken in catalogus](/help/c-recommendations/c-products/assets/catalog-search.png)

## Zoeken naar een object

U kunt een eenvoudige zoekopdracht of een geavanceerde zoekopdracht gebruiken om items in uw catalogus te zoeken.

### Een eenvoudige zoekopdracht uitvoeren

1. Typ een zoekterm in het veld **[!UICONTROL Search Products]**.

1. (Optioneel) U kunt uw zoekopdracht verfijnen door een zoekoptie te selecteren in het optiemenu dat wordt weergegeven wanneer u op de pijl omlaag klikt in het zoekveld.

   ![](assets/searchproductsmenu.png)

   Zoekopties zijn onder andere:

   * ALL - Zoekt over alle andere onderzoekscriteria, gebruikend OF logica.
   * Naam
   * Merk
   * Categorie
   * ID
   * Bericht

1. U kunt nu door de items in de zoekresultaten bladeren om miniaturen en andere productinformatie weer te geven.

   In de volgende afbeelding ziet u de resultaten van de optie Alles voor &quot;fiets&quot;.

   ![Catalogus zoeken naar fiets](/help/c-recommendations/c-products/assets/bike-results.png)

   Het aantal dat naast &quot;Producten&quot;toont is het aantal producten die de onderzoekstermijn aanpassen, van het totaal beschikbaar in het gespecificeerde milieu.

   U kunt de functie voor automatisch aanvullen zoeken gebruiken. In de volgende afbeelding retourneert het typen van &quot;bik&quot; alle producten die het woord &quot;cycle&quot; bevatten.

   ![Zoekopdracht automatisch voltooid](/help/c-recommendations/c-products/assets/bike-results-2.png)

   >[!NOTE]
   >
   >Wanneer u een catalogusonderzoek op een douanekenmerk met een numerieke waarde uitvoert, behandelen de resultaten het douanekenmerk om een koordtype in plaats van een numerieke waarde te zijn.
   >
   >Er is momenteel geen functionaliteit beschikbaar waarmee u het type van een kenmerk kunt wijzigen. Om een verandering aan te brengen, [open een klantenkwestie](/help/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C) die van de attributen verwijzen die het type veranderen van koord in numeriek nodig hebben.

1. U kunt filters ook gebruiken om het gewenste product te vinden. In het volgende voorbeeld door het [!UICONTROL Collections]-facet uit te vouwen en &quot;Extra&#39;s maken&quot; te selecteren, worden alle fietsgereedschappen in het catalogusscherm weergegeven.

   ![Teken-gereedschappen](/help/c-recommendations/c-products/assets/bike-results-3.png)

1. U kunt verder zoeken in de resultatenlijst door een zoekterm in te voeren, bijvoorbeeld &#39;keten&#39;.

   ![Zoeken naar keten](/help/c-recommendations/c-products/assets/bike-results-4.png)

### Een geavanceerde zoekopdracht uitvoeren {#advanced-search}

U kunt [!UICONTROL Advanced Search] gebruiken om uw onderzoeksresultaten verder te verfijnen of uw onderzoeksresultaten als [inzameling ](/help/c-recommendations/c-products/collections.md) of [uitsluiting](/help/c-recommendations/c-products/exclusions.md) te bewaren.

1. Klik op de koppeling **[!UICONTROL Advanced Search]**.

   ![Geavanceerde zoekpagina](/help/c-recommendations/c-products/assets/advances-search.png)

1. Gebruik de vervolgkeuzelijsten om de parameter, de operator en de waarden voor uw zoekopdracht op te geven.

1. (Optioneel) Klik op **[!UICONTROL Add Rule]** om een extra zoekregel toe te voegen.

   Elke extra onderzoeksregel wordt aangesloten bij de exploitant AND.

1. Klik op **[!UICONTROL Search]**.

1. (Optioneel) Klik op **[!UICONTROL Save As]** en vervolgens op **[!UICONTROL Collection]** of **[!UICONTROL Exclusion]**.

   ![Opslaan als opties](/help/c-recommendations/c-products/assets/save-as.png)

   Zie [Een verzameling of uitsluiting maken op basis van Geavanceerd zoeken](#save-as) hieronder voor meer informatie.

## Details van een object bekijken

U kunt de details van een afzonderlijk item, zoals de id, de naam, het bericht, de categorie en meer, weergeven door de details ervan weer te geven.

1. Klik op een item in de zoekresultaten om de details weer te geven.

   ![Productgegevens](/help/c-recommendations/c-products/assets/bike-results-5.png)

## Een item uit de catalogus verwijderen

1. Klik op een item in de zoekresultaten om de details weer te geven.

1. Klik op **[!UICONTROL Remove from Catalog]**.

1. Bevestig dat u het item wilt verwijderen.

Alle informatie over dat item wordt verwijderd uit de catalogusindex. Het item wordt alleen in de catalogus opgenomen als het opnieuw wordt toegevoegd aan een gegevensfeed. Een verwijderd item moet afzonderlijk van feeds worden verwijderd.

## De catalogus vernieuwen

De index van uw catalogus wordt automatisch gecreeerd wanneer u uw eerste voer uploadt, en volgens [gespecificeerd programma](/help/c-recommendations/c-products/feeds.md#steps) verfrist.

De catalogus wordt automatisch vernieuwd wanneer updates worden ontvangen via feed-bestanden, API- of mbox-updates. Updates worden meestal binnen een uur voltooid. Als er updates worden uitgevoerd, wordt de tijd weergegeven waarop de meest recente update is gestart. Als er geen updates worden uitgevoerd, wordt de tijd weergegeven waarop de meest recente update is gestart en voltooid.

## Een verzameling of uitsluiting maken op basis van Geavanceerd zoeken {#save-as}

U kunt [verzamelingen](/help/c-recommendations/c-products/collections.md) of [uitsluitingen](/help/c-recommendations/c-products/exclusions.md) tot stand brengen gebruikend [!UICONTROL Advanced Search] op [!UICONTROL Catalog Search] pagina ([!UICONTROL Recommendations] > [!UICONTROL Catalog Search] > [!UICONTROL Advanced Search]).

1. Voer [geavanceerd onderzoek](#advanced-search) uit.

1. Klik **[!UICONTROL Save As]**, dan klik **[!UICONTROL Collection]** of **[!UICONTROL Exclusion]**.

   ![Opslaan als opties](/help/c-recommendations/c-products/assets/save-as.png)

   >[!IMPORTANT]
   >
   >De [!UICONTROL Advanced Search] functionaliteit is case-insensitive; producten die op het tijdstip van levering worden geretourneerd, zijn echter gebaseerd op hoofdlettergevoelige zoekopdrachten. Deze wanverhouding kan tot verwarring leiden. Zorg ervoor dat u rekening houdt met hoofdlettergevoeligheid wanneer u verzamelingen of uitsluitingen maakt op basis van resultaten met de functie [!UICONTROL Advanced Search]. Als u bijvoorbeeld zoekt naar &#39;Vakantie&#39;, worden in de eerste zoekopdracht resultaten weergegeven die &#39;Vakantie&#39; en &#39;Vakantie&#39; bevatten. Als u vervolgens een catalogus maakt met de bedoeling producten met &quot;vakantie&quot; terug te sturen, worden alleen producten met &quot;vakantie&quot; geretourneerd. Producten met &quot;Vakantie&quot; worden niet geretourneerd. Uitsluitingen worden op vergelijkbare wijze behandeld.

## De omgeving wijzigen

[Met ](/help/administrating-target/environments.md) omgevingen organiseert u uw sites en pre-productieomgevingen voor eenvoudig beheer en gescheiden rapportering.

1. Klik op de koppeling Omgeving.

   ![Omgevingslink](/help/c-recommendations/c-products/assets/environment.png)

1. Selecteer de gewenste omgeving.

## De pagina Catalogus zoeken (filters en kolommen) wijzigen

U kunt de beschikbare filters en kolommen op de [!UICONTROL Catalog Search] pagina voor de huidige zitting tijdelijk wijzigen.

### Filters wijzigen

U kunt extra filterfacetten aan de [!UICONTROL Catalog Search] pagina toevoegen.

1. Klik in het **[!UICONTROL Filters]**-deelvenster op **[!UICONTROL Modify]**.

   ![Filters wijzigen, koppeling](/help/c-recommendations/c-products/assets/modify-filters.png)

1. Selecteer de gewenste zoekfacetten (ID, naam, bericht, enz.) en klik op **[!UICONTROL Save]**.

   ![Filters toevoegen](/help/c-recommendations/c-products/assets/add-filters.png)

Houd er rekening mee dat de extra filterfacetten alleen beschikbaar zijn in de huidige sessie.

### Kolommen wijzigen

U kunt de actieve kolommen op de [!UICONTROL Catalog Search] pagina tijdelijk wijzigen.

1. Klik op de koppeling **[!UICONTROL Columns]**.

   ![Kolomopties](/help/c-recommendations/c-products/assets/columns.png)

1. (Voorwaardelijk) om de orde van actieve kolommen te herschikken, sleep en laat vallen de kolommen in **[!UICONTROL Active Columns]** sectie in de gewenste orde.

1. (Voorwaardelijk) belemmering en laat vallen punten van **[!UICONTROL Active Columns]** aan **[!UICONTROL Inactive Columns]** (en vice versa), zoals gewenst.

   U kunt ook op het verwijderpictogram ( x ) klikken naast de kolom die u van de actieve naar de niet-actieve sectie wilt verplaatsen.

Wijzigingen die u aanbrengt, gelden alleen voor de huidige sessie.

