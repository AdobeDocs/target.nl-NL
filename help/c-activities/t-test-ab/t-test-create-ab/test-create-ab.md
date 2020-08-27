---
keywords: Create A/B;A/B test;A/B activity;new a/b activity
description: Gebruik de Visuele Composer van de Ervaring in Doel om uw test direct op een doel-Toegelaten pagina tot stand te brengen en gedeelten van de pagina binnen Doel te wijzigen.
title: Een A/B-test maken
feature: ab
topic: Advanced,Standard,Classic
uuid: 2a255cf9-91c7-4710-bfd7-a4d8797ef24c
translation-type: tm+mt
source-git-commit: d5a48db0c954871269714ef32d0545ed4898660f
workflow-type: tm+mt
source-wordcount: '737'
ht-degree: 0%

---


# Een A/B-test maken{#create-an-a-b-test}

Gebruik de Visuele Composer van de Ervaring in Doel om uw test direct op een doel-Toegelaten pagina tot stand te brengen en gedeelten van de pagina binnen Doel te wijzigen.

1. From the [!UICONTROL Activities] list, click **[!UICONTROL Create Activity]** > **[!UICONTROL A/B Test]**.

   ![Vervolgkeuzelijst Activiteit maken](/help/c-activities/t-test-ab/t-test-create-ab/assets/ab_select-new.png)

   >[!NOTE]
   >
   >Welke soorten activiteiten beschikbaar zijn, is afhankelijk van uw [!DNL Target] account. Sommige typen activiteiten worden mogelijk niet in de lijst weergegeven. Bijvoorbeeld, [!UICONTROL Recommendations] is een eigenschap [van de Premie van het](/help/c-intro/intro.md#premium)Doel.
   >
   >Voor informatie over de diverse soorten activiteiten, zie [Activiteiten](../../../c-activities/activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03) en de [Doelgids](/help/c-activities/target-activities-guide.md).

   ![A/B-testactiviteit maken](/help/c-activities/t-test-ab/t-test-create-ab/assets/create-ab.png)

1. Selecteer **[!UICONTROL Visual (Default)]** indien nodig.

   Selecteer [!UICONTROL Form]Formulier-based Experience Composer als u liever wilt gebruiken. Zie [Form-Based Experience Composer](/help/c-experiences/form-experience-composer.md) voor meer informatie.

   >[!NOTE]
   >
   >Naast de VEC en Form-Based Experience Composer, biedt Target de Single Page Application VEC en de VEC voor Mobile Apps. Zie [Ervaringen en Aanbiedingen](/help/c-experiences/experiences.md)voor meer informatie over de verschillende composers.
   >
   >Voor het oplossen van problemeninformatie over VEC, als u problemen hebt, zie het Oplossen van [problemen de Visuele Composer](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/troubleshoot-composer.md)van de Ervaring.
   >
   >De [!UICONTROL [Choose Workplace]](/help/administrating-target/c-user-management/property-channel/property-channel.md) optie in de voorgaande illustratie is een [doelpremiumfunctie](/help/c-intro/intro.md) . Uw organisatie heeft een licentie voor Target Standard als deze optie niet wordt weergegeven.

1. (Voorwaardelijk) Als u een klant [van de Premium van het](/help/c-intro/intro.md#premium)Doel bent, kies een [werkruimte](/help/administrating-target/c-user-management/property-channel/property-channel.md).

1. Geef de URL [van uw](../../../c-activities/t-test-ab/t-test-create-ab/ab-activity-url.md#concept_D28549AAA0A14E3BB5F05F32BE8ABC90)activiteit op en klik op **[!UICONTROL Next]**.

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

   Voor meer informatie over het toevoegen van en het wijzigen van ervaringen in [!UICONTROL Visual Experience Composer], zie [Voeg Ervaring](../../../c-activities/t-test-ab/t-test-create-ab/ab-add-experience.md#task_454646F2895242D3B92DC395A0CE1A00)toe. Om Ervaring B te wijzigen, begin met Stap 3.

1. Klik **[!UICONTROL Targeting]** bij de bovenkant van [!UICONTROL Visual Experience Composer] om naar de volgende stap in de driestapige geleide workflow te gaan.

   Het stroomdiagram wordt geopend.

   ![Doelstap A/B van de test](/help/c-activities/t-test-ab/t-test-create-ab/assets/ab_flow-new.png)

   Het stroomdiagram leidt u door de stappen om het publiek voor de activiteit te kiezen en opstellingservaringen.
1. Klik in het [!UICONTROL Audience] vak op het bewerkingspictogram en [selecteer het publiek](../../../c-activities/t-test-ab/t-test-create-ab/ab-audience.md#concept_A268236C1224451DB7844BF67F41A087) voor uw activiteit.

   Standaard wordt het publiek ingesteld op Alle bezoekers.

1. Kies het percentage in aanmerking komende bezoekers dat u de activiteit wilt ingaan.

   ![Publiek percentage](/help/c-activities/t-test-ab/t-test-create-ab/assets/audperc-new.png)

   U kunt bijvoorbeeld items beperken tot 50% van alle bezoekers of 45% van uw &quot;Californische&quot; publiek.

1. Opstelling uw verkeerstoewijzing.

   U kunt meerdere ervaringen aan hetzelfde publiek tonen. Een diagram toont het geselecteerde publiek en de ervaringen u aan de activiteit hebt toegevoegd.

   Kies uw gewenste methode voor verkeerstoewijzing:

   * **[!UICONTROL Manual (Default)]**: Geef het percentage voor alle ingangen op dat u wilt zien. U kunt de percentages gelijkmatig over alle ervaringen verdelen, of hogere of lagere percentages voor elke ervaring specificeren. Het totaal voor alle ervaringen moet 100% bedragen.

   * **[!UICONTROL Auto-allocate to best experience]**: De meeste deelnemers aan de activiteit worden automatisch gericht op beter presterende ervaringen. Sommige bezoekers worden toegewezen aan alle ervaringen, om het verkennen van ervaringen te handhaven en veranderingen in prestatietrends te erkennen. Zie [Geautomatiseerde verkeerstoewijzing](../../../c-activities/automated-traffic-allocation/automated-traffic-allocation.md#concept_A1407678796B4C569E94CBA8A9F7F5D4).

   * **[!UICONTROL Auto-target for personalized experiences]**: Het doel gebruikt geavanceerde computerleeralgoritmen om bezoekers automatisch te richten met de beste ervaring om uw doelstellingen te maximaliseren. Voor meer informatie, zie [auto-Doel optimaliseren](../../../c-activities/auto-target-to-optimize.md#concept_67779E5B7F67427A97D7EA2A6FB919B3).
   U kunt ook klikken **[!UICONTROL Add Experience]** om een andere ervaring aan de activiteit toe te voegen.

1. Als u tevreden bent met het publiek en de opties voor uw ervaring, klikt u **[!UICONTROL Next]** om naar de derde stap van de driestapige workflow met instructies te gaan.

1. Geef de [doelen en instellingen](../../../c-activities/t-test-ab/t-test-create-ab/ab-goals-and-settings.md#reference_B25389FD6F3A4989801E740364B089CC) voor de activiteit op.

   ![A/B Activiteitsinstellingen](/help/c-activities/t-test-ab/t-test-create-ab/assets/ab_settings-new.png)

1. Klik op **[!UICONTROL Save]**.

Nadat u de activiteit creeert, toont het lusje van het Overzicht informatie over de activiteit, met inbegrip van een diagram van uw activiteit.

## Trainingsvideo: Een ![zelfstudie-badge voor A/B-tests maken (8:36)](/help/assets/tutorial.png)

In deze video ziet u hoe u een A/B-test maakt met behulp van de workflow met [!DNL Target] drie stappen.

* A/B-activiteit maken in Adobe Target
* Verkeer toewijzen met een handmatige splitsing of automatische verkeerstoewijzing

>[!VIDEO](https://video.tv.adobe.com/v/17391)
