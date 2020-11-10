---
keywords: dynamic data;assets;data;offers;personalized offers;personal offers;token replace
description: U kunt profielwaarden en activiteitgegevens rechtstreeks weergeven in een HTML- of JSON-aanbieding.
title: Dynamische gegevens in aanbiedingen doorgeven
feature: offers
translation-type: tm+mt
source-git-commit: 968d36d65016e51290f6bf754f69c91fd8f68405
workflow-type: tm+mt
source-wordcount: '492'
ht-degree: 0%

---


# Dynamische gegevens in aanbiedingen doorgeven{#pass-dynamic-data-into-offers}

U kunt bezoekersinformatie dynamisch weergeven die in het doelprofiel is opgeslagen. Op dezelfde manier kan de activiteiteninformatie (zoals de naam van de activiteit of de naam van de ervaring) ook worden gebruikt om één enkele aanbieding tot stand te brengen die dynamisch gepersonaliseerde inhoud op de belangen van de bezoeker, het vroegere gedrag, en algemeen profiel terugkeert.

**Zakelijke zaken**

* Een gedisconteerd voorstel promoten om het laatste aangeschafte product te &quot;vullen&quot; of &quot;aan te vullen&quot;. In plaats van een aparte aanbieding te maken voor elk item in uw catalogus, kunt u een aanbieding maken met dynamische tekst die het &quot;laatst aangeschafte product&quot; uit het profiel leest en een koppeling in de aanbieding weergeeft.
* Een bezoeker komt op uw landingspagina aan met `keyword=world` `cup`. Je geeft de term *Wereldbeker* in het aanbod weer.
* Pas een aanbevolen label aan met informatie zoals (1) het laatste item dat aan de winkelwagentje van een bezoeker is toegevoegd (Nike Air Max 1000 s), (2) de kleurvoorkeur van de bezoeker (zwart) en (3) de favoriete niet-schoenencategorie (hoodies) van de bezoeker. Voorbeeld: &quot;Maak kennis met uw &#39;Nike Air Max 1000s&#39; met deze coole &#39;zwarte&#39; &#39;hoodies&#39;!&quot;


**Technische voordelen**

Omdat gebruikersspecifieke voorkeuren, gedrag, status, enzovoort. kan in het profiel van de gebruiker worden opgeslagen, kunt u dit bericht bij zijn of haar volgende bezoeken herhalen. Dynamische aanbiedingen maken een grotere schaal mogelijk doordat u één aanbieding kunt instellen binnen een activiteit die persoonlijke berichten voor al uw bezoekers weergeeft. Wanneer de intentie van de bezoeker verandert, worden deze wijzigingen automatisch doorgevoerd in uw website-inhoud.

**Voorbeeld**

* `mboxCreate("landingpage"`, `"profile.keyword=World Cup");`

* HTML-aanbiedingscode: `Get your ${profile.keyword} information here!`
* Gebruiker ziet: Haal hier je WK-informatie op!

De volgende waarden kunnen worden vervangen door een token:

| Waarden | Voorbeelden |
|--- |--- |
| Profielparameters in de box | `${profile.age}` |
| Scriptprofielparameters | `${user.lifetimeSpend}` |
| Mbox-parameters | `${mbox.favoriteColor}` |
| Campagnegegevens | `${campaign.name}`, `${campaign.recipe.name}`, `${campaign.id}`, `${campaign.recipe.id}`en `${campaign.recipe.trafficType}` |
| Unieke bezoeker-id | `${user.pcId}` |
| Unieke sessie-id | `${user.sessionId}` |
| Eerste sessie van bezoeker (waar of onwaar) | `${user.isFirstSession}` |
| Gedrag in verleden | `${user.endpoint.lastPurchasedEntity}`, `${user.endpoint.lastViewedEntity}`, `${user.endpoint.mostViewedEntity}`, `${user.endpoint.categoryAffinity}` |

Loggegevens in de console voor foutopsporingsdoeleinden, zoals `${campaign.name}`, `${campaign.id}`, `${campaign.recipe.name}`, `${campaign.recipe.id}`, `${offer.name}`, `${offer.id}`, `${campaign.name}`

Zie aanvullende voorbeelden in het [ontwerpoverzicht](/help/c-recommendations/c-design-overview/design-overview.md)voor Recommendations-ontwerpen.

**Implementatie**

Gebruik de syntaxis voor profielparameters die aan een box worden doorgegeven: `${profile.parameter}` Gebruik de syntaxis voor profielparameters die zijn gemaakt in een profielscript:

`${user.parameter}`

Wanneer u dynamische kenmerken in een Recommendations-ontwerp gebruikt, moet u vóór het dollarteken (&#39;$&#39;) een backslash (&#39;\&#39;) invoegen om de dynamische waarde correct te laten renderen: `\${user.endpoint.lastViewedEntity}`

Deze variabelen worden vervangen door de waarde aan de serverzijde, zodat er geen aanhalingstekens of andere JavaScript vereist zijn voor de juiste weergave.

U kunt ook standaardwaarden opgeven voor waarden die u toegankelijk wilt maken voor aanbiedingen. De syntaxis is als volgt:

`${user.testAttribute default="All Items!"}`

Als `testAttribute` dit niet het geval is of leeg is, klikt u op Alle items! wordt opgeschreven. Als een lege kenmerkwaarde geldig is en u wilt het uit in plaats van het tonen van het gebrek schrijven, kunt u gebruiken:

`${user.testAttribute default="All Items!" show_blank="true"}`

U kunt ook escape- en unescape-waarden weergeven. Als uw waarde bijvoorbeeld een apostrof heeft, wilt u aan de waarde ontsnappen zodat het JavaScript op de pagina niet wordt verbroken. (Aanbiedingen worden geschreven in JavaScript, zodat één apostrof voor een aanhalingsteken kan worden verward.) Bijvoorbeeld:

`${user.encodedValue encode="unescape"}`

`${user.unencodedValue encode="escape"}`