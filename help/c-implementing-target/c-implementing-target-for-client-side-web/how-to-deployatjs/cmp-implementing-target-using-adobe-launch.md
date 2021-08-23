---
keywords: implementeren;implementeren;implementatie;adobe launch;launch;race;redirect;Experience platform launch;platform launch
description: Leer hoe u de Adobe [!DNL Target] at.js-bibliotheek implementeert met Adobe Experience Platform Launch, de voorkeursmethode voor het implementeren van Adobe [!DNL Target].
title: Hoe voer ik  [!DNL Target] het gebruiken van de Lancering van Adobe uit?
feature: Server-kant implementeren
role: Developer
exl-id: 7cc1d3ab-4a68-4454-95b0-04fa547a6d9e
source-git-commit: fd7d3900f9e5d1a6c3d13fd2452de8528f8fd248
workflow-type: tm+mt
source-wordcount: '352'
ht-degree: 0%

---

# [!DNL Target] implementeren met [!DNL Adobe Platform Launch]

[!DNL Adobe Experience Platform Launch] is het platform voor tagbeheer van de volgende generatie van  [!DNL Adobe] en is de voorkeursmethode voor implementatie  [!DNL Adobe Target]. [!DNL Platform Launch] biedt klanten een eenvoudige manier om de analytische, marketing- en advertentietags te implementeren en te beheren die nodig zijn om de relevante ervaringen van klanten te verbeteren.

## [!DNL Target] implementeren met [!DNL Platform Launch] {#topic_5234DDAEB0834333BD6BA1B05892FC25}

In de volgende tabel worden de verschillende bronnen weergegeven waar u meer informatie kunt vinden over [!DNL Platform Launch]:

| Resource | Details |
|--- |--- |
| [Implementeren  [!DNL Target] met de  [!UICONTROL Adobe Target Extension Tutorial]](https://experienceleague.adobe.com/docs/launch-learn/implementing-in-websites-with-launch/implement-solutions/target.html#implement-solutions) | Deze zelfstudie bevat stapsgewijze instructies voor het implementeren van [!DNL Target] in een website met [!DNL Platform Launch]. Tot de onderwerpen behoren het toevoegen van de JavaScript-bibliotheek at.js, het afvuren van de globale box, het toevoegen van parameters en het integreren met andere oplossingen. Dit artikel maakt deel uit van een grotere zelfstudie die u toont hoe te om [!DNL Platform Launch], en andere [!DNL Adobe Experience Cloud] oplossingen uit te voeren. |
| [QuickStart-handleiding voor tags in Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/tags/get-started/quick-start.html) | Informatie over het opstellen van en het beheren van de analytische, marketing, en reclame markeringen noodzakelijk om relevante klantenervaringen te aandrijven. |
| [Documentatie  [!DNL Target] voor Adobe-extensies](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/adobe/target/overview.html) | Informatie over het implementeren van [!DNL Target] met [!DNL Platform Launch]. |

## Voordelen van het implementeren van at.js met de extensie [!DNL Target] [!DNL Platform Launch] {#section_48B3F938B6F8491DAF798E0DB54EF304}

De volgende voordelen zijn alleen van toepassing als u [!DNL Platform Launch] gebruikt om at.js te implementeren. Daarom [!DNL Adobe] wordt sterk aangeraden [!DNL Platform Launch] te gebruiken in plaats van een handmatige implementatie van at.js.

* **Oplost  [!DNL Adobe Analytics] en  [!DNL Target] rasvoorwaarde:** Omdat de  [!DNL Analytics] vraag vóór de  [!DNL Target] vraag kon worden in brand gestoken, wordt de  [!DNL Target] vraag niet vastgemaakt aan de  [!DNL Analytics] vraag. Deze volgorde kan leiden tot onjuiste gegevens. Beginnend met 0.6.0, zorgt de [!DNL Platform Launch] uitbreiding ervoor dat de [!DNL Analytics] bakenvraag wacht tot de [!DNL Target] vraag voltooit, met succes of niet. Met [!DNL Platform Launch] wordt de gegevensinconsistentie opgelost die klanten kunnen ervaren wanneer ze handmatig implementeren.
* **Voorkomt onjuiste omleiding van aanbiedingen:** Als u  [!DNL Target] en  [!DNL Analytics] op de pagina hebt, en er een omleidingsaanbieding door wordt uitgevoerd  [!DNL Target], kunt u een situatie ervaren waarin de  [!DNL Analytics] tracker een verzoek in brand steekt wanneer het niet zou moeten (omdat de gebruiker aan een verschillende URL wordt opnieuw gericht). Als u [!DNL Target] en [!DNL Analytics] via [!DNL Platform Launch] implementeert, zult u dit probleem niet ervaren. [!DNL Platform Launch] gebruiken, [!DNL Target] geeft [!DNL Analytics] opdracht om het [!DNL Analytics] bakenverzoek af te breken.
