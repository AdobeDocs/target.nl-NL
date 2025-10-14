---
keyword: traffic estimate;traffic estimator;estimate;traffic;confidence;statistical power;lift;bonferroni;conversion rate;visitors per day;duration
description: Leer hoe te om de schatter van het Verkeer te gebruiken die u laat weten of hebt u voldoende verkeer voor uw  [!DNL Adobe Target] [!UICONTROL Multivariate Test] activiteit om te slagen.
title: Hoeveel verkeer is nodig voor een [!UICONTROL Multivariate Test] (MVT) activiteit?
feature: Multivariate Tests
exl-id: 2b32f4a7-b9b4-40bf-a17b-88225bc88787
source-git-commit: 8f9c0ea65197fd639d463628e54db79db993c2da
workflow-type: tm+mt
source-wordcount: '489'
ht-degree: 0%

---

# Het vereiste verkeer voor een geslaagde [!UICONTROL Multivariate Test] -activiteit schatten

Omdat een multivariate test veelvoudige ervaringen vergelijkt, is het belangrijk om te weten hoeveel verkeer wordt vereist om betekenisvolle resultaten te verstrekken. De schatter van het Verkeer gebruikt statistieken over uw pagina en het aantal ervaringen die worden getest om de hoeveelheid verkeer en de testduur te schatten nodig om de test succesvol te maken.

De schatter van het Verkeer voorspelt de steekproefgrootte nodig om het volgende te verzekeren:

* 95% betrouwbaarheid. Deze statistiek betekent dat de kans op het melden van een fout-positief als er geen echte lift is, 5% is (100% - betrouwbaarheidsniveau).
* 80% statistische kracht. Dit betekent dat de waarschijnlijkheid van de test 80% bedraagt om een ware lift van 25% of meer te detecteren.
* 25% betrouwbaar waarneembare lift. [!DNL Target] berekent de hoeveelheid verkeer die vereist is om een kans van 80% te hebben om een ware lift van 25% of meer te detecteren.

De test gebruikt de Bonferroni-correctie om meerdere vergelijkingen te corrigeren. Deze methode staat bekend om conservatief te zijn, die wordt uitgebalanceerd door een relatief groot minimum aan betrouwbaar waarneembare lift te handhaven.

De schatter van het Verkeer verstrekt ook terugkoppelt die u laat weten of u voldoende verkeer voor de test hebt u ontworpen om te slagen.

1. Klik in het [!UICONTROL Visual Experience Composer] op het pictogram **[!UICONTROL Traffic]** .

   De schatter van het Verkeer opent. U kunt nogmaals op het pictogram **[!UICONTROL Traffic]** klikken om de verkeersschatting te verbergen.

   ![&#x200B; schatmatorempty beeld &#x200B;](assets/estimatorempty.png)

1. Geef de gemiddelde conversiesnelheid, de geschatte bezoekers per dag en de testduur op.

   * **[!UICONTROL Number of Content Combinations]**: Wordt automatisch berekend op basis van het aantal ervaringen dat wordt gemaakt als onderdeel van uw activiteit na eventuele uitsluitingen.
   * **[!UICONTROL Typical Conversion Rate]**: De conversiesnelheid wordt uitgedrukt als een percentage, op basis van uw schatting of gegevens uit het verleden van uw analysesysteem.
   * **[!UICONTROL Estimated Visitors Per Day]**: Dit is het aantal bezoekers dat deze pagina waarschijnlijk zal weergeven op basis van de criteria voor doelwitten. Dit kan op uw analysegegevens worden gebaseerd.
   * **[!UICONTROL Test Duration]**: Het aantal dagen dat de activiteit moet worden uitgevoerd.

   De schatter van het Verkeer gebruikt deze statistieken om te bepalen welke aanpassingen nodig zijn om een succesvolle test in werking te stellen.

   Boven aan de Verkeersschatting worden de ingevoerde waarden berekend en worden de resultaten weergegeven.

   ![&#x200B; schatten ontoereikende beeld &#x200B;](assets/estimatorinsufficient.png)

   Terwijl u de getallen wijzigt, verandert de schatting. Bijvoorbeeld, als u vele ervaringen test en uw omzettingspercentage en de beelden te laag zijn, toont de Schatter van het Verkeer hoe lang de test moet lopen om succesvol te zijn. Of, als uw verkeer laag is, zou de schatter van het Verkeer een lager aantal ervaringen kunnen voorstellen zodat kunt u de test het gewenste aantal dagen in werking stellen.

   Als u onvoldoende verkeer hebt, kunt u een van de volgende handelingen uitvoeren of beide handelingen uitvoeren:

   * Verminder het aantal combinaties aanbiedingen en het aantal plaatsen.
   * Verhoog de duur van de test.

   Pas de aantallen aan tot de schatter van het Verkeer zegt u voldoende verkeer hebt, dan ontwerp dienovereenkomstig uw test.

   ![&#x200B; schatter beeld &#x200B;](assets/estimatorok.png)
