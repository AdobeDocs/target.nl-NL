---
keywords: server side;server-side;api;sdk;node.js;nodejs;node js;recommendations api;api:apis
description: Informatie over Adobe Target API's voor levering aan de server, Node.js SDK en Target Recommendations API's.
title: Informatie over Adobe Target API's voor levering aan de server, Node.js SDK en Target Recommendations API's.
feature: server-side
topic: Recommendations
uuid: 21d321c7-3da4-44a2-a04f-1807cc2a893b
translation-type: tm+mt
source-git-commit: e203dc94e9bb34c4090f5795cbf73869808ada88
workflow-type: tm+mt
source-wordcount: '687'
ht-degree: 0%

---


# Serverzijde: Doel implementeren{#server-side-implement-target}

Informatie over API&#39;s voor levering aan de [!DNL Adobe Target] serverzijde, Node.js SDK en [!DNL Target Recommendations] API&#39;s.

Het volgende proces komt in een server-zijimplementatie van voor [!DNL Target]:

1. Een clientapparaat vraagt om een ervaring via de server.
1. Uw server verzendt die aanvraag naar [!DNL Target].
1. [!DNL Target] verzendt de reactie terug naar uw server.
1. Uw server bepaalt welke ervaring om aan het cliëntapparaat te leveren voor het terug te geven.

De ervaring hoeft niet in een browser te worden weergegeven. De ervaring kan in een e-mail of kiosk, via een stemmedewerker, of door één of andere andere niet-visuele ervaring of niet op browser-gebaseerd apparaat tonen. Omdat uw server tussen de cliënt en [!DNL Target], is dit type van implementatie ook ideaal als u grotere controle en veiligheid nodig hebt of complexe backendprocessen hebt die u op uw server wilt lopen.

De volgende secties verstrekken meer informatie over diverse APIs en NodeJS SDK:

## Server Side Delivery-API&#39;s

Koppeling: [Server Side Delivery-API&#39;s](https://developers.adobetarget.com/api/delivery-api/)

`/rest/v1/delivery`

Met de API voor [!DNL Target] aflevering kunt u:

* Lever ervaringen over Web, met inbegrip van SPAs, en mobiele kanalen evenals niet browser gebaseerde IoT apparaten, zoals aangesloten TVs, kiosken, of in-store digitale schermen.
* Lever ervaringen van om het even welke server-zijplatform of toepassing die HTTP/s vraag kan maken.
* Lever consistente en gepersonaliseerde ervaringen aan een bezoeker ongeacht welk kanaal of welke apparaten de bezoeker gebruikte om met uw zaken in gesprek te gaan.
* De ervaringen van het geheime voorgeheugen voor een bezoeker binnen een zitting op uw server zodat de veelvoudige API vraag kan worden vermeden, die betere prestaties bereikt.
* Naadloos integreren met [!DNL Adobe Experience Cloud] producten, zoals [!DNL Adobe Analytics], [!DNL Adobe Audience Manager] (AAM), en [!DNL Experience Cloud ID Service] van de serverzijde.

## Node.js SDK

Koppeling: [Node.js SDK](https://github.com/adobe/target-nodejs-sdk)

De SDK van Node.js is een geavanceerde softwareontwikkelingskit die de complexiteit van het beheren van cookies, sessies en het integreren met [!DNL Experience Cloud] producten, zoals [!DNL Analytics], [!DNL Experience Cloud Visitor ID Service]en [!DNL Audience Manager]. Achter de schermen gebruikt de SDK van Node.js de `/rest/v1/delivery` API. Hier volgen enkele belangrijke functies die worden ondersteund in de Node.js SDK:

* **Ondersteuning voor prefetch en meldingen waarmee u de prestaties kunt optimaliseren via caching:** U kunt Node.js SDK gebruiken om ervaringen terug te winnen en hen plaatselijk op uw server Node.js in het voorgeheugen onder te brengen met als doel om servervraag aan te minimaliseren [!DNL Target] en uw toepassingsprestaties te optimaliseren.
* **Capaciteit om VEC-gecreeerde activiteiten terug te winnen:** Haal VEC-gecreeerde activiteiten op server-kant terug. De reactie die VEC-gecreeerde activiteiten bevat heeft selecteurs die kunnen worden gebruikt om slechts gedeelten van uw pagina pre-te verbergen die moeten worden gepersonaliseerd. Zo kunt u de [eerste metrische](https://developers.google.com/web/fundamentals/performance/user-centric-performance-metrics.html)verf met behoud van inhoud van uw pagina optimaliseren. Dit is een belangrijke PKI voor uw bedrijf om een hoge score te behalen in het [Google PageRank](https://en.wikipedia.org/wiki/PageRank) -systeem.

## Doel Java SDK

Koppeling: [Doel Java SDK](https://github.com/adobe/target-java-sdk)

De Java SDK is een geavanceerde softwareontwikkelkit waarmee de complexiteit van het beheren van cookies, sessies en het integreren met [!DNL Adobe Experience Cloud] oplossingen, zoals [!DNL Adobe Analytics], de [!DNL Experience Cloud Visitor ID Service]en [!DNL Adobe Audience Manager]. Achter de schermen gebruikt de Java SDK de `/rest/v1/delivery` API. Hier volgen enkele belangrijke functies die worden ondersteund in de Java SDK:

* **Ondersteuning voor prefetch en meldingen waarmee u de prestaties kunt optimaliseren via caching**: U kunt de JavaSDK gebruiken om ervaringen op te halen en deze lokaal in de cache op uw Java-server op te slaan om serveraanroepen naar uw toepassingsprestaties te minimaliseren [!DNL Target] en te optimaliseren.
* **Capaciteit om VEC-gecreeerde activiteiten** terug te winnen: Haal VEC-gecreeerde activiteiten op server-kant terug. De reactie die VEC-gecreeerde activiteiten bevat heeft selecteurs die kunnen worden gebruikt om slechts gedeelten van uw pagina pre-te verbergen die moeten worden gepersonaliseerd. Zo kunt u de [eerste metrische gegevens voor inhoudelijke verf](https://developers.google.com/web/fundamentals/performance/user-centric-performance-metrics.html) van uw pagina optimaliseren. Dit is een belangrijke PKI voor uw bedrijf om een hoge score te behalen in het [Google PageRank](https://en.wikipedia.org/wiki/PageRank) -systeem.

## Doel Recommendations API&#39;s

Koppeling: [Overzicht](https://developers.adobetarget.com/api/recommendations) van Recommendations API&#39;s [en](https://docs.adobe.com/content/help/en/target-learn/recommendations-api-tutorial/recs-api-overview.html)Adobe Recommendations API.

Met de Recommendations API&#39;s kunt u programmatisch communiceren met [!DNL Target] aanbevolen servers. Deze API&#39;s kunnen worden geïntegreerd met een reeks toepassingsstapels om functies uit te voeren die u doorgaans via de [!DNL Target] gebruikersinterface doet.
