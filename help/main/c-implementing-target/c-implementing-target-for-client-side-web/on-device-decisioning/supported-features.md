---
keywords: implementatie;javascript-bibliotheek;js;atjs;apparaatbeslissingen;apparaatbeslissingen;ondersteunde functies
description: Leer welke functies worden ondersteund voor beslissingen op het apparaat.
title: Welke functies worden ondersteund in een beslissing op het apparaat
feature: at.js
role: Developer
exl-id: 3531ff55-c3db-44c1-8d0a-d7ec2ccb6505
source-git-commit: 719eb95049dad3bee5925dff794871cd65969f79
workflow-type: tm+mt
source-wordcount: '480'
ht-degree: 0%

---

# Ondersteunde functies voor apparaatbesluitvorming

De [!DNL Adobe Target] JS SDK biedt klanten de flexibiliteit om te kiezen tussen prestaties en versheid van gegevens voor beslissingen. Met andere woorden, als het voor u van het grootste belang is om de meest relevante en engaging van gepersonaliseerde inhoud via computerleren te leveren, moet er een live serveroproep worden gedaan. Maar als de prestaties kritischer zijn, moet een on-device en in-memory beslissing worden genomen. Raadpleeg de volgende secties waarin de functies worden vermeld die worden ondersteund, zodat de beslissing op het apparaat werkt.

## Ondersteunde activiteitstypen

De volgende tabel geeft aan welke [activiteitstypen](/help/main/c-activities/target-activities-guide.md) door de [Form-based Experience Composer](/help/main/c-experiences/form-experience-composer.md) of [Visual Experience Composer](/help/main/c-experiences/c-visual-experience-composer/visual-experience-composer.md) (VEC) worden ondersteund of niet ondersteund voor beslissingen op het apparaat.

| Type activiteit | Ondersteund? |
| --- | --- |
| [A/B-test](/help/main/c-activities/t-test-ab/test-ab.md) | Ja |
| [Automatisch toewijzen](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md) | Nee |
| [Automatisch doel](/help/main/c-activities/auto-target/auto-target-to-optimize.md) ![Premium](/help/main/assets/premium.png) | Nee |
| [Multivariatietest](/help/main/c-activities/c-multivariate-testing/multivariate-testing.md) (MVT) | Nee |
| [Gericht op ervaring](/help/main/c-activities/t-experience-target/experience-target.md) (XT) | Ja |
| [Automated Personalization](/help/main/c-activities/t-automated-personalization/automated-personalization.md) ![Premium](/help/main/assets/premium.png) | Nee |
| [Recommendations](/help/main/c-recommendations/recommendations.md) ![Premium](/help/main/assets/premium.png) | Nee |
| [Activiteiten die gebruikmaken van Analyses voor Doel](/help/main/c-integrating-target-with-mac/a4t/a4t.md) (A4T) | Ja |

## Doelgerichtheid publiek

In de volgende tabel wordt aangegeven welke publieksregels worden ondersteund voor apparaatbeslissingen.

| Auditieregel | Ondersteund? |
| --- | --- |
| [Geo](/help/main/c-target/c-audiences/c-target-rules/geo.md) | Ja |
| [Netwerk](/help/main/c-target/c-audiences/c-target-rules/network.md) | Nee |
| [Mobiel](/help/main/c-target/c-audiences/c-target-rules/mobile.md) | Nee |
| [Aangepaste parameters](/help/main/c-target/c-audiences/c-target-rules/custom-parameters.md) | Ja |
| [Besturingssysteem](/help/main/c-target/c-audiences/c-target-rules/operating-system.md) | Ja |
| [Sitepagina&#39;s](/help/main/c-target/c-audiences/c-target-rules/site-pages.md) | Ja |
| [Browser](/help/main/c-target/c-audiences/c-target-rules/browser.md) | Ja |
| [Bezoekerprofiel](/help/main/c-target/c-audiences/c-target-rules/visitor-profile.md) | Nee |
| [Verkeersbronnen](/help/main/c-target/c-audiences/c-target-rules/traffic-sources.md) | Nee |
| [Tijdschema](/help/main/c-target/c-audiences/c-target-rules/time-frame.md) | Ja |
| Adobe Experience Cloud-publiek<br>(Soorten publiek uit [!DNL Adobe Analytics], [!DNL Adobe Audience Manager], en [!DNL Adobe Experience Manager] | Nee |

### Geo targeting voor apparaatbesluitvorming

Om minimale latentie voor op apparaat beslissingsactiviteiten met geo-gebaseerd publiek te handhaven, adviseert Adobe u de geo waarden zelf in de vraag te verstrekken aan [getOffers](https://developer.adobe.com/target/implement/client-side/atjs/atjs-functions/adobe-target-getoffers-atjs-2/){target=_blank}. Stel het Geo-object in in de context van de aanvraag. Dit betekent vanuit de browser een manier om de locatie van elke bezoeker te bepalen. Bijvoorbeeld, kunt u een IP-aan-Geo raadpleging uitvoeren, gebruikend de dienst u vormt. Sommige hostingproviders, zoals Google Cloud, bieden deze functionaliteit via aangepaste headers in elk `HttpServletRequest`.

```javascript
window.adobe.target.getOffers({ 
	decisioningMethod: "on-device", 
	request: { 
		context: { 
			geo: { 
				city: "SAN FRANCISCO", 
				countryCode: "US", 
				stateCode: "CA", 
				latitude: 37.75, 
				longitude: -122.4 
			} 
		}, 
		execute: { 
			pageLoad: {} 
		} 
	} 
})
```

Nochtans, als u geen IP-aan-Geo raadplegingen op uw server kunt uitvoeren, maar u nog wilt op-apparatenbesluit voor uitvoeren [getOffers](https://developer.adobe.com/target/implement/client-side/atjs/atjs-functions/adobe-target-getoffers-atjs-2/){target=_blank} -aanvragen die op geo gebaseerde soorten publiek bevatten, wordt dit ook ondersteund. Het nadeel van deze benadering is dat het een verre IP-aan-Geo raadpleging gebruikt, die latentie aan elk toevoegt `getOffers` vraag. Deze latentie moet lager zijn dan een `getOffers` vraag met server-zijbesluit, omdat het een CDN raakt die dicht bij uw server wordt gevestigd. Geef alleen het veld &quot;ipAddress&quot; in het Geo-object op in de context van uw verzoek aan de SDK om de geolocatie van het IP-adres van uw bezoeker op te halen. Als een ander gebied naast &quot;ipAddress&quot;wordt verstrekt, [!DNL Target] SDK haalt de metagegevens voor de geolocatie niet op voor oplossing.

```javascript
window.adobe.target.getOffers({ 
	decisioningMethod: "on-device", 
	request: { 
		context: { 
			geo: { 
				ipAddress: "127.0.0.1" 
			} 
		}, 
		execute: { 
			pageLoad: {} 
		} 
	} 
})
```

### Toewijzingsmethode

In de volgende tabel wordt aangegeven welke toewijzingsmethoden worden ondersteund voor apparaatbeslissingen.

| Toewijzingsmethode | Ondersteund? |
| --- | --- |
| Handmatig | Ja |
| [Automatisch toewijzen aan de beste ervaring](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md) | Nee |
| [Automatisch richten voor persoonlijke ervaringen](/help/main/c-activities/auto-target/auto-target-to-optimize.md) | Nee |
