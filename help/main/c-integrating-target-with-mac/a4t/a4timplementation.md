---
keywords: A4T;Adobe Analytics;Analytics-gebaseerde activiteit;Analytics report suite;report suite;Analytics Target integration;configure report suite;at.js;atjs;adobe Experience platform web sdk;aep web sdk;platform web sdk
description: Volg de stappen worden vereist om Analytics voor  [!DNL Target]  (A4T) in uw oplossingen van Adobe  [!DNL Target]  en van Adobe Analytics uit te voeren die.
title: Hoe voer ik Analytics voor  [!DNL Target]  uit (A4T)?
feature: Analytics for Target (A4T)
exl-id: b5269b9e-01ef-449a-bb03-3dcc2cd68af7
source-git-commit: ddfb06a17a24200b2aa4f01d370cc0e92ff5f180
workflow-type: tm+mt
source-wordcount: '1055'
ht-degree: 0%

---

# Analyses voor [!DNL Target] -implementatie

Er zijn verschillende stappen vereist wanneer u [!DNL Adobe Analytics] implementeert als de rapportbron voor [!DNL Adobe Target] (A4T). Het proces varieert afhankelijk van of u A4T met [[!DNL Adobe Experience Platform Web SDK] uitvoert &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html?lang=nl-NL) of met at.js.

## ![&#x200B; Adobe Experience Platform Web SDK badge &#x200B;](/help/main/assets/platform.png) de stappen van de Implementatie voor een implementatie van SDK van het Web van Adobe Experience Platform {#platform}

De volgende secties beschrijven de stappen die worden vereist om deze integratie aan uw plaats op te stellen als u van plan bent om het Web SDK van het Platform te gebruiken:

### Stap 1: provisioning aanvragen voor [!DNL Analytics] en [!DNL Target]

Voordat u A4T implementeert, moet u provisioned zijn voor [!DNL Analytics] en [!DNL Target] . [&#x200B; Gebruik deze vorm om te verzoeken om worden provisioned &#x200B;](https://survey.adobe.com/jfe/form/SV_ekBHTLSoP5Zki2y).

### Stap 2: Gebruikersmachtigingen instellen

Aan de vereisten voor gebruikersaccounts moet worden voldaan voordat u een activiteit kunt maken op basis van [!DNL Analytics] in [!DNL Target] . Zie [&#x200B; de toestemmingsvereisten van de Gebruiker &#x200B;](/help/main/c-integrating-target-with-mac/a4t/account-reqs.md).

### Stap 3: Een Edge-configuratie maken

Maak een Edge-configuratie met [!DNL Adobe Experience Platform] met het gereedschap voor randconfiguratie. Vorm [&#x200B; creeer en vorm gegevensstromen &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/datastreams/configure.html?lang=nl-NL).

### Stap 4: Installeer en configureer het Platform Web SDK

Beginnen [!DNL Target] ervaringen te leveren en [!DNL Analytics] voor het volgen en analysedoeleinden toe te passen, [&#x200B; installeer &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/installing-the-sdk.html?lang=nl-NL) en [&#x200B; vorm &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/configuring-the-sdk.html?lang=nl-NL) het Web SDK van het Platform op uw plaatspagina&#39;s.

### Stap 5: Schakel de opties voor het gebruik van A4T in

Klik in de [!DNL Target] interface op **[!UICONTROL Administration]** > **[!UICONTROL Visual Experience Composer]** en kies vervolgens **[!UICONTROL Select per activity]** of **[!UICONTROL Adobe Analytics]** .

* In **[!UICONTROL Select per activity]** kunt u bij het maken van elke activiteit kiezen tussen [!DNL Target] en [!DNL Analytics] .
* **[!UICONTROL Adobe Analytics]** stelt [!DNL Analytics] in als de rapportbron voor alle activiteiten die u maakt.

## ![&#x200B; at.js badge &#x200B;](/help/main/assets/atjs.png) de stappen van de Implementatie voor een implementatie at.js{#section_73961BAD5BB4430A95E073DE5C026277}

In de volgende secties worden de stappen beschreven die nodig zijn om deze integratie op uw site te implementeren als u van plan bent om at.js te gebruiken:

### Stap 1: De levering van het verzoek voor Analytics en Doel

Nadat u [!DNL Analytics] hebt geïmplementeerd als de rapportbron voor [!DNL Target] , moet u een provisioning uitvoeren voor [!DNL Analytics] en [!DNL Target] . [&#x200B; Gebruik deze vorm om te verzoeken om worden provisioned &#x200B;](https://survey.adobe.com/jfe/form/SV_ekBHTLSoP5Zki2y){target=_blank}.

### Stap 2: Gebruikersmachtigingen instellen

Aan de vereisten voor gebruikersaccounts moet worden voldaan voordat u een op [!DNL Analytics] gebaseerde activiteit kunt maken in [!DNL Target] . Zie [&#x200B; de toestemmingsvereisten van de Gebruiker &#x200B;](/help/main/c-integrating-target-with-mac/a4t/account-reqs.md).

### Stap 3: Implementeer de Experience Cloud Visitor ID-service

Met de bezoekersidentiteitsservice kunt u gebruikers identificeren in [!DNL Adobe Experience Cloud] -oplossingen. Implementeer of migreer naar de vereiste versie van de Experience Cloud-bezoeker-id. Voor meer informatie, zie &quot;Vereisten van de Uitvoering&quot;in [&#x200B; alvorens u &#x200B;](/help/main/c-integrating-target-with-mac/a4t/before-implement.md) uitvoert.

Zie [&#x200B; de Dienst van identiteitskaart van Experience Cloud voor Doel &#x200B;](https://experienceleague.adobe.com/docs/id-service/using/implementation/setup-target.html?lang=nl-NL) in de *documentatie van de Dienst van identiteitskaart van de Bezoeker van Experience Cloud* uitvoeren.

### Stap 4: AppMeasurement voor JavaScript of s_code bijwerken

Implementeer of migreer naar de vereiste versie van appMeasurement.js. Voor meer informatie, zie &quot;Vereisten van de Uitvoering&quot;in [&#x200B; alvorens u &#x200B;](/help/main/c-integrating-target-with-mac/a4t/before-implement.md) uitvoert.

Voor nieuwe implementaties, zie [&#x200B; JavaScript implementatieoverzicht &#x200B;](https://experienceleague.adobe.com/docs/analytics/implementation/js/overview.html?lang=nl-NL) in de *Gids van de Implementatie van de Analyse*.

Voor een migratie, zie [&#x200B; Migrerend aan AppMeasurement voor JavaScript &#x200B;](https://experienceleague.adobe.com/docs/analytics/implementation/js/migrate-from-hcode.html?lang=nl-NL) in de *Gids van de Implementatie van de Analyse*.

### Stap 5: Download en werk de update om.js bij

Implementeer of migreer naar de vereiste versie van at.js met uw productieaccount. De code hoeft niet te worden gewijzigd.

Voor meer informatie, zie &quot;Vereisten van de Uitvoering&quot;in [&#x200B; alvorens u &#x200B;](/help/main/c-integrating-target-with-mac/a4t/before-implement.md) uitvoert.

### Stap 6: Host at.js

Als u eerder om.js opstelde, kunt u uw bestaand dossier met de bijgewerkte versie vervangen. Voor meer informatie, zie &quot;Vereisten van de Uitvoering&quot;in [&#x200B; alvorens u &#x200B;](/help/main/c-integrating-target-with-mac/a4t/before-implement.md) uitvoert.

Anders kan dit bestand worden gehost samen met de Bezoeker-id-service en AppMeasurement for JavaScript-bestanden. Deze bestanden moeten worden gehost op een webserver die toegankelijk is voor alle pagina&#39;s op uw site. U hebt het pad naar deze bestanden nodig in de volgende stap.

### Stap 7: Verwijzing bij.js op alle plaatspagina&#39;s {#step7}

Neem de code at.js onder VisitorAPI.js op door de volgende coderegel toe te voegen aan de tag op elke pagina:

Voor at.js:

```javascript
<script language="JavaScript" type="text/javascript"
src="http://INSERT-DOMAIN-AND-PATH-TO-CODE-HERE/at.js"></script>
```

De visitorAPI.js moet worden geladen vóór at.js. Als u een bestaand at.js- dossier bijwerkt, zorg ervoor dat u de ladingsorde verifieert.

De standaardinstelling voor [!DNL Target] - en [!DNL Analytics] -integratie vanuit implementatiepunt is dat de SDID die vanuit de pagina wordt doorgegeven, wordt gebruikt om de aanvraag [!DNL Target] en [!DNL Analytics] automatisch aan elkaar te koppelen op de achtergrond.

U kunt bepalen hoe en wanneer u analysegegevens met betrekking tot [!DNL Target] naar [!DNL Analytics] verzendt voor rapportagedoeleinden. Als u niet aan de standaardmontages van het hebben van [!DNL Target] en [!DNL Analytics] wilt kiezen automatisch de analysegegevens via SDID verbinden, plaats **analyticsLogging = client_side** via **window.targetGlobalSettings**. Opmerking: versies onder 2.1 ondersteunen deze aanpak niet.

Bijvoorbeeld:

```javascript
window.targetGlobalSettings = {
  analyticsLogging: "client_side"
};
```

Deze opstelling heeft een globaal effect, zo betekent het dat elke vraag die door at.js wordt gemaakt **analyticsLogging heeft: &quot;client_side&quot;** verzonden binnen de [!DNL Target] verzoeken en een analytische lading is teruggekeerd voor elk verzoek. Als deze optie is ingesteld, ziet de indeling van de geretourneerde lading er als volgt uit:

```javascript
"analytics": {
   "payload": {
      "pe": "tnt",
      "tnta": "167169:0:0|0|100,167169:0:0|2|100,167169:0:0|1|100"
   }
}
```

De nuttige lading kan dan aan Analytics via de [&#x200B; Invoeging API van Gegevens &#x200B;](https://helpx.adobe.com/nl/analytics/kb/data-insertion-api-post-method-adobe-analytics.html) door:sturen. Voor auto-Wijs en auto-Doel activiteiten, moet u sessionId ook door:sturen. Voor meer informatie, zie [&#x200B; Analytics voor Doel (A4T) die &#x200B;](https://experienceleague.adobe.com/docs/target-dev/developer/server-side/integration/a4t-reporting.html?lang=nl-NL){target=_blank} in de *gids SDKs van Adobe Target* melden.

Als het globale plaatsen niet gewenst is en een meer op bestelling benadering verkieslijk is, gebruik de functie at.js [&#x200B; getOffers () &#x200B;](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/functions-overview/adobe-target-getoffers-atjs-2.html?lang=nl-NL){target=_blank} door binnen **analyticsLogging over te gaan: &quot;client_side&quot;**. De payload van de analyse wordt alleen voor deze aanroep geretourneerd en de [!DNL Target] backend stuurt de payload niet door naar [!DNL Analytics] . Door deze benadering na te streven, keert elk verzoek at.js [!DNL Target] de lading door gebrek terug, maar in plaats daarvan slechts wanneer gewenst en gespecificeerd.

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

De nuttige lading kan dan aan [!DNL Analytics] via de [&#x200B; Invoeging API van Gegevens &#x200B;](https://helpx.adobe.com/nl/analytics/kb/data-insertion-api-post-method-adobe-analytics.html) door:sturen.

### Stap 8: De implementatie valideren {#step8}

Laad uw pagina&#39;s nadat u de JavaScript-bibliotheken hebt bijgewerkt om te bevestigen dat de `mboxMCSDID` parameterwaarden in [!DNL Target] -aanroepen overeenkomen met de `sdid` -parameterwaarde in de [!DNL Analytics] page-view aanroep.

Het is vooral belangrijk om te bevestigen dat deze waarden in Enige Toepassingen van de Pagina (SPAs) aanpassen waar de orde van vraag niet altijd voorspelbaar is.

>[!NOTE]
>
>Een4T werkt alleen correct als deze waarden overeenkomen.

### Stap 9: (Optioneel) Verwijder vorige integratiecode

Adobe raadt u aan de vorige integratie te verwijderen om de implementatie te vereenvoudigen en de verschillen tussen de systemen weg te werken. U kunt alle code verwijderen die u hebt geïmplementeerd voor een vorige integratie van SC naar T&amp;T, inclusief `mboxLoadSCPlugin` .

### Stap 10: Laat de opties toe om Analytics als rapporteringsbron voor Doel te gebruiken

Klik in [!DNL Target] op **[!UICONTROL Administration > Reporting]** en kies **[!UICONTROL Select per activity]** of **[!UICONTROL Adobe Analytics]** om de opties in te schakelen.

* In **[!UICONTROL Select per activity]** kunt u bij het maken van elke activiteit kiezen tussen [!DNL Target] en [!DNL Analytics] .
* **[!UICONTROL Adobe Analytics]** stelt [!DNL Analytics] in als de rapportbron voor alle activiteiten die u maakt.


