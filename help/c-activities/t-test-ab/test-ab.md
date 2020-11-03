---
keywords: AB;A/B;AB...n;compare experiences;Targeting;compare content
description: Bij het testen van A/B worden twee of meer versies van de inhoud van uw website vergeleken om te zien welke versie het beste uw omzettingen tijdens een vooraf gespecificeerde testperiode verbetert.
title: A/B-test
feature: ab
uuid: 154559cf-58bb-425d-bb2e-4eaf34c89451
translation-type: tm+mt
source-git-commit: 130edc89b2c324a0d892a4221f644248e23357a4
workflow-type: tm+mt
source-wordcount: '705'
ht-degree: 0%

---


# A/B-test

Een handmatige A/B test vergelijkt twee of meer versies van uw inhoud van de Website om te zien welke versie beste uw omzettingen tijdens een vooraf gespecificeerde testperiode verbetert.

>[!NOTE]
>
>Naast de Handmatige (standaard) A/B-testactiviteit (in dit gedeelte besproken) [!DNL Target] biedt deze twee extra typen testactiviteiten voor A/B: [!UICONTROL Auto-Allocate] en [!UICONTROL Auto-Target].
>
>Zie [Typen testactiviteiten](#types) voor A/B hieronder voor meer informatie.

Een handmatige A/B test (die soms als A/B...N test wordt bedoeld) vergelijkt twee of meer versies van uw inhoud van de Website om te zien welke beste tilt uw omzettingen, verkoop, of andere metriek u identificeert. Gebruik een A/B test om veranderingen in uw pagina met uw standaardpaginaontwerp te vergelijken om te bepalen welke ervaring de beste resultaten veroorzaakt.

Handmatige A/B-tests zijn met name handig wanneer u een duidelijke hypothese hebt over de manieren waarop u de prestaties van uw pagina kunt verbeteren op basis van succeswaarden of alternatieve levering van inhoud.

Handmatige A/B-tests zijn zeer geschikt voor grote wijzigingen die nieuwe schermindelingen of drastisch verschillende behandelingen van de elementen kunnen inhouden. Als het testontwerp niet gemakkelijk in afzonderlijke pagina-elementen kan worden opgedeeld, voert u een A/B-test uit voordat u een multivariate test uitvoert.

Wanneer u de test instelt, kunt u bepalen welk percentage bezoekers elke ervaring zien. Bijvoorbeeld, zou u verkeer tussen de controle en een tweede ervaring gelijkmatig kunnen verdelen, of u zou een nieuwe, riskantere ervaring kunnen uittesten door het aan slechts 5% van uw publiek te tonen.

>[!NOTE]
>
>Zie [Uw A/B-test](../../c-activities/t-test-ab/sample-size-determination.md#concept_2801F552DB874C20B8A17C1B774C0383)plannen voor gedetailleerde informatie over het bepalen van de optimale monstergrootte voor een A/B-test.

Wanneer het aantal verschillende ervaringen vijf overschrijdt en zich twee of meer plaatsen overspannen, is het een goed idee om een test [te overwegen](/help/c-activities/c-multivariate-testing/multivariate-testing.md) MVT alvorens uw tests A/B uit te voeren. De multivariate test toont welke gebieden op de pagina het meest waarschijnlijk om omzetting zullen verbeteren. Dit zijn de locaties waarop een markeerteken zich moet concentreren. Bijvoorbeeld, zou de test MVT kunnen tonen dat de vraag aan actie de belangrijkste plaats voor het ontmoeten van uw doelstellingen is. Zodra u hebt bepaald welke plaatsen en inhoud het nuttigst zijn om u te helpen uw doelstellingen bereiken, kunt u een test A/B in werking stellen om de resultaten verder te verfijnen, zoals twee specifieke beelden tegen elkaar te testen, of de formulering of de kleuren van een vraag aan actie te vergelijken. Door een MVT-test met een of meer A/B-tests uit te voeren, kunt u de best mogelijke inhoud voor de gewenste resultaten bepalen.

## Typen A/B-testactiviteiten {#types}

Naast de Handmatige (standaard) A/B-testactiviteit (in dit gedeelte besproken) [!DNL Target] biedt deze twee extra typen testactiviteiten voor A/B: [!UICONTROL Auto-Allocate] en [!UICONTROL Auto-Target].

| Type activiteit | Beschrijving |
| --- | --- |
| Handmatige A/B-test | Vergelijkt twee of meer ervaringen om te zien welke omzettingen het best gedurende een vooraf bepaalde testperiode verbeteren.<br>In dit gedeelte wordt beschreven hoe u een handmatige A/B-testactiviteit instelt, maar de stappen voor de andere soorten A/B-testactiviteiten zijn vergelijkbaar. |
| [!UICONTROL Auto-Allocate] | Identificeert een winnaar onder twee of meer ervaringen, en richt dan verkeer aan de winnaar opnieuw, die omzetting verhoogt aangezien de test loopt en leert.<br>Zie [Automatisch toewijzen](/help/c-activities/automated-traffic-allocation/automated-traffic-allocation.md)voor meer informatie. |
| ![Premium badge](/help/assets/premium.png) [!UICONTROL Auto-Target] | Gebruikt geavanceerd computerleren om inhoud en aandrijvingsomzettingen aan te passen door veelvoudige hoog-presterende, markerings-bepaalde ervaringen te identificeren, en dan de meest op maat gemaakte ervaring aan bezoekers te dienen die op hun individuele klantenprofielen en verleden gedrag van gelijkaardige bezoekers worden gebaseerd.<br>Voor meer informatie, zie [auto-Doel](/help/c-activities/auto-target-to-optimize.md). |

Zie de interactieve PDF [van de](/help/c-activities/target-activities-guide.md)Adobe Target Activity Guide voor meer informatie over welke van deze A/B-testactiviteiten geschikt is voor u.

De stappen voor het maken van de drie typen testactiviteiten voor A/B zijn vergelijkbaar. Als u een [!UICONTROL Auto-Allocate] of [!UICONTROL Auto-Target] activiteit wilt maken, begint u met het [maken van een testactiviteit](/help/c-activities/t-test-ab/t-test-create-ab/test-create-ab.md)[!UICONTROL Targeting] voor A/B. Als u echter de pagina bereikt, kiest u de gewenste methode voor verkeerstoewijzing:

* [!UICONTROL Auto-allocate to best experience]
* [!UICONTROL Auto-target for personalized experience]

![Instellingen voor de methode voor verkeerstoewijzing](/help/c-activities/t-test-ab/t-test-create-ab/assets/traffic-allocation-method.png)

## Trainingsvideo: Activiteitstypen (9:03) ![overzichtspagina](/help/assets/overview.png)

In deze video worden de activiteitstypen uitgelegd die beschikbaar zijn in [!DNL Target Standard/Premium].

* Beschrijf de soorten activiteiten die onder [!DNL Adobe Target]
* Selecteer het juiste type activiteit om uw doelen te bereiken
* Beschrijf de driestappenworkflow met instructies die van toepassing is op alle typen activiteiten

>[!VIDEO](https://video.tv.adobe.com/v/17386)
