---
keywords: recommendation;backup;back up
description: Als u de functie voor het aanbevelen van back-ups in Adobe Target gebruikt, wordt er geen standaardinhoud weergegeven als er onvoldoende aanbevolen items zijn. In plaats daarvan, tonen de aanbevelingen de resultaten van het reservealgoritme.
title: Een back-upaanbeveling gebruiken in Adobe Target Recommendations
feature: criteria
translation-type: tm+mt
source-git-commit: 968d36d65016e51290f6bf754f69c91fd8f68405
workflow-type: tm+mt
source-wordcount: '517'
ht-degree: 0%

---


# ![Een ](/help/assets/premium.png) back-upaanbeveling gebruiken{#use-a-backup-recommendation}

Als u de functie voor het aanbevelen van back-ups in Adobe Target gebruikt, wordt er geen standaardinhoud weergegeven als er onvoldoende aanbevolen items zijn. In plaats daarvan, tonen de aanbevelingen de resultaten van het reservealgoritme.

Als u geen reserveaanbeveling gebruikt, als een aanbeveling niet genoeg punten heeft om de vertoning te vullen, toont het systeem standaardinhoud aan de gebruiker.

>[!NOTE]
>
>De extra informatie is inbegrepen in [de sectie van de Inhoud van Create criteria](/help/c-recommendations/c-algorithms/create-new-algorithm.md#content) onderwerp, met inbegrip van een matrijs die de resultaten verklaart u zult waarnemen wanneer het gebruiken van [!UICONTROL Partial Design Rendering] en [!UICONTROL Show Backup Recommendations] opties samen of afzonderlijk.

De functie voor back-upaanbevelingen gebruikt altijd de items op de site die als bovenste worden weergegeven om de resterende sleuven in te vullen nadat de gegevens van het algoritme zijn gebruikt. Bijvoorbeeld, wordt uw malplaatje gevormd om vijf geadviseerde punten te tonen, en u gebruikt het *algoritme van Aankoopaffiniteiten*. U hebt echter slechts voldoende gegevens om twee van de vijf sleuven te vullen. De functie voor back-upaanbevelingen vult de andere drie punten met items die u het beste kunt bekijken.

Back-upaanbevelingen worden willekeurig gekozen uit de 500 meest bekeken producten op de hele site. De gegevenstijdsperiode voor back-upaanbevelingen is één week.

De 500 meest bekeken resultaten worden opeenvolgend gerangschikt en dan verdeeld in emmers van 20. De emmers worden op volgorde weergegeven, maar de resultaten binnen elk emmertje worden willekeurig verdeeld en naar de pagina geretourneerd. Als gebruikers de pagina vernieuwen, krijgen ze nieuwe, gerandomiseerde resultaten te zien. Als het resultaat van de vereniging van de inzameling en de het filtreren regels kleiner is dan 20, zal het willekeurig uit de inzameling selecteren.

Dit het knippen proces betekent dat de reserveaanbevelingen in de volgende orde worden getoond:

1. De 20 meest bekeken items weergeven, gerandomiseerd en vervolgens
1. De volgende 20 meest bekeken items weergeven, gerandomiseerd en vervolgens
1. De volgende 20 meest bekeken items weergeven, gerandomiseerd,
1. enzovoort

Zonder het maken van back-upaanbevelingen zou het mogelijk zijn geweest om het 499e meest bekeken item te tonen, gevolgd door het 200e meest bekeken item, gevolgd door het 380e meest bekeken item, enzovoort. Het emmeringproces zorgt ervoor dat de meest bekeken punten eerst worden geadviseerd.

>[!NOTE]
>
>Als u uw items in catalogi groepeert, wordt de catalogus ook gebruikt voor de back-upaanbevelingen die voor elk algoritme in de aanbeveling worden gegenereerd. Daarom worden alleen de items in de catalogus opgenomen in de back-upaanbeveling.

Elk item dat door de algemene uitsluitingsregels wordt uitgesloten, wordt niet als een back-upaanbeveling gebruikt.

Back-upaanbevelingen zijn standaard ingeschakeld en u vult de extra sleuven in een sjabloon in met een willekeurige selectie van de meest populaire items op de site.

Duplicaten worden verwijderd uit batches met aanbevelingen.

Het gebruik van back-upaanbevelingen maakt doorgaans deel uit van de discussie met het implementatieteam tijdens de eerste installatie. Neem contact op met uw accountmanager als u de instelling voor de back-upaanbeveling na de implementatie wilt wijzigen.

Als Gedeeltelijke weergave van ontwerp inschakelen (zie [Inhoudsinstellingen](/help/c-recommendations/c-algorithms/create-new-algorithm.md#content)) niet is ingeschakeld en de sjabloon niet wordt weergegeven, wordt in plaats daarvan de back-upaanbeveling of standaardinhoud weergegeven.
