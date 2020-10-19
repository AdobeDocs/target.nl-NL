---
keywords: inclusion rules;inclusion criteria;recommendations;promotion;promotions;dynamic filtering;dynamic;entity attribute matching
description: Filter dynamisch in Adobe Target Recommendations door een pool van potentiële aanbevelingen punten aan een specifiek punt te vergelijken dat de gebruiker met heeft in wisselwerking gestaan.
title: Filter op kenmerk van entiteit matchen in regels voor dynamische insluiting in Adobe Target Recommendations
feature: criteria
translation-type: tm+mt
source-git-commit: c814215476ef6e40f4f175fe3f9dbb2c26b966eb
workflow-type: tm+mt
source-wordcount: '497'
ht-degree: 0%

---


# ![PREMIUM](/help/assets/premium.png) -overeenkomst kenmerk entiteit

Filter dynamisch in [!DNL Adobe Target] [!DNL Recommendations] door een pool van potentiële aanbevelingen punten aan een specifiek punt te vergelijken dat de gebruiker met heeft in wisselwerking gestaan.

>[!NOTE]
>
>Het [proces voor het creëren en gebruiken van inclusieregels](/help/c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md) voor criteria en bevorderingen is gelijkaardig, zoals de gebruiksgevallen en de voorbeelden.

U kunt bijvoorbeeld alleen items aanbevelen die overeenkomen met het merk van het huidige item, zoals in het volgende voorbeeld:

Als de mbox op een Brand Landing Page terugkeert `entity.brand=Nike`, worden alleen Nike-producten geretourneerd en op die pagina weergegeven. Op dezelfde manier worden op de pagina Brand Landing voor Adidas alleen Adidas-producten geretourneerd. Met dit type van dynamische integratieregel, moet de gebruiker slechts één aanbeveling specificeren die relevante merkresultaten over alle merkpagina&#39;s eerder dan het specificeren van een inzameling of een statische filter om elke merknaam te passen terugkeert.

Dit werkt alleen als u de code `entity.brand` in de mbox op die bestemmingspagina&#39;s levert.

## Voorbeelden van overeenkomsten van entiteitskenmerken

[!UICONTROL Entity Attribute Matching] Hiermee kunt u alleen de overeenkomende items aanbevelen, bijvoorbeeld:

* Een kenmerk van het item dat de gebruiker momenteel weergeeft
* Het item dat de gebruiker het laatst heeft bekeken
* Het item dat de gebruiker het laatst heeft aangeschaft
* Het item dat de gebruiker het vaakst heeft bekeken
* Een item dat is opgeslagen in een aangepast kenmerk in het profiel van de bezoeker

### Aanbevolen objecten op basis van een merk

Nadat de regels voor de entiteitskenmerken zijn samengesteld, worden alle aanbevelingen met kenmerken uitgefilterd die niet overeenkomen met de entiteitswaarde die op de pagina wordt doorgegeven.

In het volgende voorbeeld worden aanbevelingen getoond die overeenkomen met het productmerk dat op de pagina wordt weergegeven:

Wanneer u een pagina bezoekt die een Nike-product bevat, stelt de pagina de waarde van de `entity.brand` parameter in op &quot;Nike&quot;.

![Voorbeeld van doelaanroep](/help/c-recommendations/c-algorithms/assets/example-target-call.png)

In de aanbevelingen op de pagina ziet u alleen Nike-producten.

![Nike-aanbevelingen](/help/c-recommendations/c-algorithms/assets/nike.png)

Als u vervolgens een Adidas-productpagina weergeeft, wordt de `entity.brand` waarde weer ingesteld op &quot;Adidas&quot; en worden Adidas-producten aanbevolen op de Adidas-productpagina&#39;s.

![Adidas-aanbevelingen](/help/c-recommendations/c-algorithms/assets/adidas.png)

### Upsellen naar een duurder product

Stel dat u een kledinghandelaar bent en gebruikers wilt aanmoedigen om duurdere en daarom rendabelere voorwerpen te overwegen. U kunt de operatoren ‘gelijk aan’ en ‘gelijk aan’ gebruiken om duurdere objecten van dezelfde categorie en hetzelfde merk te promoten. Een schoenenhandelaar kan bijvoorbeeld duurdere loopschoenen promoten in een poging om een bezoeker die naar lopende schoenen kijkt, te uploaden, zoals in het volgende codevoorbeeld:

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

### Privéproducten promoten

U kunt dynamische en statische filters mengen om privé-etiketproducten te bevorderen. Zo kan een kantoorbedrijf bijvoorbeeld tonercartridges van het huismerk van het bedrijf promoten om een rendabelere verkoop aan te sturen voor een bezoeker die naar toner kijkt — en pennen van het huismerk van het bedrijf promoten om een winstgevender verkoop te stimuleren voor een bezoeker die naar pennen kijkt, zoals in het volgende codevoorbeeld:

```
Entity Attribute Matching
category - equals - current item's - category 
And
Static Filter
IsHouseBrand - equals - true
```
