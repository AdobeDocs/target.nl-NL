---
description: De mobiele SDK van Adobe neemt contact op met de doelserver om de inhoud samen met andere gegevenspunten op te halen en de gebruiker de juiste ervaring te laten zien.
title: Hoe werkt Doel in mobiele apps
feature: Implement Mobile
translation-type: tm+mt
source-git-commit: 48b94f967252f5ddb009597456edf0a43bc54ba6
workflow-type: tm+mt
source-wordcount: '195'
ht-degree: 0%

---


# Hoe werkt Doel in mobiele apps{#how-target-works-in-mobile-apps}

De mobiele SDK van Adobe neemt contact op met de doelserver om de inhoud samen met andere gegevenspunten op te halen en de gebruiker de juiste ervaring te laten zien.

## Doellocaties en succeswaarden {#section_A08AAB0ABA9C4568A5AFD4D27EF1CE74}

Een *doellocatie* wordt ook een mbox genoemd. Een geïdentificeerde locatie in de app is geschikt voor testen of personalisatie (bijvoorbeeld het welkomstbericht op het thuisscherm). Deze locaties worden tijdens het maken van de test geïdentificeerd.

Een *[succesmetrische](/help/c-activities/r-success-metrics/success-metrics.md#reference_D011575C85DA48E989A244593D9B9924)* is een actie die door de gebruiker wordt uitgevoerd die zich identificeert als een specifieke activiteit succesvol was (zoals het ondertekenen, het maken van een aankoop, het boeken van een kaartje, etc.).

![](assets/mobile-target-location.png)

* **Doellocatie:** de inhoud die onder de registratieknop wordt weergegeven.

   Deze gebruiker krijgt gratis verzending tot 18.00 uur aangeboden. Deze plaats kan over veelvoudige activiteiten van het Doel worden opnieuw gebruikt om tests A/B en verpersoonlijking in werking te stellen.

* **Metrisch succes:** de actie die door de gebruiker wordt uitgevoerd waar de gebruiker op de registratieknop tikt.

**Begrijp hoe het Doel in SDK werkt**

![](assets/how-target-mobile-works.png)

