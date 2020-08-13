---
description: De mobiele SDK van Adobe neemt contact op met de doelserver om de inhoud samen met andere gegevenspunten op te halen en de gebruiker de juiste ervaring te laten zien.
title: Hoe Target werkt in mobiele apps
feature: mobile implementation
uuid: 8b302292-2cc0-46b9-b29c-088006721c7f
translation-type: tm+mt
source-git-commit: e203dc94e9bb34c4090f5795cbf73869808ada88
workflow-type: tm+mt
source-wordcount: '195'
ht-degree: 0%

---


# Hoe Target werkt in mobiele apps{#how-target-works-in-mobile-apps}

De mobiele SDK van Adobe neemt contact op met de doelserver om de inhoud samen met andere gegevenspunten op te halen en de gebruiker de juiste ervaring te laten zien.

## Doellocaties en succeswaarden {#section_A08AAB0ABA9C4568A5AFD4D27EF1CE74}

Een *doellocatie* wordt ook mbox genoemd. Een geïdentificeerde locatie in de app is geschikt voor testen of personalisatie (bijvoorbeeld het welkomstbericht op het thuisscherm). Deze locaties worden tijdens het maken van de test geïdentificeerd.

Een *[succesmetrische](../c-activities/r-success-metrics/success-metrics.md#reference_D011575C85DA48E989A244593D9B9924)* actie is een actie die door de gebruiker wordt uitgevoerd die zich identificeert als een specifieke activiteit succesvol was (zoals het ondertekenen, het maken van een aankoop, het boeken van een kaartje, etc.).

![](assets/mobile-target-location.png)

* **Doellocatie:** De inhoud die onder de registratieknop wordt weergegeven.

   Deze gebruiker krijgt gratis verzending tot 18.00 uur aangeboden. Deze plaats kan over veelvoudige activiteiten van het Doel worden opnieuw gebruikt om tests A/B en verpersoonlijking in werking te stellen.

* **Metrisch resultaat:** De actie die wordt uitgevoerd door de gebruiker waar de gebruiker op de registratieknop tikt.

**Begrijp hoe het Doel in SDK werkt**

![](assets/how-target-mobile-works.png)

