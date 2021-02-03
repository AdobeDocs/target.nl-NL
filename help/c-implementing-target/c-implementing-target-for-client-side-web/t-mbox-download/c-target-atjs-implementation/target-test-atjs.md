---
keywords: at.js;niet-productie;niet-productie;inzetten
description: Informatie over hoe te om bij.js aan een niet productiemilieu veilig op te stellen.
title: Implementeren op .js naar een niet-productieomgeving
feature: at.js
translation-type: tm+mt
source-git-commit: 48b94f967252f5ddb009597456edf0a43bc54ba6
workflow-type: tm+mt
source-wordcount: '373'
ht-degree: 0%

---


# Implementeren bij.js in een niet-productieomgeving

Informatie over de technieken om op veilige wijze in.js aan een niet-productiemilieu op te stellen.

## Distribueren naar DTM-werkruimte

Als u DTM gebruikt, kunt u gemakkelijk sparen bij.js in uw configuratie van het Hulpmiddel van Adobe Target.

Nadat u de bibliotheek hebt bewaard, gebruik het hulpmiddel van de Schakelaar DTM om het tegen uw productiecode te testen. Dit zal het voor uw consultants van de Adobe gemakkelijk maken om u te steunen.

Zie [Optie 3 voor meer informatie: Implementeer Doel handmatig met de JavaScript-doelbibliotheek die wordt gehost door DTM](https://experienceleague.adobe.com/docs/dtm/implementing/target/add-target/t-implementing-target-manually-js-hosted-dtm.html) in de *Aanbevolen procedures voor het implementeren van Adobe Target met behulp van de handleiding Dynamisch tagbeheer*.

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