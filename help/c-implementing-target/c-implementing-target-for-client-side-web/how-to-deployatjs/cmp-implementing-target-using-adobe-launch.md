---
keywords: implementeren;implementeren;implementatie;adobe launch;launch;race;redirect;Experience platform starten
description: Adobe Experience Platform Launch is het platform voor het beheer van tags van de volgende generatie van Adobe en heeft de voorkeur voor de implementatie van Adobe Target. De lancering geeft klanten een eenvoudige manier om alle analytische, marketing, en reclame markeringen noodzakelijk om relevante klantenervaringen op te stellen en te beheren.
title: Implementeren met Adobe Launch
feature: Implement Server-side
translation-type: tm+mt
source-git-commit: 48b94f967252f5ddb009597456edf0a43bc54ba6
workflow-type: tm+mt
source-wordcount: '474'
ht-degree: 0%

---


# Doel implementeren met Adobe Launch

Adobe Experience Platform Launch is het platform voor het beheer van tags van de volgende generatie van Adobe en heeft de voorkeur voor de implementatie van Adobe Target. De lancering geeft klanten een eenvoudige manier om alle analytische, marketing, en reclame markeringen noodzakelijk om relevante klantenervaringen op te stellen en te beheren.

## Doel implementeren met Adobe starten {#topic_5234DDAEB0834333BD6BA1B05892FC25}

Starten is het platform voor tagbeheer van de volgende generatie van Adobe en is de voorkeursmethode voor het implementeren van Adobe Target. De lancering geeft klanten een eenvoudige manier om alle analytische, marketing, en reclame markeringen noodzakelijk om relevante klantenervaringen op te stellen en te beheren.

In de volgende tabel worden de verschillende bronnen weergegeven waar u meer informatie over Starten kunt vinden:

| Resource | Details |
|--- |--- |
| [Doel implementeren met de zelfstudie voor Adobe Target-extensies](https://experienceleague.adobe.com/docs/experience-cloud/implementing-in-websites-with-launch/implement-solutions/target.html) | Deze zelfstudie bevat stapsgewijze instructies voor het implementeren van Adobe Target in een website met Starten. Tot de onderwerpen behoren het toevoegen van de JavaScript-bibliotheek at.js, het afvuren van de globale box, het toevoegen van parameters en het integreren met andere oplossingen. Dit artikel maakt deel uit van een grotere zelfstudie die u laat zien hoe u Adobe Launch en de andere Adobe Experience Cloud-oplossingen implementeert. |
| [Adobe Starten van documentatie](https://experienceleague.adobe.com/docs/launch/using/intro/get-started/quick-start.html) | Informatie over het opstellen en beheren van alle analyses, marketing, en reclame markeringen noodzakelijk om relevante klantenervaringen te aandrijven. |
| [Adobe Target Extension Documentation](https://experienceleague.adobe.com/docs/launch/using/extensions-ref/adobe-extension/target-extension/overview.html) | Informatie over het implementeren van Doel met behulp van Starten. |

## Voordelen van het uitvoeren van at.js die de uitbreiding {#section_48B3F938B6F8491DAF798E0DB54EF304} van de Lancering van het Doel gebruiken

De volgende voordelen zijn alleen van toepassing als u Adobe Launch gebruikt om at.js te implementeren. Daarom stellen wij ten zeerste voor om Adobe Launch te gebruiken in plaats van DTM of een handmatige implementatie van at.js.

* **Los Analytics en de Voorwaarde van de Ras van het Doel op:** Omdat de vraag van Analytics vóór de vraag van het Doel kon worden in brand gestoken, wordt de vraag van het Doel niet vastgemaakt aan de vraag van Analytics. Dit kan leiden tot onjuiste gegevens. Beginnend met 0.6.0, zorgt de uitbreiding van de Lancering van het Doel ervoor dat de het bakenvraag van de Analyse wacht tot de vraag van het Doel met succes voltooit of niet. Dit zou de gegevensinconsistentie moeten oplossen klanten zouden kunnen ervaren.
* **Voorkomt onjuiste omleiding van aanbiedingen:** Als u Doel en Analyse op de pagina hebt en er een omleidingsaanbieding door Target wordt uitgevoerd, zou u een situatie kunnen ervaren waarin de Analytics tracker een verzoek in brand steekt wanneer het niet zou moeten (omdat de gebruiker aan een verschillende URL wordt opnieuw gericht). Als u Target en Analytics implementeert via Launch, ondervindt u dit probleem niet. Gebruikend Lancering, instrueert het Doel Analytics om het het bakenverzoek van de Analyse af te breken.
