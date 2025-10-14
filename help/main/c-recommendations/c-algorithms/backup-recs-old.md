---
keywords: aanbeveling;back-up;back-up maken
description: Leer hoe te om reserveaanbevelingen in Adobe  [!DNL Target]  Aanbevelingen te gebruiken. De aanbeveling die niet genoeg geadviseerde punten heeft toont de resultaten van het reservealgoritme.
title: Hoe gebruik ik een back-upaanbeveling in aanbevelingen?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=nl-NL#premium newtab=true" tooltip="Kijk wat er in Target Premium is opgenomen."
feature: Recommendations
exl-id: 070aa8ef-5691-4106-b5cf-45eb9f6f334c
source-git-commit: 02ffe8da6cdf96039218656b9690fa719a77910c
workflow-type: tm+mt
source-wordcount: '527'
ht-degree: 0%

---

# Een back-upaanbeveling gebruiken

Als u de functie voor het aanbevelen van back-ups in [!DNL Adobe Target] gebruikt, wordt bij elke aanbeveling die niet genoeg aanbevolen items bevat, geen standaardinhoud weergegeven. In plaats daarvan geven de aanbevelingen de resultaten van het back-upalgoritme weer.

Als u geen reserveaanbeveling gebruikt, als een aanbeveling niet genoeg punten heeft om de vertoning te vullen, toont het systeem standaardinhoud aan de gebruiker.

>[!NOTE]
>
>De extra informatie is inbegrepen in de [&#x200B; sectie van de Inhoud van Create criteria &#x200B;](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md#content) onderwerp, met inbegrip van een matrijs die de resultaten verklaart u wanneer het gebruiken van [!UICONTROL Partial Design Rendering] en [!UICONTROL Show Backup Recommendations] opties samen of afzonderlijk zult waarnemen.

De functie voor back-upaanbevelingen gebruikt altijd de items op de site die als bovenste worden weergegeven om de resterende sleuven in te vullen nadat de gegevens van het algoritme zijn gebruikt. Bijvoorbeeld, wordt uw malplaatje gevormd om vijf geadviseerde punten te tonen, en u gebruikt het *algoritme van de Aankoopaffiniteiten*. U hebt echter slechts voldoende gegevens om twee van de vijf sleuven te vullen. De functie voor back-upaanbevelingen vult de andere drie punten met items die u het beste kunt bekijken.

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

Als Gedeeltelijke Teruggeven van het Ontwerp toelaat (zie [&#x200B; Montages van de Inhoud &#x200B;](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md#content)) niet wordt toegelaten en het malplaatje niet toont, dan of wordt de reserveaanbeveling of standaardinhoud in plaats daarvan getoond.
