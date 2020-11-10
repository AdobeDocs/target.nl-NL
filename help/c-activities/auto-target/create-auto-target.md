---
keywords: Create auto-target;A/B test;auto-target activity;new a/b activity;auto target;auto-target for personalized experiences;personalized
description: Gebruik Composer van de Visuele Ervaring in Adobe Target om uw auto-Wijs A/B activiteit van de Test direct op een Doel-Toegelaten pagina tot stand te brengen en gedeelten van de pagina binnen Doel te wijzigen.
title: Een automatisch doelactiviteit maken
feature: ab
translation-type: tm+mt
source-git-commit: 968d36d65016e51290f6bf754f69c91fd8f68405
workflow-type: tm+mt
source-wordcount: '784'
ht-degree: 0%

---


# ![PREMIUM](/help/assets/premium.png) Een automatisch doelactiviteit maken

Gebruik de [!UICONTROL Visual Experience Composer] (VEC) in [!DNL Adobe Target] om uw [!UICONTROL Auto-Target] activiteit direct op een [!UICONTROL A/B Test] toegelaten pagina tot stand te brengen en gedeelten van de pagina binnen te wijzigen [!DNL Target][!DNL Target].

>[!NOTE]
>
>Naast de [!UICONTROL Auto-Target] activiteit (die in dit artikel wordt besproken), [!UICONTROL A/B Test] verstrekt twee extra soorten [!DNL Target] [!UICONTROL A/B Test] activiteiten: [!UICONTROL Manual (Default)] en [!UICONTROL Auto-Allocate].
>
>Zie [Typen testactiviteiten](/help/c-activities/t-test-ab/test-ab.md#types) voor A/B in *A/B-testoverzicht*.

Een [!UICONTROL Auto-Target] activiteit maken:

1. From the **[!UICONTROL Activities]** list, click **[!UICONTROL Create Activity]** > **[!UICONTROL A/B Test]**.

   ![Vervolgkeuzelijst Activiteit maken](/help/c-activities/t-test-ab/t-test-create-ab/assets/ab_select-new.png)

   >[!NOTE]
   >
   >Welke soorten activiteiten beschikbaar zijn, is afhankelijk van uw [!DNL Target] account. Sommige typen activiteiten worden mogelijk niet in de lijst weergegeven. Dit zijn bijvoorbeeld [!UICONTROL Auto-Target] en [!UICONTROL Recommendations] zijn [Target Premium-functies](/help/c-intro/intro.md#premium).
   >
   >Voor informatie over de diverse soorten activiteiten, zie [Activiteiten](/help/c-activities/activities.md) en de [Doelgids](/help/c-activities/target-activities-guide.md).

1. Selecteer **[!UICONTROL Visual (Default)]** indien nodig.

   ![Testactiviteit A/B maken](/help/c-activities/t-test-ab/t-test-create-ab/assets/create-ab.png)

   Selecteer [!UICONTROL Form-Based Experience Composer]de optie [!UICONTROL Form]. Zie [Form-Based Experience Composer](/help/c-experiences/form-experience-composer.md) voor meer informatie.

   >[!NOTE]
   >
   >Naast de VEC en [!UICONTROL Form-Based Experience Composer], [!DNL Target] biedt toepassing VEC voor één pagina aan. Zie [Ervaringen en Aanbiedingen](/help/c-experiences/experiences.md)voor meer informatie over de verschillende composers.
   >
   >Voor het oplossen van problemeninformatie over VEC, als u problemen hebt, zie het Oplossen van [problemen de Visuele Composer](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/troubleshoot-composer.md)van de Ervaring.
   >
   >De [[!UICONTROL Choose Workplace]](/help/administrating-target/c-user-management/property-channel/property-channel.md) optie in de voorgaande illustratie is een [doelpremiumfunctie](/help/c-intro/intro.md) . Uw organisatie heeft een [!UICONTROL Target Standard] licentie als deze optie niet wordt weergegeven.

1. Kies een [werkruimte](/help/administrating-target/c-user-management/property-channel/property-channel.md).

1. Geef de URL [van uw](/help/c-activities/t-test-ab/t-test-create-ab/ab-activity-url.md)activiteit op en klik op **[!UICONTROL Next]**.

   Als uw account is geconfigureerd met een standaard-URL, wordt die URL standaard weergegeven. U kunt de standaardinstelling wijzigen in een andere URL.

   Het [!UICONTROL Visual Experience Composer] dialoogvenster wordt geopend en geeft de pagina weer die in de URL is opgegeven.

   ![VEC](/help/c-activities/t-test-ab/t-test-create-ab/assets/vec-new.png)

1. Typ een naam voor de activiteit in de beschikbare ruimte.

   ![Naamveld](/help/c-activities/t-test-ab/t-test-create-ab/assets/ab_newname-new.png)

   De volgende tekens zijn niet toegestaan in een naam van een activiteit:

   | Teken | Beschrijving |
   |--- |--- |
   | `/` | slash |
   | `?` | Vraagteken |
   | `#` | Nummerteken |
   | `:` | Colon |
   | `=` | Gelijk aan |
   | `+` | Plus |
   | `-` | Min |
   | `@` | Bij ondertekenen |

1. Maak nieuwe ervaringen door de elementen op de pagina te wijzigen.

   Nadat u een nieuwe activiteit hebt gemaakt, worden er twee tabbladen aan de linkerkant weergegeven: [!UICONTROL Visual Experience Composer] Ervaring A en ervaring B. Ervaring A is de ervaring van de controle. De focus zal liggen op het tabblad Experience B, dat u naar wens kunt wijzigen. Ervaring B is de alternatieve ervaring die u aan de test kunt toevoegen. U kunt meerdere ervaringen toevoegen aan de test. U kunt ook Experience A verwijderen uit de activiteit als u geen standaard site-ervaring wilt opnemen als optie.

   Voor meer informatie over het toevoegen van en het wijzigen van ervaringen in [!UICONTROL Visual Experience Composer], zie [Voeg Ervaring](/help/c-activities/t-test-ab/t-test-create-ab/ab-add-experience.md)toe. Om Ervaring B te wijzigen, begin met Stap 3.

1. Klik **[!UICONTROL Targeting]** bij de bovenkant van [!UICONTROL Visual Experience Composer] om naar de volgende stap in de driestapige geleide workflow te gaan.

   Het stroomdiagram wordt geopend.

   ![Doelstap A/B van de test](/help/c-activities/t-test-ab/t-test-create-ab/assets/ab_flow-new.png)

   Het stroomdiagram leidt u door de stappen om het publiek voor de activiteit te kiezen en opstellingservaringen.

1. Klik in het [!UICONTROL Audience] vak op het bewerkingspictogram (drie verticale ellipsen), klik **[!UICONTROL Replace Audience]** en [selecteer vervolgens het publiek](/help/c-activities/t-test-ab/t-test-create-ab/ab-audience.md) voor uw activiteit.

   Standaard is het publiek ingesteld op [!UICONTROL All Visitors].

1. Kies het percentage in aanmerking komende bezoekers dat u de activiteit wilt ingaan.

   ![Publiek percentage](/help/c-activities/t-test-ab/t-test-create-ab/assets/audperc-new.png)

   U kunt bijvoorbeeld items beperken tot 50% van alle bezoekers of 45% van uw &quot;Californische&quot; publiek.

1. Opstelling uw verkeerstoewijzing.

   U kunt meerdere ervaringen aan hetzelfde publiek tonen. Een diagram toont het geselecteerde publiek en de ervaringen u aan de activiteit hebt toegevoegd.

   Kies de gewenste methode voor verkeerstoewijzing. Selecteer een [!UICONTROL Auto-Target] activiteit om deze te maken **[!UICONTROL Auto-target for personalized experiences]**.

   De drie soorten verkeerstoewijzing worden hieronder beschreven:

   * **[!UICONTROL Manual (Default)]**: Geef het percentage voor alle ingangen op dat u wilt zien. U kunt de percentages gelijkmatig over alle ervaringen verdelen, of hogere of lagere percentages voor elke ervaring specificeren. Het totaal voor alle ervaringen moet 100% bedragen. Zie [Een A/B-test](/help/c-activities/t-test-ab/t-test-create-ab/test-create-ab.md)maken voor meer informatie.

   * **[!UICONTROL Auto-allocate to best experience]**: De meeste deelnemers aan de activiteit worden automatisch gericht op beter presterende ervaringen. Sommige bezoekers worden toegewezen aan alle ervaringen, om het verkennen van ervaringen te handhaven en veranderingen in prestatietrends te erkennen. Zie Overzicht [](/help/c-activities/automated-traffic-allocation/automated-traffic-allocation.md)automatisch toewijzen voor meer informatie.

   * **[!UICONTROL Auto-target for personalized experiences]**: [!DNL Target] maakt gebruik van geavanceerd computerleren om inhoud en stationsomzettingen aan te passen door het identificeren van meervoudige, door de markt gedefinieerde ervaringen, en vervolgens de meest toegesneden ervaring aan bezoekers te bezorgen op basis van hun individuele klantprofielen en eerdere gedragingen van vergelijkbare bezoekers.
   U kunt ook klikken **[!UICONTROL Add]** om een andere ervaring aan de activiteit toe te voegen.

1. Als u tevreden bent met uw publiek, ervaringsopties en opties voor verkeerstoewijzing, klikt u **[!UICONTROL Next]** om naar de derde stap van de driestappenworkflow met instructies te gaan.

1. Geef de [doelen en instellingen](/help/c-activities/t-test-ab/t-test-create-ab/ab-goals-and-settings.md) voor de activiteit op.

   ![A/B Activiteitsinstellingen](/help/c-activities/t-test-ab/t-test-create-ab/assets/ab_settings-new.png)

1. Klik **[!UICONTROL Save & Close]** of **[!UICONTROL Save]**.

Nadat u de activiteit creeert, toont het [!UICONTROL Overview] lusje informatie over de activiteit, met inbegrip van een diagram van uw activiteit.

## Trainingsvideo: Een ![zelfstudie-badge voor A/B-tests maken (8:36)](/help/assets/tutorial.png)

In deze video ziet u hoe u een A/B-test maakt met behulp van de workflow met [!DNL Target] drie stappen.

* Een [!UICONTROL A/B Test] activiteit maken in [!DNL Adobe Target]
* Verkeer toewijzen met een handmatige splitsing of automatische verkeerstoewijzing

>[!VIDEO](https://video.tv.adobe.com/v/17391)