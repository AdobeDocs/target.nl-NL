---
keywords: Automatisch doel maken;A/B-test;automatisch doelactiviteit;nieuwe a/b-activiteit;automatisch doel;automatisch doel voor persoonlijke ervaringen;gepersonaliseerd;optimalisatie
description: Leer hoe u [!UICONTROL Visual Experience Composer] (VEC) gebruikt om een [!UICONTROL Auto-Target] A/B-testactiviteit te maken.
title: Hoe maak ik een [!UICONTROL Auto-Target] -activiteit?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=nl-NL#premium newtab=true" tooltip="Kijk wat er in Target Premium is opgenomen."
feature: Auto-Target
exl-id: 5521740c-eee2-4ba2-8931-cf56d56a4561
source-git-commit: 32a91a41cd182d3a55ded7dea8c1c6ea6f46aa71
workflow-type: tm+mt
source-wordcount: '905'
ht-degree: 0%

---

# Een [!UICONTROL Auto-Target] activiteit maken

Gebruik [!UICONTROL Visual Experience Composer] (VEC) in [!DNL Adobe Target] om uw [!UICONTROL Auto-Target] [!UICONTROL A/B Test] -activiteit rechtstreeks op een pagina met [!DNL Target] functies te maken en om delen van de pagina binnen [!DNL Target] te wijzigen.

>[!NOTE]
>
>[!UICONTROL Auto-Target] is beschikbaar als onderdeel van de [!DNL Target Premium] -oplossing. Deze functie is niet beschikbaar in [!DNL Target Standard] zonder een [!DNL Target Premium] -licentie. Voor meer informatie over de geavanceerde eigenschappen verstrekt deze vergunning, zie [&#x200B; Target Premium &#x200B;](/help/main/c-intro/intro.md).

Een [!UICONTROL Auto-Target] -activiteit maken:

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

1. Klik het **[!UICONTROL Rename]** pictogram ( ![&#x200B; anders noemen pictogram &#x200B;](/help/main/assets/icons/MoreSmallListVert.svg)), klik **[!UICONTROL Rename]**, specificeer een naam voor de activiteit, dan klik **[!UICONTROL Save]**.

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

   In [!UICONTROL Visual Experience Composer] worden twee tabbladen aan de linkerkant weergegeven nadat u een nieuwe activiteit hebt gemaakt: [!UICONTROL Experience A] en [!UICONTROL Experience B] . [!UICONTROL Experience A] is de besturingservaring. De focus ligt op de tab [!UICONTROL Experience B] , die u naar wens kunt wijzigen. [!UICONTROL Experience B] is de alternatieve ervaring die u aan de test kunt toevoegen. U kunt veelvoudige ervaringen aan de test toevoegen door het [!UICONTROL Add] pictogram ( ![&#x200B; toe te voegen pictogram &#x200B;](/help/main/assets/icons/Add.svg)) bij de bovenkant van de [!UICONTROL Experiences] ruit te klikken. U kunt ook Experience A verwijderen uit de activiteit als u geen standaard site-ervaring wilt opnemen als optie.

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

      * **[!UICONTROL Audience Library]**: Maak een publiek op aanvraag dat wordt opgeslagen in de [!UICONTROL Audience Library] en dat opnieuw kan worden gebruikt in andere activiteiten
      * **[!UICONTROL This activity only]**: Creeer een [&#x200B; activiteit-specifiek publiek &#x200B;](/help/main/c-target/creating-activity-only-audience.md) dat niet aan [!UICONTROL Audience Library] wordt bewaard en in de huidige activiteit slechts kan worden gebruikt

   1. Klik op **[!UICONTROL Visitor Percentage]** in het rechterframe en kies het percentage gekwalificeerde bezoekers dat u de activiteit wilt invoeren.

   U kunt bijvoorbeeld items beperken tot 50% van alle bezoekers of 45% van uw &quot;Californische&quot; publiek.

1. Klik de **[!UICONTROL Traffic Allocation]** controle, dan kies de gewenste methode van de verkeerstoewijzing in de juiste ruit. Klik in dit scenario op **[!UICONTROL Auto-Taget for personalized experiences]** .

   ![&#x200B; montages van de Methode van de Toewijzing van het Verkeer &#x200B;](/help/main/c-activities/assets/auto-target.png)

   De volgende methoden voor verkeerstoewijzing zijn beschikbaar:

   * **[!UICONTROL Manual (Default)]**: geef het percentage van de gegadigden op dat u elke ervaring wilt zien. U kunt de percentages gelijkmatig over alle ervaringen verdelen, of hogere of lagere percentages voor elke ervaring specificeren. Het totaal voor alle ervaringen moet 100% bedragen.

   * **[!UICONTROL Auto-Allocate to best experience]**: De meeste deelnemers aan de activiteit worden automatisch omgeleid naar beter presterende ervaringen. Sommige bezoekers worden toegewezen aan alle ervaringen, om het verkennen van ervaringen te handhaven en veranderingen in prestatietrends te erkennen. Zie [[!UICONTROL Auto-Allocate] overview &#x200B;](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md#concept_A1407678796B4C569E94CBA8A9F7F5D4) voor meer informatie.

   * **[!UICONTROL Auto-Target for personalized experiences]**: [!DNL Target] maakt gebruik van geavanceerd leren van computers om inhoud en stationsomzettingen aan te passen door het identificeren van meerdere hoogwaardige, door markters gedefinieerde ervaringen en vervolgens de meest op maat gemaakte ervaring aan bezoekers te bieden op basis van hun individuele klantprofielen en eerdere gedragingen van vergelijkbare bezoekers. Voor meer informatie, zie [&#x200B; auto-Doel overzicht &#x200B;](/help/main/c-activities/auto-target/auto-target-to-optimize.md).

1. Klik op **[!UICONTROL Experiences]** in het rechterdeelvenster en geef vervolgens de gewenste verkeerstoewijzing voor elke ervaring op.

1. Als u tevreden bent met het publiek, de ervaringsopties en de keuzes voor verkeerstoewijzing, klikt u op **[!UICONTROL Next]** om naar de derde stap van de driestappenworkflow met instructies te gaan.

1. Specificeer de [&#x200B; doelstellingen en de montages &#x200B;](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-goals-and-settings.md) voor de activiteit.

   >[!NOTE]
   >
   >Als u [&#x200B; Analytics voor Doel &#x200B;](/help/main/c-integrating-target-with-mac/a4t/a4t.md) (A4T) met deze activiteit wilt gebruiken, zie belangrijke informatie in [&#x200B; steun A4T voor auto-Wijs en auto-Doel activiteiten &#x200B;](/help/main/c-integrating-target-with-mac/a4t/a4t-at-aa.md).

1. Klik op **[!UICONTROL Save & Close]** of **[!UICONTROL Save]** .

Nadat u de activiteit creeert, toont het [!UICONTROL Overview] lusje informatie over de activiteit, met inbegrip van een diagram van uw activiteit.
