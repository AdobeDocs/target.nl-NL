---
keywords: mvt;multivariate test;multivariate beste praktijken van de test;mvt beste praktijken;mvt combinaties;mvt rapporten
description: Leer hoe u de prestaties kunt verbeteren, problemen kunt voorkomen en bekende problemen kunt verhelpen die zich kunnen voordoen bij het maken en uitvoeren van [!UICONTROL Multivariate Test] -activiteiten in  [!DNL Adobe Target] .
title: Welke beste praktijken voor een [!UICONTROL Multivariate Test] activiteit?
feature: Multivariate Tests
exl-id: bcd15517-1b5f-4425-9404-1d7dd0689e28
source-git-commit: 0d73a062f70080057c3323f5150af067e3a2e27e
workflow-type: tm+mt
source-wordcount: '610'
ht-degree: 0%

---

# [!UICONTROL Multivariate Test] aanbevolen procedures

Tips om u te helpen de prestaties te verbeteren, problemen te voorkomen en bekende problemen te verhelpen die zich kunnen voordoen bij het maken en uitvoeren van [!UICONTROL Multivariate Test] (MVT)-activiteiten in [!DNL Adobe Target] .

## Plan {#section_4D4A1F6226F042379BF48DB753608579}

* Houd rekening met de locaties op de pagina die belangrijke resultaten kunnen opleveren.

  Een banner of een hoofdafbeelding zal bijvoorbeeld waarschijnlijk meer omzettingen tot gevolg hebben dan een wijziging in de voettekst. Als u minder invloedrijke locaties in de test opneemt, neemt alleen de hoeveelheid verkeer en de tijd toe die nodig is om de prominentere locaties op de pagina te testen.
* Bereid uw paginavariaties voor op tijd.

  Houd rekening met de verschillen in inhoud voor elke aanbieding en maak afbeeldingen, tekst en HTML-aanbiedingen die u in de MVT-test wilt gebruiken.

## Maken {#section_C59C722CA82E48ABA58A4A7FA758F193}

* Neem niet meer combinaties op dan nodig is voor de test.

  Elke geteste combinatie verhoogt aanzienlijk de hoeveelheid verkeer en de tijd die nodig is om aanvaardbare resultaten te bereiken. Als u bijvoorbeeld drie locaties met elk drie aanbiedingen hebt, zijn er 27 mogelijke combinaties (3x3x3). Drie locaties, waar twee locaties drie mogelijke aanbiedingen bevatten en één locatie twee aanbiedingen heeft, bieden 18 opties (3x3x2). De aantallen stijgen substantieel met elke extra plaats en aanbieding.

* Locaties en aanbiedingen benoemen.

  U kunt de naam van elke locatie en het aanbod in de test wijzigen in iets nuttigers. Het aantal aanbiedingen op elke locatie wordt weergegeven in de locatiekop. Met nuttige namen kunt u uw voorstellen identificeren wanneer u rapporten controleert.

* Gebruik de voorvertoningsfuncties om ongewenste combinaties van inhoud te voorkomen.

  Bekijk alle ervaringen die door de test zijn gegenereerd voordat u live gaat. Zorg ervoor dat er geen combinaties zijn met tegenstrijdige claims (bijvoorbeeld 20% korting en $19 korting in dezelfde ervaring) of incompatibele ontwerpen, zoals achtergrond en lettertype met dezelfde kleur.

* Gebruik de [&#x200B; schatter van het Verkeer &#x200B;](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/traffic-estimator.md) om ervoor te zorgen dat uw test voor de hoeveelheid verkeer wordt ontworpen uw pagina ontvangt.

  Zorg ervoor dat de schatter van het Verkeer uw testconfiguratie het groene licht geeft zodat kunt u de resultaten krijgen u wenst.

* De alternatieven van elk element moeten aanzienlijk van elkaar verschillen.

## Analyseren {#section_9A2118CF1039451681C13D9AE79A58AB}

* Maak frequent gebruik van het [&#x200B; rapport van de Bijdrage van de Plaats &#x200B;](/help/main/c-reports/multivariate-test-reports/location-contribution-report.md) om de prestaties van elke plaats en aanbieding te controleren.
* In het [&#x200B; rapport van de Prestaties van de Ervaring &#x200B;](/help/main/c-reports/multivariate-test-reports/experience-performance-report.md), baseer uw besluiten op de getoonde gegevens gebruikend de [!UICONTROL Best 5] en [!UICONTROL Worst 5] filters.

  Met het filter [!UICONTROL All] is het moeilijk om de gewenste informatie op te halen en niet alle ervaringen kunnen in de grafiek worden weergegeven. Gebruik het filter [!UICONTROL All] als u een specifieke ervaring wilt bekijken die niet in de beste of slechtste vijf is.

## Follow-up {#section_1C44A767F6AB4441A3EAA8AC995F46B0}

* Hoewel u in [!DNL Target] een live activiteit kunt bewerken, kunt u de test opnieuw instellen wanneer u een actieve activiteit bewerkt. Sommige wijzigingen worden mogelijk niet herkend in rapporten. Het is veilig om wijzigingen aan te brengen in HTML-aanbiedingen die alleen in de aanbiedingenbibliotheek staan.

  De specifieke acties die ervaringsnamen en rapporten terugstellen omvatten:

   * Een nieuwe locatie toevoegen
   * Een locatie verwijderen
   * Nieuwe aanbiedingen toevoegen of aanbiedingen verwijderen van een bestaande locatie
   * Opgemaakte tekst bewerken
   * Opties voor het bewerken van achtergrondkleuren

* Door een MVT-test met een of meer A/B-tests uit te voeren, kunt u de best mogelijke inhoud voor de gewenste resultaten bepalen.

  Zodra u hebt bepaald welke plaatsen en inhoud het nuttigst om u te helpen uw doelstellingen bereiken, kunt u een test A/B in werking stellen om de resultaten verder te verfijnen. Als u bijvoorbeeld weet welke locaties het belangrijkst zijn, test u twee specifieke afbeeldingen met elkaar of vergelijkt u de tekst of kleuren van een call to action.
