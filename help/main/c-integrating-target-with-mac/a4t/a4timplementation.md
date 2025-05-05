---
keywords: A4T;Adobe Analytics;Analytics-gebaseerde activiteit;Analytics report suite;report suite;Analytics Target integration;configure report suite;at.js;atjs;adobe Experience platform web sdk;aep web sdk;platform web sdk
description: Voer de stappen uit die nodig zijn voor het implementeren van Analytics voor [!DNL Target] (A4T) in uw Adobe [!DNL Target] en Adobe Analytics-oplossingen.
title: Hoe kan ik Analyses implementeren voor [!DNL Target] (A4T)?
feature: Analytics for Target (A4T)
exl-id: b5269b9e-01ef-449a-bb03-3dcc2cd68af7
source-git-commit: ddfb06a17a24200b2aa4f01d370cc0e92ff5f180
workflow-type: tm+mt
source-wordcount: '1055'
ht-degree: 0%

---

# Analyses voor [!DNL Target] uitvoering

Bij de implementatie zijn verschillende stappen vereist [!DNL Adobe Analytics] als bron van rapportage voor [!DNL Adobe Target] (A4T). Het proces varieert afhankelijk van of u A4T met [[!DNL Adobe Experience Platform Web SDK]](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html?lang=nl-NL) of met at.js.

## ![Adobe Experience Platform Web SDK-badge](/help/main/assets/platform.png) Implementatiestappen voor een Adobe Experience Platform Web SDK-implementatie {#platform}

De volgende secties beschrijven de stappen die worden vereist om deze integratie aan uw plaats op te stellen als u van plan bent om het Web SDK van het Platform te gebruiken:

### Stap 1: provisioning aanvragen voor [!DNL Analytics] en [!DNL Target]

Voordat u A4T implementeert, moet u provisioning uitvoeren voor [!DNL Analytics] en [!DNL Target]. [Gebruik dit formulier om provisioning aan te vragen](https://survey.adobe.com/jfe/form/SV_ekBHTLSoP5Zki2y).

### Stap 2: Gebruikersmachtigingen instellen

Aan de vereisten voor gebruikersaccounts moet worden voldaan voordat u een activiteit kunt maken op [!DNL Analytics] in [!DNL Target]. Zie [Vereisten voor gebruikerstoegang](/help/main/c-integrating-target-with-mac/a4t/account-reqs.md).

### Stap 3: Een Edge-configuratie maken

Een Edge-configuratie maken met [!DNL Adobe Experience Platform] met het gereedschap voor randconfiguratie. Vorm [Gegevensstromen maken en configureren](https://experienceleague.adobe.com/docs/experience-platform/datastreams/configure.html?lang=nl-NL).

### Stap 4: Installeer en vorm de SDK van het Web Platform

Beginnen met leveren [!DNL Target] ervaringen en toepassing [!DNL Analytics] voor tracerings- en analysedoeleinden, [Installeren](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/installing-the-sdk.html?lang=nl-NL) en [vormen](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/configuring-the-sdk.html?lang=nl-NL) de SDK van het Web van het Platform op uw plaatspagina&#39;s.

### Stap 5: Schakel de opties voor het gebruik van A4T in

In de [!DNL Target] UI, klik **[!UICONTROL Administration]** > **[!UICONTROL Visual Experience Composer]** kiest u vervolgens **[!UICONTROL Select per activity]** of **[!UICONTROL Adobe Analytics]**.

* **[!UICONTROL Select per activity]** laat u kiezen tussen [!DNL Target] en [!DNL Analytics] bij het maken van elke activiteit.
* **[!UICONTROL Adobe Analytics]** sets [!DNL Analytics] als de rapportbron voor alle activiteiten die u maakt.

## ![at.js badge](/help/main/assets/atjs.png) Implementatiestappen voor de implementatie van een at.js{#section_73961BAD5BB4430A95E073DE5C026277}

In de volgende secties worden de stappen beschreven die nodig zijn om deze integratie op uw site te implementeren als u van plan bent om at.js te gebruiken:

### Stap 1: De levering van het verzoek voor Analytics en Doel

Na de implementatie [!DNL Analytics] als bron van rapportage voor [!DNL Target], moet u zijn ingericht voor [!DNL Analytics] en [!DNL Target]. [Gebruik dit formulier om provisioning aan te vragen](https://survey.adobe.com/jfe/form/SV_ekBHTLSoP5Zki2y){target=_blank}.

### Stap 2: Gebruikersmachtigingen instellen

Aan de vereisten voor gebruikersaccounts moet worden voldaan voordat u een [!DNL Analytics]-gebaseerde activiteit in [!DNL Target]. Zie [Vereisten voor gebruikerstoegang](/help/main/c-integrating-target-with-mac/a4t/account-reqs.md).

### Stap 3: Voer de dienst van identiteitskaart van de Bezoeker van het Experience Cloud uit

Met de bezoekersidentiteitsservice kunt u gebruikers overal herkennen [!DNL Adobe Experience Cloud] oplossingen. Implementeer of migreer naar de vereiste versie van de Experience Cloud Bezoeker-id. Zie &quot;Implementatievereisten&quot; in [Voordat u implementeert](/help/main/c-integrating-target-with-mac/a4t/before-implement.md).

Zie [Voer de Dienst van identiteitskaart van het Experience Cloud voor Doel uit](https://experienceleague.adobe.com/docs/id-service/using/implementation/setup-target.html?lang=nl-NL) in de *Experience Cloud Visitor ID Service* documentatie.

### Stap 4: AppMeasurement voor JavaScript of s_code bijwerken

Implementeer of migreer naar de vereiste versie van appMeasurement.js. Zie &quot;Implementatievereisten&quot; in [Voordat u implementeert](/help/main/c-integrating-target-with-mac/a4t/before-implement.md).

Zie voor nieuwe implementaties [Overzicht van JavaScript-implementatie](https://experienceleague.adobe.com/docs/analytics/implementation/js/overview.html?lang=nl-NL) in de *Handleiding voor analytische implementatie*.

Voor een migratie raadpleegt u [Migreren naar AppMeasurement voor JavaScript](https://experienceleague.adobe.com/docs/analytics/implementation/js/migrate-from-hcode.html?lang=nl-NL) in de *Handleiding voor analytische implementatie*.

### Stap 5: Download en werk de update om.js bij

Implementeer of migreer naar de vereiste versie van at.js met uw productieaccount. De code hoeft niet te worden gewijzigd.

Zie &quot;Implementatievereisten&quot; in [Voordat u implementeert](/help/main/c-integrating-target-with-mac/a4t/before-implement.md).

### Stap 6: Host at.js

Als u eerder om.js opstelde, kunt u uw bestaand dossier met de bijgewerkte versie vervangen. Zie &quot;Implementatievereisten&quot; in [Voordat u implementeert](/help/main/c-integrating-target-with-mac/a4t/before-implement.md).

Anders kan dit bestand samen met de bezoekersidentiteitsservice en het AppMeasurement voor JavaScript-bestanden worden gehost. Deze bestanden moeten worden gehost op een webserver die toegankelijk is voor alle pagina&#39;s op uw site. U hebt het pad naar deze bestanden nodig in de volgende stap.

### Stap 7: Verwijzing bij.js op alle plaatspagina&#39;s {#step7}

Neem de code at.js onder VisitorAPI.js op door de volgende coderegel toe te voegen aan de tag op elke pagina:

Voor at.js:

```javascript
<script language="JavaScript" type="text/javascript"
src="http://INSERT-DOMAIN-AND-PATH-TO-CODE-HERE/at.js"></script>
```

De visitorAPI.js moet worden geladen vóór at.js. Als u een bestaand at.js- dossier bijwerkt, zorg ervoor dat u de ladingsorde verifieert.

De standaardinstelling voor [!DNL Target] en [!DNL Analytics] vanuit het perspectief van de implementatie moet de SDID die van de pagina is doorgegeven, worden gebruikt om de [!DNL Target] en [!DNL Analytics] automatisch op de achtergrond samen aanvragen.

U kunt bepalen hoe en wanneer u analysegegevens verzendt met betrekking tot [!DNL Target] tot [!DNL Analytics] voor rapportagedoeleinden. Als u zich niet wilt aanmelden bij de standaardinstellingen van [!DNL Target] en [!DNL Analytics] De analysegegevens automatisch koppelen via de SDID, instellen **analyticsLogging = client_side** via **window.targetGlobalSettings**. Opmerking: versies onder 2.1 ondersteunen deze aanpak niet.

Bijvoorbeeld:

```javascript
window.targetGlobalSettings = {
  analyticsLogging: "client_side"
};
```

Deze opzet heeft een mondiaal effect, wat betekent dat elke oproep van at.js **analyticsLogging: &quot;client_side&quot;** verzonden binnen de [!DNL Target] verzoeken en een analytische lading is teruggekeerd voor elk verzoek. Als deze optie is ingesteld, ziet de indeling van de geretourneerde lading er als volgt uit:

```javascript
"analytics": {
   "payload": {
      "pe": "tnt",
      "tnta": "167169:0:0|0|100,167169:0:0|2|100,167169:0:0|1|100"
   }
}
```

De lading kan dan aan Analytics via [API voor gegevensinvoer](https://helpx.adobe.com/nl/analytics/kb/data-insertion-api-post-method-adobe-analytics.html). Voor auto-Wijs en auto-Doel activiteiten, moet u sessionId ook door:sturen. Zie voor meer informatie [Analyses voor doelrapportage (A4T)](https://experienceleague.adobe.com/docs/target-dev/developer/server-side/integration/a4t-reporting.html?lang=nl-NL){target=_blank} in de *Adobe Target SDK&#39;s* hulplijn.

Als een globale instelling niet gewenst is en een meer on-demand aanpak de voorkeur verdient, gebruikt u de functie at.js [getOffers()](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/functions-overview/adobe-target-getoffers-atjs-2.html?lang=nl-NL){target=_blank} door **analyticsLogging: &quot;client_side&quot;**. De analytische lading is teruggekeerd voor deze vraag slechts en [!DNL Target] backend stuurt niet de lading door aan [!DNL Analytics]. Door deze benadering na te streven, om de [!DNL Target] request retourneert standaard de payload, maar alleen wanneer gewenst en opgegeven.

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

De lading kan dan door:sturen aan [!DNL Analytics] via de [API voor gegevensinvoer](https://helpx.adobe.com/nl/analytics/kb/data-insertion-api-post-method-adobe-analytics.html).

### Stap 8: De implementatie valideren {#step8}

Laad uw pagina&#39;s nadat u de JavaScript-bibliotheken hebt bijgewerkt om te bevestigen dat de `mboxMCSDID` parameterwaarden in [!DNL Target] de vraag past aan `sdid` parameterwaarde in de [!DNL Analytics] paginaweergaveaanroep.

Het is vooral belangrijk om te bevestigen dat deze waarden in de Toepassingen van de Enige Pagina (SPA) aanpassen waar de orde van vraag niet altijd voorspelbaar is.

>[!NOTE]
>
>Een4T werkt alleen correct als deze waarden overeenkomen.

### Stap 9: (Optioneel) Verwijder vorige integratiecode

Adobe raadt u aan de vorige integratie te verwijderen om de implementatie te vereenvoudigen en de verschillen tussen de systemen weg te werken. U kunt om het even welke code verwijderen u voor een vorige integratie van Sc aan T&amp;T, met inbegrip van hebt opgesteld `mboxLoadSCPlugin`.

### Stap 10: Laat de opties toe om Analytics als rapporteringsbron voor Doel te gebruiken

In [!DNL Target], klikt u op **[!UICONTROL Administration > Reporting]** en kiest u **[!UICONTROL Select per activity]** of **[!UICONTROL Adobe Analytics]** om de opties in te schakelen.

* **[!UICONTROL Select per activity]** laat u kiezen tussen [!DNL Target] en [!DNL Analytics] bij het maken van elke activiteit.
* **[!UICONTROL Adobe Analytics]** sets [!DNL Analytics] als de rapportbron voor alle activiteiten die u maakt.


