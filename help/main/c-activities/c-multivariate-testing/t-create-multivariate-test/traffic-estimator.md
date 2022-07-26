---
keyword: traffic estimate;traffic estimator;estimate;traffic;confidence;statistical power;lift;bonferroni;conversion rate;visitors per day;duration
description: Leer hoe te om de schatter van het Verkeer te gebruiken die u laat weten of hebt u voldoende verkeer voor uw Adobe [!DNL Target] De multivariate activiteit van de Test om succesvol te zijn.
title: Hoeveel verkeer wordt vereist voor een Multivariate Test (MVT) activiteit?
feature: Multivariate Tests
exl-id: 2b32f4a7-b9b4-40bf-a17b-88225bc88787
source-git-commit: 293b2869957c2781be8272cfd0cc9f82d8e4f0f0
workflow-type: tm+mt
source-wordcount: '491'
ht-degree: 0%

---

# Schatting van het verkeer dat nodig is voor een geslaagde test

Omdat een multivariate test veelvoudige ervaringen vergelijkt, is het belangrijk om te weten hoeveel verkeer wordt vereist om betekenisvolle resultaten te verstrekken. De schatter van het Verkeer gebruikt statistieken over uw pagina en het aantal ervaringen die worden getest om de hoeveelheid verkeer en de testduur te schatten nodig om de test succesvol te maken.

De schatter van het Verkeer voorspelt de steekproefgrootte nodig om het volgende te verzekeren:

* 95% betrouwbaarheid

   Dit betekent dat de kans op het melden van een fout-positief als er geen echte lift is 5% is (100% - betrouwbaarheidsniveau).
* 80% statistisch vermogen

   Dit betekent dat de kans dat de test een ware lift van 25% of meer detecteert, 80% bedraagt.
* minimaal 25% betrouwbaar detecteerbare lift

   Doel berekent de hoeveelheid verkeer die vereist is om een kans van 80% te hebben om een ware lift van 25% of meer te ontdekken.

In de test wordt de Bonferroni-correctie gebruikt om meerdere vergelijkingen te corrigeren. Deze methode staat bekend om conservatief te zijn, die wordt uitgebalanceerd door een relatief groot minimum aan betrouwbaar waarneembare lift te handhaven.

De schatter van het Verkeer verstrekt ook terugkoppelt die u laat weten of u voldoende verkeer voor de test hebt u ontworpen om te slagen.

1. Klik in de Experience Composer op de knop **[!UICONTROL Traffic]** pictogram.

   De schatter van het Verkeer opent. U kunt op de knop **[!UICONTROL Traffic]** opnieuw om de schatter van het Verkeer te verbergen.

   ![afbeelding schatten als leeg](assets/estimatorempty.png)

1. Geef de gemiddelde conversiesnelheid, de geschatte bezoekers per dag en de testduur op.

   * [!UICONTROL Number of Content Combinations]: Automatisch berekend op basis van het aantal ervaringen dat wordt gemaakt als onderdeel van uw activiteit na eventuele uitsluitingen.
   * [!UICONTROL Typical Conversion Rate]: De omrekeningskoers wordt uitgedrukt als een percentage, op basis van uw schatting of gegevens uit het verleden van uw analysesysteem
   * [!UICONTROL Estimated Visitors Per Day]: Dit is het aantal bezoekers dat deze pagina waarschijnlijk zal bekijken op basis van de doelcriteria. Dit kan op uw analysegegevens worden gebaseerd.
   * [!UICONTROL Test Duration]: Het aantal dagen waarop de activiteit moet worden uitgevoerd.

   De schatter van het Verkeer gebruikt deze statistieken om te bepalen welke aanpassingen nodig zijn om een succesvolle test in werking te stellen.

   Vlak bij de bovenkant van de schatter van het Verkeer, worden de waarden u inging berekend en de resultaten worden getoond.

   ![ontoereikende afbeelding](assets/estimatorinsufficient.png)

   Terwijl u de getallen wijzigt, verandert de schatting. Als u bijvoorbeeld een groot aantal ervaringen test en uw conversiesnelheid en indrukken te laag zijn, toont de Verkeersschatting hoe lang de test moet duren om succesvol te zijn. Of, als uw verkeer laag is, zou de schatter van het Verkeer een lager aantal ervaringen kunnen voorstellen zodat kunt u de test het gewenste aantal dagen in werking stellen.

   Als u onvoldoende verkeer hebt, kunt u een van de volgende handelingen uitvoeren of beide handelingen uitvoeren:

   * Verminder het aantal combinaties aanbiedingen en het aantal plaatsen.
   * Verhoog de duur van de test.

   Pas de aantallen aan tot de schatter van het Verkeer zegt u voldoende verkeer hebt, dan ontwerp dienovereenkomstig uw test.

   ![afbeelding schatter](assets/estimatorok.png)
