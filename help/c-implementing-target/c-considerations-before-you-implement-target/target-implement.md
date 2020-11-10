---
keywords: document.write;target;implement;implement target;dtm;dynamic tag management;at.js;mbox.js;target.js;mbox
description: Implementeer Doel door naar de doelbibliotheken (at.js of mbox.js) op uw webpagina's te verwijzen.
title: JavaScript-doelbibliotheken begrijpen
feature: implementation general
translation-type: tm+mt
source-git-commit: 968d36d65016e51290f6bf754f69c91fd8f68405
workflow-type: tm+mt
source-wordcount: '601'
ht-degree: 0%

---


# De [!DNL Target] JavaScript-bibliotheken begrijpen{#understand-the-target-javascript-libraries}

Implementeer [!DNL Target] door te verwijzen naar de [!DNL Target] bibliotheken (at.js of mbox.js) op uw webpagina&#39;s.

>[!NOTE]
>
>De bibliotheek mbox.js wordt niet meer ontwikkeld. Alle klanten moeten van mbox.js naar at.js migreren. Zie [Migreren naar at.js vanuit mbox.js voor meer informatie](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-target-atjs-implementation/target-migrate-atjs.md#task_DE55DCE9AC2F49728395665DE1B1E6EA).

## Verschillen tussen de twee bibliotheken {#section_40117C78C2F84FECAC4F1BA40CC4F171}

In de volgende tabel worden de verschillen tussen de twee bibliotheken uitgelegd:

| Bibliotheekreferentie | Beschrijving |
|--- |--- |
| at.js | bij.js vervangt mbox.js voor [!DNL Target] implementaties.<br>Met at.js worden onder andere de laadtijden voor webimplementaties verbeterd, wordt de beveiliging verbeterd, wordt voorkomen dat documenten.write-waarschuwingen in Google Chrome verschijnen en worden betere implementatieopties geboden voor toepassingen van één pagina.<br>Zie [at.js Implementation](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-target-atjs-implementation/target-atjs-implementation.md)voor meer informatie. |
| mbox.js | Voorafgaand aan [!DNL Target] 16.3.1 (Maart 2016), [!DNL Target] [!DNL Target] vereiste een vraag aan mbox.js om globale mbox tot stand te brengen die wordt vereist om activiteiten te leveren, kliks te volgen, en de meeste succesmetriek te volgen. Dit bestand bevat de bibliotheken die nodig zijn voor al uw activiteiten. U hoeft geen verschillende activiteitspecifieke versies van het bestand te onderhouden.<br>Als u reeds het verpakken vakjes op uw pagina&#39;s van een oudere stijl van [!DNL Target] implementatie hebt, kunnen deze vakjes nog in de nieuwe interface worden gebruikt. Het bijgewerkte bestand mbox.js is nog steeds vereist, maar deze vakken kunnen worden geselecteerd voor activiteiten en bewerkt met de Visual Experience Composer.<br>[!DNL Target] Standard- en Premium-update en -supplement mbox.js met een verwijzing naar het bestand target.js. Het bestand target.js wordt gehost door Adobe. Met het bestand Target.js kunt u inhoud op elke pagina bewerken met behulp van Visual Experience Composer, zelfs als de pagina geen vooraf gedefinieerde vakken bevat. U moet naar dit bestand verwijzen op elke pagina op uw site.<br>Zie [mbox.js Implementation](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/mbox-download.md)voor meer informatie.<br>**Belangrijk**: De bibliotheek mbox.js wordt nog steeds ondersteund, maar er zijn geen functie-updates. Alle klanten moeten naar om.js migreren. Zie [Migreren naar at.js vanuit mbox.js voor meer informatie](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-target-atjs-implementation/target-migrate-atjs.md)<br> |

## Effect van at.js en mbox.js op de tijd van het laden van de pagina {#section_16630CD0FF0A498EB596A51381366A5A}

Veel klanten en consultants willen weten wat de impact is van [!DNL at.js] en [!DNL mbox.js] op de laadtijd van pagina&#39;s, met name in de context van nieuwe gebruikers of gebruikers die terugkeren. Jammer genoeg, is het moeilijk om concrete aantallen betreffende te meten en te geven hoe [!DNL at.js] of [!DNL mbox.js] beïnvloedt pagina-lading tijd toe te schrijven aan de implementatie van elke klant.

Als de API voor bezoekers echter aanwezig is op de pagina, kunnen we beter begrijpen hoe [!DNL at.js] en [!DNL mbox.js] invloed deze tijd heeft.

>[!NOTE]
>
>De API voor bezoekers en [!DNL at.js] of [!DNL mbox.js] hebben alleen invloed op de laadtijd van de pagina wanneer u de globale box gebruikt (vanwege de techniek voor het verbergen van de hoofdtekst). De regionale mboxes worden niet beïnvloed door de integratie van de Bezoeker API.

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
