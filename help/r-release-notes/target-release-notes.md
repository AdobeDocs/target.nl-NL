---
keywords: releaseopmerkingen;releases;updates;toekomstige release;verbeteringen;nieuwe functies;oplossingen;updates;pre-release
description: Leer meer over de nieuwe functies, verbeteringen en oplossingen in de komende release van Adobe Target, waaronder SDK's, API's en JavaScript-bibliotheken.
title: Welke nieuwe eigenschappen worden inbegrepen in de aanstaande Versie?
feature: Release Notes
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
translation-type: tm+mt
source-git-commit: dba3044c94502ea9e25b21a3034dc581de10f431
workflow-type: tm+mt
source-wordcount: '456'
ht-degree: 0%

---

# Opmerkingen bij de release Doel (preRelease)

Dit artikel bevat pre-releasegegevens. Releasedatums, -functies en andere informatie kunnen zonder voorafgaande kennisgeving worden gewijzigd.

**Laatst bijgewerkt: 16 april 2021**

Zie [Opmerkingen bij de doelversie](release-notes.md) voor informatie over de huidige versie. De informatie op deze pagina&#39;s kan gelijk zijn, afhankelijk van de timing van releases. De uitgiftenummers tussen haakjes zijn bedoeld voor intern gebruik [!DNL Adobe].

>[!IMPORTANT]
>
>**mbox.js end-of-life**: Vanaf 31 maart 2021 wordt de bibliotheek mbox.js  [!DNL Adobe Target] niet meer ondersteund. Na 31 maart 2021 mislukken alle aanroepen van mbox.js op elegante wijze en worden deze van invloed op uw pagina&#39;s die [!DNL Target] activiteiten hebben die worden uitgevoerd door standaardinhoud te bedienen.
>
>Migreer naar de meest recente versie van de nieuwe [!DNL Adobe Experience Platform Web SDK] of de JavaScript-bibliotheek at.js om mogelijke problemen met uw sites te voorkomen. Voor meer informatie, zie [Overzicht: Implementeer Doel voor client-side web](/help/c-implementing-target/c-implementing-target-for-client-side-web/implement-target-for-client-side-web.md).

## Target Standard/Premium 21.4.1 (19 april 2021)

Deze versie bevat de volgende nieuwe functies en verbeteringen. De uitgiftenummers tussen haakjes zijn bedoeld voor intern gebruik [!DNL Adobe].

| Functie | Details |
| --- | --- |
| Ondersteuning voor apparaatbeslissingen voor at.js | Met apparaatbeslissingen kunnen marketers en ontwikkelaars experimenten en personalisatie uitvoeren in de browser van een gebruiker bij bijna-nullatentie.<br>Voor meer informatie, zie  [Op-apparatenbesluit voor at.js.](/help/c-implementing-target/c-implementing-target-for-client-side-web/on-device-decisioning/on-device-decisioning.md)<br>(Aankondigde datum) |
| ![Op ](/help/assets/premium.png) PremiumList gebaseerde operatoren voor filterregels voor entiteiten | [!DNL Target Recommendations] steunt nieuwe op lijst-gebaseerde exploitanten voor entiteit het filtreren regels. (TGT-39234)<br>Nieuw toegevoegde operatoren zijn onder andere:<br><ul><li>Is opgenomen in lijst</li><li>Is niet opgenomen in lijst</li><li>Lijst bevat een item in</li><li>Lijst bevat geen item in</li><li>Lijst bevat alle items in</li><li>Lijst bevat niet alle items in</li></ul>Zie &quot;Beschikbare operatoren&quot; in [Dynamische en statische inclusieregels gebruiken](/help/c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md#operators) voor meer informatie. |

Deze versie bevat de volgende oplossingen.

* Probleem verholpen waardoor een activiteit niet kon worden gesynchroniseerd nadat het publiek was gewijzigd in [!UICONTROL All Visitors]. (TGT-40259)
* Oplossing voor een probleem dat voorkwam dat aanbiedingen werden gedupliceerd wanneer ze op verschillende locaties in [!UICONTROL Automated Personalization]-activiteiten werden gebruikt, ook al is de optie [!UICONTROL Disallow Duplicates] ingeschakeld. (TGT-39567)
* Probleem verholpen waardoor de pagina [!UICONTROL Administration] > [!UICONTROL Scene7 configuration] niet correct kon worden geladen. (TGT-39918)
* Probleem verholpen waarbij eigenschappen werden toegewezen aan de onjuiste werkruimte. (TGT-39869)
* Probleem verholpen waarbij een oneindig laden werd veroorzaakt als de aanvraag mislukt nadat de omgeving was gewijzigd en een uitsluiting voor aanbevelingen werd gemaakt. (TGT-39948)

## at.js versie 2.5.0 (Datum van bekendmaking)

Deze versie van at.js bevat de volgende verbeteringen en wijzigingen:

* [Ondersteuning voor ](/help/c-implementing-target/c-implementing-target-for-client-side-web/on-device-decisioning/on-device-decisioning.md) beslissingen op het apparaat voor at.js.
* [Ondersteuning voor ](/help/c-activities/c-activity-qa/activity-qa.md) koppelingen voorvertonen voor Automated Personalization-activiteiten

Deze release verwijdert ook ondersteuning voor Microsoft Internet Explorer 10 en hoger.

## Voorlopige-releasegegevens {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Als u geavanceerde meldingen wilt ontvangen over toekomstige productverbeteringen voor Target en andere Adobe Experience Cloud-oplossingen, meldt u zich aan voor de Adobe Priority Product Update:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
