---
keywords: inclusieregels;inclusiecriteria;aanbevelingen;bevordering;bevordering;dynamische filtering;dynamic;entiteitattributen die aanpassen
description: Leer hoe u dynamisch filtert in Adobe [!DNL Target] Recommendations door een groep potentiële items te vergelijken met een specifiek item waarmee de gebruiker heeft gewerkt.
title: Hoe filtert ik op kenmerk Entiteit die overeenkomt met Recommendations-activiteiten?
feature: Recommendations
exl-id: aadd3132-d590-4dc9-b01b-bedf41bc7441
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '520'
ht-degree: 0%

---

# ![PREMIUM](/help/main/assets/premium.png) Identieke kenmerk entiteit

Dynamisch filteren in [!DNL Adobe Target] [!DNL Recommendations] door een pool van potentiële aanbevelingen punten met een specifiek punt te vergelijken dat de gebruiker met heeft in wisselwerking gestaan.

>[!NOTE]
>
>De [proces voor het opstellen en gebruiken van inclusieregels](/help/main/c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md) wat criteria en promoties betreft , zijn deze vergelijkbaar met de gebruiksgevallen en - voorbeelden .

U kunt bijvoorbeeld alleen items aanbevelen die overeenkomen met het merk van het huidige item, zoals in het volgende voorbeeld:

Als de mbox op een pagina voor landingen merk wordt geretourneerd `entity.brand=brandA`Vervolgens worden alleen Merk A-producten geretourneerd en op die pagina weergegeven. Op dezelfde manier worden op de pagina Brand Landing voor merk B alleen merkproducten teruggegeven. Met dit type van dynamische integratieregel, moet de gebruiker slechts één aanbeveling specificeren die relevante merkresultaten over alle merkpagina&#39;s eerder dan het specificeren van een inzameling of een statische filter om elke merknaam te passen terugkeert.

Let erop dat u de `entity.brand` in de mbox op die landingspagina&#39;s om dit te werken.

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

Wanneer u een pagina bezoekt die een merk A-product bevat, stelt de pagina de waarde van de `entity.brand` parameter &quot;BrandA&quot;.

![Voorbeeld van doelaanroep](/help/main/c-recommendations/c-algorithms/assets/example-target-call.png)

In de aanbevelingen op de pagina ziet u alleen Merk A-producten.

![Merk A aanbevelingen](/help/main/c-recommendations/c-algorithms/assets/brandA.png)

Als u dan een merkpagina B bekijkt, `entity.brand` De waarde wordt opnieuw ingesteld op &quot;BrandB&quot; en op de productpagina&#39;s van Brand B worden aanbevolen Brand B-producten weergegeven.

![Aanbevolen merk B](/help/main/c-recommendations/c-algorithms/assets/brandB.png)

### Upsellen naar een duurder product

Stel dat u een kledinghandelaar bent en gebruikers wilt aanmoedigen om duurdere en daarom rendabelere voorwerpen te overwegen. U kunt de operatoren ‘gelijk aan’ en ‘gelijk aan’ gebruiken om duurdere objecten van dezelfde categorie en hetzelfde merk te promoten. Een schoenenhandelaar kan bijvoorbeeld duurdere loopschoenen promoten in een poging om een bezoeker die op zoek is naar loopschoenen te upverkopen, zoals in het volgende voorbeeld:

![Uploaden](/help/main/c-recommendations/c-algorithms/assets/upsell.png)

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

U kunt dynamische en statische filters mengen om privé-etiketproducten te bevorderen. Zo kan een kantoorbedrijf bijvoorbeeld tonercartridges van het huismerk van het bedrijf promoten om een rendabelere verkoop aan te sturen voor een bezoeker die naar toner kijkt — en pennen van het huismerk van het bedrijf promoten om een winstgevender verkoop te stimuleren voor een bezoeker die naar pennen kijkt, zoals in het volgende voorbeeld:

![House Brand](/help/main/c-recommendations/c-algorithms/assets/housebrand.png)

```
Entity Attribute Matching
category - equals - current item's - category 
And
Static Filter
IsHouseBrand - equals - true
```
