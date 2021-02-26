---
keywords: Automatisch doel maken;A/B-test;automatisch doelactiviteit;nieuwe a/b-activiteit;automatisch doel;automatisch doel voor persoonlijke ervaringen;gepersonaliseerd;optimalisatie
description: Leer hoe te om Visual Experience Composer (VEC) in Adobe Target te gebruiken om uw auto-Doel A/B activiteit van de Test direct op een Doel-Toegelaten pagina tot stand te brengen.
title: Hoe maak ik een automatisch doelgerichte activiteit?
feature: Automatisch doel
translation-type: tm+mt
source-git-commit: d57153a26ac0bc95004900dbcb006b867bc31d81
workflow-type: tm+mt
source-wordcount: '850'
ht-degree: 0%

---


# ![](/help/assets/premium.png) PREMIUMCcreate an Auto-Target activity

Gebruik [!UICONTROL Visual Experience Composer] (VEC) in [!DNL Adobe Target] om uw [!UICONTROL Auto-Target] [!UICONTROL A/B Test] activiteit direct op een [!DNL Target]-Toegelaten pagina te creëren en delen van de pagina binnen &lt;a5 te wijzigen/>.[!DNL Target]

>[!NOTE]
>
>[!UICONTROL Auto-Target] is beschikbaar als onderdeel van de  [!DNL Target Premium] oplossing. Deze functie is niet beschikbaar in [!DNL Target Standard] zonder een [!DNL Target Premium] licentie. Zie [Doelpremium](/help/c-intro/intro.md) voor meer informatie over de geavanceerde functies die deze licentie biedt.
>
>Naast de [!UICONTROL Auto-Target] [!UICONTROL A/B Test] activiteit (in dit artikel besproken), biedt [!DNL Target] twee extra typen [!UICONTROL A/B Test] activiteiten: [!UICONTROL Manual (Default)] en [!UICONTROL Auto-Allocate].
>
>Zie [Typen A/B-testactiviteiten](/help/c-activities/t-test-ab/test-ab.md#types) in *A/B-testoverzicht*.

Een [!UICONTROL Auto-Target]-activiteit maken:

1. Klik in de lijst **[!UICONTROL Activities]** op **[!UICONTROL Create Activity]** > **[!UICONTROL A/B Test]**.

   ![Vervolgkeuzelijst Activiteit maken](/help/c-activities/t-test-ab/t-test-create-ab/assets/ab_select-new.png)

   >[!NOTE]
   >
   >De beschikbare activiteitstypen zijn afhankelijk van uw [!DNL Target]-account. Sommige typen activiteiten worden mogelijk niet in de lijst weergegeven. [!UICONTROL Auto-Target] en [!UICONTROL Recommendations] zijn bijvoorbeeld [Premiumfuncties van doel](/help/c-intro/intro.md#premium).
   >
   >Zie [Activiteiten](/help/c-activities/activities.md) en de [Handleiding voor doelactiviteiten](/help/c-activities/target-activities-guide.md) voor informatie over de verschillende soorten activiteiten.

1. Selecteer **[!UICONTROL Visual (Default)]**, indien nodig.

   ![Testactiviteit A/B maken](/help/c-activities/t-test-ab/t-test-create-ab/assets/create-ab.png)

   Selecteer [!UICONTROL Form] als u de [!UICONTROL Form-Based Experience Composer] liever wilt gebruiken. Zie [Form-Based Experience Composer](/help/c-experiences/form-experience-composer.md) voor meer informatie.

   >[!NOTE]
   >
   >Naast VEC en [!UICONTROL Form-Based Experience Composer] biedt [!DNL Target] de Single Page Application VEC. Zie [Ervaringen en aanbiedingen](/help/c-experiences/experiences.md) voor meer informatie over de verschillende composers.
   >
   >Voor het oplossen van problemeninformatie over VEC, als u problemen hebt, zie [Problemen oplossen Composer van de Visuele Ervaring](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/troubleshoot-composer.md).
   >
   >De [[!UICONTROL Choose Workplace]](/help/administrating-target/c-user-management/property-channel/property-channel.md) optie in de voorafgaande illustratie is een [eigenschap van de Premium ](/help/c-intro/intro.md) van het Doel. Uw organisatie heeft een [!UICONTROL Target Standard] vergunning als u deze optie niet ziet.

1. Kies een [werkruimte](/help/administrating-target/c-user-management/property-channel/property-channel.md).

1. Geef uw [activiteit-URL](/help/c-activities/t-test-ab/t-test-create-ab/ab-activity-url.md) op en klik vervolgens op **[!UICONTROL Next]**.

   Als uw account is geconfigureerd met een standaard-URL, wordt die URL standaard weergegeven. U kunt de standaardinstelling wijzigen in een andere URL.

   De [!UICONTROL Visual Experience Composer] wordt geopend en geeft de pagina weer die in de URL is opgegeven.

   ![VEC](/help/c-activities/t-test-ab/t-test-create-ab/assets/vec-new.png)

1. Typ een naam voor de activiteit in de beschikbare ruimte.

   ![Naamveld](/help/c-activities/t-test-ab/t-test-create-ab/assets/ab_newname-new.png)

   De naam van de activiteit mag niet met een van de volgende tekens beginnen:

   | Teken | Beschrijving |
   |--- |--- |
   | `=` | Gelijk aan |
   | `+` | Plus |
   | `-` | Min |
   | `@` | Bij ondertekenen |

1. Maak nieuwe ervaringen door de elementen op de pagina te wijzigen.

   [!UICONTROL Visual Experience Composer] toont twee lusjes op de linkerkant nadat u een nieuwe activiteit creeert: Ervaring A en ervaring B. Ervaring A is de ervaring van de controle. De focus zal liggen op het tabblad Experience B, dat u naar wens kunt wijzigen. Ervaring B is de alternatieve ervaring die u aan de test kunt toevoegen. U kunt meerdere ervaringen toevoegen aan de test. U kunt ook Experience A verwijderen uit de activiteit als u geen standaard site-ervaring wilt opnemen als optie.

   Zie [Ervaring toevoegen](/help/c-activities/t-test-ab/t-test-create-ab/ab-add-experience.md) voor meer informatie over het toevoegen en wijzigen van ervaringen in [!UICONTROL Visual Experience Composer]. Om Ervaring B te wijzigen, begin met Stap 3.

1. Klik op **[!UICONTROL Targeting]** boven aan [!UICONTROL Visual Experience Composer] om naar de volgende stap in de driestappenworkflow met instructies te gaan.

   Het stroomdiagram wordt geopend.

   ![Doelstap A/B van de test](/help/c-activities/t-test-ab/t-test-create-ab/assets/ab_flow-new.png)

   Het stroomdiagram leidt u door de stappen om het publiek voor de activiteit te kiezen en opstellingservaringen.

1. Klik in het tekstvak [!UICONTROL Audience] op het bewerkingspictogram (drie verticale ellipsen), klik op **[!UICONTROL Replace Audience]** en [selecteer vervolgens het publiek](/help/c-activities/t-test-ab/t-test-create-ab/ab-audience.md) voor uw activiteit.

   Standaard is het publiek ingesteld op [!UICONTROL All Visitors].

1. Kies het percentage in aanmerking komende bezoekers dat u de activiteit wilt ingaan.

   ![Publiek percentage](/help/c-activities/t-test-ab/t-test-create-ab/assets/audperc-new.png)

   U kunt bijvoorbeeld items beperken tot 50% van alle bezoekers of 45% van uw &quot;Californische&quot; publiek.

1. Opstelling uw verkeerstoewijzing.

   U kunt meerdere ervaringen aan hetzelfde publiek tonen. Een diagram toont het geselecteerde publiek en de ervaringen u aan de activiteit hebt toegevoegd.

   Kies de gewenste methode voor verkeerstoewijzing. Als u een [!UICONTROL Auto-Target]-activiteit wilt maken, selecteert u **[!UICONTROL Auto-target for personalized experiences]**.

   De drie soorten verkeerstoewijzing worden hieronder beschreven:

   * **[!UICONTROL Manual (Default)]**: Geef het percentage voor alle ingangen op dat u wilt zien. U kunt de percentages gelijkmatig over alle ervaringen verdelen, of hogere of lagere percentages voor elke ervaring specificeren. Het totaal voor alle ervaringen moet 100% bedragen. Zie [Een A/B-test maken](/help/c-activities/t-test-ab/t-test-create-ab/test-create-ab.md) voor meer informatie.

   * **[!UICONTROL Auto-allocate to best experience]**: De meeste deelnemers aan de activiteit worden automatisch gericht op beter presterende ervaringen. Sommige bezoekers worden toegewezen aan alle ervaringen, om het verkennen van ervaringen te handhaven en veranderingen in prestatietrends te erkennen. Zie [Overzicht automatisch toewijzen](/help/c-activities/automated-traffic-allocation/automated-traffic-allocation.md) voor meer informatie.

   * **[!UICONTROL Auto-target for personalized experiences]**:  [!DNL Target] maakt gebruik van geavanceerd computerleren om inhoud en stationsomzettingen aan te passen door het identificeren van meervoudige, door de markt gedefinieerde ervaringen, en vervolgens de meest toegesneden ervaring aan bezoekers te bezorgen op basis van hun individuele klantprofielen en eerdere gedragingen van vergelijkbare bezoekers.
   U kunt ook op **[!UICONTROL Add]** klikken om een andere ervaring aan de activiteit toe te voegen.

1. Wanneer u met uw publiek, ervaringskeuzen, en de keuzen van de verkeerstoewijzing tevreden bent, klik **[!UICONTROL Next]** om naar de derde stap van de drie-stap geleide werkschema te bewegen.

1. Geef de [doelen en instellingen](/help/c-activities/t-test-ab/t-test-create-ab/ab-goals-and-settings.md) voor de activiteit op.

   ![A/B Activiteitsinstellingen](/help/c-activities/t-test-ab/t-test-create-ab/assets/ab_settings-new.png)

   >[!NOTE]
   >
   >Als u [Analytics voor Doel](/help/c-integrating-target-with-mac/a4t/a4t.md) (A4T) met deze activiteit wilt gebruiken, zie belangrijke informatie in [A4T steun voor auto-Wijs en auto-Doel activiteiten](/help/c-integrating-target-with-mac/a4t/a4t-at-aa.md).

1. Klik op **[!UICONTROL Save & Close]** of **[!UICONTROL Save]**.

Nadat u de activiteit creeert, toont het [!UICONTROL Overview] lusje informatie over de activiteit, met inbegrip van een diagram van uw activiteit.

## Trainingsvideo: A/B-tests maken (8:36) ![Zelfstudie-badge](/help/assets/tutorial.png)

In deze video ziet u hoe u een A/B-test maakt met behulp van de driestapige workflow met instructies.[!DNL Target]

* Een [!UICONTROL A/B Test]-activiteit maken in [!DNL Adobe Target]
* Verkeer toewijzen met een handmatige splitsing of automatische verkeerstoewijzing

>[!VIDEO](https://video.tv.adobe.com/v/17391)