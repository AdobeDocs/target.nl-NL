---
keywords: Automatisch doel maken;A/B-test;automatisch doelactiviteit;nieuwe a/b-activiteit;automatisch doel;automatisch doel voor persoonlijke ervaringen;gepersonaliseerd;optimalisatie
description: Leer hoe te om [!UICONTROL Visual Experience Composer] (VEC) in  [!DNL Adobe Target]  te gebruiken om een [!UICONTROL Auto-Target] activiteit van de Test van A/B tot stand te brengen.
title: Hoe maak ik een [!UICONTROL Auto-Target] -activiteit?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=nl-NL#premium newtab=true" tooltip="Kijk wat er in Target Premium is opgenomen."
feature: Auto-Target
exl-id: 5521740c-eee2-4ba2-8931-cf56d56a4561
source-git-commit: 32a91a41cd182d3a55ded7dea8c1c6ea6f46aa71
workflow-type: tm+mt
source-wordcount: '795'
ht-degree: 0%

---

# Een [!UICONTROL Auto-Target] activiteit maken

Gebruik [!UICONTROL Visual Experience Composer] (VEC) in [!DNL Adobe Target] om uw [!UICONTROL Auto-Target] [!UICONTROL A/B Test] -activiteit rechtstreeks op een pagina met [!DNL Target] functies te maken en om delen van de pagina binnen [!DNL Target] te wijzigen.

>[!NOTE]
>
>[!UICONTROL Auto-Target] is beschikbaar als onderdeel van de [!DNL Target Premium] -oplossing. Deze functie is niet beschikbaar in [!DNL Target Standard] zonder een [!DNL Target Premium] -licentie. Voor meer informatie over de geavanceerde eigenschappen verstrekt deze vergunning, zie [ Target Premium ](/help/main/c-intro/intro.md).

Een [!UICONTROL Auto-Target] -activiteit maken:

1. Klik in de lijst **[!UICONTROL Activities]** op **[!UICONTROL Create Activity]** > **[!UICONTROL A/B Test]** .

   ![ creeer de drop-down lijst van de Activiteit ](/help/main/c-activities/t-test-ab/t-test-create-ab/assets/ab_select-new.png)

   De beschikbare activiteitstypen zijn afhankelijk van uw [!DNL Target] -account. Sommige typen activiteiten worden mogelijk niet in de lijst weergegeven. Bijvoorbeeld, [!UICONTROL Recommendations] is de eigenschap van a [ Target Premium ](/help/main/c-intro/intro.md#premium). Voor informatie over de diverse activiteitentypes, zie [ Activiteiten ](/help/main/c-activities/activities.md) en de [ gids van de Activiteiten van het Doel ](/help/main/c-activities/target-activities-guide.md).

1. Selecteer **[!UICONTROL Visual]**, indien nodig.

   Selecteer [!UICONTROL Form] als u de [!UICONTROL Form-Based Experience Composer] -toets liever wilt gebruiken. Zie [ vorm-Gebaseerde Composer van de Ervaring ](/help/main/c-experiences/form-experience-composer.md) voor meer informatie.

   >[!NOTE]
   >
   >Naast de VEC en [!UICONTROL Form-Based Experience Composer] biedt [!DNL Target] de toepassing VEC voor één pagina. Voor meer informatie over de diverse composers, zie [ Ervaringen en Aanbiedingen ](/help/main/c-experiences/experiences.md).
   >
   >Voor het oplossen van problemeninformatie over VEC, als u problemen hebt, zie [ het Oplossen van problemen de Visuele Composer van de Ervaring ](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/troubleshoot-composer.md).

1. (Voorwaardelijk) als u de klant van a [ Target Premium ](/help/main/c-intro/intro.md#premium) bent, kies a [ werkruimte ](/help/main/administrating-target/c-user-management/property-channel/property-channel.md).

1. Specificeer uw [ activiteit URL ](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-activity-url.md), dan klik **[!UICONTROL Next]**.

   Als uw account is geconfigureerd met een standaard-URL, wordt die URL standaard weergegeven. U kunt de standaardinstelling wijzigen in een andere URL.

   De [!UICONTROL Visual Experience Composer] wordt geopend en geeft de pagina weer die in de URL is opgegeven.

   ![ VEC ](/help/main/c-activities/t-test-ab/t-test-create-ab/assets/vec-new.png)

1. Typ een naam voor de activiteit in de beschikbare ruimte.

   ![ het gebied van de Naam ](/help/main/c-activities/t-test-ab/t-test-create-ab/assets/ab_newname-new.png)

   De naam van de activiteit mag niet met een van de volgende tekens beginnen:

   | Teken | Beschrijving |
   |--- |--- |
   | `=` | Gelijk aan |
   | `+` | Plus |
   | `-` | Min |
   | `@` | Bij ondertekenen |

1. Maak ervaringen door de elementen op de pagina te wijzigen.

   In [!UICONTROL Visual Experience Composer] worden twee tabbladen aan de linkerkant weergegeven nadat u een activiteit hebt gemaakt: Experience A en Experience B. Experience A is de besturingservaring. De focus ligt op het tabblad Experience B, dat u naar wens kunt wijzigen. Ervaring B is de alternatieve ervaring die u aan uw test kunt toevoegen. U kunt meerdere ervaringen toevoegen aan de test. U kunt ook Experience A verwijderen uit de activiteit als u geen standaard site-ervaring wilt opnemen als optie.

   Voor meer informatie over het toevoegen van en het wijzigen van ervaringen in [!UICONTROL Visual Experience Composer], zie [ Ervaring ](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-add-experience.md) toevoegen. Om Ervaring B te wijzigen, begin met Stap 2.

1. Klik op **[!UICONTROL Targeting]** boven aan [!UICONTROL Visual Experience Composer] om naar de volgende stap in de driestappenworkflow met instructies te gaan.

   Het stroomdiagram wordt geopend.

   ![ A/B de Test richtend stap ](/help/main/c-activities/t-test-ab/t-test-create-ab/assets/ab_flow-new.png)

   Het stroomdiagram leidt u door de stappen om het publiek voor de activiteit te kiezen en opstellingservaringen.

1. In het [!UICONTROL Audience] vakje, klik uitgeven pictogram (de verticale ellips), klik **[!UICONTROL Replace Audience]**, dan [ selecteer het publiek ](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-audience.md) voor uw activiteit.

   Standaard is het publiek ingesteld op [!UICONTROL All Visitors] .

1. Kies het percentage in aanmerking komende bezoekers dat u de activiteit wilt ingaan.

   ![ percentage van het publiek ](/help/main/c-activities/t-test-ab/t-test-create-ab/assets/audperc-new.png)

   U kunt bijvoorbeeld items beperken tot 50% van alle bezoekers of 45% van uw &quot;Californische&quot; publiek.

1. Opstelling uw verkeerstoewijzing.

   U kunt meerdere ervaringen aan hetzelfde publiek tonen. Een diagram toont het geselecteerde publiek en de ervaringen die u aan de activiteit hebt toegevoegd.

   Kies de gewenste methode voor verkeerstoewijzing. Selecteer **[!UICONTROL Auto-Target for personalized experiences]** om een [!UICONTROL Auto-Target] -activiteit te maken.

   De drie soorten verkeerstoewijzing worden hieronder beschreven:

   * **[!UICONTROL Manual (Default)]**: geef het percentage van de gegadigden op dat u elke ervaring wilt zien. U kunt de percentages gelijkmatig over alle ervaringen verdelen, of hogere of lagere percentages voor elke ervaring specificeren. Het totaal voor alle ervaringen moet 100% bedragen. Voor meer informatie, zie [ een Test van A/B ](/help/main/c-activities/t-test-ab/t-test-create-ab/test-create-ab.md) creëren.

   * **[!UICONTROL Auto-Allocate to best experience]**: De meeste deelnemers aan de activiteit worden automatisch omgeleid naar beter presterende ervaringen. Sommige bezoekers worden toegewezen aan alle ervaringen, om het verkennen van ervaringen te handhaven en veranderingen in prestatietrends te erkennen. Voor meer informatie, zie [ auto-Wijs overzicht ](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md) toe.

   * **[!UICONTROL Auto-Target for personalized experiences]**: [!DNL Target] maakt gebruik van geavanceerd leren van computers om inhoud en stationsomzettingen aan te passen door het identificeren van meerdere hoogwaardige, door markters gedefinieerde ervaringen en vervolgens de meest op maat gemaakte ervaring aan bezoekers te bieden op basis van hun individuele klantprofielen en eerdere gedragingen van vergelijkbare bezoekers.

   U kunt ook op **[!UICONTROL Add]** klikken om een andere ervaring aan de activiteit toe te voegen.

1. Als u tevreden bent met het publiek, de ervaringsopties en de keuzes voor verkeerstoewijzing, klikt u op **[!UICONTROL Next]** om naar de derde stap van de driestappenworkflow met instructies te gaan.

1. Specificeer de [ doelstellingen en de montages ](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-goals-and-settings.md) voor de activiteit.

   >[!NOTE]
   >
   >Als u [ Analytics voor Doel ](/help/main/c-integrating-target-with-mac/a4t/a4t.md) (A4T) met deze activiteit wilt gebruiken, zie belangrijke informatie in [ steun A4T voor auto-Wijs en auto-Doel activiteiten ](/help/main/c-integrating-target-with-mac/a4t/a4t-at-aa.md).

1. Klik op **[!UICONTROL Save & Close]** of **[!UICONTROL Save]** .

Nadat u de activiteit creeert, toont het [!UICONTROL Overview] lusje informatie over de activiteit, met inbegrip van een diagram van uw activiteit.

## Trainingsvideo: A/B-tests maken (8:36)

In deze video ziet u hoe u een A/B-test maakt met behulp van de [!DNL Target] driestapige geleide workflow.

* Een [!UICONTROL A/B Test] activiteit maken in [!DNL Adobe Target]
* Verkeer toewijzen met een handmatige splitsing of automatische verkeerstoewijzing

>[!VIDEO](https://video.tv.adobe.com/v/17391)
