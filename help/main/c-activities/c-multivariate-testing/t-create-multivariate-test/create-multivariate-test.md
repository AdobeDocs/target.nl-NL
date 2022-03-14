---
keywords: mvt;multivariate test;multivariate test creeert;multivariate test creeert;mvt creeert;mvt creeert;mvt hoe;multivariate test hoe
description: Leer hoe te om Visual Experience Composer (VEC) in Adobe te gebruiken [!DNL Target] om een Multivariate Test (MVT) recht op een te creëren [!DNL Target]-enabled pagina.
title: Hoe maak ik een multivariate test?
feature: Multivariate Tests
exl-id: 7712b747-543a-4e19-b689-bea36c44805c
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '542'
ht-degree: 0%

---

# Een multivariatietest maken

De [!UICONTROL Visual Experience Composer] (VEC) in [!DNL Adobe Target] maakt het gemakkelijk om uw testrecht op een Doel-Toegelaten pagina tot stand te brengen en gedeelten van de pagina binnen te wijzigen [!DNL Target].

De [!DNL Target] Met de wijs-en-klik redacteur kunt u om het even welke plaats kiezen en veelvoudige aanbiedingen toevoegen.

De [!UICONTROL Multivariate Test] (MVT) neemt een pagina-eerste rapport. Met andere woorden, de test wordt uitgevoerd op een specifieke URL, met de ervaringen u voor die pagina ontwerpt.

1. Klik op **[!UICONTROL Create Activity]** > **[!UICONTROL Multivariate Test]**.

   ![Multivariatie testen maken](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/assets/create-multivariate.png)

   >[!NOTE]
   >
   >De beschikbare activiteitstypen zijn afhankelijk van uw Target-account. Sommige typen activiteiten worden mogelijk niet in de lijst weergegeven. Bijvoorbeeld: [!UICONTROL Automated Personalization] is een [Functie Doelpremium](/help/main/c-intro/intro.md#premium).
   >
   >Voor meer informatie over de verschillende soorten activiteiten die beschikbaar zijn in [!DNL Target] en hun verschillen, zie [Activiteiten](/help/main/c-activities/activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03). Zie [Typen doelactiviteiten](/help/main/c-activities/target-activities-guide.md) om u te helpen beslissen welke type activiteit beste reeksen uw behoeften.

1. Selecteren **[!UICONTROL Visual (Default)]**, indien nodig.

   ![Dialoogvenster Multivariatie testactiviteit maken](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/assets/create-mvt-dialog.png)

   >[!NOTE]
   >
   >Voor het oplossen van problemeninformatie over VEC, als u problemen hebt, zie [Het oplossen van problemen de Visuele Composer van de Ervaring](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/troubleshoot-composer.md).
   >
   >De [!UICONTROL Choose Workplace] optie in de voorgaande illustratie is een [Doelpremie](/help/main/c-intro/intro.md) gebruiken. Uw organisatie heeft een licentie voor Target Standard als deze optie niet wordt weergegeven.

1. (Voorwaardelijk) Als u een klant van de Premie van het Doel bent, [een werkruimte kiezen](/help/main/administrating-target/c-user-management/property-channel/property-channel.md).

1. [De URL opgeven](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/url.md#concept_C12E4A85FF3B4E518E3110F6CF1AF9C0) voor de pagina die u wilt testen, klikt u op **[!UICONTROL Next]**.

   >[!NOTE]
   >
   >Gebruik aan het begin een volledige URL, inclusief de HTTP- of HTTPS-URL.

   Als er een bericht wordt weergegeven waarin u wordt gevraagd uw browser in te schakelen voor gemengde inhoud, volgt u de instructies in het bericht. Nadat u de browser hebt ingeschakeld voor gemengde inhoud, begint u opnieuw bij Stap 1.

   Visual Experience Composer opent.

1. Typ een naam voor de activiteit.

   ![Veld voor naam van activiteit](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/assets/activityname.png)

   De naam van de activiteit mag niet met een van de volgende tekens beginnen:

   | Teken | Beschrijving |
   |--- |--- |
   | `=` | Gelijk aan |
   | `+` | Plus |
   | `-` | Min |
   | `@` | Bij ondertekenen |

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

   ![](assets/estimator.png)

   De volgende illustratie geeft aan dat de activiteit onvoldoende verkeer heeft.

   ![](assets/estimator2.png)

1. Klikken **[!UICONTROL Next]** aan [!UICONTROL Targeting] pagina.

1. Kies het publiek en het percentage in aanmerking komende bezoekers dat u de activiteit wilt betreden.

   ![Doelpagina in MVT-activiteit](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/assets/mvt_audperc.png)

   U kunt bijvoorbeeld items beperken tot 50% van alle bezoekers of 45% van uw &quot;Californische&quot; publiek.

   >[!NOTE]
   >
   >Naast het selecteren van een bestaand publiek kunt u meerdere soorten publiek combineren om een gecombineerd ad-hocpubliek te maken in plaats van een nieuw publiek te maken. Zie voor meer informatie [Meerdere soorten publiek combineren](/help/main/c-target/combining-multiple-audiences.md#concept_A7386F1EA4394BD2AB72399C225981E5).

1. [De testsamenvatting bekijken](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/test-summary.md#reference_971AB225963A4DC18EEB5B0E20F0A4A7) en breng de gewenste wijzigingen aan. Klik vervolgens op **[!UICONTROL Next]**.

1. [Geef de doelen en instellingen op](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/goals-and-settings.md#reference_B25389FD6F3A4989801E740364B089CC) voor de test.

1. Klikken **[!UICONTROL Save and Close]** om de activiteit te maken.

## Trainingsvideo: Multivariate tests maken (9:25) ![Zelfstudie-badge](/help/main/assets/tutorial.png)

In deze video ziet u hoe u een multivariate test plant en maakt met behulp van de driestapige workflow met instructies voor het doel.

* Een multivariatietest definiëren en ontwerpen
* Een multivariatietest maken

>[!VIDEO](https://video.tv.adobe.com/v/17395)
