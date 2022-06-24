---
keywords: at.js;functies;javascript-bibliotheek
description: Een lijst weergeven met functies die kunnen worden gebruikt met de 1.x- en 2.x-versies van de JavaScript-bibliotheek at.js in Adobe Target.
title: Welke functies kan ik gebruiken met at.js?
feature: at.js
role: Developer
exl-id: a386e478-16f4-4bf6-9771-6b1e75f2e362
source-git-commit: 719eb95049dad3bee5925dff794871cd65969f79
workflow-type: tm+mt
source-wordcount: '685'
ht-degree: 0%

---

# at.js-functies

Lijst met functies die kunnen worden gebruikt met de JavaScript-bibliotheek Adobe Target at.js. Klik op de koppelingen in de kolom Functie voor meer informatie en voorbeelden.

| -functie | Details |
| --- | --- | 
| [adobe.target.getOffer(opties)](https://developer.adobe.com/target/implement/client-side/atjs/atjs-functions/adobe-target-getoffer/){target=_blank} | Deze functie voert een aanvraag in om een Target-aanbieding te krijgen. Gebruik met `adobe.target.applyOffer()` om de reactie te verwerken of uw eigen succesafhandeling te gebruiken. |
| [adobe.target.getOffers(opties)](https://developer.adobe.com/target/implement/client-side/atjs/atjs-functions/adobe-target-getoffers-atjs-2/){target=_blank}<br>(om 2.x.js) | Deze functie laat u veelvoudige aanbiedingen terugwinnen door in veelvoudige dozen over te gaan. Bovendien kunnen meerdere aanbiedingen worden opgehaald voor alle weergaven in actieve activiteiten.<br>**Opmerking:** Deze functie is geïntroduceerd met at.js 2.x. Deze functie is niet beschikbaar voor versie 1 van at.js.*x*. |
| [adobe.target.applyOffer(opties)](https://developer.adobe.com/target/implement/client-side/atjs/atjs-functions/adobe-target-applyoffer/){target=_blank} | Deze functie is bedoeld voor het toepassen van de inhoud van de reactie. |
| [adobe.target.applyOffers(opties)](https://developer.adobe.com/target/implement/client-side/atjs/atjs-functions/adobe-target-applyoffers-atjs-2/){target=_blank}<br>(om 2.x.js) | Met deze functie kunt u meerdere aanbiedingen toepassen die zijn opgehaald door adobe.target.getOffers().<br>**Opmerking:** Deze functie is geïntroduceerd met at.js 2.x. Deze functie is niet beschikbaar voor versie 1 van at.js.*x*. |
| [adobe.target.triggerView (viewName, options)](https://developer.adobe.com/target/implement/client-side/atjs/atjs-functions/adobe-target-triggerview-atjs-2/){target=_blank}<br>(om 2.x.js) | Deze functie kan worden aangeroepen wanneer een nieuwe pagina wordt geladen of wanneer een component op een pagina opnieuw wordt weergegeven.<br> Deze functie zou voor enige paginatoepassingen (SPA) {target=_blank} moeten worden uitgevoerd om de Visuele Composer van de Ervaring (VEC) te gebruiken om A/B Tests en Ervaring te creëren richtend (XT) activiteiten. |
| [adobe.target.trackEvent(options)](https://developer.adobe.com/target/implement/client-side/atjs/atjs-functions/adobe-target-trackevent/){target=_blank} | Deze functie voert een verzoek in om gebruikersacties, zoals kliks en omzettingen te melden. Het levert geen activiteiten in de reactie. |
| [mboxCreate(mbox,params)](https://developer.adobe.com/target/implement/client-side/atjs/atjs-functions/mboxcreate-atjs/){target=_blank}<br>(om 1.js) | Voert een verzoek uit en past de aanbieding op dichtstbijzijnde div met mboxDefault klassennaam toe.<br>**Opmerking:** Deze functie is beschikbaar voor at.js versies 1.*x* alleen. Deze functie is vervangen door de release van at.js 2.x. Deze functie retourneert standaardinhoud als deze wordt gebruikt met at.js 2.x. |
| [mboxDefine(options) en mboxUpdate(options)](https://developer.adobe.com/target/implement/client-side/atjs/atjs-functions/mboxdefine-mboxupdate-atjs-1x/){target=_blank}<br>(om 1.js) | Een box definiëren en bijwerken.<br>**Opmerking:** Deze functie is beschikbaar voor at.js versies 1.*x* alleen. Deze functie is vervangen door de release van at.js 2.x. Deze functie retourneert standaardinhoud als deze wordt gebruikt met at.js 2.x. |
| [targetGlobalSettings(opties)](https://developer.adobe.com/target/implement/client-side/atjs/atjs-functions/targetglobalsettings/){target=_blank} | U kunt instellingen in de bibliotheek at.js overschrijven met `targetGlobalSettings()`, in plaats van de instellingen te configureren in de standaardinterface/Premium van het doel of met REST API&#39;s.<ul><li>Gegevensleveranciers: Met deze instelling kunnen klanten gegevens verzamelen van gegevensleveranciers van derden, zoals Demandbase, BlueKai en aangepaste services, en de gegevens doorgeven aan Target als mbox-parameters in het algemene mbox-verzoek.</li></ul> |
| [targetPageParams(opties)](https://developer.adobe.com/target/implement/client-side/atjs/atjs-functions/targetpageparams/){target=_blank} | Met deze methode kunt u parameters aan de globale mbox koppelen van buiten de aanvraagcode. |
| [targetPageParamsAll(options)](https://developer.adobe.com/target/implement/client-side/atjs/atjs-functions/targetpageparamsall/){target=_blank} | Met deze methode kunt u parameters koppelen aan alle vakken van buiten de aanvraagcode. |
| [registerExtension(options)](https://developer.adobe.com/target/implement/client-side/atjs/atjs-functions/registerextension-atjs-1x/){target=_blank}<br>(om 1.js) | Verstrekt een standaardmanier om een specifieke uitbreiding te registreren.<br>**Opmerking:** Deze functie is beschikbaar voor at.js versies 1.*x* alleen. Deze functie is vervangen door de release van at.js 2.x. Deze functie retourneert standaardinhoud als deze wordt gebruikt met at.js 2.x. |
| [at.js, aangepaste gebeurtenissen](https://developer.adobe.com/target/implement/client-side/atjs/atjs-functions/atjs-custom-events/){target=_blank} | op.js laten de douanegebeurtenissen u weten wanneer een mbox- verzoek of een aanbieding ontbreekt of slaagt. |
| [adobe.target.sendNotifications(options)](https://developer.adobe.com/target/implement/client-side/atjs/atjs-functions/adobe-target-sendnotifications-atjs-21/){target=_blank}<br>(js 2.1.0) | Deze functie verzendt een bericht naar de rand van het Doel wanneer een ervaring zonder het gebruiken wordt teruggegeven `adobe.target.applyOffer()` of `adobe.target.applyOffers()`.<br>**Opmerking**: Deze functie is geïntroduceerd in at.js 2.1.0 en zal voor om het even welke versies boven 2.1.0 beschikbaar zijn. |
