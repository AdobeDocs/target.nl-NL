---
keywords: inclusion rules;inclusion criteria;recommendations;promotion;promotions;dynamic filtering;dynamic;entity attribute matching
description: Filter dynamisch in Adobe Target Recommendations door een pool van potentiële aanbevelingen punten aan een specifiek punt te vergelijken dat de gebruiker met heeft in wisselwerking gestaan.
title: Filter op kenmerk van entiteit matchen in regels voor dynamische insluiting in Adobe Target Recommendations
feature: criteria
translation-type: tm+mt
source-git-commit: b51c980d8e7db3ee574350a04f9056fe5b00a703
workflow-type: tm+mt
source-wordcount: '351'
ht-degree: 0%

---


# ![PREMIUM](/help/assets/premium.png) -overeenkomst kenmerk entiteit

Filter dynamisch in [!DNL Adobe Target] [!DNL Recommendations] door een pool van potentiële aanbevelingen punten aan een specifiek punt te vergelijken dat de gebruiker met heeft in wisselwerking gestaan.

Bijvoorbeeld, adviseer slechts punten die het merk van het huidige punt zoals in het volgende voorbeeld aanpassen:

Als de mbox op een Brand Landing Page terugkeert `entity.brand=Nike`, worden alleen Nike-producten geretourneerd en op die pagina weergegeven. Op dezelfde manier worden op de pagina Brand Landing voor Adidas alleen Adidas-producten geretourneerd. Met dit type van dynamische inclusieregel, moet de gebruiker slechts één adviseringsregel specificeren die relevante merkresultaten over alle merkpagina&#39;s eerder dan het specificeren van een inzameling of een statische filter om elke merknaam te passen.

## Overeenkomende voorbeelden van kenmerken van entiteiten

[!UICONTROL Entity Attribute Matching] Hiermee kunt u alleen de overeenkomende items aanbevelen, bijvoorbeeld:

* Een kenmerk van het item dat de gebruiker momenteel weergeeft
* Het item dat de gebruiker het laatst heeft bekeken
* Het item dat de gebruiker het laatst heeft aangeschaft
* Het item dat de gebruiker het vaakst heeft bekeken
* Een item dat is opgeslagen in een aangepast kenmerk in het profiel van de bezoeker

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
