---
keywords: systeemdiagram;flicker;at.js;implementatie;javascript-bibliotheek;js;atjs
description: Het systeemdiagram van Adobe Target dat de stroom van vraag en informatie toont die voor een auto-gecreeerde globale mbox wordt verzonden of wordt verzameld gebruikend at.js.
title: Hoe de JavaScript-bibliotheek at.js werkt
feature: at.js
translation-type: tm+mt
source-git-commit: 48b94f967252f5ddb009597456edf0a43bc54ba6
workflow-type: tm+mt
source-wordcount: '1111'
ht-degree: 2%

---


# Hoe werkt at.js

Als u [!DNL Adobe Target] client-kant wilt implementeren, moet u de JavaScript-bibliotheek at.js gebruiken.

In een client-side implementatie van [!DNL Adobe Target] levert [!DNL Target] de ervaringen die met een activiteit zijn gekoppeld rechtstreeks aan de clientbrowser. De browser bepaalt welke ervaring wordt weergegeven en geeft deze weer. Met een cliënt-zijimplementatie, kunt u een redacteur WYSIWYG, [Visual Experience Composer](/help/c-experiences/c-visual-experience-composer/visual-experience-composer.md) (VEC), of een niet-visuele interface, [Op vorm-gebaseerde Composer van de Ervaring](/help/c-experiences/form-experience-composer.md), gebruiken om uw test en verpersoonlijkingservaringen tot stand te brengen.

## Wat is at.js?

De [at.js bibliotheek](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-target-atjs-implementation/target-atjs-implementation.md#concept_8AC8D169E02944B1A547A0CAD97EAC17) is de nieuwe implementatiebibliotheek voor Doel. De bibliotheek at.js verbetert de laadtijden voor webimplementaties en biedt betere implementatieopties voor toepassingen van één pagina. at.js is de aanbevolen implementatiebibliotheek en wordt regelmatig bijgewerkt met nieuwe mogelijkheden. We raden u aan dat alle klanten de [nieuwste versie van at.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md#reference_DBB5EDB79EC44E558F9E08D4774A0F7A) implementeren of naar deze nieuwste versie migreren.

Zie [JavaScript-bibliotheken van doel](/help/c-intro/how-target-works.md#libraries) voor meer informatie.

In de [!DNL Target]-implementatie hieronder worden de volgende [!DNL Adobe Experience Cloud]-oplossingen geïmplementeerd: Analytics, Target en Audience Manager. Daarnaast worden de volgende Experience Cloud core services geïmplementeerd: Adobe Starten, Soorten publiek en Bezoekersidentiteitsservice.

## Wat is het verschil tussen at.js 1.*Workflowdiagrammen* bij.js 2.x uitbreiden?

Zie [Upgraden van at.js 1.x naar at.js 2.x](/help/c-implementing-target/c-implementing-target-for-client-side-web/upgrading-from-atjs-1x-to-atjs-20.md) voor meer informatie over de verschillen die in 2.O van 1 werden geïntroduceerd.*x*.

Vanuit een weergave op hoog niveau zijn er enkele verschillen tussen de twee versies:

* at.js 2.x heeft geen globaal mbox verzoekconcept maar eerder een pagina-lading verzoek. Een verzoek om pagina&#39;s te laden kan worden beschouwd als een verzoek om inhoud op te halen die moet worden toegepast op het eerste laadmoment van de pagina van uw website.
* at.js 2.x beheert de concepten Weergaven, die worden gebruikt voor toepassingen voor één pagina (SPA). te.js 1.*Dit concept* is niet bekend.

## at.js 2.x-diagrammen

Met de volgende diagrammen krijgt u inzicht in de workflow van at.js 2.x met weergaven en in de manier waarop dit de integratie van SPA verbetert. Voor een betere inleiding van de concepten die in at.js 2.x worden gebruikt, zie [de implementatie van de Toepassing van de Enige Pagina](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/target-atjs-single-page-application.md).

![Doelstroom met at.js 2.x](/help/c-implementing-target/c-implementing-target-for-client-side-web/assets/system-diagram-atjs-20.png)

| Stap | Details |
| --- | --- |
| 1 | De vraag keert [!DNL Experience Cloud ID] terug als de gebruiker voor authentiek wordt verklaard; een andere vraag synchroniseert de klant identiteitskaart |
| 2 | De bibliotheek at.js wordt synchroon geladen en de hoofdtekst van het document verborgen.<br>at.js kan ook asynchroon worden geladen met een optioneel vooraf verborgen fragment dat op de pagina is geïmplementeerd. |
| 1 | Er wordt een aanvraag voor het laden van een pagina ingediend, inclusief alle geconfigureerde parameters (MCID, SDID en klant-id). |
| 4 | Profielscripts worden uitgevoerd en vervolgens toegevoegd aan de profielenwinkel. De winkel vraagt om gekwalificeerd publiek uit de Audience Library (bijvoorbeeld publiek dat wordt gedeeld vanuit Adobe Analytics, Publiek beheer, enz.).<br>Klantkenmerken worden in een batchproces naar de profielopslag verzonden. |
| 5 | Op basis van URL-aanvraagparameters en -profielgegevens bepaalt [!DNL Target] welke activiteiten en ervaringen moeten worden geretourneerd naar de bezoeker voor de huidige pagina en de toekomstige weergaven. |
| 6 | Gerichte inhoud wordt teruggestuurd naar de pagina, waarbij eventueel ook profielwaarden voor extra personalisatie worden opgenomen.<br>Gerichte inhoud op de huidige pagina wordt zo snel mogelijk zichtbaar zonder flikkering van de standaardinhoud.<br>Gerichte inhoud voor weergaven die worden weergegeven als gevolg van gebruikershandelingen in een SPA, wordt in de browser in de cache opgeslagen, zodat deze direct kan worden toegepast zonder een extra serveraanroep wanneer de weergaven worden geactiveerd  `triggerView()`. |
| 7 | De analysegegevens worden verzonden naar de servers van de Inzameling van Gegevens. |
| 8 | De gerichte gegevens worden aangepast aan de analysegegevens via SDID en worden verwerkt in de analytische rapporteringsopslag.<br>De analysegegevens kunnen dan in zowel Analytics als Doel via Analytics voor de rapporten van het Doel (A4T) worden bekeken. |

Nu, waar `triggerView()` op uw SPA wordt uitgevoerd, worden de Meningen en de acties teruggewonnen van geheim voorgeheugen en aan de gebruiker getoond zonder een servervraag. `triggerView()` doet ook een verzoek om meldingen aan de  [!DNL Target] achterzijde om het aantal puntjes op de i te zetten en opnamen te maken. Zie [Toepassing van één pagina](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/target-atjs-single-page-application.md) voor meer informatie over at.js voor SPA met weergaven.

![Doelstroom bij.js 2.x triggerView](/help/c-implementing-target/c-implementing-target-for-client-side-web/assets/atjs-20-triggerview.png)

| Stap | Details |
| --- | --- |
| 3 | `triggerView()` wordt opgeroepen in de SPA om de weergave te renderen en acties toe te passen om visuele elementen te wijzigen. |
| 2 | De gerichte inhoud voor de mening wordt gelezen van het geheime voorgeheugen. |
| 3 | Gerichte inhoud wordt zo snel mogelijk zichtbaar zonder flikkering van de standaardinhoud. |
| 4 | Het verzoek om een melding wordt verzonden naar de [!DNL Target] Opslag van het Profiel om de bezoeker in de activiteit en verhogingsmetriek te tellen. |
| 5 | Analytische gegevens die naar de Servers van de Inzameling van Gegevens worden verzonden. |
| 6 | De doelgegevens worden via de SDID aangepast aan de analysegegevens en worden verwerkt in de analytische rapportageopslag. De analysegegevens kunnen dan in zowel Analytics als Doel via A4T- rapporten worden bekeken. |

### Video - op.js 2.x architecturaal diagram

at.js 2.x verbetert de Adobe Target-ondersteuning voor SPA en integreert deze met andere Experience Cloud-oplossingen. In deze video wordt uitgelegd hoe alles bij elkaar komt.

>[!VIDEO](https://video.tv.adobe.com/v/26250)

Zie [Begrijpen hoe at.js 2.x](https://helpx.adobe.com/target/kt/using/atjs20-diagram-technical-video-understand.html) voor meer informatie werkt.

## bij.js 1.x-diagram

![Doelstroom - bij.js 1.x](/help/c-implementing-target/c-implementing-target-for-client-side-web/assets/target-flow.png)

| Stap | Beschrijving | Bellen | Beschrijving |
|--- |--- |--- |--- |
| 3 | De vraag keert [!DNL Experience Cloud ID] (MCID) terug als de gebruiker voor authentiek wordt verklaard; een andere vraag synchroniseert de klant identiteitskaart | 2 | De bibliotheek at.js wordt synchroon geladen en de hoofdtekst van het document verborgen. |
| 1 | Er wordt een globaal mbox-verzoek ingediend, inclusief alle geconfigureerde parameters, MCID, SDID en klant-id (optioneel). | 4 | Profielscripts worden uitgevoerd en vervolgens toegevoegd aan de profielenwinkel. De opslag vraagt gekwalificeerd publiek van [!UICONTROL Audience Library] (bijvoorbeeld, publiek dat van [!DNL Adobe Analytics], [!DNL Audience Manager], enz. wordt gedeeld).<br>Klantkenmerken worden  [!DNL Profile Store] in een batchproces naar de klant verzonden. |
| 5 | Op basis van de URL, mbox-parameters en profielgegevens bepaalt [!DNL Target] welke activiteiten en ervaringen moeten worden geretourneerd aan de bezoeker. | 6 | Gerichte inhoud wordt teruggestuurd naar pagina, met eventueel ook profielwaarden voor extra personalisatie.<br>De ervaring wordt zo snel mogelijk getoond zonder flikkering van standaardinhoud. |
| 7 | [!DNL Analytics] gegevens worden naar gegevensverzamelingsservers verzonden. | 8 | [!DNL Target] gegevens worden via de SDID aan  [!DNL Analytics] gegevens aangepast en worden in de  [!DNL Analytics]  rapportageopslag verwerkt.<br>[!DNL Analytics] gegevens kunnen vervolgens zowel in  [!DNL Analytics] als   [!DNL Target] via  [!DNL Analytics for Target] (A4T) rapporten worden bekeken. |

### Video - kantooruren: tips en overzicht op .js (26 juni 2019)

Deze video is een opname van &quot;Office Hours&quot;, een initiatief onder leiding van het Adobe Customer Care-team.

* Voordelen van het gebruik van at.js
* at.js-instellingen
* Flikkerverwerking
* Foutopsporing bij.js
* Bekende problemen
* Veelgestelde vragen

>[!VIDEO](https://video.tv.adobe.com/v/27959)

## Hoe geeft at.js aanbiedingen met HTML-inhoud {#render} weer

Bij rendering van aanbiedingen met HTML-inhoud past at.js het volgende algoritme toe:

1. Afbeeldingen worden vooraf geladen (als er `<img>`-tags zijn in HTML-inhoud).

1. HTML-inhoud is gekoppeld aan het DOM-knooppunt.

1. Inline scripts worden uitgevoerd (code die wordt ingesloten door `<script>`-tags).

1. Externe scripts worden asynchroon geladen en uitgevoerd (`<script>`-tags met `src`-kenmerken).

Belangrijke opmerkingen:

* at.js verstrekt geen garanties op de orde van verre manuscriptuitvoering, aangezien deze asynchroon worden geladen.
* Inline scripts mogen geen afhankelijkheden hebben van externe scripts, omdat deze later worden geladen en uitgevoerd.