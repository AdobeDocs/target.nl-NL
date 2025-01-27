---
keywords: mvt;multivariate test;multivariate test creeert;multivariate test creeert;mvt creeert;mvt creeert;mvt hoe;multivariate test hoe
description: Leer hoe te om [!UICONTROL Visual Experience Composer] (VEC) in  [!DNL Adobe Target]  te gebruiken om a [!UICONTROL Multivariate Test] (MVT) tot stand te brengen.
title: Hoe maak ik een [!UICONTROL Multivariate Test] ?
feature: Multivariate Tests
hide: true
hidefromtoc: true
source-git-commit: 4805da617962e29794bd3af16138f3887ad250d0
workflow-type: tm+mt
source-wordcount: '724'
ht-degree: 0%

---

# Een multivariatietest maken

Met [!UICONTROL Visual Experience Composer] (VEC) in [!DNL Adobe Target] kunt u eenvoudig een [!UICONTROL Multivariate Test] -pagina maken en delen van de pagina binnen [!DNL Target] wijzigen.

Met de [!DNL Target] point-and-click-editor kunt u elke gewenste locatie kiezen en meerdere aanbiedingen toevoegen.

Voor [!UICONTROL Multivariate Test] (MVT) wordt eerst een rapport op de pagina weergegeven. Met andere woorden, de test wordt uitgevoerd op een specifieke URL, met de ervaringen u voor die pagina ontwerpt.

1. Klik op **[!UICONTROL Create Activity]** > **[!UICONTROL Multivariate Test]** .

   >[!NOTE]
   >
   >Voor meer informatie over de diverse activiteitentypes beschikbaar in [!DNL Target] en hun verschillen, zie [ Activiteiten ](/help/main/c-activities/activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03). Zie [ de types van Activiteit van het Doel ](/help/main/c-activities/target-activities-guide.md) om u te helpen beslissen welk type van activiteit beste reeksen uw behoeften.

1. (Voorwaardelijk) Kies het leveringstype: [!UICONTROL Web] , [!UICONTROL Mobile] , [!UICONTROL Email] of [!UICONTROL Other/API] .

1. (Voorwaardelijk) als u a [ Target Premium ](/help/main/c-intro/intro.md#premium) klant bent, [ kies een werkruimte ](/help/main/administrating-target/c-user-management/property-channel/property-channel.md).

1. [ specificeer URL ](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/url.md#concept_C12E4A85FF3B4E518E3110F6CF1AF9C0) voor de pagina die u wilt testen, dan klikken **[!UICONTROL Create]**.

   >[!NOTE]
   >
   >Gebruik aan het begin een volledige URL, inclusief HTTP of HTTPS.

   Als er een bericht wordt weergegeven waarin u wordt gevraagd uw browser in te schakelen voor gemengde inhoud, volgt u de instructies in het bericht. Nadat u de browser hebt ingeschakeld voor gemengde inhoud, begint u opnieuw bij Stap 1.

   De lus [!UICONTROL Visual Experience Composer] wordt geopend.

1. 
   1. Klik het **[!UICONTROL Rename]** pictogram ( ![ anders noemen pictogram ](/help/main/assets/icons/MoreSmallListVert.svg)), klik **[!UICONTROL Rename]**, specificeer een naam voor de activiteit, dan klik **[!UICONTROL Save]**.

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

1. [ creeer de aanbiedingen in elke plaats ](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/add-offers.md#concept_DCE6B45C30F7419B8EC17AFDEE8D8AA6).

   U kunt de volgende soorten voorstellen toevoegen:

   * HTML
   * Afbeelding
   * Tekst

1. Klik **[!UICONTROL Preview]** aan [ voorproef uw ervaringen ](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/preview-experiences.md).

1. Klik het **[!UICONTROL Show Experiences]** pictogram ( ![ toon het pictogram van Ervaring ](/help/main/assets/icons/WebPages.svg)) om de lijst van alle ervaringen in het linkerkader te tonen.

1. Klik op een specifieke ervaring in de lijst om die ervaring weer te geven.

1. (Voorwaardelijk) om één of meerdere ervaringen van de activiteit uit te sluiten, klik het **[!UICONTROL Manage Content]** pictogram ( ![ beheer het pictogram van Ervaring ](/help/main/assets/icons/Experience.svg)) om het [!UICONTROL Manage Experiences] dialoogvakje te tonen.

1. (Voorwaardelijk) in het [!UICONTROL Manage Experiences] dialoogvakje, klik het **[!UICONTROL More Actions]** pictogram ( ![ Meer pictogram van Acties ](/help/main/assets/icons/MoreSmallList.svg)) naast de ervaring die u wilt uitsluiten, dan klik **[!UICONTROL Exclude]**.

   U kunt een ervaring uitsluiten die conflicterende variaties vertoont of een ervaring die niet esthetisch in evenwicht is.

1. (Voorwaardelijk) Als u meerdere ervaringen wilt uitsluiten, schakelt u de selectievakjes voor de gewenste ervaringen in en klikt u op **[!UICONTROL Exclude]** .

1. [ gebruik de Schatter van het Verkeer ](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/traffic-estimator.md#task_71AA6922AFD447EA8C5E610A78ABA714) om de haalbaarheid van uw testplan te testen.

1. Klik op **[!UICONTROL Next]** om naar de [!UICONTROL Targeting] -pagina te gaan.

   De **het richten** stap kijkt vertrouwd als u andere [!DNL Target] activiteitstypes hebt gebruikt. Hier kunt u een publiek selecteren en het percentage bezoekers opgeven dat elke ervaring ziet.

   Het stroomdiagram leidt u door de stappen om een publiek en zijn verkeerspercentage toe te wijzen, die de methode van de verkeerstoewijzing selecteren, en de verkeerstoewijzing voor elke ervaring in de activiteit specificeren.

1. (Voorwaardelijk) klik de **[!UICONTROL All Visitors]** controle om een ander publiek voor de activiteit te selecteren.

   De doelgroep van [!UICONTROL All Visitors] wordt ingesteld als de standaardgroep. Als u een ander publiek selecteert, wordt de naam van het publiek uiterst links weergegeven.

   Het juiste frame wordt weergegeven, waarmee u een publiek kunt toevoegen of verwijderen en het bezoekerspercentage voor de activiteit kunt toewijzen.

   1. Om het publiek te veranderen, klik het **[!UICONTROL Replace]pictogram** ( ![ vervangt pictogram ](/help/main/assets/icons/Retweet.svg)) in het juiste kader.
   1. In het [!UICONTROL Add Audience] dialoogvakje, [ selecteer het gewenste publiek ](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-audience.md), dan klik **[!UICONTROL Assign Audience]**.

      U kunt **klikken combineert Soorten publiek** om [ een publiek tot stand te brengen dat veelvoudige publiek ](/help/main/c-target/combining-multiple-audiences.md) combineert.

      Als u een nieuw publiek moet tot stand brengen dat niet reeds in [!UICONTROL Audience Library] is, klik **creeer Publiek**. Tijdens het [ creeer-publiek werkschema ](/help/main/c-target/c-audiences/audiences.md) kunt u van de volgende opties kiezen:

      * **[!UICONTROL Audience Library]**: Maak een publiek op aanvraag dat wordt opgeslagen in [!UICONTROL Audience Library] en dat opnieuw kan worden gebruikt in andere activiteiten.
      * **[!UICONTROL This activity only]**: Creeer een [ activiteit-specifiek publiek ](/help/main/c-target/creating-activity-only-audience.md) dat niet aan [!UICONTROL Audience Library] wordt bewaard en in de huidige activiteit slechts kan worden gebruikt.

   1. Klik op **[!UICONTROL Visitor Percentage]** in het rechterframe en kies het percentage gekwalificeerde bezoekers dat u de activiteit wilt invoeren.

   U kunt bijvoorbeeld items beperken tot 50% van alle bezoekers of 45% van uw &quot;Californische&quot; publiek.

1. [ herzie de testsamenvatting ](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/test-summary.md#reference_971AB225963A4DC18EEB5B0E20F0A4A7) en breng om het even welke gewenste veranderingen aan, dan klik **[!UICONTROL Next]**.

1. [ specificeer de doelstellingen en de montages ](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/goals-and-settings.md#reference_B25389FD6F3A4989801E740364B089CC) voor de test.

1. Klik op **[!UICONTROL Save and Close]** om de activiteit te maken.

## De video van de opleiding: Het creëren van Multivariate Tests (9:25) ![ badge van het Leerprogramma ](/help/main/assets/tutorial.png)

In deze video ziet u hoe u een multivariate test plant en maakt met behulp van de [!DNL Target] driestapige geleide workflow.

* Een multivariatietest definiëren en ontwerpen
* Een multivariatietest maken

>[!VIDEO](https://video.tv.adobe.com/v/17395)
