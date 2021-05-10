---
keywords: at.js;niet-productie;niet-productie;inzetten
description: Meer informatie over de oudere mbox.js-implementatie van Adobe Target. Migreer naar de Adobe Experience Platform Web SDK (AEP Web SDK) of naar de nieuwste versie van at.js.
title: Hoe kan ik .js implementeren in een omgeving zonder productie?
feature: at.js
role: Developer
exl-id: 607b2b5b-bb2a-4443-abc0-452b421fc009
translation-type: tm+mt
source-git-commit: 824743300725bbd39077882a0971a9ccb4f753ab
workflow-type: tm+mt
source-wordcount: '306'
ht-degree: 0%

---

# Implementeren bij.js in een niet-productieomgeving

Informatie over de technieken om op veilige wijze in.js aan een niet-productiemilieu op te stellen.

## Chrome-extensie &quot;strikt&quot; gebruiken om aan een ander bestand toe te wijzen

>[!NOTE]
>
>Naast de volgende informatie kunt u de [Adobe Target VEC Helper browser extensie](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/vec-helper-browser-extension.md) voor Google Chrome gebruiken.

[](https://chrome.google.com/webstore/detail/requestly/mdnleldcmiljblolnjhpnblkcekpdkpa?hl=en) Aanvragen is een gratis Chrome-extensie waarmee u aanvragen kunt doorsturen naar een alternatieve URL.

U implementeert at.js naar een URL en gebruikt vervolgens Vereist om de huidige URL van het bestand mbox.js toe te wijzen aan de nieuwe URL van at.js. Wanneer uw website vervolgens mbox.js probeert te laden, wordt het bestand op .js geladen. Deze aanpak maakt het ook gemakkelijker voor Adobe om steun te verlenen.

## Implementeren in een ontwikkelings-, staging- of QA-omgeving

Als u mbox.js in uw codebase host en gemakkelijk updates aan uw codemilieu&#39;s kunt maken, implementeert u at.js in een van uw lagere milieu&#39;s.

Voor betere steun van Adobe, stel het dossier aan een milieu op dat Adobe kan toegang hebben.

## Charles of Fiddler gebruiken om aan een lokaal bestand toe te wijzen

[Charles Web Debugging ](https://www.charlesproxy.com/) Proxyis een toepassing beschikbaar voor MAC en Vensters de waarvan Lokale eigenschap van de Kaart kan worden gebruikt om het laden van uw productie mbox.js- dossier aan een lokaal exemplaar van at.js in kaart te brengen. Voor Mac en Windows kunt u een gratis proefversie downloaden.

[](https://www.telerik.com/fiddler) Fiddleris een vergelijkbaar programma dat gratis kan worden gedownload voor Windows.

## Distribueren naar een andere tagbeheeromgeving

Als u een andere markeringsmanager gebruikt, heeft het waarschijnlijk een manier om at.js veilig op te stellen zonder uw productieverkeer te beïnvloeden.
