---
keywords: AB;A/B;AB..n;vergelijk ervaringen;gericht;vergelijk inhoud;auto-doel;auto-toewijzen
description: Met een handmatige A/B-testactiviteit worden twee of meer versies van uw website-inhoud vergeleken om te zien welke versie uw conversies het beste verbetert tijdens een vooraf opgegeven testperiode.
title: A/B-testoverzicht
feature: A/B Tests
translation-type: tm+mt
source-git-commit: 48b94f967252f5ddb009597456edf0a43bc54ba6
workflow-type: tm+mt
source-wordcount: '717'
ht-degree: 0%

---


# A/B-testoverzicht

In een handleiding [!UICONTROL A/B Test] worden twee of meer versies van uw website-inhoud vergeleken om te zien welke versie uw conversies het beste verbetert tijdens een vooraf opgegeven testperiode.

>[!NOTE]
>
>Naast de Handmatige (Standaard) [!UICONTROL A/B Test] activiteit (in dit gedeelte besproken), biedt [!DNL Target] twee extra typen [!UICONTROL A/B Test] activiteiten: [!UICONTROL Auto-Allocate] en [!UICONTROL Auto-Target].
>
>Zie [Soorten A/B-testactiviteiten](#types) hieronder voor meer informatie.

Een handboek [!UICONTROL A/B Test] activiteit (die soms als A/B...N test wordt bedoeld) vergelijkt twee of meer versies van uw inhoud van de Website om te zien welke het beste optilt uw omzettingen, verkoop, of andere metriek u identificeert. Gebruik een A/B test om veranderingen in uw pagina met uw standaardpaginaontwerp te vergelijken om te bepalen welke ervaring de beste resultaten veroorzaakt.

Handmatige A/B-tests zijn met name handig wanneer u een duidelijke hypothese hebt over de manieren waarop u de prestaties van uw pagina kunt verbeteren op basis van succeswaarden of alternatieve levering van inhoud.

Handmatige A/B-tests zijn zeer geschikt voor grote wijzigingen die nieuwe schermindelingen of drastisch verschillende behandelingen van de elementen kunnen inhouden. Als uw testontwerp niet gemakkelijk in individuele paginaelementen opsplitst, zou u een test A/B vóór een [multivariate test](/help/c-activities/c-multivariate-testing/multivariate-testing.md) moeten in werking stellen.

Wanneer u opstelling uw test A/B, kunt u het percentage bezoekers bepalen die elke ervaring zien. Bijvoorbeeld, zou u verkeer tussen de controle en een tweede ervaring gelijkmatig kunnen verdelen, of u zou een nieuwe, riskantere ervaring kunnen uittesten door het aan slechts 5% van uw publiek te tonen.

>[!NOTE]
>
>Zie [Uw A/B-test plannen](/help/c-activities/t-test-ab/sample-size-determination.md) voor gedetailleerde informatie over het bepalen van de optimale monstergrootte voor een A/B-test.

Wanneer het aantal verschillende ervaringen vijf overschrijdt en zich twee of meer plaatsen overspannen, is het een goed idee om een [MVT test](/help/c-activities/c-multivariate-testing/multivariate-testing.md) alvorens uw tests A/B in werking te stellen te overwegen. De multivariate test toont welke gebieden op de pagina het meest waarschijnlijk om omzetting zullen verbeteren. Dit zijn de locaties waarop een markeerteken zich moet concentreren. Bijvoorbeeld, zou de test MVT kunnen tonen dat de vraag aan actie de belangrijkste plaats voor het ontmoeten van uw doelstellingen is. Zodra u hebt bepaald welke plaatsen en inhoud het nuttigst zijn om u te helpen uw doelstellingen bereiken, kunt u een test A/B dan in werking stellen om de resultaten verder te verfijnen, zoals twee specifieke beelden tegen elkaar te testen, of de formulering of de kleuren van een vraag aan actie te vergelijken. Door een MVT-test met een of meer A/B-tests uit te voeren, kunt u de best mogelijke inhoud voor de gewenste resultaten bepalen.

## Typen A/B-testactiviteiten {#types}

Naast de handmatige [!UICONTROL A/B Test]-activiteit (die in dit gedeelte wordt besproken), biedt [!DNL Target] twee extra typen A/B-testactiviteiten: [!UICONTROL Auto-Allocate] en [!UICONTROL Auto-Target].

| Type activiteit | Beschrijving |
| --- | --- |
| [!UICONTROL Manual A/B Test] | Vergelijkt twee of meer ervaringen om te zien welke omzettingen het best gedurende een vooraf bepaalde testperiode verbeteren.<br>In deze sectie wordt beschreven hoe u een handmatige  [!UICONTROL A/B Test] activiteit instelt, maar de stappen voor de andere typen  [!UICONTROL A/B Test] activiteiten zijn vergelijkbaar. |
| [!UICONTROL Auto-Allocate] | Identificeert een winnaar onder twee of meer ervaringen, en richt dan verkeer aan de winnaar opnieuw, die omzetting verhoogt aangezien de test loopt en leert.<br>Om over de voordelen te leren van het gebruiken van een auto-Wijs activiteit, zie  [auto-](/help/c-activities/t-test-ab/sample-size-determination.md#auto-allocate) Toewijzing in  *hoe lang u een A/B* Test en  [auto-Wijs overzicht](/help/c-activities/automated-traffic-allocation/automated-traffic-allocation.md) in werking moet stellen. |
| ![Premium badge](/help/assets/premium.png) [!UICONTROL Auto-Target] | Gebruikt geavanceerd computerleren om inhoud en aandrijvingsomzettingen aan te passen door veelvoudige hoog-presterende, markerings-bepaalde ervaringen te identificeren, en dan de meest op maat gemaakte ervaring aan bezoekers te dienen die op hun individuele klantenprofielen en verleden gedrag van gelijkaardige bezoekers worden gebaseerd.<br>Voor meer informatie, zie  [auto-Doel](/help/c-activities/auto-target/auto-target-to-optimize.md). |

Zie de interactieve [Adobe Target Activity Guide PDF](/help/c-activities/target-activities-guide.md) voor meer informatie over welke van deze [!UICONTROL A/B Test] activiteiten geschikt is voor u.

De stappen voor het creëren van de drie types van [!UICONTROL A/B Test] activiteiten zijn gelijkaardig. Als u een [!UICONTROL Auto-Allocate] of [!UICONTROL Auto-Target] activiteit wilt maken, begint u met [het maken van een A/B-testactiviteit](/help/c-activities/t-test-ab/t-test-create-ab/test-create-ab.md), maar wanneer u de pagina [!UICONTROL Targeting] bereikt, kiest u de gewenste methode voor verkeerstoewijzing, zoals hieronder wordt getoond:

* [!UICONTROL Auto-allocate to best experience]
* [!UICONTROL Auto-target for personalized experience]

![Instellingen voor de methode voor verkeerstoewijzing](/help/c-activities/t-test-ab/t-test-create-ab/assets/traffic-allocation-method.png)

## Trainingsvideo: Activiteitstypen (9:03) ![Overzichtsbadge](/help/assets/overview.png)

In deze video worden de activiteitstypen beschreven die beschikbaar zijn in [!DNL Target Standard/Premium].

* Beschrijf de soorten activiteiten inbegrepen in [!DNL Adobe Target]
* Selecteer het juiste type activiteit om uw doelen te bereiken
* Beschrijf de driestappenworkflow met instructies die van toepassing is op alle typen activiteiten

>[!VIDEO](https://video.tv.adobe.com/v/17386)
