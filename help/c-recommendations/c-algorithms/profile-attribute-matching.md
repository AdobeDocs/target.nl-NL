---
keywords: inclusieregels;inclusiecriteria;aanbevelingen;bevordering;bevorderingen;dynamische filtratie;dynamic;profile kenmerkovereenkomsten
description: Filter dynamisch in Adobe Target Recommendations door items (entiteiten) te vergelijken met een waarde in het gebruikersprofiel.
title: Filteren op aanpassing van profielkenmerken in dynamische insluitingsregels in doelaanbevelingen v
feature: Recommendations
translation-type: tm+mt
source-git-commit: 48b94f967252f5ddb009597456edf0a43bc54ba6
workflow-type: tm+mt
source-wordcount: '473'
ht-degree: 0%

---


# ![Identieke ](/help/assets/premium.png) PREMIUMP-profielkenmerken

Filter dynamisch in [!DNL Adobe Target] [!DNL Recommendations] door items (entiteiten) te vergelijken met een waarde in het profiel van de gebruiker.

Gebruik [!UICONTROL Profile Attribute Matching] wanneer u aanbevelingen wilt tonen die een waarde aanpassen die in het profiel van de bezoeker, zoals grootte of favoriet merk wordt opgeslagen.

>[!NOTE]
>
>Het [proces voor het creëren van en het gebruiken van inclusieregels](/help/c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md) voor criteria en bevorderingen is gelijkaardig, zoals de gebruiksgevallen en de voorbeelden zijn.

De volgende scenario&#39;s tonen hoe u [!UICONTROL Profile Attribute Matching] kunt gebruiken:

* Een bedrijf dat eyeglasses verkoopt, slaat de favoriete kleur van een bezoeker op als &quot;walnoot&quot;. Voor die specifieke bezoeker wordt aanbevolen alleen eyeglass-frames met een &quot;walnoot&quot; in kleur te retourneren.
* Een profielparameter kan voor de kledinggrootte (b.v., Klein, Middel, of Groot) van een bezoeker worden bepaald aangezien zij op de website van uw bedrijf navigeren. Er kan een aanbeveling worden ingesteld die overeenkomt met die profielparameter en die alleen producten retourneert die specifiek zijn voor de door de gebruiker voorkeurskledinggrootte.

## Voorbeelden van overeenkomsten van profielkenmerken {#section_9873E2F22E094E479569D05AD5BB1D40}

[!UICONTROL Profile Attribute Matching] Hiermee kunt u alleen de items aanbevelen die overeenkomen met een kenmerk uit het profiel van de bezoeker, zoals in de onderstaande voorbeelden.

### Aanbevolen objecten van het favoriete merk van de gebruiker

U kunt bijvoorbeeld de optie [!UICONTROL Profile Attribute Matching] gebruiken om een regel te maken die alleen items aanbeveelt wanneer het merk gelijk is aan de waarde of tekst die is opgeslagen in `profile.favoritebrand`. Met een dergelijke regel geldt dat als een bezoeker korte berichten van een bepaald merk bekijkt, alleen aanbevelingen worden weergegeven die overeenkomen met het favoriete merk van die gebruiker (de waarde die is opgeslagen in `profile.favoritebrand` in het profiel van de bezoeker).

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

Wanneer een bezoeker op verschillende afbeeldingen van ventilatoren op deze website klikt, stelt elke pagina de waarde van de parameter `entity.size` in op basis van het feit of de grootte van de ventilator in de afbeelding klein of groot is.

Stel dat u een profielscript hebt gemaakt om het aantal keren bij te houden en te tellen dat de waarde van `entity.size` is ingesteld op klein of groot.

Als de bezoeker vervolgens terugkeert naar de startpagina, ziet hij of zij gefilterde aanbevelingen op basis van de vraag of er op meer kleine of grote ventilatoren is geklikt.

Recommendations is gebaseerd op het bekijken van meer kleine ventilatoren op de website:

![aanbevelingen voor kleine ventilatoren](/help/c-recommendations/c-algorithms/assets/small-fans.png)

Recommendations is gebaseerd op het weergeven van grotere ventilatoren op de website:

![aanbevelingen voor grote ventilatoren](/help/c-recommendations/c-algorithms/assets/large-fans.png)