---
keywords: A4T;Adobe Analytics;Analytics-based activity;Analytics report suite;report suite;Analytics Target integration;configure report suite
description: Bij de implementatie van Adobe Analytics als rapportagebron voor Target (A4T) zijn verschillende stappen vereist.
title: Analyses voor doelimplementatie
feature: null
uuid: da6498c8-1549-4c36-ae42-38c731a28f08
translation-type: tm+mt
source-git-commit: a51addc6155f2681f01f2329b25d72327de36701
workflow-type: tm+mt
source-wordcount: '865'
ht-degree: 0%

---


# Analyses voor doelimplementatie{#analytics-for-target-implementation}

Er zijn verschillende stappen vereist bij de implementatie [!DNL Adobe Analytics] als rapportagebron voor [!DNL Target] (A4T).

## Uitvoeringsstappen {#section_73961BAD5BB4430A95E073DE5C026277}

In de volgende secties worden de stappen beschreven die nodig zijn om deze integratie op uw site te implementeren.

## Stap 1: Aanvoer aanvragen voor Analytics en Target

Nadat u [!DNL Analytics] als rapporteringsbron voor uitvoert, moet u voor [!DNL Target]en [!DNL Analytics] [!DNL Target]worden provisioned. [Gebruik dit formulier om provisioning](http://www.adobe.com/go/audiences)aan te vragen.

## Stap 2: Gebruikersmachtigingen instellen

Aan de vereisten voor gebruikersaccounts moet worden voldaan voordat u een [!DNL Analytics]op basis van activiteiten kunt maken in [!DNL Target]. Zie [Gebruikersvereisten](/help/c-integrating-target-with-mac/a4t/account-reqs.md).

## Stap 3: De service Experience Cloud Visitor ID implementeren

Met de service bezoekersidentiteitskaart kunt u gebruikers identificeren voor verschillende [!DNL Adobe Experience Cloud] oplossingen. U moet de vereiste versie van de Experience Cloud Bezoeker-id implementeren of migreren. Zie &quot;Implementatievereisten&quot; in [Voordat u implementeert](/help/c-integrating-target-with-mac/a4t/before-implement.md)voor meer informatie.

Zie [Voer de Dienst van identiteitskaart van Experience Cloud voor Doel](https://docs.adobe.com/content/help/en/id-service/using/implementation-guides/setup-target.html) in de documentatie van de Dienst *van de* Bezoeker van Experience Cloud uit.

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

De manier de uit-van-de-doos montages voor [!DNL Target] en [!DNL Analytics] integratie vanuit een implementatieperspectief wordt gevormd is SDID te gebruiken die van de pagina wordt overgegaan om het [!DNL Target] en [!DNL Analytics] verzoek samen op de achtergrond automatisch voor u te verbinden.

Als u echter meer controle wilt hebben over hoe en wanneer u analysegegevens wilt verzenden die betrekking hebben [!DNL Target] op [!DNL Analytics] rapportagedoeleinden, en u zich niet wilt aanmelden bij de standaardinstellingen voor het [!DNL Target] automatisch koppelen van de analysegegevens via de SDID, kunt u [!DNL Analytics] analyticsLogging = client_side **via** window.targetGlobalSettings **** instellen. Opmerking: versies onder 2.1 ondersteunen deze aanpak niet.

Bijvoorbeeld:

```
window.targetGlobalSettings = {
  analyticsLogging: "client_side"
};
```

Deze opstelling heeft een globaal effect, zo betekent het dat elke vraag die door at.js wordt gemaakt **analyticsLogging zal hebben: &quot;client_side&quot;** die binnen de [!DNL Target] verzoeken wordt verzonden en een analytische lading zal voor elk verzoek worden teruggegeven. Als deze is ingesteld, ziet de indeling van de geretourneerde lading er als volgt uit:

```
"analytics": {
   "payload": {
      "pe": "tnt",
      "tnta": "167169:0:0|0|100,167169:0:0|2|100,167169:0:0|1|100"
   }
}
```

De payload kan vervolgens naar Analytics worden doorgestuurd via de API [voor het invoegen van](https://helpx.adobe.com/analytics/kb/data-insertion-api-post-method-adobe-analytics.html)gegevens.

Als een globale instelling niet gewenst is en een meer on-demand aanpak de voorkeur verdient, kunt u de functie at.js [getOffers()](/help/c-implementing-target/c-implementing-target-for-client-side-web/adobe-target-getoffers-atjs-2.md) gebruiken om dit te bereiken door **analyticsLogging door te geven: &quot;client_side&quot;**. De analytische lading zal voor slechts deze vraag worden teruggekeerd en de [!DNL Target] backend zal niet de nuttige lading aan [!DNL Analytics]. door:sturen. Door deze benadering na te streven, zal elk [!DNL Target] verzoek at.js niet de lading door gebrek terugkeren, maar in plaats daarvan slechts wanneer gewenst en gespecificeerd.

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

De lading kan dan aan [!DNL Analytics] via de Invoeging van [Gegevens API](https://helpx.adobe.com/analytics/kb/data-insertion-api-post-method-adobe-analytics.html)worden doorgestuurd.

## Stap 8: De implementatie valideren {#step8}

Laad uw pagina&#39;s nadat u de JavaScript-bibliotheken hebt bijgewerkt om te bevestigen dat de `mboxMCSDID` parameterwaarden in [!DNL Target] aanroepen overeenkomen met de `sdid` parameterwaarde in de [!DNL Analytics] paginaweergaveaanroep.

Dit is vooral belangrijk om in de Toepassingen van de Enige Pagina (SPAs) te bevestigen waar de orde van vraag niet altijd voorspelbaar is.

**Opmerking:** Een4T werkt alleen correct als deze waarden overeenkomen.

## Stap 9: (Optioneel) Vorige integratiecode verwijderen

We raden u aan de vorige integratie te verwijderen om uw implementatie te vereenvoudigen en de verschillen tussen de systemen weg te werken. U kunt om het even welke code verwijderen u voor vorige Sc aan integratie T&amp;T, met inbegrip van `mboxLoadSCPlugin`zou kunnen opgesteld.

## Stap 10: De opties inschakelen voor het gebruik van Analytics als rapportagebron voor Doel

Klik [!DNL Target]in en kies een van de opties **[!UICONTROL Administation > Visual Experience Composer]** of **[!UICONTROL Select per activity]** **[!UICONTROL Adobe Analytics]** om de opties in te schakelen.

* **[!UICONTROL Select per activity]** Hiermee kunt u kiezen tussen [!DNL Target] en [!DNL Analytics] bij het maken van elke activiteit.
* **[!UICONTROL Adobe Analytics]** Hiermee stelt u [!DNL Analytics] de rapportbron in voor alle activiteiten die u maakt.

