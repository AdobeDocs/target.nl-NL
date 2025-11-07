---
keywords: dynamische gegevens;elementen;gegevens;aanbiedingen;gepersonaliseerde aanbiedingen;persoonlijke aanbiedingen;symbolische vervanging
description: Leer hoe te om dynamische gegevens in Aanbiedingen in  [!DNL Adobe Target] over te gaan.
title: Hoe geef ik dynamische gegevens in aanbiedingen door?
feature: Experiences and Offers
exl-id: b8f9c6eb-1000-41a2-aa3f-bc42c1ef5669
source-git-commit: e45ac15a60c83e35b8b2b2ba29a42727faf746df
workflow-type: tm+mt
source-wordcount: '536'
ht-degree: 0%

---

# Dynamische gegevens in aanbiedingen doorgeven

U kunt bezoekersinformatie dynamisch weergeven die is opgeslagen in het [!DNL Adobe Target] -profiel. Op dezelfde manier kan de activiteiteninformatie (zoals de naam van de activiteit of de naam van de ervaring) ook worden gebruikt om één enkele aanbieding tot stand te brengen die dynamisch gepersonaliseerde inhoud op de belangen van de bezoeker, het vroegere gedrag, en algemeen profiel terugkeert.

## Zakelijke zaken

* Een gedisconteerd voorstel promoten om het laatste aangeschafte product te &quot;vullen&quot; of &quot;aan te vullen&quot;. In plaats van een aparte aanbieding te maken voor elk item in uw catalogus, kunt u een aanbieding maken met dynamische tekst die het &quot;laatst aangeschafte product&quot; uit het profiel leest en een koppeling in de aanbieding weergeeft.
* Een bezoeker arriveert op de bestemmingspagina met `keyword=world` `cup` . U toont de term *Wekker van de Wereld* in de aanbieding.
* Pas een aanbevolen label aan met informatie, zoals (1) het laatste item dat aan het winkelwagentje van een bezoeker is toegevoegd (Nike Air Max 1000 s), (2) de kleurvoorkeur van de bezoeker (zwart) en (3) de favoriete niet-schoenencategorie (hoodies) van de bezoeker. Voorbeeld: &quot;Maak uw &#39;Nike Air Max 1000s&#39; bekend met deze coole &#39;zwarte&#39; &#39;hoodies&#39;!&quot;

## Technische voordelen

Omdat bezoekersspecifieke voorkeuren, gedrag en status kunnen worden opgeslagen in het profiel van de bezoeker, kunt u dit bericht bij de volgende bezoeken herhalen. Dynamische aanbiedingen maken een grotere schaal mogelijk doordat u één aanbieding kunt instellen binnen een activiteit die persoonlijke berichten voor al uw bezoekers weergeeft. Wanneer de intentie van de bezoeker verandert, worden deze wijzigingen automatisch doorgevoerd in uw website-inhoud.

## Voorbeeld

* `mboxCreate("landingpage"`, `"profile.keyword=World Cup");`

* HTML-aanbiedingscode: `Get your ${profile.keyword} information here!`
* Bezoeker ziet: Haal hier je WK-informatie!

De volgende waarden kunnen worden vervangen door een token:

| Waarde | Voorbeelden |
|--- |--- |
| Profielparameters in de box | `${profile.age}` |
| Scriptprofielparameters | `${user.lifetimeSpend}` |
| Mbox-parameters | `${mbox.favoriteColor}` |
| Campagnegegevens | `${campaign.name}` , `${campaign.recipe.name}` , `${campaign.id}` , `${campaign.recipe.id}` en `${campaign.recipe.trafficType}` |
| Unieke bezoeker-id | `${user.pcId}` |
| Unieke sessie-id | `${user.sessionId}` |
| Eerste sessie van bezoeker (waar of onwaar) | `${user.isFirstSession}` |
| Gedrag in verleden | `${user.endpoint.lastPurchasedEntity}`, `${user.endpoint.lastViewedEntity}`, `${user.endpoint.mostViewedEntity}`, `${user.endpoint.categoryAffinity}` |

Loggegevens in de console voor foutopsporingsdoeleinden, zoals `${campaign.name}` , `${campaign.id}` , `${campaign.recipe.name}` , `${campaign.recipe.id}` , `${offer.name}` , `${offer.id}` , `${campaign.name}`

Voor [!DNL Recommendations] ontwerpen, zie extra voorbeelden in [ Overzicht van het Ontwerp ](/help/main/c-recommendations/c-design-overview/design-overview.md).

## Implementatie

Gebruik de syntaxis voor profielparameters die aan een box worden doorgegeven:

`${profile.parameter}`

Gebruik de syntaxis voor profielparameters die zijn gemaakt in een profielscript:

`${user.parameter}`

Wanneer u dynamische kenmerken in een [!DNL Recommendations] -ontwerp gebruikt, moet u vóór het dollarteken ( $ ) een backslash ( \ ) invoegen om de dynamische waarde correct te renderen:

`\${user.endpoint.lastViewedEntity}`

Deze variabelen worden vervangen door de waarde aan de serverzijde, zodat er geen aanhalingstekens of andere JavaScript nodig zijn voor de juiste weergave.

U kunt ook standaardwaarden opgeven voor waarden die u toegankelijk wilt maken voor aanbiedingen. De syntaxis is als volgt:

`${user.testAttribute default="All Items!"}`

Wanneer `testAttribute` niet bestaat of leeg is, &quot;Alle items!&quot; wordt uitgeschreven. Als een lege kenmerkwaarde geldig is en u wilt het uit in plaats van het tonen van het gebrek schrijven, kunt u gebruiken:

`${user.testAttribute default="All Items!" show_blank="true"}`

U kunt ook escape- en unescape-waarden weergeven. Als uw waarde bijvoorbeeld een apostrof heeft, kunt u de waarde laten ontsnappen zodat de JavaScript niet wordt verbroken op de pagina. (Aanbiedingen worden geschreven in JavaScript, zodat één apostrof voor een prijsopgave kan worden verward.) Bijvoorbeeld:

`${user.encodedValue encode="unescape"}`

`${user.unencodedValue encode="escape"}`

Voor aanbiedingsparameters (aanbieding.name, aanbieding.id) die worden gebruikt in de inhoud van een aanbieding:

Als dat aanbod een van de verschillende aanbiedingen is die op een ervaring zijn ingesteld, wordt met de waarde van de laatste toegevoegde aanbieding de waarde van de parameter ingevuld. Dit betekent dat deze parameters op het ervaringsniveau worden geëvalueerd.