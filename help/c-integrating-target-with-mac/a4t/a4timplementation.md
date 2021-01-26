---
keywords: A4T;Adobe Analytics;Analytics-based activity;Analytics report suite;report suite;Analytics Target integration;configure report suite
description: Bij de implementatie van Adobe Analytics als rapportagebron voor Target (A4T) zijn verschillende stappen vereist.
title: Analyses voor doelimplementatie
feature: Analytics for Target (A4T)
translation-type: tm+mt
source-git-commit: cf47b7f3625bb1c3430b9fba00c573f489efc448
workflow-type: tm+mt
source-wordcount: '878'
ht-degree: 0%

---


# Analyses voor doelimplementatie{#analytics-for-target-implementation}

Bij de implementatie van [!DNL Adobe Analytics] als rapportagebron voor [!DNL Target] (A4T) zijn verschillende stappen vereist.

## Implementatiestappen {#section_73961BAD5BB4430A95E073DE5C026277}

In de volgende secties worden de stappen beschreven die nodig zijn om deze integratie op uw site te implementeren.

## Stap 1: Aanvoer aanvragen voor Analytics en Target

Nadat u [!DNL Analytics] als rapporteringsbron voor [!DNL Target] uitvoert, moet u provisioned voor [!DNL Analytics] en [!DNL Target] zijn. [Gebruik dit formulier om provisioning](http://www.adobe.com/go/audiences) aan te vragen.

## Stap 2: Gebruikersmachtigingen instellen

Aan de vereisten voor gebruikersaccounts moet worden voldaan voordat u een op [!DNL Analytics] gebaseerde activiteit kunt maken in [!DNL Target]. Zie [Vereisten voor gebruikerstoestemming](/help/c-integrating-target-with-mac/a4t/account-reqs.md).

## Stap 3: De service Experience Cloud Visitor ID implementeren

Met de bezoekersidentiteitsservice kunt u gebruikers identificeren met verschillende [!DNL Adobe Experience Cloud]-oplossingen. U moet de vereiste versie van de Experience Cloud Bezoeker-id implementeren of migreren. Zie &quot;Implementatievereisten&quot; in [Voordat u](/help/c-integrating-target-with-mac/a4t/before-implement.md) implementeert voor meer informatie.

Zie [De Experience Cloud ID-service voor doel implementeren](https://experienceleague.adobe.com/docs/id-service/using/implementation-guides/setup-target.html) in de *Experience Cloud-documentatie voor bezoekers-id Service*.

## Stap 4: AppMeasurement voor JavaScript of s_code bijwerken

U moet de vereiste versie van appMeasurement.js implementeren of migreren. Zie &quot;Implementatievereisten&quot; in [Voordat u](/help/c-integrating-target-with-mac/a4t/before-implement.md) implementeert voor meer informatie.

Voor nieuwe implementaties, zie [Overzicht van de implementatie JavaScript](https://experienceleague.adobe.com/docs/analytics/implementation/javascript-implementation/javascript-implementation-overview.html) in *de Gids van de Implementatie van Analytics*.

Voor een migratie, zie [Migrating to AppMeasurement for JavaScript](https://experienceleague.adobe.com/docs/analytics/implementation/javascript-implementation/appmeasurement-js/appmeasure-mjs-migrate.html) in *Analytics Implementation Guide*.

## Stap 5: Downloaden en bijwerken om.js

U moet de vereiste versie van at.js implementeren of migreren met uw productieaccount. De code hoeft niet te worden gewijzigd.

Zie &quot;Implementatievereisten&quot; in [Voordat u](/help/c-integrating-target-with-mac/a4t/before-implement.md) implementeert voor meer informatie.

## Stap 6: Host om.js

Als u eerder om.js opstelde, kunt u uw bestaand dossier met de bijgewerkte versie vervangen. Zie &quot;Implementatievereisten&quot; in [Voordat u](/help/c-integrating-target-with-mac/a4t/before-implement.md) implementeert voor meer informatie.

Anders kan dit bestand worden gehost samen met de bezoekersidentiteitsservice en AppMeasurement voor JavaScript-bestanden. Deze bestanden moeten worden gehost op een webserver die toegankelijk is voor alle pagina&#39;s op uw site. U hebt het pad naar deze bestanden nodig in de volgende stap.

## Stap 7: Referentie om.js op alle sitepagina&#39;s {#step7}

Neem de code at.js onder VisitorAPI.js op door de volgende coderegel toe te voegen aan de tag op elke pagina:

Voor at.js:

```javascript
<script language="JavaScript" type="text/javascript"
src="http://INSERT-DOMAIN-AND-PATH-TO-CODE-HERE/at.js"></script>
```

Het is van essentieel belang dat VisitorAPI.js vóór at.js wordt geladen. Als u een bestaand bestand van het type at.js of mbox.js bijwerkt, moet u de laadvolgorde controleren.

De manier de uit-van-de-doos montages voor [!DNL Target] en [!DNL Analytics] integratie uit een implementatieperspectief wordt gevormd is SDID te gebruiken die van de pagina wordt overgegaan om [!DNL Target] en [!DNL Analytics] verzoek samen op het achterste eind automatisch voor u te binden.

Als u echter meer controle wilt hebben over de manier waarop en wanneer u analysegegevens met betrekking tot [!DNL Target] naar [!DNL Analytics] wilt verzenden voor rapportagedoeleinden, en u zich niet wilt aanmelden bij de standaardinstellingen om [!DNL Target] en [!DNL Analytics] automatisch te koppelen via de SDID, kunt u **analyticsLogging = client_side** via **instellen window.targetGlobalSettings**. Opmerking: versies onder 2.1 ondersteunen deze aanpak niet.

Bijvoorbeeld:

```javascript
window.targetGlobalSettings = {
  analyticsLogging: "client_side"
};
```

Deze opstelling heeft een globaal effect, wat betekent dat elke vraag die door at.js wordt gemaakt **analyticsLogging zal hebben: &quot;client_side&quot;** verzonden binnen de [!DNL Target] verzoeken en een analytische lading zal voor elk verzoek worden teruggegeven. Als deze is ingesteld, ziet de indeling van de geretourneerde lading er als volgt uit:

```javascript
"analytics": {
   "payload": {
      "pe": "tnt",
      "tnta": "167169:0:0|0|100,167169:0:0|2|100,167169:0:0|1|100"
   }
}
```

De nuttige lading kan dan aan Analytics via [de Invoeging API van Gegevens](https://helpx.adobe.com/analytics/kb/data-insertion-api-post-method-adobe-analytics.html) door:sturen. Merk op dat, voor [!UICONTROL Auto-Allocate] en [!UICONTROL Auto-Target] activiteiten u ook sessionId zult moeten door:sturen. Zie [Analytics for Target (A4T) reporting](https://adobetarget-sdks.gitbook.io/docs/integration-with-experience-cloud/analytics-for-target-a4t-reporting) in de handleiding *Adobe Target SDKs* voor meer informatie.

Als een globale instelling niet gewenst is en een meer on-demand aanpak de voorkeur verdient, kunt u de functie at.js [getOffers()](/help/c-implementing-target/c-implementing-target-for-client-side-web/adobe-target-getoffers-atjs-2.md) gebruiken om dit te bereiken door **analyticsLogging door te geven: &quot;client_side&quot;**. De payload van de analyse wordt alleen voor deze aanroep geretourneerd en de backend [!DNL Target] stuurt de payload niet door naar [!DNL Analytics]. Door deze benadering na te streven, zal elk verzoek at.js [!DNL Target] niet de nuttige lading door gebrek terugkeren, maar in plaats daarvan slechts wanneer gewenst en gespecificeerd.

Bijvoorbeeld:

```javascript
adobe.target.getOffers({
      request: {
        experienceCloud: {
          analytics: {
            logging: "client_side"
          }
        },
        prefetch: {
          mboxes: [{
            index: 0,
            name: "a1-serverside-xt"
          }]
        }
      }
    })
    .then(console.log)
```

Deze vraag haalt een reactie aan waaruit u de analytische lading kunt halen.

De reactie ziet er als volgt uit:

```javascript
{
  "prefetch": {
    "mboxes": [{
      "index": 0,
      "name": "a1-serverside-xt",
      "options": [{
        "content": "<img src=\"http://s7d2.scene7.com/is/image/TargetAdobeTargetMobile/L4242-xt-usa?tm=1490025518668&fit=constrain&hei=491&wid=980&fmt=png-alpha\"/>",
        "type": "html",
        "eventToken": "n/K05qdH0MxsiyH4gX05/2qipfsIHvVzTQxHolz2IpSCnQ9Y9OaLL2gsdrWQTvE54PwSz67rmXWmSnkXpSSS2Q==",
        "responseTokens": {
          "profile.memberlevel": "0",
          "geo.city": "bucharest",
          "activity.id": "167169",
          "experience.name": "USA Experience",
          "geo.country": "romania"
        }
      }],
      "analytics": {
        "payload": {
          "pe": "tnt",
          "tnta": "167169:0:0|0|100,167169:0:0|2|100,167169:0:0|1|100"
        }
      }
    }]
  }
}
```

De lading kan dan aan [!DNL Analytics] via [de Invoeging API van Gegevens](https://helpx.adobe.com/analytics/kb/data-insertion-api-post-method-adobe-analytics.html) door:sturen.

## Stap 8: Implementatie {#step8} valideren

Laad uw pagina&#39;s nadat u de JavaScript-bibliotheken hebt bijgewerkt om te bevestigen dat de `mboxMCSDID`-parameterwaarden in [!DNL Target]-aanroepen overeenkomen met de `sdid`-parameterwaarde in de paginaweergaveaanroep [!DNL Analytics].

Dit is vooral belangrijk om in de Toepassingen van de Enige Pagina (SPA) te bevestigen waar de orde van vraag niet altijd voorspelbaar is.

**Opmerking:** de overeenstemming van deze waarden is vereist om A4T correct te laten functioneren.

## Stap 9: (Optioneel) Vorige integratiecode verwijderen

We raden u aan de vorige integratie te verwijderen om uw implementatie te vereenvoudigen en de verschillen tussen de systemen weg te werken. U kunt om het even welke code verwijderen u voor vorige Sc aan integratie T&amp;T, met inbegrip van `mboxLoadSCPlugin` zou kunnen opgesteld.

## Stap 10: De opties inschakelen voor het gebruik van Analytics als rapportagebron voor Doel

Klik in [!DNL Target] op **[!UICONTROL Administation > Visual Experience Composer]** en kies **[!UICONTROL Select per activity]** of **[!UICONTROL Adobe Analytics]** om de opties in te schakelen.

* **[!UICONTROL Select per activity]** Hiermee kunt u kiezen tussen  [!DNL Target] en  [!DNL Analytics] bij het maken van elke activiteit.
* **[!UICONTROL Adobe Analytics]** Hiermee stelt u  [!DNL Analytics] de rapportbron in voor alle activiteiten die u maakt.

