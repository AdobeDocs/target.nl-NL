---
keyword: traffic estimate;traffic estimator;estimate;traffic;confidence;statistical power;lift;bonferroni;conversion rate;visitors per day;duration
description: Leer hoe te om de schatter van het Verkeer te gebruiken die u laat weten of hebt u voldoende verkeer voor uw  [!DNL Adobe Target] [!UICONTROL Multivariate Test] activiteit om te slagen.
title: Hoeveel verkeer is nodig voor een [!UICONTROL Multivariate Test] (MVT) activiteit?
feature: Multivariate Tests
exl-id: 2b32f4a7-b9b4-40bf-a17b-88225bc88787
source-git-commit: 8f9c0ea65197fd639d463628e54db79db993c2da
workflow-type: tm+mt
source-wordcount: '485'
ht-degree: 0%

---

# Het vereiste verkeer voor een geslaagde [!UICONTROL Multivariate Test] -activiteit schatten

Omdat een multivariate test veelvoudige ervaringen vergelijkt, is het belangrijk om te weten hoeveel verkeer wordt vereist om betekenisvolle resultaten te verstrekken. [!UICONTROL Traffic Estimator] gebruikt statistieken over uw pagina en het aantal ervaringen die worden getest om de hoeveelheid verkeer en de testduur te schatten nodig om de test succesvol te maken.

In [!UICONTROL Traffic Estimator] wordt de samplegrootte voorspeld die nodig is om het volgende te garanderen:

* 95% betrouwbaarheid. Deze statistiek betekent dat de kans op het melden van een fout-positief als er geen echte lift is, 5% is (100% - betrouwbaarheidsniveau).
* 80% statistische kracht. Dit betekent dat de waarschijnlijkheid van de test 80% bedraagt om een ware lift van 25% of meer te detecteren.
* 25% betrouwbaar waarneembare lift. [!DNL Target] berekent de hoeveelheid verkeer die vereist is om een kans van 80% te hebben om een ware lift van 25% of meer te detecteren.

De test gebruikt de Bonferroni-correctie om meerdere vergelijkingen te corrigeren. Deze methode staat bekend om conservatief te zijn, die wordt uitgebalanceerd door een relatief groot minimum aan betrouwbaar waarneembare lift te handhaven.

[!UICONTROL Traffic Estimator] verstrekt ook terugkoppelt die u laat weten of u voldoende verkeer voor de test hebt u ontworpen om succesvol te zijn.

1. Van de [!UICONTROL Experiences] pagina van [!UICONTROL Visual Experience Composer] in a [!UICONTROL Multivariate] activiteit, klik het **[!UICONTROL Traffic]** pictogram ( ![&#x200B; pictogram van de Schatter van het Verkeer &#x200B;](/help/main/assets/icons/Gauge2.svg)) in de hoogste linkerhoek van de [!UICONTROL Experiences] pagina.

   De lus [!UICONTROL Traffic Estimator] wordt geopend.

   ![&#x200B; het gebruikersinterface van de schatter van het Verkeer &#x200B;](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/assets/mvt-est.png)

   U kunt opnieuw op het pictogram klikken om de [!UICONTROL Traffic Estimator] te verbergen.

   Boven aan de [!UICONTROL Traffic Estimator] worden de ingevoerde waarden berekend en worden de resultaten weergegeven.

1. (Voorwaardelijk) Verstrek de typische omrekeningskoers, geschatte bezoekers per dag, en testduur.

   * **[!UICONTROL Number of Content Combinations]**: Wordt automatisch berekend op basis van het aantal ervaringen dat wordt gemaakt als onderdeel van uw activiteit na eventuele uitsluitingen.
   * **[!UICONTROL Typical Conversion Rate]**: De conversiesnelheid wordt uitgedrukt als een percentage, op basis van uw schatting of gegevens uit het verleden van uw analysesysteem.
   * **[!UICONTROL Estimated Visitors Per Day]**: Dit is het aantal bezoekers dat deze pagina waarschijnlijk zal weergeven op basis van de criteria voor doelwitten. Dit kan op uw analysegegevens worden gebaseerd.
   * **[!UICONTROL Test Duration]**: Het aantal dagen dat de activiteit moet worden uitgevoerd.

   [!UICONTROL Traffic Estimator] gebruikt deze statistieken om te bepalen welke aanpassingen nodig zijn om een succesvolle test in werking te stellen.

   Terwijl u de getallen wijzigt, verandert de schatting. Als u bijvoorbeeld een groot aantal ervaringen test en uw conversiesnelheid en -indrukkingen te laag zijn, toont [!UICONTROL Traffic Estimator] hoe lang de test moet duren om te slagen. Als uw verkeer laag is, kan [!UICONTROL Traffic Estimator] een lager aantal ervaringen voorstellen zodat u de test het gewenste aantal dagen kunt uitvoeren.

   Als u onvoldoende verkeer hebt, kunt u een van de volgende handelingen uitvoeren of beide handelingen uitvoeren:

   * Verminder het aantal combinaties aanbiedingen en het aantal plaatsen.
   * Verhoog de duur van de test.

   Pas de getallen aan totdat [!UICONTROL Traffic Estimator] aangeeft dat u voldoende verkeer hebt en stel vervolgens de test dienovereenkomstig in.
