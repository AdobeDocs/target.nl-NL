---
description: Informatie over hoe te om bij.js aan een niet productiemilieu veilig op te stellen.
title: Implementeren op .js naar een niet-productieomgeving
uuid: 7f1adc43-35b4-442c-bb06-feab60604a87
translation-type: tm+mt
source-git-commit: 217ca811521e67dcd1b063d77a644ba3ae94a72c

---


# Implementeren bij.js in een niet-productieomgeving{#deploy-at-js-to-a-non-production-environment}

Informatie over de technieken om op veilige wijze in.js aan een niet-productiemilieu op te stellen.

## Distribueren naar DTM-werkruimte

Als u DTM gebruikt, kunt u gemakkelijk sparen bij.js in uw configuratie van het Hulpmiddel van het Doel van Adobe.

Nadat u de bibliotheek hebt bewaard, gebruik het hulpmiddel van de Schakelaar DTM om het tegen uw productiecode te testen. Hierdoor kunnen uw Adobe-consultants u ook eenvoudig ondersteunen.

Zie [Optie 3 voor meer informatie: Implementeer Doel handmatig met de doelJavaScript-bibliotheek die wordt gehost door DTM](https://docs.adobe.com/content/help/en/dtm/implementing/target/add-target/t-implementing-target-manually-js-hosted-dtm.html) in de *aanbevolen procedures voor het implementeren van Adobe Target met behulp van de handleiding Dynamisch tagbeheer* .

## Chrome-extensie &quot;strikt&quot; gebruiken om aan een ander bestand toe te wijzen

>[!NOTE]
>
>Naast de volgende informatie kunt u de [Adobe Target VEC Helper-browserextensie](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/vec-helper-browser-extension.md) voor Google Chrome gebruiken.

[Vraaglijk](https://chrome.google.com/webstore/detail/requestly/mdnleldcmiljblolnjhpnblkcekpdkpa?hl=en) is een gratis Chrome-extensie waarmee u aanvragen kunt doorsturen naar een alternatieve URL.

U implementeert at.js naar een URL en gebruikt vervolgens Vereist om de huidige URL van het bestand mbox.js toe te wijzen aan de nieuwe URL van at.js. Wanneer uw website vervolgens mbox.js probeert te laden, wordt het bestand op .js geladen. Op deze manier wordt het ook gemakkelijker voor Adobe om ondersteuning te bieden.

## Implementeren in een ontwikkelings-, staging- of QA-omgeving

Als u mbox.js in uw codebase host en gemakkelijk updates aan uw codemilieu&#39;s kunt maken, implementeert u at.js in een van uw lagere milieu&#39;s.

Implementeer het bestand in een omgeving die toegankelijk is voor Adobe voor betere ondersteuning van Adobe.

## Charles of Fiddler gebruiken om aan een lokaal bestand toe te wijzen

[Charles Web Debugging Proxy](https://www.charlesproxy.com/) is een toepassing beschikbaar voor MAC en Vensters de waarvan Lokale eigenschap van de Kaart kan worden gebruikt om het laden van uw productie mbox.js- dossier aan een lokaal exemplaar van at.js in kaart te brengen. Voor Mac en Windows kunt u een gratis proefversie downloaden.

[Fiddler](https://www.telerik.com/fiddler) is een vergelijkbaar programma dat u gratis kunt downloaden voor Windows.

## Distribueren naar een andere tagbeheeromgeving

Als u een andere markeringsmanager gebruikt, heeft het waarschijnlijk een manier om at.js veilig op te stellen zonder uw productieverkeer te beïnvloeden.