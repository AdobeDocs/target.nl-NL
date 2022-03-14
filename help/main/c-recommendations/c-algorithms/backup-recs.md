---
keywords: aanbeveling;back-up;back-up maken
description: Leer hoe u back-upaanbevelingen kunt gebruiken in Adobe [!DNL Target] Recommendations. De aanbeveling die niet genoeg geadviseerde punten heeft toont de resultaten van het reservealgoritme.
title: Hoe gebruik ik een back-upaanbeveling in Recommendations?
feature: Recommendations
exl-id: 070aa8ef-5691-4106-b5cf-45eb9f6f334c
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '513'
ht-degree: 0%

---

# ![PREMIUM](/help/main/assets/premium.png) Een back-upaanbeveling gebruiken

Als u de functie voor het aanbevelen van back-ups in Adobe Target gebruikt, wordt er geen standaardinhoud weergegeven als er onvoldoende aanbevolen items zijn. In plaats daarvan, tonen de aanbevelingen de resultaten van het reservealgoritme.

Als u geen reserveaanbeveling gebruikt, als een aanbeveling niet genoeg punten heeft om de vertoning te vullen, toont het systeem standaardinhoud aan de gebruiker.

>[!NOTE]
>
>Aanvullende informatie is opgenomen in het [Sectie Inhoud van de criteria Maken](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md#content) onderwerp, met inbegrip van een matrijs die de resultaten verklaart u wanneer het gebruiken van zult waarnemen [!UICONTROL Partial Design Rendering] en [!UICONTROL Show Backup Recommendations] opties samen of afzonderlijk.

De functie voor back-upaanbevelingen gebruikt altijd de items op de site die als bovenste worden weergegeven om de resterende sleuven in te vullen nadat de gegevens van het algoritme zijn gebruikt. Bijvoorbeeld, wordt uw malplaatje gevormd om vijf geadviseerde punten te tonen, en u gebruikt *Aankoopaffiniteiten* algoritme. U hebt echter slechts voldoende gegevens om twee van de vijf sleuven te vullen. De functie voor back-upaanbevelingen vult de andere drie punten met items die u het beste kunt bekijken.

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

Indien gedeeltelijke weergave van ontwerp inschakelen (zie [Inhoudsinstellingen](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md#content)) is niet ingeschakeld en de sjabloon wordt niet weergegeven. In plaats daarvan wordt de back-upaanbeveling of de standaardinhoud weergegeven.
