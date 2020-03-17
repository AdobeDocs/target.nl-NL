---
keywords: at.js;api;release;updates;apis;sdks;server side;serverside;server-side;api;delivery api
description: Opmerkingen bij de release die betrekking hebben op de API's aan de serverzijde van Adobe Target.
title: Opmerkingen bij de release die betrekking hebben op de API's aan de serverzijde van Adobe Target.
topic: Standard
translation-type: tm+mt
source-git-commit: 217ca811521e67dcd1b063d77a644ba3ae94a72c

---


# Opmerkingen bij de release - Doelserver-side API&#39;s

Opmerkingen bij de release die betrekking hebben op de API&#39;s van de [Adobe Target-server](https://developers.adobetarget.com/api/delivery-api/).

## V1/levering (9 oktober 2019)

Een volledig nieuw levering API eindpunt is vrijgegeven.

* Er is nieuwe [documentatie](https://developers.adobetarget.com/api/delivery-api/) beschikbaar.
* Één eindpunt om ervaringen voor één of meerdere dozen terug te winnen.
* Haal VEC-activiteiten op via de API.

   De reactie die VEC-gecreeerde activiteiten bevat heeft selecteurs die kunnen worden gebruikt om slechts gedeelten van uw pagina pre-te verbergen die moeten worden gepersonaliseerd. Zo kunt u de [eerste metrische](https://developers.google.com/web/fundamentals/performance/user-centric-performance-metrics.html)verf met behoud van inhoud van uw pagina optimaliseren. Dit is een belangrijke PKI voor uw bedrijf om een hoge score te behalen in het [Google PageRank](https://en.wikipedia.org/wiki/PageRank) -systeem.

* Ondersteuning voor een geheel nieuw object met de naam Weergaven dat wordt gebruikt voor toepassingen [voor](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/target-atjs-single-page-application.md) één pagina (SPA&#39;s) en [mobiele toepassingen](/help/c-target-mobile-app/target-mobile-app.md).
* Ondersteuning voor het vooraf instellen van weergaven en vakken om de prestaties via caching te optimaliseren.
* Ondersteuning voor het verzenden van meldingen voor vooraf ingestelde weergaven en vakken.

>[!IMPORTANT]
>
>De oudere [/v1/mbox- en /v2/batchbox-API-documentatie](https://developers.adobetarget.com/api/legacy-api/index.html) is nog steeds toegankelijk. Nieuwe functies worden echter ontwikkeld in de nieuwe API voor levering en worden niet teruggezet naar de oudere API&#39;s.
