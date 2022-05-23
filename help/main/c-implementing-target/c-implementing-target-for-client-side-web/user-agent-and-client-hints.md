---
keywords: at.js;browser gebruikersagent;gebruikersagent;cliëntwenken;gebruiker-agent
description: Meer informatie [!DNL Adobe Target] gebruikt de gebruiker-agent en de Hints van de Cliënt om bezoekers voor segmentatie en verpersoonlijking te kwalificeren.
title: Gebruikersagent en clienttips
feature: at.js
role: Developer
source-git-commit: 2527608fc781913024d5d6ffee49aff9eb6c2f42
workflow-type: tm+mt
source-wordcount: '1303'
ht-degree: 0%

---

# Gebruiker-agent en de wenken van de Cliënt

[!DNL Adobe Target] gebruikt de gebruiker-agent om bezoekers voor segmentatie en verpersoonlijking te kwalificeren.

Elke keer dat een webbrowser een aanvraag naar een server indient, wordt in de header van de aanvraag informatie opgenomen over de browser en de omgeving waarin de browser wordt uitgevoerd. Sinds de vroege dagen van Internet, zijn deze gegevens bijeengevoegd in één enkel koord genoemd user-agent.

De volgende tekst is een voorbeeld van een gebruiker-agent van een op Mac OS X-Gebaseerde computer gebruikend Browser Safari:

```
Mozilla/5.0 (Linux; Android 12; SM-S908E) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/101.0.4951.41 Mobile Safari/537.36 
```

Van deze user-agent, kan de server die het verzoek ontvangt de volgende informatie over browser en werkend systeem ontdekken:

| Informatie | Details |
| --- | --- |
| Naam software | Chroom |
| Softwareversie | 101 |
| Volledige softwareversie | 101.0.4951.41 |
| Naam van lay-outengine | AppleWebKit |
| Versie van lay-outengine | 537,36 |
| Besturingssysteem | Android |
| Versie besturingssysteem | Android 12 (sneeuwkloon) |
| Apparaat | SM-S908E (Samsung Galaxy S22 Ultra) |

In de loop der jaren is de hoeveelheid browser- en apparaatinformatie in de user-agent-tekenreeks toegenomen.

## Gebruiksgevallen van gebruikersagenten

De gebruiker-agenten zijn lang gebruikt om marketing en ontwikkelaarteams van belangrijke inzichten in te voorzien hoe browsers, werkende systemen. en apparaten geven site-inhoud weer en hoe gebruikers met websites werken. De gebruiker-agenten worden ook gebruikt om spam en filterbots te blokkeren die plaatsen voor een verscheidenheid van extra doeleinden kruipen.

In de afgelopen jaren hebben sommige eigenaars van sites en marketingverkopers de gebruikersagent echter samen met andere informatie in aanvraagheaders gebruikt om digitale vingerafdrukken te maken die kunnen worden gebruikt om gebruikers zonder hun medeweten te identificeren. Ondanks het belangrijke doel dat de gebruiker-agent voor plaatseigenaren dient, hebben de browser ontwikkelaars besloten om veranderingen in te brengen hoe user-agents werken om potentiële privacykwesties voor plaatsbezoekers te beperken.

De gebruiker-Agent wenken van de Cliënt is de oplossingsbrowser ontwikkelaars hebben ontwikkeld. Met behulp van Client Hints kunnen sites nog steeds de benodigde browser-, besturingssysteem- en apparaatinformatie verzamelen en tegelijkertijd een betere bescherming bieden tegen methoden voor het bijhouden van gegevens, zoals vingerafdrukken.

## Clienttips

De gebruikers-Agent wenken van de Cliënt verstrekken websiteeigenaars de capaciteit om tot veel van de zelfde informatie toegang te hebben beschikbaar in gebruiker-agent, maar op een meer privacy-bewarende manier. Wanneer moderne browsers een user-agent naar een Webserver verzenden, wordt de volledige user-agent verzonden op elk verzoek, ongeacht of het wordt vereist. Clienttips daarentegen dwingen een model in waarin de server de browser om aanvullende informatie over de client moet vragen. Op het ontvangen van dit verzoek, kan browser zijn eigen beleid of gebruiker-configuratie toepassen om te bepalen welke gegevens zijn teruggekeerd. In plaats van de volledige gebruiker-agent door gebrek op alle verzoeken bloot te stellen, wordt de toegang nu geleid op een expliciete en controleerbare manier.

Client Hints voor gebruikersagent zijn sinds versie 89 beschikbaar in Chrome. Recente versies van Chromium-gebaseerde browsers, zoals Microsoft Edge, Opera, Brave, Chrome Android, Opera Android en Samsung Internet, ondersteunen ook de client Hints-API.

De wenken van de cliënt in de kopballen van het eerste verzoek dat door browser aan een Webserver wordt gemaakt bevatten het browser merk, de belangrijkste versie van browser, en een indicator van of de cliënt een mobiel apparaat is. Elk stuk gegevens heeft zijn eigen kopbalwaarde, eerder dan wordt gegroepeerd in één enkel user-agent koord, zoals aangetoond in de volgende steekproef:

```
Sec-CH-UA: "Chromium";v="101", "Google Chrome";v="101", " Not;A Brand";v="99" 
Sec-CH-UA-Mobile: ?0 
Sec-CH-UA-Platform: "macOS"
```

Het volgende voorbeeld is de user-agent voor dezelfde browser:

```
Mozilla/5.0 (Macintosh; Intel Mac OS X 10_15_7) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/101.0.4951.54 Safari/537.36 
```

Hoewel de informatie gelijkaardig is, bevat het eerste verzoek aan de server de Tips van de Cliënt die slechts een ondergroep van wat in het user-agent koord beschikbaar is bevat. De aanvraag heeft geen betrekking op de architectuur van het besturingssysteem, de volledige versie van het besturingssysteem, de naam van de lay-outengine, de versie van de lay-outengine en de volledige browserversie. Bij volgende aanvragen staat de client Hints-API webservers echter wel toe om aanvullende, hoge entropiedetails over het apparaat te vragen. Wanneer deze hoge entropiewaarden worden gevraagd, afhankelijk van het browserbeleid of gebruikersinstellingen, kan de browserreactie die informatie bevatten.

In het volgende voorbeeld ziet u een JSON-object dat door de client Hints-API wordt geretourneerd wanneer hoge entropiewaarden worden aangevraagd:

```
{ 

    "architecture":"x86", 
    "bitness":"64", 
    "brands":[ 
        { 
            "brand":" Not A;Brand", 
            "version":"99" 
        }, 
        { 
            "brand":"Chromium", 
            "version":"100" 
        }, 
        { 
            "brand":"Google Chrome", 
            "version":"100" 
        } 
    ], 
    "fullVersionList":[ 
        { 
            "brand":" Not A;Brand", 
            "version":"99.0.0.0" 
        }, 
        { 
            "brand":"Chromium", 
            "version":"100.0.4896.127" 
        }, 
        { 
            "brand":"Google Chrome", 
            "version":"100.0.4896.127" 
        } 
    ], 
    "mobile":false, 
    "model":"", 
    "platformVersion":"12.2.1" 
} 
```

De hoge entropiewaarden omvatten verscheidene extra stukken van informatie die niet in de standaardinformatie van de wenken van de Cliënt beschikbaar zijn. De volgende lijst bevat details van welke gegevens in het standaardverzoek tegenover de hoge entropie gebruiker-Agent informatie van de Cliënt beschikbaar zijn.

| HTTP-header | JavaScript | Gebruikersagent | Clienttip | Hoog entropclientijd |
| --- | --- | --- | --- | --- |
| Sec-CH-UA | merken | Ja | Ja | Nee |
| Sec-CH-UA-Platform | platform | Ja | Ja | Nee |
| Sec-CH-UA-Mobile | mobiel | Ja | Ja | Nee |
| Sec-CH-UA-Platform-Version | platformVersion | Ja | Nee | Ja |
| Sec-CH-UA-Arch | architectuur | Ja | Nee | Ja |
| Sec-CH-UA-model | model | Ja | Nee | Ja |
| Sec-CH-UA-Bitness | Bitsheid | Ja | Nee | Ja |
| Sec-CH-UA-Full-Version-List | fullVersionList | Ja | Nee | Ja |

## Migratie naar clienttips

Op dit moment blijven op chroom gebaseerde browsers de user-agent samen met de Tips van de Cliënt in de kopballen van verzoeken verzenden die aan Webservers worden gemaakt. Vanaf april 2022 en tot februari 2023 wordt de hoeveelheid gegevens in de user-agent-tekenreeks echter verminderd. Andere browsers, zoals Safari en Firefox, zullen hefboomwerking het user-agent koord blijven voortzetten; ook zij zullen echter de daarin vervatte informatie verminderen .

## [!DNL Target] gebruik gevallen waarvoor kleurtips vereist zijn

De volgende gebruiksgevallen in Doel vereisen de wenken van de Cliënt:

### Kenmerken publiek

Als u [!DNL Target] publiek en gebruik een van de volgende publiekskenmerken: [!DNL Target] vereist de wenken van de Cliënt om de correcte segmentatie uit te voeren:

* Browser
* Besturingssysteem
* Mobiel

### Profielscripts

Als u profielscripts gebruikt en naar de `user.browser` attribuut (dat naar gebruiker-agent verwijst), zou u het profielmanuscript kunnen moeten bijwerken om één of meerdere wenken van de Cliënt ook te controleren. U kunt tot om het even welke wenken van de Cliënt toegang hebben gebruikend de functie `user.clientHint('sec-ch-ua-xxxxx')`. De naam van de header van de client-tip moet allemaal in kleine letters zijn.

In het volgende voorbeeld ziet u hoe u een Windows-besturingssysteem correct detecteert in een profielscript:

```
"return (((user.browser != null) && (user.browser.indexOf(\"Windows\") > -1)) || " + 
      "((user.clientHint('sec-ch-ua-platform') != null) && 
(user.clientHint('sec-ch-ua-platform') === 'Windows')));" 
```

In de volgende secties worden de kopteksten van Clienttips en de bijbehorende gebruikssemantiek voor profielscripts weergegeven.

#### Sec-CH-UA

Entropie: Lage documentatie: [https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Sec-CH-UA](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Sec-CH-UA){target=_blank} Audience, kenmerk: Scriptgebruik voor browserprofiel: `user.clientHint('sec-ch-ua')`

#### Sec-CH-UA-Arch

Entropie: Hoge documentatie: [https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Sec-CH-UA-Arch](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Sec-CH-UA-Arch){target=_blank} Audience, kenmerk: Gebruik van profielscript: `user.clientHint('sec-ch-ua-arch')`

#### Sec-CH-UA-Bitness

Entropie: Hoge documentatie: [https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Sec-CH-UA-Bitness](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Sec-CH-UA-Bitness){target=_blank} Audience, kenmerk: Gebruik van profielscript: `user.clientHint('sec-ch-ua-bitness')`

#### Sec-CH-UA-Full-Version-List

Entropie: Hoge documentatie: [https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Sec-CH-UA-Full-Version-List](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Sec-CH-UA-Full-Version-List){target=_blank} Audience, kenmerk: Scriptgebruik voor browserprofiel: `user.clientHint('sec-ch-ua-full-version-list')`

#### Sec-CH-UA-Mobile

Entropie: Lage documentatie: [https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Sec-CH-UA-Mobile](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Sec-CH-UA-Mobile){target=_blank} Audience, kenmerk: Scriptgebruik voor mobiele profielen: `user.clientHint('sec-ch-ua-mobile')`

#### Sec-CH-UA-model

Entropie: Hoge documentatie: [https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Sec-CH-UA-Model](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Sec-CH-UA-Model){target=_blank} Audience, kenmerk: Scriptgebruik voor mobiele profielen: `user.clientHint('sec-ch-ua-model')`

#### Sec-CH-UA-Platform

Entropie: Lage documentatie: [https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Sec-CH-UA-Platform](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Sec-CH-UA-Platform){target=_blank} Audience, kenmerk: Scriptgebruik van besturingssysteemprofiel: `user.clientHint('sec-ch-ua-platform')`

#### Sec-CH-UA-Platform-Version

Entropie: Hoge documentatie: [https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Sec-CH-UA-Platform-Version](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Sec-CH-UA-Platform-Version){target=_blank} Audience, kenmerk: Gebruik van profielscript: `user.clientHint('sec-ch-ua-platform-version')`

## Clienttips doorgeven aan [!DNL Adobe Target]

De volgende secties bevatten meer informatie over hoe te om de Tips van de Cliënt over te gaan, afhankelijk van uw [!DNL Target] uitvoering.

### at.js versie 2.9.0 (of hoger)

Vanaf at.js 2.9.0, zullen de wenken van de Cliënt van de Agent van de Gebruiker automatisch van browser worden verzameld en verzonden naar [!DNL Target] wanneer `getOffer/getOffers()` wordt aangeroepen. Standaard verzamelt at at.js alleen &#39;Low Entropy&#39;-clienttips. Als het uitvoeren van publiekssegmentatie of het gebruiken van profielmanuscripten die op gegevens worden gebaseerd die als &quot;Hoge Entropie&quot;van de voorafgaande secties worden gecategoriseerd, moet u at.js vormen om de Hints van de Cliënt &quot;High Entropy&quot;van browser via te verzamelen `targetGlobalSettings`.

`window.targetGlobalSettings = { allowHighEntropyClientHints: true };`

### SDK&#39;s aan serverzijde

Voor meer informatie over hoe te om cliëntwenken via server-kant SDKs over te gaan, zie [Clienttips](https://adobetarget-sdks.gitbook.io/docs/core-principles/audience-targeting#client-hints){target=_blank} in het dialoogvenster *Adobe Target SDK&#39;s* documentatie.












