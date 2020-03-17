---
keywords: A4T;Adobe Analytics;Analytics-based activity;Analytics report suite;report suite;Analytics Target integration;configure report suite
description: Er zijn verschillende stappen vereist voor het implementeren van Adobe Analytics als de rapportbron voor Target (A4T).
title: Analyses voor doelimplementatie
uuid: da6498c8-1549-4c36-ae42-38c731a28f08
translation-type: tm+mt
source-git-commit: 217ca811521e67dcd1b063d77a644ba3ae94a72c

---


# Analyses voor doelimplementatie{#analytics-for-target-implementation}

Er zijn verschillende stappen vereist voor het implementeren van Adobe Analytics als de rapportbron voor Target (A4T).

## Implementatiestappen {#section_73961BAD5BB4430A95E073DE5C026277}

In de volgende tabel worden de stappen beschreven die zijn vereist om deze integratie op uw site te implementeren.

## Stap 1: Aanvoer aanvragen voor Analytics en Target

Nadat u Analytics als rapporteringsbron voor Doel uitvoert, moet u voor Analytics en Doel worden provisioned. [Gebruik dit formulier om provisioning](http://www.adobe.com/go/audiences)aan te vragen.

## Stap 2: Gebruikersmachtigingen instellen

Aan de vereisten voor gebruikersaccounts moet worden voldaan voordat u een op Adobe Analytics gebaseerde activiteit kunt maken in Adobe Target. Zie [Gebruikersvereisten](/help/c-integrating-target-with-mac/a4t/account-reqs.md).

## Stap 3: De dienst Experience Cloud Visitor ID implementeren

Met de bezoeker-id-service kunt u gebruikers identificeren op verschillende manieren met de Experience Cloud-oplossingen. U moet de vereiste versie van de Experience Cloud Visitor ID implementeren of migreren. Zie &quot;Implementatievereisten&quot; in [Voordat u implementeert](/help/c-integrating-target-with-mac/a4t/before-implement.md)voor meer informatie.

Zie [De Experience Cloud ID Service for Target](https://docs.adobe.com/content/help/en/id-service/using/implementation-guides/setup-target.html) implementeren in de documentatie van de Experience Cloud Visitor ID Service.

## Stap 4: AppMeasurement voor JavaScript of s_code bijwerken

U moet de vereiste versie van appMeasurement.js implementeren of migreren. Zie &quot;Implementatievereisten&quot; in [Voordat u implementeert](/help/c-integrating-target-with-mac/a4t/before-implement.md)voor meer informatie.

Zie Overzicht [van](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/javascript-implementation-overview.html) JavaScript-implementatie in de *handleiding* Analytics Implementation voor nieuwe implementaties.

Zie [Migreren naar AppMeasurement voor JavaScript](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/appmeasurement-js/appmeasure-mjs-migrate.html) in de *handleiding* voor analysetransplementatie voor een migratie.

## Stap 5: Downloaden en bijwerken om.js of mbox.js

U moet de vereiste versie van at.js of mbox.js implementeren of migreren met uw productieaccount. De code hoeft niet te worden gewijzigd.

Zie &quot;Implementatievereisten&quot; in [Voordat u implementeert](/help/c-integrating-target-with-mac/a4t/before-implement.md)voor meer informatie.

## Stap 6: Host at.js of mbox.js

Als u eerder om.js of mbox.js opstelde, kunt u uw bestaand dossier met de bijgewerkte versie vervangen. Zie &quot;Implementatievereisten&quot; in [Voordat u implementeert](/help/c-integrating-target-with-mac/a4t/before-implement.md)voor meer informatie.

Anders kan dit bestand worden gehost samen met de bezoekersidentiteitsservice en AppMeasurement voor JavaScript-bestanden. Deze bestanden moeten worden gehost op een webserver die toegankelijk is voor alle pagina&#39;s op uw site. U hebt het pad naar deze bestanden nodig in de volgende stap.

## Stap 7: Verwijzing om.js of mbox.js op alle plaatspagina&#39;s {#step7}

Neem at.js of mbox.js op onder VisitorAPI.js door de volgende coderegel toe te voegen aan de tag op elke pagina:

Voor at.js:

```
<script language="JavaScript" type="text/javascript"
src="http://INSERT-DOMAIN-AND-PATH-TO-CODE-HERE/at.js"></script>
```

Voor mbox.js:

```
<script language="JavaScript" type="text/javascript"
src="http://INSERT-DOMAIN-AND-PATH-TO-CODE-HERE/mbox.js"></script>
```

Het is van essentieel belang dat VisitorAPI.js vóór at.js of mbox.js wordt geladen. Als u een bestaand bestand van het type at.js of mbox.js bijwerkt, moet u de laadvolgorde controleren.

De manier de uit-van-de-doos montages voor de integratie van het Doel en van de Analyse van een implementatieperspectief worden gevormd is SDID te gebruiken die van de pagina wordt overgegaan om het doel en verzoek van de Analyse samen op de achtergrond automatisch voor u te binden.

Als u echter meer controle wilt hebben over de manier waarop en wanneer analysegegevens met betrekking tot Target naar Analytics worden verzonden voor rapportagedoeleinden, en u zich niet wilt aanmelden bij de standaardinstellingen voor het automatisch koppelen van de analysegegevens via de SDID door Doel en Analytics, kunt u **analyticsLogging = client_side** via **window.targetGlobalSettings** instellen. Opmerking: versies onder 2.1 ondersteunen deze aanpak niet.

Bijvoorbeeld:

```
window.targetGlobalSettings = {
  analyticsLogging: "client_side"
};
```

Deze opstelling heeft een globaal effect, zo betekent het dat elke vraag die door at.js wordt gemaakt **analyticsLogging zal hebben: &quot;client_side&quot;** die binnen de verzoeken van het Doel wordt verzonden en een analytische lading zal voor elk verzoek worden teruggegeven. Als deze is ingesteld, ziet de indeling van de geretourneerde lading er als volgt uit:

```
"analytics": {
   "payload": {
      "pe": "tnt",
      "tnta": "167169:0:0|0|100,167169:0:0|2|100,167169:0:0|1|100"
   }
}
```

De payload kan vervolgens naar Analytics worden doorgestuurd via de API [voor het invoegen van](https://helpx.adobe.com/analytics/kb/data-insertion-api-post-method-adobe-analytics.html)gegevens.

Als een globale instelling niet gewenst is en een meer on-demand aanpak de voorkeur verdient, kunt u de functie at.js [getOffers()](/help/c-implementing-target/c-implementing-target-for-client-side-web/adobe-target-getoffers-atjs-2.md) gebruiken om dit te bereiken door **analyticsLogging door te geven: &quot;client_side&quot;**. De analytische lading zal voor slechts deze vraag worden teruggekeerd en de backend van het Doel zal niet de nuttige lading aan Analytics door:sturen. Door deze benadering na te streven, zal elk verzoek van het Doel at.js niet de nuttige lading door gebrek terugkeren, maar in plaats daarvan slechts wanneer gewenst en gespecificeerd.

Bijvoorbeeld:

```
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

```
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

De payload kan vervolgens naar Analytics worden doorgestuurd via de API [voor het invoegen van](https://helpx.adobe.com/analytics/kb/data-insertion-api-post-method-adobe-analytics.html)gegevens.

## Stap 8: De implementatie valideren {#step8}

Laad uw pagina&#39;s nadat u de JavaScript-bibliotheken hebt bijgewerkt om te bevestigen dat de parameterwaarden mboxMCSDID in de aanroepen van Target overeenkomen met de parameterwaarde in de paginaweergaveaanroep Analytics.

Dit is vooral belangrijk om in de Toepassingen van de Enige Pagina (SPAs) te bevestigen waar de orde van vraag niet altijd voorspelbaar is.

**Opmerking:** Een4T werkt alleen correct als deze waarden overeenkomen.

## Stap 9: (Optioneel) Vorige integratiecode verwijderen

We raden u aan de vorige integratie te verwijderen om uw implementatie te vereenvoudigen en de verschillen tussen de systemen weg te werken. U kunt om het even welke code verwijderen u voor vorige Sc aan integratie T&amp;T, met inbegrip van `mboxLoadSCPlugin`zou kunnen opgesteld.

## Stap 10: De opties inschakelen voor het gebruik van Analytics als rapportagebron voor Doel

Klik op Doel [!UICONTROL Setup > Preferences] en kies [!UICONTROL Select per activity] of [!UICONTROL Adobe Analytics] om de opties in te schakelen.

* Met de optie Per activiteit selecteren kunt u kiezen tussen Doel en Analyse bij het maken van elke activiteit.
* Adobe Analytics stelt Analytics in als de rapportbron voor alle activiteiten die u maakt.

