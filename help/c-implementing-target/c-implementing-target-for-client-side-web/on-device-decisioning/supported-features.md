---
keywords: implementatie;javascript-bibliotheek;js;atjs;apparaatbeslissingen;apparaatbeslissingen;ondersteunde functies
description: Leer welke functies worden ondersteund voor beslissingen op het apparaat.
title: Welke functies worden ondersteund in een beslissing op het apparaat
feature: at.js
role: Developer
translation-type: tm+mt
source-git-commit: 5fcc5776e69222e0a232bd92ddfd10cee748e577
workflow-type: tm+mt
source-wordcount: '467'
ht-degree: 0%

---

# Ondersteunde functies voor apparaatbesluitvorming

De [!DNL Adobe Target] JS SDK biedt klanten de flexibiliteit om te kiezen tussen prestaties en versheid van gegevens voor beslissingen. Met andere woorden, als het voor u van het grootste belang is om de meest relevante en engaging van gepersonaliseerde inhoud via computerleren te leveren, moet er een live serveroproep worden gedaan. Maar als de prestaties kritischer zijn, moet een on-device en in-memory beslissing worden genomen. Raadpleeg de volgende secties waarin de functies worden vermeld die worden ondersteund, zodat de beslissing op het apparaat werkt.

## Ondersteunde activiteitstypen

In de volgende tabel wordt aangegeven welke [activiteitstypen](/help/c-activities/target-activities-guide.md) die zijn gemaakt door de [Form-based Experience Composer](/help/c-experiences/form-experience-composer.md) of [Visual Experience Composer](/help/c-experiences/c-visual-experience-composer/visual-experience-composer.md) (VEC) worden ondersteund of niet voor beslissingen op het apparaat.

| Type activiteit | Ondersteund? |
| --- | --- |
| [A/B-test](/help/c-activities/t-test-ab/test-ab.md) | Ja |
| [Automatisch toewijzen](/help/c-activities/automated-traffic-allocation/automated-traffic-allocation.md) | Nee |
| [Auto-](/help/c-activities/auto-target/auto-target-to-optimize.md) ![TargetPremium](/help/assets/premium.png) | Nee |
| [Multivariatietest](/help/c-activities/c-multivariate-testing/multivariate-testing.md)  (MVT) | Nee |
| [Gericht op](/help/c-activities/t-experience-target/experience-target.md)  ervaring (XT) | Ja |
| [Automated ](/help/c-activities/t-automated-personalization/automated-personalization.md) ![Personalization Premium](/help/assets/premium.png) | Nee |
| [](/help/c-recommendations/recommendations.md) ![RecommendationsPremium](/help/assets/premium.png) | Nee |
| [Activiteiten die gebruikmaken van Analytics voor Target](/help/c-integrating-target-with-mac/a4t/a4t.md)  (A4T) | Ja |

## Doelgerichtheid publiek

In de volgende tabel wordt aangegeven welke publieksregels worden ondersteund voor apparaatbeslissingen.

| Auditieregel | Ondersteund? |
| --- | --- |
| [Geo](/help/c-target/c-audiences/c-target-rules/geo.md) | Ja |
| [Netwerk](/help/c-target/c-audiences/c-target-rules/network.md) | Nee |
| [Mobiel](/help/c-target/c-audiences/c-target-rules/mobile.md) | Nee |
| [Aangepaste parameters](/help/c-target/c-audiences/c-target-rules/custom-parameters.md) | Ja |
| [Besturingssysteem](/help/c-target/c-audiences/c-target-rules/operating-system.md) | Ja |
| [Sitepagina&#39;s](/help/c-target/c-audiences/c-target-rules/site-pages.md) | Ja |
| [Browser](/help/c-target/c-audiences/c-target-rules/browser.md) | Ja |
| [Bezoekerprofiel](/help/c-target/c-audiences/c-target-rules/visitor-profile.md) | Nee |
| [Verkeersbronnen](/help/c-target/c-audiences/c-target-rules/traffic-sources.md) | Nee |
| [Tijdschema](/help/c-target/c-audiences/c-target-rules/time-frame.md) | Ja |
| Adobe Experience Cloud Publiek<br>(Publiek van [!DNL Adobe Analytics], [!DNL Adobe Audience Manager] en [!DNL Adobe Experience Manager] | Nee |

### Geo targeting voor apparaatbesluitvorming

Om minimale latentie voor op apparaat beslissingsactiviteiten met geo-gebaseerd publiek te handhaven, adviseert Adobe u de geo waarden in de vraag aan [getOffers](/help/c-implementing-target/c-implementing-target-for-client-side-web/adobe-target-getoffers-atjs-2.md) te verstrekken. Stel het Geo-object in in de context van de aanvraag. Dit betekent vanuit de browser een manier om de locatie van elke bezoeker te bepalen. Bijvoorbeeld, kunt u een IP-aan-Geo raadpleging uitvoeren, gebruikend de dienst u vormt. Sommige hostingproviders, zoals Google Cloud, bieden deze functionaliteit via aangepaste koppen in elke `HttpServletRequest`.

(Te ontvangen code)

Nochtans, als u geen IP-aan-Geo raadplegingen op uw server kunt uitvoeren, maar u nog op-apparatenbesluit voor [getOffers](/help/c-implementing-target/c-implementing-target-for-client-side-web/adobe-target-getoffers-atjs-2.md) verzoeken wilt uitvoeren die geo-based publiek bevatten, wordt dit ook gesteund. Het nadeel van deze benadering is dat het een verre IP-aan-Geo raadpleging gebruikt, die latentie aan elke `getOffers` vraag toevoegt. Deze latentie zou lager moeten zijn dan een `getOffers` vraag met server-zijbesluit, omdat het een CDN raakt die dicht bij uw server wordt gevestigd. Geef alleen het veld &quot;ipAddress&quot; in het Geo-object op in de context van uw verzoek aan de SDK om de geolocatie van het IP-adres van uw bezoeker op te halen. Als er een ander veld wordt opgegeven naast &quot;ipAddress&quot;, haalt de SDK [!DNL Target] de metagegevens voor de geolocatie niet op voor oplossing.

(Te ontvangen code)

### Toewijzingsmethode

In de volgende tabel wordt aangegeven welke toewijzingsmethoden worden ondersteund voor apparaatbeslissingen.

| Toewijzingsmethode | Ondersteund? |
| --- | --- |
| Handmatig | Ja |
| [Automatisch toewijzen aan de beste ervaring](/help/c-activities/automated-traffic-allocation/automated-traffic-allocation.md) | Nee |
| [Automatisch richten voor persoonlijke ervaringen](/help/c-activities/auto-target/auto-target-to-optimize.md) | Nee |
