---
keywords: inclusieregels;inclusiecriteria;aanbevelingen;bevordering;bevordering;dynamische filtering;dynamic;entiteitattributen die aanpassen
description: Leer hoe te om dynamisch in de Aanbevelingen van Adobe  [!DNL Target]  te filtreren door een pool van potentiële punten aan een specifiek punt te vergelijken dat de gebruiker met in wisselwerking heeft gestaan.
title: Hoe filtert ik op kenmerk Entiteit dat overeenkomt met activiteiten in Aanbevelingen?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=nl-NL#premium newtab=true" tooltip="Kijk wat er in Target Premium is opgenomen."
feature: Recommendations
exl-id: aadd3132-d590-4dc9-b01b-bedf41bc7441
source-git-commit: 02ffe8da6cdf96039218656b9690fa719a77910c
workflow-type: tm+mt
source-wordcount: '529'
ht-degree: 0%

---

# Identieke entiteitskenmerk

Filter dynamisch in [!DNL Adobe Target] [!DNL Recommendations] door een groep potentiële aanbevelingen-items te vergelijken met een specifiek item waarmee de gebruiker heeft gewerkt.

>[!NOTE]
>
>Het [&#x200B; proces om inclusieregels &#x200B;](/help/main/c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md) voor criteria en bevorderingen tot stand te brengen en te gebruiken is gelijkaardig, zoals de gebruiksgevallen en de voorbeelden zijn.

U kunt bijvoorbeeld alleen items aanbevelen die overeenkomen met het merk van het huidige item, zoals in het volgende voorbeeld:

Als de mbox op een Brand Landing Page `entity.brand=brandA` retourneert, worden alleen Merk A-producten geretourneerd en op die pagina weergegeven. Op dezelfde manier worden op de pagina Brand Landing voor merk B alleen merkproducten teruggegeven. Met dit type van dynamische integratieregel, moet de gebruiker slechts één aanbeveling specificeren die relevante merkresultaten over alle merkpagina&#39;s eerder dan het specificeren van een inzameling of een statische filter om elke merknaam te passen terugkeert.

Dit werkt alleen als u de instructie `entity.brand` in de mbox op de bestemmingspagina&#39;s hebt geplaatst.

## Voorbeelden van overeenkomsten van entiteitskenmerken

In [!UICONTROL Entity Attribute Matching] kunt u alleen de overeenkomende items aanbevelen, bijvoorbeeld:

* Een kenmerk van het item dat de gebruiker momenteel weergeeft
* Het item dat de gebruiker het laatst heeft bekeken
* Het item dat de gebruiker het laatst heeft aangeschaft
* Het item dat de gebruiker het vaakst heeft bekeken
* Een item dat is opgeslagen in een aangepast kenmerk in het profiel van de bezoeker

### Aanbevolen objecten op basis van een merk

Nadat de regels voor de entiteitskenmerken zijn samengesteld, worden alle aanbevelingen met kenmerken uitgefilterd die niet overeenkomen met de entiteitswaarde die op de pagina wordt doorgegeven.

In het volgende voorbeeld worden aanbevelingen getoond die overeenkomen met het productmerk dat op de pagina wordt weergegeven:

Wanneer u een pagina bezoekt die een merk A-product bevat, stelt de pagina de waarde van de parameter `entity.brand` in op &quot;MerkA&quot;.

![&#x200B; de vraag van het Doel van het Voorbeeld &#x200B;](/help/main/c-recommendations/c-algorithms/assets/example-target-call.png)

In de aanbevelingen op de pagina ziet u alleen Merk A-producten.

![&#x200B; merkA aanbevelingen &#x200B;](/help/main/c-recommendations/c-algorithms/assets/brandA.png)

Als u vervolgens een productpagina van merk B weergeeft, wordt de waarde van `entity.brand` opnieuw ingesteld op &quot;MerkB&quot; en worden de producten van merk B aanbevolen op de productpagina&#39;s van merk B.

![&#x200B; aanbevelingen van 0&rbrace; Merk B](/help/main/c-recommendations/c-algorithms/assets/brandB.png)

### Upsellen naar een duurder product

Stel dat je een apparel retailer bent en gebruikers wil aanmoedigen om duurdere en dus winstgevender objecten te overwegen. U kunt de operatoren ‘gelijk aan’ en ‘gelijk aan’ gebruiken om duurdere objecten van dezelfde categorie en hetzelfde merk te promoten. Een schoenen retailer kan bijvoorbeeld duurdere loopschoenen promoten in een poging om een bezoeker die op zoek is naar loopschoenen te uploaden, zoals in het volgende voorbeeld:

![&#x200B; Upselling &#x200B;](/help/main/c-recommendations/c-algorithms/assets/upsell.png)

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

![&#x200B; Merk van het Huis &#x200B;](/help/main/c-recommendations/c-algorithms/assets/housebrand.png)

```
Entity Attribute Matching
category - equals - current item's - category 
And
Static Filter
IsHouseBrand - equals - true
```
