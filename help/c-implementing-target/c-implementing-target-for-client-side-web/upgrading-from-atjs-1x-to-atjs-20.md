---
keywords: at.js releases;at.js versions;single page app;spa;cross domain;cross-domain
description: Gedetailleerde informatie over het upgraden vanaf Adobe Target op 0.js 1.*x* naar at.js versie 2.0.0
title: Voer een upgrade uit van Adobe Target op.js versie 1.*x* naar at.js versie 2.*x*
feature: at.js
translation-type: tm+mt
source-git-commit: 6bb75e3b818a71af323614d9150e50e3e9f611b7
workflow-type: tm+mt
source-wordcount: '2735'
ht-degree: 0%

---


# Upgrade uitvoeren vanaf 0,js 1.** xto om.js 2.*x* {#upgrading-from-atjs-1x-to-atjs-200}

De nieuwste versie van at.js in [!DNL Adobe Target] verstrekt rijke eigenschapreeksen die uw zaken uitrusten om verpersoonlijking op volgende-generatie, cliënt-zijtechnologieën uit te voeren. Deze nieuwe versie is gericht op het upgraden van at.js voor harmonieuze interacties met toepassingen van één pagina (SPA).

Hier volgen enkele voordelen van het gebruik van at.js 2.** xdie niet beschikbaar zijn in vorige versies:

* De capaciteit om alle aanbiedingen op pagina-lading in het voorgeheugen onder te brengen om veelvoudige servervraag aan één enkele servervraag te verminderen.
* Verbeter de ervaringen van uw eindgebruikers op uw site aanzienlijk, omdat aanbiedingen direct via het cachegeheugen worden weergegeven zonder vertraging die traditionele serveraanroepen introduceren.
* Eenvoudige one-line code en eenmalige ontwikkelaarsopstelling om uw marketers toe te laten om A/B en XT activiteiten via VEC op uw SPA tot stand te brengen en in werking te stellen.

## te.js 2.*Diagrammen* van het xsystem

De volgende diagrammen helpen u het werkschema van at.js 2 begrijpen.** Met weergaven en hoe dit de integratie van de SPA verbetert. Een betere introductie van de concepten die worden gebruikt in at.js 2.*x*, zie de implementatie [ van de Toepassing van de ](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/target-atjs-single-page-application.md)Enige Pagina.

![Doelstroom met at.js 2.*x*](/help/c-implementing-target/c-implementing-target-for-client-side-web/assets/system-diagram-atjs-20.png)

| Bellen | Details |
| --- | --- |
| 3 | De vraag keert [!DNL Experience Cloud ID] terug als de gebruiker voor authentiek wordt verklaard; een andere vraag synchroniseert de klant identiteitskaart |
| 2 | De bibliotheek at.js wordt synchroon geladen en de hoofdtekst van het document verborgen.<br>at.js kan ook asynchroon worden geladen met een optie die fragment verbergt dat op de pagina is geïmplementeerd. |
| 3 | Er wordt een aanvraag voor het laden van een pagina ingediend, inclusief alle geconfigureerde parameters (MCID, SDID en klant-id). |
| 4 | Profielscripts worden uitgevoerd en vervolgens toegevoegd aan de profielenwinkel. De winkel vraagt om gekwalificeerd publiek uit de Audience Library (bijvoorbeeld publiek dat wordt gedeeld vanuit Adobe Analytics, Publiek beheer, enz.).<br>Klantkenmerken worden in een batchproces naar de profielopslag verzonden. |
| 5 | Op basis van URL-aanvraagparameters en -profielgegevens bepaalt [!DNL Target] welke activiteiten en ervaringen moeten worden geretourneerd naar de bezoeker voor de huidige pagina en de toekomstige weergaven. |
| 6 | Gerichte inhoud wordt teruggestuurd naar de pagina, waarbij eventueel ook profielwaarden voor extra personalisatie worden opgenomen.<br>Gerichte inhoud op de huidige pagina wordt zo snel mogelijk zichtbaar zonder flikkering van de standaardinhoud.<br>Gerichte inhoud voor meningen die als resultaat aan gebruikersacties in een SPA worden getoond die in browser caching is zodat kan het onmiddellijk zonder een extra servervraag worden toegepast wanneer de meningen door worden teweeggebracht  `triggerView()`. |
| 7 | De analysegegevens worden verzonden naar de servers van de Inzameling van Gegevens. |
| 8 | De gerichte gegevens worden aangepast aan de analysegegevens via SDID en worden verwerkt in de analytische rapporteringsopslag.<br>De analysegegevens kunnen dan in zowel Analytics als Doel via Analytics voor de rapporten van het Doel (A4T) worden bekeken. |

Nu, waar `triggerView()` op uw SPA wordt uitgevoerd, worden de Meningen en de acties teruggewonnen van geheim voorgeheugen en aan de gebruiker getoond zonder een servervraag. `triggerView()` doet ook een verzoek om meldingen aan de  [!DNL Target] achterzijde om het aantal puntjes op de i te zetten en opnamen te maken.

![Doelstroom bij.js 2.** xtriggerView](/help/c-implementing-target/c-implementing-target-for-client-side-web/assets/atjs-20-triggerview.png)

| Bellen | Details |
| --- | --- |
| 3 | `triggerView()` wordt opgeroepen in de SPA om de weergave te renderen en acties toe te passen om visuele elementen te wijzigen. |
| 2 | De gerichte inhoud voor de mening wordt gelezen van het geheime voorgeheugen. |
| 3 | Gerichte inhoud wordt zo snel mogelijk zichtbaar zonder flikkering van de standaardinhoud. |
| 4 | Het verzoek om een melding wordt verzonden naar de [!DNL Target] Opslag van het Profiel om de bezoeker in de activiteit en verhogingsmetriek te tellen. |
| 5 | Analytische gegevens die naar de Servers van de Inzameling van Gegevens worden verzonden. |
| 6 | De doelgegevens worden via de SDID aangepast aan de analysegegevens en worden verwerkt in de analytische rapportageopslag. De analysegegevens kunnen dan in zowel Analytics als Doel via A4T- rapporten worden bekeken. |

## Implementeer om.js 2.*x* {#deploy-atjs-200}

1. Implementeer om.js 2.** xvia de  [Adobe ](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/cmp-implementing-target-using-adobe-launch.md) Launchextension.

   >[!NOTE]
   >
   > Het implementeren van at.js met behulp van Adobe Launch heeft de voorkeur.

   of

   Handmatig downloaden om.js 2.*Het* gebruiken van het Doel UI en stelt het op gebruikend de  [methode van uw keus](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/how-to-deployatjs.md).

## Vervangen at.js-functies

Er zijn verschillende functies die zijn vervangen in at.js 2.*x*.

>[!IMPORTANT]
>
>Als deze vervangen functies nog steeds op uw site worden gebruikt wanneer at.js 2.** xis opgesteld, zult u consolewaarschuwingen zien. De aanbevolen aanpak bij de upgrade is het testen van de implementatie van at.js 2.** xin een het opvoeren milieu en zorg ervoor om door elk te gaan en elke waarschuwing die in de console is geregistreerd en vertalen de vervangen functies aan nieuwe functies die in at.js 2 worden geïntroduceerd.*x*.

U kunt de vervangen functies en hun tegenhanger hieronder vinden. Voor een volledige lijst van functies, zie [at.js functies](/help/c-implementing-target/c-implementing-target-for-client-side-web/cmp-atjs-functions.md).

>[!NOTE]
>te.js 2.** Hiermee worden  `mboxDefault` gemarkeerde elementen niet meer automatisch vooraf verborgen. Klanten moeten daarom de vooraf verborgen logica handmatig op de site of via een tagmanager kunnen gebruiken.

### mboxCreate(mbox,params)

**Omschrijving**:

Voert een verzoek uit en past de aanbieding op dichtstbijzijnde DIV met de `mboxDefault` klassennaam toe.

**Voorbeeld**:

```
<div class="mboxDefault">
  default content to replace by offer
</div>
<script>
  mboxCreate('mboxName','param1=value1','param2=value2');
</script>
```

**te.js 2.** xequivalent**

Een alternatief voor `mboxCreate(mbox, params)` is `getOffer()` en `applyOffer()`.

**Voorbeeld**:

```
<div class="mboxDefault"> 
  default content to replace by offer 
</div> 
<script> 
  var el = document.currentScript.previousElementSibling;
  adobe.target.getOffer({
    mbox: "mboxName",
    params: {
      param1: "value1",
      param2: "value2"
    },
    success: function(offer) {
      adobe.target.applyOffer({
        mbox: "mboxName",
        selector: el,
        offer: offer
      });
    },
    error: function(error) {
      console.error(error);
      el.style.visibility = "visible";
    }
  });
</script> 
```

### mboxDefine() en mboxUpdate()

**Omschrijving**:

Maakt een interne toewijzing tussen een element en een naam van een box, maar voert de aanvraag niet uit. Wordt gebruikt in combinatie met `mboxUpdate()`, die het verzoek uitvoert en de aanbieding op het element toepast dat door nodeId in `mboxDefine()` wordt geïdentificeerd. Kan ook worden gebruikt om een mbox bij te werken die door `mboxCreate` in werking wordt gesteld.

**Voorbeeld**:

```
<div id="someId" class="mboxDefault"></div>
<script>
 mboxDefine('someId','mboxName','param1=value1','param2=value2');
 mboxUpdate('mboxName','param3=value3','param4=value4');
</script>
```

**te.js 2.** xequivalent**:

Een alternatief voor `mboxDefine()` en `mboxUpdate` is `getOffer()` en `applyOffer()`, met de selecteursoptie die in `applyOffer()` wordt gebruikt. Met deze methode kunt u de aanbieding aan een element toewijzen met elke CSS-kiezer, niet alleen met een id.

**Voorbeeld**:

```
<div id="someId" class="mboxDefault"> 
  default content to replace by offer 
</div> 
<script> 
  adobe.target.getOffer({
    mbox: "mboxName",
    params: {
      param1: "value1",
      param2: "value2",
      param3: "value3",
      param4: "value4" 
    },
    success: function(offer) {
      adobe.target.applyOffer({
        mbox: "mboxName",
        selector: "#someId",
        offer: offer
      });
    },
    error: function(error) {
      console.error(error);
      var el = document.getElementById("someId");
      el.style.visibility = "visible";
    }
  });
</script>
```

### adobe.target.registerExtension()

**Omschrijving**:

Verstrekt een standaardmanier om een specifieke uitbreiding te registreren.

Dit wordt niet meer ondersteund en mag niet worden gebruikt.

## Overzicht van vervangen, nieuwe en ondersteunde at.js-functies in 2.*x*

| Methode | Ondersteund? | Nieuw? | Vervangen?<br>(Standaardinhoud wordt weergegeven) |
| --- | --- | --- | --- |
| `getOffer()` | Ja |  |  |
| `getOffers()` |  | Ja |  |
| `applyOffer()` | Ja |  |  |
| `applyOffers()` |  | Ja |  |
| `triggerView()` |  | Ja |  |
| `trackEvent()` | Ja |  |  |
| `mboxCreate()` |  |  | Ja |
| `mboxDefine()`<br>`mboxUpdate()` |  |  | Ja |
| `targetGlobalSettings()` | Ja |  |  |
| `Data Providers` | Ja |  |  |
| `targetPageParams()` | Ja |  |  |
| `targetPageParamsAll()` | Ja |  |  |
| `registerExtension()` |  |  | Ja |
| `At.js Custom Events` | Ja |  |  |

## Beperkingen en callouts

Houd rekening met de volgende beperkingen en bijschriften:

### Conversie bijhouden

Klanten die `mboxCreate()` gebruiken voor het bijhouden van conversies, moeten `trackEvent()` of `getOffer()` gebruiken.

### Levering aanbieden

Klanten die `mboxCreate()` niet vervangen door `getOffer()` of `applyOffer()`, lopen het risico dat er geen aanbiedingen worden geleverd.

### Mag om.js 2.*Op sommige pagina&#39;s* wordt xbe gebruikt en op 0,js 1.*Wilt* u xor mbox.js op andere pagina&#39;s plaatsen?

Ja, het bezoekersprofiel blijft op alle pagina&#39;s behouden met behulp van verschillende versies en bibliotheken. De cookieindeling is hetzelfde.

### Nieuw API-gebruik in at.js 2.*x*

te.js 2.*Er wordt* een nieuwe API gebruikt, die we de API voor levering noemen. Om te zuiveren of at.js [!DNL Target] randserver correct roept, kunt u het lusje van het Netwerk van de Hulpmiddelen van de Ontwikkelaar van uw browser aan &quot;levering&quot;, &quot;`tt.omtrdc.net`,&quot;of uw cliëntcode filtreren. U zult ook merken dat [!DNL Target] een JSON nuttige lading in plaats van sleutel-waardeparen verzendt.

### Globale doelbox wordt niet meer gebruikt

In at.js 2.*x*, ziet u niet meer &quot;`target-global-mbox`&quot;zichtbaar in de netwerkvraag. In plaats daarvan hebben we de syntaxis &quot;`target-global-mbox`&quot; vervangen in &quot;`execute > pageLoad`&quot; in de JSON-payload die naar de [!DNL Target]-servers is verzonden, zoals hieronder wordt getoond:

```
{
  "id": {
    // ...
  },
  "context": {
    "channel": "web",
    // ...
  },
  "execute": {
    "pageLoad": {}
  }
}
```

In wezen is het algemene mbox-concept geïntroduceerd om [!DNL Target] te laten weten of aanbiedingen en inhoud moeten worden opgehaald tijdens het laden van de pagina. Daarom hebben we dit in onze nieuwste versie duidelijker gemaakt.

### Maakt de globale naam van de box in at.js nog uit?

Klanten kunnen een algemene naam voor een box opgeven via [!UICONTROL Target > Administration > Implementation > Edit at.js Settings]. Deze instelling wordt door de Edge-servers [!DNL Target] gebruikt om uitvoering > pageLoad om te zetten in de algemene naam van het selectievakje die wordt weergegeven in de gebruikersinterface [!DNL Target]. Hierdoor kunnen klanten API&#39;s aan de serverzijde, de op formulieren gebaseerde composer, profielscripts blijven gebruiken en een publiek maken met de algemene mbox-naam. Wij adviseren sterk dat u ook ervoor zorgt de zelfde globale naam van mbox op de [!UICONTROL Administration > Visual Experience Composer] pagina wordt gevormd, eveneens voor het geval u nog pagina&#39;s hebt die at.js 1 gebruiken.** xor mbox.js, zoals in de volgende afbeeldingen wordt getoond.

![Dialoogvenster Wijzigen bij.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/assets/modify-atjs.png)

en

![Aangepaste algemene mbox](/help/c-implementing-target/c-implementing-target-for-client-side-web/assets/custom-global-mbox.png)

### Moet de instelling voor automatisch maken van globale mbox worden ingeschakeld voor at.js 2.*x*?

In de meeste gevallen ja. Deze instelling vertelt at.js 2.*Voer* een aanvraag uit bij de  [!DNL Target] Edge-servers wanneer de pagina wordt geladen. Omdat globale mbox wordt vertaald om uit te voeren > pageLoad, en als u een verzoek op paginading wilt in werking stellen, dan zou deze het plaatsen moeten zijn.

### Zal de bestaande activiteiten VEC blijven werken, hoewel de doel globale mbox naam niet van at.js 2 wordt gespecificeerd.*x*?

Ja, omdat execute > pageLoad op de [!DNL Target] backend zoals `target-global-mbox` wordt behandeld.

### Als mijn op vorm-gebaseerde activiteiten aan `target-global-mbox` worden gericht, zullen die activiteiten blijven werken?

Ja, omdat execute > pageLoad op de [!DNL Target] Edge-servers wordt behandeld zoals `target-global-mbox`.

### Ondersteund en niet-ondersteund at.js 2.** xSettings

| Instelling | Ondersteund? |
| --- | --- |
| X-domein | Nee |
| Globale box automatisch maken | Ja |
| Algemene naam van box | Ja |

### Ondersteuning voor interdomeintracering in at.js 2.x {#cross-domain}

Met interdomeinspatiëring kunt u bezoekers aan elkaar koppelen in verschillende domeinen. Omdat voor elk domein een nieuwe cookie moet worden gemaakt, is het moeilijk bezoekers bij te houden wanneer ze van domein naar domein navigeren. [!DNL Target] gebruikt een cookie van een andere fabrikant om bezoekers in verschillende domeinen te volgen. Hierdoor kunt u een doelactiviteit maken die `siteA.com` en `siteB.com` omvat en bezoekers in dezelfde ervaring blijven wanneer ze door unieke domeinen navigeren. Deze functionaliteit is verbonden met het gedrag van cookies van derden en van andere bedrijven.

>[!NOTE]
>
>Uit het vak in at.js 2 wordt geen ondersteuning geboden voor het bijhouden van domeinoverschrijdingen.*x*. Interdomeintracering wordt ondersteund in at.js 2.** xvia de Experience Cloud ID-bibliotheek v4.3.0+.

Bij Doel wordt het cookie van de andere fabrikant opgeslagen in `<CLIENTCODE>.tt.omtrdc.net`. Het cookie van de eerste partij wordt opgeslagen in `clientdomain.com`. De eerste aanvraag retourneert HTTP-antwoordheaders die proberen cookies van derden met de naam `mboxSession` en `mboxPC` in te stellen, terwijl een omleidingsverzoek wordt teruggestuurd met een extra parameter (`mboxXDomainCheck=true`). Als de browser cookies van derden accepteert, bevat de omleidingsaanvraag deze cookies en wordt de ervaring geretourneerd. Dit werkschema is mogelijk omdat wij de methode van de GET van HTTP gebruiken.

In punt 2.js.*x*, wordt de GET van HTTP niet meer gebruikt en in plaats daarvan gebruiken wij de POST van HTTP. HTTP-POST wordt nu gebruikt via at.js 2.** xto verzendt JSON-ladingen naar Target Edge-servers. Dit betekent dat de omleidingsaanvraag om te controleren of een browser cookies van derden ondersteunt, nu wordt afgebroken. Dit komt doordat HTTP-GET-aanvragen epidemiologische transacties zijn, terwijl HTTP-POST niet-epidemiologisch is en niet willekeurig mag worden herhaald. Daarom is het volgen tussen domeinen in at.js 2.*Het* tekstvak wordt niet meer ondersteund. Alleen om.js 1.*Ondersteuning voor* xhas out-of-the-box voor cross-domain tracking.

Als u interdomeintracering wilt gebruiken, moet u de [ECID-bibliotheek v4.3.0+](https://experienceleague.adobe.com/docs/id-service/using/release-notes/release-notes.html) in combinatie met at.js 2 installeren.*x*. De ECID-bibliotheek bestaat voor het beheer van permanente id&#39;s waarmee een bezoeker zelfs in verschillende domeinen kan worden geïdentificeerd.

>[!NOTE]
>
>Na installatie van de ECID-bibliotheek v4.3.0+ en at.js 2.*x*, zult u activiteiten kunnen tot stand brengen die unieke domeinen evenals spoorgebruikers omspannen. Het is belangrijk om op te merken dat deze functionaliteit slechts werkt nadat de zitting verloopt.

### Automatisch globale box maken wordt ondersteund

Deze instelling vertelt at.js 2.*Voer* een aanvraag uit naar de  [!DNL Target] Edge-servers bij het laden van de pagina. Omdat het globale mbox wordt vertaald om > pageLoad uit te voeren, en dit door de [!DNL Target] randservers wordt geïnterpreteerd, zouden de klanten dit moeten aanzetten als zij een verzoek op pagina-lading willen in brand steken.

### Algemene naam van box wordt ondersteund

Klanten kunnen een algemene naam voor een box opgeven via [!UICONTROL Target > Administration > Implementation > Edit]. Deze instelling wordt door de Edge-servers [!DNL Target] gebruikt om uitvoering > pageLoad om te zetten in de ingevoerde algemene naam van het invoervak. Hierdoor kunnen klanten API&#39;s aan de serverzijde, de op formulieren gebaseerde composer, profielscripts blijven gebruiken en een publiek maken dat zich richt op de algemene box.

### Zijn de onderstaande aangepaste gebeurtenissen at.js van toepassing op `triggerView()` of alleen voor `applyOffer()` of `applyOffers()`?

* `adobe.target.event.CONTENT_RENDERING_FAILED`
* `adobe.target.event.CONTENT_RENDERING_SUCCEEDED`
* `adobe.target.event.CONTENT_RENDERING_NO_OFFERS`
* `adobe.target.event.CONTENT_RENDERING_REDIRECT`

Ja zijn de aangepaste gebeurtenissen at.js ook van toepassing op `triggerView()`.

### Er staat: wanneer ik `triggerView()` aanroep met &amp;accolade;`“page” : “true”`&amp;break; er wordt een melding verzonden naar de [!DNL Target]-achterkant en de indruk vergroot. Zorgt het er ook voor dat de profielscripts worden uitgevoerd?

Wanneer een prefetch vraag aan [!DNL Target] achterkant wordt gemaakt, worden de profielmanuscripten uitgevoerd. Daarna worden de profielgegevens gecodeerd en teruggestuurd naar de clientzijde. Nadat `triggerView()` met `{"page": "true"}` wordt aangehaald, wordt een bericht verzonden samen met de gecodeerde profielgegevens. Dit is wanneer de [!DNL Target] backend dan de profielgegevens zal decrypteren en in de gegevensbestanden zal opslaan.

### Moeten wij pre-verbergende code toevoegen alvorens `triggerView()` te roepen om flikkering te beheren?

Nee, u hoeft geen code toe te voegen die zich voor het verbergen van objecten bevindt voordat u `triggerView()` aanroept. te.js 2.*Beheert* de logica voor het vooraf verbergen en flikkeren voordat de weergave wordt weergegeven en toegepast.

### welke om.js 1.** xparameters voor het maken van soorten publiek worden niet ondersteund in at.js 2.*x*?  {#audience-parameters}

De volgende parameters at.js 1.x worden *NOT* momenteel gesteund voor publieksverwezenlijking wanneer het gebruiken van at.js 2.*x*:

* browserHeight
* browserWidth
* browserTimeOffset
* screenHeight
* screenWidth
* screenOrientation
* colorDepth
* devicePixelRatio

## at.js-compatibiliteit

In de volgende tabellen wordt om .js uitgelegd. 2.*x* compatibiliteit met verschillende activiteitstypen, integraties, functies en at.js-functies.

### Activiteitstypen {#types}

| Type | Ondersteund? |
| --- | --- |
| A/B-test | Ja |
| Automatisch toewijzen | Ja |
| Automatisch doel | Ja |
| Gericht op ervaring | Ja |
| Multivariatietest | Ja |
| Automated Personalization | Ja |
| Recommendations | Ja |

>[!NOTE]
>
>Auto-Target activiteiten worden gesteund door at.js 2.*VEC* uitbreiden wanneer alle wijzigingen op het  `Page Load Event`bestand worden toegepast. Als er wijzigingen worden toegevoegd aan bepaalde weergaven, worden alleen de activiteiten A/B Test, Auto-Allocate en Experience Targeting (XT) ondersteund.

### Integratie {#integrations}

| Type | Ondersteund? |
| --- | --- |
| Analyses voor doel (A4T) | Ja |
| Soorten publiek | Ja |
| Klantkenmerken | Ja |
| Fragmenten voor AEM | Ja |
| Adobe-extensie starten | [Ja](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/cmp-implementing-target-using-adobe-launch.md) |
| Foutopsporing | Ja |
| Auditor | De regels zijn nog niet bijgewerkt voor om.js 2.*x* |
| Dynamisch tagbeheer (DTM) | Ja |
| Inschakelen | Nee. Ondersteuning voor aanmelden voor [GDPR](/help/c-implementing-target/c-considerations-before-you-implement-target/c-privacy/cmp-privacy-and-general-data-protection-regulation.md) wordt ondersteund in [at.js versie 2.1.0](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md). |
| AEM verbeterde personalisatie door Adobe Target | Nee |

### Functies

| Functie | Ondersteund? |
| --- | --- |
| X-domein | Nee |
| Eigenschappen/werkruimten | Ja |
| QA-koppelingen | Ja |
| Form-based Experience Composer | Ja |
| Visual Experience Composer (VEC) | Ja |
| Aangepaste code | Ja |
| Reactietokens | [Ja](#response-tokens) |
| Klikken en bijhouden | Ja |
| Levering van meerdere activiteiten | Ja |
| targetGlobalSettings | Ja (maar niet x-domain) |
| methoden at.js | Alles wordt ondersteund, behalve voor<br>`mboxCreate()`<br>`mboxUpdate()`<br>`mboxDefine()`<br>dat standaardinhoud weergeeft. |

### Parameters van queryreeks

| Parameter | Ondersteund? |
| --- | --- |
| `?mboxDisable` | Ja |
| `?mboxDisable` | Ja |
| `?mboxTrace` | Ja |
| `?mboxSession` | Nee |
| `?mboxOverride.browserIp` | Nee |

## Reactietokens {#response-tokens}

te.js 2.*x*, net als bij .js 1.*x*, gebruikt de douanegebeurtenis  `at-request-succeeded` aan tokens van de oppervlakreactie. Voor codevoorbeelden die de `at-request-succeeded` douanegebeurtenis gebruiken, zie [Reactietokens](/help/administrating-target/response-tokens.md).

## te.js 1.*xparameters* naar at.js 2.** xpayload-toewijzing  {#payload-mapping}

In deze sectie worden de toewijzingen tussen at.js 1 beschreven.** xand at.js 2.*x*.

Voordat u gaat overstappen op parametertoewijzing, zijn de eindpunten die in deze bibliotheekversies worden gebruikt, gewijzigd:

* te.js 1.*x* -  `http://<client code>.tt.omtrdc.net/m2/<client code>/mbox/json`
* te.js 2.*x* -  `http://<client code>.tt.omtrdc.net/rest/v1/delivery`

Een ander belangrijk verschil is dat:

* te.js 1.*x* - Clientcode maakt deel uit van het pad
* te.js 2.*x* - De code van de cliënt wordt verzonden als parameter van het vraagkoord, zoals:
   `http://<client code>.tt.omtrdc.net/rest/v1/delivery?client=democlient`

De volgende secties maken een lijst van elk bij.js 1.** xparameter, de beschrijving ervan en de bijbehorende 2.** xJSON-lading (indien van toepassing):

### at_property

(te.js 1.** xparameter)

Wordt gebruikt voor [Enterprise-gebruikersmachtigingen](/help/administrating-target/c-user-management/property-channel/property-channel.md).

```
{
  ....
  "property": {
    "token": "1213213123122313121"
  }
  ....
}
```

### mboxHost

(te.js 1.** xparameter)

Het domein van de pagina waarop de doelbibliotheek wordt uitgevoerd.

te.js 2.** xJSON-lading:

```
{
  "context": {
    "browser": {
       "host": "test.com"
    }
  }
}
```

### webGLRenderer

(te.js 1.** xparameter)

De WEB GL-renderermogelijkheden van de browser. Dit wordt gebruikt door ons mechanisme voor apparaatdetectie om te bepalen of het apparaat van de bezoeker een bureaublad, iPhone, Android enzovoort is.

te.js 2.** xJSON-lading:

```
{
  "context": {
    "browser": {
       "webGLRenderer": "AMD Radeon Pro 560X OpenGL Engine"
    }
  }
}
```

### mboxURL

(te.js 1.** xparameter)

De pagina-URL.

te.js 2.** xJSON-lading:

```
{
  "context": {
    "address": {
       "url": "http://test.com"
    }
  }
}
```

### mboxReferrer

(te.js 1.** xparameter)

De paginareferentie.

te.js 2.** xJSON-lading:

```
{
  "context": {
    "address": {
       "referringUrl": "http://google.com"
    }
  }
}
```

### mbox (de naam) is gelijk aan global mbox

(te.js 1.** xparameter)

Delivery API heeft niet langer een globaal mbox-concept. In de JSON-payload moet u `execute > pageLoad` gebruiken.

te.js 2.** xJSON-lading:

```
{
  "execute": {
    "pageLoad": {
       "parameters": ....
       "profileParameters": ...
       .....
    }
  }
}
```

### mbox (de naam) is *not* gelijk aan global mbox

(te.js 1.** xparameter)

Als u de naam van een box wilt gebruiken, geeft u deze door aan `execute > mboxes`. Een box vereist een index en een naam.

te.js 2.** xJSON-lading:

```
{
  "execute": {
    "mboxes": [{
       "index": 0,
       "name": "some-mbox",
       "parameters": ....
       "profileParameters": ...
       .....
    }]
  }
}
```

### mboxId

(te.js 1.** xparameter)

Niet meer gebruikt.

### mboxCount

(te.js 1.** xparameter)

Niet meer gebruikt.

### mboxRid

(te.js 1.** xparameter)

Id van verzoek die door stroomafwaartse systemen wordt gebruikt om met het zuiveren te helpen.

te.js 2.** xJSON-lading:

```
{
  "requestId": "2412234442342"
  ....
}
```

### mboxTime

(te.js 1.** xparameter)

Niet meer gebruikt.

### mboxSession

(te.js 1.** xparameter)

Identiteitskaart van de zitting wordt verzonden als parameter van het vraagkoord (`sessionId`) aan het eindpunt van levering API.

### mboxPC

(te.js 1.** xparameter)

De TNT-id wordt doorgegeven naar `id > tntId`.

te.js 2.** xJSON-lading:

```
{
  "id": {
    "tntId": "ca5ddd7e33504c58b70d45d0368bcc70.21_3"
  }
  ....
}
```

### mboxMCGVID

(te.js 1.** xparameter)

De Marketing Cloud Bezoeker-id wordt doorgegeven naar `id > marketingCloudVisitorId`.

te.js 2.** xJSON-lading:

```
{
  "id": {
    "marketingCloudVisitorId": "797110122341429343505"
  }
  ....
}
```

### `vst.aaaa.id` en  `vst.aaaa.authState`

(te.js 1.** xparameters)

Klantid&#39;s moeten worden doorgegeven aan `id > customerIds`.

te.js 2.** xJSON-lading:

```
{
  "id": {
    "customerIds": [{
       "id": "1232131",
       "integrationCode": "aaaa",
       "authenticatedState": "....."
     }]
  }
  ....
}
```

### mbox3rdPartyId

(te.js 1.** xparameter)

Id van derde partij van klant die wordt gebruikt om verschillende doel-id&#39;s te koppelen.

te.js 2.** xJSON-lading:

```
{
  "id": {
    "thirdPartyId": "1232312323123"
  }
  ....
}
```

### mboxMCSDID

(te.js 1.** xparameter)

SDID, ook wel Supplemental Data ID genoemd. Moet worden doorgegeven aan `experienceCloud > analytics > supplementalDataId`.

te.js 2.** xJSON-lading:

```
{
  "experienceCloud": {
    "analytics": {
      "supplementalDataId": "1212321132123131"
    }
  }
  ....
}
```

### vst.trk

(te.js 1.** xparameter)

Analytics tracking-server. Moet worden doorgegeven aan `experienceCloud > analytics > trackingServer`.

te.js 2.** xJSON-lading:

```
{
  "experienceCloud": {
    "analytics": {
      "trackingServer": "analytics.test.com"
    }
  }
  ....
}
```

### vst.trks

(te.js 1.** xparameter)

Beveiliging van de analytische trackingserver. Moet worden doorgegeven aan `experienceCloud > analytics > trackingServerSecure`.

te.js 2.** xJSON-lading:

```
{
  "experienceCloud": {
    "analytics": {
      "trackingServerSecure": "secure-analytics.test.com"
    }
  }
  ....
}
```

### mboxMCGLH

(te.js 1.** xparameter)

Tip voor locatie van Audience Manager. Moet worden doorgegeven aan `experienceCloud > audienceManager > locationHint`.

te.js 2.** xJSON-lading:

```
{
  "experienceCloud": {
    "audienceManager": {
      "locationHint": 9
    }
  }
  ....
}
```

### mboxAAMB

(te.js 1.** xparameter)

Audience Manager blob. Moet worden doorgegeven aan `experienceCloud > audienceManager > blob`.

te.js 2.** xJSON-lading:

```
{
  "experienceCloud": {
    "audienceManager": {
      "blob": "2142342343242342"
    }
  }
  ....
}
```

### mboxVersion

(te.js 1.** xparameter)

Versie wordt verzonden als parameter van het vraagkoord via de versieparameter.

## Trainingsvideo: te.js 2.** xarchitecturaal diagram  ![Overzicht badge](/help/assets/overview.png)

te.js 2.*Vergroot de Adobe Target-ondersteuning voor SPA en integreert deze met andere Experience Cloud-oplossingen.* In deze video wordt uitgelegd hoe alles bij elkaar komt.

>[!VIDEO](https://video.tv.adobe.com/v/26250)

Zie [Begrijpen hoe at.js 2.** ](https://helpx.adobe.com/target/kt/using/atjs20-diagram-technical-video-understand.html) werkt meer informatie uit.