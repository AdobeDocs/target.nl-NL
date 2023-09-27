---
keywords: multivariëren;mvt;metriek;vastgestelde metriek;doel metrisch;activiteitenmontages;succes metrisch;omzetting;opbrengst;betrokkenheid
description: Leer hoe u metriek kunt opgeven in een [!DNL Adobe Target] [!UICONTROL Multivariate Test] activiteit om te bepalen wanneer een bezoek succesvol is, zoals [!UICONTROL Conversion], [!UICONTROL Revenue], en [!UICONTROL Engagement].
title: Hoe stel ik Goederen in een [!UICONTROL Multivariate Test] (MVT) Activiteit?
feature: Multivariate Tests
exl-id: 8530b3f1-5daa-4a03-a482-93b10eb23208
source-git-commit: 6c00224e814abb33cdf968a249bd36fb2e5ed2ed
workflow-type: tm+mt
source-wordcount: '321'
ht-degree: 0%

---

# Metriek instellen voor een [!UICONTROL Multivariate Test] activiteit

Metrische gegevens gebruiken in een [!DNL Adobe Target] [!UICONTROL Multivariate Test] bepalen wanneer een bezoek succesvol is.

Voor gedetailleerde informatie over succesmetriek, zie [Succeswaarden](/help/main/c-activities/r-success-metrics/success-metrics.md#reference_D011575C85DA48E989A244593D9B9924).

1. Geef het doel van de activiteit op.
1. Selecteer een [succesmetrisch](/help/main/c-activities/r-success-metrics/success-metrics.md#reference_D011575C85DA48E989A244593D9B9924)

   ![Lijst met metriek instellen](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/assets/mvt_metrics-list.png)

   De [!UICONTROL Select Metrics] De pagina bevat de succesmaatstaven die u voor uw activiteit kunt kiezen. De succeswaarden zijn verdeeld in de volgende categorieën:

   * [!UICONTROL Conversion]
   * [!UICONTROL Revenue]
   * [!UICONTROL Engagement]

   U kunt om het even welke vooraf gebouwde succesmetriek gebruiken, of een metrisch van het douanesucces tot stand brengen. U kunt metrisch succes als primaire metrisch ook merken. De rapporten en de kaarten van het Experience Cloud worden standaard om primaire metrisch te tonen, als één wordt geplaatst.

1. Geef de instellingen voor uw metriek op.

   De beschikbare instellingen zijn afhankelijk van de succesmaatstaf die u gebruikt.

   Indien ingeschakeld, wordt de [!UICONTROL Estimated Value of the Conversion] veld (niet beschikbaar voor de [!UICONTROL Page Score] metriek) biedt een waarde voor uw doel. Deze waarde schakelt [!DNL Target] een geraamde verhoging van de inkomsten te berekenen. Dit veld is facultatief, maar incrementele inkomsten voor elke metrische waarde zonder inkomsten kunnen niet worden berekend. Het gegevenstype is currency. Dit veld wordt progressief weergegeven nadat de gebruiker de actie aangeeft die is ondernomen om het doel te bereiken. Zie [Schatting van de opbrengst](/help/main/administrating-target/r-target-account-preferences/estimating-lift-in-revenue.md) voor meer informatie .

   De correcte configuratie van succesmetriek is kritiek om ervoor te zorgen u de gegevens krijgt u verwacht.

   Zie voor meer informatie [Succeswaarden](/help/main/c-activities/r-success-metrics/success-metrics.md#reference_D011575C85DA48E989A244593D9B9924)

1. (Optioneel) Voeg aanvullende metriek toe.
1. Klikken **[!UICONTROL Continue]** wanneer u klaar bent met het instellen van de metriek.

Wanneer u metrisch noemt of anders noemt, worden de volgende karakters niet toegestaan:

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

## Trainingsvideo: Activiteitenstatistieken (7:43) ![Zelfstudie-badge](/help/main/assets/tutorial.png)

Deze video bevat informatie over het werken met succesmetriek.

* Begrijp &quot;doel&quot;metriek
* Begrijpen en bouwen [!UICONTROL Conversion], [!UICONTROL Revenue], en [!UICONTROL Engagement] cijfers
* Een metrisch object voor klikken bijhouden maken

>[!VIDEO](https://video.tv.adobe.com/v/17380)
