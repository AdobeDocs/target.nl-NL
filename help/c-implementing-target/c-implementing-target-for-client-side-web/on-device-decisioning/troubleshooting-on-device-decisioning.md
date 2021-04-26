---
keywords: implementatie;javascript-bibliotheek;js;atjs;apparaatbeslissingen;op apparaatbeslissingen;at.js;op apparaat;op apparaat;problemen oplossen;problemen oplossen
description: Leer hoe te om op-apparatenbesluit met de bibliotheek at.js problemen op te lossen.
title: Hoe los ik op-Apparaatbesluit met de JavaScript-bibliotheek at.js problemen op?
feature: at.js
role: Developer
translation-type: tm+mt
source-git-commit: 85a17944c7d5924edb1bbabb7531274249ceaaa8
workflow-type: tm+mt
source-wordcount: '257'
ht-degree: 0%

---

# Problemen met apparaatbeslissingen voor at.js oplossen

Voer de volgende stappen uit om problemen op te lossen bij het bepalen van het apparaat in [!DNL Adobe Target] met de JavaScript-bibliotheek at.js:

## Stap 1: Het consolelogboek voor at.js inschakelen

Als u de URL-parameter `mboxDebug=1` toevoegt, kan at.js berichten afdrukken in de browserconsole.

Alle berichten bevatten een voorvoegsel &quot;AT:&quot;voor geschikt overzicht. Om ervoor te zorgen dat een artefact met succes is geladen, zou uw consolelogboek berichten gelijkend op het volgende moeten bevatten:

```
AT: LD.ArtifactProvider fetching artifact - https://assets.adobetarget.com/your-client-cide/production/v1/rules.json
AT: LD.ArtifactProvider artifact received - status=200
```

De volgende illustratie toont deze berichten in het consolelogboek:

![Logbestand van console met artefactberichten](/help/c-implementing-target/c-implementing-target-for-client-side-web/on-device-decisioning/assets/browser-console.png)

## Stap 2: Verifieer de download van het regelartefact in het lusje van het Netwerk van uw browser

Open het tabblad Netwerk van uw browser.

Als u bijvoorbeeld DevTools wilt openen in Google Chrome:

1. Druk op Ctrl+Shift+J (Windows) of Command+Option+J (Mac).
1. Navigeer naar het tabblad Netwerk.
1. Filter uw vraag door sleutelwoord &quot;rules.json&quot;om ervoor te zorgen dat slechts de vertoningen van het artefactregelingendossier.

   Daarnaast kunt u filteren op &quot;/delivery|rules.json/&quot; om alle [!DNL Target] aanroepen en artefactrules.json weer te geven.

   ![Het tabblad Netwerk in Google Chrome](/help/c-implementing-target/c-implementing-target-for-client-side-web/on-device-decisioning/assets/rule-json.png)

## Stap 3: Verifieer de download van het regelartefact gebruikend at.js douanegebeurtenissen

De bibliotheek at.js verzendt twee nieuwe douanegebeurtenissen om op-apparatenbesluit te steunen.

* `adobe.target.event.ARTIFACT_DOWNLOAD_SUCCEEDED`
* `adobe.target.event.ARTIFACT_DOWNLOAD_FAILED`

U kunt zich abonneren om naar deze aangepaste gebeurtenissen in uw toepassing te luisteren en deze te activeren wanneer het downloaden van het bestand met artefactregels is gelukt of mislukt.

In het volgende voorbeeld ziet u een voorbeeld van code die luistert naar gebeurtenissen voor het downloaden van artefacten en mislukken:

```javascript
document.addEventListener(adobe.target.event.ARTIFACT_DOWNLOAD_SUCCEEDED, function(e) { 
  console.log("Artifact successfully downloaded", e.detail);
}, false);

document.addEventListener(adobe.target.event.ARTIFACT_DOWNLOAD_FAILED, function(e) { 
  console.log("Artifact failed to download", e.detail);
}, false);
```
