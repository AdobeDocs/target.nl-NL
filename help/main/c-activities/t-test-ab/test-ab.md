---
keywords: AB;A/B;AB...n;vergelijk ervaringen;gericht;vergelijk inhoud;auto-doel;auto-wijs toe
description: Meer informatie over de verschillende soorten A/B-testactiviteiten in Adobe [!DNL Target] - Handmatig, automatisch toegewezen en automatisch doel. Kies de juiste voor je.
title: Welk type A/B-activiteiten is als doel beschikbaar?
feature: A/B Tests
exl-id: e8ff8994-a0a9-4fc7-8fcb-e3a1b7697604
source-git-commit: b5da2f5d41739af39d97e0ce9761006794c04d2b
workflow-type: tm+mt
source-wordcount: '753'
ht-degree: 0%

---

# A/B-testoverzicht

Een handleiding [!UICONTROL A/B Test] Deze activiteit vergelijkt twee of meer versies van uw website inhoud om te zien welke versie uw omzettingen tijdens een vooraf bepaalde testperiode het best verbetert.

>[!NOTE]
>
>Naast de handleiding (standaard) [!UICONTROL A/B Test] activiteit (in dit deel besproken), [!DNL Target] verstrekt twee extra types van [!UICONTROL A/B Test] activiteiten: [!UICONTROL Auto-Allocate] en [!UICONTROL Auto-Target]. Zie [Typen A/B-testactiviteiten](#types) hieronder voor meer informatie .

Een handleiding [!UICONTROL A/B Test] De activiteit (die soms als test A/B...N wordt bedoeld) vergelijkt twee of meer versies van uw inhoud van de Website om te zien welke versie beste optilt uw omzettingen, verkoop, of andere metriek u identificeert. Gebruik een A/B test om veranderingen in uw pagina met uw standaardpaginaontwerp te vergelijken om te bepalen welke ervaring de beste resultaten veroorzaakt.

Handmatige A/B-tests zijn handig wanneer u een duidelijke hypothese hebt over manieren om de prestaties van uw pagina te verbeteren op basis van succeswaarden of alternatieve levering van inhoud.

Handmatige A/B-tests zijn zeer geschikt voor grote wijzigingen die nieuwe schermindelingen of drastisch verschillende behandelingen van de elementen kunnen inhouden. Als het testontwerp niet gemakkelijk in afzonderlijke pagina-elementen kan worden opgedeeld, voert u een A/B-test uit vóór een [multivariatietest](/help/main/c-activities/c-multivariate-testing/multivariate-testing.md).

Wanneer u opstelling uw test A/B, kunt u het percentage bezoekers bepalen die elke ervaring zien. Bijvoorbeeld, zou u verkeer tussen de controle en een tweede ervaring gelijkmatig kunnen verdelen, of u zou een nieuwe, riskantere ervaring kunnen uittesten door het aan slechts 5% van uw publiek te tonen.

>[!NOTE]
>
>Voor gedetailleerde informatie over het bepalen van de optimale monstergrootte voor een A/B-test, zie [Uw A/B-test plannen](/help/main/c-activities/t-test-ab/sample-size-determination.md).

Wanneer het aantal verschillende ervaringen groter is dan vijf en twee of meer locaties omvat, is het raadzaam een [MVT-test](/help/main/c-activities/c-multivariate-testing/multivariate-testing.md) voordat u uw A/B-tests uitvoert. De multivariate test toont welke gebieden op de pagina het meest waarschijnlijk om omzetting zullen verbeteren. Dit zijn de locaties waarop een markeerteken zich moet concentreren. Bijvoorbeeld, zou de test MVT kunnen tonen dat de vraag aan actie de belangrijkste plaats voor het ontmoeten van uw doelstellingen is. Nadat u hebt bepaald welke locaties en inhoud het nuttigst zijn om u te helpen uw doelstellingen te bereiken, kunt u een test A/B uitvoeren om de resultaten verder te verfijnen. Bijvoorbeeld, om twee specifieke beelden tegen elkaar te testen, of de formulering of de kleuren van een vraag aan actie te vergelijken. Door een MVT-test met een of meer A/B-tests uit te voeren, kunt u de best mogelijke inhoud voor de gewenste resultaten bepalen.

## Typen A/B-testactiviteiten {#types}

Naast de handleiding [!UICONTROL A/B Test] activiteit (in dit deel besproken), [!DNL Target] bevat twee aanvullende soorten A/B-testactiviteiten: [!UICONTROL Auto-Allocate] en [!UICONTROL Auto-Target].

| Type activiteit | Beschrijving |
| --- | --- |
| [!UICONTROL Manual A/B Test] | Vergelijkt twee of meer ervaringen om te zien welke beste ervaring conversies gedurende een vooraf bepaalde testperiode verbetert.<P>In deze sectie wordt beschreven hoe u een handleiding instelt [!UICONTROL A/B Test] , maar de stappen voor de andere typen [!UICONTROL A/B Test] de activiteiten zijn vergelijkbaar . |
| [!UICONTROL Auto-Allocate] | Identificeert een winnaar onder twee of meer ervaringen, en richt dan verkeer aan de winnaar opnieuw, die omzetting verhoogt aangezien de test loopt en leert.<P>Meer informatie over de voordelen van een [!UICONTROL Auto-Allocate] activiteit, zie [Automatisch toewijzen](/help/main/c-activities/t-test-ab/sample-size-determination.md#auto-allocate) in *Hoe lang moet u een A/B test uitvoeren* en [Overzicht van automatisch toewijzen](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md). |
| ![Premium badge](/help/main/assets/premium.png) [!UICONTROL Auto-Target] | Gebruikt geavanceerd computerleren om inhoud en aandrijvingsomzettingen aan te passen door veelvoudige hoog-presterende, markeer-bepaalde ervaringen te identificeren. De meest toegesneden ervaring wordt vervolgens aan bezoekers aangeboden op basis van hun individuele klantprofielen en gedrag van vergelijkbare bezoekers in het verleden.<P>Zie voor meer informatie [Automatisch doel](/help/main/c-activities/auto-target/auto-target-to-optimize.md). |

Voor meer informatie over welke van deze [!UICONTROL A/B Test] activiteiten zijn geschikt voor u, zie interactieve [Adobe Target Activity Guide PDF](/help/main/c-activities/target-activities-guide.md).

De stappen voor het maken van de drie typen [!UICONTROL A/B Test] de activiteiten zijn vergelijkbaar . Om een [!UICONTROL Auto-Allocate] of [!UICONTROL Auto-Target] activiteit, beginnen met [een A/B-testactiviteit maken](/help/main/c-activities/t-test-ab/t-test-create-ab/test-create-ab.md), maar wanneer u de [!UICONTROL Targeting] pagina, kies de gewenste methode van de verkeerstoewijzing, zoals hieronder getoond:

* [!UICONTROL Auto-allocate to best experience]
* [!UICONTROL Auto-target for personalized experience]

![Instellingen voor de methode voor verkeerstoewijzing](/help/main/c-activities/t-test-ab/t-test-create-ab/assets/traffic-allocation-method.png)

## Aanbevelingen opnemen in A/B-activiteiten

U kunt aanbevelingen opnemen in [!UICONTROL A/B Test], [!UICONTROL Auto-Allocate], en [!UICONTROL Auto-Target] activiteiten [!UICONTROL Experience Targeting] (XT) activiteiten. Zie voor meer informatie [Recommendations als voorstel](/help/main/c-recommendations/recommendations-as-an-offer.md).

Voor deze functionaliteit hebt u een [Licentie voor doelpremie](/help/main/c-intro/intro.md#premium)

## Trainingsvideo: Activiteitstypen (9:03) ![Overzicht badge](/help/main/assets/overview.png)

In deze video wordt uitgelegd welke soorten activiteiten beschikbaar zijn in [!DNL Target Standard/Premium].

* Beschrijf de soorten activiteiten die onder [!DNL Adobe Target]
* Selecteer het juiste type activiteit om uw doelen te bereiken
* Beschrijf de driestappenworkflow met instructies die van toepassing is op alle typen activiteiten

>[!VIDEO](https://video.tv.adobe.com/v/17386)
