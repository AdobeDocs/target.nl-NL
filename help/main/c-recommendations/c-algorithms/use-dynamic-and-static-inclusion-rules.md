---
keywords: inclusieregels;inclusiecriteria;aanbevelingen;creeer nieuwe criteria;bevordering;bevordering;dynamisch filtreren;dynamiek;lege waarden;negeren het filtreren regel;statische filter;filter door waarde;entiteitattribuut aanpassing;parameter aanpassing;filter door waarde;statische filter
description: Leer hoe u regels voor insluiting maakt in Adobe [!DNL Target] Recommendations voor criteria en promoties. U bereikt betere resultaten door meer dynamische of statische filterregels toe te voegen.
title: Hoe gebruik ik dynamische en statische inclusieregels in Recommendations?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="See what's included in Target Premium."
feature: Recommendations
mini-toc-levels: 3
exl-id: 49b20e75-ee55-4239-94a0-6d175e2d4811
source-git-commit: 07062b7df75300bd7558a24da5121df454520e42
workflow-type: tm+mt
source-wordcount: '1996'
ht-degree: 0%

---

# Regels voor dynamische en statische integratie gebruiken

Informatie over het opstellen van inclusieregels voor criteria en promoties in [!DNL Adobe Target] en het toevoegen van dynamische of statische het filtreren regels om betere resultaten voor uw aanbevelingen te bereiken.

Het proces om inclusieregels voor criteria en promoties tot stand te brengen en te gebruiken is gelijkaardig, zoals de gebruiksgevallen en de voorbeelden. In deze afdeling worden zowel de criteria als de promoties en het gebruik van de regels voor inclusie behandeld.

## Filterregels toevoegen aan criteria {#section_CD0D74B8D3BE4A75A78C36CF24A8C57F}

Terwijl u [criteria maken](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md#task_8A9CB465F28D44899F69F38AD27352FE), klikt u op **[!UICONTROL Add Filtering Rule]** krachtens **[!UICONTROL Inclusion Rules]**.

![include_options_new image](assets/inclusion_options_new.png)

Welke opties beschikbaar zijn, is afhankelijk van de verticale en aanbevolen industriesleutel.

## Filterregels toevoegen aan aanbiedingen {#section_D59AFB62E2EE423086281CF5D18B1076}

while [promoten](/help/main/c-recommendations/t-create-recs-activity/adding-promotions.md#task_CC5BD28C364742218C1ACAF0D45E0E14), selecteert u **[!UICONTROL Promote by Attribute]** en klik vervolgens op **[!UICONTROL Add Filtering Rule]**.

![opname_opties, afbeelding](assets/inclusion_options.png)

## Filtertypen {#section_0125F1ED10A84C0EB45325122460EBCD}

In de volgende secties worden de typen filteropties weergegeven voor [!UICONTROL Dynamic Filtering] en [!UICONTROL Filter by Value] voor zowel criteria als promoties:

### Dynamisch filteren

Dynamische insluitingsregels zijn krachtiger dan statische insluitingsregels en leveren betere resultaten en betrokkenheid op. Overweeg het volgende:

* De dynamische inclusieregels leveren aanbevelingen door een attribuut in de het profielparameter van een gebruiker of in een mbox vraag aan te passen.

   U kunt bijvoorbeeld een aanbeveling met de naam &quot;Populaire criteria&quot; maken. Van de reeks teruggekeerde aanbevelingen, kunt u om het even welke aanbevelingen (in echt - tijd) tegen een attribuut filtreren dat wordt overgegaan wanneer de gebruiker tot een pagina toegang heeft waar de aanbevelingen worden getoond.

* Gebruik statische regels om te beperken welke items worden opgenomen in de aanbeveling (in plaats van verzamelingen te gebruiken).

* U kunt zo veel dynamische inclusieregels tot stand brengen zoals nodig. De inclusieregels worden verbonden met een exploitant AND. Aan alle regels moet worden voldaan om een punt in een aanbeveling te omvatten.

De volgende opties zijn beschikbaar voor dynamisch filteren:

| Dynamisch filteren, optie | Details |
| --- | --- |
| [Identieke kenmerk entiteit](/help/main/c-recommendations/c-algorithms/entity-attribute-matching.md) | Filter dynamisch door een pool van potentiële aanbevelingen punten aan een specifiek punt te vergelijken dat de gebruikers met in wisselwerking staan.<br>Gebruiken [!UICONTROL Entity Attribute Matching] wanneer u aanbevelingen wilt weergeven die de bezoeker het meest waarschijnlijk aanspreken, zoals het favoriete merk van de bezoeker. |
| [Overeenkomende profielkenmerken](/help/main/c-recommendations/c-algorithms/profile-attribute-matching.md) | Filter dynamisch door items (entiteiten) te vergelijken met een waarde in het profiel van de gebruiker.<br>Gebruiken [!UICONTROL Profile Attribute Matching] als u aanbevelingen wilt weergeven die overeenkomen met een waarde die is opgeslagen in het profiel van de bezoeker, zoals de grootte of het favoriete merk. |
| [Overeenkomende parameters](/help/main/c-recommendations/c-algorithms/parameter-matching.md) | Filter dynamisch door items (entiteiten) te vergelijken met een waarde in de aanvraag (API of mbox).<br>Gebruiken [!UICONTROL Parameter Matching] om inhoud aan te bevelen die de paginaparameters of de parameters van de bezoeker, zoals apparatenafmetingen of geo-plaats aanpast. |

### Filteren op waarde

De volgende optie is beschikbaar voor het filtreren door waarde:

| Filteren op waarde, optie | Details |
| --- | --- |
| [Statisch filter](/help/main/c-recommendations/c-algorithms/static-value.md) | Voer handmatig een of meer statische waarden in die u wilt filteren. |

## Beschikbare operatoren {#operators}

Dynamische criteria en promoties zijn veel krachtiger dan statische criteria en promoties en leveren betere resultaten en betrokkenheid op.

De volgende voorbeelden bieden algemene ideeën over hoe u dynamische promoties en uitsluitingen kunt gebruiken bij uw marketingactiviteiten:

| Operator | Voorbeelden |
| --- | --- |
| Gelijk<br>(Beschikbaar bij de Vergelijking van kenmerken van entiteiten, de Vergelijking van attributen van het Profiel, de Vergelijking van de Parameter, en Statische Filter.) | Wanneer u de operator &quot;equals&quot; gebruikt in dynamische promoties en een bezoeker een item op uw website bekijkt (zoals een product, artikel of film), kunt u andere items promoten op:<ul><li>Hetzelfde merk</li><li>Dezelfde categorie</li><li>Dezelfde categorie AND van het huismerk</li><li>Dezelfde winkel</li></ul> |
| Niet gelijk<br>(Beschikbaar bij de Vergelijking van kenmerken van entiteiten, de Vergelijking van attributen van het Profiel, de Vergelijking van de Parameter, en Statische Filter.) | Met de operator &quot;is niet gelijk aan&quot; in dynamische promoties kunt u andere items promoten via:<ul><li>Een andere tv-serie</li><li>Een ander genre</li><li>Een andere productreeks</li><li>Een andere stijl-id</li></ul> |
| Bevat geen subtekenreeks<br>(Beschikbaar bij de Vergelijking van kenmerken van entiteiten, de Vergelijking van attributen van het Profiel, de Vergelijking van de Parameter, en Statische Filter.) | Wanneer u de operator &quot;bevat geen subtekenreeks&quot; gebruikt en een bezoeker een item op uw website weergeeft (zoals een product), kunt u andere items promoten die:<ul><li>Titel bevat geen woord zweren</li></ul> |
| Begint met<br>(Beschikbaar bij de Vergelijking van kenmerken van entiteiten, de Vergelijking van attributen van het Profiel, de Vergelijking van de Parameter, en Statische Filter.) | Wanneer een bezoeker een item op uw website (zoals een product) weergeeft met de operator &quot;start met&quot;, kunt u andere items onder de aandacht brengen die:<ul><li>De productnaam begint met iPhone</li></ul> |
| Eindigt met<br>(Beschikbaar bij de Vergelijking van kenmerken van entiteiten, de Vergelijking van attributen van het Profiel, de Vergelijking van de Parameter, en Statische Filter.) | Wanneer een bezoeker een item op uw website bekijkt (bijvoorbeeld een product), kunt u andere items promoten met de operator &quot;ends with&quot;:<ul><li>Inhoud eindigt met NL, die de Engelse taal aangeeft</li></ul> |
| Is groter dan of gelijk aan<br>(Beschikbaar bij de Vergelijking van kenmerken van entiteiten, de Vergelijking van attributen van het Profiel, de Vergelijking van de Parameter, en Statische Filter.) | Wanneer een bezoeker een item op uw website (zoals een product) bekijkt, gebruikt de operator &quot;is groter dan of gelijk aan&quot;, kunt u andere items promoten die:<ul><li>Kostprijs hetzelfde of duurder</li></ul> |
| is kleiner dan of gelijk aan<br>(Beschikbaar bij de Vergelijking van kenmerken van entiteiten, de Vergelijking van attributen van het Profiel, de Vergelijking van de Parameter, en Statische Filter.) | Wanneer een bezoeker een item op uw website (zoals een product) bekijkt, gebruikt de operator &quot;is kleiner dan of gelijk aan&quot;, kunt u andere items promoten die:<ul><li>Kostprijs hetzelfde of minder duur</li><li>Objecten uitsluiten die goedkoper zijn</li></ul> |
| Is tussen<br>(Beschikbaar bij Identieke eigenschappen van Entiteit, Identieke Attributen van het Profiel, en de Vergelijking van de Parameter.) | Wanneer u de operator &#39;is between&#39; gebruikt in dynamische promoties en een bezoeker een item op uw website weergeeft (zoals een product, artikel of film), kunt u andere items promoten:<ul><li>Meer geld</li><li>Minder duur</li><li>Kosten plus of min 30%</li><li>Later afleveringen in hetzelfde seizoen</li><li>Eerdere boeken in een reeks</li></ul> |
| Is opgenomen in lijst<br>(Beschikbaar met aanpassing van profielkenmerken en parameters.) | Wanneer u de operator &quot;bevindt zich in lijst&quot; gebruikt in overeenkomsten met profielkenmerken, kunt u andere items promoten wanneer een bezoeker een item op uw website weergeeft (zoals een product, artikel of film):<ul><li>Beschikbaar in de geografie van de bezoeker</li></ul>**Voorbeeld**: Je wilt alleen objecten aanbevelen die beschikbaar zijn in het geografische gebied van een bezoeker.<br>Uw filterregel kan er als volgt uitzien:<br>`availableGeographies list contains an item in user.currentGeography`<br>**Opmerking**: Wanneer u deze operator gebruikt, wordt een lijst verwacht in het dialoogvenster [rechterkant](#caveats) van de regel. |
| Is niet opgenomen in lijst<br>(Beschikbaar met aanpassing van profielkenmerken en parameters.) | Wanneer u de operator &quot;is niet opgenomen in lijst&quot; gebruikt in overeenkomsten met profielkenmerken, kunt u andere items uitsluiten die:<ul><li>In de lijst van de laatste tien items die de bezoeker heeft weergegeven</li></ul></ul>**Voorbeeld**: Je wilt geen objecten promoten die de bezoeker onlangs heeft bekeken en waarin hij geen interesse heeft getoond.<br>Uw filterregel zou als kunnen kijken:<br>`id is not contained in list user.lastViewedItems`<br>**Opmerking**: Wanneer u deze operator gebruikt, wordt een lijst verwacht in het dialoogvenster [rechterkant](#caveats) van de regel. |
| Lijst bevat een item in<br>(Beschikbaar bij Identieke eigenschappen van Entiteit, Identieke Attributen van het Profiel, en de Vergelijking van de Parameter.) | Als u de operator &quot;list contains an item in&quot; gebruikt in overeenkomsten met profielkenmerken, kunt u andere items promoten die:<ul><li>Gekoppeld aan een van de favoriete teams van de bezoeker</li></ul>**Voorbeeld**: Je wilt games aanbevelen die zijn gekoppeld aan een van de favoriete teams van de bezoeker.<br>Uw filterregel zou als kunnen kijken:<br>` teamsPlaying list contains an item in user.favoriteTeams`<br>**Opmerking**: Wanneer u deze operator gebruikt, wordt een lijst verwacht in [beide zijden](#caveats) van de regel. |
| Lijst bevat geen item in<br>(Beschikbaar bij Identieke eigenschappen van Entiteit, Identieke Attributen van het Profiel, en de Vergelijking van de Parameter.) | Wanneer u de operator &quot;list bevat geen item in&quot; gebruikt in overeenkomende parameterkenmerken, kunt u andere items uitsluiten die:<ul><li>Bevat in een lijst met verboden typen</li></ul>**Voorbeeld**: U wilt items uitsluiten die beschikbaar zijn voor volwassenen, zoals tabak en alcohol.<br>Uw filterregel zou als kunnen kijken:<br>`itemType is not contained in list mbox.prohibitedTypes`<br>**Opmerking**: Wanneer u deze operator gebruikt, wordt een lijst verwacht in [beide zijden](#caveats) van de regel. |
| Lijst bevat alle items in<br>(Beschikbaar bij Identieke eigenschappen van Entiteit, Identieke Attributen van het Profiel, en de Vergelijking van de Parameter.) | Als u de operator &quot;list contains all items in&quot; gebruikt in overeenkomsten met profielkenmerken, kunt u andere items promoten die door een bezoeker worden weergegeven op uw website (bijvoorbeeld posten of recept):<ul><li>Een set vaardigheden opnemen</li><li>Een set vereiste ingrediënten opnemen</li></ul>**Voorbeeld 1**: Stel dat een bezoeker een reeks vaardigheden heeft (Java, C++ en HTML). De items in de catalogus zijn taken met de vereiste vaardigheden (Java en HTML). U wilt ervoor zorgen dat het profiel van de bezoeker alle vereiste vaardigheden bevat voordat u de taak aan de bezoeker aanbeveelt.<br>Uw filterregel zou als kunnen kijken:<br>`profile.jobSeekerSkills contains all items in entity.requiredSkills`<br>**Voorbeeld 2**: Stel dat een gebruiker een lijst heeft met ingrediënten in het deelvenster. Het recept bevat een lijst van de vereiste ingrediënten. U wilt ervoor zorgen dat het profiel van de bezoeker alle vereiste ingrediënten bevat voordat u het recept aan de bezoeker aanbeveelt.<br>Uw filterregel zou als kunnen kijken:<br>`profile.ingredientsInPantry contains all items in recipe.ingredientsRequired`<br>**Opmerking**: Wanneer u deze operator gebruikt, wordt een lijst verwacht in [beide zijden](#caveats) van de regel. |
| Lijst bevat niet alle items in<br>(Beschikbaar bij Identieke eigenschappen van Entiteit, Identieke Attributen van het Profiel, en de Vergelijking van de Parameter.) | Als u de operator &quot;list bevat niet alle items in&quot; gebruikt in overeenkomsten met entiteitskenmerken, kunt u andere items promoten die:<ul><li>Geen set met teams opnemen</li></ul>**Voorbeeld**: Stel dat een sportevenement twee teams omvat. Het profiel van de bezoeker geeft aan dat deze bezoeker geen games voor deze teams wil weergeven. U wilt ervoor zorgen dat u geen spel aanbeveelt als deze teams spelen.<br>Uw filterregel zou als kunnen kijken:<br>`profile.leastfavoriteTeams does not contain all items in entity.teamsPlaying`<br>**Opmerking**: Wanneer u deze operator gebruikt, wordt een lijst verwacht in [beide zijden](#caveats) van de regel. |

## Lege waarden afhandelen bij het filteren op overeenkomsten van kenmerken van entiteit, overeenkomsten van kenmerken van profiel en overeenkomsten van parameters {#section_7D30E04116DB47BEA6FF840A3424A4C8}

U kunt verschillende opties kiezen om lege waarden af te handelen tijdens het filteren door [!UICONTROL Entity Attribute Matching], [!UICONTROL Profile Attribute Matching], en [!UICONTROL Parameter Matching] voor uitstapcriteria en promoties.

Eerder werden geen resultaten geretourneerd als een waarde leeg was. &quot;if *x* is Lege&quot; in de vervolgkeuzelijst, kunt u de juiste handeling kiezen om uit te voeren als de criteria lege waarden hebben, zoals in de volgende afbeelding wordt getoond:

![empty_value image](assets/empty_value.png)

Houd de muisaanwijzer boven het tandwielpictogram (![icon_tandbeeld](assets/icon_gear.png)) en kiest u de gewenste actie:

| Handeling | Beschikbaar voor | Details |
|--- |--- |--- |
| [!UICONTROL Ignore this filtering rule] | [!UICONTROL Profile Attribute Matching] en [!UICONTROL Parameter Matching] | Deze handeling is de standaardinstelling voor [!UICONTROL Profile Attribute Matching] en [!UICONTROL Parameter Matching].<br>Met deze optie wordt opgegeven dat de regel wordt genegeerd. Bijvoorbeeld, als er drie het filtreren regels zijn en de derde regel geen waarden overgaat, in plaats van om het even welke resultaten terug te keren, kunt u de derde regel met de lege waarden eenvoudig negeren. |
| [!UICONTROL Do not show any results for this criteria]<br>(Alleen criteria) | [!UICONTROL Entity Attribute Matching], [!UICONTROL Profile Attribute Matching], en [!UICONTROL Parameter Matching] | Deze handeling is de standaardinstelling voor [!UICONTROL Entity Attribute Matching].<br>Deze actie is hoe [!DNL Target] lege waarden afgehandeld vóór de toevoeging van deze optie: voor deze criteria worden geen resultaten getoond . |
| [!UICONTROL Do not promote any items<br>(Alleen aanbiedingen)] | [!UICONTROL Entity Attribute Matching], [!UICONTROL Profile Attribute Matching], en [!UICONTROL Parameter Matching] | Deze handeling is de standaardinstelling voor [!UICONTROL Entity Attribute Matching].<br>Deze actie is hoe [!DNL Target] lege waarden afgehandeld vóór de toevoeging van deze optie: voor deze criteria worden geen resultaten getoond . |
| [!UICONTROL Use a static value] | [!UICONTROL Entity Attribute Matching], [!UICONTROL Profile Attribute Matching], en [!UICONTROL Parameter Matching] | Als een waarde leeg is, kunt u een statische waarde gebruiken. |

## Caveats {#caveats}

>[!IMPORTANT]
>
>Verschillende kenmerken van gegevenstypen zijn mogelijk niet compatibel in dynamische criteria of promoties tijdens runtime met de operatoren &#39;equals&#39; en &#39;does not equal&#39;. Gebruiken [!UICONTROL Value], [!UICONTROL Margin], [!UICONTROL Inventory], en [!UICONTROL Environment] Aan de rechterkant verstandig als de linkerkant vooraf gedefinieerde kenmerken of aangepaste kenmerken heeft.

![afbeelding left_right](assets/left_right.png)

De volgende tabel bevat effectieve regels en regels die mogelijk niet compatibel zijn tijdens runtime:

| Compatibele regels | Mogelijk niet-compatibele regels |
|--- |--- |
| waarde - ligt tussen - 90% en 110% van de verkoopwaarde van het huidige object | salesValue - ligt tussen - 90% en 110% van huidige waarde van object |
| waarde - ligt tussen - 90% en 110% van de huidige waarde van het item | klaringPrijs - ligt tussen - 90% en 110% van marge van huidige post |
| marge - ligt tussen - 90% en 110% van de marge van de huidige post | Winkelvoorraad - gelijk aan - voorraad van huidig object |
| voorraad - is gelijk aan - voorraad van huidig object |  |
