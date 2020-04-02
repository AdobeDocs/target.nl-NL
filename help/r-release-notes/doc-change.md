---
keywords: target documentation change log;documentation updates;new topics;edits;updates
description: Deze pagina bevat een overzicht van belangrijke wijzigingen die in de Adobe Target-documentatie zijn aangebracht en die in releases zijn besteld.
title: Wijzigingen in de documentatie bij het Adobe Target-product.
topic: Standard
uuid: 6fba75e2-0a93-488d-9010-fffa423600c0
translation-type: tm+mt
source-git-commit: cb5dd23e6cc8b15fda81cdb4fb615ac3efdad83f

---


# Documentatiewijzigingen{#documentation-changes}

Deze pagina bevat belangrijke wijzigingen die in de [!DNL Adobe Target] productdocumentatie zijn aangebracht.

## Adobe Target Standard/Premium 20.2.1 (19 februari 2020)

| Datum | Onderwerp | Wijzigingen |
| --- | --- | --- |
| 2 april | [Profiel en verklarende woordenlijst voor variabelen](/help/c-target/c-visitor-profile/variables-profiles-parameters-methods.md) | Toegevoegde informatie over het gebruik `user.header('x-forwarded-for')` met nieuwere randen van AWS om IP van gebruikers adressen terug te winnen. |
|  | [Upgrade uitvoeren vanaf 0,js 1.*x* tot at.js 2.*x *](/help/c-implementing-target/c-implementing-target-for-client-side-web/upgrading-from-atjs-1x-to-atjs-20.md) | Toegevoegd:<ul><li>Na installatie van de ECID-bibliotheek v4.3.0+ en at.js 2.*x*, zult u activiteiten kunnen tot stand brengen die unieke domeinen evenals spoorgebruikers omspannen. Het is belangrijk om op te merken dat deze functionaliteit slechts werkt nadat de zitting verloopt.</li></ul> |
| 30 maart | [Bekende problemen en opgeloste problemen](/help/r-release-notes/known-issues-resolved-issues.md#atjs) | Er zijn een bekende problemen toegevoegd die van invloed zijn op versies at.js vóór at.js 2.2.0. Dit probleem heeft ertoe geleid dat klikspatiëring geen conversies rapporteert in Analytics for Target (A4T) wanneer Adobe Analytics-code niet aanwezig was op pagina-elementen. |
|  | [details van de at.js-versie](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md) | De volgende informatie is toegevoegd aan de gegevens van at.js versie 2.2.0:<ul><li>Probleem verholpen waarbij klikspatiëring ertoe leidde dat conversies niet werden gerapporteerd in Analytics for Target (A4T) wanneer Adobe Analytics-code niet aanwezig was op pagina-elementen.</li></ul> |
| 25 maart | [details van de at.js-versie](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md) | Informatie toegevoegd over de volgende nieuwe versies van at.js:<ul><li>at.js versie 2.3.0</li><li>at.js versie 1.8.1</li></ul> |
|  | [targetGlobalSettings()](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetgobalsettings.md) | De volgende nieuwe rijen zijn toegevoegd in de sectie &quot;Instellingen&quot;:<ul><li>cspScriptNonce</li><li>cspStyleNonce</li></ul>De volgende nieuwe sectie toegevoegd:<ul><li>Beveiligingsbeleid voor inhoud</li></ul> |
| 24 maart | [Apple Intelligent Tracking Prevention (ITP) 2.x](/help/c-implementing-target/c-considerations-before-you-implement-target/c-privacy/apple-itp-2x.md#impact) | Toegevoegde informatie over de gevolgen voor:<ul><li>Profielscripts gebaseerd op 3rdPartyID</li><li>URL&#39;s met kwaliteitscontrole/voorvertoning op iOS-apparaten</li></ul> |
| 20 maart | [Opmerkingen bij de release (huidig)](/help/r-release-notes/release-notes.md) | Geeft aan dat de release Target Standard/Premium 20.2.1 23 maart 2020 zal zijn. |
| 13 maart | [Limieten](/help/r-troubleshooting-target/target-limits.md) | Het aantal &quot;Soorten publiek, herbruikbaar per account&quot; is bijgewerkt. |
| 12 maart | [Opmerkingen bij de release (huidige)](/help/r-release-notes/release-notes.md#summit) | Toegevoegde registratiegegevens voor gratis toegang tot de online, digitale topconferentie. |
| 9 maart | [Privacy](/help/c-implementing-target/c-considerations-before-you-implement-target/c-privacy/privacy.md) | Meer informatie toegevoegd in de sectie &quot;Vervanging van laatste octet van IP adressen&quot;. |
|  | [Werken met kenmerken van meerdere waarden](/help/c-recommendations/c-algorithms/work-with-multi-value-attributes.md) | Bijgewerkt codevoorbeeld in *Geef een parameter met meerdere waarden door in JavaScript*. |
|  | [Aangepaste entiteitskenmerken](/help/c-recommendations/c-products/custom-entity-attributes.md) | Codevoorbeeld toegevoegd in API&#39;s *gebruiken* onder *Meerwaardekenmerken* implementeren. |
| 4 maart | [Profielkenmerken](/help/c-target/c-visitor-profile/profile-parameters.md) | Gehele onderwerp is bijgewerkt, met uitgebreide revisies van de sectie &quot;Beste werkwijzen&quot;. |
| 21 februari | [Opmerkingen bij de release (huidig)](/help/r-release-notes/release-notes.md) | Informatie toegevoegd over de nieuwe Adobe Experience Cloud-navigatie. |
| 20 februari | [targetGlobalSettings()](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetgobalsettings.md) | De beschrijving voor de `enabled` instelling is bijgewerkt. Informatie toegevoegd voor de volgende instellingen: `pageLoadEnabled` en `viewsEnabled`. |
| 19 februari | [Opmerkingen bij de release](/help/r-release-notes/release-notes.md) | Toegevoegde informatie over de aanstaande afbraak van de bibliotheek mbox.js. |
|  | [Geo](/help/c-target/c-audiences/c-target-rules/geo.md) | Toegevoegde opmerking die `mboxOverride.browserIp` wordt ondersteund in at.js 1.*alleen x* . |
|  | [details van de at.js-versie](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md) | Verduidelijkte tekst die verklaart welke versies van bij.js het team van het Doel steunt. |
|  | [Opmerkingen bij](/help/r-release-notes/release-notes.md)de release: 20.2.1. | Deze release bevat verbeteringen en correcties. U kunt over hen lezen en met de documentatie van de Nota&#39;s van de Versie verbinden. Deze release bevat ook een groot aantal documentatie-updates voor de hele Help. |

## Adobe Target Standard/Premium 20.1.1 (4 februari 2020)

| Datum | Onderwerp | Wijzigingen |
| --- | --- | --- |
| 4 februari | [Opmerkingen bij](/help/r-release-notes/release-notes.md)de release: 20.1.1. | Deze release bevat verbeteringen en correcties. U kunt over hen lezen en met de documentatie van de Nota&#39;s van de Versie verbinden. Deze release bevat ook een groot aantal documentatie-updates voor de hele Help. |

## Adobe Target Standard/Premium 19.10.1 (22 oktober 2019)

| Datum | Onderwerp | Wijzigingen |
| --- | --- | --- |
| 29 januari 2020 | [Een ontwerp aanpassen met Snelheid](/help/c-recommendations/c-design-overview/customizing-a-template.md) | Bijgewerkte tekst- en codevoorbeelden. De nieuwe codesteekproeven tonen hoe te met aantallen in de malplaatjes van de Snelheid te werken. |
| 28 januari 2020 | [Opmerkingen bij de release Doel (preRelease)](/help/r-release-notes/target-release-notes.md) | Wijzigt de releasedatum van de Target Standard/Premium 20.1.1-release. De releasedatum is nu 4 februari 2020. |
| 27 januari 2020 | [Persoonlijkheidsrapporten](/help/c-reports/c-personalization-insights-reports/personalization-insights-reports.md) | Nieuwe sectie toegevoegd: &quot;Adobe-blogs.&quot; |
|  | [Limieten](/help/r-troubleshooting-target/target-limits.md) | De volgende gegevens zijn toegevoegd: &quot;Als u de API voor het leveren van batches gebruikt, is de limiet 50 dozen per aanvraag.&quot; |
|  | [Bronnen en contactgegevens](/help/cmp-resources-and-contact-information.md#section_354AC2658BA84A2A96E64C5B2C43B73B) | Bijgewerkte verbinding om een steunkaartje te openen. |
|  | [Samenvattingsrapport voor automatisch doel](/help/c-reports/auto-target-summary-report.md) | Tekst en afbeeldingen zijn bijgewerkt. |
| 23 januari 2020 | [Rapporten automatisch toewijzen interpreteren](/help/c-activities/automated-traffic-allocation/determine-winner.md) | Opmerking toegevoegd om de voorbeeldgroottecalculator voor Adobe Target te gebruiken om de winnaar te bepalen. |
|  | [Entiteitskenmerken](/help/c-recommendations/c-products/entity-attributes.md) | Opmerking toegevoegd waarin wordt uitgelegd dat als u at.js 2 gebruikt.*x*, `mboxCreate` wordt niet meer ondersteund. Product- of inhoudsgegevens doorgeven aan Aanbevelingen met behulp van at.js 2.*x*, gebruik `targetPageParams`. |
| 22 januari 2020 | [Automatisch toewijzen](/help/c-activities/automated-traffic-allocation/automated-traffic-allocation.md) | Bijgewerkt van de volgende veelgestelde vragen: &quot;Kan ik de calculator van de steekproefgrootte gebruiken wanneer het gebruiken van Auto-Toewijzing om te schatten hoe lang de activiteit zal duren om de winnaar te identificeren?&quot; |
| 15 januari 2020 | [Gemengde inhoud in uw browser inschakelen](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/mixed-content.md) | Er is een trainingsvideo en instructies toegevoegd waarin wordt uitgelegd hoe u uw site-instellingen kunt bijwerken om gemengde inhoud toe te staan in de nieuwste versie van Chrome. |
|  | [Feeds](/help/c-recommendations/c-products/feeds.md) | Opmerking toegevoegd over het uploaden en verwijderen van entiteiten en entiteitskenmerken. |
|  | [Veelgestelde vragen over aanbevelingen](/help/c-recommendations/c-recommendations-faq/recommendations-faq.md) | Volgende veelgestelde vragen toegevoegd: Wat betekent de reactie NO_CONTENT soms teruggekeerd in de inhoud van Aanbevelingen spoor? |
|  | [Een bevestigingsbox voor bestellingen maken - mbox.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/orderconfirm-create.md) | Toegevoegde notitie waarin wordt uitgelegd hoe u orderbevestiging kunt uitvoeren met behulp van at.js 2.*x*. |
| 9 januari 2020 | [De encryptieveranderingen van TLS (de Veiligheid van de Laag van het Vervoer)](/help/c-implementing-target/c-considerations-before-you-implement-target/tls-transport-layer-security-encryption.md) | Bijgewerkte tekst.<br>Na 1 maart 2020 biedt Adobe Target geen ondersteuning meer voor TLS 1.1-codering voor Visual Experience Composer (VEC), Enhanced Experience Composer (EEC), activity delivery, API&#39;s, enz. Upgrade vóór 1 maart 2020 naar TLS 1.2 om problemen te voorkomen. |
| 6 januari 2020 | [Bekende problemen en opgeloste problemen](/help/r-release-notes/known-issues-resolved-issues.md) | Bekend probleem met de status van de feed Custom Criteria toegevoegd. |
| 19 december 2019 | [Opmerkingen bij de release - Doel Java SDK](/help/c-implementing-target/c-api-and-sdk-overview/releases-target-java-sdk.md) | Informatie over versie 1.1.0 toegevoegd. |
| 11 december 2019 | [CNAME en Adobe Target](/help/c-implementing-target/c-considerations-before-you-implement-target/implement-cname-support-in-target.md) | Bijgewerkte sectie Veelgestelde vragen. |
|  | [Rapporten automatisch toewijzen interpreteren](/help/c-activities/automated-traffic-allocation/determine-winner.md) | Benoemd onderwerp en toegevoegd de volgende sectie: &quot;Werken met rapportage van optillen en vertrouwen bij activiteiten voor automatisch toewijzen.&quot; |
| 12 december 2019 | [Veelgestelde vragen over doelen en doelgroepen](/help/c-target/c-troubleshooting-targets-and-audiences/troubleshooting-targets-and-audiences.md) | Nieuwe veelgestelde vragen toegevoegd: &quot;Hoe evalueert Doel URLs in het richten?&quot; |
| 10 december 2019 | [Doelgrenzen](/help/r-troubleshooting-target/target-limits.md) | De sectie mbox-parameters is bijgewerkt. |
|  | [Criteria](/help/c-recommendations/c-algorithms/algorithms.md) | Opmerking toegevoegd over ondersteuning voor de functie Criteria Usage. |
| 5 december 2019 | [Sitepagina&#39;s](/help/c-target/c-audiences/c-target-rules/site-pages.md) | Bijgewerkt onderwerp. |
| 2 december 2019 | [Locatieservice gebruiken](/help/c-target-mobile-app/use-location-service.md) | Nieuw onderwerp. |
| 26 november 2019 | [Hoe at.js flikkering beheert](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/manage-flicker-with-atjs.md) | Bijgewerkte tekst in &quot;Flicker beheren bij asynchroon laden bij.js.&quot; |
|  | [Nieuwsbrief Target Insider](/help/r-release-notes/target-insider-newsletter.md) | Koppeling toegevoegd aan de nieuwsbrief van november 2019. |
|  | [Gebruikers](/help/administrating-target/c-user-management/c-user-management/user-management.md) | Bijgewerkte tekst en afbeeldingen onder &quot;Rollen en machtigingen opgeven&quot;. |
| 15 november 2019 | [Tien gemeenschappelijke A/B-testvalkuilen en hoe deze te vermijden](/help/c-activities/t-test-ab/common-ab-testing-pitfalls.md) | Toegevoegd &quot;Pitfall 7: De verkeerstoewijzing tijdens de testperiode wijzigen.&quot; |
| 11 november 2019 | [Opmerkingen bij de release - Doel Java SDK](/help/c-implementing-target/c-api-and-sdk-overview/releases-target-java-sdk.md) | Informatie over versie 1.0.1 toegevoegd. |
|  | [CNAME en Adobe Target](/help/c-implementing-target/c-considerations-before-you-implement-target/implement-cname-support-in-target.md) | Volledig onderwerp bijgewerkt. |
|  | [Geo](/help/c-target/c-audiences/c-target-rules/geo.md#section_DD308A53AF0F48FA8C81423580561FE7) | Toegevoegde informatie waarin wordt uitgelegd dat er geen geografische informatie [!DNL Target] wordt opgeslagen, zoals postcodes. |
| 8 november 2019 | [Nieuwsbrief Target Insider](/help/r-release-notes/target-insider-newsletter.md) | Koppelingen toegevoegd naar andere problemen uit het verleden. |
|  | [Regels inzake privacy en gegevensbescherming](/help/c-implementing-target/c-considerations-before-you-implement-target/c-privacy/cmp-privacy-and-general-data-protection-regulation.md) | Bijgewerkte sectie CCPA met nieuwe nota.<br>Nieuwe veelgestelde vragen die klanten ervan op de hoogte stelden dat Target klanten niet in staat heeft om gegevens rechtstreeks van Target aan derden te delen of te verkopen, zodat er geen sprake is van een opt-out voor Target. |
| 7 november 2019 | [Profielkenmerken](/help/c-target/c-visitor-profile/profile-parameters.md#examples) | Codevoorbeeld toegevoegd voor de adobeQA-parameter. |
| 5 november 2019 | [Sitepagina&#39;s](/help/c-target/c-audiences/c-target-rules/site-pages.md#ts) | Bijgewerkte tekst in de sectie van het &quot;Oplossen van problemen&quot;. |
| 4 november 2019 | [om.js Veelgestelde Vragen](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-target-atjs-faq/target-atjs-faq.md) | Bijgewerkte tekst onder de volgende veelgestelde vragen: &quot;Waarom zie ik waarschuwingsberichten, zoals &quot;acties met ontbrekende kiezers&quot;?&quot; |
| 31 oktober 2019 | [Werken met kenmerken van meerdere waarden](/help/c-recommendations/c-algorithms/work-with-multi-value-attributes.md) | Nieuw onderwerp. |
|  | [Opmerkingen bij de release - Doel Java SDK](/help/c-implementing-target/c-api-and-sdk-overview/releases-target-java-sdk.md) | Nieuw onderwerp. |
|  | [Bijwerken van at.js 1.x naar at.js 2.x](/help/c-implementing-target/c-implementing-target-for-client-side-web/upgrading-from-atjs-1x-to-atjs-20.md#audience-parameters) | Nieuwe sectie toegevoegd: &quot;Welke om.js 1.*x* -parameters voor het maken van soorten publiek worden niet ondersteund in at.js 2.*x*?&quot; |
|  | [Bekende problemen en opgeloste problemen](/help/r-release-notes/known-issues-resolved-issues.md) | Nieuw bekend probleem toegevoegd met extra spaties die aan sjabloonregels worden toegevoegd. |
|  | [Opmerkingen bij de doelversie (huidig)](/help/r-release-notes/release-notes.md) | Toegevoegde informatie over de doelversie van Premium 19.10.2 en de doelversie van Java SDK. |
| 30 oktober 2019 | [Opmerkingen bij de release Doel (preRelease)](/help/r-release-notes/target-release-notes.md) | Extra informatie over de aanstaande release van Target Premium 19.10.2 (31 oktober 2019). |
| 29 oktober 2019 | [Overeenkomende inhoud](/help/c-recommendations/c-algorithms/create-new-algorithm.md#concept_5402DAFA279C4E46A9A449526889A0CB) | Opmerking toegevoegd. |
|  | [Activiteiten van uw aanbevelingen voorvertonen en starten](/help/c-recommendations/t-create-recs-activity/previewing-and-launching-your-recommendations-activity.md) | Nieuw onderwerp. |
| 25 oktober 2019 | [Aangepaste parameters](/help/c-target/c-audiences/c-target-rules/custom-parameters.md#considerations) | Nieuw item toegevoegd onder &quot;Overwegingen&quot; om uit te leggen dat het aanwijzen van doelen niet op interne parameters mbox wordt geëvalueerd. |
|  | [Regels voor dynamische en statische integratie gebruiken](/help/c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md) | Het bijgewerkte onderwerp volledig en verwijderde verouderde voorbeelden. |
|  | [adobe.target.getOffers(options) - at.js 2.x](/help/c-implementing-target/c-implementing-target-for-client-side-web/adobe-target-getoffers-atjs-2.md) | Toegevoegde opmerking die is gekoppeld aan de documentatie van de API voor doellevering om u te helpen de beschikbare typen voor aanvragen/reacties (array, tekenreeks, enzovoort) te begrijpen. |
|  | [adobe.target.getOffers(options) - at.js 2.x](/help/c-implementing-target/c-implementing-target-for-client-side-web/adobe-target-getoffers-atjs-2.md) | Toegevoegde opmerking die is gekoppeld aan de documentatie van de API voor doellevering om u te helpen de beschikbare typen voor aanvragen/reacties (array, tekenreeks, enzovoort) te begrijpen. |
|  | [Sitepagina&#39;s](/help/c-target/c-audiences/c-target-rules/site-pages.md#ts) | Sectie &quot;Problemen oplossen&quot; toegevoegd. |
| 24 oktober 2019 | [Veelgestelde vragen over aanbevelingen](/help/c-recommendations/c-recommendations-faq/recommendations-faq.md#section_DB3F40673AED42228E407C05437D99E9) | Bijgewerkte tekst in de volgende veelgestelde vragen: &quot;Waarom kan Target soms geen aanbevelingen tonen?&quot; |
|  | [Bekende problemen en opgeloste problemen](/help/r-release-notes/known-issues-resolved-issues.md#atjs) | Er is een notitie toegevoegd aan een bekende uitgave die invloed heeft op eerdere versies van at.js (ouder dan versie 2.2.0). |
|  | [Succeswaarden](/help/c-activities/r-success-metrics/success-metrics.md) | Toegevoegde nota over het standaardgedrag voor succesmetriek voor activiteiten die A4T gebruiken. |
| 22 oktober 2019 | [Criteria/algoritmen](/help/c-recommendations/c-algorithms/algorithms.md#criteria-algorithms) | Toegevoegde rij voor op gebruiker gebaseerde Aanbevelingen. |
|  | [Criteria](/help/c-recommendations/c-algorithms/algorithms.md#custom-key) | Nieuwe sectie toegevoegd: &quot;Gebruikend een sleutel van douaneaanbevelingen.&quot; |
|  | [Veelgestelde vragen over doel en publiek](/help/c-target/c-troubleshooting-targets-and-audiences/troubleshooting-targets-and-audiences.md) | Nieuwe veelgestelde vragen toegevoegd: &quot;Wanneer het creëren van complexe koorden URL, [!DNL Target] evalueert volledige URL?&quot; |
|  | [Opmerkingen bij](/help/r-release-notes/release-notes.md)de release: 19.10.1. | Deze release bevat verbeteringen en correcties. U kunt over hen lezen en met de documentatie van de Nota&#39;s van de Versie verbinden. Deze release bevat ook een groot aantal documentatie-updates voor de hele Help. |

## Adobe Target/Standard/Premium 19.9.1 (30 september 2019)

| Datum | Onderwerp | Wijzigingen |
| --- | --- | --- |
| 17 oktober 2019 | [Activiteit QA](/help/c-activities/c-activity-qa/activity-qa.md) | Bijgewerkt onderwerp om te verklaren hoe Activiteit QA met derdekoekjes werkt. |
|  | [Opmerkingen bij de release Doel (preRelease)](/help/r-release-notes/target-release-notes.md) | Bijgewerkte versienota&#39;s om informatie over veranderingen in Verenigde Shell te omvatten. |
| 10 oktober 2019 | [targetGlobalSettings](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetgobalsettings.md#server-state) | Nieuwe sectie toegevoegd: &quot;serverState.&quot; |
|  | [Opmerkingen bij de doelversie (huidig)](/help/r-release-notes/release-notes.md) | Toegevoegde informatie over de versies at.js 2.2 en at.js 1.8. |
|  | [details van de at.js-versie](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md) | Toegevoegde informatie over de versies at.js 2.2 en at.js 1.8. |
|  | [Problemen met activiteiten oplossen](/help/c-activities/c-troubleshooting-activities/troubleshooting-activities.md) | Nieuwe sectie toegevoegd: &quot;Ik heb een activiteit gemaakt met behulp van de doelinterface en ik kan deze niet bijwerken via de API.&quot; |
| 9 oktober 2019 | [Serverzijde: Doel implementeren](/help/c-implementing-target/c-api-and-sdk-overview/api-and-sdk-overview.md) | Bijgewerkt onderwerp. |
|  | [Opmerkingen bij de release - Doelserver-side API&#39;s](/help/c-implementing-target/c-api-and-sdk-overview/releases-server-side.md) | Nieuw onderwerp. |
|  | [Opmerkingen bij de release - Doel Node.js SDK](/help/c-implementing-target/c-api-and-sdk-overview/releases-nodejs.md) | Nieuw onderwerp. |
|  | [Opmerkingen bij de doelversie (huidig)](/help/r-release-notes/release-notes.md) | Toegevoegde informatie over de V1/Delivery-API en Node.js SDK-releases. |
| 8 oktober 2019 | [Nieuwsbrief Target Insider](/help/r-release-notes/target-insider-newsletter.md) | Nieuw onderwerp met verbindingen aan de eerste partij nieuwsbrieven, met meer te komen. |
| 3 oktober 2019 | [Bekende problemen en opgeloste problemen](/help/r-release-notes/known-issues-resolved-issues.md) | Het volgende toegevoegd: <ul><li>Bekende kwestie en oplossing wanneer het creëren van een ervaring zonder wijzigingen gebruikend at.js 2.*x* -bibliotheek.</li><li>Verzamelingen, uitsluitingen, criteria en ontwerpen die via de API zijn gemaakt, zijn niet zichtbaar in de doelgebruikersinterface en kunnen alleen via de API worden bewerkt.</li><li>Activiteiten van aanbevelingen die via API zijn gemaakt, kunnen in de gebruikersinterface worden weergegeven, maar kunnen alleen via API worden bewerkt.</li></ul> |
|  | [Problemen met de levering van inhoud oplossen](/help/c-activities/c-troubleshooting-activities/content-trouble.md#mboxdebug) | Opmerking toegevoegd aan de sectie &quot;mboxDebug&quot;. |
| 2 oktober 2029 | [Opmerkingen bij de release Doel (preRelease)](/help/r-release-notes/target-release-notes.md) | Informatie toegevoegd over komende releases. |
| 1 oktober 2019 | [Profiel en verklarende woordenlijst voor variabelen](/help/c-target/c-visitor-profile/variables-profiles-parameters-methods.md) | Bijgewerkte tekst in de sectie &quot;Kenmerken van klant&quot;. |
|  | [adobe.target.getOffers(options) - at.js 2.x](/help/c-implementing-target/c-implementing-target-for-client-side-web/adobe-target-getoffers-atjs-2.md) | Bijgewerkte codesteekproef in de &quot;Vraag getOffers () voor alle meningen&quot;sectie. |
| 30 september 2019 | [Opmerkingen bij](/help/r-release-notes/release-notes.md)de release: 19.9.1. | Deze release bevat verbeteringen en correcties. U kunt over hen lezen en met de documentatie van de Nota&#39;s van de Versie verbinden. Deze release bevat ook een groot aantal documentatie-updates voor de hele Help. |

## Adobe Target Standard/Premium 19.7.1 (23 juli 2019) {#tgt-19-7-1}

| Datum | Onderwerp | Wijzigingen |
| --- | --- | --- |
| 27 september 2019 | [Hoe lang moet u een A/B-test uitvoeren?](/help/c-activities/t-test-ab/sample-size-determination.md) | Bijgewerkte tekst over de calculator van de Grootte van de Steekproef van het Doel. |
|  | [Automatisch toewijzen](/help/c-activities/automated-traffic-allocation/automated-traffic-allocation.md) | Bijgewerkte tekst over de calculator van de Grootte van de Steekproef van het Doel. |
| 24 september 2019 | [Opmerkingen bij de release Doel (preRelease)](/help/r-release-notes/target-release-notes.md) | Gewijzigde datum van de release Target/Standard 19.2.1 naar 30 september 2019. |
|  | [Aanbevelingen als voorstel](/help/c-recommendations/recommendations-as-an-offer.md) | Opleidingsvideo toegevoegd. |
| 10 september 2019 | [Opmerkingen bij de doelversie (huidig)](/help/r-release-notes/release-notes.md) | Toegevoegde informatie over de doelversie Standard/Premium 19.9.1. |
| 9 september 2019 | [AEM ervaart fragmenten](/help/c-experiences/c-manage-content/aem-experience-fragments.md#considerations) | Sectie &quot;Overwegingen&quot; toegevoegd. |
|  | [Google Chrome SameSite-cookiebeleid](/help/c-implementing-target/c-considerations-before-you-implement-target/c-privacy/google-chrome-samesite-cookie-policies.md) | Bijgewerkte tekst voor het hele onderwerp. |
|  | [Inhoudsbeveiligingsbeleid (CSP)](/help/c-implementing-target/c-considerations-before-you-implement-target/c-privacy/content-security-policy.md) | Nieuw onderwerp. |
| 6 september 2019 | [Opmerkingen bij de release Doel (preRelease)](/help/r-release-notes/target-release-notes.md) | Toegevoegde informatie over de release Target Standard/Premium 19.9.1 (10 september 2019). |
|  | [Veelgestelde vragen over het doel voor mobiele apps](/help/c-target-mobile-app/target-for-mobile-apps-faq.md) | Nieuw onderwerp. |
| 4 september 2019 | [CNAME en Adobe Target](/help/c-implementing-target/c-considerations-before-you-implement-target/implement-cname-support-in-target.md) | Bijgewerkt onderwerp. |
| 23 augustus 2019 | [Voorvertoning voor mobiele doelversie](/help/c-target-mobile-app/target-mobile-preview.md) | Bijgewerkt codefragment in `AndroidManifest.xml`. |
|  | [Aangepaste parameters](/help/c-target/c-audiences/c-target-rules/custom-parameters.md#considerations) | Nieuwe sectie toegevoegd: &quot;Overwegingen.&quot; |
|  | [Aangepaste criteria uploaden](/help/c-recommendations/c-algorithms/recommendations-csv.md) | Bijgewerkte volgende zin: Updates van aangepaste criteria zijn standaard &#39;cumulatief&#39;. Nieuwe sleutelwaardeparen die in het CSV-uploadbestand zijn opgegeven, overschrijven bestaande sleutelwaardeparen. Bestaande sleutel-waarde paren die geen sleutels hebben die in CSV uploaden worden gespecificeerd zullen nog voor levering beschikbaar zijn en zullen verlopen over 31 dagen vanaf de tijd zij als deel van het Csv- dossier het laatst worden geupload. |
| 20 augustus 2019 | [Opmerkingen bij de release Doel (preRelease)](/help/r-release-notes/target-release-notes.md) | De release Target/Premium 19.8.1 uitgesteld (20 augustus 2019). Inhoud uit deze release wordt toegevoegd aan de release van 19.9.1 (24 september 2019). |
|  | [Veelgestelde vragen over ontwerp](/help/c-recommendations/c-design-overview/template-faq.md) | De volgende veelgestelde vragen zijn toegevoegd: De prijs van mijn aanbevolen object geeft beide waarden niet rechts van het decimaalteken weer. Hoe kan ik ze weergeven?&quot; |
| 16 augustus 2019 | [Profielsynchronisatie in realtime voor mbox3rdPartyID](/help/c-target/c-visitor-profile/3rd-party-id.md) | Nieuwe sectie toegevoegd: &quot;Overwegingen.&quot; |
|  | [Een handeling Aanbevelingen maken](/help/c-recommendations/t-create-recs-activity/create-recs-activity.md) | Opleidingsvideo toegevoegd. |
|  | [Feeds](/help/c-recommendations/c-products/feeds.md) | Toegevoegde trainingsvideo&#39;s. |
|  | [Criteria maken](/help/c-recommendations/c-algorithms/create-new-algorithm.md) | Opleidingsvideo toegevoegd. |
|  | [Aangepaste criteria uploaden](/help/c-recommendations/c-algorithms/recommendations-csv.md) | Opleidingsvideo toegevoegd. |
|  | [Criteria-reeksen maken](/help/c-recommendations/c-algorithms/create-criteria-sequence.md) | Opleidingsvideo toegevoegd. |
|  | [Een ontwerp maken](/help/c-recommendations/c-design-overview/create-design.md) | Opleidingsvideo toegevoegd. |
|  | [Verzamelingen](/help/c-recommendations/c-products/collections.md) | Opleidingsvideo toegevoegd. |
|  | [Uitsluitingen](/help/c-recommendations/c-products/exclusions.md) | Opleidingsvideo toegevoegd. |
| 14 augustus 2019 | [CNAME en Adobe Target](/help/c-implementing-target/c-considerations-before-you-implement-target/implement-cname-support-in-target.md) | Bijgewerkte tekst en toegevoegde videokoppeling voor training. |
|  | [adobe.target.getOffers(options) - at.js 2.x](/help/c-implementing-target/c-implementing-target-for-client-side-web/adobe-target-getoffers-atjs-2.md) | Duidelijke informatie over de `consumerID` sleutel. |
|  | [Opties voor composer visuele ervaring](/help/c-experiences/c-visual-experience-composer/viztarget-options.md#move) | Bijgewerkte informatie in de sectie &quot;Layout > Verplaatsen&quot;. |
| 12 augustus 2019 | [Een activiteit bewerken of opslaan als concept](/help/c-activities/edit-activity.md#classic) | Nieuwe sectie toegevoegd: &quot;Werken met verouderde activiteiten die zijn gemaakt in Recommendations Classic.&quot; |
| 9 augustus 2019 | [Hoe werkt at.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/how-atjs-works.md#render) | Nieuwe sectie toegevoegd: &quot;Hoe at.js aanbiedingen met HTML-inhoud rendert.&quot; |
|  | [Opties voor composer visuele ervaring](/help/c-experiences/c-visual-experience-composer/viztarget-options.md#considerations) | Nieuwe sectie toegevoegd: &quot;Overwegingen.&quot; |
| 7 augustus 2019 | [Prefetaanbiedingsinhoud](/help/c-target-mobile-app/prefetch-offer-content.md) | Toegevoegde nota dat de prefetch functionaliteit in SDKs niet voor AutoDoel, Auto wordt gesteund, en de Geautomatiseerde types van de Personalisatieactiviteit. |
|  | [Los de Analytics en integratie van het Doel (A4T) problemen op](/help/c-integrating-target-with-mac/a4t/c-a4t-troubleshooting/a4t-troubleshooting.md#unspecified) | Bijgewerkte notitie die aangeeft hoe lang het indelingsproces duurt. |
|  | [Rapporten weergeven - Veelgestelde vragen voor A4T](/help/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-viewing-reports.md#unspecified) | Bijgewerkte notitie die aangeeft hoe lang het indelingsproces duurt. |
|  | [Regels inzake privacy en gegevensbescherming](/help/c-implementing-target/c-considerations-before-you-implement-target/c-privacy/cmp-privacy-and-general-data-protection-regulation.md) | Bijgewerkt onderwerp om informatie over de Wet van de Privacy van de consument van Californië (CCPA) te omvatten. |
|  | [Rapporten weergeven - Veelgestelde vragen voor A4T](/help/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-viewing-reports.md#metrics) | Bijgewerkte overweging over het gebruik van [!UICONTROL Activiteitenindrukkingen] en [!UICONTROL Activiteitenconversies] in [!DNL Analysis Workspace]. |
| 1 augustus 2019 | [Opmerkingen bij de doelversie (huidig)](/help/r-release-notes/release-notes.md) | Belangrijke aankondiging toegevoegd met betrekking tot API-ondersteuning voor Enterprise-machtigingen. |
|  | [Adobe I/O-integratie toegang verlenen tot werkruimten en rollen toewijzen](/help/administrating-target/c-user-management/property-channel/configure-adobe-io-integration.md) | Nieuw onderwerp. |
| 31 juli 2019 | [Inleiding tot aanbevelingen](/help/c-recommendations/introduction-to-recommendations.md) | Nieuw onderwerp. |
|  | [Criteria maken](/help/c-recommendations/c-algorithms/create-new-algorithm.md#recently-viewed) | Opmerking toegevoegd aan onlangs bekeken objecten. |
|  | [Bekende problemen en opgeloste problemen](/help/r-release-notes/known-issues-resolved-issues.md#preview) | Bekende uitgave toegevoegd met de voorvertoningskoppelingen voor Activity QA. |
| 29 juli 2019 | [Veelgestelde vragen over rapportage](/help/c-reports/reporting-frequently-asked-questions.md) | Nieuwe veelgestelde vragen toegevoegd: &quot;Waarom bevatten mijn [!UICONTROL Ervaring richtend] (XT) rapporten metriek voor controleervaringen?&quot; |
| 24 juli 2019 | [Upgrade uitvoeren vanaf 0,js 1.*x* tot at.js 2.*x *](/help/c-implementing-target/c-implementing-target-for-client-side-web/upgrading-from-atjs-1x-to-atjs-20.md) | Nieuwe sectie toegevoegd: Ondersteuning voor [interdomeintracering in at.js 2.x](/help/c-implementing-target/c-implementing-target-for-client-side-web/upgrading-from-atjs-1x-to-atjs-20.md#cross-domain) |
|  | [Apple Intelligent Tracking Prevention (ITP) 2.*x *](/help/c-implementing-target/c-considerations-before-you-implement-target/c-privacy/apple-itp-2x.md) | Nieuw onderwerp. |
|  | [Aanbevelingen als voorstel](/help/c-recommendations/recommendations-as-an-offer.md#status) | Nieuwe sectie toegevoegd: &quot;De status van de aanbevelingen bekijken.&quot; |
|  | [Feeds](/help/c-recommendations/c-products/feeds.md) | De rij &#39;Items importeren&#39; is bijgewerkt en de rij &#39; *Op tijd* geïmporteerd feed&#39; is toegevoegd onder [Voederstatus](/help/c-recommendations/c-products/feeds.md#status). |
|  | [Catalogus zoeken](/help/c-recommendations/c-products/catalog-search.md) | Bijgewerkte tekst over hoe de catalogus wordt vernieuwd. |
|  | [Werken met Adobe Target](/help/c-intro/how-target-works.md#bots) | Nieuwe sectie toegevoegd: &quot;Bots.&quot; |
|  | [Profielkenmerken](/help/c-target/c-visitor-profile/profile-parameters.md#best) | Toegevoegde beste praktijken om langzame regex uitvoering te vermijden. |
|  | [Feeds](/help/c-recommendations/c-products/feeds.md#steps) | Ondersteunde FTP-serverinstellingen zijn toegevoegd aan stappen. |
|  | [details van de at.js-versie](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md) | Extra informatie over at.js 2.1.1. |
|  | [Opmerkingen bij](/help/r-release-notes/release-notes.md)de release: 19.7.1 | Deze release bevat verbeteringen en correcties. U kunt over hen lezen en met de documentatie van de Nota&#39;s van de Versie verbinden. Deze release bevat ook een groot aantal documentatie-updates voor de hele Help. |

## Adobe Target Standard/Premium 19.6.1 (26 juni 2019) {#tgt-19-6-1}

| Datum | Onderwerp | Wijzigingen |
| --- | --- | --- |
| 10 juli 2019 | [Limieten](/help/r-troubleshooting-target/target-limits.md) | Extra limietgegevens voor de volgende items:<ul><li>Aantal ervaringen per activiteit.</li><li>Aantal succesmetingen per activiteit.</li><li>Aantal verslaggevingsdoelgroepen/segmenten per activiteit.</li><li>Aantal doelgroepen per doos, metrisch en ervaring.</li><li>Aantal unieke waarden per doelregel.</li><li>Aantal unieke doelgroepen per doelregel.</li><li>Aantal unieke doelregels per activiteit.</li><li>Aantal actieve profielscripts.</li><li>Aantal scripts in totaal profiel.</li><li>Aantal totale lussen per profielmanuscript.</li><li>Aantal levende activiteiten.</li><li>Aantal actieve opgeslagen (en niet beëindigde) activiteiten.</li><li>Aantal eigenschappen.</li><li>Aantal voorstellen.</li></ul> |
|  | [Opmerkingen bij de release Doel (preRelease)](/help/r-release-notes/target-release-notes.md) | Toegevoegde informatie over de aanstaande release van Target 19.7.1 (23 juli 2019).<br>Deze gegevens kunnen worden gewijzigd. |
| 8 juli 2019 | [CNAME en Adobe Target](/help/c-implementing-target/c-considerations-before-you-implement-target/implement-cname-support-in-target.md) | Toegevoegde informatie die verklaart waarom u CNAME zou moeten gebruiken. |
| 28 juni 2019 | [Bekende problemen en opgeloste](/help/r-release-notes/known-issues-resolved-issues.md#redirect)<br>[problemenVerwachte gegevensvariaties tussen Target en Analytics bij gebruik en niet bij gebruik van A4](/help/c-integrating-target-with-mac/a4t/understanding-expected-data-variances.md)<br>[TRedirect aanbiedingen-A4T Veelgestelde vragen](/help/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-redirect-offers.md) | Toegevoegde informatie over een bekende kwestie die een beperkt aantal klanten veroorzaakt die omleidingen met A4T gebruiken om een hoger percentage van unstitched hit tarieven te zien. |
| 26 juni 2019 | [Opties voor visuele ervaring](/help/c-experiences/c-visual-experience-composer/viztarget-options.md#styles) | Informatie toegevoegd over de optie [!UICONTROL Achtergrond] onder *Stijlen*. |
|  | [Single Page App (SPA) Visual Experience Composer](/help/c-experiences/spa-visual-experience-composer.md) | Informatie toegevoegd over de handeling [!UICONTROL Klonen] . |
|  | [Klikken bijhouden](/help/c-activities/r-success-metrics/click-tracking.md) | Informatie over het deelvenster [!UICONTROL Geselecteerde elementen] toegevoegd. |
|  | [Single Page App (SPA) Visual Experience Composer](/help/c-experiences/spa-visual-experience-composer.md#page-delivery-settings) | Nieuwe sectie: &quot;De montages van de Levering van de pagina voor SPA VEC.&quot; |
|  | [Selecteer de controle voor uw Geautomatiseerde Personalisatie of Auto-Doelactiviteit](/help/c-activities/t-automated-personalization/experience-as-control.md) | Nieuw onderwerp. |
|  | [Google Chrome SameSite-cookiebeleid](/help/c-implementing-target/c-considerations-before-you-implement-target/c-privacy/google-chrome-samesite-cookie-policies.md) | Nieuw onderwerp. |
|  | [Gegevensverzameling voor de personalisatiealgoritmen van het Doel](/help/c-activities/t-automated-personalization/ap-data.md) | Nieuwe tabellen toegevoegd om afzonderlijke kenmerken toe te lichten en voorbeelden te geven. |
|  | [Veelgestelde vragen over geautomatiseerde personalisatie](/help/c-activities/t-automated-personalization/automated-personalization-faq.md) | Nieuwe veelgestelde vragen toegevoegd: &quot;Kan ik een specifieke ervaring specificeren die als controle moet worden gebruikt?&quot;<br>Bewerkt de volgende veelgestelde vragen: &quot;Wat zijn beste praktijken aan opstelling een Geautomatiseerde Personalisatieactiviteit?&quot; |
|  | [Automatisch doel](/help/c-activities/auto-target-to-optimize.md) | Toegevoegde informatie en FAQ over het specificeren van een specifieke ervaring die als controle moet worden gebruikt.<br>De sectie &quot;Bepaling van verkeerstoewijzing&quot; is bijgewerkt. |
|  | [Een Automated Personalization-activiteit maken](/help/c-activities/t-automated-personalization/create-ap-activity.md) | Toegevoegde stap met informatie om een specifieke ervaring als gebrek te selecteren. |
|  | [Bekende problemen en opgeloste problemen](/help/r-release-notes/known-issues-resolved-issues.md) | Toegevoegde informatie over rapporten die niet voor Auto-Doelactiviteiten in bepaalde situaties teruggeven. |
|  | [Opmerkingen bij](/help/r-release-notes/release-notes.md)de release: 19.6.1. | Deze release bevat verbeteringen en correcties. U kunt over hen lezen en met de documentatie van de Nota&#39;s van de Versie verbinden. Deze release bevat ook een groot aantal documentatie-updates voor de hele Help. |

## Adobe Target Standard/Premium 19.5.1 (21 mei 2019) {#tgt-19-5-1}

| Datum | Onderwerp | Wijzigingen |
| --- | --- | --- |
| 19 juni 2019 | [Promoties toevoegen](/help/c-recommendations/t-create-recs-activity/adding-promotions.md) | Extra informatie over aanbiedingen die worden gedupliceerd ten opzichte van objecten die worden aanbevolen door de criteria voor je activiteit. |
| 13 juni 2019 | [Rapport Belangrijke kenmerken](/help/c-reports/c-personalization-insights-reports/important-attributes-report.md) | Nieuwe veelgestelde vragen toegevoegd: &quot;Waarom ontvangen sommige aanbiedingen/ervaringen met een lagere omrekeningskoers een grotere hoeveelheid verkeer dan andere aanbiedingen/ervaringen voor een bepaald geautomatiseerd segment?&quot; |
|  | [De werking van Adobe Target](/help/c-intro/how-target-works.md) | Belangrijke opmerking toegevoegd over het gebruik van Target in China. |
|  | [Ondersteunde browsers](/help/c-implementing-target/c-considerations-before-you-implement-target/supported-browsers.md) | Microsoft Internet Explorer 11 (IE 11) is verwijderd uit de sectie &quot;Target Standard/Premium interface&quot;. Het doel ondersteunt of handhaaft geen compatibiliteit meer voor IE 11. Deze wijziging is alleen van invloed op de doelinterface. Dit heeft geen invloed op de levering van inhoud. Deze wijziging volgt op vergelijkbare aankondigingen van Adobe Analytics, het Adobe Experience Platform en Adobe Audience Manager. We raden gebruikers aan over te schakelen op een ondersteunde browser. |
| 11 juni 2019 | [Activiteitenschepping](/help/c-integrating-target-with-mac/a4t/campaign-creation.md) | Verwijderde notitie die aangeeft dat een trackingserver moet worden opgegeven als u A4T gebruikt. |
|  | [Activiteiten](/help/c-activities/activities.md) | Benadrukt dat u een geschrapte activiteit niet kunt herstellen. Als beste praktijken kunt u een activiteit archiveren zodat het kan worden unarchived, indien nodig. |
|  | [Bijwerken van at.js 1.x naar at.js 2.x](/help/c-implementing-target/c-implementing-target-for-client-side-web/upgrading-from-atjs-1x-to-atjs-20.md) | Verwijderde beperking die aangeeft dat de Experience Cloud Debugger niet volledig wordt ondersteund in at.js 2.x. |
| 7 juni 2019 | [Een ontwerp aanpassen met Snelheid](/help/c-recommendations/c-design-overview/customizing-a-template.md#default) | Nieuwe sectie toegevoegd: &quot;Scenario: Maak een ontwerp met standaardaanbevelingen van 4x2 met logica voor null-controle.&quot; |
|  | [Trainingsvideo&#39;s voor Adobe Target Standard en Premium](/help/c-intro/target-standard-premium-training-videos.md#tutorials) | Bijgewerkte koppeling naar nieuwe Adobe Target Tutorials-site. |
| 6 juni 2019 | [adobe.target.triggerView (viewName, options) - at.js 2.x](/help/c-implementing-target/c-implementing-target-for-client-side-web/adobe-target-triggerview-atjs-2.md) | De beschrijving van de `options > page` parameter is bijgewerkt. |
|  | [Eerste stappen van beheerder](/help/administrating-target/start-target.md) | Geheel artikel bijgewerkt. |
|  | [Opmerkingen bij de release Doel (preRelease)](/help/r-release-notes/target-release-notes.md) | Opmerkingen bij de voorlopige release voor de doelversie 19.6.1 zijn toegevoegd. |
|  | [Bijwerken van at.js 1.x naar at.js 2.x](/help/c-implementing-target/c-implementing-target-for-client-side-web/upgrading-from-atjs-1x-to-atjs-20.md) | Bijgewerkte informatie over de implementatie van at.js met Adobe Launch, de voorkeursmethode voor de implementatie. |
|  | [Doelsleutelbegrippen](/help/c-intro/target-key-concepts.md) | Kleine tekstbewerkingen. |
| 3 juni 2019 | [Opmerkingen bij de release (huidig)](/help/r-release-notes/release-notes.md) | Informatie toegevoegd over de aanstaande release van at.js 2.1.0. |
|  | [details van de at.js-versie](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md) | Informatie toegevoegd over de aanstaande release van at.js 2.1.0. |
|  | [Voordat u gaat implementeren](/help/c-integrating-target-with-mac/a4t/before-implement.md) | Nieuwe sectie toegevoegd: &quot;Logboekregistratie voor clientanalyse.&quot; |
|  | [Analyses voor doelimplementatie](/help/c-integrating-target-with-mac/a4t/a4timplementation.md) | Herziene stap 7. |
|  | [adobe.target.getOffers(options) - at.js 2.x](/help/c-implementing-target/c-implementing-target-for-client-side-web/adobe-target-getoffers-atjs-2.md) | Er zijn rijen toegevoegd aan de tabel voor de volgende veldnamen:<ul><li>Verzoek > ExperienceCloud</li><li>Request > ExperienceCloud > Analytics</li><li>Request > ExperienceCloud > Analytics > logging</li></ul> |
|  | [at.js-functies](/help/c-implementing-target/c-implementing-target-for-client-side-web/cmp-atjs-functions.md) | Rij toegevoegd aan de tabel voor `adobe.target.sendNotifications(options)`. |
|  | [adobe.target.sendNotifications(options)](/help/c-implementing-target/c-implementing-target-for-client-side-web/adobe.target.sendnotifications-atjs-21.md) | Nieuw onderwerp. |
|  | [Bijwerken van at.js 1.x naar at.js 2.x](/help/c-implementing-target/c-implementing-target-for-client-side-web/upgrading-from-atjs-1x-to-atjs-20.md#integrations) | Extra informatie over ondersteuning voor Adobe Opt-in vindt u in at.js 2.1.0. |
|  | [Privacy en algemene gegevensbeschermingsverordening](/help/c-implementing-target/c-considerations-before-you-implement-target/c-privacy/cmp-privacy-and-general-data-protection-regulation.md) | Bijgewerkte informatie over opt-in-ondersteuning in at.js 2.1.0. |
| 31 mei 2019 | [Mobiel](/help/c-target/c-audiences/c-target-rules/mobile.md) | Opmerking toegevoegd over doelapparaten met iOS 12.2. |
|  | [Aanbevelingen plannen en implementeren](/help/c-recommendations/plan-implement.md) | Bijgewerkt codevoorbeeld. |
| 30 mei 2019 | [Toegang tot doel via de Adobe Experience Cloud](/help/c-intro/target-access-from-mac.md#doc-lang) | De documentatie is nu beschikbaar in de Vereenvoudigde taal van het Chinees. |
|  | [Gegevens downloaden in een CSV-bestand](/help/c-reports/downloading-data-in-csv-file.md) | Nieuw voorbehoud toegevoegd in de sectie Bestelgegevens exporteren aan CSV: &quot;Het publiek dat in het Doel wordt toegepast rapporteert UI draagt niet over aan het downloadrapport.&quot; |
|  | [Rapportinstellingen](/help/c-reports/c-report-settings/report-settings.md) | Bijgewerkte schermafbeeldingen. |
| 29 mei 2019 | [Categorie-affiniteit](/help/c-target/c-visitor-profile/category-affinity.md) | Bijgewerkte tekst om het verschil tussen `user.categoryId` en `entity.categoryId`te verduidelijken. |
|  | [Migreren van mbox.js naar at.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-target-atjs-implementation/target-atjs-implementation.md) | Verplaatste sectie naar dit onderwerp: Voordelen van at.js. |
|  | [om.js Veelgestelde Vragen](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-target-atjs-faq/target-atjs-faq.md) | Verplaatste sectie naar dit onderwerp: &quot;Wat is het effect van at.js en mbox.js op pagina-ladingstijd?&quot; |
|  | [Dynamische gegevens in aanbiedingen doorgeven](/help/c-experiences/c-manage-content/passing-profile-attributes-to-the-html-offer.md) | Gecorrigeerde syntaxis in de gedragsrij Afgelopen. |
| 28 mei 2019 | [Toegang tot doel via de Adobe Experience Cloud](/help/c-intro/target-access-from-mac.md#doc-lang) | Nieuwe sectie toegevoegd: &quot;Wijzig de taal voor de productdocumentatie van het Doel.&quot; |
|  | [Een winnaar bepalen](/help/c-activities/automated-traffic-allocation/determine-winner.md) | Bijgewerkte informatie over p-waarden. |
|  | [Problemen oplossen met betrekking tot Visual Experience Composer en Enhanced Experience Composer](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/issues-related-to-the-visual-experience-composer-vec-and-enhanced-experience-composer-eec.md) | Toegevoegde het oplossen van problemensectie over hoe het Doel multi-level iframes behandelt. |
|  | [Veelgestelde vragen over aanbevelingen](/help/c-recommendations/c-recommendations-faq/recommendations-faq.md) | Nieuwe veelgestelde vragen toegevoegd: &quot;Wat is de verwachte ingangstijd voor de verrichtingen van Aanbevelingen?&quot; |
|  | [Doel implementeren met Adobe Launch](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/cmp-implementing-target-using-adobe-launch.md) | Bijgewerkt de informatie onder &quot;Voordelen van het Uitvoeren at.js die de Uitbreiding van de Lancering van het Doel gebruiken.&quot; |
|  | [Problemen met de levering van inhoud oplossen](/help/c-activities/c-troubleshooting-activities/content-trouble.md) | Er is een nieuwe sectie toegevoegd over het oplossen van problemen in het bestand at.js. Er worden geen selectievakjes geactiveerd als u een ongeldig documenttype gebruikt. |
| 24 mei 2019 | [Opmerkingen bij de release Doel (preRelease)](/help/r-release-notes/target-release-notes.md) | Extra informatie over at.js 2.1.0. |
| 23 mei 2019 | [Uitsluitingen beheren](/help/c-activities/t-automated-personalization/managing-exclusions.md) | Toegevoegde informatie en link om te beperken welke doelgroepen specifieke aanbiedingen kunnen zien in AP-activiteiten die zich richten op regels. |
|  | [Serverzijde: Doel implementeren](/help/c-implementing-target/c-api-and-sdk-overview/api-and-sdk-overview.md) | Bijgewerkte tekst in de inleiding. |
|  | [Ervaringen en aanbiedingen](/help/c-experiences/experiences.md) | Bijgewerkte tekst in de inleiding. |
|  | [Soorten publiek](/help/c-target/target.md) | Bijgewerkte tekst in de inleiding. |
|  | [Succeswaarden](/help/c-activities/r-success-metrics/success-metrics.md) | Bijgewerkte tekst in de inleiding. |
|  | [Rapporten](/help/c-reports/reports.md) | Bijgewerkte tekst in de inleiding. |
|  | [Visual Experience Composer (VEC)](/help/c-experiences/c-visual-experience-composer/visual-experience-composer.md) | Bijgewerkte tekst in de inleiding. |
|  | [Form-based Experience Composer](/help/c-experiences/form-experience-composer.md) | Bijgewerkte tekst in de inleiding. |
|  | [Machtigingen voor Enterprise-gebruikers](/help/administrating-target/c-user-management/property-channel/property-channel.md) | Bijgewerkte tekst in de inleiding. |
|  | [Verklarende woordenlijst](/help/c-intro/glossary.md) | Verschillende items toegevoegd en bijgewerkt. |
| 22 mei 2019 | [Inleiding tot doel](/help/c-intro/intro.md#kit) | Koppeling naar de Adobe Target-welkomstkit toegevoegd. |
| 21 mei 2019 | [Single Page App (SPA) Visual Experience Composer](/help/c-experiences/spa-visual-experience-composer.md) | <ul><li>Bijgewerkte informatie over de optie Verplaatsen.</li><li>Opmerking toegevoegd: u kunt veel handelingen uitvoeren voordat de pagina in de VEC wordt geladen of zelfs als de pagina niet volledig wordt geladen. </li></ul> |
|  | [Gebruikers](/help/administrating-target/c-user-management/c-user-management/user-management.md) | Bijgewerkte tekst, bijgewerkte afbeeldingen en trainingsvideo. |
|  | [Bedrijfsmachtigingen configureren](/help/administrating-target/c-user-management/property-channel/properties-overview.md) | Bijgewerkte tekst en afbeeldingen. |
|  | [Limieten](/help/r-troubleshooting-target/target-limits.md) | De tekenlimiet voor de alias-id van het klantkenmerk is toegevoegd. |
|  | [Opmerkingen bij](/help/r-release-notes/release-notes.md)de release: 19.5.1. | Deze release bevat verbeteringen en correcties. U kunt over hen lezen en met de documentatie van de Nota&#39;s van de Versie verbinden. Deze release bevat ook een groot aantal documentatie-updates voor de hele Help. |

## Adobe Target Standard/Premium 19.4.2 (30 april 2019) {#target-19-4-2}

**Opmerking**: De doelversie van Standard/Premium 19.4.1 was een onderhoudsrelease om de gebruikersinterface van Adobe Experience Cloud bij te werken met informatie over branding en productwijzigingen.

| Datum | Onderwerp | Wijzigingen |
| --- | --- | --- |
| 15 mei 2019 | [Toepassing van één pagina](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/target-atjs-single-page-application.md#triggerview) | Opmerking toegevoegd: u moet de gebeurtenissen `at-view-start` en `at-view-end` gebeurtenissen starten. |
|  | [Dynamische gegevens in aanbiedingen doorgeven](/help/c-experiences/c-manage-content/passing-profile-attributes-to-the-html-offer.md) | Bijgewerkte tekst. |
| 13 mei 2019 | [Activiteit QA](/help/c-activities/c-activity-qa/activity-qa.md) | Item toegevoegd aan de lijst Overwegingen over het gebruik van de QA-modus in een activiteit van meerdere pagina&#39;s. |
|  | [Dezelfde ervaring opnemen op vergelijkbare pagina&#39;s](/help/c-experiences/c-visual-experience-composer/temtest.md) | Bijgewerkte stappen die overeenkomen met de gebruikersinterface. |
|  | [om.js Veelgestelde Vragen](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-target-atjs-faq/target-atjs-faq.md) | Nieuwe veelgestelde vragen toegevoegd: &quot;Welk HTML-doctype vereist at.js?&quot; |
| 10 mei 2019 | [Voorkeuren](/help/administrating-target/r-target-account-preferences/target-account-preferences.md) | Tekst en afbeelding zijn bijgewerkt. |
|  | [Activiteit QA](/help/c-activities/c-activity-qa/activity-qa.md) | Bijgewerkte tekst. |
| 9 mei 2019 | [A4T-rapportage](/help/c-integrating-target-with-mac/a4t/reporting.md#reports-in-analysis-workspace) | Nieuwe sectie toegevoegd: &quot;Rapporten in de Werkruimte van de Analyse.&quot; |
|  | [Rapporten weergeven - Veelgestelde vragen voor A4T](/help/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-viewing-reports.md) | Nieuwe veelgestelde vragen toegevoegd: &quot;Kan ik mijn doelactiviteitgegevens weergeven in de Adobe Analyse Workspace?&quot; |
|  | [Machtigingen voor Enterprise-gebruikers](/help/administrating-target/c-user-management/property-channel/property-channel.md#faqs) | Nieuwe veelgestelde vragen toegevoegd: &quot;Zijn klikspooromzettingen geregistreerd als een omleidingspagina en activiteit URL tot verschillende eigenschappen behoren?&quot; |
| 8 mei 2019 | [Trainingsvideo&#39;s voor Adobe Target Standard en Premium](/help/c-intro/target-standard-premium-training-videos.md) | Inhoud en koppelingen zijn bijgewerkt. |
|  | [Entiteitskenmerken](/help/c-recommendations/c-products/entity-attributes.md) | Bijgewerkte tekst in de notitie onder de `entity.id` variabele. |
| 1 mei 2019 | [Entiteitskenmerken](/help/c-recommendations/c-products/entity-attributes.md) | Gecorrigeerd hoofdlettergebruik in de volgende variabelenamen:<br>Gewijzigd `pageURL` in `pageUrl`.<br>Veranderd `thumbnailURL` in `thumbnailUrl`. |
| 30 april 2019 | [Opties voor composer visuele ervaring](/help/c-experiences/c-visual-experience-composer/viztarget-options.md) | <ul><li>Nieuwe sectie toegevoegd: &quot;Stijlen.&quot;</li><li>Toegevoegde tabel met HTML5-tags die kunnen worden genest.</li></ul> |
|  | [Klikken bijhouden](/help/c-activities/r-success-metrics/click-tracking.md) | Informatie over de DOM-padfunctie is toegevoegd aan de sectie &quot;Overwegingen&quot;. |
|  | [Status en indicatoren van diervoeders](/help/c-recommendations/c-products/feeds.md#section_5DDC2DECF70A42FDAFF2235E91371537) | De tabel &quot;Feed Statuses&quot; is bijgewerkt. |
|  | [Werken met inhoud in de bibliotheek](/help/c-experiences/c-manage-content/assets-working.md) | Informatie toegevoegd over het verwijderen van mappen en afbeeldingen uit de elementenbibliotheek. |
|  | [Opmerkingen bij](/help/r-release-notes/release-notes.md)de release: 19.4.2. | Deze release bevat verbeteringen en correcties. U kunt over hen lezen en met de documentatie van de Nota&#39;s van de Versie verbinden. Deze release bevat ook een groot aantal documentatie-updates voor de hele Help. |

## Adobe Target Standard/Premium 19.3.1 (29 maart 2019) {#section-19-3-1}

| Datum | Onderwerp | Wijzigingen |
| --- | --- | --- |
| 29 april 2019 | [Machtigingen voor Enterprise-gebruikers](/help/administrating-target/c-user-management/property-channel/property-channel.md#section_31D3450ADEAE4A29963A34F8E8C19FE0) | Volgende veelgestelde vragen toegevoegd: &quot;Waarom krijg ik een foutenmelding erop wijst die dat geen bezit aan deze activiteit wordt geassocieerd, alhoewel er een toegewezen bezit is?&quot; |
| 24 april 2019 | [Bijwerken van at.js 1.x naar at.js 2.x](/help/c-implementing-target/c-implementing-target-for-client-side-web/upgrading-from-atjs-1x-to-atjs-20.md#types) | Opmerking toegevoegd aan de sectie &quot;Activiteitstypen&quot;. |
|  | [Een e-mailafbeeldingsvenster testen](/help/c-implementing-target/c-non-javascript-based-implementation/testing-email-image-adbox.md) | Hervormd codevoorbeeld. |
|  | [Activiteit QA](/help/c-activities/c-activity-qa/activity-qa.md) | Kleine tipos gecorrigeerd. |
| 23 april 2019 | [Opmerkingen bij de release Doel (preRelease)](/help/r-release-notes/target-release-notes.md) | Opmerkingen bij de bijgewerkte release en datum gewijzigd in 30 april (29 april). |
| 22 april 2019 | [Toegang tot doel via de Adobe Experience Cloud](/help/c-intro/target-access-from-mac.md) | Nieuwe sectie toegevoegd: &quot;Wijzig de standaardtaal voor de doelgebruikersinterface.&quot; |
| 19 april 2019 | [Rapport Automated Segments](/help/c-reports/c-personalization-insights-reports/automated-segments-report.md#section_740910A52FA646B4AC9452F98C2F5719) | Nieuwe veelgestelde vragen toegevoegd: &quot;Is er om het even welke logica aan de orde dat de attributen in een segmentkaart verschijnen?&quot; |
|  | [Feeds](/help/c-recommendations/c-products/feeds.md#section_5DDC2DECF70A42FDAFF2235E91371537) | Bijgewerkte belangrijke opmerking die beschrijft wanneer geüploade entiteiten verlopen. |
| 16 april 2019 | [Rapporten weergeven - Veelgestelde vragen voor A4T](/help/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-viewing-reports.md) | Nieuwe veelgestelde vragen toegevoegd: &quot;Kan ik het percentage van verkeerstoewijzing in een activiteit veranderen die A4T gebruikt nadat de activiteit is geactiveerd?&quot; |
| 15 april 2019 | [Aanvankelijke levering - Veelgestelde vragen A4T](/help/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-initial-provisioning.md) | Nieuwe veelgestelde vragen toegevoegd: &quot;Hoe kan ik een A4T-activiteit met meerdere pagina&#39;s instellen?&quot; |
|  | [Vereisten voor gebruikerstoegang](/help/c-integrating-target-with-mac/a4t/account-reqs.md) | Bijgewerkt onderwerp. |
|  | [Bekende problemen en opgeloste problemen](/help/r-release-notes/known-issues-resolved-issues.md) | Bekende problemen voor uitsluitingsgroepen verplaatst naar de tabel met opgeloste problemen. |
| 11 april 2019 | [adobe.target.getOffers(options) - at.js 2.x](/help/c-implementing-target/c-implementing-target-for-client-side-web/adobe-target-getoffers-atjs-2.md) | Bijgewerkte codevoorbeelden. |
|  | [Helpextensie Visual Experience Composer](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/vec-helper-browser-extension.md) | Toegevoegde schermafbeeldingen. |
|  | [Automatisch toewijzen](/help/c-activities/automated-traffic-allocation/automated-traffic-allocation.md) | De volgende veelgestelde vragen zijn toegevoegd: &quot;Moet ik een ondermaatse ervaring verwijderen uit een automatisch toegewezen activiteit om het proces om een winnaar te bepalen te versnellen?&quot; |
| 10 april 2019 | [Voordat u implementeert](/help/c-integrating-target-with-mac/a4t/before-implement.md) | Kleine tekstupdates voor de sectie &quot;Implementatievereisten&quot; (vereisten opnieuw geordend). |
|  | [adobe.target.triggerView (viewName, options) - at.js 2.x](/help/c-implementing-target/c-implementing-target-for-client-side-web/adobe-target-triggerview-atjs-2.md) | Bijgewerkte tekst voor de parameter &quot;options > page&quot;. |
| 8 april 2019 | [Verwachte gegevensvariaties tussen Doel en Analytics bij gebruik en niet bij gebruik van A4T](/help/c-integrating-target-with-mac/a4t/understanding-expected-data-variances.md) | Bijgewerkte [verwachte gegevensvariantie bij gebruik van A4T](/help/c-integrating-target-with-mac/a4t/understanding-expected-data-variances.md#expected-using-a4t). |
|  | [Vergrote aantallen bezoeken en bezoekers in A4T minimaliseren](/help/c-integrating-target-with-mac/a4t/c-a4t-troubleshooting/minimizing-inflated-visit-and-visitor-counts-a4t.md) | Bijgewerkte informatie over A4T en herleidt onder [Wat tot gedeeltelijke gegevens bijdraagt?](/help/c-integrating-target-with-mac/a4t/c-a4t-troubleshooting/minimizing-inflated-visit-and-visitor-counts-a4t.md#section_C9C906BEAA7D44DAB9D3C03932A2FEB8) |
|  | [Voordat u implementeert](/help/c-integrating-target-with-mac/a4t/before-implement.md#section_A0D2EF18033D4C3997B08A6EBB34C17A) | Bijgewerkt aan de minimale vereisten om A4T te gebruiken met omleidingen (at.js versie 1.6.2). |
|  | [Aanbiedingen omleiden - Veelgestelde vragen A4T](/help/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-redirect-offers.md#section_FA9384C2AA9D41EDBCE263FFFD1D9B58) | <ul><li>Bijgewerkt aan de minimale vereisten om A4T te gebruiken met omleidingen (at.js versie 1.6.2).</li><li>Toegevoegde informatie die beschrijft hoe gegevensmetriek worden geteld wanneer een Target-hit optreedt, maar er vindt geen Analytics-hit plaats. </li> |
|  | [Limieten](/help/r-troubleshooting-target/target-limits.md#excludedid) | Toegevoegde informatie over de limieten van de parameter `excludedIDs` mbox. |
|  | [Bijwerken van at.js 1.x naar at.js 2.x](/help/c-implementing-target/c-implementing-target-for-client-side-web/upgrading-from-atjs-1x-to-atjs-20.md#response-tokens) | Nieuwe sectie toegevoegd: Reactietokens. |
| 5 april 2019 | [Adobe Target Basics Webinar: Inleiding tot aanbevelingen](/help/c-recommendations/recommendations.md#intro-to-recs) | Toegevoegde koppeling naar de webinar-opname &quot;Introduction to Recommendations&quot;. |
|  | [Activity QA-bladwijzer](/help/c-activities/c-activity-qa/activity-qa-bookmark.md) | Bijgewerkte JavaScript-code voor de activiteit QA-bladwijzer. |
|  | [Opmerkingen bij de release Doel (preRelease)](/help/r-release-notes/target-release-notes.md) | Bijgewerkt van de voorlopige releaseopmerkingen voor de versies Target 19.4.1 en Target 19.4.2, beide gepland voor april 2019. |
| 4 april 2019 | [Opmerkingen bij de release Doel (preRelease)](/help/r-release-notes/target-release-notes.md) | Toegevoegde voorlopige releaseopmerkingen voor de versies Target 19.4.1 en Target 19.4.2, beide gepland voor april 2019. |
| 30 maart 2019 | [Limieten](/help/r-troubleshooting-target/target-limits.md#excludedid) | Toegevoegde informatie over de limieten van de parameter `excludedID` mbox. |
| 29 maart 2019 | [Bekende problemen en opgeloste problemen](/help/r-release-notes/known-issues-resolved-issues.md) | Het volgende bekende probleem is toegevoegd: &quot;Voor de websites van de Toepassing van de Enige Pagina (SPA), staat het annuleren van lading u niet toe om acties onder het paneel van [!UICONTROL Wijzigingen] uit te geven.&quot;<br>Verplaatst het volgende bekende probleem naar de sectie Opgeloste problemen: &quot;v1-versie van de API&#39;s voor aanbiedingen op Adobe I/O behandelt alle aanbiedingen die via Target zijn gemaakt, in de standaardwerkruimte.&quot; |
| 28 maart 2019 | [Visual Experience Composer (VEC)](/help/c-experiences/c-visual-experience-composer/visual-experience-composer.md) | De volgende nieuwe secties toegevoegd:<ul><li>[Het laden van een pagina in de VEC annuleren.](/help/c-experiences/c-visual-experience-composer/visual-experience-composer.md#cancel-loading)</li><li>[Bewerk een pagina terwijl de pagina wordt geladen of nadat de pagina niet is geladen](/help/c-experiences/c-visual-experience-composer/visual-experience-composer.md#loading).</li></ul> |
|  | [Opties voor Visual Experience Composer](/help/c-experiences/c-visual-experience-composer/viztarget-options.md) | Nieuwe sectie: &quot;[Navigeren door elementen met het DOM-pad](/help/c-experiences/c-visual-experience-composer/viztarget-options.md#dom-path).&quot; |
|  | [Bekende problemen en opgeloste problemen](/help/r-release-notes/known-issues-resolved-issues.md#cancel) | Er is een bekend probleem toegevoegd over wanneer u het laden van een pagina in de VEC annuleert. |
|  | [Opmerkingen bij](/help/r-release-notes/release-notes.md)de release: 19.3.1. | Deze release bevat verbeteringen en correcties. U kunt over hen lezen en met de documentatie van de Nota&#39;s van de Versie verbinden. Deze release bevat ook een groot aantal documentatie-updates voor de hele Help. |

## Adobe Target Standard/Premium 19.2.1 (19 februari 2019) {#section-19-2-1}

| Datum | Onderwerp | Wijzigingen |
| --- | --- | --- |
| 20 maart 2019 | [om.js Veelgestelde Vragen](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-target-atjs-faq/target-atjs-faq.md) | Bijgewerkt van de volgende veelgestelde vragen: &quot;[Kan ik de doelbibliotheek asynchroon laden?](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-target-atjs-faq/target-atjs-faq.md#section_AB9A0CA30C5440C693413F1455841470)&quot; |
|  | [Profielsynchronisatie in realtime voor mbox3rdPartyID](/help/c-target/c-visitor-profile/3rd-party-id.md) | Opmerking toegevoegd onder aan de pagina. |
|  | [Kenmerken](/help/r-troubleshooting-target/target-limits.md)<br>[van aangepaste entiteit Limits](/help/c-recommendations/c-products/custom-entity-attributes.md#limits) | Toegevoegde informatie over limieten van aangepaste entiteitskenmerken. |
|  | [Veelgestelde vragen over doelen en doelgroepen](/help/c-target/c-troubleshooting-targets-and-audiences/troubleshooting-targets-and-audiences.md#strings-that-represent-numbers) | Bijgewerkte tekst. |
|  | [Nieuwe criteria maken](/help/c-recommendations/c-algorithms/create-new-algorithm.md#custom) | Nieuwe sectie toegevoegd waarin wordt uitgelegd hoe u op profielen gebaseerde groepen voor populariteitsalgoritmen kunt maken: &quot;Gebruik een sleutel voor aangepaste aanbevelingen.&quot; |
| 19 maart 2019 | [Opmerkingen bij de doelversie (huidig)](/help/r-release-notes/release-notes.md) | Extra informatie over at.js versies 2.0.1 en 1.7.1. |
|  | [Rapporten weergeven - Veelgestelde vragen voor A4T](/help/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-viewing-reports.md) | De volgende veelgestelde vragen zijn toegevoegd: &quot;Steunt A4T virtuele rapportsuites?&quot; |
| 18 maart 2019 | [Opmerkingen bij de doelversie (prerelease)](/help/r-release-notes/target-release-notes.md) en [op.js versiedetails](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md) | Extra informatie over at.js versies 2.0.1 en 1.7.1. |
|  | [Methoden om gegevens op te halen uit de kenmerken Doel](/help/c-implementing-target/c-considerations-before-you-implement-target/c-methods-to-get-data-into-target/methods-to-get-data-into-target.md#section_92AB4820A5624C669D9A1F1B6220D4FA) en [Klant](/help/c-target/c-visitor-profile/working-with-customer-attributes.md) | Toegevoegd: U kunt de volgende tekens niet verzenden in `mbox3rdPartyID`: plus-teken (+) en slash (/). |
| 15 maart 2019 | [Voordat u implementeert](/help/c-implementing-target/c-considerations-before-you-implement-target/considerations-before-you-implement-target.md) | Belangrijke opmerking toegevoegd: Wijzigingen in at.js of mbox.js worden niet ondersteund door de klantenservice van Adobe. |
| 14 maart 2019 | [Opmerkingen bij de release Doel (preRelease)](/help/r-release-notes/target-release-notes.md) | De datum van de introductie van Target Standard/Premium 19.3.1 is gewijzigd in 29 maart 2019. |
| 13 maart 2019 | [Een Automated Personalization-activiteit maken](/help/c-activities/t-automated-personalization/create-ap-activity.md) | De tekst in de rij Metrisch omzetten is bijgewerkt. |
|  | [Profielkenmerken](/help/c-target/c-visitor-profile/profile-parameters.md) | Nieuwe sectie toegevoegd: &quot;JavaScript-referentie voor scriptprofielparameters.&quot; |
|  | [at.js-functies](/help/c-implementing-target/c-implementing-target-for-client-side-web/cmp-atjs-functions.md) | Geherstructureerde pagina en nieuwe pagina&#39;s voor elke functie at.js om de toegang tot van informatie gemakkelijker te maken. |
|  | [Hoe werkt at.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/how-atjs-works.md) | Inleidende alinea toegevoegd om een implementatie aan de clientzijde uit te leggen. |
|  | [Veelgestelde vragen over aanbevelingen](/help/c-recommendations/c-recommendations-faq/recommendations-faq.md) | Volgende veelgestelde vragen toegevoegd: &quot;Kan ik een entiteit dynamisch uitsluiten?&quot; |
| 12 maart 2019 | [Een upgrade uitvoeren van at.js 1.x naar at.js 2.x](/help/c-implementing-target/c-implementing-target-for-client-side-web/upgrading-from-atjs-1x-to-atjs-20.md) en [Debug at.js met Adobe Experience Cloud Debugger](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-target-debugging-atjs/target-debugging-atjs.md) | Foutopsporing is nu een ondersteunde integratie met at.js 2.x. |
| 11 maart 2019 | [Opmerkingen bij de doelversie (huidig)](/help/r-release-notes/release-notes.md), opmerkingen bij de<br>[doelversie (pre-release)](/help/r-release-notes/target-release-notes.md)en coderingswijzigingen bij <br>[TLS (Transport Layer Security)](/help/c-implementing-target/c-considerations-before-you-implement-target/tls-transport-layer-security-encryption.md) | Bijgewerkte tekst die aangeeft dat TLS-wijzigingen zullen plaatsvinden op 1 **april 2019**. |
|  | [adobe.target.getOffers](/help/c-implementing-target/c-implementing-target-for-client-side-web/adobe-target-getoffers-atjs-2.md) | De volgende sectie toegevoegd: &quot;Gegevens ophalen en renderen uit meerdere vakken via getOffers() en applyOffers().&quot; |
| 6 maart 2019 | [Bijwerken van at.js 1.x naar at.js 2.x](/help/c-implementing-target/c-implementing-target-for-client-side-web/upgrading-from-atjs-1x-to-atjs-20.md) | Toegevoegd at_property rij aan de &quot;bij.js 1.x parameters aan at.js 2.x ladingstoewijzinglijst&quot;. |
|  | [Toepassing van één pagina](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/target-atjs-single-page-application.md) | Nieuwe sectie toegevoegd: &quot;Gebruik TriggerView om ervoor te zorgen dat A4T correct met at.js 2.x en SPAs.&quot;werkt |
| 4 maart 2019 | [Aanbevelingen Klassieke documentatie](/help/c-recommendations/recommendations-classic-documentaton.md) | Nieuw onderwerp. |
|  | [Activiteiten op het gebied van Aanbevelingen Klassieke versus Aanbevelingen in Target Premium](/help/c-recommendations/c-recommendations-faq/recommendations-classic-versus-recommendations-activities-target-premium.md) | Extra informatie over Aanbevelingen als voorstel. |
| 28 februari 2019 | [Activiteiten](/help/c-activities/activities.md) | Tekst en afbeeldingen zijn bijgewerkt. |
|  | [Inleiding tot doel](/help/c-intro/intro.md) | Added &quot;Aanbevelingen als aanbieding&quot;onder &quot;Premie van het Doel.&quot; |
|  | [Doelsleutelbegrippen](/help/c-intro/target-key-concepts.md) | Bijgewerkte tabel &quot;Activiteitstypen&quot;. |
| 26 februari 2019 | [Bekende problemen en opgeloste problemen](/help/r-release-notes/known-issues-resolved-issues.md) | Er is een bekend probleem toegevoegd met de ondersteuning voor Enterprise-machtigingen in doel-API&#39;s. |
| 25 februari 2019 | [De versienota&#39;s van het doel (huidig)](/help/r-release-notes/release-notes.md), <br>[de versienota&#39;s van het Doel (pre-release)](/help/r-release-notes/target-release-notes.md), en <br>[TLS (de Veiligheid van de Laag van het Vervoer) encryptieveranderingen](/help/c-implementing-target/c-considerations-before-you-implement-target/tls-transport-layer-security-encryption.md) | De volgende informatie is bijgewerkt:<br>Op 20 februari 2019 is de Adobe Target-infrastructuur in de regio&#39;s EMEA, Japan en APAC bijgewerkt en zijn er geen gegevens meer verzameld van eindgebruikers met oudere apparaten of webbrowsers die geen TLS 1.1 of hoger ondersteunen. Dezelfde upgrade is gepland voor de regio Noord-Amerika op 4 **maart 2019**. Migratie naar TLS 1.2 biedt betere beveiliging. Het is belangrijk dat u de details doorloopt en de wijzigingen uitwerkt voor een vloeiende overgang. |
|  | [Bijwerken van at.js 1.x naar at.js 2.x](/help/c-implementing-target/c-implementing-target-for-client-side-web/upgrading-from-atjs-1x-to-atjs-20.md#payload-mapping) | Nieuwe sectie: &quot;at.js 1.x parameters aan at.js 2.x ladingstoewijzing.&quot; |
|  | [Problemen met de Enhanced Experience Composer oplossen](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/troubleshooting-issues-related-to-the-enhanced-experience-composer-eec.md) | De kolom &quot;Hostnames&quot; is toegevoegd aan de IP-adressen van whitelist. |
| 22 februari 2019 | [Bedrijfsmachtigingen configureren](/help/administrating-target/c-user-management/property-channel/properties-overview.md) | Sectie &#39;Uw werkruimte-id verkrijgen&#39; toegevoegd. |
| 20 februari 2019 | [Categorie-affiniteit](/help/c-target/c-visitor-profile/category-affinity.md) | Bijgewerkte sectie &quot;Categorie affiniteitsalgoritme&quot;. |
| 19 februari 2019 | [Single Page App (SPA) Visual Experience Composer](/help/c-experiences/spa-visual-experience-composer.md) | Nieuwe onderwerp- en trainingsvideo&#39;s. |
|  | [Toepassing van één pagina](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/target-atjs-single-page-application.md) | Nieuwe onderwerp- en trainingsvideo&#39;s. |
|  | [details van de at.js-versie](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md) | Informatie toegevoegd over at.js versies 1.7.0 en 2.0.0. |
|  | [Bijwerken van at.js 1.x naar at.js 2.x](/help/c-implementing-target/c-implementing-target-for-client-side-web/upgrading-from-atjs-1x-to-atjs-20.md) | Nieuwe onderwerp- en trainingsvideo. |
|  | [at.js-functies](/help/c-implementing-target/c-implementing-target-for-client-side-web/cmp-atjs-functions.md) | Bijgewerkt onderwerp om op veranderingen met de introductie van at.js 2.x te wijzen.<br>Er zijn drie nieuwe functies beschikbaar voor at.js 2.x.<ul><li>adobe.target.getOffers(options)</li><li>adobe.target.applyOffers(options)</li><li>adobe.target.triggerView (viewName, options)</li></ul> |
|  | [Hoe werkt at.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/how-atjs-works.md) | Bijgewerkt onderwerp om op veranderingen met de introductie van at.js 2.x te wijzen. en trainingsvideo toegevoegd. |
|  | [Hoe at.js flikkering beheert](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/manage-flicker-with-atjs.md) | Bijgewerkt onderwerp om op veranderingen met de introductie van at.js 2.x te wijzen. |
|  | [om.js Veelgestelde Vragen](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-target-atjs-faq/target-atjs-faq.md) | Bijgewerkt onderwerp om op veranderingen met de introductie van at.js 2.x te wijzen. |
|  | [Foutopsporing in.js met Adobe Experience Cloud Debugger](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-target-debugging-atjs/target-debugging-atjs.md) | Opmerking waarin wordt uitgelegd dat de functies Adobe Experience Cloud Debugger Network Request en Mbox Trace nog niet worden ondersteund voor at.js 2.x. |
|  | [at.js cookies](/help/c-implementing-target/c-implementing-target-for-client-side-web/atjs-cookies.md) | Nieuw onderwerp. |
|  | [Aanbevelingen als voorstel](/help/c-recommendations/recommendations-as-an-offer.md) | Nieuw onderwerp. |
|  | [Opties voor composer visuele ervaring](/help/c-experiences/c-visual-experience-composer/viztarget-options.md) | <ul><li>Toegevoegde informatie over het gebruiken van [!UICONTROL Tussenvoegsel vóór, Tussenvoegsel na, of vervangt door] actie om aanbevelingen aan een ervaring in een Test toe te voegen A/B of de Begeleidende activiteit van de Ervaring.</li><li>Er is informatie toegevoegd over het gebruik van de actie [!UICONTROL Invoegen voor of Invoegen na] om AEM-ervaringsfragmenten aan een ervaring toe te voegen.</li></ul> |
|  | [Helpextensie Visual Experience Composer](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/vec-helper-browser-extension.md) | Nieuw onderwerp. |
|  | [Privacy en algemene gegevensbeschermingsverordening](/help/c-implementing-target/c-considerations-before-you-implement-target/c-privacy/cmp-privacy-and-general-data-protection-regulation.md) (GDPR) | Kleine bewerkingen en informatie over de aanmeldingsfunctionaliteit en at.js 1.7.0 en at.js 2.x. |
|  | [Bekende problemen en opgeloste problemen](/help/r-release-notes/known-issues-resolved-issues.md) | Bekende problemen met doel-API&#39;s toegevoegd. |
|  | [Entiteitskenmerken](/help/c-recommendations/c-products/entity-attributes.md) | Opmerking toegevoegd dat bepaalde waarden van entiteitskenmerken na 61 dagen verlopen. |
|  | [Opmerkingen bij](/help/r-release-notes/release-notes.md)de release: 19.2.1. | Deze release bevat verbeteringen en correcties. U kunt over hen lezen en met de documentatie van de Nota&#39;s van de Versie verbinden. Deze release bevat ook een groot aantal documentatie-updates voor de hele Help. |

## Adobe Target Standard/Premium 19.1.1 (22 januari 2019) {#section-19-1-1}

| Datum | Onderwerp | Wijzigingen |
| --- | --- | --- |
| 2 februari 2019 | [Opmerkingen bij](/help/r-release-notes/target-release-notes.md) de release Doel | Bijgewerkte pre-releaseopmerkingen voor de release van [!DNL Target] 19.2.1 (19 februari 2019). |
| 30 januari 2019 | [Doelstellingen en doelgroepen](/help/c-target/c-troubleshooting-targets-and-audiences/troubleshooting-targets-and-audiences.md) | Nieuwe veelgestelde vragen toegevoegd: Tekenreeksen die getallen vertegenwoordigen (drijvende-kommagetallen worden ook ondersteund) worden als getallen vergeleken. |
| 29 januari 2019 | [Opmerkingen bij de doelversie (huidig)](/help/r-release-notes/release-notes.md) | Ondersteuning voor Enterprise-machtigingen in beschikbaarheidsdatum van doel-API&#39;s bijgewerkt naar 21 februari 2019. |
|  | [Systeemstatusupdates en proactieve meldingen](/help/r-release-notes/system-status-updates.md) | Sectie voor proactieve meldingen toegevoegd. |
| 22 januari 2019 | [](/help/c-recommendations/c-products/collections.md)<br>[](/help/c-recommendations/c-products/exclusions.md)<br>[CollectionsExclusionsCatalog](/help/c-recommendations/c-products/catalog-search.md)<br>[](/help/c-recommendations/plan-implement.md#concept_C1E1E2351413468692D6C21145EF0B84)<br>[searchSettingsRecommendations: filterverzamelingen en -uitsluitingen naar omgeving (hostgroep)](/help/administrating-target/hosts.md) | Toegevoegde informatie over het filtreren inzamelingen en uitsluitingen door milieu (gastheergroep). |
|  | [Limieten](/help/r-troubleshooting-target/target-limits.md) | Bijgewerkte informatie in de rij van de Waarde van het Manuscript van het Profiel. |
|  | [Opmerkingen bij](/help/r-release-notes/release-notes.md)de release: 19.1.1. | Deze release bevat verbeteringen en correcties. U kunt over hen lezen en met de documentatie van de Nota&#39;s van de Versie verbinden. Deze release bevat ook een groot aantal documentatie-updates voor de hele Help. |

## Adobe Target Standard/Premium 18.11.1 (12 november 2018) {#section_4AD10E8B7EB04F96807FFDB763F31703}

| Datum | Onderwerp | Wijzigingen |
|--- |--- |--- |
| 16 januari 2019 | [Opmerkingen bij de doelversie (huidig)](/help/r-release-notes/release-notes.md)<br>[Opmerkingen bij de doelversie (prerelease)](/help/r-release-notes/target-release-notes.md)<br>[at.js versiedetails](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md) | Informatie over at.js versie 1.6.3 toegevoegd. |
| 10 januari 2019 | [De Nota&#39;s van de Versie van het doel (huidig)](/help/r-release-notes/release-notes.md)<br>[De Nota&#39;s van de Versie van het doel (prerelease)](/help/r-release-notes/target-release-notes.md)<br>[TLS (de Veiligheid van de Laag van het Vervoer) encryptieveranderingen](/help/c-implementing-target/c-considerations-before-you-implement-target/tls-transport-layer-security-encryption.md) | De datum toegevoegd waarop de ondersteuning voor TLS 1.0-codering volledig wordt beëindigd door Target: 20 februari 2019. |
| 9 januari 2019 | [Opties voor composer visuele ervaring](/help/c-experiences/c-visual-experience-composer/viztarget-options.md) | Informatie toegevoegd over aanbevelingen voor invoegen, invoegen na en vervangen door rijen. |
|  | [Opmerkingen bij de doelversie (huidig)](/help/r-release-notes/release-notes.md)<br>[Opmerkingen bij de doelversie (pre-release)](/help/r-release-notes/target-release-notes.md)<br>[Ondersteunde browsers](/help/c-implementing-target/c-considerations-before-you-implement-target/supported-browsers.md) | Vanaf maart 2019 is er informatie toegevoegd over Target en de Adobe Marketing Cloud die ondersteuning bieden voor Microsoft Internet Explorer 11. |
|  | [Opmerkingen bij de release Doel (preRelease)](/help/r-release-notes/target-release-notes.md) | Toegevoegde informatie voor Target 19.1.1 en at.js 1.6.4 versies. |
|  | [details van de at.js-versie](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md) | Toegevoegde informatie voor release van at.js 1.6.4. |
|  | [Het aantal bezoekers en bezoekers in A4T minimaliseren](/help/c-integrating-target-with-mac/a4t/c-a4t-troubleshooting/minimizing-inflated-visit-and-visitor-counts-a4t.md) | Verwijderd nota die verklaart dat na 14 november 2016, klanten niet meer A4T activiteiten met omleidingsaanbiedingen zullen kunnen tot stand brengen. |
|  | [Aanbiedingen omleiden - Veelgestelde vragen A4T](/help/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-redirect-offers.md) | Opmerking toegevoegd onder &quot;Waarom worden paginaweergaven op de oorspronkelijke pagina en op de pagina voor omleiding soms geteld?&quot; |
| 20 december 2018 | [Implementatiedoel server](../c-implementing-target/c-api-and-sdk-overview/api-and-sdk-overview.md) | Opmerking over CORS toegevoegd. |
| 14 december 2018 | [Doel implementeren met Adobe Launch](../c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/cmp-implementing-target-using-adobe-launch.md) | Toegevoegde koppeling naar een nieuwe trainingsvideo: Doel implementeren met de Adobe-zelfstudie voor starten. |
|  | [Persoonlijkheidsrapporten](../c-reports/c-personalization-insights-reports/personalization-insights-reports.md) | Koppeling naar trainingsvideo toegevoegd. |
| 13 december 2018 | [Form-based Experience Composer](../c-experiences/form-experience-composer.md) | Tekst en afbeelding zijn bijgewerkt. |
|  | [Bekende problemen en opgeloste problemen](known-issues-resolved-issues.md) | Het toegevoegde bekende probleem dat de feed-index van Aanbevelingen &quot;Waiting for index&quot; kan weergeven als de items in de feed gelijk zijn aan de items in de vorige uitvoering. |
|  | [Doelgroep selecteren](../c-activities/t-test-ab/t-test-create-ab/ab-audience.md) | Bijgewerkte afbeeldingen. |
|  | [Ervaring toevoegen](../c-activities/t-test-ab/t-test-create-ab/ab-add-experience.md) | Bijgewerkte afbeelding. |
|  | [Een A/B-test maken](../c-activities/t-test-ab/t-test-create-ab/test-create-ab.md) | Bijgewerkte afbeeldingen. |
|  | [Samenvatting testen](../c-activities/c-multivariate-testing/t-create-multivariate-test/test-summary.md) | Bijgewerkte afbeelding. |
|  | [Voorvertoning van ervaringen voor een multivariatietest](../c-activities/c-multivariate-testing/t-create-multivariate-test/preview-experiences.md) | Bijgewerkte afbeelding. |
|  | [Combinaties maken](../c-activities/c-multivariate-testing/t-create-multivariate-test/add-offers.md) | Tekst en afbeeldingen zijn bijgewerkt. |
|  | [Een multivariatietest maken](../c-activities/c-multivariate-testing/t-create-multivariate-test/create-multivariate-test.md) | Tekst en afbeeldingen zijn bijgewerkt. |
| 11 december 2018 | [targetGlobalSettings](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetgobalsettings.md) | Toegevoegd dat de standaardwaarde voor overrideMboxEdgeServer &quot;waar&quot; is, te beginnen met at.js versie 1.6.2. |
| 7 december 2018 | [ Bekende problemen en opgeloste problemen ](known-issues-resolved-issues.md) | Verplaatst het volgende van de Bekende lijst van Kwesties naar de Resolved lijst van Kwesties: <ul><li>at.js: Mboxen die niet worden geactiveerd in Microsoft Explorer 11-browsers na de upgrade naar at.js versie 1.0 vanwege de interactie tussen at.js en Visitor API 2.2.0.0.</li><li>Geo gericht: Het zoeken naar een tekenreeks die speciale tekens bevat (zoals een spatie of komma) werkt momenteel niet wanneer u doelgroepen maakt.</li></ul> |
| 5 december 2018 | [ Persoonlijkheidsrapporten ](../c-reports/c-personalization-insights-reports/personalization-insights-reports.md) | Toegevoegde nota dat de rapporten van de Inzichten van de Personalisatie slechts in het standaardmilieu beschikbaar zijn. |
|  | [ Adobe Analytics as the reporting source for Adobe Target (AT) ](../c-integrating-target-with-mac/a4t/a4t.md) | Bijgewerkte lijst om erop te wijzen dat A4T server-zijplaatsingen steunt. |
| 29 november 2018 | [ Schatting van het verkeer dat nodig is voor een geslaagde test](../c-activities/c-multivariate-testing/t-create-multivariate-test/traffic-estimator.md) | Kleine tekstupdates en bijgewerkte afbeeldingen. |
| 27 november 2018 | [ Activiteiten ](../c-activities/activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03) | Tekst en afbeeldingen zijn bijgewerkt. |
|  | [ Profielscriptkenmerken ](../c-target/c-visitor-profile/profile-parameters.md#concept_8C07AEAB0A144FECA8B4FEB091AED4D2) | Opmerking toegevoegd: Target heeft een limiet van 1.000 profielscripts per account. |
| 15 november 2018 | [ Opmerkingen bij de doelversie (huidig) Opmerkingen bij de ](../r-release-notes/release-notes.md#reference_8FE40B43A5A34DDF8F26A53D55EE036A)<br>[ doelversie (pre-release) ](../r-release-notes/target-release-notes.md#reference_4A966062C61048D1A81412E2DDB16E34)<br>[ om.js versiedetails ](../c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md#reference_DBB5EDB79EC44E558F9E08D4774A0F7A) | Informatie toegevoegd over at.js versie 1.6.4. |
|  | [ Persoonlijkheidsrapporten ](../c-reports/c-personalization-insights-reports/personalization-insights-reports.md#concept_A897070E1EDC403EB84CFB7A6ECAD767) | Nieuwe onderwerpen toegevoegd voor de nieuwe rapporten van de Inzichten van de Personalisatie:  Geautomatiseerde segmenten en belangrijke kenmerken. |
| 14 november 2018 | Release 18.11.1 [ Opmerkingen bij de doelversie (huidige) ](../r-release-notes/release-notes.md#reference_8FE40B43A5A34DDF8F26A53D55EE036A) | Deze release bevat verbeteringen en correcties. U kunt over hen lezen en met de documentatie van de Nota&#39;s van de Versie verbinden. Deze release bevat ook een groot aantal documentatie-updates voor de hele Help. |

## Adobe Target Standard/Premium 18.10.1 (24 oktober 2018) {#section_F3DB9A89D944428DBEE04634EB712601}

| Datum | Onderwerp | Wijzigingen |
|--- |--- |--- |
| 8 november 2018 | [Adobe Analytics als de rapportbron voor Adobe Target (A4T)](../c-integrating-target-with-mac/a4t/a4t.md#concept_7540C8C04259434AB6EE33B09F47A1DE) | De NodeJS SDK is toegevoegd aan de compatibiliteitstabel. |
| 7 november 2018 | [Hoe lang moet u een A/B-test uitvoeren?](../c-activities/t-test-ab/sample-size-determination.md#concept_2801F552DB874C20B8A17C1B774C0383) | Bewerkt onderwerp en aanvullende informatie toegevoegd. |
|  | [Opmerkingen bij de release Doel (preRelease)](../r-release-notes/target-release-notes.md#reference_4A966062C61048D1A81412E2DDB16E34) | Extra informatie over functies in de doelversie 18.11.1. |
| 5 november 2018 | [Aanbevelingen integreren met e-mail](../c-recommendations/c-recommendations-faq/integrating-recs-email.md#reference_256B16C894864F24AF970E43DC174420) | Bijgewerkte koppeling in optie 3. |
|  | [Klantkenmerken](../c-target/c-visitor-profile/working-with-customer-attributes.md#concept_16C5C434D32D4EB1AD44A71821F3DEE8) | De volgende opmerking is toegevoegd:<br>**Belangrijk **: De naam van de gegevensbron en de kenmerknaam mogen geen punt bevatten. |
| 31 oktober 2018 | [Systeemstatusupdates](../r-release-notes/system-status-updates.md#concept_5CBDF506BEFA40E483CC7DE0DA915EAD) | Bijgewerkt onderwerp. |
|  | [Doelbasis van de webinarreeks](../cmp-resources-and-contact-information.md#concept_11902FAC95C64479AABE020557A7EEE4) | Toegevoegde verbinding aan de Beste praktijken in de opname van de Segmentatie van het Publiek. |
| 29 oktober 2018 | [De encryptieveranderingen van TLS (de Veiligheid van de Laag van het Vervoer)](../c-implementing-target/c-considerations-before-you-implement-target/tls-transport-layer-security-encryption.md#concept_CC1001E9D3AE4BABAF90B8311B0A6451) | Nieuwe sectie toegevoegd: Gedrag verwacht met browsers die alleen TLS 1.0 ondersteunen. |
| 26 oktober 2018 | [Bekende problemen en opgeloste problemen](../r-release-notes/known-issues-resolved-issues.md#concept_625C3A16B7F24D4B82EFF130F0945541) | <ul><li>Er is een bekend probleem toegevoegd met het zoeken naar tekenreeksen die speciale tekens bevatten wanneer u doelgroepen maakt.</li><li>Verplaatst om 1.js 1.6.0 richt kwestie aan de lijst van Opgeloste Kwesties opnieuw.</li><li>Probleem verplaatst naar de tabel Opgeloste problemen met betrekking tot activiteiten in de standaardwerkruimte die zijn verwijderd via API die wordt weergegeven in de doelinterface</li></ul> |
| 24 oktober 2018 | [Voorkeuren](../administrating-target/r-target-account-preferences/target-account-preferences.md#reference_0CF97B1C2214412ABBC8222EA8A36D7E) | Toegevoegde informatie waarmee u rekening moet houden wanneer u de rapportbron kiest voor activiteiten in Setup > Voorkeuren of per activiteit. |
|  | [Een Automated Personalization-activiteit maken](../c-activities/t-automated-personalization/create-ap-activity.md#task_8AAF837796D74CF893CA2F88BA1491C9) | Toegevoegde informatie over het filtreren voor Niet toegewezen Aanbiedingen. |
|  | [Ervaring maken](../c-activities/t-experience-target/t-xt-create/xt-add-experience.md#task_454646F2895242D3B92DC395A0CE1A00) | Toegevoegde informatie over het dupliceren van ervaringen in XT-activiteiten. |
|  | [Ervaring toevoegen](../c-activities/t-test-ab/t-test-create-ab/ab-add-experience.md#task_454646F2895242D3B92DC395A0CE1A00) | Toegevoegde informatie over het dupliceren van ervaringen in A/B-tests. |
|  | [Informatie over publiek](../c-target/c-audiences/audiences.md#concept_65BE870D290E412D8BBF557EEA67C271) | Toegevoegde informatie over de verwerking van publiek waarnaar wordt verwezen in Doelactiviteiten die zijn verwijderd in Adobe Audience Manager (AAM). |
|  | [at.js-integratie](../c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/target-atjs-integrations.md#concept_C100BC4F073C4B57A608B309D0157B39) | Bijgewerkt onderwerp. |
|  | [Doel implementeren zonder tagbeheer](../c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/implementing-target-without-a-tag-manager.md#topic_397FFA3D6918456BBE02A9FBE9537894) | Alle secties zijn bijgewerkt.  Nieuwe sectie toegevoegd: om.js Implementatie. |
|  | Release 18.10.1 [Opmerkingen bij de release](../r-release-notes/release-notes.md#reference_8FE40B43A5A34DDF8F26A53D55EE036A) | Deze release bevat verbeteringen en correcties. U kunt over hen lezen en met de documentatie van de Nota&#39;s van de Versie verbinden. Deze release bevat ook een groot aantal documentatie-updates voor de hele Help. |

## Adobe Target Standard/Premium 18.9.1 (26 september 2018) {#section_F7E74227BB9D467E9ABC0797EDC2FE0D}

<table id="table_0348AA29207D48A4BDFFA187F4F845B7"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Datum </th> 
   <th colname="col2" class="entry"> Onderwerp </th> 
   <th colname="col3" class="entry"> Wijzigingen </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> 24 oktober 2018 </td> 
   <td colname="col2"> <p> <a href="../r-release-notes/known-issues-resolved-issues.md#concept_625C3A16B7F24D4B82EFF130F0945541" format="dita" scope="local"> Bekende problemen en opgeloste problemen </a> </p> </td> 
   <td colname="col3"> <p>Bekend probleem met verwijderde activiteiten via API in de standaardwerkruimte die in de doelinterface blijft bestaan, is toegevoegd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p> <a href="../c-reports/c-report-settings/average-lift-bounds-and-confidence-interval.md#topic_AFFDC672A8A34D028B100EF6BE5D8129" format="dita" scope="local"> Gemiddelde optillen, Lift Bounds en het Interval van het Vertrouwen </a> </p> </td> 
   <td colname="col3"> <p>Er is een opmerking toegevoegd waarin wordt uitgelegd dat kleine verschillen tussen handmatige berekeningen met behulp van de vermelde formules en de in het rapport weergegeven cijfers te verwachten zijn. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 22 oktober 2018 </td> 
   <td colname="col2"> <p> <a href="../c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/cookie-behavior.md#concept_4D8107E193B64168A3C0B85B51612991" format="dita" scope="local"> Doelcookie </a> </p> </td> 
   <td colname="col3"> <p>Toegevoegde Belangrijke nota bij bovenkant van onderwerp adviserend cliënten om gevoelige informatie aan mboxSession en mboxPC niet te verbinden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 21 oktober 2018 </td> 
   <td colname="col2"> <p> <a href="../c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md#reference_DBB5EDB79EC44E558F9E08D4774A0F7A" format="dita" scope="local"> at.js - Versiedetails </a> </p> </td> 
   <td colname="col3"> <p>Toegevoegde informatie over at.js Versie 1.6.2. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p> <a href="../c-implementing-target/c-considerations-before-you-implement-target/c-privacy/cmp-privacy-and-general-data-protection-regulation.md#topic_6BCC0D0984184379A2A2EA6FFC948899" format="dita" scope="local"> Privacy en algemene gegevensbeschermingsverordening (GDPR) </a> </p> </td> 
   <td colname="col3"> <p>De sectie "Adobe Target and Adobe Launch Opt-In" is toegevoegd. </p> <p>De volgende veelgestelde vragen zijn bijgewerkt: </p> <p> 
     <ul id="ul_BBF57B0E30A541E1BD1BCADD21A3D0F7"> 
      <li id="li_020DE613F4F340D8B68186465883A60C"> <p>Hoe werkt Adobe Target met het beheer van toestemmingen? </p> </li> 
      <li id="li_515B157F27B04342BB5664FD8E258FE2"> <p>Welke id's worden ondersteund om klanten te helpen een aanvraag voor GDPR-toegang en -verwijdering voor Target te voltooien? </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p> <a href="../c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/cmp-implementing-target-using-adobe-launch.md#topic_5234DDAEB0834333BD6BA1B05892FC25" format="dita" scope="local"> Doel implementeren met Adobe Launch </a> </p> </td> 
   <td colname="col3"> <p>Bijgewerkte koppeling naar de Adobe Target-extensie. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 18 oktober 2018 </td> 
   <td colname="col2"> <p> <a href="../c-recommendations/c-recommendations-faq/ip-addresses-marketing-cloud.md#concept_216F959FF18143D6A3BA0BE937918580" format="dita" scope="local"> IP Adressen die door de servers van de Feed-Verwerking van Aanbevelingen worden gebruikt </a> </p> </td> 
   <td colname="col3"> <p>Bijgewerkte IP adreswaaier die door de activiteiten van de Aanbevelingen van het Doel wordt gebruikt. </p> <p>Toegevoegde IP adreswaaier die door de Aanbevelingen APIs van het Doel wordt gebruikt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 12 oktober 2018 </td> 
   <td colname="col2"> <p> <a href="../c-activities/c-activity-qa/activity-qa.md#concept_9329EF33DE7D41CA9815C8115DBC4E40" format="dita" scope="local"> Activiteit QA </a> </p> </td> 
   <td colname="col3"> <p>Bewerkte de volgende paragraaf onder <span class="wintitle"> Overwegingen</span>: </p> <p>Activiteits-QA geeft geen inhoud weer voor gearchiveerde activiteiten of activiteiten die hun einddatum hebben bereikt. Als u een beëindigde activiteit deactiveert, moet u de activiteit opnieuw bewaren voor Activiteit QA om te werken. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 10 oktober 2018 </td> 
   <td colname="col2"> <p> <a href="../target-home.md#topic_74F655D8648E4586BCCFD789E60D13CE" format="dita" scope="local"> Adobe Target-productdocumentatie </a> </p> </td> 
   <td colname="col3"> <p>De Adobe Target-productdocumentatie is bijgewerkt in de volgende talen: Duits, Spaans, Frans, Italiaans, Japans en Portugees (Brazilië). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 9 oktober 2019 </td> 
   <td colname="col2"> <p> <a href="../c-target/c-visitor-profile/profile-parameters.md#concept_01A30B4762D64CD5946B3AA38DC8A201" format="dita" scope="local"> Profielkenmerken </a> </p> </td> 
   <td colname="col3"> <p>Sectie Veelgestelde vragen over toegevoegde profielscripts. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p> <a href="../c-recommendations/c-recommendations-faq/ip-addresses-marketing-cloud.md#concept_216F959FF18143D6A3BA0BE937918580" format="dita" scope="local"> IP Adressen die door de servers van de Feed-Verwerking van Aanbevelingen worden gebruikt </a> </p> </td> 
   <td colname="col3"> <p>Bewerkte tekst om erop te wijzen dat de <span class="wintitle"> </span> activiteiten van Aanbevelingen IP adressen gebruiken die in het de gegevenscentrum van Oregon worden gevestigd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 8 oktober 2018 </td> 
   <td colname="col2"> <p> <a href="../c-recommendations/c-recommendations-faq/ip-addresses-marketing-cloud.md#concept_216F959FF18143D6A3BA0BE937918580" format="dita" scope="local"> IP Adressen die door de servers van de Feed-Verwerking van Aanbevelingen worden gebruikt </a> </p> </td> 
   <td colname="col3"> <p>Toegevoegde nieuwe IP adreswaaier voor CIDR Notation 192.243.242.0.0/24. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 5 oktober 2018 </td> 
   <td colname="col2"> <p> <a href="../c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-viewing-reports.md#concept_72A95F6466A04B409FCD5989A6B6A554" format="dita" scope="local"> Rapporten weergeven - Veelgestelde vragen A4T </a> </p> </td> 
   <td colname="col3"> <p>Gehele sectie herzien: "Moet ik bezoekers, activiteitenindrukken, of bezoeken gebruiken wanneer het bekijken van rapporten?" Omgezette metrische beschrijvingen en een lijst van overwegingen toegevoegd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 4 oktober 2018 </td> 
   <td colname="col2"> <p> <a href="../c-recommendations/c-algorithms/create-new-algorithm.md#task_8A9CB465F28D44899F69F38AD27352FE" format="dita" scope="local"> Criteria maken </a> </p> </td> 
   <td colname="col3"> <p>Sectie 'Verwachte verwerkingstijd criteria' toegevoegd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p> <a href="../c-activities/activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03" format="dita" scope="local"> Activiteiten </a> </p> </td> 
   <td colname="col3"> <p>Extra informatie over hoe te om Tip van de Dag onbruikbaar te maken. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 3 oktober 2018 </td> 
   <td colname="col2"> <p> <a href="https://spark.adobe.com/page/Lo3Spm4oBOvwF/" format="https" scope="external"> Analyse en doel: Beste praktijken voor Analyse </a> </p> </td> 
   <td colname="col3"> <p>Bekijk de nieuwe zelfstudie Analytics for Target (A4t). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p> <a href="../c-intro/how-target-works.md#concept_459AB4DEE7364A9290C2FD405DC29584" format="dita" scope="local"> Werken met Adobe Target </a> </p> </td> 
   <td colname="col3"> <p>Volledig onderwerp bijgewerkt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p> <a href="../c-activities/t-test-ab/t-test-create-ab/test-create-ab.md#task_68C8079BF9FF4625A3BD6680D554BB72" format="dita" scope="local"> Een A/B-test maken </a> </p> <p> <a href="../c-activities/t-automated-personalization/create-ap-activity.md#task_8AAF837796D74CF893CA2F88BA1491C9" format="dita" scope="local"> Een geautomatiseerde personalisatieactiviteit maken </a> </p> <p> <a href="../c-activities/t-experience-target/t-xt-create/xt-create.md#task_D6B3429AC31549E1A70EDF04B3DDC765" format="dita" scope="local"> Een ervaring maken die gericht is op activiteiten </a> </p> <p> <a href="../c-activities/c-multivariate-testing/t-create-multivariate-test/create-multivariate-test.md#task_BF870FA60A8245AB8F0B775BE32EA710" format="dita" scope="local"> Een multivariatietest maken </a> </p> <p> <a href="../c-recommendations/t-create-recs-activity/recs-activity-settings.md#reference_3FDA8388CEEC4159949151C1829E2FBB" format="dita" scope="local"> Instellingen voor activiteiten voor aanbevelingen </a> </p> <p> <a href="../c-activities/t-test-ab/t-test-create-ab/ab-add-experience.md#task_454646F2895242D3B92DC395A0CE1A00" format="dita" scope="local"> Ervaring toevoegen </a> </p> <p> <a href="../c-activities/t-test-ab/t-test-create-ab/ab-set-metrics.md#task_A04AB66007C1467DA1C21A519A5C7BEB" format="dita" scope="local"> Metrisch instellen </a> </p>
   </td> 
   <td colname="col3"> <p>De tabellijsttekens die niet zijn toegestaan in namen van activiteiten, ervaringen of metrische gegevens zijn bijgewerkt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 2 oktober 2018 </td> 
   <td colname="col2"> <p> <a href="../c-recommendations/c-products/collections.md#concept_671BEFFB997D4F1282665BF3CAC00AC5" format="dita" scope="local"> Verzamelingen </a> </p> </td> 
   <td colname="col3"> <p>Opmerking toegevoegd na stap 1. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p> <a href="../c-recommendations/c-products/exclusions.md#task_E79DA82BA402415FB41232976EDEF1CA" format="dita" scope="local"> Uitsluitingen </a> </p> </td> 
   <td colname="col3"> <p>Opmerking toegevoegd na stap 1. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 27 september 2018 </td> 
   <td colname="col2"> <p> <a href="../c-implementing-target/c-considerations-before-you-implement-target/c-methods-to-get-data-into-target/methods-to-get-data-into-target.md#concept_0069C0EFB56C4700BB33F2F35C2B9B17" format="dita" scope="local"> Methoden om gegevens op te halen in doel </a> </p> </td> 
   <td colname="col3"> <p>Toegevoegde informatie over toegestane karakters in vraagmontages. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p> <a href="../r-release-notes/known-issues-resolved-issues.md#concept_625C3A16B7F24D4B82EFF130F0945541" format="dita" scope="local"> Bekende problemen en opgeloste problemen </a> </p> </td> 
   <td colname="col3"> <p>Bekende kwestie betreffende aanbiedingsniveau rapportering in AP-activiteiten naar de lijst Opgeloste problemen verplaatst. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 26 september 2018 </td> 
   <td colname="col2"> <p> <a href="../c-experiences/c-visual-experience-composer/viztarget-options.md#reference_3BD1BEEAFA584A749ED2D08F14732E81" format="dita" scope="local"> Opties voor composer visuele ervaring </a> </p> </td> 
   <td colname="col3"> <p>Informatie toegevoegd over de <span class="wintitle"> </span> optie Invoegen voor. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <a href="../c-activities/t-automated-personalization/create-ap-activity.md#task_8AAF837796D74CF893CA2F88BA1491C9" format="dita" scope="local"> Een geautomatiseerde personalisatieactiviteit maken </a> </td> 
   <td colname="col3"> <p>Toegevoegde informatie over de lijst van de Groep van het Rapport die u aanbiedingen door rapportgroep laat filtreren. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p> <a href="../c-activities/t-automated-personalization/managing-exclusions.md#topic_30B4E4F89C914EB2B20B038C0299ED2E" format="dita" scope="local"> Uitsluitingen beheren </a> </p> </td> 
   <td colname="col3"> <p>Extra informatie over het gebruiken van veelvoudige aanbiedingen van de zelfde plaats in een uitsluitingsgroep. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p> <a href="../cmp-resources-and-contact-information.md#concept_11902FAC95C64479AABE020557A7EEE4" format="dita" scope="local"> Doelbasis van de webinarreeks </a> </p> </td> 
   <td colname="col3"> <p>Toegevoegde verbinding aan de Beste praktijken in de zitting van de Socialisatie van de Rapportering &amp; van de Waarde. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p> <a href="../c-recommendations/c-products/feeds.md#concept_1228B31E3D0B483B9DD42C5E2AE436E3" format="dita" scope="local"> Feeds </a> </p> </td> 
   <td colname="col3"> <p>Toegevoegd: </p> <p> <p>Belangrijk:  Geüploade feeds verlopen na 61 dagen. Dit betekent dat aanbevelingen niet meer worden teruggegeven als een voederbestand in de afgelopen 60 dagen niet is verwerkt. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p> <a href="../r-release-notes/known-issues-resolved-issues.md#concept_625C3A16B7F24D4B82EFF130F0945541" format="dita" scope="local"> Bekende problemen en opgeloste problemen </a> </p> </td> 
   <td colname="col3"> <p>Toegevoegde bekende kwestie met betrekking tot de rapportage op aanbodniveau in AP-activiteiten. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p> <a href="../c-recommendations/c-recommendations-faq/integrating-recs-email.md#reference_256B16C894864F24AF970E43DC174420" format="dita" scope="local"> Aanbevelingen integreren met e-mail </a> </p> </td> 
   <td colname="col3"> <p>Bijgewerkte notitie onder "Optie 1: Gebruik de leverings-API." </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p> <a href="../c-recommendations/recommendations.md#concept_7556C8A4543942F2A77B13A29339C0C0" format="dita" scope="local"> Aanbevelingen </a> </p> </td> 
   <td colname="col3"> <p>Herschikte onderwerpen in volledige sectie. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p>Release 18.9.1 <a href="../r-release-notes/release-notes.md#reference_8FE40B43A5A34DDF8F26A53D55EE036A" format="dita" scope="local"> Opmerkingen bij de release </a> </p> </td> 
   <td colname="col3"> <p>Deze release bevat verbeteringen en correcties. U kunt over hen lezen en met de documentatie van de Nota's van de Versie verbinden. Deze release bevat ook een groot aantal documentatie-updates voor de hele Help. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Adobe Target Standard/Premium 18.8.1 (21 augustus 2018) {#section_6A146EE91FFB49D1BA398B36817CD0A2}

<table id="table_F09AC99B587A4D6390B1F8AE54F5DC47"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Datum </th> 
   <th colname="col2" class="entry"> Onderwerp </th> 
   <th colname="col3" class="entry"> Wijzigingen </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> 21 september 2018 </td> 
   <td colname="col2"> <p> <a href="../c-implementing-target/c-implementing-target-for-client-side-web/c-target-debugging-atjs/target-debugging-atjs.md#concept_CAE591DA8C404C22917584ECD4F7494F" format="dita" scope="local"> Foutopsporing in.js met Adobe Experience Cloud Debugger </a> </p> </td> 
   <td colname="col3"> <p>Gewijzigd volledig onderwerp en toegevoegde trainingsvideo's. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 20 september 2018 </td> 
   <td colname="col2"> <p> <a href="../r-release-notes/release-notes.md#reference_8FE40B43A5A34DDF8F26A53D55EE036A" format="dita" scope="local"> Opmerkingen bij de doelversie </a> </p> <p> <a href="../c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md#reference_DBB5EDB79EC44E558F9E08D4774A0F7A" format="dita" scope="local"> at.js - Versiedetails </a> </p> </td> 
   <td colname="col3"> <p>Toegevoegde informatie over de release at.js 1.6.1. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 19 september 2018 </td> 
   <td colname="col2"> <p> <a href="../r-release-notes/known-issues-resolved-issues.md#concept_625C3A16B7F24D4B82EFF130F0945541" format="dita" scope="local"> Bekende problemen en opgeloste problemen </a> </p> </td> 
   <td colname="col3"> Probleem met betrekking tot de Code-editor is verplaatst van de tabel Bekende problemen naar de tabel Opgeloste problemen. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 18 september 2018 </td> 
   <td colname="col2"> <p> <a href="../c-experiences/c-visual-experience-composer/c-vec-code-editor/experience-templates.md#concept_109BBD7EABC04DD39E6B7B1687786652" format="dita" scope="local"> Experience Templates </a> </p> </td> 
   <td colname="col3"> <p>Nieuw onderwerp. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p> <a href="../cmp-resources-and-contact-information.md#concept_11902FAC95C64479AABE020557A7EEE4" format="dita" scope="local"> Doelbasis van de webinarreeks </a> </p> </td> 
   <td colname="col3"> <p>De volgende webinar datums zijn bijgewerkt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 11 september 2018 </td> 
   <td colname="col2"> <p> <a href="../c-activities/c-activity-qa/use-qa-mode-with-server-side-delivery.md#concept_54698C5CE8934F68B20961CD83FD6202" format="dita" scope="local"> Activiteit QA met levering op de server gebruiken </a> </p> </td> 
   <td colname="col3"> <p>Nieuw onderwerp. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p> <a href="../c-target/c-audiences/c-target-rules/custom-parameters.md#concept_C4C6E00D7C5A4BE9B72D471DB2E3027B" format="dita" scope="local"> Aangepaste parameters </a> </p> </td> 
   <td colname="col3"> <p>Toegevoegde informatie over het opnieuw opslaan van aangepaste soorten publiek die vóór de release 18.5.1 zijn gemaakt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p> <a href="../r-release-notes/known-issues-resolved-issues.md#concept_625C3A16B7F24D4B82EFF130F0945541" format="dita" scope="local"> Bekende problemen en opgeloste problemen </a> </p> </td> 
   <td colname="col3"> <p>Bekend probleem toegevoegd: Impressies en conversies van doelactiviteiten worden momenteel onjuist geteld in de analysewerkruimte. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p> <a href="../c-implementing-target/c-considerations-before-you-implement-target/c-privacy/cmp-privacy-and-general-data-protection-regulation.md#concept_41F88DE95D2943178BEC382736B5C038" format="dita" scope="local"> Algemene veelgestelde vragen over de verordening gegevensbescherming </a> </p> </td> 
   <td colname="col3"> <p>Bijgewerkt codevoorbeeld. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p> <a href="../c-recommendations/c-recommendations-faq/recommendations-faq.md#concept_EF272DE4AC6C47B19026BFBE816F5DB8" format="dita" scope="local"> Veelgestelde vragen over aanbevelingen </a> </p> </td> 
   <td colname="col3"> <p>Veranderde vereiste versie van de Snelheid in 1.7.0. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 10 september 2018 </td> 
   <td colname="col2"> <p> <a href="../r-release-notes/release-notes.md#reference_8FE40B43A5A34DDF8F26A53D55EE036A" format="dita" scope="local"> Opmerkingen bij de doelversie </a> </p> <p> <a href="../c-implementing-target/c-considerations-before-you-implement-target/tls-transport-layer-security-encryption.md#concept_CC1001E9D3AE4BABAF90B8311B0A6451" format="dita" scope="local"> Wijzigingen in TLS-codering (Transport Layer Security) </a> </p> </td> 
   <td colname="col3"> <p>De datum waarop Adobe de ondersteuning voor TLS 1.0 afbouwt, is gewijzigd van 12 september 2018 tot februari 2019. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p> <a href="../c-reports/reports.md#concept_B5077F5503AA4C98901AA99EDCE6CDE6" format="dita" scope="local"> Rapporten </a> </p> </td> 
   <td colname="col3"> <p>Toegevoegde informatie en link om A/B Tests te helpen plannen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p> <a href="../c-recommendations/c-recommendations-faq/recommendations-faq.md#concept_EF272DE4AC6C47B19026BFBE816F5DB8" format="dita" scope="local"> Veelgestelde vragen over aanbevelingen </a> </p> </td> 
   <td colname="col3"> <p>Volgende veelgestelde vragen toegevoegd: Wat is de maximumgrootte van een CSV-bestand voor een feed-upload? </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p> <a href="../c-target/c-audiences/c-target-rules/visitor-profile.md#concept_E972690B9A4C4372A34229FA37EDA38E" format="dita" scope="local"> Bezoekerprofiel </a> </p> </td> 
   <td colname="col3"> <p>Toegevoegd na alinea: </p> <p>Er wordt een bezoekersprofiel gemaakt in het lokale Edge-geheugen voor elke mbox-aanroep met nieuwe <span class="codeph"> mboxPC </span>. Na 30 minuten inactiviteit, wordt het profiel bewaard aan het gegevensbestand van het Doel en is toegankelijk van andere randen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p> <a href="../c-activities/t-test-ab/t-test-create-ab/ab-activity-url.md#concept_D28549AAA0A14E3BB5F05F32BE8ABC90" format="dita" scope="local"> URL van activiteit </a> </p> </td> 
   <td colname="col3"> <p>Gewijzigde tekst en bijgewerkte illustratie. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 7 september 2018 </td> 
   <td colname="col2"> <p> <a href="../c-recommendations/c-recommendations-faq/recommendations-faq.md#concept_EF272DE4AC6C47B19026BFBE816F5DB8" format="dita" scope="local"> Veelgestelde vragen over aanbevelingen </a> </p> </td> 
   <td colname="col3"> <p>Nieuwe veelgestelde vragen toegevoegd: Waarom kan ik mijn activiteit van de Aanbevelingen van de erfenis niet bewaren na het bepalen van een nieuw publiek? </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 4 september 2018 </td> 
   <td colname="col2"> <p> <a href="../c-implementing-target/c-implementing-target-for-client-side-web/cmp-atjs-functions.md#section_42725F3C837247D58AE1831EA330E44D" format="dita" scope="local"> Gegevensleveranciers </a> </p> </td> 
   <td colname="col3"> <p>Bijgewerkt codevoorbeeld. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p> <a href="../c-implementing-target/c-considerations-before-you-implement-target/c-privacy/cmp-privacy-and-general-data-protection-regulation.md#concept_41F88DE95D2943178BEC382736B5C038" format="dita" scope="local"> Algemene veelgestelde vragen over de verordening gegevensbescherming </a> </p> </td> 
   <td colname="col3"> <p>Kleine bewerkingen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 30 augustus 2018 </td> 
   <td colname="col2"> <p> <a href="../r-release-notes/known-issues-resolved-issues.md#concept_625C3A16B7F24D4B82EFF130F0945541" format="dita" scope="local"> Bekende problemen en opgeloste problemen </a> </p> </td> 
   <td colname="col3"> Toegevoegd na bekende uitgave: <p> 
     <ul id="ul_7AF527E5989D468BBC9472EA1C7F376D"> 
      <li id="li_7F53C6F01E1E471FB546AF98F1FF7F1E"> <p>Wanneer u <span class="codeph"> versie 1.6.0 van </span> at.js gebruikt, vindt een omleiding van Analytics for Target (A4T) plaats, maar zonder activiteitkwalificatie. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 28 augustus 2018 </td> 
   <td colname="col2"> <p> <a href="../c-recommendations/c-products/entity-attributes.md#reference_3BCC1383FB3F44F4A2120BB36270387F" format="dita" scope="local"> Entiteitskenmerken </a> </p> </td> 
   <td colname="col3"> <p>De rij van de entiteit-id is bijgewerkt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p> <a href="../c-recommendations/c-algorithms/create-new-algorithm.md#concept_BC16005C7A1E4F1A87E33D16221F4A96" format="dita" scope="local"> Inhoudsinstellingen </a> </p> </td> 
   <td colname="col3"> <p>Verduidelijkt informatie over de <span class="wintitle"> optie Eerder aangeschafte objecten </span> aanbevelen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 21 augustus 2018 </td> 
   <td colname="col2"> <p> <a href="../c-reports/c-personalization-insights-reports/personalization-insights-reports.md#concept_A897070E1EDC403EB84CFB7A6ECAD767" format="dita" scope="local"> Persoonlijkheidsrapporten </a> </p> </td> 
   <td colname="col3"> <p>Nieuw onderwerp. </p> <p> <p>Opmerking:  Deze functie is binnenkort beschikbaar. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p> <a href="../c-experiences/c-visual-experience-composer/c-vec-code-editor/vec-code-editor.md#concept_B3A6E9EE3A60406DB640E205EA1745B5" format="dita" scope="local"> Wijzigingen </a> </p> </td> 
   <td colname="col3"> <p>Informatie toegevoegd over het koppelen van het deelvenster Wijzigingen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p> <a href="../c-experiences/c-visual-experience-composer/viztarget-options.md#reference_3BD1BEEAFA584A749ED2D08F14732E81" format="dita" scope="local"> Opties voor composer visuele ervaring </a> </p> </td> 
   <td colname="col3"> <p>Nieuwe indeling van tabel voor nieuwe groepen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p> <a href="../cmp-resources-and-contact-information.md#concept_11902FAC95C64479AABE020557A7EEE4" format="dita" scope="local"> Doelbasis van de webinarreeks </a> </p> </td> 
   <td colname="col3"> <p> 
     <ul id="ul_D5E4E05DFE7A4E45BF199395D7AC3CE1"> 
      <li id="li_7A4A621EC5C34E4AADD46AA294620D9C"> <p>Extra informatie over komende webinars. </p> </li> 
      <li id="li_A77B214010EF45BEBD0E2CBB256AD67D"> <p>Toegevoegde koppeling naar de opname voor het tweede webinar: Stappen om automatisering en meer geavanceerde activiteiten toe te voegen. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p> <a href="../c-activities/activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03" format="dita" scope="local"> Activiteiten </a> </p> </td> 
   <td colname="col3"> <p>De sectie Tips en trucs is toegevoegd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p> <a href="../r-release-notes/known-issues-resolved-issues.md#concept_625C3A16B7F24D4B82EFF130F0945541" format="dita" scope="local"> Bekende problemen en opgeloste problemen </a> </p> </td> 
   <td colname="col3"> <p>Het herhaalde probleem met omleidingsactiviteiten in <span class="codeph"> at.js- </span> implementaties kan ertoe leiden dat de voorbeeld-URL een lus binnengaat. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p> <a href="../c-implementing-target/c-considerations-before-you-implement-target/tls-transport-layer-security-encryption.md#concept_CC1001E9D3AE4BABAF90B8311B0A6451" format="dita" scope="local"> Wijzigingen in TLS-codering (Transport Layer Security) </a> </p> </td> 
   <td colname="col3"> <p>De eerder voorgestelde datum waarop de TLS 1.0-ondersteuning zou worden afgeschaft, is geschrapt (12 september 2018). </p> <p>De datum waarop de TLS 1.0-ondersteuning wordt verwijderd, wordt later bekendgemaakt; Het is echter belangrijk dat u de details doorloopt en de wijzigingen voor een vloeiende overgang indeelt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p>Release 18.8.1 <a href="../r-release-notes/release-notes.md#reference_8FE40B43A5A34DDF8F26A53D55EE036A" format="dita" scope="local"> Opmerkingen bij de release </a> </p> </td> 
   <td colname="col3"> <p>Deze release bevat verbeteringen en correcties. U kunt over hen lezen en met de documentatie van de Nota's van de Versie verbinden. Deze release bevat ook een groot aantal documentatie-updates voor de hele Help. </p> </td> 
  </tr> 
 </tbody> 
</table>

