---
keywords: variables;profiles;parameters;built in profiles;methods;url variables;geo profiles;third party profiles;mbox variables;campaign variables;customer attributes
description: Deze pagina bevat profielen, variabelen en parameters die nuttig zijn in profielscripts.
title: Profiel en verklarende woordenlijst voor variabelen
feature: visitor profiles
translation-type: tm+mt
source-git-commit: 968d36d65016e51290f6bf754f69c91fd8f68405
workflow-type: tm+mt
source-wordcount: '562'
ht-degree: 0%

---


# Profiel en variabele woordenlijst{#profile-and-variable-glossary}

Deze pagina bevat profielen, variabelen en parameters die nuttig zijn in profielscripts.

## Ingebouwde profielen {#section_2B694370003C4F8E8E29E0B2F6E52045}

| Profiel | Notities |
|--- |--- |
| user.activeActivities<br>user.activeCampaigns | Retourneer de campagne-id voor alle campagnes/activiteiten waarin de gebruiker zich bevindt, zelfs als hij of zij in de huidige sessie niet heeft gereageerd op de campagne/activiteit. |
| user.pcId |  |
| user.sessionId |  |
| user.categoryAffinity |  |
| user.categoryAffinities | Hiermee wordt een array geretourneerd van de affiniteiten die een bezoeker heeft gevuld |
| user.isFirstSession |  |
| user.isNewSession |  |
| user.daysSinceLastVisit |  |
| user.browser | De gebruikersagent |
| user.header | Alle `user.header` profielen zijn ingebouwd van de koptekstgegevens van de mbox-aanvraag |
| user.header(&#39;x-door:sturen-for&#39;) | Het openbaar-onder ogen ziet IP adres van de netwerkverbinding die de bezoeker is.<br>U kunt dit op verschillende manieren krijgen, bijvoorbeeld  [whatismyip.com](https://www.whatismyip.com/). Het IP adres is niet het NATIONAAL adres (intern adres), beginnend met 10., 192.168., of 172.<br>Opmerking: user.header(&#39;x-cluster-client-ip&#39;) is afgekeurd. |
| user.header(&#39;host&#39;) | Hostnaam website |
| user.header(&#39;cookie&#39;) | Cookgegevens van bezoekers |
| user.header(&#39;user-agent&#39;) | Gebruikersagent browser van bezoeker |
| user.header(&#39;accept-language&#39;) | Taal van bezoeker |
| user.header(&#39;accept-encoding&#39;) | Tekencodering bezoeker |
| user.header(&#39;accept&#39;) | Taal en tekencodering van bezoekers |
| user.header(&#39;connection&#39;) | Serververbinding. Bijvoorbeeld:  live houden |
| user.header(&#39;reference&#39;) | URL van website van huidige pagina van bezoeker. Werkt niet voor Internet Explorer. |
| user.getLocal(&#39;param_name&#39;,&#39;value&#39;); |  |
| user.setLocal(&#39;param_name&#39;,&#39;value&#39;); |  |
| user.get(&#39;param_name&#39;) |  |
| user.parameter | Profielkenmerken voor continue verbindingen die zijn gemaakt op basis van profielscripts. Verwijst ook naar &#39;systeem&#39;-profielen zoals geolocatie, aantal bezoeken, enz. |
| profile.get(&#39;param_name&#39;) | De juiste manier om een profielparameter te verkrijgen om in een profielmanuscript te gebruiken is profiel.get (&#39;param_name&#39;) methode. |
| profile.param(&#39;param_name&#39;); |  |
| profile.parameter(&#39;parameter_name&#39;); | Mbox-parameters die blijvend worden gemaakt vanwege hun profiel.  voorvoegsel. |
| profile.browserTime | De lokale browsertijd van de bezoeker. Maak voor de systeemtijd een nieuw datumobject in het profielscript |
| profile.averageDaysBetweenVisits |  |
| profile.sessionCount |  |
| parameter= | Algemene term voor extra waarden die met een box worden doorgegeven, meestal als naam-/waardeparen. Niet blijvend tenzij gemaakt met `profile.parameter` of `user.parameter`. |

## URL-variabelen {#section_8F25958273164EBAA6DC659302993FD3}

| `landing` | `referrer` | `page` |
|---|---|---|
| `landing.url` | `referrer.url` | `page.url` |
| `landing.domain` | `referrer.domain` | `page.domain` |
| `landing.protocol` | `referrer.protocol` | `page.protocol` |
| `landing.param` | `referrer.param` | `page.param` |
| `landing.query` | `referrer.query` | `page.query` |

## Profielen van geo- en mobiele transporteurs {#section_08441DA42E7346918FBB345818854997}

* `profile.geolocation.country`
* `profile.geolocation.state`
* `profile.geolocation.city`
* `profile.geolocation.zip`
* `profile.geolocation.dma`
* `profile.geolocation.domainName`
* `profile.geolocation.ispName`
* `profile.geolocation.connectionSpeed`
* `profile.geolocation.mobileCarrier`
* `profile.geolocation.latitude`
* `profile.geolocation.longitude`

## Mbox-variabelen {#section_C42F0D33BD8044BE812FA0B7905CC0ED}

| Variabele | Notities |
|--- |--- |
| `mbox.name` |  |
| mbox.param(&#39;param_name&#39;) |  |
| Parameters die automatisch bij elk verzoek worden doorgegeven:<ul><li>mbox.param(&#39;browserHeight&#39;)</li><li>mbox.param(&#39;browserTimeOffset&#39;)</li><li>mbox.param(&#39;browserWidth&#39;)</li><li>mbox.param(&#39;colorDepth&#39;)</li><li>mbox.param(&#39;mboxXDomain&#39;)</li><li>mbox.param(&#39;mboxTime&#39;)</li><li>mbox.param(&#39;screenHeight&#39;)</li><li>mbox.param(&#39;screenWidth&#39;)</li></ul> |
| Parameters die met volgvakjes worden doorgegeven:<ul><li>mbox.param(&#39;orderId&#39;)</li><li>mbox.param(&#39;orderTotal&#39;)</li><li>mbox.param(&#39;productPurchasedId&#39;)</li></ul> |
| mbox3rdPartyId | Een mbox-parameter om een klant-id te synchroniseren met de mboxPCID van Target. Een klant-id is een id die uw bedrijf gebruikt om bezoekers bij te houden, zoals een CRM-id, lidmaatschap-id of iets dergelijks. Deze id kan vervolgens worden gebruikt om informatie toe te voegen via de profiel-API&#39;s en [Klantkenmerken](/help/c-target/c-visitor-profile/working-with-customer-attributes.md). |
| mboxPageValue | In elke mbox-aanroep wordt een waarde toegewezen aan de pagina. |
| mboxDebug | Wordt alleen gebruikt voor foutopsporingsinformatie. Toegevoegd aan de pagina-URL waar mbox.js ernaar zoekt. |
| mboxOverride.browserIp | Hiermee stelt u een andere geo in dan de werkelijke locatie, zodat u kunt testen hoe iets er op een andere locatie uitziet.<br>**Opmerking:** Het gebruik van mboxOverride-parameters mag alleen worden gebruikt tijdens het testen van de activiteit en niet tijdens de productie. Het gebruik van willekeurige mboxOverride-parameters kan bij gebruik van [Analytics voor Target](/help/c-integrating-target-with-mac/a4t/a4t.md) (A4T) tot discrepanties bij rapportage leiden. U zou [De wijze van QA van de Activiteit](/help/c-activities/c-activity-qa/activity-qa.md) moeten gebruiken terwijl het testen om ervoor te zorgen dat uw activiteit zoals verwacht werkt alvorens de activiteit in uw levende milieu te duwen. |

## Klantkenmerken {#section_62B4821EB6564FF4A14159A837AD4EDB}

In profielscripts, opgemaakt als `crs.get('<Datasource Name>.<Attribute name>')`, kan naar de kenmerken van de klant worden verwezen.

Deze kenmerken zijn ook beschikbaar als tokens in profielscripts en rechtstreeks in aanbiedingen zonder eerst een profielscript te hoeven schrijven. De token moet de volgende vorm hebben: `${crs.datasourceName.attributeName}`. Merk op dat de ruimten in `datasourceName` van om het even welke API vraag zouden moeten worden gestript.
