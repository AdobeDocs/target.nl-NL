---
keywords: implement;implementing;implementation;adobe launch;launch;race;redirect;experience platform launch
description: Adobe Experience Platform Launch is het platform voor het beheer van tags van de volgende generatie van Adobe en heeft de voorkeur voor de implementatie van Adobe Target. De lancering geeft klanten een eenvoudige manier om alle analytische, marketing, en reclame markeringen noodzakelijk om relevante klantenervaringen op te stellen en te beheren.
title: Doel implementeren met Adobe Launch
feature: implementation with launch
uuid: c8cd855b-bed1-4fc2-a0e3-f1ea6ab620e6
translation-type: tm+mt
source-git-commit: e203dc94e9bb34c4090f5795cbf73869808ada88
workflow-type: tm+mt
source-wordcount: '470'
ht-degree: 0%

---


# Doel implementeren met Adobe Launch{#implement-target-using-adobe-launch}

Adobe Experience Platform Launch is het platform voor het beheer van tags van de volgende generatie van Adobe en heeft de voorkeur voor de implementatie van Adobe Target. De lancering geeft klanten een eenvoudige manier om alle analytische, marketing, en reclame markeringen noodzakelijk om relevante klantenervaringen op te stellen en te beheren.

## Doel implementeren met Adobe Launch {#topic_5234DDAEB0834333BD6BA1B05892FC25}

Starten is het platform voor tagbeheer van de volgende generatie van Adobe en is de voorkeursmethode voor het implementeren van Adobe Target. De lancering geeft klanten een eenvoudige manier om alle analytische, marketing, en reclame markeringen noodzakelijk om relevante klantenervaringen op te stellen en te beheren.

In de volgende tabel worden de verschillende bronnen weergegeven waar u meer informatie over Starten kunt vinden:

| Resource | Details |
|--- |--- |
| [Doel implementeren met de zelfstudie voor Adobe Target-extensies](https://docs.adobe.com/content/help/en/experience-cloud/implementing-in-websites-with-launch/implement-solutions/target.html) | Deze zelfstudie bevat stapsgewijze instructies voor het implementeren van Adobe Target in een website met Starten. Tot de onderwerpen behoren het toevoegen van de JavaScript-bibliotheek at.js, het afvuren van de globale box, het toevoegen van parameters en het integreren met andere oplossingen. Dit artikel maakt deel uit van een grotere zelfstudie die u laat zien hoe u Adobe Launch en de andere Adobe Experience Cloud-oplossingen implementeert. |
| [Adobe Starten van documentatie](https://docs.adobe.com/content/help/en/launch/using/intro/get-started/quick-start.html) | Informatie over het opstellen en beheren van alle analyses, marketing, en reclame markeringen noodzakelijk om relevante klantenervaringen te aandrijven. |
| [Adobe Target Extension Documentation](https://docs.adobe.com/content/help/en/launch/using/extensions-ref/adobe-extension/target-extension/overview.html) | Informatie over het implementeren van Doel met behulp van Starten. |

## Voordelen van het Uitvoeren at.js die de Uitbreiding van de Lancering van het Doel gebruiken {#section_48B3F938B6F8491DAF798E0DB54EF304}

De volgende voordelen zijn alleen van toepassing als u Adobe Launch gebruikt om at.js te implementeren. Daarom stellen wij ten zeerste voor om Adobe Launch te gebruiken in plaats van DTM of een handmatige implementatie van at.js.

* **Analyse van oplosmiddelen en voorwaarde van doelruimte:** Omdat de vraag van Analytics vóór de vraag van het Doel kon worden in brand gestoken, wordt de vraag van het Doel niet vastgemaakt aan de vraag van Analytics. Dit kan leiden tot onjuiste gegevens. Beginnend met 0.6.0, zorgt de uitbreiding van de Lancering van het Doel ervoor dat de het bakenvraag van de Analyse wacht tot de vraag van het Doel met succes voltooit of niet. Dit zou de gegevensinconsistentie moeten oplossen klanten zouden kunnen ervaren.
* **Voorkomt onjuiste omleiding van voorstel:** Als u Doel en Analyse op de pagina hebt en Target een omleidingsaanbieding heeft uitgevoerd, kan er een situatie optreden waarin de Analytics tracker een verzoek afhandelt wanneer dit niet zou mogen (omdat de gebruiker wordt omgeleid naar een andere URL). Als u Target en Analytics implementeert via Launch, ondervindt u dit probleem niet. Gebruikend Lancering, instrueert het Doel Analytics om het het bakenverzoek van de Analyse af te breken.
