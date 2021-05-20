---
keywords: wijzigingslogboek van doeldocumentatie;documentatie-updates;nieuwe onderwerpen;bewerkingen;updates;update
description: Houd up-to-date met belangrijke toevoegingen en wijzigingen in de Adobe [!DNL Target] productdocumentatie.
title: Waar kan ik documentatieupdates voor Doel bekijken?
feature: Opmerkingen bij de release
exl-id: 36d19598-eb46-4be6-a652-658b653287cb
source-git-commit: 943513649b5f3513d3b118172d4207d983c53eef
workflow-type: tm+mt
source-wordcount: '1203'
ht-degree: 0%

---

# Documentatiewijzigingen

Deze pagina bevat een overzicht van belangrijke wijzigingen die zijn aangebracht in de productdocumentatie van [!DNL Adobe Target].

## Adobe [!DNL Target] Standaard/Premium 21.4.1 (19 april 2021)

| Datum | Onderwerp | Wijzigingen |
| --- | --- | --- |
| 20 mei | [Bekende problemen en opgeloste problemen](/help/r-release-notes/known-issues-resolved-issues.md) | Het volgende bekende probleem is toegevoegd: Bij archivering van [!UICONTROL Auto Target] kunnen synchronisatieproblemen optreden. |
| 17 mei | [Opmerkingen bij de doelversie (huidig)](/help/r-release-notes/release-notes.md) | Informatie toegevoegd over de release at.js 2.5.0. |
|  | [Activiteit QA](/help/c-activities/c-activity-qa/activity-qa.md) | Bijgewerkt onderwerp om erop te wijzen dat de voorproefverbindingen voor [!UICONTROL Automated Personalization] (AP) activiteiten met at.js 2.5.0 (en later) beschikbaar zijn. |
|  | [Ondersteunde browsers](/help/c-implementing-target/c-considerations-before-you-implement-target/supported-browsers.md) | Geeft aan dat de release van at.js 2.5.0 ondersteuning voor Microsoft Internet Explorer 10, Internet Explorer 11 en alle oudere versies verwijdert. Microsoft Edge wordt nog steeds ondersteund in at.js 2.5.0 en hoger. |
|  | [Problemen met de  [!UICONTROL Enhanced Experience Composer]](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/troubleshooting-issues-related-to-the-enhanced-experience-composer-eec.md) | Bijgewerkt de lijst van IP adressen aan lijst van gewenste personen. |
| 12 mei | [[!DNL Target] releaseopmerkingen (pre-release)](/help/r-release-notes/target-release-notes.md) | Voorlopige opmerkingen toegevoegd voor het volgende:<ul><li>Adobe Experience Platform Web SDK (17 mei 2021)</li><li>Target Standard Premium 21.5.2</li></ul> |
| 10 mei | [[!DNL Recommendations] Veelgestelde vragen](/help/c-recommendations/c-recommendations-faq/recommendations-faq.md) | De volgende veelgestelde vragen zijn toegevoegd: &quot;Kan ik een algoritme gebruiken die in [!DNL Adobe Recommendations Classic] in [!DNL Recommendations Premium] wordt gecreeerd?&quot; |
|  | [Implementeren [!DNL Target] using [!DNL Dynamic Tag Manager]  (DTM)](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/implementing-target-using-dynamic-tag-management.md) | Geeft aan dat [!DNL Adobe Dynamic Tag Manager] niet meer wordt ondersteund. [!DNL Adobe] raadt in plaats daarvan implementatie met [[!DNL Adobe Experience Platform Launch]](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/cmp-implementing-target-using-adobe-launch.md) aan. |
| 6 mei | [Veelgestelde vragen over Recommendations](/help/c-recommendations/c-recommendations-faq/recommendations-faq.md) | De volgende veelgestelde vragen zijn toegevoegd:<ul><li>Hoe lang duurt het voor een wijziging in de configuratie van mijn [!UICONTROL Recommendations] activiteit, aanbieding, bevorderingen, of criteria montages op mijn plaats worden weerspiegeld?</li><li>Hoe lang duurt het voordat het gedrag van een gebruiker (bijvoorbeeld door op product A te klikken en product B te kopen) wordt weerspiegeld in de aanbevelingen *die* gebruiker ontvangt?</li><li>Hoe lang duurt het voordat het gedrag van een gebruiker (bijvoorbeeld door op product A te klikken en product B te kopen) wordt weerspiegeld in de aanbevelingen *andere* gebruikers ontvangen?</li></ul> |
|  | [Apparaatbeslissingen](/help/c-implementing-target/c-api-and-sdk-overview/on-device-decisioning.md) | Koppeling toegevoegd naar het volgende blogbericht op het Tech Blog van Adobe:<ul><li>Deel 1: Adobe Target NodeJS SDK uitvoeren voor experimenteren en personaliseren op Edge-Platforms (Akamai Edge Workers)</li></ul> |
| 5 mei | [Aankondigingen en gebeurtenissen van het doel](/help/r-release-notes/target-announcements.md) | Toegevoegde informatie over de door de Adobe Target Community opgestelde afkapping van vragen en antwoorden die woensdag 12 mei 2021 om 8.00 uur wordt gehouden. (PDT, GMT-7). |
| 27 april | [Cookie-instellingen](/help/c-implementing-target/c-implementing-target-for-client-side-web/atjs-cookies.md) | Bijgewerkt onderwerp om erop te wijzen dat de koekjesduur (`deviceIdLifetime` het plaatsen) in at.js versie 2.3.1 of later met voeten kan treden. |
|  | [Adobe Target-gids](/help/target-home.md) | Informatie toegevoegd over de top van Adobe. |
| 26 april | [Beslissing van problemen op het apparaat voor at.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/on-device-decisioning/troubleshooting-on-device-decisioning.md) | Nieuw onderwerp. |
| 19 april | [Apparaatbeslissingen](/help/c-implementing-target/c-implementing-target-for-client-side-web/on-device-decisioning/on-device-decisioning.md) | De volgende nieuwe artikelen zijn toegevoegd:<ul><li>[Apparaatbeslissingen](/help/c-implementing-target/c-implementing-target-for-client-side-web/on-device-decisioning/on-device-decisioning.md)</li><li>[Ondersteunde functies voor apparaatbesluitvorming](/help/c-implementing-target/c-implementing-target-for-client-side-web/on-device-decisioning/supported-features.md)</li><li>[Artefact van de regel voor apparaatbeslissingen](/help/c-implementing-target/c-implementing-target-for-client-side-web/on-device-decisioning/rule-artifact.md)</li></ul> |
|  | [targetGlobalSettings()](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetgobalsettings.md#on-device-decisioning) | Extra informatie over `decisioningMethod`. |
|  | [adobe.target.getOffers() - at.js 2.x](/help/c-implementing-target/c-implementing-target-for-client-side-web/adobe-target-getoffers-atjs-2.md) | Het volgende toegevoegd:<ul><li>Informatie over de `decisioningMethod` sleutel.</li><li>Een voorbeeld voor &quot;getCallOffers() om een apparaatbeslissing te maken.&quot;</li></ul> |
|  | [at.js, aangepaste gebeurtenissen](/help/c-implementing-target/c-implementing-target-for-client-side-web/atjs-custom-events.md) | De volgende informatie is toegevoegd:<ul><li>Artefact voor apparaatbeslissingen is geslaagd</li><li>Artefact voor beslissingen op het apparaat is mislukt</li></ul> |
|  | [Activiteiten](/help/c-activities/activities.md) | Toegevoegde informatie over apparaatbeslissingen. |
|  | [details van de at.js-versie](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md) | Extra informatie over at.js 2.5.0. |
|  | [Doel implementeren zonder tagbeheer](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/implementing-target-without-a-tag-manager.md) | Toegevoegde informatie over apparaatbeslissingen. |
|  | [Activiteit QA](/help/c-activities/c-activity-qa/activity-qa.md) | Ondersteuning voor voorbeeldkoppelingen voor [!UICONTROL Automated Personalization]-activiteiten is toegevoegd met [at.js 2.5.0](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md). |
|  | [Regels voor dynamische en statische integratie gebruiken](/help/c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md#operators) | Informatie toegevoegd over de volgende nieuwe operatoren:<ul><li>Is opgenomen in lijst</li><li> Is niet opgenomen in lijst</li><li>Lijst bevat een item in</li><li>Lijst bevat geen item in</li><li>Lijst bevat alle items in</li><li>Lijst bevat niet alle items in</li></ul> |
|  | [Adobe Target cookies](https://experienceleague.adobe.com/docs/core-services/interface/ec-cookies/cookies-target.html)<br> (*Experience Cloud Services and* Administration guide) | Extra informatie over sessie-id toegevoegd. |
|  | [Opmerkingen bij](/help/r-release-notes/release-notes.md) de release: 21.4.1. | Deze release bevat verbeteringen en correcties. U kunt over hen lezen en met de documentatie van de Nota&#39;s van de Versie verbinden. Deze release bevat ook een groot aantal documentatie-updates voor de hele Help. |

## Adobe [!DNL Target] Standaard/Premium 21.2.1 (9 maart 2021)

| Datum | Onderwerp | Wijzigingen |
| --- | --- | --- |
| 9 april | [Opmerkingen bij de release Doel (preRelease)](/help/r-release-notes/target-release-notes.md) | Voorlopige informatie voor de release van at.js versie 2.5.0 is toegevoegd (19 april 2021) |
| 9 april | [Opmerkingen bij de release Doel (preRelease)](/help/r-release-notes/target-release-notes.md) | Voorlopige informatie voor de doelstandaard/Premium versie 21.4.1 is toegevoegd (19 april 2021) |
|  | [Recommendations integreren met e-mail](/help/c-recommendations/c-recommendations-faq/integrating-recs-email.md) | Toegevoegde notitie met een beschrijving van de capaciteitsrichtlijnen voor opties 1 en 2. |
| 29 maart | [Veelgestelde vragen over Recommendations](/help/c-recommendations/c-recommendations-faq/recommendations-faq.md#persist-across-devices) | Nieuwe veelgestelde vragen toegevoegd:<ul><li>Blijven aanbevelingen op basis van onlangs weergegeven items op meerdere apparaten voor één bezoeker?</li></ul> |
| 23 maart | [Opmerkingen bij de release](/help/r-release-notes/release-notes.md) | Opmerkingen bij de release toegevoegd voor versie 2.4.1 van at.js. |
|  | [details van de at.js-versie](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md) | Opmerkingen bij de release toegevoegd voor versie 2.4.1 van at.js. |
|  | [Veelgestelde vragen over Recommendations](/help/c-recommendations/c-recommendations-faq/recommendations-faq.md) | Bijgewerkt van de volgende veelgestelde vragen:<ul><li>Hoe lang duurt het voordat updates van items in mijn catalogus op mijn site worden weergegeven?</li></ul> |
| 22 maart | [IP-adressen die worden gebruikt door Recommendations-voederverwerkingsservers](/help/c-recommendations/c-recommendations-faq/ip-addresses-marketing-cloud.md) | Bijgewerkte lijst van IP adressen. |
|  | [Limieten](/help/r-troubleshooting-target/target-limits.md) | De sectie &quot;Aantal entiteiten&quot; onder &quot;Entiteiten&quot; is bijgewerkt. |
|  | [Geo](/help/c-target/c-audiences/c-target-rules/geo.md) | Extra informatie over at.js 2.** xunder &quot;Hoe kan ik mijn activiteiten testen alsof ik een gebruiker ben die van een verschillende plaats komt?&quot; |
|  | [Opmerkingen bij](/help/r-release-notes/release-notes.md) de release: 21.2.1. | Toegevoegd: <ul><li>IP adresveranderingen voor de server van Recommendations feed-processing (16 maart 2021)</li></ul> |
| 19 maart | [Rapporten weergeven - Veelgestelde vragen voor A4T](/help/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-viewing-reports.md#deactivated) | Volgende veelgestelde vragen toegevoegd:<ul><li>Waarom zie ik nog meer indrukken nadat mijn activiteit is gedeactiveerd?</li></ul> |
| 12 maart | [A4T-ondersteuning voor activiteiten voor automatisch toewijzen en automatisch richten](/help/c-integrating-target-with-mac/a4t/a4t-at-aa.md#tutorial) | De volgende nieuwe zelfstudie is toegevoegd:<ul><li>A4T-rapporten instellen in Analysis Workspace voor Auto-Target-activiteiten</li></ul> |
| 9 maart | [Limieten](/help/r-troubleshooting-target/target-limits.md#offer-size) | <ul><li>De toegestane limiet voor de aanbiedingsgrootte is bijgewerkt.</li><li>Correctie van de tekenlimiet voor de parameter categoryId.</li></ul> |
|  | [Lijst van gewenste personen randknooppunten doel](/help/c-implementing-target/c-considerations-before-you-implement-target/allowlist-edges.md) | Bijgewerkte [!DNL Target] rand IP adressen. |
|  | [Entiteitskenmerken](/help/c-recommendations/c-products/entity-attributes.md) | Toegevoegde tekst die aangeeft dat entity.value een decimale notatie moet hebben (bijvoorbeeld 15.99 in plaats van 15.99). |
|  | [Opmerkingen bij](/help/r-release-notes/release-notes.md) de release: 21.2.1. | Deze release bevat verbeteringen en correcties. U kunt over hen lezen en met de documentatie van de Nota&#39;s van de Versie verbinden. Deze release bevat ook een groot aantal documentatie-updates voor de hele Help. |

## Adobe [!DNL Target] Standaard/Premium 21.1.1 (19 januari 2021)

| Datum | Onderwerp | Wijzigingen |
| --- | --- | --- |
| 22 februari | [Rapporten weergeven - Veelgestelde vragen voor A4T](/help/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-viewing-reports.md) | Bijgewerkt van de volgende veelgestelde vragen:<ul><li>Waar kunnen segmenten worden toegepast in Analysis Workspace?</li></ul> |
| 16 februari | [Opmerkingen bij de release Doel (preRelease)](/help/r-release-notes/target-release-notes.md) | De bijgewerkte tekst voor de limietgrootte van de aanbieding in de prereleaseopmerkingen. |
| 11 februari | [Hoe Target werkt](/help/c-intro/how-target-works.md) | Bijgewerkte sectie &quot;Bots&quot;. |
| 10 februari | [Aankondigingen en gebeurtenissen van het doel](/help/r-release-notes/target-announcements.md) | Informatie toegevoegd over het pagina-einde van de Adobe Target Community Coffee Coffee op woensdag 24 februari 2021. |
| 8 februari | [Voorvertoning voor mobiele doelversie](/help/c-target-mobile-app/target-mobile-preview.md) | Het codefragment dat u moet toevoegen aan het bestand AndroidManifest.xml voor versie 4 van de SDK van Adobe Mobile. |
|  | [Bekende problemen en opgeloste problemen](/help/r-release-notes/known-issues-resolved-issues.md) | Het volgende bekende probleem wordt verduidelijkt:<ul><li>Verzamelingen, uitsluitingen, criteria en ontwerpen die via de API zijn gemaakt, zijn niet zichtbaar in de doelgebruikersinterface en kunnen alleen via de API worden bewerkt. Op dezelfde manier, als u om het even welk van deze punten in het Doel UI creeert en later hen via API uitgeeft, zullen die veranderingen niet in het Doel UI worden weerspiegeld. Items die via de API worden bewerkt, moeten ook in de toekomst via de API worden bewerkt om te voorkomen dat wijzigingen verloren gaan.</li></ul> |
| 1 februari | [Samenvattingsrapporten van Automated Personalization](/help/c-reports/reports-ap.md) | Nieuwe sectie toegevoegd: &quot;Veelgestelde vragen.&quot; |
| 27 januari | [Omleidingsvoorstellen maken](/help/c-experiences/c-manage-content/offer-redirect.md) | Bijgewerkt onderwerp. |
|  | [Externe aanbiedingen maken](/help/c-experiences/c-manage-content/about-remote-offers.md) | Bijgewerkt onderwerp. |
| 26 januari | [Omrekeningskoers](/help/c-reports/conversion-rate.md) | Verduidelijkt hoe het Doel de &quot;som vierkanten&quot;in t-tests van de Student gebruikt. |
| 22 januari | [Omrekeningskoers](/help/c-reports/conversion-rate.md#t-test) | Toegevoegd: &quot;Waarom adviseert het Doel het gebruiken t-tests van de Student?&quot; |
| 21 januari | [Los de Analytics en integratie van het Doel (A4T) problemen op](/help/c-integrating-target-with-mac/a4t/c-a4t-troubleshooting/a4t-troubleshooting.md) | Nieuwe sectie toegevoegd: &quot;A4T Activiteitenrapporten bevatten een rij met een groot aantal &quot;ongespecificeerde&quot; gebeurtenissen.&quot; |
|  | [Rapporten weergeven - Veelgestelde vragen voor A4T](/help/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-viewing-reports.md) | Bijgewerkte volgende sectie: &quot;Waarom zie ik &quot;niet gespecificeerd&quot;in de rapporten van Analytics? Wat betekent het?&quot; |
| 20 januari | [Adobe Experience Platform Web SDK](/help/c-implementing-target/c-implementing-target-for-client-side-web/aep-web-sdk.md) | Nieuw onderwerp. |
| 19 januari | [Opmerkingen bij de doelversie (huidig)](/help/r-release-notes/release-notes.md) | Toegevoegde informatie over de doelversie 21.1.1 (19 januari 2021). |
|  | [Limieten](/help/r-troubleshooting-target/target-limits.md) | Bijgewerkte tekst voor de parameter `productPurchasedID`. |
|  | [Bekende problemen en opgeloste problemen](/help/r-release-notes/known-issues-resolved-issues.md) | Een bekend probleem toegevoegd bij het kopiëren van een [!UICONTROL Recommendation] activiteit met een actieve bevordering. Elke wijziging in de duplicaatactiviteit heeft ook invloed op de oorspronkelijke activiteit en omgekeerd. Een tijdelijke oplossing is inbegrepen. |
|  | [Opmerkingen bij](/help/r-release-notes/release-notes.md) de release: 21.1.1. | Deze release bevat verbeteringen en correcties. U kunt over hen lezen en met de documentatie van de Nota&#39;s van de Versie verbinden. Deze release bevat ook een groot aantal documentatie-updates voor de hele Help. |
