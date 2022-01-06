---
keywords: op formulieren gebaseerde ervaringscomposer;op formulieren gebaseerde composer;verfijningen
description: Leer hoe u de Adobe gebruikt [!DNL Target] Form-Based Experience Composer voor het maken van niet-visuele beleving. Gebruik deze composer wanneer VEC niet beschikbaar of niet praktisch is te gebruiken.
title: Hoe gebruik ik de op formulieren gebaseerde Experience Composer?
feature: Form-based Experience Composer
exl-id: d06a271b-f058-4c83-af75-da2a29774967
source-git-commit: fb9c9e4d2a3d0cf330724dfd02e329fedc388f01
workflow-type: tm+mt
source-wordcount: '766'
ht-degree: 2%

---

# Formuliergebaseerde Experience Composer

De [!DNL Adobe Target] [!UICONTROL Form-Based Experience Composer] is een niet-visuele ervaring en biedt een aanmaakinterface die handig is voor het maken van ervaringen voor gebruik in [!UICONTROL A/B Test], [!UICONTROL Experience Targeting], [!UICONTROL Automated Personalization], en [!UICONTROL Recommendations] wanneer de [!UICONTROL Visual Experience Composer] (VEC) niet beschikbaar of praktisch voor gebruik. U kunt bijvoorbeeld de Form-Based Experience Composer gebruiken om ervaringen en aanbiedingen te maken voor levering in e-mails, kiosken en spraakassistenten.

Als u een [!UICONTROL Recommendations] geen ervaring. Kies uw criteria en ontwerp. Als u meerdere criteria of ontwerpen kiest, [!UICONTROL Target] genereert automatisch de ervaringen.

1. Klikken **[!UICONTROL Create Activity]** Selecteer vervolgens het type activiteit dat u wilt maken.

   De [!UICONTROL Form-Based Experience Composer] is beschikbaar voor [!UICONTROL A/B Test], [!UICONTROL Experience Targeting], [!UICONTROL Automated Personalization], en [!UICONTROL Recommendations] activiteiten.

1. Selecteren **[!UICONTROL Form]** van de [!UICONTROL Create Activity] in.

1. (Voorwaardelijk) Kies een werkruimte en eigenschap.

1. Klik op **[!UICONTROL Next]**.

   De [!UICONTROL Form-Based Experience Composer] wordt geopend.

   ![](assets/location_refinements.png)

   Dit scherm is anders als u een [!UICONTROL Recommendations] activiteit. [!UICONTROL Recommendations] activiteiten omvatten geen ervaring.

1. Geef een naam op voor de activiteit door op &quot;[!UICONTROL Untitled Activity].&quot;
1. Selecteer een locatie.

   Wanneer u in [!UICONTROL Select Location] wordt een lijst met beschikbare locaties weergegeven. Selecteer een van deze locaties.

   U kunt ook een locatie invoeren die hier niet wordt vermeld. Dit kan handig zijn als het mbox nog niet is gemaakt of weergegeven op een pagina. Typ de naam van de locatie. Wees voorzichtig wanneer u een locatie invoert die nog niet bestaat. Als de spelling of het hoofdlettergebruik niet overeenkomt met de spelling en het hoofdlettergebruik op het moment dat de aanroep van de box wordt uitgevoerd, levert de activiteit geen resultaat. Handmatig ingevoerde locaties worden opgeslagen in de lijst met beschikbare locaties. De volgende keer dat u een handmatig ingevoerde locatie probeert te selecteren, kunt u deze vinden op het tabblad [!UICONTROL Select Location] vervolgkeuzelijst voor die activiteit.

   >[!NOTE]
   >
   >Als u een handmatig ingevoerde locatie maakt tijdens het maken van een activiteit, wordt niet automatisch een nieuwe locatie gemaakt. De locatienaam wordt alleen opgeslagen in de context van de activiteit. De plaats wordt gecreeerd wanneer er een vraag van de inhoudslevering is. Na de locatie die wordt gemaakt, zal deze beschikbaar zijn voor gebruik in andere activiteiten, voor het creëren van publiek, enz. in de vervolgkeuzelijst met beschikbare locaties.

1. Klikken **[!UICONTROL Add Audience Refinements]** kiest u een of meer [publiek](/help/c-target/target.md#concept_A782F8481A5041EBA75103CB26376522) voor deze activiteit klikt u op **[!UICONTROL Done]**.

   ![](assets/location_refinements_2.png)

   In de [!UICONTROL Form-based Experience Composer]verfijningen zijn vervangen door volledige publieksfunctionaliteit. Verfijningen voor bestaande activiteiten zijn gemigreerd naar [alleen-activiteitstoepassingen](/help/c-target/creating-activity-only-audience.md#concept_A6BADCF530ED4AE1852E677FEBE68483).

1. Selecteer het type inhoud dat u op die locatie wilt weergeven.

   ![](assets/form_content.png)

1. Geef voor het geselecteerde inhoudstype de inhoud op.

   **HTML-voorstel wijzigen:** Kies een HTML-voorstel.

   **Afbeeldingsvoorstel wijzigen:** Kies een afbeelding die is opgeslagen in de inhoudsbibliotheek in Doel.

   U kunt ook een koppeling naar een afbeelding toevoegen (doorklikken, bestemming, landen, enzovoort).

   1. Klik op [!UICONTROL Change Image Offer].
   1. Selecteer de gewenste afbeelding en klik op [!UICONTROL Edit Links].
   1. Geef de gewenste URL of pagina op uw site op en klik vervolgens op [!UICONTROL Update].

   **JSON-voorstel wijzigen:** Kies een aanbieding voor json.

   **Fragment ervaring wijzigen:** Kies een ervaringsfragment. Zie voor meer informatie [Ervaar fragment](/help/c-experiences/c-manage-content/aem-experience-fragments.md).

   **Omleidingsvoorstel wijzigen:** Kies een omleidingsvoorstel. Zie voor meer informatie [Omleidingsvoorstellen maken](/help/c-experiences/c-manage-content/offer-redirect.md).

   **Externe aanbieding wijzigen:** Kies een externe aanbieding. Zie voor meer informatie [Externe aanbiedingen maken](/help/c-experiences/c-manage-content/about-remote-offers.md).

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

   **Aanbeveling toevoegen:**

   Voor een Recommendations-activiteit geeft de vervolgkeuzelijst Inhoud u de [!UICONTROL Add Recommendation] optie. Klikken **[!UICONTROL Add Recommendation]** Selecteer vervolgens het paginatype. Volg vervolgens de gebruikelijke stappen zoals gedefinieerd in de interface naar [een Recommendations-activiteit maken](/help/c-recommendations/t-create-recs-activity/create-recs-activity.md).

   Bij het selecteren van Recommendations-criteria in de Form-Based Experience Composer is er nu een directe koppeling naar de geselecteerde Criteria Card zodat u de criteria snel en eenvoudig kunt bewerken.

   ![](assets/change_criteria.png)

   Van de Doelpagina van het Doel driestappe geleide werkschema:

   ![](assets/change_criteria_2.png)

   **Beslissing voorstel toevoegen:**

   Een voorstel toevoegen dat is gemaakt in [!DNL Adobe Journey Optimizer] (AJO) naar een [!DNL Adobe Target] activiteit om de beste dynamische aanbieding en ervaring aan uw bezoekers op uw website of mobiele plaats te presenteren gebruikend offer decisioning. Deze optie is beschikbaar voor handmatige [!UICONTROL A/B Test] en [!UICONTROL Experience Targeting] (XT) alleen activiteiten.

   Zie voor meer informatie [Besluiten over aanbiedingen gebruiken](/help/c-integrating-target-with-mac/ajo/offer-decision.md).

1. (Optioneel, voor [!UICONTROL A/B Test], [!UICONTROL Automated Personalization], en [!UICONTROL Experience Targeting] (activiteiten) Om dit proces voor extra plaatsen te herhalen, klik **[!UICONTROL Add Location]** en configureert u de locatie en inhoud.
1. Klikken **[!UICONTROL Next]** Voer vervolgens de gebruikelijke stappen voor het maken van activiteiten uit voor het type activiteit.

* [Een A/B-test maken](/help/c-activities/t-test-ab/t-test-create-ab/test-create-ab.md)
* [Een ervaring maken die gericht is op activiteiten](/help/c-activities/t-experience-target/t-xt-create/xt-create.md#task_D6B3429AC31549E1A70EDF04B3DDC765)
* [Een Recommendations-activiteit maken](/help/c-recommendations/t-create-recs-activity/create-recs-activity.md#task_6874328773C64C44A73F0A130AD3F96F)

## Trainingsvideo: Op formulieren gebaseerde composer ![Zelfstudie-badge](/help/assets/tutorial.png)

Deze video bevat een demo van de op formulieren gebaseerde composer.

* Een activiteit maken met de Form-Based Experience Composer
* Begrijp wanneer om vorm-Gebaseerde Composer van de Ervaring tegenover Visual Experience Composer te gebruiken
* Verfijningen gebruiken om een locatie als doel in te stellen

>[!VIDEO](https://video.tv.adobe.com/v/17390)
