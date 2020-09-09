---
keywords: recommendation;backup;back up
description: Als u de functie voor back-upaanbevelingen gebruikt, wordt er geen standaardinhoud weergegeven voor aanbevelingen die onvoldoende aanbevolen items bevatten. In plaats daarvan, tonen de aanbevelingen de resultaten van het reservealgoritme.
title: Een back-upaanbeveling gebruiken
feature: criteria
uuid: 2910a844-9dd6-4e69-8652-b2215fed1545
translation-type: tm+mt
source-git-commit: 92bce65559d46a4f22a3ecf249b9c754bbb0ea84
workflow-type: tm+mt
source-wordcount: '477'
ht-degree: 0%

---


# ![PREMIUM](/help/assets/premium.png) Gebruik een back-upaanbeveling{#use-a-backup-recommendation}

Als u de functie voor back-upaanbevelingen gebruikt, wordt er geen standaardinhoud weergegeven voor aanbevelingen die onvoldoende aanbevolen items bevatten. In plaats daarvan, tonen de aanbevelingen de resultaten van het reservealgoritme.

Als u geen reserveaanbeveling gebruikt, als een aanbeveling niet genoeg punten heeft om de vertoning te vullen, toont het systeem standaardinhoud aan de gebruiker.

De functie voor back-upaanbevelingen gebruikt altijd de items op de site die als bovenste worden weergegeven om de resterende sleuven in te vullen nadat de gegevens van het algoritme zijn gebruikt. Uw sjabloon is bijvoorbeeld geconfigureerd om vijf aanbevolen items weer te geven en u gebruikt het algoritme *Purchase Affinities* . U hebt echter slechts voldoende gegevens om twee van de vijf sleuven te vullen. De functie voor back-upaanbevelingen vult de andere drie punten met items die u het beste kunt bekijken.

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

Als Partial Design Rendering inschakelen (zie [Inhoudsinstellingen](/help/c-recommendations/c-algorithms/create-new-algorithm.md#content)) niet is ingeschakeld en de sjabloon niet wordt weergegeven, wordt in plaats daarvan de back-upaanbeveling of de standaardinhoud weergegeven.
