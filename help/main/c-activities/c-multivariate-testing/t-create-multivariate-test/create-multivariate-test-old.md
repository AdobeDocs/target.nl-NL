---
keywords: mvt;multivariate test;multivariate test creeert;multivariate test creeert;mvt creeert;mvt creeert;mvt hoe;multivariate test hoe
description: Leer hoe te om [!UICONTROL Visual Experience Composer] (VEC) in  [!DNL Adobe Target]  te gebruiken om a [!UICONTROL Multivariate Test] (MVT) tot stand te brengen.
title: Hoe maak ik een [!UICONTROL Multivariate Test] ?
feature: Multivariate Tests
exl-id: 7712b747-543a-4e19-b689-bea36c44805c
source-git-commit: 8f9c0ea65197fd639d463628e54db79db993c2da
workflow-type: tm+mt
source-wordcount: '504'
ht-degree: 0%

---

# Een multivariatietest maken

Met [!UICONTROL Visual Experience Composer] (VEC) in [!DNL Adobe Target] kunt u eenvoudig een [!UICONTROL Multivariate Test] -pagina maken en delen van de pagina binnen [!DNL Target] wijzigen.

Met de [!DNL Target] point-and-click-editor kunt u elke gewenste locatie kiezen en meerdere aanbiedingen toevoegen.

Voor [!UICONTROL Multivariate Test] (MVT) wordt eerst een rapport op de pagina weergegeven. Met andere woorden, de test wordt uitgevoerd op een specifieke URL, met de ervaringen u voor die pagina ontwerpt.

1. Klik op **[!UICONTROL Create Activity]** > **[!UICONTROL Multivariate Test]** .

   ![&#x200B; creeer Multivariate Test &#x200B;](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/assets/create-multivariate.png)

   >[!NOTE]
   >
   >Voor meer informatie over de diverse activiteitentypes beschikbaar in [!DNL Target] en hun verschillen, zie [&#x200B; Activiteiten &#x200B;](/help/main/c-activities/activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03). Zie [&#x200B; de types van Activiteit van het Doel &#x200B;](/help/main/c-activities/target-activities-guide.md) om u te helpen beslissen welk type van activiteit beste reeksen uw behoeften.

1. (Voorwaardelijk) Kies het leveringstype: [!UICONTROL Web] , [!UICONTROL Mobile] , [!UICONTROL Email] of [!UICONTROL Other/API] .

1. (Voorwaardelijk) als u a [&#x200B; Target Premium &#x200B;](/help/main/c-intro/intro.md#premium) klant bent, [&#x200B; kies een werkruimte &#x200B;](/help/main/administrating-target/c-user-management/property-channel/property-channel.md).

1. [&#x200B; specificeer URL &#x200B;](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/url.md#concept_C12E4A85FF3B4E518E3110F6CF1AF9C0) voor de pagina die u wilt testen, dan klikken **[!UICONTROL Next]**.

   >[!NOTE]
   >
   >Gebruik aan het begin een volledige URL, inclusief HTTP of HTTPS.

   Als er een bericht wordt weergegeven waarin u wordt gevraagd uw browser in te schakelen voor gemengde inhoud, volgt u de instructies in het bericht. Nadat u de browser hebt ingeschakeld voor gemengde inhoud, begint u opnieuw bij Stap 1.

   De lus [!UICONTROL Visual Experience Composer] wordt geopend.

1. Typ een naam voor de activiteit.

   {het gebied van de Naam van de Activiteit 0} ![](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/assets/activityname.png)

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

1. [&#x200B; creeer de aanbiedingen in elke plaats &#x200B;](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/add-offers.md#concept_DCE6B45C30F7419B8EC17AFDEE8D8AA6).

   ![&#x200B; geef de dialoogdoos van de Tekst/van HTML uit &#x200B;](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/assets/editoffers.png)

   U kunt de volgende soorten voorstellen toevoegen:

   * HTML
   * Afbeelding
   * Tekst

1. Klik **[!UICONTROL Preview]** aan [&#x200B; voorproef uw ervaringen &#x200B;](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/preview-experiences.md).

   ![&#x200B; Ervaringen van de Voorproef &#x200B;](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/assets/preview-mvt.png)

   U kunt elke ervaring bekijken en alle ervaringen uitsluiten die u niet in de test wilt opnemen. Als u een of meer ervaringen wilt uitsluiten, selecteert u de gewenste selectievakjes en klikt u op **[!UICONTROL Exclude]** .

   ![&#x200B; sluit ervaringen &#x200B;](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/assets/preview-mvt-exclude.png) uit

1. [&#x200B; gebruik de Schatter van het Verkeer &#x200B;](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/traffic-estimator.md#task_71AA6922AFD447EA8C5E610A78ABA714) om de haalbaarheid van uw testplan te testen.

   ![&#x200B; indicator van het Verkeer &#x200B;](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/assets/mvt-traffic-indicator.png)

   De volgende illustratie geeft aan dat de activiteit onvoldoende verkeer heeft.

   ![&#x200B; schatter beeld &#x200B;](assets/estimator.png)

   De volgende illustratie geeft aan dat de activiteit onvoldoende verkeer heeft.

   ![&#x200B; estimator2 beeld &#x200B;](assets/estimator2.png)

1. Klik op **[!UICONTROL Next]** om naar de [!UICONTROL Targeting] -pagina te gaan.

1. Kies het publiek en het percentage in aanmerking komende bezoekers dat u de activiteit wilt betreden.

   ![&#x200B; het richten pagina in activiteit MVT &#x200B;](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/assets/mvt_audperc.png)

   U kunt bijvoorbeeld items beperken tot 50% van alle bezoekers of 45% van uw &quot;Californische&quot; publiek.

   >[!NOTE]
   >
   >Naast het selecteren van een bestaand publiek kunt u meerdere soorten publiek combineren om een gecombineerd ad-hocpubliek te maken in plaats van een nieuw publiek te maken. Voor meer informatie, zie [&#x200B; Combinerend Veelvoudige Soorten publiek &#x200B;](/help/main/c-target/combining-multiple-audiences.md#concept_A7386F1EA4394BD2AB72399C225981E5).

1. [&#x200B; herzie de testsamenvatting &#x200B;](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/test-summary.md#reference_971AB225963A4DC18EEB5B0E20F0A4A7) en breng om het even welke gewenste veranderingen aan, dan klik **[!UICONTROL Next]**.

1. [&#x200B; specificeer de doelstellingen en de montages &#x200B;](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/goals-and-settings.md#reference_B25389FD6F3A4989801E740364B089CC) voor de test.

1. Klik op **[!UICONTROL Save and Close]** om de activiteit te maken.

## De video van de opleiding: Creërend Multivariate Tests (9 :25) ![&#x200B; badge van het Leerprogramma &#x200B;](/help/main/assets/tutorial.png)

In deze video ziet u hoe u een multivariate test plant en maakt met behulp van de [!DNL Target] driestapige geleide workflow.

* Een multivariatietest definiëren en ontwerpen
* Een multivariatietest maken

>[!VIDEO](https://video.tv.adobe.com/v/17395)
