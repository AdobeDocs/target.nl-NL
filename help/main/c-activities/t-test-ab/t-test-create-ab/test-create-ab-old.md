---
keywords: A/B;A/B test;A/B activiteit;nieuwe a/b activiteit;creeer a/b
description: Leer hoe te om de Visuele Composer van de Ervaring (VEC) in Adobe  [!DNL Target]  te gebruiken om uw activiteit van de Test van A/B direct op a  [!DNL Target]-Toegelaten pagina tot stand te brengen.
title: Hoe maak ik een A/B-test?
feature: A/B Tests
exl-id: 76002873-0b7c-44a8-8e89-8ad28b63eccb
source-git-commit: eb7e892a85fa3952ffc22172085d421756d0dfb5
workflow-type: tm+mt
source-wordcount: '848'
ht-degree: 0%

---

# Een A/B-test maken

Gebruik [!UICONTROL Visual Experience Composer] (VEC) in [!DNL Adobe Target] om de [!UICONTROL A/B Test] -activiteit rechtstreeks op een pagina met [!DNL Target] activering te maken en om gedeelten van de pagina binnen [!DNL Target] te wijzigen.

>[!NOTE]
>
>Naast de activiteit Handmatig (standaard) [!UICONTROL A/B Test] (die in dit artikel wordt besproken), biedt [!DNL Target] twee extra typen [!UICONTROL A/B Test] -activiteiten: [!UICONTROL Auto-Allocate] en [!UICONTROL Auto-Target] .
>
>Zie [&#x200B; Types van A/B het Testen activiteiten &#x200B;](/help/main/c-activities/t-test-ab/test-ab.md#types) in *A/B het overzicht van de Test*.

Een handmatige [!UICONTROL A/B Test] activiteit maken:

1. Klik in de lijst **[!UICONTROL Activities]** op **[!UICONTROL Create Activity]** > **[!UICONTROL A/B Test]** .

   ![&#x200B; creeer de drop-down lijst van de Activiteit &#x200B;](/help/main/c-activities/t-test-ab/t-test-create-ab/assets/ab_select-new.png)

   >[!NOTE]
   >
   >De beschikbare activiteitstypen zijn afhankelijk van uw [!DNL Target] -account. Sommige typen activiteiten worden mogelijk niet in de lijst weergegeven. Bijvoorbeeld, [!UICONTROL Recommendations] is de eigenschap van a [&#x200B; Target Premium &#x200B;](/help/main/c-intro/intro.md#premium).
   >
   >Voor informatie over de diverse activiteitentypes, zie [&#x200B; Activiteiten &#x200B;](/help/main/c-activities/activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03) en de [&#x200B; gids van de Activiteiten van het Doel &#x200B;](/help/main/c-activities/target-activities-guide.md).

1. Selecteer, indien nodig, **[!UICONTROL Visual (Default)]** in het dialoogvenster A/B-testactiviteit maken.

   Selecteer [!UICONTROL Form-Based Experience Composer] als u de [!UICONTROL Form] -toets liever wilt gebruiken. Zie [&#x200B; vorm-Gebaseerde Composer van de Ervaring &#x200B;](/help/main/c-experiences/form-experience-composer.md) voor meer informatie.

   >[!NOTE]
   >
   >Naast de VEC en [!UICONTROL Form-Based Experience Composer] biedt [!DNL Target] de toepassing VEC voor één pagina. Voor meer informatie over de diverse composers, zie [&#x200B; Ervaringen en Aanbiedingen &#x200B;](/help/main/c-experiences/experiences.md).
   >
   >Voor het oplossen van problemeninformatie over VEC, als u problemen hebt, zie [&#x200B; het Oplossen van problemen de Visuele Composer van de Ervaring &#x200B;](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/troubleshoot-composer.md).

1. (Voorwaardelijk) als u a [&#x200B; klant van Target Premium &#x200B;](/help/main/c-intro/intro.md#premium) bent, van de **[!UICONTROL Choose Workspace]** drop-down lijst, kies a [&#x200B; werkruimte &#x200B;](/help/main/administrating-target/c-user-management/property-channel/property-channel.md).

   De [[!UICONTROL Choose Workplace]](/help/main/administrating-target/c-user-management/property-channel/property-channel.md) optie in de voorafgaande illustratie is a [&#x200B; Target Premium &#x200B;](/help/main/c-intro/intro.md) eigenschap en zou niet kunnen tonen als uw organisatie een [!UICONTROL Target Standard] vergunning heeft.

1. In het **[!UICONTROL Enter Activity URL]** vakje, specificeer uw [&#x200B; activiteit URL &#x200B;](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-activity-url.md), dan klik **[!UICONTROL Create]**.

   Als uw rekening [&#x200B; met een gebrek URL &#x200B;](/help/main/administrating-target/visual-experience-composer-set-up.md) wordt gevormd, verschijnt die URL door gebrek. U kunt desgewenst van de standaard naar een andere URL overschakelen.

   De [!UICONTROL Visual Experience Composer] wordt geopend en geeft de pagina weer die in de URL is opgegeven.

1. Klik **[!UICONTROL Untitled Activity]** bij de bovenkant van VEC, dan specificeer een naam voor de activiteit in de verstrekte ruimte.

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

   In [!UICONTROL Visual Experience Composer] worden twee tabbladen aan de linkerkant weergegeven nadat u een nieuwe activiteit hebt gemaakt: Experience A en Experience B. Experience A is de controleleving. De focus ligt op het tabblad Experience B, dat u naar wens kunt wijzigen. Ervaring B is de alternatieve ervaring die u aan uw test kunt toevoegen. U kunt meerdere ervaringen toevoegen aan de test. U kunt ook Experience A verwijderen uit de activiteit als u geen standaard site-ervaring wilt opnemen als optie.

   Voor meer informatie over het toevoegen van en het wijzigen van ervaringen in [!UICONTROL Visual Experience Composer], zie [&#x200B; Ervaring &#x200B;](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-add-experience.md#task_454646F2895242D3B92DC395A0CE1A00) toevoegen. Om Ervaring B te wijzigen, begin met Stap 2.

1. Klik op **[!UICONTROL Targeting]** boven aan [!UICONTROL Visual Experience Composer] om naar de volgende stap in de driestappenworkflow met instructies te gaan.

   Het stroomdiagram wordt geopend.

   ![&#x200B; A/B de Test richtend stap &#x200B;](/help/main/c-activities/t-test-ab/t-test-create-ab/assets/ab_flow-new.png)

   Het stroomdiagram leidt u door de stappen om het publiek voor de activiteit te kiezen en opstellingservaringen.

1. In het **[!UICONTROL Audience]** vakje, klik uitgeven pictogram (de verticale ellips), klik **[!UICONTROL Replace Audience]**, dan [&#x200B; selecteer het publiek &#x200B;](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-audience.md) voor uw activiteit.

   Standaard is het publiek ingesteld op [!UICONTROL All Visitors] .

1. Kies het percentage in aanmerking komende bezoekers dat u de activiteit wilt ingaan.

   ![&#x200B; percentage van het publiek &#x200B;](/help/main/c-activities/t-test-ab/t-test-create-ab/assets/audperc-new.png)

   U kunt bijvoorbeeld items beperken tot 50% van alle bezoekers of 45% van uw &quot;Californische&quot; publiek.

1. Opstelling uw verkeerstoewijzing.

   U kunt meerdere ervaringen aan hetzelfde publiek tonen. Een diagram toont het geselecteerde publiek en de ervaringen die u aan de activiteit hebt toegevoegd.

   Kies uw gewenste methode voor verkeerstoewijzing:

   * **[!UICONTROL Manual (Default)]**: geef het percentage van de gegadigden op dat u elke ervaring wilt zien. U kunt de percentages gelijkmatig over alle ervaringen verdelen, of hogere of lagere percentages voor elke ervaring specificeren. Het totaal voor alle ervaringen moet 100% bedragen.

   * **[!UICONTROL Auto-allocate to best experience]**: De meeste deelnemers aan de activiteit worden automatisch omgeleid naar beter presterende ervaringen. Sommige bezoekers worden toegewezen aan alle ervaringen, om het verkennen van ervaringen te handhaven en veranderingen in prestatietrends te erkennen. Zie [[!UICONTROL Auto-Allocate] overview &#x200B;](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md#concept_A1407678796B4C569E94CBA8A9F7F5D4) voor meer informatie.

   * **[!UICONTROL Auto-target for personalized experiences]**: [!DNL Target] maakt gebruik van geavanceerd leren van computers om inhoud en stationsomzettingen aan te passen door het identificeren van meerdere hoogwaardige, door markters gedefinieerde ervaringen en vervolgens de meest op maat gemaakte ervaring aan bezoekers te bieden op basis van hun individuele klantprofielen en eerdere gedragingen van vergelijkbare bezoekers. Voor meer informatie, zie [&#x200B; auto-Doel overzicht &#x200B;](/help/main/c-activities/auto-target/auto-target-to-optimize.md).

   U kunt ook op **[!UICONTROL Add]** klikken om een andere ervaring aan de activiteit toe te voegen.

1. Als u tevreden bent met het publiek, de ervaringsopties en de keuzes voor verkeerstoewijzing, klikt u op **[!UICONTROL Next]** om naar de derde stap van de driestappenworkflow met instructies te gaan.

1. Specificeer de [&#x200B; doelstellingen en de montages &#x200B;](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-goals-and-settings.md) voor de activiteit.

1. Klik op **[!UICONTROL Save & Close]** of **[!UICONTROL Save]** .

Nadat u de activiteit creeert, toont het [!UICONTROL Overview] lusje informatie over de activiteit, met inbegrip van een diagram van uw activiteit.

## De video van de opleiding: Creërend A/B Tests (8 :36) ![&#x200B; badge van het Leerprogramma &#x200B;](/help/main/assets/tutorial.png)

In deze video ziet u hoe u een A/B-test maakt met behulp van de [!DNL Target] driestapige geleide workflow.

* Een [!UICONTROL A/B Test] activiteit maken in [!DNL Adobe Target]
* Verkeer toewijzen met een handmatige splitsing of automatische verkeerstoewijzing

>[!VIDEO](https://video.tv.adobe.com/v/17391)
