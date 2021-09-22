---
keywords: implementeren;implementeren;implementatie;adobe launch;launch;ras;redirect;Experience platform launch;platform launch;tags;adobe platform
description: Leer hoe te om  [!DNL Adobe Target] at.js bibliotheek uit te voeren gebruikend [!DNL Adobe Experience Platform], the preferred method to implement [!DNL Target].
title: Hoe implementeer ik [!DNL Target] using [!DNL Adobe Experience Platform]?
feature: Implement Server-side
role: Developer
exl-id: 7cc1d3ab-4a68-4454-95b0-04fa547a6d9e
source-git-commit: f4b490c489427130e78d84b573b2d290a8a60585
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# [!DNL Target] implementeren met [!DNL Adobe Experience Platform]

Tags in [!DNL Adobe Experience Platform] zijn de volgende generatie mogelijkheden voor tagbeheer van [!DNL Adobe]. Met labels kunnen klanten op eenvoudige wijze de analytische, marketing- en advertentietags implementeren en beheren die nodig zijn om relevante klantervaringen mogelijk te maken.

>[!NOTE]
>
>[!DNL Adobe Experience Platform Launch] is omgedoopt tot een reeks technologieën voor gegevensverzameling in  [!DNL Adobe Experience Platform]. Diverse terminologische wijzigingen zijn als gevolg hiervan in de productdocumentatie doorgevoerd. Raadpleeg het volgende [document](https://experienceleague.adobe.com/docs/experience-platform/tags/term-updates.html?lang=en) voor een geconsolideerde referentie van de terminologische wijzigingen.

In de volgende tabel worden de verschillende bronnen weergegeven waar u meer informatie kunt vinden:

| Resource | Details |
|--- |--- |
| [Toevoegen  [!UICONTROL Adobe Target]](https://experienceleague.adobe.com/docs/launch-learn/implementing-in-websites-with-launch/implement-solutions/target.html#implement-solutions) | Deze zelfstudie bevat stapsgewijze instructies voor het implementeren van [!DNL Target] in een website met tags in [!DNL Adobe Experience Platform]. Tot de onderwerpen behoren het toevoegen van de JavaScript-bibliotheek at.js, het afvuren van de globale box, het toevoegen van parameters en het integreren met andere oplossingen. Dit artikel maakt deel uit van een grotere zelfstudie die u toont hoe te om [!DNL Adobe Experience Platform], en andere [!DNL Adobe Experience Cloud] oplossingen uit te voeren. |
| [Snelstartgids](https://experienceleague.adobe.com/docs/experience-platform/tags/get-started/quick-start.html) | Informatie over het opstellen van en het beheren van de analytische, marketing, en reclame markeringen noodzakelijk om relevante klantenervaringen te aandrijven. |
| [Overzicht van  [!DNL Target] AdobeExtension](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/adobe/target/overview.html) | Informatie over het implementeren van [!DNL Target] met [!DNL Adobe Experience Platform]. |

## Voordelen van het implementeren van at.js met de extensie [!DNL Target] {#section_48B3F938B6F8491DAF798E0DB54EF304}

De volgende voordelen zijn alleen van toepassing als u tags gebruikt in [!DNL Adobe Experience Platform] om at.js te implementeren. Daarom [!DNL Adobe] wordt sterk aangeraden dat u labels gebruikt in [!DNL Adobe Experience Platform] in plaats van een handmatige implementatie van at.js.

* **Oplost  [!DNL Adobe Analytics] en  [!DNL Target] rasvoorwaarde:** Omdat de  [!DNL Analytics] vraag vóór de  [!DNL Target] vraag kon worden in brand gestoken, wordt de  [!DNL Target] vraag niet vastgemaakt aan de  [!DNL Analytics] vraag. Deze volgorde kan leiden tot onjuiste gegevens. De [!DNL Target] uitbreiding zorgt ervoor dat de [!DNL Analytics] bakenvraag wacht tot de [!DNL Target] vraag voltooit, met succes of niet. Door tags te gebruiken in [!DNL Adobe Experience Platform] worden de inconsistente gegevens opgelost die klanten kunnen ervaren bij het handmatig implementeren.

   >[!NOTE]
   >
   >Gebruik de [!UICONTROL Send Beacon] actie in de [!DNL Adobe Analytics] uitbreiding zodat de [!DNL Analytics] vraag op de [!DNL Target] vraag wacht. Als u `s.t()` of `s.tl()` gebruikend douanecode direct roept, [!DNL Analytics] de vraag wacht niet tot [!DNL Target] volledig vraag is.

* **Voorkomt onjuiste omleiding van aanbiedingen:** Als u  [!DNL Target] en  [!DNL Analytics] op de pagina hebt, en er een omleidingsaanbieding door wordt uitgevoerd  [!DNL Target], kunt u een situatie ervaren waarin de  [!DNL Analytics] tracker een verzoek in brand steekt wanneer het niet zou moeten (omdat de gebruiker aan een verschillende URL wordt opnieuw gericht). Als u [!DNL Target] en [!DNL Analytics] via tags implementeert in [!DNL Adobe Experience Platform], zult u dit probleem niet ervaren. Met behulp van tags in [!DNL Adobe Experience Platform] geeft [!DNL Target] [!DNL Analytics] de instructie om het [!DNL Analytics]-verzoek af te breken.
