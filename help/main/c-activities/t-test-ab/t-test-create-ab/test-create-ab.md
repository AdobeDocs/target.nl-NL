---
keywords: A/B;A/B test;A/B activiteit;nieuwe a/b activiteit;creeer a/b
description: Gebruik [!UICONTROL Visual Experience Composer] (VEC) om de activiteiten van de Test van A/B rechtstreeks op a  [!DNL Target]-Toegelaten pagina tot stand te brengen.
title: Hoe maak ik een A/B-test?
feature: A/B Tests
exl-id: 76002873-0b7c-44a8-8e89-8ad28b63eccb
source-git-commit: 9cc1eb4c5c95ea51bc0a1fc9e89b245a18c9914b
workflow-type: tm+mt
source-wordcount: '888'
ht-degree: 0%

---

# Een A/B-testactiviteit maken

Gebruik [!UICONTROL Visual Experience Composer] (VEC) in [!DNL Adobe Target] om [!UICONTROL A/B Test] -activiteiten rechtstreeks op een pagina met [!DNL Target] activering te maken en paginagedeelten in [!DNL Target] te wijzigen.

>[!NOTE]
>
>Naast de [!UICONTROL Manual] (Standaard) [!UICONTROL A/B Test] -activiteit (die in dit artikel wordt besproken), biedt [!DNL Target] twee extra typen [!UICONTROL A/B Test] -activiteiten: [!UICONTROL Auto-Allocate] en [!UICONTROL Auto-Target] .
>
>Zie [&#x200B; Types van A/B het Testen activiteiten &#x200B;](/help/main/c-activities/t-test-ab/test-ab.md#types) in *A/B het overzicht van de Test*.

Een handmatige [!UICONTROL A/B Test] activiteit maken:

1. Klik in de lijst **[!UICONTROL Activities]** op **[!UICONTROL Create Activity]** > **[!UICONTROL A/B Test]** .

1. Selecteer, indien nodig, [!UICONTROL Create A/B Test Activity] in het dialoogvenster **[!UICONTROL Visual]** .

   Selecteer [!UICONTROL Form-Based Experience Composer] als u de [!UICONTROL Form] -toets liever wilt gebruiken. Zie [&#x200B; vorm-Gebaseerde Composer van de Ervaring &#x200B;](/help/main/c-experiences/form-experience-composer.md) voor meer informatie.

   >[!NOTE]
   >
   >Naast de VEC en [!UICONTROL Form-Based Experience Composer] biedt [!DNL Target] ook de VEC. [!UICONTROL Single Page Application] Voor meer informatie over de diverse composers, zie [&#x200B; Ervaringen en Aanbiedingen &#x200B;](/help/main/c-experiences/experiences.md).
   >
   >Voor het oplossen van problemeninformatie over VEC, zie [&#x200B; het Oplossen van problemen de Visuele Composer van de Ervaring &#x200B;](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/troubleshoot-composer.md).

1. (Voorwaardelijk) als u a [&#x200B; klant van Target Premium &#x200B;](/help/main/c-intro/intro.md#premium) bent, van de **[!UICONTROL Choose Workspace]** drop-down lijst, kies a [&#x200B; werkruimte &#x200B;](/help/main/administrating-target/c-user-management/property-channel/property-channel.md).

   De [[!UICONTROL Choose Workplace]](/help/main/administrating-target/c-user-management/property-channel/property-channel.md) optie is a [&#x200B; Target Premium &#x200B;](/help/main/c-intro/intro.md) eigenschap en zou niet kunnen tonen als uw organisatie een [!UICONTROL Target Standard] vergunning heeft.

1. In het **[!UICONTROL Enter Activity URL]** vakje, specificeer uw [&#x200B; activiteit URL &#x200B;](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-activity-url.md).

   Als uw rekening [&#x200B; met een gebrek URL &#x200B;](/help/main/administrating-target/visual-experience-composer-set-up.md) wordt gevormd, verschijnt die URL door gebrek. U kunt desgewenst van de standaard naar een andere URL overschakelen.

1. Klik op **[!UICONTROL Create]**.

   De [!UICONTROL Visual Experience Composer] wordt geopend en geeft de pagina weer die in de URL is opgegeven.

1. Om de activiteit te noemen, klik het **[!UICONTROL Edit]** pictogram ( ![&#x200B; geef pictogram &#x200B;](/help/main/assets/icons/Edit.svg)) naast &quot; [!UICONTROL Untitled Activity] uit,&quot;specificeer een beschrijvende naam voor de activiteit, en klik dan **[!UICONTROL Save]**.

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

   In [!UICONTROL Visual Experience Composer] worden twee tabbladen aan de linkerkant weergegeven nadat u een nieuwe activiteit hebt gemaakt: Experience A en Experience B. Experience A is de controleleving. De focus ligt op het tabblad Experience B, dat u naar wens kunt wijzigen. Ervaring B is de alternatieve ervaring die u aan uw test kunt toevoegen. U kunt veelvoudige ervaringen aan de test toevoegen door het [!UICONTROL Add] pictogram ( ![&#x200B; toe te voegen pictogram &#x200B;](/help/main/assets/icons/Add.svg)) bij de bovenkant van de [!UICONTROL Experiences] ruit te klikken. U kunt ook Experience A verwijderen uit de activiteit als u geen standaard site-ervaring wilt opnemen als optie.

   Voor meer informatie over het toevoegen van en het wijzigen van ervaringen in [!UICONTROL Visual Experience Composer], zie [&#x200B; Ervaring &#x200B;](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-add-experience.md#task_454646F2895242D3B92DC395A0CE1A00) toevoegen. Om Ervaring B te wijzigen, begin met Stap 2.

1. Klik op **[!UICONTROL Targeting]** boven aan [!UICONTROL Visual Experience Composer] om naar de volgende stap in de driestappenworkflow met instructies te gaan.

   Het stroomdiagram wordt geopend.

   ![&#x200B; A/B de Test richtend stap &#x200B;](/help/main/c-activities/t-test-ab/t-test-create-ab/assets/ab_flow-new-ui.png)

   Het stroomdiagram leidt u door de stappen om een publiek en zijn verkeerspercentage toe te wijzen, die de methode van de verkeerstoewijzing selecteren, en de verkeerstoewijzing voor elke ervaring in de activiteit specificeren.

1. (Voorwaardelijk) klik de **[!UICONTROL All Visitors]** controle om een ander publiek voor de activiteit te selecteren.

   De doelgroep van [!UICONTROL All Visitors] wordt ingesteld als de standaardgroep. Als u een ander publiek selecteert, wordt de naam van het publiek uiterst links weergegeven.

   Het juiste frame wordt weergegeven, waarmee u een publiek kunt toevoegen of verwijderen en het bezoekerspercentage voor de activiteit kunt toewijzen.

   1. Om het publiek te veranderen, klik het **[!UICONTROL Replace]pictogram** ( ![&#x200B; vervangt pictogram &#x200B;](/help/main/assets/icons/Retweet.svg)) in het juiste kader.
   1. In het [!UICONTROL Add Audience] dialoogvakje, [&#x200B; selecteer het gewenste publiek &#x200B;](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-audience.md), dan klik **[!UICONTROL Assign Audience]**.

      U kunt **klikken combineert Soorten publiek** om [&#x200B; een publiek tot stand te brengen dat veelvoudige publiek &#x200B;](/help/main/c-target/combining-multiple-audiences.md) combineert.

      Als u een nieuw publiek moet tot stand brengen dat niet reeds in [!UICONTROL Audience Library] is, klik **creeer Publiek**. Tijdens het [&#x200B; creeer-publiek werkschema &#x200B;](/help/main/c-target/c-audiences/audiences.md) kunt u van de volgende opties kiezen:

      * **[!UICONTROL Audience Library]**: Maak een publiek op aanvraag dat wordt opgeslagen in [!UICONTROL Audience Library] en dat opnieuw kan worden gebruikt in andere activiteiten.
      * **[!UICONTROL This activity only]**: Creeer een [&#x200B; activiteit-specifiek publiek &#x200B;](/help/main/c-target/creating-activity-only-audience.md) dat niet aan [!UICONTROL Audience Library] wordt bewaard en in de huidige activiteit slechts kan worden gebruikt.

   1. Klik op **[!UICONTROL Visitor Percentage]** in het rechterframe en kies het percentage gekwalificeerde bezoekers dat u de activiteit wilt invoeren.

   U kunt bijvoorbeeld items beperken tot 50% van alle bezoekers of 45% van uw &quot;Californische&quot; publiek.

1. Klik de **[!UICONTROL Traffic Allocation]** controle, dan kies de gewenste methode van de verkeerstoewijzing in de juiste ruit, zoals hieronder getoond:

   ![&#x200B; montages van de Methode van de Toewijzing van het Verkeer &#x200B;](/help/main/c-activities/t-test-ab/t-test-create-ab/assets/traffic-allocation-method-new.png)

   Kies uw gewenste methode voor verkeerstoewijzing:

   * **[!UICONTROL Manual (Default)]**: geef het percentage van de gegadigden op dat u elke ervaring wilt zien. U kunt de percentages gelijkmatig over alle ervaringen verdelen, of hogere of lagere percentages voor elke ervaring specificeren. Het totaal voor alle ervaringen moet 100% bedragen.

   * **[!UICONTROL Auto-Allocate to best experience]**: De meeste deelnemers aan de activiteit worden automatisch omgeleid naar beter presterende ervaringen. Sommige bezoekers worden toegewezen aan alle ervaringen, om het verkennen van ervaringen te handhaven en veranderingen in prestatietrends te erkennen. Zie [[!UICONTROL Auto-Allocate] overview &#x200B;](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md#concept_A1407678796B4C569E94CBA8A9F7F5D4) voor meer informatie.

   * **[!UICONTROL Auto-Target for personalized experiences]**: [!DNL Target] maakt gebruik van geavanceerd leren van computers om inhoud en stationsomzettingen aan te passen door het identificeren van meerdere hoogwaardige, door markters gedefinieerde ervaringen en vervolgens de meest op maat gemaakte ervaring aan bezoekers te bieden op basis van hun individuele klantprofielen en eerdere gedragingen van vergelijkbare bezoekers. Voor meer informatie, zie [&#x200B; auto-Doel overzicht &#x200B;](/help/main/c-activities/auto-target/auto-target-to-optimize.md).

1. Klik op **[!UICONTROL Experiences]** in het rechterdeelvenster en geef vervolgens de gewenste verkeerstoewijzing voor elke ervaring op.

1. Als u tevreden bent met het publiek, de ervaringsopties en de keuzes voor verkeerstoewijzing, klikt u op **[!UICONTROL Next]** om naar de derde stap van de driestappenworkflow met instructies te gaan.

1. Specificeer de [&#x200B; doelstellingen en de montages &#x200B;](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-goals-and-settings.md) voor de activiteit.

1. Klik op **[!UICONTROL Save & Close]** of **[!UICONTROL Save]** .

Nadat u de activiteit creeert, toont het [!UICONTROL Overview] lusje informatie over de activiteit, met inbegrip van een diagram van uw activiteit.
