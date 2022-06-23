---
keywords: implementeren;implementeren;implementatie;adobe launch;launch;ras;redirect;Experience platform launch;platform launch;tags;adobe platform
description: Leer hoe u de [!DNL Adobe Target] at.js-bibliotheek gebruiken [!DNL Adobe Experience Platform], de methode die de voorkeur verdient [!DNL Target].
title: Hoe kan ik implementeren [!DNL Target] gebruiken [!DNL Adobe Experience Platform]?
feature: Implement Server-side
role: Developer
exl-id: 7cc1d3ab-4a68-4454-95b0-04fa547a6d9e
source-git-commit: c196b7e41101978ee029f93d5cd71c9b2d5b99f1
workflow-type: tm+mt
source-wordcount: '418'
ht-degree: 0%

---

# Implementeren [!DNL Target] gebruiken [!DNL Adobe Experience Platform]

Tags in [!DNL Adobe Experience Platform] zijn de volgende generatie mogelijkheden voor tagbeheer van [!DNL Adobe]. Met labels kunnen klanten op een eenvoudige manier de analytische, marketing- en advertentietags implementeren en beheren die nodig zijn om relevante klantervaringen mogelijk te maken.

>[!NOTE]
>
>[!DNL Adobe Experience Platform Launch] is omgedoopt tot een reeks technologieën voor gegevensverzameling in [!DNL Adobe Experience Platform]. Diverse terminologische wijzigingen zijn als gevolg hiervan in de productdocumentatie doorgevoerd. Raadpleeg het volgende [document](https://experienceleague.adobe.com/docs/experience-platform/tags/term-updates.html?lang=en) voor een geconsolideerde referentie van de terminologische wijzigingen.

In de volgende tabel worden de verschillende bronnen weergegeven waar u meer informatie kunt vinden:

| Resource | Details |
|--- |--- |
| [Toevoegen [!UICONTROL Adobe Target]](https://experienceleague.adobe.com/docs/launch-learn/implementing-in-websites-with-launch/implement-solutions/target.html#implement-solutions) | Deze zelfstudie bevat stapsgewijze instructies voor het implementeren [!DNL Target] in een website met tags in [!DNL Adobe Experience Platform]. Tot de onderwerpen behoren het toevoegen van de JavaScript-bibliotheek at.js, het afvuren van de globale box, het toevoegen van parameters en het integreren met andere oplossingen. Dit artikel maakt deel uit van een grotere zelfstudie die u laat zien hoe u het programma implementeert [!DNL Adobe Experience Platform]en andere [!DNL Adobe Experience Cloud] oplossingen. |
| [Snelstartgids](https://experienceleague.adobe.com/docs/experience-platform/tags/get-started/quick-start.html) | Informatie over het opstellen van en het beheren van de analytische, marketing, en reclame markeringen noodzakelijk om relevante klantenervaringen te aandrijven. |
| [Adobe [!DNL Target] extensieoverzicht](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/adobe/target/overview.html) | Informatie over de uitvoering [!DNL Target] gebruiken [!DNL Adobe Experience Platform]. |

## Voordelen van de implementatie van at.js met behulp van de [!DNL Target] extension {#section_48B3F938B6F8491DAF798E0DB54EF304}

De volgende voordelen zijn alleen van toepassing als u tags gebruikt in [!DNL Adobe Experience Platform] om te implementeren in.js. Daarom [!DNL Adobe] stelt u sterk voor tags te gebruiken in [!DNL Adobe Experience Platform] in plaats van een handmatige implementatie van at.js.

* **Solven [!DNL Adobe Analytics] en [!DNL Target] ras:** Omdat [!DNL Analytics] de vraag kon vóór worden in brand gestoken [!DNL Target] de [!DNL Target] aanroep is niet gekoppeld aan de [!DNL Analytics] vraag. Deze volgorde kan leiden tot onjuiste gegevens. De [!DNL Target] zorgt ervoor dat de [!DNL Analytics] de bakenvraag wacht tot [!DNL Target] de vraag voltooit, met succes of niet. Tags gebruiken in [!DNL Adobe Experience Platform] lost de gegevensinconsistentie op klanten kunnen ervaren wanneer manueel het uitvoeren.

   >[!NOTE]
   >
   >Gebruik de [!UICONTROL Send Beacon] in de [!DNL Adobe Analytics] zodat de [!DNL Analytics] de vraag wacht op [!DNL Target] vraag. Als u rechtstreeks `s.t()` of `s.tl()` aangepaste code gebruiken, [!DNL Analytics] vraag wacht niet tot [!DNL Target] de vraag is volledig.

* **Voorkomt onjuiste omleiding van aanbiedingen:** Als u [!DNL Target] en [!DNL Analytics] op de pagina en er is een doorleidingsaanbod uitgevoerd door [!DNL Target]kan een situatie optreden waarin [!DNL Analytics] tracker voert een aanvraag in als dat niet het geval is (omdat de gebruiker naar een andere URL wordt omgeleid). Als u [!DNL Target] en [!DNL Analytics] via tags in [!DNL Adobe Experience Platform], zult u dit probleem niet ervaren. Tags gebruiken in [!DNL Adobe Experience Platform], [!DNL Target] instructies [!DNL Analytics] om de [!DNL Analytics] baken-verzoek.
