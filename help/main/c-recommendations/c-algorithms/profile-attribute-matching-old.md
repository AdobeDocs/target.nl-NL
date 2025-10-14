---
keywords: inclusieregels;inclusiecriteria;aanbevelingen;bevordering;bevorderingen;dynamische filtratie;dynamic;profile kenmerkovereenkomsten
description: Leer hoe te om dynamisch in Adobe  [!DNL Target]  Aanbevelingen te filtreren door punten (entiteiten) tegen een waarde in het profiel van de gebruiker te vergelijken.
title: Hoe filtreer ik door het attribuut van het Profiel dat in de activiteiten van Aanbevelingen past?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=nl-NL#premium newtab=true" tooltip="Kijk wat er in Target Premium is opgenomen."
feature: Recommendations
exl-id: d4b837af-771b-41b4-982b-f9f08e4753f2
source-git-commit: 02ffe8da6cdf96039218656b9690fa719a77910c
workflow-type: tm+mt
source-wordcount: '483'
ht-degree: 0%

---

# Correctie van profielkenmerk

Filter dynamisch in [!DNL Adobe Target] [!DNL Recommendations] door items (entiteiten) te vergelijken met een waarde in het gebruikersprofiel.

Gebruik [!UICONTROL Profile Attribute Matching] als u aanbevelingen wilt weergeven die overeenkomen met een waarde die is opgeslagen in het profiel van de bezoeker, zoals de grootte of het favoriete merk.

>[!NOTE]
>
>Het [&#x200B; proces om inclusieregels &#x200B;](/help/main/c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md) voor criteria en bevorderingen tot stand te brengen en te gebruiken is gelijkaardig, zoals de gebruiksgevallen en de voorbeelden zijn.

De volgende scenario&#39;s laten zien hoe u [!UICONTROL Profile Attribute Matching] kunt gebruiken:

* Een bedrijf dat eyeglasses verkoopt, slaat de favoriete framegleur van een bezoeker op als &quot;walnoot&quot;. Voor die specifieke bezoeker wordt aanbevolen alleen eyeglass-frames met een &quot;walnoot&quot; in kleur te retourneren.
* Een profielparameter kan voor de kledinggrootte (b.v., Klein, Medium, of Groot) van een bezoeker worden bepaald aangezien zij op de website van uw bedrijf navigeren. Er kan een aanbeveling worden ingesteld die overeenkomt met die profielparameter en die alleen producten retourneert die specifiek zijn voor de door de gebruiker gewenste kledinggrootte.

## Voorbeelden van overeenkomsten van profielkenmerken {#section_9873E2F22E094E479569D05AD5BB1D40}

In [!UICONTROL Profile Attribute Matching] kunt u alleen de items aanbevelen die overeenkomen met een kenmerk van het profiel van de bezoeker, zoals in de onderstaande voorbeelden.

### Aanbevolen objecten van het favoriete merk van de gebruiker

Met de optie [!UICONTROL Profile Attribute Matching] kunt u bijvoorbeeld een regel maken die alleen items aanbeveelt als het merk gelijk is aan de waarde of tekst die in `profile.favoritebrand` is opgeslagen. Met een dergelijke regel geldt dat als een bezoeker korte berichten van een bepaald merk bekijkt, alleen aanbevelingen worden weergegeven die overeenkomen met het favoriete merk van die gebruiker (de waarde die is opgeslagen in `profile.favoritebrand` in het profiel van de bezoeker).

![&#x200B; Favoriete merk &#x200B;](/help/main/c-recommendations/c-algorithms/assets/favorite-brand.png)

```
Profile Attribute Matching
brand - equals - the value/text stored in - profile.favoritebrand
```

### Arbeidstaken afstemmen op werkzoekenden

Stel dat je probeert banen te koppelen aan werkzoekenden. U wilt alleen taken aanbevelen die zich in dezelfde stad bevinden als de werkzoekende.

U kunt inclusieregels gebruiken om de plaats van een baanzoeker van het profiel van zijn of haar bezoeker aan een baanlijst aan te passen, zoals in het volgende voorbeeld:

![&#x200B; Plaats van de Gebruiker &#x200B;](/help/main/c-recommendations/c-algorithms/assets/city.png)

```
Profile Attribute Matching
jobCity - equals - the value/text stored in - profile.usersCity
```

### Aanbevolen objecten op basis van grootte

Bekijk een website die elektrische ventilatoren verkoopt voor een visueel voorbeeld van de invloed van profielkenmerkafstemming op aanbevelingen.

Wanneer een bezoeker op verschillende afbeeldingen van ventilatoren op deze website klikt, stelt elke pagina de waarde van de parameter `entity.size` in op basis van het feit of de grootte van de ventilator in de afbeelding klein of groot is.

Stel dat u een profielscript hebt gemaakt waarmee u kunt bijhouden en tellen hoe vaak de waarde van `entity.size` is ingesteld op klein of groot.

Als de bezoeker vervolgens terugkeert naar de startpagina, ziet hij of zij gefilterde aanbevelingen op basis van de vraag of er op meer kleine of grote ventilatoren is geklikt.

Aanbevelingen op basis van het bekijken van meer kleine ventilatoren op de website:

![&#x200B; kleine ventilatoraanbevelingen &#x200B;](/help/main/c-recommendations/c-algorithms/assets/small-fans.png)

Aanbevelingen op basis van het weergeven van grotere ventilatoren op de website:

![&#x200B; grote ventilatoraanbevelingen &#x200B;](/help/main/c-recommendations/c-algorithms/assets/large-fans.png)
