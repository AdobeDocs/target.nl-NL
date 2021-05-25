---
keywords: Opmerkingen bij de release;nieuwe functies;releases;updates;update;release;verbetering;verbeteringen;correcties;foutoplossingen;updates
description: Leer meer over de nieuwe functies, verbeteringen en oplossingen die zijn opgenomen in de huidige versie van Adobe Target, waaronder SDK's, API's en JavaScript-bibliotheken.
title: Welke nieuwe eigenschappen worden inbegrepen in de huidige Versie?
feature: Opmerkingen bij de release
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
source-git-commit: d102e3b93e258199bad40de089443eda3a07d7fe
workflow-type: tm+mt
source-wordcount: '630'
ht-degree: 0%

---

# Opmerkingen bij de doelversie (huidig)

Deze releaseopmerkingen bevatten informatie over functies, verbeteringen en oplossingen voor elke [!DNL Adobe Target Standard]- en [!DNL Target Premium]-versie. Daarnaast worden releaseopmerkingen voor doel-API&#39;s, SDK&#39;s, de JavaScript-bibliotheek (at.js) en andere platformwijzigingen, indien van toepassing, ook opgenomen.

>[!IMPORTANT]
>
>**mbox.js end-of-life**: Vanaf 31 maart 2021 wordt de bibliotheek mbox.js  [!DNL Adobe Target] niet meer ondersteund. Na 31 maart 2021 zullen alle aanroepen van mbox.js netjes mislukken en van invloed zijn op uw pagina&#39;s die [!DNL Target] activiteiten hebben die door standaardinhoud te dienen worden uitgevoerd.
>
>Migreer naar de meest recente versie van de nieuwe [!DNL Adobe Experience Platform Web SDK] of de JavaScript-bibliotheek at.js om mogelijke problemen met uw sites te voorkomen. Voor meer informatie, zie [Overzicht: Implementeer Doel voor client-side web](/help/c-implementing-target/c-implementing-target-for-client-side-web/implement-target-for-client-side-web.md).

(De uitgiftenummers tussen haakjes zijn bedoeld voor intern gebruik [!DNL Adobe].)

## at.js versie 2.5.0 (13 mei 2021)

Deze versie van at.js bevat de volgende verbeteringen en wijzigingen:

* [Ondersteuning voor ](/help/c-implementing-target/c-implementing-target-for-client-side-web/on-device-decisioning/on-device-decisioning.md) beslissingen op het apparaat voor at.js.
* [Ondersteuning voor ](/help/c-activities/c-activity-qa/activity-qa.md) koppelingen voorvertonen voor Automated Personalization-activiteiten

Deze versie verwijdert ook ondersteuning voor Microsoft Internet Explorer 10, Internet Explorer 11 en alle oudere versies. Microsoft Edge wordt nog steeds ondersteund in at.js 2.5.0 en hoger.

## Target Standard/Premium 21.4.1 (19 april 2021)

Deze versie bevat de volgende nieuwe functies en verbeteringen. De uitgiftenummers tussen haakjes zijn bedoeld voor intern gebruik [!DNL Adobe].

| Functie | Details |
| --- | --- |
| Apparaatondersteuning voor beslissingen voor at.js<br>(Datum die moet worden aangekondigd) | Met apparaatbeslissingen kunnen marketers en ontwikkelaars experimenten en personalisatie uitvoeren in de browser van een gebruiker bij bijna-nullatentie.<br>Voor meer informatie, zie  [Op-apparatenbesluit voor at.js.](/help/c-implementing-target/c-implementing-target-for-client-side-web/on-device-decisioning/on-device-decisioning.md) |
| ![Op ](/help/assets/premium.png) PremiumList gebaseerde operatoren voor filterregels voor entiteiten | [!DNL Target Recommendations] steunt nieuwe op lijst-gebaseerde exploitanten voor entiteit het filtreren regels. (TGT-39234)<br>Nieuw toegevoegde operatoren zijn onder andere:<br><ul><li>Is opgenomen in lijst</li><li>Is niet opgenomen in lijst</li><li>Lijst bevat een item in</li><li>Lijst bevat geen item in</li><li>Lijst bevat alle items in</li><li>Lijst bevat niet alle items in</li></ul>Zie &quot;Beschikbare operatoren&quot; in [Dynamische en statische inclusieregels gebruiken](/help/c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md#operators) voor meer informatie. |

Deze versie bevat de volgende oplossingen.

* Probleem verholpen waardoor een activiteit niet kon worden gesynchroniseerd nadat het publiek was gewijzigd in [!UICONTROL All Visitors]. (TGT-40259)
* Oplossing voor een probleem dat voorkwam dat aanbiedingen werden gedupliceerd wanneer ze op verschillende locaties in [!UICONTROL Automated Personalization]-activiteiten werden gebruikt, ook al is de optie [!UICONTROL Disallow Duplicates] ingeschakeld. (TGT-39567)
* Probleem verholpen waardoor de pagina [!UICONTROL Administration] > [!UICONTROL Scene7 configuration] niet correct kon worden geladen. (TGT-39918)
* Probleem verholpen waarbij eigenschappen werden toegewezen aan de onjuiste werkruimte. (TGT-39869)
* Probleem verholpen waarbij een oneindig laden werd veroorzaakt als de aanvraag mislukt nadat de omgeving was gewijzigd en een uitsluiting voor aanbevelingen werd gemaakt. (TGT-39948)

## Aanvullende opmerkingen bij de release en versiedetails

| Resource | Details |
|--- |--- |
| [details van de at.js-versie](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md) | Informatie over wijzigingen in elke versie van de JavaScript-bibliotheek [!DNL Adobe Target] at.js. |

## Documentatiewijzigingen, Opmerkingen bij de vorige release en Opmerkingen bij de release Experience Cloud

Naast de notities voor elke release bevatten de volgende bronnen aanvullende informatie:

| Resource | Details |
|--- |--- |
| Documentatiewijzigingen | Gedetailleerde informatie weergeven over updates van deze handleiding die niet zijn opgenomen in deze releaseopmerkingen.<br>Zie  [Documentatiewijzigingen](/help/r-release-notes/doc-change.md#reference_366123CF00994BACBBF9BBDF2C4D840C) voor meer informatie. |
| Opmerkingen bij de release van vorige releases | Informatie weergeven over nieuwe functies en verbeteringen in eerdere versies van Target Standard en Target Premium.<br>Voor meer informatie, zie de nota&#39;s van de  [Versie voor vorige versies](/help/r-release-notes/release-notes-for-previous-releases.md). |
| Opmerkingen bij de release van Adobe Experience Cloud | Bekijk de nieuwste releaseopmerkingen voor de Adobe Experience Cloud-oplossingen.<br>Zie Opmerkingen bij de release  [Experience Cloud voor meer informatie](https://experienceleague.adobe.com/docs/release-notes/experience-cloud/current.html). |

## Prerelease-informatie {#section_5D588F0415A2435B851A4D0113ACA3A0}

De volgende middelen laten u zien wat in de volgende versie van het Doel komt.

| Resource | Details |
|--- |--- |
| Adobe Priority-productupdate | Als u geavanceerde meldingen wilt ontvangen over toekomstige productverbeteringen voor Target en andere Adobe Experience Cloud-oplossingen, meldt u zich aan voor de Adobe Priority Product Update:<br>[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html) |
| Opmerkingen bij de volgende release | Voor informatie over de versies van het Doel van de huidige maand, met inbegrip van prereleaseinformatie, zie [de Nota&#39;s van de Versie van het Doel - Prerelease](/help/r-release-notes/target-release-notes.md) pagina. |
