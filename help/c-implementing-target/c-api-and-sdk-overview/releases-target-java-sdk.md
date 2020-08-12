---
keywords: at.js;sdk;release;updates;sdks;server side;serverside;server-side;java;java sdk
description: Opmerkingen bij de release met betrekking tot de Adobe Target Java SDK.
title: Opmerkingen bij de release met betrekking tot de Adobe Target Java SDK.
feature: null
topic: Standard
translation-type: tm+mt
source-git-commit: a51addc6155f2681f01f2329b25d72327de36701
workflow-type: tm+mt
source-wordcount: '314'
ht-degree: 0%

---


# Opmerkingen bij de release - Doel Java SDK

Opmerkingen bij de release met betrekking tot de [Target Java SDK](https://github.com/adobe/target-java-sdk).

Met de [!DNL Target] Java SDK kunt u [!DNL Target] server-side implementeren. Met deze Java SDK kunt u eenvoudig integreren [!DNL Target] met andere [!DNL Adobe Experience Cloud] oplossingen, zoals de [!DNL Adobe Experience Cloud Identity Service], [!DNL Adobe Analytics]en [!DNL Adobe Audience Manager].

De SDK van Java introduceert beste praktijken en verwijdert ingewikkeldheid wanneer het integreren met [!DNL Target] via onze levering API zodat uw techniekteams zich op bedrijfslogica kunnen concentreren.

Meer informatie over de doel-Java SDK vindt u op de Tech Blog - [Server-Side Optimization met de nieuwe Target Java SDK](https://medium.com/adobetech/server-side-optimization-with-the-new-target-java-sdk-421dc418a3f2).

## Versie 1.1.0 (16 december 2019)

In de volgende sectie vindt u meer informatie over versie 1.1.0 van de Target Java SDK:

### Toegevoegd

* Ondersteuning voor proxyconfig toegevoegd vanwege een open-bronbijdrage van @hisham-hassan.

## Versie 1.0.1 (11 november 2019)

In de volgende sectie vindt u meer informatie over versie 1.0.1 van de Target Java SDK:

### Vast

* Stuur een aanvullende gegevens-id in een doelaanvraag, zelfs als er geen bezoeker-API cookie aanwezig is.

## Versie 1.0.0 (31 oktober 2019)

De volgende secties verstrekken meer informatie over versie 1.0.0 van het Doel Java SDK:

### Toegevoegd

* [Ondersteuning voor versie 1 API](https://developers.adobetarget.com/api/delivery-api/) voor doelweergave, inclusief de voorkeuren voor het laden van pagina&#39;s en weergave.
   * Volledige steun voor het leveren van alle soorten aanbiedingen die in Visual Experience Composer (VEC) worden authored.
* Ondersteuning voor prefetching en meldingen die optimalisatie van de prestaties mogelijk maken door vooraf ingestelde inhoud in cache te plaatsen.
* Ondersteuning voor het optimaliseren van prestaties bij hybride [!DNL Target] integratie via `serverState`, wanneer [!DNL Target] deze zowel op de server als op de client wordt geïmplementeerd.
   * Wij introduceren het plaatsen genoemd `serverState` die ervaringen bevat die via server-kant worden teruggewonnen, zodat at.js v2.2+ geen extra servervraag zal maken om de ervaringen terug te winnen. Deze aanpak optimaliseert de prestaties bij het laden van pagina&#39;s.
* Open die op GitHub als [DoelJava SDK](https://github.com/adobe/target-java-sdk)wordt ingekocht.
* Validatie van API-methodeargumenten voor SDK.
* Toegevoegde README, steekproeven, en eenheidstests.
* Toegevoegde CvC, de richtlijnen van de Bijdrage, PR, en uitgiftesjablonen.

