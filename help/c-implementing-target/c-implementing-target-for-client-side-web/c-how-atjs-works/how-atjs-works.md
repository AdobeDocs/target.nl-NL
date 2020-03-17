---
keywords: system diagram;flicker;at.js;implementation;javascript library;js;atjs
description: Het systeemdiagram van het Doel van Adobe dat de stroom van vraag en informatie toont die voor een auto-gecreeerde globale mbox wordt verzonden of wordt verzameld gebruikend at.js.
title: De werking van de Adobe Target-bibliotheek op .js JavaScript
topic: Standard
uuid: 8ed04881-3dd9-496f-9c9c-feb9c740ed80
translation-type: tm+mt
source-git-commit: 65a4fd0d05ad065c9291a83dc0b3066451f7373e

---


# Hoe werkt at.js{#how-at-js-works}

Als u de [!DNL Adobe Target] client-side wilt implementeren, moet u de JavaScript-bibliotheek at.js gebruiken.

In een client-side implementatie van [!DNL Adobe Target], [!DNL Target] levert de ervaringen verbonden aan een activiteit direct aan cliëntbrowser. De browser bepaalt welke ervaring wordt weergegeven en geeft deze weer. Met een cliënt-zijimplementatie, kunt u een redacteur WYSIWYG, de [Visuele Composer](/help/c-experiences/c-visual-experience-composer/visual-experience-composer.md) van de Ervaring (VEC), of een niet-visuele interface, de [Op vorm-gebaseerde Composer](/help/c-experiences/form-experience-composer.md)van de Ervaring gebruiken, om uw test en verpersoonlijkingservaringen tot stand te brengen.

## Wat is at.js?

De bibliotheek [at.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-target-atjs-implementation/target-atjs-implementation.md#concept_8AC8D169E02944B1A547A0CAD97EAC17) is de nieuwe implementatiebibliotheek voor Doel. De bibliotheek at.js verbetert de laadtijden voor webimplementaties en biedt betere implementatieopties voor toepassingen van één pagina. at.js is de aanbevolen implementatiebibliotheek en wordt regelmatig bijgewerkt met nieuwe mogelijkheden. Wij adviseren dat alle klanten uitvoeren of aan de [recentste versie van at.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md#reference_DBB5EDB79EC44E558F9E08D4774A0F7A)migreren.

Zie JavaScript-bibliotheken [](/help/c-intro/how-target-works.md#libraries)Doel voor meer informatie.

In de hieronder weergegeven [!DNL Target] implementatie worden de volgende [!DNL Adobe Experience Cloud] oplossingen geïmplementeerd: Analytics, Target en Audience Manager. Daarnaast worden de volgende Experience Cloud-kernservices geïmplementeerd: Adobe-service Starten, Soorten publiek en Bezoeker-id.

## Wat is het verschil tussen at.js 1.*workflowdiagrammen x* en at.js 2.x?

Zie [Bevorderen van at.js 1.x aan at.js 2.x](/help/c-implementing-target/c-implementing-target-for-client-side-web/upgrading-from-atjs-1x-to-atjs-20.md) voor meer informatie over de verschillen die in 2.O van 1 werden geïntroduceerd.*x*.

Vanuit een weergave op hoog niveau zijn er enkele verschillen tussen de twee versies:

* at.js 2.x heeft geen globaal mbox verzoekconcept maar eerder een pagina-lading verzoek. Een verzoek om pagina&#39;s te laden kan worden beschouwd als een verzoek om inhoud op te halen die moet worden toegepast op het eerste laadmoment van de pagina van uw website.
* at.js 2.x beheert de concepten genoemd Meningen, die voor de Toepassingen van de Enige Pagina (SPAs) worden gebruikt. te.js 1.*x* is zich niet bewust van dit concept.

## at.js 2.x-diagrammen

De volgende diagrammen helpen u het werkschema van at.js 2.x met Meningen begrijpen en hoe dit de integratie van het KUUROORD verbetert. Voor een betere inleiding van de concepten die in at.js 2.x worden gebruikt, zie de implementatie [van de Toepassing van de](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/target-atjs-single-page-application.md)Enige Pagina.

![Doelstroom met at.js 2.x](/help/c-implementing-target/c-implementing-target-for-client-side-web/assets/system-diagram-atjs-20.png)

| Stap | Details |
| --- | --- |
| 1 | De vraag keert terug [!DNL Experience Cloud ID] als de gebruiker voor authentiek wordt verklaard; een andere vraag synchroniseert de klant identiteitskaart |
| 2 | De bibliotheek at.js wordt synchroon geladen en de hoofdtekst van het document verborgen.<br>at.js kan ook asynchroon worden geladen met een optioneel vooraf verborgen fragment dat op de pagina is geïmplementeerd. |
| 3 | Er wordt een aanvraag voor het laden van een pagina ingediend, inclusief alle geconfigureerde parameters (MCID, SDID en klant-id). |
| 4 | Profielscripts worden uitgevoerd en vervolgens toegevoegd aan de profielenwinkel. De winkel vraagt om gekwalificeerd publiek uit de Audience Library (bijvoorbeeld een publiek dat wordt gedeeld via Adobe Analytics, Audience Management, enz.).<br>Klantkenmerken worden in een batchproces naar de profielopslag verzonden. |
| 5 | Op basis van URL-aanvraagparameters en -profielgegevens [!DNL Target] bepaalt u welke activiteiten en ervaringen u wilt retourneren aan de bezoeker voor de huidige pagina en de toekomstige weergaven. |
| 6 | Gerichte inhoud wordt teruggestuurd naar de pagina, waarbij eventueel ook profielwaarden voor extra personalisatie worden opgenomen.<br>Gerichte inhoud op de huidige pagina wordt zo snel mogelijk zichtbaar zonder flikkering van de standaardinhoud.<br>De gerichte inhoud voor meningen die als resultaat van gebruikersacties in een KUUROORD worden getoond wordt caching in browser zodat kan het onmiddellijk zonder een extra servervraag worden toegepast wanneer de meningen door `triggerView()`. worden teweeggebracht. |
| 7 | De analysegegevens worden verzonden naar de servers van de Inzameling van Gegevens. |
| 8 | De gerichte gegevens worden aangepast aan de analysegegevens via SDID en worden verwerkt in de analytische rapporteringsopslag.<br>De analysegegevens kunnen dan in zowel Analytics als Doel via Analytics voor de rapporten van het Doel (A4T) worden bekeken. |

Nu, waar `triggerView()` op uw SPA wordt uitgevoerd, worden de Meningen en de acties teruggewonnen van geheim voorgeheugen en aan de gebruiker zonder een servervraag getoond. `triggerView()` doet ook een verzoek om meldingen aan de [!DNL Target] achterzijde om het aantal beeldpunten te verhogen en te registreren. Voor meer informatie over at.js voor SPAs met Mening, zie de implementatie [van de Toepassing van de](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/target-atjs-single-page-application.md)Enige Pagina.

![Doelstroom bij.js 2.x triggerView](/help/c-implementing-target/c-implementing-target-for-client-side-web/assets/atjs-20-triggerview.png)

| Stap | Details |
| --- | --- |
| 1 | `triggerView()` wordt geroepen in het KUUROORD om de Mening terug te geven en acties toe te passen om visuele elementen te wijzigen. |
| 2 | De gerichte inhoud voor de mening wordt gelezen van het geheime voorgeheugen. |
| 3 | Gerichte inhoud wordt zo snel mogelijk zichtbaar zonder flikkering van de standaardinhoud. |
| 4 | Aanvraag voor meldingen wordt naar de [!DNL Target] profielenwinkel verzonden om de bezoeker te tellen in de activiteit en incrementele metingen. |
| 5 | Analytische gegevens die naar de Servers van de Inzameling van Gegevens worden verzonden. |
| 6 | De doelgegevens worden via de SDID aangepast aan de analysegegevens en worden verwerkt in de analytische rapportageopslag. De analysegegevens kunnen dan in zowel Analytics als Doel via A4T- rapporten worden bekeken. |

## bij.js 1.x-diagram

![Doelstroom - bij.js 1.x](/help/c-implementing-target/c-implementing-target-for-client-side-web/assets/target-flow.png)

| Stap | Beschrijving | Bellen | Beschrijving |
|--- |--- |--- |--- |
| 1 | De vraag keert [!DNL Experience Cloud ID] (MCID) terug als de gebruiker voor authentiek wordt verklaard; een andere vraag synchroniseert de klant identiteitskaart | 2 | De bibliotheek at.js wordt synchroon geladen en de hoofdtekst van het document verborgen. |
| 3 | Er wordt een globaal mbox-verzoek ingediend, inclusief alle geconfigureerde parameters, MCID, SDID en klant-id (optioneel). | 4 | Profielscripts worden uitgevoerd en vervolgens toegevoegd aan de profielenwinkel. De winkel vraagt om gekwalificeerd publiek van de [!UICONTROL Audience Library] (bijvoorbeeld publiek dat wordt gedeeld van [!DNL Adobe Analytics], [!DNL Audience Manager]enz.).<br>Klantkenmerken worden in een batchproces naar de [!DNL Profile Store] klant verzonden. |
| 5 | Op basis van de URL, de parameters mbox en de profielgegevens [!DNL Target] bepaalt u welke activiteiten en ervaringen u wilt retourneren aan de bezoeker. | 6 | Gerichte inhoud wordt teruggestuurd naar pagina, met eventueel ook profielwaarden voor extra personalisatie.<br>De ervaring wordt zo snel mogelijk getoond zonder flikkering van standaardinhoud. |
| 7 | [!DNL Analytics] gegevens worden naar gegevensverzamelingsservers verzonden. | 8 | [!DNL Target] gegevens worden met behulp van de SDID aan [!DNL Analytics] gegevens aangepast en worden in de [!DNL Analytics] rapportageopslag verwerkt.<br>[!DNL Analytics] gegevens kunnen vervolgens zowel in [!DNL Analytics] als [!DNL Target] via [!DNL Analytics for Target] (A4T) rapporten worden bekeken. |

## Hoe geeft at.js aanbiedingen met HTML-inhoud weer {#render}

Bij rendering van aanbiedingen met HTML-inhoud past at.js het volgende algoritme toe:

1. Afbeeldingen worden vooraf geladen (als er `<img>` tags in HTML-inhoud voorkomen).

1. HTML-inhoud is gekoppeld aan het DOM-knooppunt.

1. Inline scripts worden uitgevoerd (code die in `<script>` tags wordt ingesloten).

1. Externe scripts worden asynchroon geladen en uitgevoerd (`<script>` tags met `src` kenmerken).

Belangrijke opmerkingen:

* at.js verstrekt geen garanties op de orde van verre manuscriptuitvoering, aangezien deze asynchroon worden geladen.
* Inline scripts mogen geen afhankelijkheden hebben van externe scripts, omdat deze later worden geladen en uitgevoerd.

## Trainingsvideo: bij.js 2.x het diagram van de architectuur ![Overzicht badge](/help/assets/overview.png) van het ![Overzicht badge](/help/assets/overview.png)

at.js 2.x verbetert de ondersteuning van Adobe Target voor SPA&#39;s en integreert deze met andere Experience Cloud-oplossingen. In deze video wordt uitgelegd hoe alles bij elkaar komt.

>[!VIDEO](https://video.tv.adobe.com/v/26250)

Zie [Begrijpen hoe at.js 2.x voor meer informatie werkt](https://helpx.adobe.com/target/kt/using/atjs20-diagram-technical-video-understand.html) .
