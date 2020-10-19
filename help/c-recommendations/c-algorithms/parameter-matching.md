---
keywords: inclusion rules;inclusion criteria;recommendations;promotion;promotions;dynamic filtering;dynamic;parameter matching
description: Filter dynamisch in Adobe Target Recommendations door items (entiteiten) te vergelijken met een waarde in de aanvraag (API of mbox).
title: Filteren op parameterovereenkomst in dynamische-inclusieregels in Adobe Target Recommendations
feature: criteria
translation-type: tm+mt
source-git-commit: b51c980d8e7db3ee574350a04f9056fe5b00a703
workflow-type: tm+mt
source-wordcount: '218'
ht-degree: 0%

---


# ![PREMIUM](/help/assets/premium.png) -parameterovereenkomst

Filter dynamisch door items (entiteiten) te vergelijken met een waarde in de aanvraag (API of mbox).

U kunt bijvoorbeeld alleen inhoud aanbevelen die overeenkomt met de pagina-parameter &#39;industrie&#39; of andere parameters, zoals apparaatafmetingen of geo-locatie, zoals in de volgende voorbeelden.

* Mbox-parameters voor schermbreedte en -hoogte kunnen worden gebruikt om mobiele bezoekers te bereiken en bieden alleen de aanbeveling voor mobiele apparaten en accessoires.
* De regionale geolocatieparameters kunnen worden gebruikt om aanbevelingen voor hulpmiddelen tijdens de winter terug te keren. Sneeuwruimers en andere sneeuwbestrijdingsmiddelen kunnen worden aanbevolen voor bezoekers in gebieden waar het sneeuwt, maar niet voor bezoekers in gebieden waar het sneeuwt.

>[!NOTE]
>
>Als de activiteit vóór 31 oktober 2016 werd gecreeerd, zal zijn levering ontbreken als het de &quot;Aanpassing van de Parameter&quot;filter gebruikt. U kunt dit probleem als volgt oplossen:
>
>* Maak een nieuwe activiteit en voeg daar uw criteria aan toe.
>* Gebruik een criterium dat het filter &quot;Parameter Matching&quot; niet bevat.
>* Verwijder het filter &quot;Parameter Matching&quot; uit de criteria.


Beschikbare operatoren:

* equals
* is niet gelijk aan
* contains
* bevat niet
* begint met
* eindigt met
* is groter dan of gelijk aan
* is kleiner dan of gelijk aan
* is tussen