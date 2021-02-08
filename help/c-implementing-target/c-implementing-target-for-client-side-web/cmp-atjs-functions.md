---
keywords: at.js;functies;javascript-bibliotheek
description: Een lijst weergeven met functies die kunnen worden gebruikt met de 1.x- en 2.x-versies van de JavaScript-bibliotheek at.js in Adobe Target.
title: Welke functies kan ik gebruiken met at.js?
feature: at.js
role: Developer
translation-type: tm+mt
source-git-commit: bb27f6e540998f7dbe7642551f7a5013f2fd25b4
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# at.js-functies{#at-js-functions}

Lijst met functies die kunnen worden gebruikt met de JavaScript-bibliotheek Adobe Target at.js. Klik op de koppelingen in de kolom Functie voor meer informatie en voorbeelden.

| -functie | Details |
| --- | --- | 
| [adobe.target.getOffer(opties)](/help/c-implementing-target/c-implementing-target-for-client-side-web/adobe-target-getoffer.md) | Deze functie voert een aanvraag in om een Target-aanbieding te krijgen. Gebruik deze methode met `adobe.target.applyOffer()` om de reactie te verwerken of uw eigen succesafhandeling te gebruiken. |
| [adobe.target.getOffers(opties)](/help/c-implementing-target/c-implementing-target-for-client-side-web/adobe-target-getoffers-atjs-2.md)<br>(at.js 2.x) | Deze functie laat u veelvoudige aanbiedingen terugwinnen door in veelvoudige dozen over te gaan. Bovendien kunnen meerdere aanbiedingen worden opgehaald voor alle weergaven in actieve activiteiten.<br>**Opmerking:** deze functie is geïntroduceerd met at.js 2.x. Deze functie is niet beschikbaar voor versie 1 van at.js.*x*. |
| [adobe.target.applyOffer(opties)](/help/c-implementing-target/c-implementing-target-for-client-side-web/adobe-target-applyoffer.md) | Deze functie is bedoeld voor het toepassen van de inhoud van de reactie. |
| [adobe.target.applyOffers(options)](/help/c-implementing-target/c-implementing-target-for-client-side-web/adobe-target-applyoffers-atjs-2.md)<br>(at.js 2.x) | Met deze functie kunt u meerdere aanbiedingen toepassen die zijn opgehaald door adobe.target.getOffers().<br>**Opmerking:** deze functie is geïntroduceerd met at.js 2.x. Deze functie is niet beschikbaar voor versie 1 van at.js.*x*. |
| [adobe.target.triggerView (viewName, options)](/help/c-implementing-target/c-implementing-target-for-client-side-web/adobe-target-triggerview-atjs-2.md)<br>(at.js 2.x) | Deze functie kan worden aangeroepen wanneer een nieuwe pagina wordt geladen of wanneer een component op een pagina opnieuw wordt weergegeven.<br> Deze functie zou voor enige paginatoepassingen (SPA) moeten worden uitgevoerd om Visual Experience Composer (VEC) te gebruiken om A/B Tests en Ervaring te creëren richtend (XT) activiteiten. |
| [adobe.target.trackEvent(options)](/help/c-implementing-target/c-implementing-target-for-client-side-web/adobe-target-trackevent.md) | Deze functie voert een verzoek in om gebruikersacties, zoals kliks en omzettingen te melden. Het levert geen activiteiten in de reactie. |
| [mboxCreate(mbox,params)](/help/c-implementing-target/c-implementing-target-for-client-side-web/mboxcreate-atjs.md)<br>(at.js 1.x) | Voert een verzoek uit en past de aanbieding op dichtstbijzijnde div met mboxDefault klassennaam toe.<br>**Opmerking:** deze functie is beschikbaar voor at.js versies 1.** Alleen. Deze functie is vervangen door de release van at.js 2.x. Deze functie retourneert standaardinhoud als deze wordt gebruikt met at.js 2.x. |
| [mboxDefine(options) en mboxUpdate(options)](/help/c-implementing-target/c-implementing-target-for-client-side-web/mboxdefine-mboxupdate-atjs-1x.md)<br>(at.js 1.x) | Een box definiëren en bijwerken.<br>**Opmerking:** deze functie is beschikbaar voor at.js versies 1.** Alleen. Deze functie is vervangen door de release van at.js 2.x. Deze functie retourneert standaardinhoud als deze wordt gebruikt met at.js 2.x. |
| [targetGlobalSettings(opties)](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetgobalsettings.md) | U kunt instellingen in de bibliotheek at.js overschrijven met behulp van `targetGlobalSettings()` in plaats van de instellingen in de gebruikersinterface van Target Standard/Premium te configureren of met behulp van REST API&#39;s.<ul><li>Gegevensleveranciers: Met deze instelling kunnen klanten gegevens verzamelen van gegevensleveranciers van derden, zoals Demandbase, BlueKai en aangepaste services, en de gegevens doorgeven aan Target als mbox-parameters in het algemene mbox-verzoek.</li></ul> |
| [targetPageParams(opties)](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetpageparams.md) | Met deze methode kunt u parameters aan de globale mbox koppelen van buiten de aanvraagcode. |
| [targetPageParamsAll(options)](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetpageparamsall.md) | Met deze methode kunt u parameters koppelen aan alle vakken van buiten de aanvraagcode. |
| [registerExtension(options)](/help/c-implementing-target/c-implementing-target-for-client-side-web/registerextension-atjs-1x.md)<br>(at.js 1.x) | Verstrekt een standaardmanier om een specifieke uitbreiding te registreren.<br>**Opmerking:** deze functie is beschikbaar voor at.js versies 1.** Alleen. Deze functie is vervangen door de release van at.js 2.x. Deze functie retourneert standaardinhoud als deze wordt gebruikt met at.js 2.x. |
| [at.js, aangepaste gebeurtenissen](/help/c-implementing-target/c-implementing-target-for-client-side-web/atjs-custom-events.md) | op.js laten de douanegebeurtenissen u weten wanneer een mbox- verzoek of een aanbieding ontbreekt of slaagt. |
| [adobe.target.sendNotifications(options)](/help/c-implementing-target/c-implementing-target-for-client-side-web/adobe.target.sendnotifications-atjs-21.md)<br>(at.js 2.1.0) | Deze functie verzendt een bericht naar de rand van het Doel wanneer een ervaring wordt teruggegeven zonder `adobe.target.applyOffer()` of `adobe.target.applyOffers()` te gebruiken.<br>**Opmerking**: Deze functie is geïntroduceerd in at.js 2.1.0 en zal voor om het even welke versies boven 2.1.0 beschikbaar zijn. |

