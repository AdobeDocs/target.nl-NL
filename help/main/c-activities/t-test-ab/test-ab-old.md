---
keywords: AB;A/B;AB...n;vergelijk ervaringen;gericht;vergelijk inhoud;auto-doel;auto-wijs toe
description: Leer over de verschillende soorten de activiteiten van de Test van A/B in Adobe  [!DNL Target]  - Handboek, auto-Toewijzing, en auto-Doel. Kies de juiste voor je.
title: Welk type A/B-activiteiten is als doel beschikbaar?
feature: A/B Tests
exl-id: e8ff8994-a0a9-4fc7-8fcb-e3a1b7697604
source-git-commit: 974746e25724abf0e5edd3884331ec0975e5352e
workflow-type: tm+mt
source-wordcount: '755'
ht-degree: 0%

---

# A/B-testoverzicht

Met een handmatige [!UICONTROL A/B Test] activiteit worden twee of meer versies van uw website-inhoud vergeleken om te zien welke versie uw conversies het beste verbetert tijdens een vooraf opgegeven testperiode.

>[!NOTE]
>
>Naast de activiteit Handmatig (standaard) [!UICONTROL A/B Test] (die in deze sectie wordt besproken), biedt [!DNL Target] twee extra typen [!UICONTROL A/B Test] -activiteiten: [!UICONTROL Auto-Allocate] en [!UICONTROL Auto-Target] . Zie [&#x200B; Types van het Testen A/B activiteiten &#x200B;](#types) hieronder voor meer informatie.

Een handmatige [!UICONTROL A/B Test] activiteit (die soms als test A/B...N wordt bedoeld) vergelijkt twee of meer versies van uw inhoud van de Website om te zien welke versie het beste uw omzettingen, verkoop, of andere metriek optilt u identificeert. Gebruik een A/B test om veranderingen in uw pagina met uw standaardpaginaontwerp te vergelijken om te bepalen welke ervaring de beste resultaten veroorzaakt.

Handmatige A/B-tests zijn handig wanneer u een duidelijke hypothese hebt over manieren om de prestaties van uw pagina te verbeteren op basis van succeswaarden of alternatieve levering van inhoud.

Handmatige A/B-tests zijn zeer geschikt voor grote wijzigingen die nieuwe schermindelingen of drastisch verschillende behandelingen van de elementen kunnen inhouden. Als uw testontwerp niet gemakkelijk in individuele paginaelementen breekt, zou u een test A/B vóór a [&#x200B; moeten in werking stellen multivariate test &#x200B;](/help/main/c-activities/c-multivariate-testing/multivariate-testing.md).

Wanneer u opstelling uw test A/B, kunt u het percentage bezoekers bepalen die elke ervaring zien. Bijvoorbeeld, zou u verkeer tussen de controle en een tweede ervaring gelijkmatig kunnen verdelen, of u zou een nieuwe, riskantere ervaring kunnen uittesten door het aan slechts 5% van uw publiek te tonen.

>[!NOTE]
>
>Voor gedetailleerde informatie over het bepalen van de optimale steekproefgrootte voor een test A/B, zie [&#x200B; Plan Uw Test A/B &#x200B;](/help/main/c-activities/t-test-ab/sample-size-determination.md).

Wanneer het aantal verschillende ervaringen vijf overschrijdt en twee of meer plaatsen overspant, is het een goed idee om een [&#x200B; test MVT &#x200B;](/help/main/c-activities/c-multivariate-testing/multivariate-testing.md) te overwegen alvorens uw tests A/B in werking te stellen. De multivariate test toont welke gebieden op de pagina het meest waarschijnlijk om omzetting zullen verbeteren. Dit zijn de locaties waarop een markeerteken zich moet concentreren. De MVT-test kan bijvoorbeeld laten zien dat de call to action de belangrijkste locatie is voor het bereiken van uw doelen. Nadat u hebt bepaald welke locaties en inhoud het nuttigst zijn om u te helpen uw doelstellingen te bereiken, kunt u een test A/B uitvoeren om de resultaten verder te verfijnen. Bijvoorbeeld, om twee specifieke beelden tegen elkaar te testen, of de formulering of de kleuren van een call to action te vergelijken. Door een MVT-test met een of meer A/B-tests uit te voeren, kunt u de best mogelijke inhoud voor de gewenste resultaten bepalen.

## Typen A/B-testactiviteiten {#types}

Naast de handmatige [!UICONTROL A/B Test] -activiteit (die in deze sectie wordt besproken), biedt [!DNL Target] twee extra typen testactiviteiten voor A/B: [!UICONTROL Auto-Allocate] en [!UICONTROL Auto-Target] .

| Type activiteit | Beschrijving |
| --- | --- |
| [!UICONTROL Manual A/B Test] | Vergelijkt twee of meer ervaringen om te zien welke beste ervaring conversies gedurende een vooraf bepaalde testperiode verbetert.<P>In deze sectie wordt beschreven hoe u een handmatige [!UICONTROL A/B Test] activiteit instelt, maar de stappen voor de andere typen [!UICONTROL A/B Test] -activiteiten zijn vergelijkbaar. |
| [!UICONTROL Auto-Allocate] | Identificeert een winnaar onder twee of meer ervaringen, en richt dan verkeer aan de winnaar opnieuw, die omzetting verhoogt aangezien de test loopt en leert.<P>Om over de voordelen te leren om een [!UICONTROL Auto-Allocate] activiteit te gebruiken, zie [&#x200B; auto-toewijs &#x200B;](/help/main/c-activities/t-test-ab/sample-size-determination.md#auto-allocate) in *hoe lang u een Test A/B* in werking zou moeten stellen en [&#x200B; auto-toewijs overzicht &#x200B;](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md) toe. |
| ![&#x200B; het badge van de Premium &#x200B;](/help/main/assets/premium.png) [!UICONTROL Auto-Target] | Gebruikt geavanceerd computerleren om inhoud en aandrijvingsomzettingen aan te passen door veelvoudige hoog-presterende, markeer-bepaalde ervaringen te identificeren. De meest toegesneden ervaring wordt vervolgens aan bezoekers aangeboden op basis van hun individuele klantprofielen en gedrag van vergelijkbare bezoekers in het verleden.<P>Voor meer informatie, zie [&#x200B; auto-Doel &#x200B;](/help/main/c-activities/auto-target/auto-target-to-optimize.md). |

Voor meer informatie over welke van deze [!UICONTROL A/B Test] activiteiten juist voor u is, zie de interactieve [&#x200B; Gids PDF van de Activiteiten van Adobe Target &#x200B;](/help/main/c-activities/target-activities-guide.md).

De stappen voor het maken van de drie typen [!UICONTROL A/B Test] -activiteiten zijn vergelijkbaar. Om een [!UICONTROL Auto-Allocate] of [!UICONTROL Auto-Target] activiteit tot stand te brengen, begin door [&#x200B; een activiteit van de Test A/B &#x200B;](/help/main/c-activities/t-test-ab/t-test-create-ab/test-create-ab.md) te creëren, maar wanneer u aan de [!UICONTROL Targeting] pagina krijgt, kies de gewenste methode van de verkeerstoewijzing, zoals hieronder getoond:

* [!UICONTROL Auto-allocate to best experience]
* [!UICONTROL Auto-target for personalized experience]

![&#x200B; montages van de Methode van de Toewijzing van het Verkeer &#x200B;](/help/main/c-activities/t-test-ab/t-test-create-ab/assets/traffic-allocation-method.png)

## Aanbevelingen opnemen in A/B-activiteiten

U kunt aanbevelingen opnemen in [!UICONTROL A/B Test] -, [!UICONTROL Auto-Allocate] - en [!UICONTROL Auto-Target] -activiteiten (en [!UICONTROL Experience Targeting] -activiteiten (XT)). Voor meer informatie, zie [&#x200B; Aanbevelingen als aanbieding &#x200B;](/help/main/c-recommendations/recommendations-as-an-offer.md).

Deze functionaliteit vereist dat u a [&#x200B; vergunning van Target Premium &#x200B;](/help/main/c-intro/intro.md#premium) hebt

## De video van de opleiding: De Types van Activiteit (9 :03) ![&#x200B; badge van het Overzicht &#x200B;](/help/main/assets/overview.png)

In deze video worden de activiteitstypen uitgelegd die beschikbaar zijn in [!DNL Target Standard/Premium] .

* Beschrijf de typen activiteiten die zijn opgenomen in [!DNL Adobe Target]
* Selecteer het juiste type activiteit om uw doelen te bereiken
* Beschrijf de driestappenworkflow met instructies die van toepassing is op alle typen activiteiten

>[!VIDEO](https://video.tv.adobe.com/v/17386)
