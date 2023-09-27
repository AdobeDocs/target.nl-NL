---
keywords: mvt;multivariate test;multivariate test creeert;multivariate test creeert;mvt creeert;mvt creeert;mvt hoe;multivariate test hoe
description: Leer hoe u de [!UICONTROL Visual Experience Composer] (VEC) in [!DNL Adobe Target] om een [!UICONTROL Multivariate Test] (MVT).
title: Hoe maak ik een [!UICONTROL Multivariate Test]?
feature: Multivariate Tests
exl-id: 7712b747-543a-4e19-b689-bea36c44805c
source-git-commit: 7853d8c5934e40d1026e067dfa413f520ecba931
workflow-type: tm+mt
source-wordcount: '500'
ht-degree: 0%

---

# Een multivariatietest maken

De [!UICONTROL Visual Experience Composer] (VEC) in [!DNL Adobe Target] maakt het gemakkelijk om een [!UICONTROL Multivariate Test] en delen van de pagina in [!DNL Target].

De [!DNL Target] Met de wijs-en-klik redacteur kunt u om het even welke plaats kiezen en veelvoudige aanbiedingen toevoegen.

De [!UICONTROL Multivariate Test] (MVT) neemt een pagina-eerste rapport. Met andere woorden, de test wordt uitgevoerd op een specifieke URL, met de ervaringen u voor die pagina ontwerpt.

1. Klik op **[!UICONTROL Create Activity]** > **[!UICONTROL Multivariate Test]**.

   ![Multivariatie testen maken](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/assets/create-multivariate.png)

   >[!NOTE]
   >
   >Voor meer informatie over de verschillende activiteitstypen die beschikbaar zijn in [!DNL Target] en hun verschillen, zie [Activiteiten](/help/main/c-activities/activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03). Zie [Typen doelactiviteiten](/help/main/c-activities/target-activities-guide.md) om u te helpen beslissen welke type activiteit beste reeksen uw behoeften.

1. (Voorwaardelijk) Kies het leveringstype: [!UICONTROL Web], [!UICONTROL Mobile], [!UICONTROL Email], of [!UICONTROL Other/API].

1. (Voorwaardelijk) Als u een [Doelpremie](/help/main/c-intro/intro.md#premium) klant, [een werkruimte kiezen](/help/main/administrating-target/c-user-management/property-channel/property-channel.md).

1. [De URL opgeven](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/url.md#concept_C12E4A85FF3B4E518E3110F6CF1AF9C0) voor de pagina die u wilt testen, klikt u op **[!UICONTROL Next]**.

   >[!NOTE]
   >
   >Gebruik aan het begin een volledige URL, inclusief HTTP of HTTPS.

   Als er een bericht wordt weergegeven waarin u wordt gevraagd uw browser in te schakelen voor gemengde inhoud, volgt u de instructies in het bericht. Nadat u de browser hebt ingeschakeld voor gemengde inhoud, begint u opnieuw bij Stap 1.

   De [!UICONTROL Visual Experience Composer] wordt geopend.

1. Typ een naam voor de activiteit.

   ![Veld voor naam van activiteit](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/assets/activityname.png)

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

1. [Maak op elke locatie de aanbiedingen](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/add-offers.md#concept_DCE6B45C30F7419B8EC17AFDEE8D8AA6).

   ![Dialoogvenster Tekst/HTML bewerken](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/assets/editoffers.png)

   U kunt de volgende soorten voorstellen toevoegen:

   * HTML
   * Afbeelding
   * Tekst

1. Klikken **[!UICONTROL Preview]** tot [een voorbeeld van je ervaringen bekijken](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/preview-experiences.md).

   ![Voorvertoning](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/assets/preview-mvt.png)

   U kunt elke ervaring bekijken en alle ervaringen uitsluiten die u niet in de test wilt opnemen. Als u een of meer ervaringen wilt uitsluiten, selecteert u de gewenste selectievakjes en klikt u op **[!UICONTROL Exclude]** .

   ![Ervaringen uitsluiten](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/assets/preview-mvt-exclude.png)

1. [De schatter van het Verkeer gebruiken](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/traffic-estimator.md#task_71AA6922AFD447EA8C5E610A78ABA714) om de haalbaarheid van uw testplan te testen.

   ![Verkeersindicator](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/assets/mvt-traffic-indicator.png)

   De volgende illustratie geeft aan dat de activiteit onvoldoende verkeer heeft.

   ![afbeelding schatten](assets/estimator.png)

   De volgende illustratie geeft aan dat de activiteit onvoldoende verkeer heeft.

   ![afbeelding voor schatting2](assets/estimator2.png)

1. Klikken **[!UICONTROL Next]** aan de [!UICONTROL Targeting] pagina.

1. Kies het publiek en het percentage in aanmerking komende bezoekers dat u de activiteit wilt betreden.

   ![Doelpagina in MVT-activiteit](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/assets/mvt_audperc.png)

   U kunt bijvoorbeeld items beperken tot 50% van alle bezoekers of 45% van uw &quot;Californische&quot; publiek.

   >[!NOTE]
   >
   >Naast het selecteren van een bestaand publiek kunt u meerdere soorten publiek combineren om een gecombineerd ad-hocpubliek te maken in plaats van een nieuw publiek te maken. Zie voor meer informatie [Meerdere soorten publiek combineren](/help/main/c-target/combining-multiple-audiences.md#concept_A7386F1EA4394BD2AB72399C225981E5).

1. [De testsamenvatting bekijken](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/test-summary.md#reference_971AB225963A4DC18EEB5B0E20F0A4A7) en breng de gewenste wijzigingen aan. Klik vervolgens op **[!UICONTROL Next]**.

1. [Geef de doelen en instellingen op](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/goals-and-settings.md#reference_B25389FD6F3A4989801E740364B089CC) voor de test.

1. Klikken **[!UICONTROL Save and Close]** om de activiteit te maken.

## Trainingsvideo: Multivariate Tests maken (9:25) ![Zelfstudie-badge](/help/main/assets/tutorial.png)

In deze video ziet u hoe u een multivariërende test plant en maakt met de [!DNL Target] driestapsgerichte workflow.

* Een multivariatietest definiëren en ontwerpen
* Een multivariatietest maken

>[!VIDEO](https://video.tv.adobe.com/v/17395)
