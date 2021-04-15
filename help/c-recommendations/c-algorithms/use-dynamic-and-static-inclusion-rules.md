---
keywords: inclusieregels;inclusiecriteria;aanbevelingen;creeer nieuwe criteria;bevordering;bevordering;dynamisch filtreren;dynamiek;lege waarden;negeren het filtreren regel;statische filter;filter door waarde;entiteitattribuut aanpassing;parameter aanpassing;filter door waarde;statische filter
description: Leer hoe u regels voor deelname maakt in Adobe Target Recommendations voor criteria en promoties. U bereikt betere resultaten door meer dynamische of statische filterregels toe te voegen.
title: Hoe gebruik ik dynamische en statische inclusieregels in Recommendations?
feature: Recommendations
mini-toc-levels: 3
exl-id: 49b20e75-ee55-4239-94a0-6d175e2d4811
translation-type: tm+mt
source-git-commit: 5fcc5776e69222e0a232bd92ddfd10cee748e577
workflow-type: tm+mt
source-wordcount: '1744'
ht-degree: 0%

---

# ![Regels voor dynamische en statische integratie ](/help/assets/premium.png) PREMIUMU gebruiken

Informatie over het creëren van integratieregels voor criteria en bevorderingen in [!DNL Adobe Target] en het toevoegen van dynamische of statische het filtreren regels om betere resultaten voor uw aanbevelingen te bereiken.

Het proces om inclusieregels voor criteria en promoties tot stand te brengen en te gebruiken is gelijkaardig, zoals de gebruiksgevallen en de voorbeelden. In deze afdeling worden zowel de criteria als de promoties en het gebruik van de regels voor inclusie behandeld.

## Filterregels toevoegen aan criteria {#section_CD0D74B8D3BE4A75A78C36CF24A8C57F}

Als u [criteria maakt, klikt u **[!UICONTROL Add Filtering Rule]** onder **[!UICONTROL Inclusion Rules]**.](/help/c-recommendations/c-algorithms/create-new-algorithm.md#task_8A9CB465F28D44899F69F38AD27352FE)

![](assets/inclusion_options_new.png)

Welke opties beschikbaar zijn, is afhankelijk van de verticale en aanbevolen industriesleutel.

## Filterregels toevoegen aan speciale acties {#section_D59AFB62E2EE423086281CF5D18B1076}

Terwijl [een bevordering creëren](/help/c-recommendations/t-create-recs-activity/adding-promotions.md#task_CC5BD28C364742218C1ACAF0D45E0E14), selecteer **[!UICONTROL Promote by Attribute]**, dan klik **[!UICONTROL Add Filtering Rule]**.

![](assets/inclusion_options.png)

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
| [Identieke kenmerk entiteit](/help/c-recommendations/c-algorithms/entity-attribute-matching.md) | Filter dynamisch door een pool van potentiële aanbevelingen punten aan een specifiek punt te vergelijken dat de gebruikers met in wisselwerking staan.<br>Gebruik deze optie  [!UICONTROL Entity Attribute Matching] wanneer u aanbevelingen wilt weergeven die de bezoeker het meest aanspreken, zoals het favoriete merk van de bezoeker. |
| [Overeenkomende profielkenmerken](/help/c-recommendations/c-algorithms/profile-attribute-matching.md) | Filter dynamisch door items (entiteiten) te vergelijken met een waarde in het profiel van de gebruiker.<br>Gebruik deze optie  [!UICONTROL Profile Attribute Matching] als u aanbevelingen wilt weergeven die overeenkomen met een waarde die is opgeslagen in het profiel van de bezoeker, zoals de grootte of het favoriete merk. |
| [Overeenkomende parameters](/help/c-recommendations/c-algorithms/parameter-matching.md) | Filter dynamisch door items (entiteiten) te vergelijken met een waarde in de aanvraag (API of mbox).<br>Gebruik deze optie  [!UICONTROL Parameter Matching] om inhoud aan te bevelen die overeenkomt met de paginaparameters of de parameters van de bezoeker, zoals apparaatafmetingen of geo-locatie. |

### Filteren op waarde

De volgende optie is beschikbaar voor het filtreren door waarde:

| Filteren op waarde, optie | Details |
| --- | --- |
| [Statisch filter](/help/c-recommendations/c-algorithms/static-value.md) | Voer handmatig een of meer statische waarden in die u wilt filteren. |

## Beschikbare operatoren {#operators}

Dynamische criteria en promoties zijn veel krachtiger dan statische criteria en promoties en leveren betere resultaten en betrokkenheid op.

De volgende voorbeelden bieden algemene ideeën over hoe u dynamische promoties en uitsluitingen kunt gebruiken bij uw marketingactiviteiten:

| Operator | Voorbeelden |
| --- | --- |
| Gelijk aan<br> (Beschikbaar met de Vergelijking van de Attributen van de Entiteit, de Vergelijking van de Attributen van het Profiel, de Vergelijking van de Parameter, en Statische Filter.) | Wanneer u de operator &quot;equals&quot; gebruikt in dynamische promoties en een bezoeker een item op uw website weergeeft (zoals een product, artikel of film), kunt u andere items promoten op:<ul><li>Hetzelfde merk</li><li>Dezelfde categorie</li><li>Dezelfde categorie AND van het huismerk</li><li>Dezelfde winkel</li></ul> |
| Niet gelijk<br> (Beschikbaar met de Vergelijking van de Attributen van de Entiteit, de Vergelijking van de Attributen van het Profiel, de Vergelijking van de Parameter, en Statisch filter.) | Met de operator &quot;is niet gelijk aan&quot; in dynamische promoties kunt u andere items promoten via:<ul><li>Een andere tv-serie</li><li>Een ander genre</li><li>Een andere productreeks</li><li>Een andere stijl-id</li></ul> |
| Bevat substring<br> (Beschikbaar met kenmerk Matching van Entiteit, Attributen van het Profiel het Verstemmen, Identieke Parameter, en Statische Filter.) | Wanneer een bezoeker een item op uw website (zoals een product) weergeeft met de operator &quot;contains substring&quot;, kunt u andere items promoten die:<ul><li></li></ul> |  |
| Bevat geen substring<br> (Beschikbaar met kenmerk Matching van Entiteit, Attributen van het Profiel het Verstemmen, Identieke Parameter, en Statische Filter.) | Wanneer u de operator &quot;bevat geen subtekenreeks&quot; gebruikt en een bezoeker een item op uw website weergeeft (zoals een product), kunt u andere items promoten die:<ul><li></li></ul> |
| Begint met<br> (Beschikbaar met de Vergelijking van de Attributen van de Entiteit, de Vergelijking van de Attributen van het Profiel, de Vergelijking van de Parameter, en Statische Filter.) | Wanneer een bezoeker een item op uw website (zoals een product) weergeeft met de operator &quot;start met&quot;, kunt u andere items onder de aandacht brengen die:<ul><li></li></ul> |
| Eindigt met<br> (Beschikbaar met de Vergelijking van de Attributen van de Entiteit, de Vergelijking van de Attributen van het Profiel, de Vergelijking van de Parameter, en Statisch filter.) | Wanneer een bezoeker een item op uw website bekijkt (bijvoorbeeld een product), kunt u andere items promoten met de operator &quot;ends with&quot;:<ul><li></li></ul> |
| Is groter dan of gelijk aan <br> (Beschikbaar met de Vergelijking van de Attributen van de Entiteit, de Vergelijking van de Attributen van het Profiel, de Vergelijking van de Parameter, en Statische Filter.) | Wanneer een bezoeker een item op uw website (zoals een product) bekijkt, gebruikt de operator &quot;is groter dan of gelijk aan&quot;, kunt u andere items promoten die:<ul><li>Kostprijs hetzelfde of duurder</li></ul> |
| Is minder dan of gelijk aan <br> (Beschikbaar met de Vergelijking van de Attributen van de Entiteit, de Vergelijking van de Attributen van het Profiel, de Vergelijking van de Parameter, en Statische Filter.) | Wanneer een bezoeker een item op uw website (zoals een product) bekijkt, gebruikt de operator &quot;is kleiner dan of gelijk aan&quot;, kunt u andere items promoten die:<ul><li>Kostprijs hetzelfde of minder duur</li><li>Objecten uitsluiten die goedkoper zijn</li></ul> |
| Is tussen<br> (Beschikbaar met de Vergelijking van de Attributen van de Entiteit, de Vergelijking van de Attributen van het Profiel, en de Vergelijking van de Parameter.) | Wanneer u de operator &#39;is between&#39; gebruikt in dynamische promoties en een bezoeker een item op uw website weergeeft (zoals een product, artikel of film), kunt u andere items promoten:<ul><li>Meer geld</li><li>Minder duur</li><li>Kosten plus of min 30%</li><li>Later afleveringen in hetzelfde seizoen</li><li>Eerdere boeken in een reeks</li></ul> |
| Bevat in lijst<br> (Beschikbaar met de aanpassing van de Attributen van het Profiel en van de Parameter.) | Wanneer u de operator &quot;bevindt zich in lijst&quot; gebruikt in overeenkomsten met profielkenmerken, kunt u andere items promoten wanneer een bezoeker een item op uw website weergeeft (zoals een product, artikel of film):<ul><li>Beschikbaar in de geografie van de bezoeker</li></ul>Wanneer het gebruiken van deze exploitant, wordt een lijst verwacht in [rechterkant](#caveats) van de regel. |
| Is niet opgenomen in lijst<br> (Beschikbaar met de aanpassing van de Attributen van het Profiel en de Aanpassing van de Parameter.) | Wanneer u de operator &quot;is niet opgenomen in lijst&quot; gebruikt in overeenkomsten met profielkenmerken, kunt u andere items uitsluiten die:<ul><li>In de lijst van de laatste tien items die de bezoeker heeft weergegeven</li></ul></ul>Wanneer het gebruiken van deze exploitant, wordt een lijst verwacht in [rechterkant](#caveats) van de regel. |
| De lijst bevat een punt in<br> (Beschikbaar met de Vergelijking van de Attributen van de Entiteit, de Vergelijking van de Attributen van het Profiel, en de Aanpassing van de Parameter.) | Wanneer u de operator &quot;list contains an item in&quot; gebruikt in overeenkomsten met profielkenmerken, kunt u andere items aanbevelen die zich voordoen wanneer een bezoeker een item op uw website weergeeft (zoals een product, artikel of film):<ul><li>Gekoppeld aan een van de favoriete teams van de bezoeker</li></ul></ul>Wanneer het gebruiken van deze exploitant, wordt een lijst verwacht in [beide kanten](#caveats) van de regel. |
| De lijst bevat geen punt in<br> (Beschikbaar met de Vergelijking van de Attributen van de Entiteit, de Vergelijking van de Attributen van het Profiel, en de Aanpassing van de Parameter.) | Wanneer u de operator &quot;list bevat geen item in&quot; gebruikt in overeenkomende parameterkenmerken, kunt u andere items uitsluiten die:<ul><li>Bevat in een lijst met verboden typen</li></ul>Wanneer het gebruiken van deze exploitant, wordt een lijst verwacht in [beide kanten](#caveats) van de regel. |
| De lijst bevat alle punten in<br> (Beschikbaar met de Vergelijking van de Attributen van de Entiteit, de Vergelijking van de Attributen van het Profiel, en de Aanpassing van de Parameter.) | Wanneer u de operator &quot;list contains all items in&quot; gebruikt in overeenkomende parameterkenmerken, kunt u andere items promoten die:<ul><li></li></ul>Wanneer het gebruiken van deze exploitant, wordt een lijst verwacht in [beide kanten](#caveats) van de regel. |
| De lijst bevat niet alle punten in <br> (Beschikbaar met de Vergelijking van de Attributen van de Entiteit, de Vergelijking van de Attributen van het Profiel, en de Aanpassing van de Parameter.) | Wanneer u de operator &quot;list bevat niet alle items in&quot; gebruikt in overeenkomende parameterkenmerken, kunt u andere items promoten die:<ul><li></li></ul>Wanneer het gebruiken van deze exploitant, wordt een lijst verwacht in [beide kanten](#caveats) van de regel. |

## Lege waarden afhandelen bij het filteren op overeenkomsten van kenmerken van entiteit, overeenkomsten van kenmerken van profiel en overeenkomsten van parameters {#section_7D30E04116DB47BEA6FF840A3424A4C8}

U kunt verschillende opties kiezen om lege waarden af te handelen bij het filteren door [!UICONTROL Entity Attribute Matching], [!UICONTROL Profile Attribute Matching] en [!UICONTROL Parameter Matching] voor afsluitcriteria en -promoties.

Eerder werden geen resultaten geretourneerd als een waarde leeg was. In de vervolgkeuzelijst &quot;If *x* is Empty&quot; kunt u de juiste actie kiezen om uit te voeren als de criteria lege waarden hebben, zoals in de volgende afbeelding wordt getoond:

![](assets/empty_value.png)

Als u de gewenste actie wilt selecteren, houdt u de muisaanwijzer boven het tandwielpictogram (![](assets/icon_gear.png)) en kiest u de gewenste actie:

| Handeling | Beschikbaar voor | Details |
|--- |--- |--- |
| [!UICONTROL Ignore this filtering rule] | [!UICONTROL Profile Attribute Matching] en  [!UICONTROL Parameter Matching] | Deze handeling is de standaardinstelling voor [!UICONTROL Profile Attribute Matching] en [!UICONTROL Parameter Matching].<br>Met deze optie wordt opgegeven dat de regel wordt genegeerd. Bijvoorbeeld, als er drie het filtreren regels zijn en de derde regel geen waarden overgaat, in plaats van om het even welke resultaten terug te keren, kunt u de derde regel met de lege waarden eenvoudig negeren. |
| [!UICONTROL Do not show any results for this criteria]<br>(Alleen criteria) | [!UICONTROL Entity Attribute Matching],  [!UICONTROL Profile Attribute Matching]en  [!UICONTROL Parameter Matching] | Deze actie is het gebrek voor [!UICONTROL Entity Attribute Matching].<br>Zo worden lege waarden vóór de toevoeging van deze optie  [!DNL Target] afgehandeld: voor deze criteria worden geen resultaten getoond . |
| [!UICONTROL Do not promote any items<br>(Alleen aanbiedingen)] | [!UICONTROL Entity Attribute Matching],  [!UICONTROL Profile Attribute Matching]en  [!UICONTROL Parameter Matching] | Deze actie is het gebrek voor [!UICONTROL Entity Attribute Matching].<br>Zo worden lege waarden vóór de toevoeging van deze optie  [!DNL Target] afgehandeld: voor deze criteria worden geen resultaten getoond . |
| [!UICONTROL Use a static value] | [!UICONTROL Entity Attribute Matching],  [!UICONTROL Profile Attribute Matching]en  [!UICONTROL Parameter Matching] | Als een waarde leeg is, kunt u een statische waarde gebruiken. |

## Voorwerpen {#caveats}

>[!IMPORTANT]
>
>Verschillende kenmerken van gegevenstypen zijn mogelijk niet compatibel in dynamische criteria of promoties tijdens runtime met de operatoren &#39;equals&#39; en &#39;does not equal&#39;. Gebruik de waarden [!UICONTROL Value], [!UICONTROL Margin], [!UICONTROL Inventory] en [!UICONTROL Environment] verstandig aan de rechterkant als de linkerkant vooraf gedefinieerde kenmerken of aangepaste kenmerken heeft.

![](assets/left_right.png)

De volgende tabel bevat effectieve regels en regels die mogelijk niet compatibel zijn tijdens runtime:

| Compatibele regels | Mogelijk niet-compatibele regels |
|--- |--- |
| waarde - ligt tussen - 90% en 110% van de verkoopwaarde van het huidige object | salesValue - ligt tussen - 90% en 110% van huidige waarde van object |
| waarde - ligt tussen - 90% en 110% van de huidige waarde van het item | klaringPrijs - ligt tussen - 90% en 110% van marge van huidige post |
| marge - ligt tussen - 90% en 110% van de marge van de huidige post | Winkelvoorraad - gelijk aan - voorraad van huidig object |
| voorraad - is gelijk aan - voorraad van huidig object |  |
