---
keywords: AB;A/B;AB...n;vergelijk ervaringen;gericht;vergelijk inhoud;auto-doel;auto-wijs toe
description: Verken de A/B-testactiviteiten in  [!DNL Target]  - [!UICONTROL Manual] , [!UICONTROL Auto-Allocate] en [!UICONTROL Auto-Target] .
title: Ontdek de A/B de Activiteiten van de Test beschikbaar in  [!DNL Target].
feature: A/B Tests
exl-id: e8ff8994-a0a9-4fc7-8fcb-e3a1b7697604
source-git-commit: 974746e25724abf0e5edd3884331ec0975e5352e
workflow-type: tm+mt
source-wordcount: '670'
ht-degree: 0%

---

# A/B-testoverzicht

Een handmatige [!UICONTROL A/B Test] activiteit (die soms als test A/B...N wordt bedoeld) vergelijkt twee of meer versies van uw inhoud van de Website om te zien welke versie het beste uw omzettingen, verkoop, of andere metriek optilt u identificeert. Gebruik een A/B test om veranderingen in uw pagina met uw standaardpaginaontwerp te vergelijken om te bepalen welke ervaring de beste resultaten veroorzaakt.

>[!TIP]
>
>Naast de [!UICONTROL Manual] (Standaard) [!UICONTROL A/B Test] -activiteit (die in dit artikel wordt besproken), biedt [!DNL Target] twee extra typen [!UICONTROL A/B Test] -activiteiten: [!UICONTROL Auto-Allocate] en [!UICONTROL Auto-Target] . Zie [&#x200B; Types van het Testen A/B activiteiten &#x200B;](#types) hieronder voor meer informatie.

Handmatige A/B-tests zijn handig wanneer u een duidelijke hypothese hebt over manieren om de prestaties van uw pagina te verbeteren op basis van succeswaarden of alternatieve levering van inhoud.

Handmatige A/B-tests zijn zeer geschikt voor grote wijzigingen die nieuwe schermindelingen of drastisch verschillende behandelingen van de elementen kunnen inhouden. Als uw testontwerp niet gemakkelijk in individuele paginaelementen breekt, zou u een test A/B moeten in werking stellen alvorens a [&#x200B; multivariate test &#x200B;](/help/main/c-activities/c-multivariate-testing/multivariate-testing.md) in werking te stellen.

Wanneer u opstelling uw test A/B, kunt u het percentage bezoekers bepalen die elke ervaring zien. Bijvoorbeeld, zou u verkeer tussen de controle en een tweede ervaring gelijkmatig kunnen verdelen, of u zou een nieuwe, riskantere ervaring kunnen testen door het aan slechts 5% van uw publiek te tonen.

>[!NOTE]
>
>Voor gedetailleerde informatie over het bepalen van de optimale steekproefgrootte voor een test A/B, zie [&#x200B; Plan Uw Test A/B &#x200B;](/help/main/c-activities/t-test-ab/sample-size-determination.md).

Wanneer het aantal verschillende ervaringen vijf overschrijdt en twee of meer plaatsen overspant, is het een goed idee om een [&#x200B; test MVT &#x200B;](/help/main/c-activities/c-multivariate-testing/multivariate-testing.md) te overwegen alvorens uw tests A/B in werking te stellen. De multivariate test toont welke gebieden op de pagina het meest waarschijnlijk om omzetting zullen verbeteren. Dit zijn de locaties waarop een markeerteken zich moet concentreren. De MVT-test kan bijvoorbeeld laten zien dat de call to action de belangrijkste locatie is voor het bereiken van uw doelen. Nadat u hebt bepaald welke locaties en inhoud het nuttigst zijn om u te helpen uw doelstellingen te bereiken, kunt u een test A/B uitvoeren om de resultaten verder te verfijnen. Bijvoorbeeld, om twee specifieke beelden tegen elkaar te testen, of de formulering of de kleuren van een call to action te vergelijken. Door een MVT-test met een of meer A/B-tests uit te voeren, kunt u de best mogelijke inhoud voor de gewenste resultaten bepalen.

## Typen A/B-testactiviteiten {#types}

Naast de handmatige [!UICONTROL A/B Test] activiteit, biedt [!DNL Target] twee extra typen [!UICONTROL A/B Testing] activiteiten: [!UICONTROL Auto-Allocate] en [!UICONTROL Auto-Target] .

| Type activiteit | Beschrijving |
| --- | --- |
| [!UICONTROL Manual A/B Test] | Vergelijkt twee of meer ervaringen om te zien welke ervaring het best omzettingen gedurende een vooraf bepaalde testperiode verbetert.<P>In deze sectie wordt beschreven hoe u een handmatige [!UICONTROL A/B Test] activiteit instelt, maar de stappen voor de andere typen [!UICONTROL A/B Test] -activiteiten zijn vergelijkbaar. |
| [!UICONTROL Auto-Allocate] | Identificeert een winnaar onder twee of meer ervaringen, en richt dan verkeer aan de winnaar opnieuw, die omzetting verhoogt aangezien de test loopt en leert.<P>Om over de voordelen te leren om een [!UICONTROL Auto-Allocate] activiteit te gebruiken, zie [&#x200B; auto-toewijs &#x200B;](/help/main/c-activities/t-test-ab/sample-size-determination.md#auto-allocate) in *hoe lang u een Test A/B* in werking zou moeten stellen en [&#x200B; auto-toewijs overzicht &#x200B;](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md) toe. |
| ![&#x200B; het badge van de Premium &#x200B;](/help/main/assets/premium.png) [!UICONTROL Auto-Target] | Gebruikt geavanceerd computerleren om inhoud en aandrijvingsomzettingen aan te passen door veelvoudige hoog-presterende, markeer-bepaalde ervaringen te identificeren. De meest toegesneden ervaring wordt vervolgens aan bezoekers aangeboden op basis van hun individuele klantprofielen en gedrag van vergelijkbare bezoekers in het verleden.<P>Voor meer informatie, zie [&#x200B; auto-Doel &#x200B;](/help/main/c-activities/auto-target/auto-target-to-optimize.md). |

Voor meer informatie over welke van deze [!UICONTROL A/B Test] activiteiten juist voor u is, zie de interactieve [&#x200B; Gids PDF van de Activiteiten van Adobe Target &#x200B;](/help/main/c-activities/target-activities-guide.md).

De stappen voor het maken van de drie typen [!UICONTROL A/B Test] -activiteiten zijn vergelijkbaar. Een [!UICONTROL Auto-Allocate] - of [!UICONTROL Auto-Target] -activiteit maken:

1. Begin door [&#x200B; creërend een activiteit van de Test A/B &#x200B;](/help/main/c-activities/t-test-ab/t-test-create-ab/test-create-ab.md).
1. Wanneer u aan de [!UICONTROL Targeting] pagina krijgt, klik de [!UICONTROL Traffic Allocation] controle, dan kies de gewenste methode van de verkeerstoewijzing in de juiste ruit, zoals hieronder getoond:

   * [!UICONTROL Auto-Allocate to best experience]
   * [!UICONTROL Auto-Target for personalized experience]

   ![&#x200B; montages van de Methode van de Toewijzing van het Verkeer &#x200B;](/help/main/c-activities/t-test-ab/t-test-create-ab/assets/traffic-allocation-method-new.png)

## Aanbevelingen opnemen in A/B-activiteiten

U kunt aanbevelingen opnemen in [!UICONTROL A/B Test] -, [!UICONTROL Auto-Allocate] - en [!UICONTROL Auto-Target] -activiteiten (en [!UICONTROL Experience Targeting] -activiteiten (XT)). Voor meer informatie, zie [&#x200B; Aanbevelingen als aanbieding &#x200B;](/help/main/c-recommendations/recommendations-as-an-offer.md).

Deze functionaliteit vereist dat u de vergunning van a [&#x200B; Target Premium &#x200B;](/help/main/c-intro/intro.md#premium) hebt.
