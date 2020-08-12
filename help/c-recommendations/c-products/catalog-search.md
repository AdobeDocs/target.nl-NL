---
keywords: catalog;search
description: Met de zoekactie in de catalogus in Adobe Target kunt u de producten of inhoud in de catalogus vinden.
title: Cataloguszoekopdracht in Adobe Target
feature: null
uuid: e0876963-5905-4850-a615-953e435f26e9
translation-type: tm+mt
source-git-commit: a51addc6155f2681f01f2329b25d72327de36701
workflow-type: tm+mt
source-wordcount: '342'
ht-degree: 0%

---


# ![zoeken naar PREMIUM](/help/assets/premium.png) -catalogus {#catalog-search}

Met de zoekopdracht in de catalogus kunt u de producten of inhoud in de catalogus zoeken.

Klik op **[!UICONTROL Recommendations]** > **[!UICONTROL Catalog Search]**.

U kunt uw zoekopdracht verfijnen door een zoekoptie te selecteren in het optiemenu dat wordt weergegeven wanneer u op de pijl omlaag klikt in het zoekveld.

![](assets/searchproductsmenu.png)

Zoekopties zijn onder andere:

* ALLES
* Naam
* Merk
* Categorie
* ID
* Bericht

**[!UICONTROL ALL]** zoekt in alle andere zoekcriteria met OR-logica.

In de onderzoeksresultaten, klikt u de **[!UICONTROL Environment]** filter om het milieu [van de de](/help/administrating-target/hosts.md) gastheergroep van de productie te specificeren waarvan catalogus u toont. U kunt ook door de items in de zoekresultaten bladeren om miniaturen en andere productinformatie weer te geven.

Het aantal dat naast &quot;Producten&quot;toont is het aantal producten die de onderzoekstermijn aanpassen, van het totaal beschikbaar in het gespecificeerde milieu.

De catalogus wordt automatisch vernieuwd wanneer updates worden ontvangen via feed-bestanden, API- of mbox-updates. Updates worden meestal binnen een uur voltooid. Als er updates worden uitgevoerd, wordt de tijd weergegeven waarop de meest recente update is gestart. Als er geen updates worden uitgevoerd, wordt de tijd weergegeven waarop de meest recente update is gestart en voltooid.

## Een verzameling of uitsluiting maken op basis van Geavanceerd zoeken

U kunt [verzamelingen](/help/c-recommendations/c-products/collections.md) of [uitsluitingen](/help/c-recommendations/c-products/exclusions.md) maken met Geavanceerd zoeken op de pagina Catalogus zoeken ([!UICONTROL Recommendations] > [!UICONTROL Catalog Search] > [!UICONTROL Advanced Search]).

![Opslaan als dialoogvenster](/help/c-recommendations/c-products/assets/save-as-dialog.png)

Nadat u een zoekopdracht hebt gemaakt met &#39;id > contains&#39;, kunt u bijvoorbeeld op [!UICONTROL Save As] > [!UICONTROL Collection or Exclusion]klikken.

>[!IMPORTANT]
>
>De functie Geavanceerd zoeken is niet hoofdlettergevoelig. producten die op het tijdstip van levering worden geretourneerd, zijn echter gebaseerd op hoofdlettergevoelige zoekopdrachten. Deze wanverhouding kan tot verwarring leiden. Zorg ervoor dat u rekening houdt met hoofdlettergevoeligheid wanneer u verzamelingen of uitsluitingen maakt op basis van resultaten met de functie Geavanceerd zoeken. Als u bijvoorbeeld zoekt naar &#39;Vakantie&#39;, worden in de eerste zoekopdracht resultaten weergegeven die &#39;Vakantie&#39; en &#39;Vakantie&#39; bevatten. Als u vervolgens een catalogus maakt met de bedoeling producten met &quot;vakantie&quot; terug te sturen, worden alleen producten met &quot;vakantie&quot; geretourneerd. Producten met &quot;Vakantie&quot; worden niet geretourneerd. Uitsluitingen worden op vergelijkbare wijze behandeld.
