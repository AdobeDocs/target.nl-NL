---
keywords: inclusieregels;inclusiecriteria;aanbevelingen;creeer nieuwe criteria;bevordering;bevordering;dynamisch filtreren;dynamiek;lege waarden;negeren het filtreren regel;statische filter;filter door waarde;entiteitattribuut aanpassing;parameter aanpassing;filter door waarde;statische filter
description: Leer hoe te om inclusieregels in  [!DNL Target]  Aanbevelingen voor criteria en bevorderingen tot stand te brengen.
title: Hoe gebruik ik dynamische en statische inclusieregels in Aanbevelingen?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=nl-NL#premium newtab=true" tooltip="Kijk wat er in Target Premium is opgenomen."
feature: Recommendations
mini-toc-levels: 3
exl-id: 49b20e75-ee55-4239-94a0-6d175e2d4811
source-git-commit: 51e484d54f4d318ea59fdfdb16d1ed7014abdfdb
workflow-type: tm+mt
source-wordcount: '1846'
ht-degree: 0%

---

# Regels voor dynamische en statische integratie gebruiken

Maak inclusieregels voor criteria en promoties in [!DNL Adobe Target] en voeg dynamische of statische filterregels toe voor betere resultaten voor uw aanbevelingen.

Het proces om inclusieregels voor criteria en promoties tot stand te brengen en te gebruiken is gelijkaardig, zoals de gebruiksgevallen en de voorbeelden. In deze afdeling worden zowel de criteria als de promoties en het gebruik van de regels voor inclusie behandeld.

## Filterregels toevoegen aan criteria en promoties {#section_CD0D74B8D3BE4A75A78C36CF24A8C57F}

De volgende secties bevatten meer informatie:

### Filterregels toevoegen aan criteria

1. Terwijl [&#x200B; het creëren van criteria &#x200B;](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md#task_8A9CB465F28D44899F69F38AD27352FE) (**[!UICONTROL Recommendations]> [!UICONTROL Criteria] > [!UICONTROL Create Criteria] >[!UICONTROL Create Criteria]**), klik **[!UICONTROL Add Filtering Rule]** onder **[!UICONTROL Inclusion Rules]**.

   ![&#x200B; voegt het Filtreren Regel &#x200B;](/help/main/c-recommendations/c-algorithms/assets/add-fitering-rule.png) toe

1. Klik de **Statische drop-down lijst van de Filter** in &quot;Welke andere regels de aanbeveling&quot;doos zouden moeten volgen, dan kies de gewenste optie van de [!UICONTROL Static Filter] drop-down lijst.

   ![&#x200B; Statische drop-down lijst van de Filter &#x200B;](/help/main/c-recommendations/c-algorithms/assets/dynamic-and-static.png)

   Welke opties beschikbaar zijn, is afhankelijk van de verticale en aanbevolen industriesleutel.

### Filterregels toevoegen aan promoties

1. Terwijl [&#x200B; creërend een bevordering &#x200B;](/help/main/c-recommendations/t-create-recs-activity/adding-promotions.md#task_CC5BD28C364742218C1ACAF0D45E0E14), selecteer **[!UICONTROL Promote by Attribute]**, dan klik **[!UICONTROL Add Filtering Rule]**.

## Filtertypen {#section_0125F1ED10A84C0EB45325122460EBCD}

De volgende secties geven een overzicht van de typen filteropties voor [!UICONTROL Dynamic Filtering] en [!UICONTROL Filter by Value] voor zowel criteria als promoties:

### Dynamisch filteren

Dynamische insluitingsregels zijn krachtiger dan statische insluitingsregels en leveren betere resultaten en betrokkenheid op. Overweeg het volgende:

* De dynamische inclusieregels leveren aanbevelingen door een attribuut in de het profielparameter van een gebruiker of in een mbox vraag aan te passen.

  U kunt bijvoorbeeld een aanbeveling met de naam &quot;Populaire criteria&quot; maken. Van de reeks teruggekeerde aanbevelingen, kunt u om het even welke aanbevelingen (in echt - tijd) tegen een attribuut filtreren dat wordt overgegaan wanneer de gebruiker tot een pagina toegang heeft waar de aanbevelingen worden getoond.

* Gebruik statische regels om te beperken welke items worden opgenomen in de aanbeveling (in plaats van verzamelingen te gebruiken).

* U kunt zo veel dynamische inclusieregels tot stand brengen zoals nodig. De inclusieregels worden verbonden met een exploitant AND. Aan alle regels moet worden voldaan om een punt in een aanbeveling te omvatten.

De volgende opties zijn beschikbaar voor dynamisch filteren:

| Dynamisch filteren, optie | Details |
| --- | --- |
| [[!UICONTROL Entity Attribute Matching]](/help/main/c-recommendations/c-algorithms/entity-attribute-matching.md) | Filter dynamisch door een pool van potentiële aanbevelingen punten aan een specifiek punt te vergelijken dat de gebruikers met in wisselwerking staan.<P>Gebruik [!UICONTROL Entity Attribute Matching] als u aanbevelingen wilt weergeven die de bezoeker het meest aanspreken, zoals het favoriete merk van de bezoeker. |
| [[!UICONTROL Profile Attribute Matching]](/help/main/c-recommendations/c-algorithms/profile-attribute-matching.md) | Filter dynamisch door items (entiteiten) te vergelijken met een waarde in het gebruikersprofiel.<P>Gebruik [!UICONTROL Profile Attribute Matching] als u aanbevelingen wilt weergeven die overeenkomen met een waarde die is opgeslagen in het profiel van de bezoeker, zoals de grootte of het favoriete merk. |
| [[!UICONTROL Parameter Matching]](/help/main/c-recommendations/c-algorithms/parameter-matching.md) | Filter dynamisch door items (entiteiten) te vergelijken met een waarde in de aanvraag (API of mbox).<P>Gebruik [!UICONTROL Parameter Matching] om inhoud aan te bevelen die overeenkomt met de paginaparameters of de parameters van de bezoeker, zoals apparaatafmetingen of geo-locatie. |

### Filteren op waarde

De volgende optie is beschikbaar voor het filtreren door waarde:

| Filteren op waarde, optie | Details |
| --- | --- |
| [[!UICONTROL Static Filter]](/help/main/c-recommendations/c-algorithms/static-value.md) | Voer handmatig een of meer statische waarden in die u wilt filteren. |

## Beschikbare operatoren {#operators}

Dynamische criteria en promoties zijn veel krachtiger dan statische criteria en promoties en leveren betere resultaten en betrokkenheid op.

De volgende voorbeelden bieden algemene ideeën over hoe u dynamische promoties en uitsluitingen kunt gebruiken bij uw marketingactiviteiten:

>[!NOTE]
>
>&quot;List&quot; vereist dat zowel de entiteiten als de profielkenmerken als arrays worden opgeslagen. Een door komma&#39;s gescheiden lijst werkt niet.

| Operator | Voorbeelden |
| --- | --- |
| [!UICONTROL equals any of]<P>(Beschikbaar bij [!UICONTROL Entity Attribute Matching] , [!UICONTROL Profile Attribute Matching] , [!UICONTROL Parameter Matching] en [!UICONTROL Static Filter] .) | Wanneer u de operator &quot;equals&quot; gebruikt in dynamische promoties en een bezoeker een item op uw website bekijkt (zoals een product, artikel of film), kunt u andere items promoten op:<ul><li>Hetzelfde merk</li><li>Dezelfde categorie</li><li>Dezelfde categorie AND van het huismerk</li><li>Dezelfde winkel</li></ul> |
| [!UICONTROL does not equal any of]<P>(Beschikbaar bij [!UICONTROL Entity Attribute Matching] , [!UICONTROL Profile Attribute Matching] , [!UICONTROL Parameter Matching] en [!UICONTROL Static Filter] .) | Met de operator &quot;[!UICONTROL does not equal any of]&quot; in dynamische promoties kunt u andere items promoten vanaf:<ul><li>Een andere tv-serie</li><li>Een ander genre</li><li>Een andere productreeks</li><li>Een andere stijl-id</li></ul> |
| [!UICONTROL is greater than or equal to any of]<P>(Beschikbaar bij [!UICONTROL Entity Attribute Matching] , [!UICONTROL Profile Attribute Matching] , [!UICONTROL Parameter Matching] en [!UICONTROL Static Filter] .) | Wanneer u de operator &quot;[!UICONTROL is greater than or equal to any of]&quot; gebruikt en een bezoeker een item op uw website (zoals een product) bekijkt, kunt u andere items promoten die:<ul><li>Kostprijs hetzelfde of duurder</li></ul> |
| [!UICONTROL is less than or equal to any of]<P>(Beschikbaar bij [!UICONTROL Entity Attribute Matching] , [!UICONTROL Profile Attribute Matching] , [!UICONTROL Parameter Matching] en [!UICONTROL Static Filter] .) | Wanneer u de operator &quot;[!UICONTROL is less than or equal to an of]&quot; gebruikt en een bezoeker een item op uw website (zoals een product) bekijkt, kunt u andere items promoten die:<ul><li>Kostprijs hetzelfde of minder kostbaar</li><li>Objecten uitsluiten die goedkoper zijn</li></ul> |
| [!UICONTROL contains any of] (Beschikbaar bij [!UICONTROL Entity Attribute Matching] , [!UICONTROL Profile Attribute Matching] , [!UICONTROL Parameter Matching] en [!UICONTROL Static Filter] .) | Wanneer u de operator &quot;[!UICONTROL contains any of]&quot; gebruikt en een bezoeker een item op uw website (zoals een product) bekijkt, kunt u andere items promoten die:<ul><li>Titel bevat hetzelfde merk</li></ul> |
| [!UICONTROL does not contain any of]<P>(Beschikbaar bij [!UICONTROL Entity Attribute Matching] , [!UICONTROL Profile Attribute Matching] , [!UICONTROL Parameter Matching] en [!UICONTROL Static Filter] .) | Wanneer een bezoeker een item op uw website (zoals een product) bekijkt, gebruikt de operator &quot;bevat geen van&quot;, kunt u andere items promoten die:<ul><li>Titel bevat geen woord zweren</li></ul> |
| [!UICONTROL starts with any of]<P>(Beschikbaar bij [!UICONTROL Entity Attribute Matching] , [!UICONTROL Profile Attribute Matching] , [!UICONTROL Parameter Matching] en [!UICONTROL Static Filter] .) | Wanneer u de operator &quot;[!UICONTROL starts with an of]&quot; gebruikt en een bezoeker een item op uw website (zoals een product) bekijkt, kunt u andere items promoten die:<ul><li>De productnaam begint met iPhone</li></ul> |
| [!UICONTROL ends with any of]<P>(Beschikbaar bij [!UICONTROL Entity Attribute Matching] , [!UICONTROL Profile Attribute Matching] , [!UICONTROL Parameter Matching] en [!UICONTROL Static Filter] .) | Wanneer u de operator &quot;[!UICONTROL ends with an of]&quot; gebruikt en een bezoeker een item op uw website (zoals een product) bekijkt, kunt u andere items promoten die:<ul><li>Inhoud eindigt met NL, die de Engelse taal aangeeft</li></ul> |
| [!UICONTROL is between]<P>(Beschikbaar bij [!UICONTROL Entity Attribute Matching] , [!UICONTROL Profile Attribute Matching] en [!UICONTROL Parameter Matching] .) | Gebruikend de &quot;i [!UICONTROL s between]&quot;exploitant in dynamische bevorderingen, wanneer een bezoeker een punt op uw website (zoals een product, artikel, of een film) bekijkt, kunt u andere punten bevorderen die zijn:<ul><li>Meer geld</li><li>Minder duur</li><li>Kosten plus of min 30%</li><li>Later afleveringen in hetzelfde seizoen</li><li>Eerdere boeken in een reeks</li></ul> |
| [!UICONTROL list contains an item in]<P>(Beschikbaar bij [!UICONTROL Profile Attribute Matching] en [!UICONTROL Parameter Matching] .) | Met de operator &quot;[!UICONTROL list contains an item in]&quot; in overeenkomsten met profielkenmerken kunt u andere items promoten die:<ul><li>Beschikbaar in de geografie van de bezoeker</li></ul>**Voorbeeld**: U wilt punten adviseren die slechts in het geografische gebied van een bezoeker beschikbaar zijn.<P>Uw filterregel kan er als volgt uitzien:<P>`availableGeographies list contains an item in user.currentGeography`<P>**Nota**: Wanneer het gebruiken van deze exploitant, wordt een lijst verwacht in de [&#x200B; juiste kant &#x200B;](#caveats) van de regel. |
| [!UICONTROL list does not contain an item in]<P>(Beschikbaar bij [!UICONTROL Profile Attribute Matching] en [!UICONTROL Parameter Matching] .) | Met de operator &quot;[!UICONTROL list does not contain an item in]&quot; in overeenkomsten voor profielkenmerken kunt u andere items uitsluiten die:<ul><li>In de lijst van de laatste tien items die de bezoeker heeft weergegeven</li></ul></ul>**Voorbeeld**: U wilt geen punten bevorderen die de bezoeker onlangs heeft bekeken en geen interesse in getoond.<P>Uw filterregel zou als kunnen kijken:<P>`id is not contained in list user.lastViewedItems`<P>**Nota**: Wanneer het gebruiken van deze exploitant, wordt een lijst verwacht in de [&#x200B; juiste kant &#x200B;](#caveats) van de regel. |
| [!UICONTROL list contains an item in]<P>(Beschikbaar bij [!UICONTROL Entity Attribute Matching] , [!UICONTROL Profile Attribute Matching] en [!UICONTROL Parameter Matching] .) | Met de operator &quot;[!UICONTROL list contains an item in]&quot; in overeenkomsten met profielkenmerken kunt u andere items promoten die:<ul><li>Gekoppeld aan een van de favoriete teams van de bezoeker</li></ul>**Voorbeeld**: U wilt spelen aanbevelen die met één van de favoriete teams van de bezoeker worden geassocieerd.<P>Uw filterregel zou als kunnen kijken:<P>` teamsPlaying list contains an item in user.favoriteTeams`<P>**Nota**: Wanneer het gebruiken van deze exploitant, wordt een lijst verwacht in [&#x200B; beide kanten &#x200B;](#caveats) van de regel. |
| [!UICONTROL list does not contain an item in]<P>(Beschikbaar bij [!UICONTROL Entity Attribute Matching] , [!UICONTROL Profile Attribute Matching] en [!UICONTROL Parameter Matching] .) | Gebruikend de &quot;[!UICONTROL list does not contain an item in]&quot;exploitant in parameter kenmerkenaanpassing, wanneer een bezoeker een punt op uw website (zoals een product, een artikel, of een film) bekijkt, kunt u andere punten uitsluiten die zijn:<ul><li>Bevat in een lijst met verboden typen</li></ul>**Voorbeeld**: U wilt punten uitsluiten die aan bezoekers beschikbaar zijn die volwassenen, zoals tabak en alcohol zijn.<P>Uw filterregel zou als kunnen kijken:<P>`itemType is not contained in list mbox.prohibitedTypes`<P>**Nota**: Wanneer het gebruiken van deze exploitant, wordt een lijst verwacht in [&#x200B; beide kanten &#x200B;](#caveats) van de regel. |
| [!UICONTROL list contains all items in]<P>(Beschikbaar bij [!UICONTROL Entity Attribute Matching] , [!UICONTROL Profile Attribute Matching] en [!UICONTROL Parameter Matching] .) | Met de operator &quot;[!UICONTROL list does not contain an item in]&quot; in overeenkomsten met profielkenmerken kunt u andere items promoten die:<ul><li>Een set vaardigheden opnemen</li><li>Een set vereiste ingrediënten opnemen</li></ul>**Voorbeeld 1**: Veronderstel dat een bezoeker een reeks vaardigheden (Java, C++, en HTML) heeft. De items in de catalogus zijn taken met de vereiste vaardigheden (Java en HTML). U wilt ervoor zorgen dat het profiel van de bezoeker alle vereiste vaardigheden bevat voordat u de taak aan de bezoeker aanbeveelt.<P>Uw filterregel zou als kunnen kijken:<P>`profile.jobSeekerSkills contains all items in entity.requiredSkills`<P>**Voorbeeld 2**: Veronderstel dat een gebruiker een lijst van paneelingrediënten heeft. Het recept bevat een lijst van de vereiste ingrediënten. U wilt ervoor zorgen dat het profiel van de bezoeker alle vereiste ingrediënten bevat voordat u het recept aan de bezoeker aanbeveelt.<P>Uw filterregel zou als kunnen kijken:<P>`profile.ingredientsInPantry contains all items in recipe.ingredientsRequired`<P>**Nota**: Wanneer het gebruiken van deze exploitant, wordt een lijst verwacht in [&#x200B; beide kanten &#x200B;](#caveats) van de regel. |
| [!UICONTROL list does not contain all items in]<P>(Beschikbaar bij [!UICONTROL Entity Attribute Matching] , [!UICONTROL Profile Attribute Matching] en [!UICONTROL Parameter Matching] .) | Met de operator &quot;[!UICONTROL list does not contain all items in]&quot; in overeenkomsten met entiteitskenmerken kunt u andere items promoten die:<ul><li>Geen set met teams opnemen</li></ul>**Voorbeeld**: Stel dat een sportevenement twee teams omvat. Het profiel van de bezoeker geeft aan dat deze bezoeker geen games voor deze teams wil weergeven. U wilt ervoor zorgen dat u geen spel aanbeveelt als deze teams spelen.<P>Uw filterregel zou als kunnen kijken:<P>`profile.leastfavoriteTeams does not contain all items in entity.teamsPlaying`<P>**Nota**: Wanneer het gebruiken van deze exploitant, wordt een lijst verwacht in [&#x200B; beide kanten &#x200B;](#caveats) van de regel. |

## Lege waarden afhandelen tijdens filteren op [!UICONTROL Entity Attribute Matching] , [!UICONTROL Profile Attribute Matching] en [!UICONTROL Parameter Matching] {#section_7D30E04116DB47BEA6FF840A3424A4C8}

U kunt verschillende opties kiezen om lege waarden af te handelen wanneer u filtert door [!UICONTROL Entity Attribute Matching] , [!UICONTROL Profile Attribute Matching] en [!UICONTROL Parameter Matching] voor afsluitcriteria en -promoties.

Eerder werden geen resultaten geretourneerd als een waarde leeg was. &quot;Als *x* Leeg&quot;drop-down lijst is laat u de aangewezen actie kiezen om uit te voeren als de criteria lege waarden, zoals aangetoond in de volgende illustratie hebben:

![&#x200B; empty_value beeld &#x200B;](assets/empty_value.png)

Om de gewenste actie te selecteren, houd over het tandwielpictogram (![&#x200B; icon_tandwielbeeld &#x200B;](assets/icon_gear.png)), dan de gewenste actie:

| Handeling | Beschikbaar voor | Details |
|--- |--- |--- |
| [!UICONTROL Ignore this filtering rule] | [!UICONTROL Profile Attribute Matching] en [!UICONTROL Parameter Matching] | Deze handeling is de standaardinstelling voor [!UICONTROL Profile Attribute Matching] en [!UICONTROL Parameter Matching] .<P>Met deze optie wordt opgegeven dat de regel wordt genegeerd. Bijvoorbeeld, als er drie het filtreren regels zijn en de derde regel geen waarden overgaat, in plaats van om het even welke resultaten terug te keren, kunt u de derde regel met de lege waarden eenvoudig negeren. |
| [!UICONTROL Do not show any results for this criteria]<P>(Alleen criteria) | [!UICONTROL Entity Attribute Matching] , [!UICONTROL Profile Attribute Matching] en [!UICONTROL Parameter Matching] | Deze handeling is de standaardinstelling voor [!UICONTROL Entity Attribute Matching] .<P>Zo verwerkte [!DNL Target] lege waarden voordat deze optie werd toegevoegd: er worden geen resultaten voor deze criteria weergegeven. |
| [!UICONTROL &#x200B; Geen items promoten<P>(Alleen promoties) &#x200B;] | [!UICONTROL Entity Attribute Matching] , [!UICONTROL Profile Attribute Matching] en [!UICONTROL Parameter Matching] | Deze handeling is de standaardinstelling voor [!UICONTROL Entity Attribute Matching] .<P>Zo verwerkte [!DNL Target] lege waarden voordat deze optie werd toegevoegd: er worden geen resultaten voor deze criteria weergegeven. |
| [!UICONTROL Use a static value] | [!UICONTROL Entity Attribute Matching] , [!UICONTROL Profile Attribute Matching] en [!UICONTROL Parameter Matching] | Als een waarde leeg is, kunt u ervoor kiezen om een statische waarde te gebruiken. |

## Caveats {#caveats}

>[!IMPORTANT]
>
>Verschillende kenmerken van gegevenstypen zijn mogelijk niet compatibel in dynamische criteria of promoties tijdens runtime met de operatoren &#39;equals&#39; en &#39;does not equal&#39;. Gebruik [!UICONTROL Value] -, [!UICONTROL Margin] -, [!UICONTROL Inventory] - en [!UICONTROL Environment] -waarden verstandig aan de rechterkant als de linkerkant vooraf gedefinieerde kenmerken of aangepaste kenmerken heeft.

![&#x200B; left_right beeld &#x200B;](assets/left_right.png)

De volgende tabel bevat effectieve regels en regels die mogelijk niet compatibel zijn tijdens runtime:

| Compatibele regels | Mogelijk niet-compatibele regels |
|--- |--- |
| waarde - ligt tussen - 90% en 110% van de verkoopwaarde van het huidige object | salesValue - ligt tussen - 90% en 110% van huidige waarde van object |
| waarde - ligt tussen - 90% en 110% van de huidige waarde van het item | klaringPrijs - ligt tussen - 90% en 110% van marge van huidige post |
| marge - ligt tussen - 90% en 110% van de marge van de huidige post | Winkelvoorraad - gelijk aan - voorraad van huidig object |
| voorraad - is gelijk aan - voorraad van huidig object |  |
