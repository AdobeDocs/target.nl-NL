---
keywords: automatisch toewijzen maken;A/B-test;automatisch toewijzen van activiteit;nieuwe a/b-activiteit;automatisch toewijzen;automatisch toewijzen aan beste ervaring;toewijzen;automatisch toewijzen
description: Leer hoe u de [!UICONTROL Visual Experience Composer] (VEC) in [!DNL Adobe Target] om een [!UICONTROL Auto-Allocate] A/B Testactiviteit.
title: Hoe maak ik een [!UICONTROL Auto-Allocate] Activiteit?
feature: Auto-Allocate
exl-id: 30bc95e0-4f5e-4d1f-bad2-7b20b8f3c7d2
source-git-commit: 3e8c2d77f300bf0e2ca83a53d30e7b9eee48894e
workflow-type: tm+mt
source-wordcount: '787'
ht-degree: 0%

---

# Een [!UICONTROL Auto-Allocate] activiteit

Gebruik de [!UICONTROL Visual Experience Composer] (VEC) in [!DNL Adobe Target] om uw [!UICONTROL Auto-Allocate] [!UICONTROL A/B Test] rechtstreeks op een [!DNL Target]-enabled pagina en om gedeelten van de pagina binnen te wijzigen [!DNL Target].

Naast de [!UICONTROL Auto-Allocate] [!UICONTROL A/B Test] activiteit (in dit artikel besproken), [!DNL Target] verstrekt twee extra types van [!UICONTROL A/B Test] activiteiten: [!UICONTROL Manual (Default)] en [!UICONTROL Auto-Target]. Zie [Typen A/B-testactiviteiten](/help/main/c-activities/t-test-ab/test-ab.md#types) in *A/B-testoverzicht*.

Om een [!UICONTROL Auto-Allocate] activiteit:

1. Van de **[!UICONTROL Activities]** lijst, klik **[!UICONTROL Create Activity]** > **[!UICONTROL A/B Test]**.

   ![Vervolgkeuzelijst Activiteit maken](/help/main/c-activities/t-test-ab/t-test-create-ab/assets/ab_select-new.png)

   De beschikbare activiteitstypen zijn afhankelijk van uw [!DNL Target] account. Sommige typen activiteiten worden mogelijk niet in de lijst weergegeven. Bijvoorbeeld: [!UICONTROL Recommendations] is een [Functie Doelpremium](/help/main/c-intro/intro.md#premium). Voor informatie over de diverse activiteitstypen raadpleegt u [Activiteiten](/help/main/c-activities/activities.md) en de [Doelgids voor activiteiten](/help/main/c-activities/target-activities-guide.md).

1. In de **[!UICONTROL Create A/B Test Activity]** dialoogvenster selecteert u **[!UICONTROL Visual]**, indien nodig.

   Als u liever het [!UICONTROL Form-Based Experience Composer], selecteert u [!UICONTROL Form]. Zie [Formuliergebaseerde Experience Composer](/help/main/c-experiences/form-experience-composer.md) voor meer informatie .

   >[!NOTE]
   >
   >Naast de VEC en [!UICONTROL Form-Based Experience Composer], [!DNL Target] biedt de Single Page Application VEC aan. Zie voor meer informatie over de verschillende composers [Ervaringen en aanbiedingen](/help/main/c-experiences/experiences.md).
   >
   >Voor het oplossen van problemeninformatie over VEC, als u problemen hebt, zie [Problemen oplossen met de composer voor visuele ervaring](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/troubleshoot-composer.md).

1. (Voorwaardelijk) Als u een [De klant van de Premium van het doel](/help/main/c-intro/intro.md#premium), kiest u een [werkruimte](/help/main/administrating-target/c-user-management/property-channel/property-channel.md).

1. Geef uw [activiteit-URL](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-activity-url.md)en klik vervolgens op **[!UICONTROL Create]**.

   Als uw account is geconfigureerd met een standaard-URL, wordt die URL standaard weergegeven. U kunt desgewenst van de standaard naar een andere URL overschakelen.

   De [!UICONTROL Visual Experience Composer] wordt geopend en wordt de pagina weergegeven die in de URL is opgegeven.

   ![VEC](/help/main/c-activities/t-test-ab/t-test-create-ab/assets/vec-new.png)

1. Typ een naam voor de activiteit in de beschikbare ruimte.

   ![Naamveld](/help/main/c-activities/t-test-ab/t-test-create-ab/assets/ab_newname-new.png)

   De naam van de activiteit mag niet met een van de volgende tekens beginnen:

   | Teken | Beschrijving |
   |--- |--- |
   | `=` | Gelijk aan |
   | `+` | Plus |
   | `-` | Min |
   | `@` | Bij ondertekenen |

1. Maak ervaringen door de elementen op de pagina te wijzigen.

   De [!UICONTROL Visual Experience Composer] Hiermee geeft u twee tabbladen aan de linkerkant weer nadat u een nieuwe activiteit hebt gemaakt: Experience A en Experience B. Experience A is the control experience. De focus ligt op het tabblad Experience B, dat u naar wens kunt wijzigen. Ervaring B is de alternatieve ervaring die u aan de test kunt toevoegen. U kunt meerdere ervaringen toevoegen aan de test. U kunt ook Experience A verwijderen uit de activiteit als u geen standaard site-ervaring wilt opnemen als optie.

   Voor meer informatie over het toevoegen van en het wijzigen van ervaringen in [!UICONTROL Visual Experience Composer], zie [Ervaring toevoegen](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-add-experience.md). Om Ervaring B te wijzigen, begin met Stap 2.

1. Klikken **[!UICONTROL Targeting]** boven aan het dialoogvenster [!UICONTROL Visual Experience Composer] om naar de volgende stap in de driestappenworkflow met instructies te gaan.

   Het stroomdiagram wordt geopend.

   ![Teststap A/B](/help/main/c-activities/t-test-ab/t-test-create-ab/assets/ab_flow-new.png)

   Het stroomdiagram leidt u door de stappen om het publiek voor de activiteit te kiezen en opstellingservaringen.

1. In de [!UICONTROL Audience] , klikt u op het pictogram Bewerken (de verticale ellips) en klikt u op **[!UICONTROL Replace Audience]** vervolgens [het publiek selecteren](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-audience.md) voor je activiteit.

   Standaard is de doelgroep ingesteld op [!UICONTROL All Visitors].

1. Kies het percentage in aanmerking komende bezoekers dat u de activiteit wilt ingaan.

   ![Publiek percentage](/help/main/c-activities/t-test-ab/t-test-create-ab/assets/audperc-new.png)

   U kunt bijvoorbeeld items beperken tot 50% van alle bezoekers of 45% van uw &quot;Californische&quot; publiek.

1. Opstelling uw methode van de verkeerstoewijzing.

   U kunt meerdere ervaringen aan hetzelfde publiek tonen. Een diagram toont het geselecteerde publiek en de ervaringen die u aan de activiteit hebt toegevoegd.

   Kies de gewenste methode voor verkeerstoewijzing. Om een [!UICONTROL Auto-Allocate] activiteit, selecteren **[!UICONTROL Auto-Allocate to best experience]**.

   De drie soorten verkeerstoewijzing worden hieronder beschreven:

   * **[!UICONTROL Manual (Default)]**: Geef het percentage van de gegadigden op dat u voor elke ervaring wilt zien. U kunt de percentages gelijkmatig over alle ervaringen verdelen, of hogere of lagere percentages voor elke ervaring specificeren. Het totaal voor alle ervaringen moet 100% bedragen. Zie voor meer informatie [Een A/B-test maken](/help/main/c-activities/t-test-ab/t-test-create-ab/test-create-ab.md).

   * **[!UICONTROL Auto-allocate to best experience]**: De meeste deelnemers aan de activiteit worden automatisch gericht op beter presterende ervaringen. Sommige bezoekers worden toegewezen aan alle ervaringen, om het verkennen van ervaringen te handhaven en veranderingen in prestatietrends te erkennen.

   * **[!UICONTROL Auto-target for personalized experiences]**: [!DNL Target] maakt gebruik van geavanceerd computerleren om inhoud en stationsomzettingen aan te passen door het identificeren van meervoudige, door de markt gedefinieerde ervaringen, en vervolgens de meest toegesneden ervaring aan bezoekers te bezorgen op basis van hun individuele klantprofielen en eerdere gedragingen van vergelijkbare bezoekers. Zie voor meer informatie [Automatisch doel](/help/main/c-activities/auto-target/auto-target-to-optimize.md).

   U kunt ook op **[!UICONTROL Add]** om een andere ervaring aan de activiteit toe te voegen.

1. Wanneer u met uw publiek, ervaringskeuzen, en de keuzen van de verkeerstoewijzing tevreden bent, klik **[!UICONTROL Next]** om naar de derde stap van de driestappenworkflow met instructies te gaan.

1. Geef de [doelstellingen en instellingen](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-goals-and-settings.md) voor de activiteit.

   >[!NOTE]
   >
   >Als u wilt gebruiken [Analyses voor doel](/help/main/c-integrating-target-with-mac/a4t/a4t.md) (A4T) met deze activiteit. [A4T-ondersteuning voor activiteiten voor automatisch toewijzen en automatisch richten](/help/main/c-integrating-target-with-mac/a4t/a4t-at-aa.md).

1. Klikken **[!UICONTROL Save & Close]** of **[!UICONTROL Save]**.

Nadat u de activiteit creeert, [!UICONTROL Overview] op het tabblad vindt u informatie over de activiteit, inclusief een diagram met uw activiteit.

## Trainingsvideo: A/B-tests maken (8:36)

In deze video ziet u hoe u een A/B-test maakt met de opdracht [!DNL Target] driestapsgerichte workflow.

* Een [!UICONTROL A/B Test] activiteit in [!DNL Adobe Target]
* Verkeer toewijzen met een handmatige splitsing of automatische verkeerstoewijzing

>[!VIDEO](https://video.tv.adobe.com/v/17391)
