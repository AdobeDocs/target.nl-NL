---
keywords: inclusion rules;inclusion criteria;recommendations;create new criteria;promotion;promotions;dynamic filtering;dynamic;empty values;ignore filtering rule;static filter;filter by value;entity attribute matching;profile attribute matching;parameter matching;filter by value;static filter
description: Informatie over het creëren van inclusieregels in Adobe Target Recommendations voor criteria en bevorderingen, en het toevoegen van extra dynamische of statische het filtreren regels om betere resultaten te bereiken.
title: Regels voor dynamische en statische integratie gebruiken in Adobe Target Recommendations
feature: criteria
uuid: f0ee2086-1126-44a4-9379-aa897dc0e06b
translation-type: tm+mt
source-git-commit: 3cf1f4fa56f86c106dccdc2c97c080c17c3982b4
workflow-type: tm+mt
source-wordcount: '1433'
ht-degree: 0%

---


# ![PREMIUM](/help/assets/premium.png) : dynamische en statische inclusieregels gebruiken{#use-dynamic-and-static-inclusion-rules}

Informatie over het creëren van inclusieregels voor criteria en bevorderingen, en het toevoegen van extra dynamische of statische het filtreren regels om betere resultaten te bereiken.

Het proces om inclusieregels voor criteria en promoties tot stand te brengen en te gebruiken is gelijkaardig, zoals de gebruiksgevallen en de voorbeelden. Zowel criteria als promoties en het gebruik van inclusieregels worden in dit onderwerp behandeld.

## Filterregels toevoegen aan criteria {#section_CD0D74B8D3BE4A75A78C36CF24A8C57F}

Terwijl u criteria [](../../c-recommendations/c-algorithms/create-new-algorithm.md#task_8A9CB465F28D44899F69F38AD27352FE)creeert, klik **[!UICONTROL Add Filtering Rule]** onder **[!UICONTROL Inclusion Rules]**.

![](assets/inclusion_options.png)

Welke opties beschikbaar zijn, is afhankelijk van de verticale en aanbevolen industriesleutel.

## Filterregels toevoegen aan aanbiedingen {#section_D59AFB62E2EE423086281CF5D18B1076}

Selecteer tijdens het [maken van een aanbieding](../../c-recommendations/t-create-recs-activity/adding-promotions.md#task_CC5BD28C364742218C1ACAF0D45E0E14)de optie **[!UICONTROL Promote by Attribute]** en klik op **[!UICONTROL Add Filtering Rule]**.

![](assets/inclusion_options_promotion.png)

## Filtertypen {#section_0125F1ED10A84C0EB45325122460EBCD}

In de volgende tabel worden de typen filteropties voor zowel criteria als promoties weergegeven:

| Type | Option | Beschikbare operatoren |
|--- |--- |--- |
| **Dynamisch filteren** | **Identieke overeenkomst kenmerk entiteit:** Filter dynamisch door een pool van potentiële aanbevelingen punten aan een specifiek punt te vergelijken dat de gebruikers met in wisselwerking staan.<br>U kunt bijvoorbeeld alleen items aanbevelen die overeenkomen met het merk van het huidige item. | <br>equalsdoes not<br>equalis<br><br>between containers does not<br>contains arts<br>withends<br>with value is<br>present value is not<br>presence greater than or equal<br>to of equal |
|  | **Overeenkomende profielkenmerken:** Filter dynamisch door items (entiteiten) te vergelijken met een waarde in het profiel van de gebruiker.<br>U kunt bijvoorbeeld alleen objecten aanbevelen die overeenkomen met het favoriete merk van de bezoeker. | equalcontainers<br> bevat geen<br><br>gelijkmatige<br>lagen<br>met een<br>groter dan of gelijk<br>aan het verschil<br>tussen |
|  | **Overeenkomende parameters:** Filter dynamisch door items (entiteiten) te vergelijken met een waarde in de aanvraag (API of mbox).<br>U kunt bijvoorbeeld alleen inhoud aanbevelen die overeenkomt met de pagina-parameter &#39;industrie&#39;.<br>**Belangrijk:** Als de activiteit vóór 31 oktober 2016 werd gecreeerd, zal zijn levering ontbreken als het de &quot;Aanpassing van de Parameter&quot;filter gebruikt. U kunt dit probleem als volgt oplossen:<ul><li>Maak een nieuwe activiteit en voeg daar uw criteria aan toe.</li><li>Gebruik een criterium dat het filter &quot;Parameter Matching&quot; niet bevat.</li><li>Verwijder het filter &quot;Parameter Matching&quot; uit de criteria.</li></ul> | <br>equalsi bevat geen<br><br>gelijkmatige insluiting en geen<br>kunststofverbindingen<br>met een<br>waarde groter dan of gelijk<br>aan die tussen<br>de |
| **Filteren op waarde** | **Statisch filter:** Voer handmatig een of meer statische waarden in die u wilt filteren.<br>U kunt bijvoorbeeld alleen inhoud met een MPAA-score van &quot;G&quot; of &quot;PG&quot; aanbevelen. | <br>equalsdoes not<br><br>equalcontainers contains not<br>content<br>withends<br>with value is<br>present value is not<br>present greater than or equal<br>to less than or equal to |

>[!NOTE]
>
>Als u vertrouwd met bent hoe de inclusieregels voorafgaand aan Doel 17.6.1 versie (Juni 2017) werden gevormd, zult u merken dat sommige opties en exploitanten zijn veranderd. Alleen de operatoren die van toepassing zijn op de geselecteerde optieweergave en sommige operatoren hebben een andere naam gekregen (&quot;overeenkomsten&quot; zijn nu &quot;gelijk&quot;), zodat ze consistenter en intuïtiever zijn. Alle bestaande uitsluitingsregels die vóór deze release zijn gemaakt, zijn automatisch naar de nieuwe structuur gemigreerd. Van uw kant is geen herstructurering nodig.

U kunt zo veel inclusieregels tot stand brengen zoals nodig. De inclusieregels worden verbonden met een exploitant AND. Aan alle regels moet worden voldaan om een punt in een aanbeveling te omvatten.

Dynamische criteria en promoties zijn veel krachtiger dan statische criteria en promoties en leveren betere resultaten en betrokkenheid op. De volgende voorbeelden geven u ideeën over hoe u dynamische promoties kunt gebruiken bij uw marketingactiviteiten:

**Gelijk aan:** Wanneer u de operator &quot;equals&quot; gebruikt in dynamische promoties en een bezoeker een item op uw website weergeeft (zoals een product, artikel of film), kunt u andere items promoten op:

* hetzelfde merk
* dezelfde categorie
* dezelfde categorie AND van het huismerk
* dezelfde winkel

**Niet gelijk:** Met de operator &quot;is niet gelijk aan&quot; in dynamische promoties kunt u andere items promoten via:

* een andere tv-serie
* een ander genre
* een andere productreeks
* een andere stijl-id

**Is tussen:** Wanneer u de operator &#39;is between&#39; gebruikt in dynamische promoties en een bezoeker een item op uw website weergeeft (zoals een product, artikel of film), kunt u andere items promoten:

* duurder
* goedkoper
* kosten plus of minus 30%
* latere episodes in hetzelfde seizoen
* eerdere boeken in een reeks

## Lege waarden afhandelen bij het filteren op overeenkomst van kenmerk Entiteit, Afstemming van kenmerken profiel en Overeenkomende parameters {#section_7D30E04116DB47BEA6FF840A3424A4C8}

U kunt verschillende opties kiezen om lege waarden af te handelen wanneer u filtert op Vergelijking kenmerk entiteit, Vergelijking kenmerk profiel en Vergelijking parameter voor exit-criteria en -promoties.

Eerder werden geen resultaten geretourneerd als een waarde leeg was. In de vervolgkeuzelijst &quot;If *x* is Empty&quot; (Als x leeg is) kunt u de juiste actie kiezen om uit te voeren als de criteria lege waarden hebben, zoals in de volgende afbeelding wordt getoond:

![](assets/empty_value.png)

Als u de gewenste actie wilt selecteren, houdt u de muisaanwijzer boven het tandwielpictogram (![](assets/icon_gear.png)) en kiest u de gewenste actie:

| Handeling | Beschikbaar voor | Details |
|--- |--- |--- |
| Deze filterregel negeren | Profielkenmerk<br>MatchingParameter Matching | Dit is de standaardactie voor het Aanpassen van Attributen van het Profiel en de Aanpassing van de Parameter.<br>Met deze optie wordt opgegeven dat de regel wordt genegeerd. Bijvoorbeeld, als er drie het filtreren regels zijn en de derde regel geen waarden overgaat, in plaats van om het even welke resultaten terug te keren, kunt u de derde regel met de lege waarden eenvoudig negeren. |
| Geen resultaten tonen voor deze criteria | Identiteitskenmerk<br>MatchingProfile-kenmerk<br>MatchingParameter Matching | Dit is de standaardhandeling voor overeenkomsten van entiteitskenmerken.<br>Deze actie is hoe Doel lege waarden vóór de toevoeging van deze optie behandelde: voor deze criteria zullen geen resultaten worden getoond . |
| Een statische waarde gebruiken | Identiteitskenmerk<br>MatchingProfile-kenmerk<br>MatchingParameter Matching | Als een waarde leeg is, kunt u een statische waarde gebruiken. |

## Voorbeelden van overeenkomsten van profielkenmerken {#section_9873E2F22E094E479569D05AD5BB1D40}

[!UICONTROL Profile Attribute Matching] Hiermee kunt u alleen de items aanbevelen die overeenkomen met een kenmerk uit het profiel van de bezoeker, zoals in de onderstaande voorbeelden.

**Voorbeeld 1: Aanbevolen items van het favoriete merk** van de gebruiker. Met de [!UICONTROL Profile Attribute Matching] optie kunt u bijvoorbeeld een regel maken die alleen items aanbeveelt als het merk gelijk is aan de waarde of tekst in `profile.favoritebrand`. Met een dergelijke regel geldt dat als een bezoeker korte berichten van een bepaald merk bekijkt, alleen aanbevelingen worden weergegeven die overeenkomen met het favoriete merk van die gebruiker (de waarde die is opgeslagen in het profiel van de bezoeker). `profile.favoritebrand`

```
Profile Attribute Matching
brand - equals - the value/text stored in - profile.favoritebrand
```

**Voorbeeld 2: banen afstemmen op werkzoekenden** Stel dat je probeert banen af te stemmen op werkzoekenden. U wilt alleen taken aanbevelen die zich in dezelfde stad bevinden als de werkzoekende.

U kunt inclusieregels gebruiken om de plaats van een baanzoeker van het profiel van zijn of haar bezoeker aan een baanlijst aan te passen, zoals in het volgende voorbeeld:

```
Profile Attribute Matching
jobCity - equals - the value/text stored in - profile.usersCity
```

## Overeenkomende voorbeelden van kenmerken van entiteiten

[!UICONTROL Entity Attribute Matching] Hiermee kunt u alleen de items aanbevelen die overeenkomen met een kenmerk van het item dat de gebruiker momenteel bekijkt, het item dat de gebruiker het laatst heeft weergegeven, het item dat de gebruiker het laatst heeft aangeschaft, het item dat de gebruiker het vaakst heeft weergegeven of een item dat is opgeslagen in een aangepast kenmerk in het profiel van de bezoeker, zoals in de onderstaande voorbeelden.

**Voorbeeld 3: Upselling naar een duurder product** Stel dat je een detailhandelaar bent in de kledingindustrie en gebruikers wil aanmoedigen om duurdere en dus winstgevender objecten te overwegen. U kunt de operatoren ‘gelijk aan’ en ‘gelijk aan’ gebruiken om duurdere objecten van dezelfde categorie en hetzelfde merk te promoten. Een bezoeker die bijvoorbeeld een lopend bedrijf ziet, kan duurdere loopschoenen promoten in een poging om een bezoeker die op zoek is naar loopschoenen te upverkopen.

```
Entity Attribute Matching
category - equals - current item's - category 
And 
Entity Attribute Matching
brand - equals - current item's - brand 
And 
Entity Attribute Matching
value - is between - 100% and 1000% of - current item's - value
```

**Voorbeeld 4: Het bevorderen van privé-etiketproducten** U kunt dynamische en statische filters mengen om privé-etiketproducten te bevorderen. Zo kan een kantoorbedrijf bijvoorbeeld tonercartridges van het huismerk van het bedrijf promoten om een rendabelere verkoop te stimuleren voor een bezoeker die naar toner kijkt — en pennen van het huismerk van het bedrijf promoten om een rendabelere verkoop te drijven voor een bezoeker die naar pennen kijkt.

```
Entity Attribute Matching
category - equals - current item's - category 
And
Static Filter
IsHouseBrand - equals - true
```

## Caveats {#section_A889FAF794B7458CA074DEE06DD0E345}

>[!IMPORTANT]
>
>Verschillende kenmerken van gegevenstypen zijn mogelijk niet compatibel in dynamische criteria of promoties tijdens runtime met de operatoren &#39;equals&#39; en &#39;does not equal&#39;. U zou waarden van de Waarde, van de Marge, van de Inventaris, en van het Milieu verstandiger aan de rechterkant moeten gebruiken als de linkerkant vooraf bepaalde attributen of douaneattributen heeft.

![](assets/left_right.png)

De volgende tabel bevat effectieve regels en regels die mogelijk niet compatibel zijn tijdens runtime:

| Compatibele regels | Mogelijk niet-compatibele regels |
|--- |--- |
| waarde - ligt tussen - 90% en 110% van de verkoopwaarde van het huidige object | salesValue - ligt tussen - 90% en 110% van huidige waarde van object |
| waarde - ligt tussen - 90% en 110% van de huidige waarde van het item | klaringPrijs - ligt tussen - 90% en 110% van marge van huidige post |
| marge - ligt tussen - 90% en 110% van de marge van de huidige post | Winkelvoorraad - gelijk aan - voorraad van huidig object |
| voorraad - is gelijk aan - voorraad van huidig object |  |
