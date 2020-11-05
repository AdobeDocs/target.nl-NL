---
keywords: AB;A/B;AB...n;compare experiences;Targeting;compare content;auto-target;auto-allocate
description: Met een handmatige A/B-testactiviteit worden twee of meer versies van uw website-inhoud vergeleken om te zien welke versie uw conversies het beste verbetert tijdens een vooraf opgegeven testperiode.
title: A/B-testoverzicht
feature: ab
uuid: 154559cf-58bb-425d-bb2e-4eaf34c89451
translation-type: tm+mt
source-git-commit: 95450abc32be19d04b791af3c62673e9411ab53c
workflow-type: tm+mt
source-wordcount: '706'
ht-degree: 0%

---


# A/B-testoverzicht

Met een handmatige [!UICONTROL A/B Test] activiteit worden twee of meer versies van uw website-inhoud vergeleken om te zien welke versie uw conversies het beste verbetert tijdens een vooraf opgegeven testperiode.

>[!NOTE]
>
>Naast de [!UICONTROL A/B Test] activiteit Handmatig (Standaard) (die in deze sectie wordt besproken), [!DNL Target] verstrekt twee extra soorten [!UICONTROL A/B Test] activiteiten: [!UICONTROL Auto-Allocate] en [!UICONTROL Auto-Target].
>
>Zie [Typen testactiviteiten](#types) voor A/B hieronder voor meer informatie.

Een handmatige [!UICONTROL A/B Test] activiteit (die soms als test A/B...N wordt bedoeld) vergelijkt twee of meer versies van uw inhoud van de Website om te zien welke beste tilt uw omzettingen, verkoop, of andere metriek u identificeert. Gebruik een A/B test om veranderingen in uw pagina met uw standaardpaginaontwerp te vergelijken om te bepalen welke ervaring de beste resultaten veroorzaakt.

Handmatige A/B-tests zijn met name handig wanneer u een duidelijke hypothese hebt over de manieren waarop u de prestaties van uw pagina kunt verbeteren op basis van succeswaarden of alternatieve levering van inhoud.

Handmatige A/B-tests zijn zeer geschikt voor grote wijzigingen die nieuwe schermindelingen of drastisch verschillende behandelingen van de elementen kunnen inhouden. Als het testontwerp niet gemakkelijk in afzonderlijke pagina-elementen kan worden opgedeeld, voert u een A/B-test uit voordat u een [multivariate test](/help/c-activities/c-multivariate-testing/multivariate-testing.md)uitvoert.

Wanneer u opstelling uw test A/B, kunt u het percentage bezoekers bepalen die elke ervaring zien. Bijvoorbeeld, zou u verkeer tussen de controle en een tweede ervaring gelijkmatig kunnen verdelen, of u zou een nieuwe, riskantere ervaring kunnen uittesten door het aan slechts 5% van uw publiek te tonen.

>[!NOTE]
>
>Zie [Uw A/B-test](/help/c-activities/t-test-ab/sample-size-determination.md)plannen voor gedetailleerde informatie over het bepalen van de optimale monstergrootte voor een A/B-test.

Wanneer het aantal verschillende ervaringen vijf overschrijdt en zich twee of meer plaatsen overspannen, is het een goed idee om een test [te overwegen](/help/c-activities/c-multivariate-testing/multivariate-testing.md) MVT alvorens uw tests A/B uit te voeren. De multivariate test toont welke gebieden op de pagina het meest waarschijnlijk om omzetting zullen verbeteren. Dit zijn de locaties waarop een markeerteken zich moet concentreren. Bijvoorbeeld, zou de test MVT kunnen tonen dat de vraag aan actie de belangrijkste plaats voor het ontmoeten van uw doelstellingen is. Zodra u hebt bepaald welke plaatsen en inhoud het nuttigst zijn om u te helpen uw doelstellingen bereiken, kunt u een test A/B dan in werking stellen om de resultaten verder te verfijnen, zoals twee specifieke beelden tegen elkaar te testen, of de formulering of de kleuren van een vraag aan actie te vergelijken. Door een MVT-test met een of meer A/B-tests uit te voeren, kunt u de best mogelijke inhoud voor de gewenste resultaten bepalen.

## Typen A/B-testactiviteiten {#types}

Naast de handmatige [!UICONTROL A/B Test] activiteit (besproken in dit deel) [!DNL Target] biedt het twee extra typen testactiviteiten voor A/B: [!UICONTROL Auto-Allocate] en [!UICONTROL Auto-Target].

| Type activiteit | Beschrijving |
| --- | --- |
| [!UICONTROL Manual A/B Test] | Vergelijkt twee of meer ervaringen om te zien welke omzettingen het best gedurende een vooraf bepaalde testperiode verbeteren.<br>In deze sectie wordt beschreven hoe u een handmatige [!UICONTROL A/B Test] activiteit instelt, maar de stappen voor de andere typen [!UICONTROL A/B Test] activiteiten zijn vergelijkbaar. |
| [!UICONTROL Auto-Allocate] | Identificeert een winnaar onder twee of meer ervaringen, en richt dan verkeer aan de winnaar opnieuw, die omzetting verhoogt aangezien de test loopt en leert.<br>Zie [Automatisch toewijzen](/help/c-activities/t-test-ab/sample-size-determination.md#auto-allocate) in *Hoe lang moet u een A/B-test* uitvoeren en een overzicht [](/help/c-activities/automated-traffic-allocation/automated-traffic-allocation.md)Automatisch toewijzen voor meer informatie over de voordelen van het gebruik van een activiteit voor automatisch toewijzen. |
| ![Premium badge](/help/assets/premium.png) [!UICONTROL Auto-Target] | Gebruikt geavanceerd computerleren om inhoud en aandrijvingsomzettingen aan te passen door veelvoudige hoog-presterende, markerings-bepaalde ervaringen te identificeren, en dan de meest op maat gemaakte ervaring aan bezoekers te dienen die op hun individuele klantenprofielen en verleden gedrag van gelijkaardige bezoekers worden gebaseerd.<br>Voor meer informatie, zie [auto-Doel](/help/c-activities/auto-target/auto-target-to-optimize.md). |

Zie de interactieve PDF [!UICONTROL A/B Test] van de [Adobe Target Activity Guide voor meer informatie over welke van deze](/help/c-activities/target-activities-guide.md)activiteiten geschikt is voor u.

De stappen voor het maken van de drie soorten [!UICONTROL A/B Test] activiteiten zijn vergelijkbaar. Om een [!UICONTROL Auto-Allocate] of [!UICONTROL Auto-Target] activiteit tot stand te brengen, begin door een activiteit [van de Test van A/B te](/help/c-activities/t-test-ab/t-test-create-ab/test-create-ab.md)creëren, maar wanneer u aan de [!UICONTROL Targeting] pagina krijgt, kies de gewenste methode van de verkeerstoewijzing, zoals hieronder getoond:

* [!UICONTROL Auto-allocate to best experience]
* [!UICONTROL Auto-target for personalized experience]

![Instellingen voor de methode voor verkeerstoewijzing](/help/c-activities/t-test-ab/t-test-create-ab/assets/traffic-allocation-method.png)

## Trainingsvideo: Activiteitstypen (9:03) ![overzichtspagina](/help/assets/overview.png)

In deze video worden de activiteitstypen uitgelegd die beschikbaar zijn in [!DNL Target Standard/Premium].

* Beschrijf de soorten activiteiten die onder [!DNL Adobe Target]
* Selecteer het juiste type activiteit om uw doelen te bereiken
* Beschrijf de driestappenworkflow met instructies die van toepassing is op alle typen activiteiten

>[!VIDEO](https://video.tv.adobe.com/v/17386)
