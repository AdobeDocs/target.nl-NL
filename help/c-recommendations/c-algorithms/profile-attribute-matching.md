---
keywords: inclusion rules;inclusion criteria;recommendations;promotion;promotions;dynamic filtering;dynamic;profile attribute matching
description: Filter dynamisch in Adobe Target Recommendations door items (entiteiten) te vergelijken met een waarde in het gebruikersprofiel.
title: Filteren op aanpassing van profielkenmerken in regels voor dynamische integratie in Adobe Target Recommendations
feature: criteria
translation-type: tm+mt
source-git-commit: b51c980d8e7db3ee574350a04f9056fe5b00a703
workflow-type: tm+mt
source-wordcount: '613'
ht-degree: 0%

---


# ![PREMIUM](/help/assets/premium.png) -profielkenmerkovereenkomst

Filter dynamisch in [!DNL Adobe Target] [!DNL Recommendations] door items (entiteiten) te vergelijken met een waarde in het profiel van de gebruiker.

Gebruik deze optie [!UICONTROL Profile Attribute Matching] als u aanbevelingen wilt weergeven die overeenkomen met een waarde die is opgeslagen in het profiel van de bezoeker, zoals de grootte of het favoriete merk.

De volgende scenario&#39;s tonen hoe u kunt gebruiken [!UICONTROL Profile Attribute Matching]:

* Een bedrijf dat eyeglasses verkoopt, slaat de favoriete kleur van een bezoeker op als &quot;walnoot&quot;. Voor die specifieke bezoeker wordt aanbevolen alleen eyeglass-frames met een &quot;walnoot&quot; in kleur te retourneren.
* Een profielparameter kan voor de kledinggrootte (b.v., Klein, Middel, of Groot) van een bezoeker worden bepaald aangezien zij op de website van uw bedrijf navigeren. Er kan een aanbeveling worden ingesteld die overeenkomt met die profielparameter en die alleen producten retourneert die specifiek zijn voor de door de gebruiker voorkeurskledinggrootte.

## Voorbeelden van overeenkomsten van profielkenmerken {#section_9873E2F22E094E479569D05AD5BB1D40}

[!UICONTROL Profile Attribute Matching] Hiermee kunt u alleen de items aanbevelen die overeenkomen met een kenmerk uit het profiel van de bezoeker, zoals in de onderstaande voorbeelden.

### Aanbevolen objecten van het favoriete merk van de gebruiker

U kunt bijvoorbeeld de [!UICONTROL Profile Attribute Matching] optie gebruiken om een regel te maken die alleen items aanbeveelt wanneer het merk gelijk is aan de waarde of tekst die is opgeslagen in `profile.favoritebrand`. Met een dergelijke regel geldt dat als een bezoeker korte berichten van een bepaald merk bekijkt, alleen aanbevelingen worden weergegeven die overeenkomen met het favoriete merk van die gebruiker (de waarde die is opgeslagen in het profiel van de bezoeker). `profile.favoritebrand`

```
Profile Attribute Matching
brand - equals - the value/text stored in - profile.favoritebrand
```

### Arbeidstaken afstemmen op werkzoekenden

Stel dat je probeert banen te koppelen aan werkzoekenden. U wilt alleen taken aanbevelen die zich in dezelfde stad bevinden als de werkzoekende.

U kunt inclusieregels gebruiken om de plaats van een baanzoeker van het profiel van zijn of haar bezoeker aan een baanlijst aan te passen, zoals in het volgende voorbeeld:

```
Profile Attribute Matching
jobCity - equals - the value/text stored in - profile.usersCity
```

### Aanbevolen kleren die overeenkomen met de grootte van een bezoeker

Laten we een voorbeeld bekijken om aan te bevelen dat kleding overeenkomt met de kledinggrootte die is ingesteld in het profiel van de bezoeker.

De productpagina verzendt `entity.size` in de mbox vraag (rode pijl in de illustratie hieronder).

U kunt een [profielscript](/help/c-target/c-visitor-profile/profile-parameters.md) maken om de profielkenmerken en waarden van de bezoeker vast te leggen op de laatste pagina die de bezoeker heeft bezocht.

Bijvoorbeeld:

```
if ((mbox.name=="target-global-mbox") &&(mbox.param('entity.size') == 'small')) { return 'small';
}

else if ((mbox.name=="target-global-mbox") &&(mbox.param('entity.size') == 'medium')) { return 'medium';
}

else if ((mbox.name=="target-global-mbox") &&(mbox.param('entity.size') == 'large')) { return 'large';
}
```

Met het profielscript wordt de `entity.size` waarde van de benoemde mbox vastgelegd `target-global-mbox` en geretourneerd als een profielkenmerk met de naam `user.size` (blauwe pijl in de onderstaande afbeelding).

![size mbox vraag](/help/c-recommendations/c-algorithms/assets/size.png)

Klik bij het maken van de aanbevelingen op criteria [!UICONTROL Add Filtering Rule]en selecteer [!UICONTROL Profile Attribute Matching].

![Correctie van profielkenmerken](/help/c-recommendations/c-algorithms/assets/profile-attribute-matching.png)

Als uw `user.size` profiel in [!DNL Target]is geladen, toont het in drop-down voor aanpassing wanneer u opstelling de regel om de waarde te passen die in de mbox vraag (`size`) aan de naam van het profielmanuscript (`user.size`) wordt overgegaan.

U kunt dan &quot;grootte&quot;selecteren &quot;evenaart&quot;de waarde/de tekst die in &quot;user.size&quot;voor uw profielkenmerkaanpassing wordt opgeslagen.

Nadat de regels voor het profielkenmerk zijn samengesteld, worden alle aanbevelingen met kenmerken die niet overeenkomen met het opgeslagen profielkenmerk van de bezoeker uitgefilterd.

### Aanbevolen objecten op basis van grootte

Bekijk een website die ventilatoren verkoopt voor een visueel voorbeeld van de invloed van profielkenmerkafstemming op aanbevelingen.

Wanneer een bezoeker op verschillende afbeeldingen van ventilatoren op deze website klikt, stelt elke pagina de waarde van de `entity.size` parameter in op basis van het feit of de grootte van de ventilator in de afbeelding klein of groot is.

Stel dat u een profielscript hebt gemaakt om het aantal keren bij te houden en te tellen dat de waarde van `entity.size` is ingesteld op klein of groot.

Als de bezoeker vervolgens terugkeert naar de startpagina, ziet hij of zij gefilterde aanbevelingen op basis van de vraag of er op meer kleine of grote ventilatoren is geklikt.

Recommendations is gebaseerd op het bekijken van meer kleine ventilatoren op de website:

![aanbevelingen voor kleine ventilatoren](/help/c-recommendations/c-algorithms/assets/small-fans.png)

Recommendations is gebaseerd op het weergeven van grotere ventilatoren op de website:

![aanbevelingen voor grote ventilatoren](/help/c-recommendations/c-algorithms/assets/large-fans.png)