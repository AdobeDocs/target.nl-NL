---
keywords: op formulieren gebaseerde ervaringscomposer;op formulieren gebaseerde composer;verfijningen
description: Leer hoe te om Adobe  [!DNL Target]  vorm-Gebaseerde Composer van de Ervaring voor niet-visuele ervaringsverwezenlijking te gebruiken. Gebruik deze composer wanneer VEC niet beschikbaar of niet praktisch is te gebruiken.
title: Hoe gebruik ik de op formulieren gebaseerde Experience Composer?
feature: Form-based Experience Composer
exl-id: d06a271b-f058-4c83-af75-da2a29774967
source-git-commit: 2f86c9ee89b4e1698180f6b3dc9df393733eb780
workflow-type: tm+mt
source-wordcount: '776'
ht-degree: 1%

---

# Formuliergebaseerde Experience Composer

[!DNL Adobe Target] [!UICONTROL Form-Based Experience Composer] is een niet-visuele ervaring en biedt een aanmaakinterface die handig is voor het maken van ervaringen voor gebruik in [!UICONTROL A/B Test] -, [!UICONTROL Experience Targeting] -, [!UICONTROL Automated Personalization] - en [!UICONTROL Recommendations] -activiteiten wanneer [!UICONTROL Visual Experience Composer] (VEC) niet beschikbaar of praktisch is voor gebruik. U kunt bijvoorbeeld de Form-Based Experience Composer gebruiken om ervaringen en aanbiedingen te maken voor levering in e-mails, kiosken en spraakassistenten.

Er zijn geen ervaringen als u een [!UICONTROL Recommendations] -activiteit maakt. Kies uw criteria en ontwerp. Als u meerdere criteria of ontwerpen kiest, genereert [!UICONTROL Target] automatisch de ervaringen.

1. Klik op **[!UICONTROL Create Activity]** en selecteer het type activiteit dat u wilt maken.

   [!UICONTROL Form-Based Experience Composer] is beschikbaar voor [!UICONTROL A/B Test] -, [!UICONTROL Experience Targeting] -, [!UICONTROL Automated Personalization] - en [!UICONTROL Recommendations] -activiteiten.

1. Selecteer **[!UICONTROL Form]** in het dialoogvenster [!UICONTROL Create Activity] .

1. (Voorwaardelijk) Kies een werkruimte en eigenschap.

1. Klik op **[!UICONTROL Next]**.

   De lus [!UICONTROL Form-Based Experience Composer] wordt geopend.

   ![&#x200B; location_affinements beeld &#x200B;](assets/location_refinements.png)

   Dit scherm is anders als u een [!UICONTROL Recommendations] activiteit creeert. [!UICONTROL Recommendations] -activiteiten omvatten geen ervaringen.

1. Noem de activiteit door &quot;[!UICONTROL Untitled Activity]&quot; te klikken.
1. Selecteer een locatie.

   Wanneer u in het vak [!UICONTROL Select Location] klikt, wordt een lijst met beschikbare locaties weergegeven. Selecteer een van deze locaties.

   U kunt ook een locatie invoeren die hier niet wordt vermeld. Dit kan handig zijn als het mbox nog niet is gemaakt of weergegeven op een pagina. Typ de naam van de locatie. Wees voorzichtig wanneer u een locatie invoert die nog niet bestaat. Als de spelling of het hoofdlettergebruik niet overeenkomt met de spelling en het hoofdlettergebruik op het moment dat de aanroep van de box wordt uitgevoerd, levert de activiteit geen resultaat. Handmatig ingevoerde locaties worden opgeslagen in de lijst met beschikbare locaties. De volgende keer dat u een handmatig ingevoerde locatie probeert te selecteren, is deze beschikbaar in de vervolgkeuzelijst [!UICONTROL Select Location] voor die activiteit.

   >[!NOTE]
   >
   >Als u een handmatig ingevoerde locatie maakt tijdens het maken van een activiteit, wordt niet automatisch een nieuwe locatie gemaakt. De locatienaam wordt alleen opgeslagen in de context van de activiteit. De plaats wordt gecreeerd wanneer er een vraag van de inhoudslevering is. Na de locatie die wordt gemaakt, zal deze beschikbaar zijn voor gebruik in andere activiteiten, voor het creëren van publiek, enz. in de vervolgkeuzelijst met beschikbare locaties.

1. Klik **[!UICONTROL Add Audience Refinements]**, kies één of meerdere [&#x200B; publiek &#x200B;](/help/main/c-target/target.md#concept_A782F8481A5041EBA75103CB26376522) voor deze activiteit, dan klik **[!UICONTROL Done]**.

   ![&#x200B; location_raffements_2 beeld &#x200B;](assets/location_refinements_2.png)

   In [!UICONTROL Form-based Experience Composer] zijn verfijningen vervangen door volledige publieksfunctionaliteit. De verfijningen voor bestaande activiteiten zijn gemigreerd aan [&#x200B; activiteit-slechts publiek &#x200B;](/help/main/c-target/creating-activity-only-audience.md#concept_A6BADCF530ED4AE1852E677FEBE68483).

1. Selecteer het type inhoud dat u op die locatie wilt weergeven.

   ![&#x200B; form_content beeld &#x200B;](assets/form_content.png)

1. Geef voor het geselecteerde inhoudstype de inhoud op.

   **Aanbieding van HTML van de Verandering:** kies een aanbieding van HTML.

   **Aanbieding van het Beeld van de Verandering:** kies een beeld in de inhoudsbibliotheek in Doel wordt bewaard dat.

   U kunt ook een koppeling naar een afbeelding toevoegen (doorklikken, bestemming, landen, enzovoort).

   1. Klik op [!UICONTROL Change Image Offer].
   1. Selecteer de gewenste afbeelding en klik op [!UICONTROL Edit Links] .
   1. Geef de gewenste URL of pagina op de site op en klik op [!UICONTROL Update] .

   **de aanbieding van JSON van de Verandering:** kies een json aanbieding.

   **de Fragment van de Ervaring van de Verandering:** kies een Fragment van de Ervaring. Voor meer informatie, zie [&#x200B; Fragment van de Ervaring &#x200B;](/help/main/c-experiences/c-manage-content/aem-experience-fragments.md).

   **Verandering richt Aanbieding om:** kies een omleidingsaanbieding. Voor meer informatie, zie [&#x200B; leiden aanbiedingen &#x200B;](/help/main/c-experiences/c-manage-content/offer-redirect.md) om.

   **Verre Aanbieding van de Verandering:** kies een verre aanbieding. Voor meer informatie, zie [&#x200B; verre aanbiedingen &#x200B;](/help/main/c-experiences/c-manage-content/about-remote-offers.md) creëren.

   **creeer de Aanbieding van HTML:**

   1. Klik op [!UICONTROL Offers] en selecteer vervolgens het tabblad [!UICONTROL Code Offers].
   1. Klik op [!UICONTROL Create] > [!UICONTROL HTML Offer] .
   1. Typ een naam voor het voorstel.
   1. Typ of plak de HTML-code in het vak Code.
   1. Klik op [!UICONTROL Save].

   **creeer JSON Aanbieding:**

   1. Klik op [!UICONTROL Offers] en selecteer vervolgens het tabblad [!UICONTROL Code Offers].
   1. Klik op [!UICONTROL Create] > [!UICONTROL JSON Offer] .
   1. Typ een naam voor het voorstel.
   1. Typ of plak uw JSON-code in het vak Code.
   1. Klik op [!UICONTROL Save].

   **voeg Aanbeveling toe:**

   Voor een activiteit van Aanbevelingen, geeft de drop-down Inhoud u de [!UICONTROL Add Recommendation] optie. Klik op **[!UICONTROL Add Recommendation]** en selecteer het paginatype. Dan volg de gebruikelijke stappen zoals die in de interface worden bepaald [&#x200B; creeer een activiteit van Aanbevelingen &#x200B;](/help/main/c-recommendations/t-create-recs-activity/create-recs-activity.md).

   Bij het selecteren van criteria voor Aanbevelingen in de Form-Based Experience Composer is er nu een directe koppeling naar de geselecteerde Criteria Card zodat u de criteria snel en eenvoudig kunt bewerken.

   ![&#x200B; change_criteria beeld &#x200B;](assets/change_criteria.png)

   Van de Doelpagina van het Doel driestappe geleide werkschema:

   ![&#x200B; change_criteria_2 beeld &#x200B;](assets/change_criteria_2.png)

   **voeg Besluit van de Aanbieding toe:**

   Voeg een aanbieding die in [!DNL Adobe Journey Optimizer] (AJO) is gemaakt toe aan een [!DNL Adobe Target] -activiteit om de beste dynamische aanbieding en ervaring aan uw bezoekers op uw website of mobiele site te presenteren met behulp van de functie voor het bepalen van aanbiedingen. Deze optie is alleen beschikbaar voor handmatige [!UICONTROL A/B Test] - en [!UICONTROL Experience Targeting] -activiteiten (XT).

   Voor meer informatie, zie [&#x200B; Aanbiedingsbesluiten van het Gebruik &#x200B;](/help/main/c-integrating-target-with-mac/ajo/offer-decision.md).

1. (Optioneel, voor [!UICONTROL A/B Test] -, [!UICONTROL Automated Personalization] - en [!UICONTROL Experience Targeting] -activiteiten) Als u dit proces voor extra locaties wilt herhalen, klikt u op **[!UICONTROL Add Location]** en configureert u de locatie en inhoud.
1. Klik op **[!UICONTROL Next]** en voer de gebruikelijke stappen voor het maken van activiteiten uit voor het type activiteit.

* [&#x200B; creeer een Test A/B &#x200B;](/help/main/c-activities/t-test-ab/t-test-create-ab/test-create-ab.md)
* [&#x200B; creeer een Ervaring richtend Activiteit &#x200B;](/help/main/c-activities/t-experience-target/t-xt-create/xt-create.md#task_D6B3429AC31549E1A70EDF04B3DDC765)
* [Een activiteit voor aanbevelingen maken](/help/main/c-recommendations/t-create-recs-activity/create-recs-activity.md#task_6874328773C64C44A73F0A130AD3F96F)

## De video van de opleiding: Op vorm-Gebaseerde Composer ![&#x200B; badge van het Leerprogramma &#x200B;](/help/main/assets/tutorial.png)

Deze video bevat een demo van de op formulieren gebaseerde composer.

* Een activiteit maken met de Form-Based Experience Composer
* Begrijp wanneer om vorm-Gebaseerde Composer van de Ervaring tegenover Visual Experience Composer te gebruiken
* Verfijningen gebruiken om een locatie als doel in te stellen

>[!VIDEO](https://video.tv.adobe.com/v/17390)
