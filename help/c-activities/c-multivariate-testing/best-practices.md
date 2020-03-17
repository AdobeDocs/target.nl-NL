---
keywords: mvt;multivariate test;multivariate test best practices;mvt best practices;mvt combinations;mvt reports
description: Tips om u te helpen de prestaties te verbeteren, problemen te voorkomen en bekende problemen te verhelpen die zich kunnen voordoen bij het maken en uitvoeren van multivariate testactiviteiten in Adobe Target.
title: Best practices voor multivariatie testen met Adobe Target
topic: Standard
uuid: 4468a2eb-3fc1-4bc5-85ac-90cc02db4fbb
translation-type: tm+mt
source-git-commit: 217ca811521e67dcd1b063d77a644ba3ae94a72c

---


# Best practices voor multivariatie testen{#multivariate-test-best-practices}

Tips om u te helpen prestaties verbeteren, problemen te vermijden en bekende problemen te verhelpen die zich kunnen voordoen bij het maken en uitvoeren van MVT-activiteiten (Multivariate Test) in [!DNL Adobe Target].

## Plan {#section_4D4A1F6226F042379BF48DB753608579}

* Houd rekening met de locaties op de pagina die belangrijke resultaten kunnen opleveren.

   Een banner of een hoofdafbeelding zal bijvoorbeeld waarschijnlijk meer omzettingen tot gevolg hebben dan een wijziging in de voettekst. Als u minder invloedrijke locaties in de test opneemt, neemt alleen de hoeveelheid verkeer en de tijd toe die nodig is om de prominente locaties op de pagina te testen.
* Bereid uw paginavariaties voor op tijd.

   Houd rekening met de verschillen in inhoud voor elke aanbieding en maak afbeeldingen, tekst en HTML-aanbiedingen die u in de MVT-test wilt gebruiken.

## Maken {#section_C59C722CA82E48ABA58A4A7FA758F193}

* Neem niet meer combinaties op dan nodig is voor de test.

   Elke geteste combinatie verhoogt aanzienlijk de hoeveelheid verkeer en de tijd die nodig is om aanvaardbare resultaten te bereiken. Als u bijvoorbeeld drie locaties met elk drie aanbiedingen hebt, zijn er 27 mogelijke combinaties (3x3x3). Drie locaties, waar twee locaties drie mogelijke aanbiedingen bevatten en één locatie twee aanbiedingen heeft, bieden 18 opties (3x3x2). De aantallen stijgen substantieel met elke extra plaats en aanbieding.

* Locaties en aanbiedingen benoemen.

   U kunt de naam van elke locatie en het aanbod in de test wijzigen in iets nuttigers. Het aantal aanbiedingen op elke locatie wordt weergegeven in de locatiekop. Met nuttige namen kunt u uw voorstellen identificeren wanneer u rapporten onderzoekt.

* Gebruik de voorvertoningsfuncties om ongewenste combinaties van inhoud te voorkomen.

   Bekijk alle ervaringen die door de test zijn gegenereerd voordat u live gaat. Zorg ervoor dat er geen combinaties zijn met tegenstrijdige claims (bijvoorbeeld 20% korting en $19 korting in dezelfde ervaring) of met incompatibele ontwerpen, zoals achtergrond en lettertype met dezelfde kleur.

* Gebruik de [schatter](/help/c-activities/c-multivariate-testing/t-create-multivariate-test/traffic-estimator.md) van het Verkeer om ervoor te zorgen dat uw test voor de hoeveelheid verkeer wordt ontworpen uw pagina ontvangt.

   Zorg ervoor de schatter van het Verkeer uw testconfiguratie het groene licht geeft zodat kunt u de resultaten krijgen u wenst.
* Aanbevolen wordt dat de alternatieven van elk element aanzienlijk van elkaar verschillen.

## Analyseren {#section_9A2118CF1039451681C13D9AE79A58AB}

* Vaak gebruik maken van het rapport [](/help/c-reports/location-contribution-report.md) Locatiebijdrage om de prestaties van elke locatie en elke aanbieding te controleren.
* In het rapport [van de Prestaties van de](/help/c-reports/experience-performance-report.md)Ervaring, baseer uw besluiten op de gegevens die gebruikend Beste 5 en de Beste 5 filters worden getoond.

   Het [!UICONTROL All] filter maakt het moeilijk om de gewenste informatie op te halen en niet alle ervaringen kunnen in de grafiek worden weergegeven. Gebruik het [!UICONTROL All] filter als u een specifieke ervaring wilt bekijken die niet in de beste of slechtste vijf is.

## Follow-up {#section_1C44A767F6AB4441A3EAA8AC995F46B0}

* Hoewel u een actieve activiteit [!DNL Target] kunt bewerken, dient u niet te vergeten dat het bewerken van een actieve activiteit de test opnieuw kan instellen. In rapporten worden sommige wijzigingen mogelijk niet herkend. Het is veilig om wijzigingen aan HTML-aanbiedingen aan te brengen die alleen in de aanbiedingsbibliotheek staan.

   De specifieke acties die ervaringsnamen en rapporten terugstellen zijn:

   * Een nieuwe locatie toevoegen
   * Een locatie verwijderen
   * Nieuwe aanbiedingen toevoegen of aanbiedingen verwijderen van een bestaande locatie
   * Opgemaakte tekst bewerken
   * Opties voor het bewerken van achtergrondkleuren

* Door een MVT-test met een of meer A/B-tests uit te voeren, kunt u de best mogelijke inhoud voor de gewenste resultaten bepalen.

   Zodra u hebt bepaald welke plaatsen en inhoud het nuttigst om u te helpen uw doelstellingen bereiken, kunt u een test A/B in werking stellen om de resultaten verder te verfijnen. Wanneer u bijvoorbeeld weet welke locaties het belangrijkst zijn, test u twee specifieke afbeeldingen met elkaar of vergelijkt u de tekst of kleuren van een oproep tot actie.

