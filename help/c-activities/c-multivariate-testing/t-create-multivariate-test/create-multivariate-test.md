---
keywords: mvt;multivariate test;multivariate test create;multivariate test creating;mvt create;mvt creating;mvt how;multivariate test how
description: Met Visual Experience Composer (VEC) in Adobe Target kunt u gemakkelijk een Multivariate Test (MVT) maken op een pagina die geschikt is voor Doel en delen van de pagina binnen Doel wijzigen.
title: Een multivariatietest maken
feature: mvt
uuid: 876441bd-d841-4974-b1ec-3ad7cb6ef3ee
translation-type: tm+mt
source-git-commit: 8d0faeb83e7fe854dcf99c89081fb656cf16c4c0
workflow-type: tm+mt
source-wordcount: '537'
ht-degree: 0%

---


# Een multivariatietest maken{#create-a-multivariate-test}

Met de insteekmodule [!UICONTROL Visual Experience Composer] (VEC) [!DNL Target] kunt u eenvoudig uw testrecht maken op een pagina die geschikt is voor Doel en delen van de pagina in de pagina wijzigen [!DNL Target].

Met de wijs-en-klikeditor van het doel kunt u elke gewenste locatie kiezen en meerdere aanbiedingen toevoegen.

De [!UICONTROL Multivariate Test] (MVT) neemt een pagina-eerste rapport. Met andere woorden, de test wordt uitgevoerd op een specifieke URL, met de ervaringen u voor die pagina ontwerpt.

1. Klik op **[!UICONTROL Create Activity]** > **[!UICONTROL Multivariate Test]**.

   ![Multivariatie testen maken](/help/c-activities/c-multivariate-testing/t-create-multivariate-test/assets/create-multivariate.png)

   >[!NOTE]
   >
   >De beschikbare activiteitstypen zijn afhankelijk van uw Target-account. Sommige typen activiteiten worden mogelijk niet in de lijst weergegeven. Bijvoorbeeld, [!UICONTROL Automated Personalization] is een eigenschap [van de Premie van het](/help/c-intro/intro.md#premium)Doel.
   >
   >Zie [!DNL Target] Activiteiten [voor meer informatie over de verschillende soorten activiteiten die beschikbaar zijn in](../../../c-activities/activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03)en hun verschillen. Zie [Doelactiviteitstypen](/help/c-activities/target-activities-guide.md) om u te helpen bepalen welk type activiteit het beste geschikt is voor uw behoeften.

1. Selecteer **[!UICONTROL Visual (Default)]** indien nodig.

   ![Dialoogvenster Multivariatie testactiviteit maken](/help/c-activities/c-multivariate-testing/t-create-multivariate-test/assets/create-mvt-dialog.png)

   >[!NOTE]
   >
   >Voor het oplossen van problemeninformatie over VEC, als u problemen hebt, zie het Oplossen van [problemen de Visuele Composer](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/troubleshoot-composer.md)van de Ervaring.
   >
   >De [!UICONTROL Choose Workplace] optie in de voorgaande illustratie is een [doelpremiumfunctie](/help/c-intro/intro.md) . Uw organisatie heeft een licentie voor Target Standard als deze optie niet wordt weergegeven.

1. (Voorwaardelijk) Als u een klant van de Premium van het Doel bent, [kies een werkruimte](/help/administrating-target/c-user-management/property-channel/property-channel.md).

1. [Geef de URL](../../../c-activities/c-multivariate-testing/t-create-multivariate-test/url.md#concept_C12E4A85FF3B4E518E3110F6CF1AF9C0) op voor de pagina die u wilt testen en klik op **[!UICONTROL Next]**.

   >[!NOTE]
   >
   >Gebruik aan het begin een volledige URL, inclusief de HTTP- of HTTPS-URL.

   Als er een bericht wordt weergegeven waarin u wordt gevraagd uw browser in te schakelen voor gemengde inhoud, volgt u de instructies in het bericht. Nadat u de browser hebt ingeschakeld voor gemengde inhoud, begint u opnieuw bij Stap 1.

   Visual Experience Composer opent.

1. Typ een naam voor de activiteit.

   ![Veld voor naam van activiteit](/help/c-activities/c-multivariate-testing/t-create-multivariate-test/assets/activityname.png)

   De volgende tekens zijn niet toegestaan in een naam van een activiteit:

   | Teken | Beschrijving |
   |--- |--- |
   | / | slash |
   | ? | Vraagteken |
   | # | Nummerteken |
   | : | Colon |
   | = | Gelijk aan |
   | + | Plus |
   | - | Min |
   | @ | Bij ondertekenen |

1. [Maak de voorstellen op elke locatie](../../../c-activities/c-multivariate-testing/t-create-multivariate-test/add-offers.md#concept_DCE6B45C30F7419B8EC17AFDEE8D8AA6).

   ![Dialoogvenster Tekst/HTML bewerken](/help/c-activities/c-multivariate-testing/t-create-multivariate-test/assets/editoffers.png)

   U kunt de volgende soorten voorstellen toevoegen:

   * HTML
   * Afbeelding
   * Tekst

1. Klik **[!UICONTROL Preview]** om een [voorvertoning van uw ervaringen](/help/c-activities/c-multivariate-testing/t-create-multivariate-test/preview-experiences.md)weer te geven.

   ![Voorvertoning](/help/c-activities/c-multivariate-testing/t-create-multivariate-test/assets/preview-mvt.png)

   U kunt elke ervaring bekijken en alle ervaringen uitsluiten die u niet in de test wilt opnemen. Als u een of meer ervaringen wilt uitsluiten, selecteert u de gewenste selectievakjes en klikt u op **[!UICONTROL Exclude]** .

   ![Ervaringen uitsluiten](/help/c-activities/c-multivariate-testing/t-create-multivariate-test/assets/preview-mvt-exclude.png)

1. [Gebruik de schatter](../../../c-activities/c-multivariate-testing/t-create-multivariate-test/traffic-estimator.md#task_71AA6922AFD447EA8C5E610A78ABA714) van het Verkeer om de haalbaarheid van uw testplan te testen.

   ![Verkeersindicator](/help/c-activities/c-multivariate-testing/t-create-multivariate-test/assets/mvt-traffic-indicator.png)

   De volgende illustratie geeft aan dat de activiteit onvoldoende verkeer heeft.

   ![](assets/estimator.png)

   De volgende illustratie geeft aan dat de activiteit onvoldoende verkeer heeft.

   ![](assets/estimator2.png)

1. Klik **[!UICONTROL Next]** om naar de [!UICONTROL Targeting] pagina te gaan.

1. Kies het publiek en het percentage in aanmerking komende bezoekers dat u de activiteit wilt betreden.

   ![Doelpagina in MVT-activiteit](/help/c-activities/c-multivariate-testing/t-create-multivariate-test/assets/mvt_audperc.png)

   U kunt bijvoorbeeld items beperken tot 50% van alle bezoekers of 45% van uw &quot;Californische&quot; publiek.

   >[!NOTE]
   >
   >Naast het selecteren van een bestaand publiek kunt u meerdere soorten publiek combineren om een gecombineerd ad-hocpubliek te maken in plaats van een nieuw publiek te maken. Zie Meerdere soorten publiek [combineren voor meer informatie](../../../c-target/combining-multiple-audiences.md#concept_A7386F1EA4394BD2AB72399C225981E5).

1. [Herzie de testsamenvatting](../../../c-activities/c-multivariate-testing/t-create-multivariate-test/test-summary.md#reference_971AB225963A4DC18EEB5B0E20F0A4A7) en breng om het even welke gewenste veranderingen aan, dan klik **[!UICONTROL Next]**.

1. [Geef de doelen en instellingen](../../../c-activities/c-multivariate-testing/t-create-multivariate-test/goals-and-settings.md#reference_B25389FD6F3A4989801E740364B089CC) voor de test op.

1. Klik **[!UICONTROL Save and Close]** om de activiteit tot stand te brengen.

## Trainingsvideo: Zelfstudie-badge voor meerdere ![tests maken (9:25)](/help/assets/tutorial.png)

In deze video ziet u hoe u een multivariate test plant en maakt met behulp van de driestapige workflow met instructies voor het doel.

* Een multivariatietest definiëren en ontwerpen
* Een multivariatietest maken

>[!VIDEO](https://video.tv.adobe.com/v/17395)
