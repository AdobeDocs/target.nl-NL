---
keywords: implementeren;implementeren;instellen;instellen;gegevensproviders
description: Krijg gegevens in Doel gebruikend gegevensleveranciers.
title: Hoe krijg ik gegevens in doel gebruikend de Leveranciers van Gegevens?
feature: Implementatie
role: Developer
exl-id: 05fe9190-4d36-43e2-9fc7-c354a6821bfb
translation-type: tm+mt
source-git-commit: 20daf4510e754d77cd16be64770105932178fec5
workflow-type: tm+mt
source-wordcount: '301'
ht-degree: 0%

---

# Gegevensleveranciers

Gegevensleveranciers zijn een mogelijkheid waarmee u gegevens van derden eenvoudig kunt doorgeven aan [!DNL Adobe Target].

Opmerking: Gegevensleveranciers vereisen at.js 1.3 of later.

## Indeling

De instelling `window.targetGlobalSettings.dataProviders` is een array van gegevensproviders.

Zie [Gegevensleveranciers](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetgobalsettings.md#data-providers) voor meer informatie over de structuur voor elke gegevensaanbieder.

## Voorbeelden van gebruiksgevallen

Verzamel gegevens van derden, zoals een weerservice, een DMP of zelfs uw eigen webservice. Vervolgens kunt u deze gegevens gebruiken om een publiek te maken, inhoud te benoemen en het profiel van de bezoeker te verrijken.

## Voordelen van de methode

Met deze instelling kunnen klanten gegevens verzamelen van gegevensleveranciers van derden, zoals Demandbase, BlueKai en aangepaste services, en de gegevens doorgeven aan Target als mbox-parameters in het algemene mbox-verzoek.

Het steunt de inzameling van gegevens van veelvoudige leveranciers via async en synchronisatieverzoeken.

Op deze manier kunt u flikkering van de standaardpagina-inhoud eenvoudig beheren en onafhankelijke time-outs opnemen voor elke provider om de invloed op de paginaprestaties te beperken

## Caveats

Als de gegevensleveranciers die aan `window.targetGlobalSettings.dataProviders` worden toegevoegd asynchroon zijn, worden zij uitgevoerd parallel. De aanvraag voor de API van de bezoeker wordt parallel met de functies uitgevoerd die aan `window.targetGlobalSettings.dataProviders` worden toegevoegd om een minimale wachttijd mogelijk te maken.

at.js probeert niet om de gegevens in het voorgeheugen onder te brengen. Als de gegevensleverancier gegevens slechts één keer haalt, zou de gegevensleverancier ervoor moeten zorgen dat de gegevens in het voorgeheugen wordt opgeslagen en, wanneer de leveranciersfunctie wordt aangehaald, de geheim voorgeheugengegevens voor de tweede aanroeping dienen.

## Codevoorbeelden

Verschillende voorbeelden vindt u in [Gegevensleveranciers](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetgobalsettings.md#data-providers).

## Koppelingen naar relevante informatie

Documentatie: [Gegevensleveranciers](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetgobalsettings.md#data-providers)

## Trainingsvideo&#39;s:

* [Gegevensleveranciers gebruiken in Adobe Target](https://helpx.adobe.com/target/kt/using/dataProviders-atjs-feature-video-use.html)
* [Gegevensleveranciers implementeren in Adobe Target](https://helpx.adobe.com/target/kt/using/dataProviders-atjs-technical-video-implement.html)
