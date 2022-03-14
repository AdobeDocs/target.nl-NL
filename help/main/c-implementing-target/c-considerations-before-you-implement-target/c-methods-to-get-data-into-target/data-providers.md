---
keywords: implementeren;implementeren;instellen;instellen;gegevensproviders
description: Gegevens ophalen in [!DNL Target] het gebruik van gegevensaanbieders.
title: Hoe krijg ik gegevens in [!DNL Target] Gegevensproviders gebruiken?
feature: Implementation
role: Developer
exl-id: 05fe9190-4d36-43e2-9fc7-c354a6821bfb
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '298'
ht-degree: 0%

---

# Gegevensleveranciers

Gegevensleveranciers zijn een mogelijkheid waarmee u gegevens van derden eenvoudig kunt doorgeven aan [!DNL Adobe Target].

Opmerking: Gegevensleveranciers vereisen at.js 1.3 of later.

## Indeling

De `window.targetGlobalSettings.dataProviders` het plaatsen is een serie van gegevensleveranciers.

Voor meer informatie over de structuur voor elke gegevensleverancier, zie [Gegevensleveranciers](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/targetgobalsettings.md#data-providers).

## Voorbeelden van gebruiksgevallen

Verzamel gegevens van derden, zoals een weerservice, een DMP of zelfs uw eigen webservice. Vervolgens kunt u deze gegevens gebruiken om een publiek te maken, inhoud te benoemen en het profiel van de bezoeker te verrijken.

## Voordelen van de methode

Met deze instelling kunnen klanten gegevens verzamelen van gegevensleveranciers van derden, zoals Demandbase, BlueKai en aangepaste services, en de gegevens doorgeven aan Target als mbox-parameters in het algemene mbox-verzoek.

Het steunt de inzameling van gegevens van veelvoudige leveranciers via async en synchronisatieverzoeken.

Op deze manier kunt u flikkering van de standaardpagina-inhoud eenvoudig beheren en onafhankelijke time-outs opnemen voor elke provider om de invloed op de paginaprestaties te beperken

## Caveats

Als de gegevensleveranciers `window.targetGlobalSettings.dataProviders` asynchroon zijn, worden ze parallel uitgevoerd. De visitor-API-aanvraag wordt uitgevoerd in combinatie met toegevoegde functies `window.targetGlobalSettings.dataProviders` om een minimale wachttijd toe te staan.

at.js probeert niet om de gegevens in het voorgeheugen onder te brengen. Als de gegevensleverancier gegevens slechts één keer haalt, zou de gegevensleverancier ervoor moeten zorgen dat de gegevens in het voorgeheugen wordt opgeslagen en, wanneer de leveranciersfunctie wordt aangehaald, de geheim voorgeheugengegevens voor de tweede aanroeping dienen.

## Codevoorbeelden

Verschillende voorbeelden vindt u in [Gegevensleveranciers](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/targetgobalsettings.md#data-providers).

## Koppelingen naar relevante informatie

Documentatie: [Gegevensleveranciers](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/targetgobalsettings.md#data-providers)

## Trainingsvideo&#39;s:

* [Gegevensleveranciers gebruiken in Adobe Target](https://helpx.adobe.com/target/kt/using/dataProviders-atjs-feature-video-use.html)
* [Gegevensleveranciers implementeren in Adobe Target](https://helpx.adobe.com/target/kt/using/dataProviders-atjs-technical-video-implement.html)
