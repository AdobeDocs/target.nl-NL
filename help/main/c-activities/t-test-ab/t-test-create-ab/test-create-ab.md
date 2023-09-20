---
keywords: A/B;A/B test;A/B activiteit;nieuwe a/b activiteit;creeer a/b
description: Leer hoe te om Visual Experience Composer (VEC) in Adobe te gebruiken [!DNL Target] om uw A/B-testactiviteit rechtstreeks op een [!DNL Target]-enabled pagina.
title: Hoe maak ik een A/B-test?
feature: A/B Tests
exl-id: 76002873-0b7c-44a8-8e89-8ad28b63eccb
source-git-commit: ec1041fd1823d1ab7f1af147af5825c3ae8662b5
workflow-type: tm+mt
source-wordcount: '843'
ht-degree: 0%

---

# Een A/B-test maken

Gebruik de [!UICONTROL Visual Experience Composer] (VEC) in [!DNL Adobe Target] om uw [!UICONTROL A/B Test] rechtstreeks op een [!DNL Target]-enabled pagina en om gedeelten van de pagina binnen te wijzigen [!DNL Target].

>[!NOTE]
>
>Naast de handleiding (standaard) [!UICONTROL A/B Test] activiteit (in dit artikel besproken), [!DNL Target] verstrekt twee extra types van [!UICONTROL A/B Test] activiteiten: [!UICONTROL Auto-Allocate] en [!UICONTROL Auto-Target].
>
>Zie [Typen A/B-testactiviteiten](/help/main/c-activities/t-test-ab/test-ab.md#types) in *A/B-testoverzicht*.

Een handleiding maken [!UICONTROL A/B Test] activiteit:

1. Van de **[!UICONTROL Activities]** lijst, klik **[!UICONTROL Create Activity]** > **[!UICONTROL A/B Test]**.

   ![Vervolgkeuzelijst Activiteit maken](/help/main/c-activities/t-test-ab/t-test-create-ab/assets/ab_select-new.png)

   >[!NOTE]
   >
   >De beschikbare activiteitstypen zijn afhankelijk van uw [!DNL Target] account. Sommige typen activiteiten worden mogelijk niet in de lijst weergegeven. Bijvoorbeeld: [!UICONTROL Recommendations] is een [Functie Doelpremium](/help/main/c-intro/intro.md#premium).
   >
   >Voor informatie over de diverse activiteitstypen raadpleegt u [Activiteiten](/help/main/c-activities/activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03) en de [Doelgids voor activiteiten](/help/main/c-activities/target-activities-guide.md).

1. Selecteer in het dialoogvenster A/B-testactiviteit maken de optie **[!UICONTROL Visual (Default)]**, indien nodig.

   Als u liever het [!UICONTROL Form-Based Experience Composer], selecteert u [!UICONTROL Form]. Zie [Formuliergebaseerde Experience Composer](/help/main/c-experiences/form-experience-composer.md) voor meer informatie .

   >[!NOTE]
   >
   >Naast de VEC en [!UICONTROL Form-Based Experience Composer], [!DNL Target] biedt de Single Page Application VEC aan. Zie voor meer informatie over de verschillende composers [Ervaringen en aanbiedingen](/help/main/c-experiences/experiences.md).
   >
   >Voor het oplossen van problemeninformatie over VEC, als u problemen hebt, zie [Problemen oplossen met de composer voor visuele ervaring](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/troubleshoot-composer.md).

1. (Voorwaardelijk) Als u een [De klant van de Premium van het doel](/help/main/c-intro/intro.md#premium)van de **[!UICONTROL Choose Workspace]** vervolgkeuzelijst, kies een [werkruimte](/help/main/administrating-target/c-user-management/property-channel/property-channel.md).

   De [[!UICONTROL Choose Workplace]](/help/main/administrating-target/c-user-management/property-channel/property-channel.md) optie in de voorgaande illustratie is een [Doelpremie](/help/main/c-intro/intro.md) en wordt mogelijk niet weergegeven als uw organisatie een [!UICONTROL Target Standard] licentie.

1. In de **[!UICONTROL Enter Activity URL]** in, geef uw [activiteit-URL](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-activity-url.md)en klik vervolgens op **[!UICONTROL Create]**.

   Als uw account [geconfigureerd met een standaard-URL](/help/main/administrating-target/visual-experience-composer-set-up.md), wordt die URL standaard weergegeven. U kunt desgewenst van de standaard naar een andere URL overschakelen.

   De [!UICONTROL Visual Experience Composer] wordt geopend en wordt de pagina weergegeven die in de URL is opgegeven.

1. Klikken **[!UICONTROL Untitled Activity]** boven aan de VEC geeft u een naam op voor de activiteit in de beschikbare ruimte.

   De naam van de activiteit mag niet met een van de volgende tekens beginnen:

   | Teken | Beschrijving |
   |--- |--- |
   | `=` | Gelijk aan |
   | `+` | Plus |
   | `-` | Min |
   | `@` | Bij ondertekenen |

   De naam van de activiteit mag geen van de volgende tekenreeksen bevatten:

   | Tekenreeks | Beschrijving |
   |--- |--- |
   | ;= | Semicolon, is gelijk aan |
   | ;+ | Puntkomma, plus |
   | ;- | Puntkomma, min |
   | ;@ | Puntkomma, bij teken |
   | ,= | Komma, is gelijk aan |
   | ,+ | Komma, plus |
   | ,- | Komma, min |
   | ,@ | Komma, bij teken |
   | `[`&quot; | Vierkante haak openen, dubbele aanhalingstekens |
   | &quot;`]` | Dubbele aanhalingstekens, vierkant haakje sluiten |

1. Maak nieuwe ervaringen door de elementen op de pagina te wijzigen.

   De [!UICONTROL Visual Experience Composer] Hiermee geeft u twee tabbladen aan de linkerkant weer nadat u een nieuwe activiteit hebt gemaakt: Experience A en Experience B. Experience A is the control experience. De focus ligt op het tabblad Experience B, dat u naar wens kunt wijzigen. Ervaring B is de alternatieve ervaring die u aan uw test kunt toevoegen. U kunt meerdere ervaringen toevoegen aan de test. U kunt ook Experience A verwijderen uit de activiteit als u geen standaard site-ervaring wilt opnemen als optie.

   Voor meer informatie over het toevoegen van en het wijzigen van ervaringen in [!UICONTROL Visual Experience Composer], zie [Ervaring toevoegen](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-add-experience.md#task_454646F2895242D3B92DC395A0CE1A00). Om Ervaring B te wijzigen, begin met Stap 2.

1. Klikken **[!UICONTROL Targeting]** boven aan het dialoogvenster [!UICONTROL Visual Experience Composer] om naar de volgende stap in de driestappenworkflow met instructies te gaan.

   Het stroomdiagram wordt geopend.

   ![Teststap A/B](/help/main/c-activities/t-test-ab/t-test-create-ab/assets/ab_flow-new.png)

   Het stroomdiagram leidt u door de stappen om het publiek voor de activiteit te kiezen en opstellingservaringen.

1. In de **[!UICONTROL Audience]** , klikt u op het pictogram Bewerken (de verticale ellips) en klikt u op **[!UICONTROL Replace Audience]** vervolgens [het publiek selecteren](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-audience.md) voor je activiteit.

   Standaard is de doelgroep ingesteld op [!UICONTROL All Visitors].

1. Kies het percentage in aanmerking komende bezoekers dat u de activiteit wilt ingaan.

   ![Publiek percentage](/help/main/c-activities/t-test-ab/t-test-create-ab/assets/audperc-new.png)

   U kunt bijvoorbeeld items beperken tot 50% van alle bezoekers of 45% van uw &quot;Californische&quot; publiek.

1. Opstelling uw verkeerstoewijzing.

   U kunt meerdere ervaringen aan hetzelfde publiek tonen. Een diagram toont het geselecteerde publiek en de ervaringen die u aan de activiteit hebt toegevoegd.

   Kies uw gewenste methode voor verkeerstoewijzing:

   * **[!UICONTROL Manual (Default)]**: Geef het percentage van de gegadigden op dat u voor elke ervaring wilt zien. U kunt de percentages gelijkmatig over alle ervaringen verdelen, of hogere of lagere percentages voor elke ervaring specificeren. Het totaal voor alle ervaringen moet 100% bedragen.

   * **[!UICONTROL Auto-allocate to best experience]**: De meeste deelnemers aan de activiteit worden automatisch gericht op beter presterende ervaringen. Sommige bezoekers worden toegewezen aan alle ervaringen, om het verkennen van ervaringen te handhaven en veranderingen in prestatietrends te erkennen. Zie voor meer informatie [[!UICONTROL Auto-Allocate] overzicht](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md#concept_A1407678796B4C569E94CBA8A9F7F5D4).

   * **[!UICONTROL Auto-target for personalized experiences]**: [!DNL Target] maakt gebruik van geavanceerd computerleren om inhoud en stationsomzettingen aan te passen door het identificeren van meervoudige, door de markt gedefinieerde ervaringen, en vervolgens de meest toegesneden ervaring aan bezoekers te bezorgen op basis van hun individuele klantprofielen en eerdere gedragingen van vergelijkbare bezoekers. Zie voor meer informatie [Overzicht van automatisch doel](/help/main/c-activities/auto-target/auto-target-to-optimize.md).

   U kunt ook op **[!UICONTROL Add]** om een andere ervaring aan de activiteit toe te voegen.

1. Wanneer u met uw publiek, ervaringskeuzen, en de keuzen van de verkeerstoewijzing tevreden bent, klik **[!UICONTROL Next]** om naar de derde stap van de driestappenworkflow met instructies te gaan.

1. Geef de [doelstellingen en instellingen](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-goals-and-settings.md) voor de activiteit.

1. Klikken **[!UICONTROL Save & Close]** of **[!UICONTROL Save]**.

Nadat u de activiteit creeert, [!UICONTROL Overview] op het tabblad vindt u informatie over de activiteit, inclusief een diagram met uw activiteit.

## Trainingsvideo: A/B-tests maken (8:36) ![Zelfstudie-badge](/help/main/assets/tutorial.png)

In deze video ziet u hoe u een A/B-test maakt met de opdracht [!DNL Target] driestapsgerichte workflow.

* Een [!UICONTROL A/B Test] activiteit in [!DNL Adobe Target]
* Verkeer toewijzen met een handmatige splitsing of automatische verkeerstoewijzing

>[!VIDEO](https://video.tv.adobe.com/v/17391)
