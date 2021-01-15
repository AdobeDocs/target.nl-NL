---
keywords: document.write;target;implement;implement target;dtm;dynamic tag management;at.js;mbox.js;target.js;mbox;adobe experience platform web skd;aep web sdk;web sdk
description: Implementeer Adobe Target door te verwijzen naar de doelbibliotheken (at.js of mbox.js) op uw webpagina's.
title: JavaScript-doelbibliotheken begrijpen
feature: Implementation
translation-type: tm+mt
source-git-commit: a85a5c10c31fb0d7eb00c21ff03b2012d044de45
workflow-type: tm+mt
source-wordcount: '684'
ht-degree: 0%

---


# De JavaScript-bibliotheken [!DNL Target] begrijpen

Implementeer [!DNL Target] door te verwijzen naar de [!DNL Adobe Target]-bibliotheken (Adobe Experience Platform Web SDK, at.js of mbox.js) op uw webpagina&#39;s.

>[!NOTE]
>
>De bibliotheek mbox.js wordt niet meer ontwikkeld. Alle klanten moeten van mbox.js naar at.js migreren. Zie [Migreren naar at.js vanuit mbox.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-target-atjs-implementation/target-migrate-atjs.md#task_DE55DCE9AC2F49728395665DE1B1E6EA) voor meer informatie.

## Verschillen tussen de JavaScript-doelbibliotheken {#section_40117C78C2F84FECAC4F1BA40CC4F171}

In de volgende tabel worden de verschillen tussen de JavaScript-bibliotheken [!DNL Target] uitgelegd:

| Bibliotheekreferentie | Beschrijving |
|--- |--- |
| Adobe Experience Platform Web SDK | Met [!UICONTROL Adobe Experience Platform Web SDK] kunt u via het Adobe Experience Edge Network communiceren met de verschillende services in [!DNL Experience Cloud] (inclusief [!DNL Target]). Als u ervoor kiest om naar [!DNL Adobe Experience Platform Web SDK] te migreren, zie [Wat is Adobe Experience Platform Web SDK](/help/c-implementing-target/c-implementing-target-for-client-side-web/aep-web-sdk.md) in *Web SDK Guide*. |
| at.js | at.js vervangt mbox.js voor [!DNL [!DNL Target]] implementaties.<br>Met at.js worden onder andere de laadtijden voor webimplementaties verbeterd, wordt de beveiliging verbeterd, wordt voorkomen dat documenten.write-waarschuwingen in Google Chrome verschijnen en worden betere implementatieopties geboden voor toepassingen van één pagina.<br>Zie  [at.js Implementation](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-target-atjs-implementation/target-atjs-implementation.md) voor meer informatie. |
| mbox.js | Vóór [!DNL Target] 16.3.1 (Maart 2016), vereiste [!DNL Target] een vraag aan mbox.js om globale mbox tot stand te brengen die voor [!DNL Target] wordt vereist om activiteiten te leveren, kliks te volgen, en de meeste succesmetriek te volgen. Dit bestand bevat de bibliotheken die nodig zijn voor al uw activiteiten. U hoeft geen verschillende activiteitspecifieke versies van het bestand te onderhouden.<br>Als u reeds het verpakken vakjes op uw pagina&#39;s van een oudere stijl van  [!DNL Target] implementatie hebt, kunnen deze vakjes nog in de nieuwe interface worden gebruikt. Het bijgewerkte bestand mbox.js is nog steeds vereist, maar deze vakken kunnen worden geselecteerd voor activiteiten en bewerkt met de Visual Experience Composer.<br>[!DNL Target] Standard- en Premium-update en -supplement mbox.js met een verwijzing naar het bestand target.js. Het bestand target.js wordt gehost door Adobe. Met het bestand Target.js kunt u inhoud op elke pagina bewerken met behulp van Visual Experience Composer, zelfs als de pagina geen vooraf gedefinieerde vakken bevat. U moet naar dit bestand verwijzen op elke pagina op uw site.<br>Zie  [mbox.js Implementation](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/mbox-download.md) voor meer informatie.<br>**Belangrijk**: Op 31 maart 2021  [!DNL Adobe Target] wordt de bibliotheek mbox.js niet meer ondersteund. Na 31 maart 2021 zullen alle aanroepen van mbox.js netjes mislukken en van invloed zijn op uw pagina&#39;s die [!DNL Target] activiteiten hebben die door standaardinhoud te dienen worden uitgevoerd. We raden alle klanten aan vóór deze datum naar de meest recente versie van de nieuwe [!DNL Adobe Experience Platform Web SDK] of de JavaScript-bibliotheek at.js te migreren om mogelijke problemen met uw sites te voorkomen.<br> |

## Effect van at.js en mbox.js op pagina-laadtijd {#section_16630CD0FF0A498EB596A51381366A5A}

Veel klanten en consultants willen weten wat de gevolgen zijn van [!DNL at.js] en [!DNL mbox.js] voor de laadtijd van de pagina, vooral in de context van nieuwe gebruikers of terugkerende gebruikers. Jammer genoeg, is het moeilijk om concrete aantallen betreffende te meten en te geven hoe [!DNL at.js] of [!DNL mbox.js] paginaoplaadtijd wegens de implementatie van elke klant beïnvloeden.

Als de API voor bezoekers echter aanwezig is op de pagina, kunnen we beter begrijpen hoe [!DNL at.js] en [!DNL mbox.js] de laadtijd van pagina&#39;s beïnvloeden.

>[!NOTE]
>
>De API voor bezoekers en [!DNL at.js] of [!DNL mbox.js] hebben alleen invloed op de laadtijd van de pagina wanneer u de globale box gebruikt (vanwege de body-hide techniek). De regionale mboxes worden niet beïnvloed door de integratie van de Bezoeker API.

De volgende secties beschrijven de opeenvolging van acties voor nieuwe en terugkerende bezoekers:

### Nieuwe bezoekers

1. De bezoeker-API wordt geladen, geparseerd en uitgevoerd.
1. at.js / mbox.js wordt geladen, geparseerd en uitgevoerd.
1. Als Automatisch maken van globale box is ingeschakeld, wordt de JavaScript-doelbibliotheek gebruikt:

   * Instantieert het object Visitor.
   * De doelbibliotheek probeert de gegevens van de Experience Cloud Visitor-id op te halen.
   * Omdat dit een nieuwe bezoeker is, leidt de bezoeker-API een aanvraag voor een ander domein in naar demdex.net.
   * Nadat de gegevens van de identiteitskaart van de Bezoeker van Experience Cloud worden teruggewonnen, wordt een verzoek aan Doel in brand gestoken.

### Bezoekers terugsturen

1. De bezoeker-API wordt geladen, geparseerd en uitgevoerd.
1. at.js / mbox.js wordt geladen, geparseerd en uitgevoerd.
1. Als Automatisch maken van globale box is ingeschakeld, wordt de JavaScript-doelbibliotheek gebruikt:

   * Instantieert het object Visitor.
   * De doelbibliotheek probeert de gegevens van de Experience Cloud Visitor-id op te halen.
   * De bezoeker-API haalt gegevens op uit cookies.
   * Nadat de gegevens van de identiteitskaart van de Bezoeker van Experience Cloud worden teruggewonnen, wordt een verzoek aan Doel in brand gestoken.

>[!NOTE]
>
>Voor nieuwe bezoekers, wanneer de Bezoeker-API aanwezig is, moet Target meerdere keren over de kabel gaan om ervoor te zorgen dat de doelaanvragen gegevens van de Experience Cloud Bezoeker-id bevatten. Voor terugkerende bezoekers, gaat het Doel over de draad slechts aan Doel om de gepersonaliseerde inhoud terug te winnen.
