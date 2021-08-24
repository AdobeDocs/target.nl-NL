---
keywords: A4T;Adobe Analytics;Analytics-gebaseerde activiteit;Analytics report suite;report suite;Analytics Target integration;configure report suite;at.js;atjs;adobe Experience platform web sdk;aep web sdk;platform web sdk
description: Voer de stappen uit die nodig zijn voor het implementeren van Analytics voor [!DNL Target] (A4T) in your Adobe [!DNL Target] en Adobe Analytics-oplossingen.
title: Hoe implementeer ik Analytics voor [!DNL Target] (A4T)?
feature: Analyses voor doel (A4T)
exl-id: b5269b9e-01ef-449a-bb03-3dcc2cd68af7
source-git-commit: eddde1bae345e2e28ca866662ba9664722dedecd
workflow-type: tm+mt
source-wordcount: '1114'
ht-degree: 0%

---

# Analyses voor implementatie [!DNL Target]

Bij de implementatie van [!DNL Adobe Analytics] als rapportagebron voor [!DNL Adobe Target] (A4T) zijn verschillende stappen vereist. Het proces varieert afhankelijk van of u A4T met [[!DNL Adobe Experience Platform Web SDK]](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html) of met at.js implementeert.

## ![Adobe Experience Platform Web SDK ](/help/assets/platform.png) badgeImplementation-stappen voor een Adobe Experience Platform Web SDK-implementatie {#platform}

De volgende secties beschrijven de stappen die worden vereist om deze integratie aan uw plaats op te stellen als u van plan bent om SDK van het Web van het Platform te gebruiken:

### Stap 1: Aanvraag voor [!DNL Analytics] en [!DNL Target]

Voordat u A4T implementeert, moet u provisioned zijn voor [!DNL Analytics] en [!DNL Target]. [Gebruik dit formulier om provisioning](https://adobe.allegiancetech.com/cgi-bin/qwebcorporate.dll?idx=X8SVES) aan te vragen.

### Stap 2: Gebruikersmachtigingen instellen

Aan de vereisten voor gebruikersaccounts moet worden voldaan voordat u een activiteit kunt maken op basis van [!DNL Analytics] in [!DNL Target]. Zie [Vereisten voor gebruikerstoestemming](/help/c-integrating-target-with-mac/a4t/account-reqs.md).

### Stap 3: Een Edge-configuratie maken

Creeer een configuratie van de Rand gebruikend [!DNL Adobe Experience Platform] gebruikend het hulpmiddel van de randconfiguratie. Vorm [[!DNL Analytics] and [!DNL Target] de montages van de randconfiguratie](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/datastreams.html).

### Stap 4: De SDK van het Web Platform installeren en configureren

[Installeer ](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/installing-the-sdk.html) en [configureer](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/configuring-the-sdk.html) de Web SDK van het Platform op uw sitepagina&#39;s om [!DNL Target] ervaringen te leveren en [!DNL Analytics] toe te passen voor tracerings- en analysedoeleinden.

### Stap 5: Opties inschakelen voor het gebruik van A4T

In [!DNL Target] UI, klik **[!UICONTROL Administration]** > **[!UICONTROL Visual Experience Composer]**, dan kies of **[!UICONTROL Select per activity]** of **[!UICONTROL Adobe Analytics]**.

* **[!UICONTROL Select per activity]** Hiermee kunt u kiezen tussen  [!DNL Target] en  [!DNL Analytics] bij het maken van elke activiteit.
* **[!UICONTROL Adobe Analytics]** Hiermee stelt u  [!DNL Analytics] de rapportbron in voor alle activiteiten die u maakt.

## ![at.js ](/help/assets/atjs.png) badgeImplementatiestappen voor een at.js-implementatie{#section_73961BAD5BB4430A95E073DE5C026277}

In de volgende secties worden de stappen beschreven die nodig zijn om deze integratie op uw site te implementeren als u van plan bent om at.js te gebruiken:

### Stap 1: Aanvoer aanvragen voor Analytics en Target

Nadat u [!DNL Analytics] als rapporteringsbron voor [!DNL Target] uitvoert, moet u provisioned voor [!DNL Analytics] en [!DNL Target] zijn. [Gebruik dit formulier om provisioning](https://www.adobe.com/go/audiences) aan te vragen.

### Stap 2: Gebruikersmachtigingen instellen

Aan de vereisten voor gebruikersaccounts moet worden voldaan voordat u een op [!DNL Analytics] gebaseerde activiteit kunt maken in [!DNL Target]. Zie [Vereisten voor gebruikerstoestemming](/help/c-integrating-target-with-mac/a4t/account-reqs.md).

### Stap 3: De service Experience Cloud Visitor ID implementeren

Met de bezoekersidentiteitsservice kunt u gebruikers identificeren met verschillende [!DNL Adobe Experience Cloud]-oplossingen. Voer of migreer aan de vereiste versie van identiteitskaart van de Bezoeker van de Experience Cloud uit. Zie &quot;Implementatievereisten&quot; in [Voordat u](/help/c-integrating-target-with-mac/a4t/before-implement.md) implementeert voor meer informatie.

Zie [De Experience Cloud ID-service voor doel implementeren](https://experienceleague.adobe.com/docs/id-service/using/implementation/setup-target.html) in de *Experience Cloud-documentatie voor bezoekers-id Service*.

### Stap 4: AppMeasurement voor JavaScript of s_code bijwerken

Implementeer of migreer naar de vereiste versie van appMeasurement.js. Zie &quot;Implementatievereisten&quot; in [Voordat u](/help/c-integrating-target-with-mac/a4t/before-implement.md) implementeert voor meer informatie.

Voor nieuwe implementaties, zie [Overzicht van de implementatie JavaScript](https://experienceleague.adobe.com/docs/analytics/implementation/js/overview.html) in *de Gids van de Implementatie van Analytics*.

Voor een migratie, zie [Migrating to AppMeasurement for JavaScript](https://experienceleague.adobe.com/docs/analytics/implementation/js/migrate-from-hcode.html) in *Analytics Implementation Guide*.

### Stap 5: Downloaden en bijwerken om.js

Implementeer of migreer naar de vereiste versie van at.js met uw productieaccount. De code hoeft niet te worden gewijzigd.

Zie &quot;Implementatievereisten&quot; in [Voordat u](/help/c-integrating-target-with-mac/a4t/before-implement.md) implementeert voor meer informatie.

### Stap 6: Host om.js

Als u eerder om.js opstelde, kunt u uw bestaand dossier met de bijgewerkte versie vervangen. Zie &quot;Implementatievereisten&quot; in [Voordat u](/help/c-integrating-target-with-mac/a4t/before-implement.md) implementeert voor meer informatie.

Anders kan dit bestand worden gehost samen met de bezoekersidentiteitsservice en AppMeasurement voor JavaScript-bestanden. Deze bestanden moeten worden gehost op een webserver die toegankelijk is voor alle pagina&#39;s op uw site. U hebt het pad naar deze bestanden nodig in de volgende stap.

### Stap 7: Referentie om.js op alle sitepagina&#39;s {#step7}

Neem de code at.js onder VisitorAPI.js op door de volgende coderegel toe te voegen aan de tag op elke pagina:

Voor at.js:

```javascript
<script language="JavaScript" type="text/javascript"
src="http://INSERT-DOMAIN-AND-PATH-TO-CODE-HERE/at.js"></script>
```

De visitorAPI.js moet worden geladen vóór at.js. Als u een bestaand at.js- dossier bijwerkt, zorg ervoor dat u de ladingsorde verifieert.

De standaardinstelling voor [!DNL Target]- en [!DNL Analytics]-integratie vanuit implementatieperspectief is dat de SDID wordt gebruikt die vanuit de pagina wordt doorgegeven, zodat de aanvraag [!DNL Target] en [!DNL Analytics] automatisch op de achtergrond wordt gekoppeld.

U kunt bepalen hoe en wanneer u analysegegevens wilt verzenden met betrekking tot [!DNL Target] naar [!DNL Analytics] voor rapportagedoeleinden. Als u niet aan de standaardinstellingen wilt deelnemen om [!DNL Target] en [!DNL Analytics] automatisch de analysegegevens via de SDID te laten aansluiten, stelt u **analyticsLogging = client_side** via **window.targetGlobalSettings** in. Opmerking: versies onder 2.1 ondersteunen deze aanpak niet.

Bijvoorbeeld:

```javascript
window.targetGlobalSettings = {
  analyticsLogging: "client_side"
};
```

Deze opstelling heeft een globaal effect, zo betekent het dat elke vraag die door at.js wordt gemaakt **analyticsLogging heeft: &quot;client_side&quot;** verzonden binnen de [!DNL Target] verzoeken en een analytische lading is teruggekeerd voor elke verzoek. Als deze optie is ingesteld, ziet de indeling van de geretourneerde lading er als volgt uit:

```javascript
"analytics": {
   "payload": {
      "pe": "tnt",
      "tnta": "167169:0:0|0|100,167169:0:0|2|100,167169:0:0|1|100"
   }
}
```

De nuttige lading kan dan aan Analytics via [de Invoeging API van Gegevens](https://helpx.adobe.com/analytics/kb/data-insertion-api-post-method-adobe-analytics.html) door:sturen. Voor auto-Wijs en auto-Doel activiteiten, moet u sessionId ook door:sturen. Zie [Analytics for Target (A4T) reporting](https://adobetarget-sdks.gitbook.io/docs/integration-with-experience-cloud/analytics-for-target-a4t-reporting) in de handleiding *Adobe Target SDKs* voor meer informatie.

Als een globale instelling niet gewenst is en een meer on-demand-aanpak de voorkeur verdient, gebruikt u de at.js-functie [getOffers()](/help/c-implementing-target/c-implementing-target-for-client-side-web/adobe-target-getoffers-atjs-2.md) door **analyticsLogging door te geven: &quot;client_side&quot;**. De analytische lading wordt teruggekeerd voor deze vraag slechts en [!DNL Target] achterste niet door:sturen de nuttige lading aan [!DNL Analytics]. Door deze benadering na te streven, keert elk verzoek at.js [!DNL Target] de nuttige lading door gebrek terug, maar in plaats daarvan slechts wanneer gewenst en gespecificeerd.

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

### Stap 8: De implementatie valideren {#step8}

Laad uw pagina&#39;s nadat u de JavaScript-bibliotheken hebt bijgewerkt om te bevestigen dat de `mboxMCSDID`-parameterwaarden in [!DNL Target]-aanroepen overeenkomen met de `sdid`-parameterwaarde in de paginaweergaveaanroep [!DNL Analytics].

Het is vooral belangrijk om te bevestigen dat deze waarden in de Toepassingen van de Enige Pagina (SPA) aanpassen waar de orde van vraag niet altijd voorspelbaar is.

>[!NOTE]
>
>Een4T werkt alleen correct als deze waarden overeenkomen.

### Stap 9: (Optioneel) Vorige integratiecode verwijderen

Adobe raadt u aan de vorige integratie te verwijderen om de implementatie te vereenvoudigen en de verschillen tussen de systemen weg te werken. U kunt om het even welke code verwijderen u voor vorige Sc aan integratie T&amp;T, met inbegrip van `mboxLoadSCPlugin` hebt opgesteld.

### Stap 10: De opties inschakelen voor het gebruik van Analytics als rapportagebron voor Doel

Klik in [!DNL Target] op **[!UICONTROL Administration > Visual Experience Composer]** en kies **[!UICONTROL Select per activity]** of **[!UICONTROL Adobe Analytics]** om de opties in te schakelen.

* **[!UICONTROL Select per activity]** Hiermee kunt u kiezen tussen  [!DNL Target] en  [!DNL Analytics] bij het maken van elke activiteit.
* **[!UICONTROL Adobe Analytics]** Hiermee stelt u  [!DNL Analytics] de rapportbron in voor alle activiteiten die u maakt.


