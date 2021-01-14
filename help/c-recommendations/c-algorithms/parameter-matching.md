---
keywords: inclusion rules;inclusion criteria;recommendations;promotion;promotions;dynamic filtering;dynamic;parameter matching
description: Filter dynamisch in Adobe Target Recommendations door items (entiteiten) te vergelijken met een waarde in de aanvraag (API of mbox).
title: Filteren op parameterovereenkomst in dynamische-inclusieregels in Adobe Target Recommendations
feature: Recommendations
translation-type: tm+mt
source-git-commit: 7b86db4b45f93a3c6169caf81c2cd52236bb5a45
workflow-type: tm+mt
source-wordcount: '316'
ht-degree: 0%

---


# ![Overeenkomende ](/help/assets/premium.png) parameters PREMIUMP

Filter dynamisch door items (entiteiten) te vergelijken met een waarde in de aanvraag (API of mbox).

U kunt bijvoorbeeld alleen inhoud aanbevelen die overeenkomt met de pagina-parameter &#39;industrie&#39; of andere parameters, zoals apparaatafmetingen of geo-locatie, zoals in de volgende voorbeelden.

* Mbox-parameters voor schermbreedte en -hoogte kunnen worden gebruikt om mobiele bezoekers te bereiken en bieden alleen de aanbeveling voor mobiele apparaten en accessoires.
* Maak een regel met aanbevelingen die alleen de meest verkochte mobiele telefoons retourneert die overeenkomen met de schermhoogte van het mobiele apparaat dat de bezoeker gebruikt in de weergave van de pagina of deze overschrijdt.
* De regionale geolocatieparameters kunnen worden gebruikt om aanbevelingen voor hulpmiddelen tijdens de winter terug te keren. Sneeuwruimers en andere sneeuwbestrijdingsmiddelen kunnen worden aanbevolen voor bezoekers in gebieden waar het sneeuwt, maar niet voor bezoekers in gebieden waar het sneeuwt.

>[!NOTE]
>
>Als de activiteit vóór 31 oktober 2016 werd gecreeerd, zal zijn levering ontbreken als het de &quot;Aanpassing van de Parameter&quot;filter gebruikt. U kunt dit probleem als volgt oplossen:
>
>* Maak een nieuwe activiteit en voeg daar uw criteria aan toe.
>* Gebruik een criterium dat het filter &quot;Parameter Matching&quot; niet bevat.
>* Verwijder het filter &quot;Parameter Matching&quot; uit de criteria.


## Voorbeelden van overeenkomsten met parameters

[!UICONTROL Parameter Matching] kunt u inhoud aanbevelen die overeenkomt met de paginaparameters of de parameters van de bezoeker, zoals apparaatafmetingen of geo-locatie, zoals in het volgende voorbeeld:

[!DNL Recommendations] Kan parameterwaarden aanpassen die in de  [!DNL Target] aanroep worden verzonden. In deze instantie detecteert [!DNL Target] dat een bezoeker een mobiel apparaat gebruikt, op basis van de parameters voor schermhoogte en -breedte die zijn verzonden in de [!DNL Target]-aanroep, en worden alleen items aanbevolen die mobiele apparaten zijn.

Overweeg de volgende vraag van het voorbeeldDoel:

![Doeloproep](/help/c-recommendations/c-algorithms/assets/example-target-call-2.png)

Op de pagina die een bezoeker bekijkt, ziet hij of zij producten voor mobiele apparaten.

![Mobiele apparaten](/help/c-recommendations/c-algorithms/assets/phones.png)
