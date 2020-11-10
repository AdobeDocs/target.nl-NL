---
keywords: form-based experience composer;form-based composer;refinements
description: Met de Form-Based Experience Composer kunt u niet-visuele ervaringen creëren.
title: Formuliergebaseerde Experience Composer
feature: form-based composer
translation-type: tm+mt
source-git-commit: 968d36d65016e51290f6bf754f69c91fd8f68405
workflow-type: tm+mt
source-wordcount: '705'
ht-degree: 2%

---


# Formuliergebaseerde Experience Composer{#form-based-experience-composer}

De Form-Based Experience Composer is een niet-visuele ervaring en biedt een aanmaakinterface die handig is voor het maken van ervaringen voor gebruik in A/B Tests, Experience Targeting, Automated Personalization en Recommendations activiteiten als de visuele ervaringscomposer niet beschikbaar of praktisch is voor gebruik. U kunt bijvoorbeeld de op formulieren gebaseerde composer gebruiken om ervaringen en aanbiedingen te maken voor levering in e-mails, kiosken en spraakassistenten.

Er zijn geen ervaringen als u een Recommendations-activiteit maakt. Kies uw criteria en ontwerp. Als u meerdere criteria of ontwerpen kiest, genereert Target automatisch de ervaringen.

1. Klik **[!UICONTROL Create Activity]** en selecteer het type activiteit dat u wilt maken.

   De Form-Based Experience Composer is beschikbaar voor A/B tests, Experience Targeting, Automated Personalization en Recommendations activiteiten.
1. Selecteer **[!UICONTROL Form-Based Experience Composer]** in het [!UICONTROL New Activity]dialoogvenster.

   De op formulieren gebaseerde Experience Composer wordt geopend.

   ![](assets/location_refinements.png)

   Dit scherm is anders als u een Recommendations-activiteit maakt. De activiteiten van Recommendations omvatten geen ervaringen.
1. Geef de activiteit een naam.
1. Selecteer een locatie.

   Wanneer u in het [!UICONTROL Select Location] vak klikt, wordt een lijst met beschikbare locaties weergegeven. Selecteer een van deze locaties. Kies &quot;target-global-mbox&quot; als u de algemene locatie wilt kiezen die via target.js wordt geleverd.

   U kunt ook een locatie invoeren die hier niet wordt vermeld. Dit kan handig zijn als het mbox nog niet is gemaakt of weergegeven op een pagina. Typ de naam van de locatie. Wees voorzichtig wanneer u een locatie invoert die nog niet bestaat. Als de spelling of het hoofdlettergebruik niet overeenkomt met de spelling en het hoofdlettergebruik op het moment dat de aanroep van de box wordt uitgevoerd, levert de activiteit geen resultaat. Handmatig ingevoerde locaties worden opgeslagen in de lijst met beschikbare locaties. De volgende keer dat u een handmatig ingevoerde locatie probeert te selecteren, is deze beschikbaar in de [!UICONTROL Select Location] vervolgkeuzelijst voor die activiteit.

   >[!NOTE]
   >
   >Als u een handmatig ingevoerde locatie maakt tijdens het maken van een activiteit, wordt niet automatisch een nieuwe locatie gemaakt. De locatienaam wordt alleen opgeslagen in de context van de activiteit. De plaats wordt gecreeerd wanneer er een vraag van de inhoudslevering is. Na de locatie die wordt gemaakt, zal deze beschikbaar zijn voor gebruik in andere activiteiten, voor het creëren van publiek, enz. in de vervolgkeuzelijst met beschikbare locaties.

1. Klik **[!UICONTROL Add Audience Refinements]** en kies een of meer [doelgroepen](/help/c-target/target.md#concept_A782F8481A5041EBA75103CB26376522) voor deze activiteit.

   ![](assets/location_refinements_2.png)

   In de Form-based Experience Composer zijn Refinements vervangen door volledige publieksfunctionaliteit. Verfijningen voor bestaande activiteiten zijn gemigreerd naar [activiteiten-alleen-publiek](/help/c-target/creating-activity-only-audience.md#concept_A6BADCF530ED4AE1852E677FEBE68483).
1. Selecteer het type inhoud dat u op die locatie wilt weergeven.

   ![](assets/form_content.png)

1. Geef voor het geselecteerde inhoudstype de inhoud op.

   **HTML-voorstel wijzigen:** Kies een HTML-aanbieding.

   **Afbeeldingsvoorstel wijzigen:** Kies een afbeelding die is opgeslagen in de inhoudsbibliotheek in Doel.

   U kunt ook een koppeling naar een afbeelding toevoegen (doorklikken, bestemming, landen, enzovoort).

   1. Klik op [!UICONTROL Change Image Offer].
   1. Selecteer de gewenste afbeelding en klik op [!UICONTROL Edit Links].
   1. Geef de gewenste URL of pagina op uw site op en klik op [!UICONTROL Update].

   **JSON-voorstel wijzigen:** Kies een aanbieding voor json.

   **Fragment ervaring wijzigen:** Kies een ervaringsfragment.

   **Omleidingsvoorstel wijzigen:** Kies een omleidingsvoorstel.

   **Externe aanbieding wijzigen:** Kies een externe aanbieding.

   **HTML-voorstel maken:**

   1. Klik op [!UICONTROL Offers] en selecteer vervolgens het tabblad [!UICONTROL Code Offers].
   1. Klik op [!UICONTROL Create] > [!UICONTROL HTML Offer].
   1. Typ een naam voor het voorstel.
   1. Typ of plak de HTML-code in het vak Code.
   1. Klik op [!UICONTROL Save].

   **JSON-voorstel maken:**

   1. Klik op [!UICONTROL Offers] en selecteer vervolgens het tabblad [!UICONTROL Code Offers].
   1. Klik op [!UICONTROL Create] > [!UICONTROL JSON Offer].
   1. Typ een naam voor het voorstel.
   1. Typ of plak uw JSON-code in het vak Code.
   1. Klik op [!UICONTROL Save].

   Voor een Recommendations-activiteit bevat de vervolgkeuzelijst Inhoud de optie Aanbeveling toevoegen. Klik **[!UICONTROL Add Recommendation]** en selecteer het paginatype. Voer vervolgens de gebruikelijke stappen uit zoals gedefinieerd in de interface om een Recommendations-activiteit [te](/help/c-recommendations/t-create-recs-activity/create-recs-activity.md)maken.

   Bij het selecteren van Recommendations-criteria in de Form-Based Experience Composer is er nu een directe koppeling naar de geselecteerde Criteria Card zodat u de criteria snel en eenvoudig kunt bewerken.

   ![](assets/change_criteria.png)

   Van de Doelpagina van het Doel driestappe geleide werkschema:

   ![](assets/change_criteria_2.png)

1. (Optioneel, voor AB-activiteiten, Automated Personalization en Experience Targeting) U kunt dit proces voor extra locaties herhalen door op de locatie en inhoud te klikken **[!UICONTROL Add Location]** en deze te configureren.
1. Klik **[!UICONTROL Next]** en voer de gebruikelijke stappen voor het maken van activiteiten voor het type activiteit uit.

* [Een A/B-test maken](/help/c-activities/t-test-ab/t-test-create-ab/test-create-ab.md)
* [Een ervaring maken die gericht is op activiteiten](/help/c-activities/t-experience-target/t-xt-create/xt-create.md#task_D6B3429AC31549E1A70EDF04B3DDC765)
* [Een Recommendations-activiteit maken](/help/c-recommendations/t-create-recs-activity/create-recs-activity.md#task_6874328773C64C44A73F0A130AD3F96F)

## Trainingsvideo: Zelfstudie ![voor formuliergebaseerde composer](/help/assets/tutorial.png)

Deze video bevat een demo van de op formulieren gebaseerde composer.

* Een activiteit maken met de Form-Based Experience Composer
* Begrijp wanneer om vorm-Gebaseerde Composer van de Ervaring tegenover Visual Experience Composer te gebruiken
* Verfijningen gebruiken om een locatie als doel in te stellen

>[!VIDEO](https://video.tv.adobe.com/v/17390)