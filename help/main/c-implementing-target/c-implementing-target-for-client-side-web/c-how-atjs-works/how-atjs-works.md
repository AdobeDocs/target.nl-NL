---
keywords: systeemdiagram;flicker;at.js;implementatie;javascript-bibliotheek;js;atjs
description: Meer informatie over [!DNL Target] in.js JavaScript-bibliotheekfuncties, waaronder systeemdiagrammen, waarmee u de workflow tijdens het laden van pagina's kunt begrijpen.
title: Hoe werkt de JavaScript-bibliotheek at.js?
feature: at.js
role: Developer
exl-id: 2193c02a-2a85-4ae1-bfbd-40fa7b87f0a0
source-git-commit: a0a20b99a76ba0346f00e3841a345e916ffde8ea
workflow-type: tm+mt
source-wordcount: '1136'
ht-degree: 2%

---

# Hoe werkt at.js

Om [!DNL Adobe Target] aan clientzijde, moet u de JavaScript-bibliotheek at.js gebruiken.

Bij een clientimplementatie van [!DNL Adobe Target], [!DNL Target] levert de ervaringen verbonden aan een activiteit rechtstreeks aan cliëntbrowser. De browser bepaalt welke ervaring wordt weergegeven en geeft deze weer. Met een cliënt-zijimplementatie, kunt u een redacteur gebruiken WYSIWYG, [Visual Experience Composer](/help/main/c-experiences/c-visual-experience-composer/visual-experience-composer.md) (VEC) of een niet-visuele interface [Form-based Experience Composer](/help/main/c-experiences/form-experience-composer.md), om uw test- en personaliservaringen te maken.

## Wat is at.js?

De bibliotheek at.js is de nieuwe implementatiebibliotheek voor Doel. De bibliotheek at.js verbetert de laadtijden voor webimplementaties en biedt betere implementatieopties voor toepassingen van één pagina. at.js is de aanbevolen implementatiebibliotheek en wordt regelmatig bijgewerkt met nieuwe mogelijkheden. Wij adviseren dat alle klanten uitvoeren of aan migreren [nieuwste versie van at.js](https://developer.adobe.com/target/implement/client-side/atjs/target-atjs-versions/).

Zie voor meer informatie [JavaScript-doelbibliotheken](/help/main/c-intro/how-target-works.md#libraries).

In de [!DNL Target] hieronder weergegeven, de volgende [!DNL Adobe Experience Cloud] oplossingen worden geïmplementeerd: Analytics, Target en Audience Manager. Daarnaast worden de volgende Experience Cloud core services geïmplementeerd: [!DNL Adobe Experience Platform], [!DNL Audiences], en [!DNL Visitor ID Service].

## Wat is het verschil tussen at.js 1.*x* en werkstroomdiagrammen bij .js 2.x?

Zie [Bijwerken van at.js 1.x naar at.js 2.x](https://developer.adobe.com/target/implement/client-side/atjs/target-atjs-versions/){target=_blank} voor meer informatie over de verschillen die zijn geïntroduceerd in 2.O vanaf 1.*x*.

Vanuit een weergave op hoog niveau zijn er enkele verschillen tussen de twee versies:

* at.js 2.x heeft geen globaal mbox verzoekconcept maar eerder een pagina-lading verzoek. Een verzoek om pagina&#39;s te laden kan worden beschouwd als een verzoek om inhoud op te halen die moet worden toegepast op het eerste laadmoment van de pagina van uw website.
* at.js 2.x beheert de concepten Weergaven, die worden gebruikt voor toepassingen voor één pagina (SPA). te.js 1.*x* is zich niet bewust van dit concept.

## at.js 2.x-diagrammen

Met de volgende diagrammen krijgt u inzicht in de workflow van at.js 2.x met weergaven en in de manier waarop dit de integratie van SPA verbetert. Voor een betere inleiding van de concepten die in at.js 2.x worden gebruikt, zie [Toepassing van één pagina](https://developer.adobe.com/target/implement/client-side/atjs/how-to-deployatjs/target-atjs-single-page-application/).

![Doelstroom met at.js 2.x](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/assets/system-diagram-atjs-20.png)

| Stap | Details |
| --- | --- |
| 1 | De vraag keert terug [!DNL Experience Cloud ID] indien de gebruiker is geverifieerd; een andere vraag synchroniseert de klant identiteitskaart |
| 2 | De bibliotheek at.js wordt synchroon geladen en de hoofdtekst van het document verborgen.<br>at.js kan ook asynchroon worden geladen met een optioneel vooraf verborgen fragment dat op de pagina is geïmplementeerd. |
| 3 | Er wordt een aanvraag voor het laden van een pagina ingediend, inclusief alle geconfigureerde parameters (MCID, SDID en klant-id). |
| 4 | Profielscripts worden uitgevoerd en vervolgens toegevoegd aan de profielenwinkel. De winkel vraagt om gekwalificeerd publiek uit de Audience Library (bijvoorbeeld publiek dat wordt gedeeld vanuit Adobe Analytics, Publiek beheer, enz.).<br>Klantkenmerken worden in een batchproces naar de profielopslag verzonden. |
| 5 | Gebaseerd op parameters en profielgegevens van het URL-verzoek, [!DNL Target] bepaalt welke activiteiten en ervaringen u wilt retourneren aan de bezoeker voor de huidige pagina en de toekomstige weergaven. |
| 6 | Gerichte inhoud wordt teruggestuurd naar de pagina, waarbij eventueel ook profielwaarden voor extra personalisatie worden opgenomen.<br>Gerichte inhoud op de huidige pagina wordt zo snel mogelijk zichtbaar zonder flikkering van de standaardinhoud.<br>Gerichte inhoud voor weergaven die worden weergegeven als gevolg van gebruikershandelingen in een SPA, wordt in de browser in cache geplaatst, zodat deze direct kan worden toegepast zonder een extra serveraanroep wanneer de weergaven worden geactiveerd `triggerView()`. |
| 7 | De analysegegevens worden verzonden naar de servers van de Inzameling van Gegevens. |
| 8 | De gerichte gegevens worden aangepast aan de analysegegevens via SDID en worden verwerkt in de analytische rapporteringsopslag.<br>De analysegegevens kunnen dan in zowel Analytics als Doel via Analytics voor de rapporten van het Doel (A4T) worden bekeken. |

Nu, waar dan ook `triggerView()` wordt geïmplementeerd op uw SPA, worden de weergaven en acties opgehaald uit het cachegeheugen en aan de gebruiker getoond zonder een serveraanroep. `triggerView()` verzoekt de Commissie tevens [!DNL Target] achterkant om het aantal beeldingen te verhogen en op te nemen. Ga voor meer informatie over at.js voor SPA met Weergaven naar [Toepassing van één pagina](https://developer.adobe.com/target/implement/client-side/atjs/how-to-deployatjs/target-atjs-single-page-application/).

![Doelstroom bij.js 2.x triggerView](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/assets/atjs-20-triggerview.png)

| Stap | Details |
| --- | --- |
| 1 | `triggerView()` wordt opgeroepen in de SPA om de weergave te renderen en acties toe te passen om visuele elementen te wijzigen. |
| 2 | De gerichte inhoud voor de mening wordt gelezen van het geheime voorgeheugen. |
| 3 | Gerichte inhoud wordt zo snel mogelijk zichtbaar zonder flikkering van de standaardinhoud. |
| 4 | Aanmelding wordt verzonden naar de [!DNL Target] De Opslag van het profiel om de bezoeker in de activiteit en verhogingsmetriek te tellen. |
| 5 | Analytische gegevens die naar de Servers van de Inzameling van Gegevens worden verzonden. |
| 6 | De doelgegevens worden via de SDID aangepast aan de analysegegevens en worden verwerkt in de analytische rapportageopslag. De analysegegevens kunnen dan in zowel Analytics als Doel via A4T- rapporten worden bekeken. |

### Video - op.js 2.x architecturaal diagram

at.js 2.x verbetert de Adobe Target-ondersteuning voor SPA en integreert deze met andere Experience Cloud-oplossingen. In deze video wordt uitgelegd hoe alles bij elkaar komt.

>[!VIDEO](https://video.tv.adobe.com/v/26250)

Zie [Begrijpen hoe at.js 2.x werkt](https://helpx.adobe.com/target/kt/using/atjs20-diagram-technical-video-understand.html) voor meer informatie .

## bij.js 1.x-diagram

![Doelstroom - bij.js 1.x](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/assets/target-flow.png)

| Stap | Beschrijving | Bellen | Beschrijving |
|--- |--- |--- |--- |
| 1 | De vraag keert terug [!DNL Experience Cloud ID] (MCID) als de gebruiker is geverifieerd; een andere vraag synchroniseert de klant identiteitskaart | 2 | De bibliotheek at.js wordt synchroon geladen en de hoofdtekst van het document verborgen. |
| 3 | Er wordt een globaal mbox-verzoek ingediend, inclusief alle geconfigureerde parameters, MCID, SDID en klant-id (optioneel). | 4 | Profielscripts worden uitgevoerd en vervolgens toegevoegd aan de profielenwinkel. De winkel vraagt een gekwalificeerd publiek aan via [!UICONTROL Audience Library] (bijvoorbeeld publiek dat wordt gedeeld vanuit [!DNL Adobe Analytics], [!DNL Audience Manager], enz.).<br>Klantkenmerken worden naar de [!DNL Profile Store] in een batchproces. |
| 5 | Gebaseerd op URL, mbox parameters, en profielgegevens, [!DNL Target] bepaalt welke activiteiten en ervaringen moeten worden teruggegeven aan de bezoeker. | 6 | Gerichte inhoud wordt teruggestuurd naar pagina, met eventueel ook profielwaarden voor extra personalisatie.<br>De ervaring wordt zo snel mogelijk getoond zonder flikkering van standaardinhoud. |
| 7 | [!DNL Analytics] gegevens worden naar gegevensverzamelingsservers verzonden. | 8 | [!DNL Target] gegevens komen overeen met [!DNL Analytics] gegevens via de SDID en worden verwerkt in de [!DNL Analytics]  rapporteringsopslag.<br>[!DNL Analytics] gegevens kunnen vervolgens in beide worden weergegeven [!DNL Analytics] en  [!DNL Target] via [!DNL Analytics for Target] (A4T) verslagen. |

### Video - kantooruren: tips en overzicht op .js (26 juni 2019)

Deze video is een opname van &quot;Office Hours&quot;, een initiatief onder leiding van het Adobe Customer Care-team.

* Voordelen van het gebruik van at.js
* at.js-instellingen
* Flikkerverwerking
* Foutopsporing bij.js
* Bekende problemen
* Veelgestelde vragen

>[!VIDEO](https://video.tv.adobe.com/v/27959)

## Hoe at.js aanbiedingen met HTML-inhoud rendert {#render}

Bij rendering van aanbiedingen met HTML-inhoud past at.js het volgende algoritme toe:

1. Afbeeldingen worden vooraf geladen (als er `<img>` -tags in HTML-inhoud).

1. HTML-inhoud is gekoppeld aan het DOM-knooppunt.

1. Inline scripts worden uitgevoerd (code omsloten in `<script>` -tags).

1. Externe scripts worden asynchroon geladen en uitgevoerd (`<script>` tags met `src` kenmerken).

Belangrijke opmerkingen:

* at.js verstrekt geen garanties op de orde van verre manuscriptuitvoering, aangezien deze asynchroon worden geladen.
* Inline scripts mogen geen afhankelijkheden hebben van externe scripts, omdat deze later worden geladen en uitgevoerd.
