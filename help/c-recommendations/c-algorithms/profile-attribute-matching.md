---
keywords: inclusion rules;inclusion criteria;recommendations;promotion;promotions;dynamic filtering;dynamic;profile attribute matching
description: Filter dynamisch in Adobe Target Recommendations door items (entiteiten) te vergelijken met een waarde in het gebruikersprofiel.
title: Filteren op aanpassing van profielkenmerken in regels voor dynamische integratie in Adobe Target Recommendations
feature: criteria
translation-type: tm+mt
source-git-commit: 60b71c426b61bb16a23976da9a03926f8e73cf6c
workflow-type: tm+mt
source-wordcount: '461'
ht-degree: 0%

---


# ![PREMIUM](/help/assets/premium.png) -profielkenmerkovereenkomst

Filter dynamisch in [!DNL Adobe Target] [!DNL Recommendations] door items (entiteiten) te vergelijken met een waarde in het profiel van de gebruiker.

Gebruik deze optie [!UICONTROL Profile Attribute Matching] als u aanbevelingen wilt weergeven die overeenkomen met een waarde die is opgeslagen in het profiel van de bezoeker, zoals de grootte of het favoriete merk.

>[!NOTE]
>
>Het [proces voor het creëren en gebruiken van inclusieregels](/help/c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md) voor criteria en bevorderingen is gelijkaardig, zoals de gebruiksgevallen en de voorbeelden.

De volgende scenario&#39;s tonen hoe u kunt gebruiken [!UICONTROL Profile Attribute Matching]:

* Een bedrijf dat eyeglasses verkoopt, slaat de favoriete kleur van een bezoeker op als &quot;walnoot&quot;. Voor die specifieke bezoeker wordt aanbevolen alleen eyeglass-frames met een &quot;walnoot&quot; in kleur te retourneren.
* Een profielparameter kan voor de kledinggrootte (b.v., Klein, Middel, of Groot) van een bezoeker worden bepaald aangezien zij op de website van uw bedrijf navigeren. Er kan een aanbeveling worden ingesteld die overeenkomt met die profielparameter en die alleen producten retourneert die specifiek zijn voor de door de gebruiker voorkeurskledinggrootte.

## Voorbeelden van overeenkomsten van profielkenmerken {#section_9873E2F22E094E479569D05AD5BB1D40}

[!UICONTROL Profile Attribute Matching] Hiermee kunt u alleen de items aanbevelen die overeenkomen met een kenmerk uit het profiel van de bezoeker, zoals in de onderstaande voorbeelden.

### Aanbevolen objecten van het favoriete merk van de gebruiker

U kunt bijvoorbeeld de [!UICONTROL Profile Attribute Matching] optie gebruiken om een regel te maken die alleen items aanbeveelt wanneer het merk gelijk is aan de waarde of tekst die is opgeslagen in `profile.favoritebrand`. Met een dergelijke regel geldt dat als een bezoeker korte berichten van een bepaald merk bekijkt, alleen aanbevelingen worden weergegeven die overeenkomen met het favoriete merk van die gebruiker (de waarde die is opgeslagen in het profiel van de bezoeker). `profile.favoritebrand`

![Favoriet merk](/help/c-recommendations/c-algorithms/assets/favorite-brand.png)

```
Profile Attribute Matching
brand - equals - the value/text stored in - profile.favoritebrand
```

### Arbeidstaken afstemmen op werkzoekenden

Stel dat je probeert banen te koppelen aan werkzoekenden. U wilt alleen taken aanbevelen die zich in dezelfde stad bevinden als de werkzoekende.

U kunt inclusieregels gebruiken om de plaats van een baanzoeker van het profiel van zijn of haar bezoeker aan een baanlijst aan te passen, zoals in het volgende voorbeeld:

![Plaats van gebruiker](/help/c-recommendations/c-algorithms/assets/city.png)

```
Profile Attribute Matching
jobCity - equals - the value/text stored in - profile.usersCity
```

### Aanbevolen objecten op basis van grootte

Bekijk een website die elektrische ventilatoren verkoopt voor een visueel voorbeeld van de invloed van profielkenmerkafstemming op aanbevelingen.

Wanneer een bezoeker op verschillende afbeeldingen van ventilatoren op deze website klikt, stelt elke pagina de waarde van de `entity.size` parameter in op basis van het feit of de grootte van de ventilator in de afbeelding klein of groot is.

Stel dat u een profielscript hebt gemaakt om het aantal keren bij te houden en te tellen dat de waarde van `entity.size` is ingesteld op klein of groot.

Als de bezoeker vervolgens terugkeert naar de startpagina, ziet hij of zij gefilterde aanbevelingen op basis van de vraag of er op meer kleine of grote ventilatoren is geklikt.

Recommendations is gebaseerd op het bekijken van meer kleine ventilatoren op de website:

![aanbevelingen voor kleine ventilatoren](/help/c-recommendations/c-algorithms/assets/small-fans.png)

Recommendations is gebaseerd op het weergeven van grotere ventilatoren op de website:

![aanbevelingen voor grote ventilatoren](/help/c-recommendations/c-algorithms/assets/large-fans.png)