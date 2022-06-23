---
keywords: at.js releases;at.js versies;app van één pagina;spa;cross-domain;cross-domain
description: Leer hoe u een upgrade uitvoert vanaf Adobe [!DNL Target] at.js 1.x tot at.js 2.x. Onderzoek systeemstroomdiagrammen, leer over nieuwe en verouderde functies, en meer.
title: Hoe werk ik bij van versie 1.js naar versie 2.x?
feature: at.js
role: Developer
exl-id: f5ec6bf1-f38c-4681-a6c1-b862272ee55d
source-git-commit: c196b7e41101978ee029f93d5cd71c9b2d5b99f1
workflow-type: tm+mt
source-wordcount: '2860'
ht-degree: 0%

---

# Upgrade uitvoeren vanaf 0,js 1.*x* tot en met at.js 2.*x*

De nieuwste versie van at.js in [!DNL Adobe Target] verstrekt rijke eigenschapreeksen die uw zaken uitrusten om verpersoonlijking op volgende-generatie, cliënt-zijtechnologieën uit te voeren. Deze nieuwe versie is gericht op het upgraden van at.js voor harmonieuze interacties met toepassingen van één pagina (SPA).

Hier volgen enkele voordelen van het gebruik van at.js 2.*x* die niet beschikbaar zijn in vorige versies:

* De capaciteit om alle aanbiedingen op pagina-lading in het voorgeheugen onder te brengen om veelvoudige servervraag aan één enkele servervraag te verminderen.
* Verbeter de ervaringen van uw eindgebruikers op uw site aanzienlijk, omdat aanbiedingen direct via het cachegeheugen worden weergegeven zonder vertraging die traditionele serveraanroepen introduceren.
* Eenvoudige one-line code en eenmalige ontwikkelaarsopstelling om uw marketers toe te laten om A/B en XT activiteiten via VEC op uw SPA tot stand te brengen en in werking te stellen.

## te.js 2.*x* systeemdiagrammen

De volgende diagrammen helpen u het werkschema van at.js 2 begrijpen.*x* met Weergaven en hoe dit de SPA integratie verbetert. Een betere introductie van de concepten die worden gebruikt in at.js 2.*x*, zie [Toepassing van één pagina](https://developer.adobe.com/target/implement/client-side/atjs/how-to-deployatjs/target-atjs-single-page-application/).

![Doelstroom met at.js 2.*x*](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/assets/system-diagram-atjs-20.png)

| Bellen | Details |
| --- | --- |
| 1 | De vraag keert terug [!DNL Experience Cloud ID] indien de gebruiker is geverifieerd; een andere vraag synchroniseert de klant identiteitskaart |
| 2 | De bibliotheek at.js wordt synchroon geladen en de hoofdtekst van het document verborgen.<br>at.js kan ook asynchroon worden geladen met een optie die fragment verbergt dat op de pagina is geïmplementeerd. |
| 3 | Er wordt een aanvraag voor het laden van een pagina ingediend, inclusief alle geconfigureerde parameters (MCID, SDID en klant-id). |
| 4 | Profielscripts worden uitgevoerd en vervolgens toegevoegd aan de profielenwinkel. De winkel vraagt om gekwalificeerd publiek uit de Audience Library (bijvoorbeeld publiek dat wordt gedeeld vanuit Adobe Analytics, Publiek beheer, enz.).<br>Klantkenmerken worden in een batchproces naar de profielopslag verzonden. |
| 5 | Gebaseerd op parameters en profielgegevens van het URL-verzoek, [!DNL Target] bepaalt welke activiteiten en ervaringen u wilt retourneren aan de bezoeker voor de huidige pagina en de toekomstige weergaven. |
| 6 | Gerichte inhoud wordt teruggestuurd naar de pagina, waarbij eventueel ook profielwaarden voor extra personalisatie worden opgenomen.<br>Gerichte inhoud op de huidige pagina wordt zo snel mogelijk zichtbaar zonder flikkering van de standaardinhoud.<br>Gerichte inhoud voor weergaven die worden weergegeven als resultaat van gebruikershandelingen in een SPA die in de browser in de cache is opgeslagen, zodat deze direct kan worden toegepast zonder extra serveraanroep wanneer de weergaven worden geactiveerd `triggerView()`. |
| 7 | De analysegegevens worden verzonden naar de servers van de Inzameling van Gegevens. |
| 8 | De gerichte gegevens worden aangepast aan de analysegegevens via SDID en worden verwerkt in de analytische rapporteringsopslag.<br>De analysegegevens kunnen dan in zowel Analytics als Doel via Analytics voor de rapporten van het Doel (A4T) worden bekeken. |

Nu, waar dan ook `triggerView()` wordt geïmplementeerd op uw SPA, worden de weergaven en acties opgehaald uit het cachegeheugen en aan de gebruiker getoond zonder een serveraanroep. `triggerView()` verzoekt de Commissie tevens [!DNL Target] achterkant om het aantal beeldingen te verhogen en op te nemen.

![Doelstroom bij.js 2.*x* triggerView](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/assets/atjs-20-triggerview.png)

| Bellen | Details |
| --- | --- |
| 1 | `triggerView()` wordt opgeroepen in de SPA om de weergave te renderen en acties toe te passen om visuele elementen te wijzigen. |
| 2 | De gerichte inhoud voor de mening wordt gelezen van het geheime voorgeheugen. |
| 3 | Gerichte inhoud wordt zo snel mogelijk zichtbaar zonder flikkering van de standaardinhoud. |
| 4 | Aanmelding wordt verzonden naar de [!DNL Target] De Opslag van het profiel om de bezoeker in de activiteit en verhogingsmetriek te tellen. |
| 5 | Analytische gegevens die naar de Servers van de Inzameling van Gegevens worden verzonden. |
| 6 | De doelgegevens worden via de SDID aangepast aan de analysegegevens en worden verwerkt in de analytische rapportageopslag. De analysegegevens kunnen dan in zowel Analytics als Doel via A4T- rapporten worden bekeken. |

## Implementeer om.js 2.*x* {#deploy-atjs-200}

1. Implementeer om.js 2.*x* via tags in [[!DNL Adobe Experience Platform]](https://developer.adobe.com/target/implement/client-side/atjs/how-to-deployatjs/implement-target-using-adobe-launch/) extensie.

   >[!NOTE]
   >
   > At.js implementeren met tags in [!DNL Adobe Experience Platform] is de voorkeursmethode.

   of

   Handmatig downloaden om.js 2.*x* het gebruiken van het Doel UI en stelt het op gebruikend [methode naar keuze](https://developer.adobe.com/target/implement/client-side/atjs/how-to-deployatjs/how-to-deployatjs/).

## Vervangen at.js-functies

Er zijn verschillende functies die zijn vervangen in at.js 2.*x*.

>[!IMPORTANT]
>
>Als deze vervangen functies nog steeds op uw site worden gebruikt wanneer at.js 2.*x* wordt opgesteld, zult u consolewaarschuwingen zien. De aanbevolen aanpak bij de upgrade is het testen van de implementatie van at.js 2.*x* in een het opvoeren milieu en zorg ervoor om door elk en elke waarschuwing te gaan die in de console is geregistreerd en de verouderde functies aan nieuwe functies te vertalen die in at.js 2 worden geïntroduceerd.*x*.

U kunt de vervangen functies en hun tegenhanger hieronder vinden. Voor een volledige lijst met functies raadpleegt u [at.js-functies](https://developer.adobe.com/target/implement/client-side/atjs/atjs-functions/atjs-functions/).

>[!NOTE]
>te.js 2.*x* niet meer automatisch voorverborgen `mboxDefault` gemarkeerde elementen. Klanten moeten daarom de vooraf verborgen logica handmatig op de site of via een tagmanager kunnen gebruiken.

### mboxCreate(mbox,params)

**Beschrijving**:

Voert een verzoek uit en past de aanbieding op dichtstbijzijnde DIV met toe `mboxDefault` klassenaam.

**Voorbeeld**:

```
<div class="mboxDefault">
  default content to replace by offer
</div>
<script>
  mboxCreate('mboxName','param1=value1','param2=value2');
</script>
```

**te.js 2.*x* equivalent**

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

**Beschrijving**:

Maakt een interne toewijzing tussen een element en een naam van een box, maar voert de aanvraag niet uit. Wordt gebruikt in combinatie met `mboxUpdate()`, die het verzoek uitvoert en de aanbieding op het element toepast dat door nodeId wordt geïdentificeerd in `mboxDefine()`. Kan ook worden gebruikt om een box bij te werken die is gestart door `mboxCreate`.

**Voorbeeld**:

```
<div id="someId" class="mboxDefault"></div>
<script>
 mboxDefine('someId','mboxName','param1=value1','param2=value2');
 mboxUpdate('mboxName','param3=value3','param4=value4');
</script>
```

**te.js 2.*x* equivalent**:

Een alternatief voor `mboxDefine()` en `mboxUpdate` is `getOffer()` en `applyOffer()`met de optie Selector in `applyOffer()`. Met deze methode kunt u de aanbieding aan een element toewijzen met elke CSS-kiezer, niet alleen met een id.

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

**Beschrijving**:

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

Klanten die `mboxCreate()` voor conversie-tracking moet worden gebruikt `trackEvent()` of `getOffer()`.

### Levering aanbieden

Klanten die niet vervangen `mboxCreate()` with `getOffer()` of `applyOffer()` risico dat er geen aanbiedingen zijn gedaan.

### Mag om.js 2.*x* worden gebruikt op sommige pagina&#39;s en op 0,js 1.*x* bevindt zich op andere pagina&#39;s?

Ja, het bezoekersprofiel blijft op alle pagina&#39;s behouden met behulp van verschillende versies en bibliotheken. De cookieindeling is hetzelfde.

### Nieuw API-gebruik in at.js 2.*x*

te.js 2.*x* gebruikt een nieuwe API, die wij de levering API noemen. Om te kunnen bepalen of at.js het [!DNL Target] de randserver correct, kunt u het lusje van het Netwerk van de Hulpmiddelen van de Ontwikkelaar van uw browser aan &quot;levering&quot;filtreren, &quot;`tt.omtrdc.net`,&quot; of uw clientcode. U zult ook merken dat [!DNL Target] verzendt een JSON-payload in plaats van sleutel-waardeparen.

### Globale doelbox wordt niet meer gebruikt

In at.js 2.*x*, wordt &#39;`target-global-mbox`&quot; zichtbaar in de netwerkvraag. In plaats daarvan hebben we de &quot;`target-global-mbox`&quot; syntaxis naar &quot;`execute > pageLoad`&quot; in de aan de [!DNL Target] servers, zoals hieronder weergegeven:

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

In wezen is het concept global mbox geïntroduceerd om [!DNL Target] weet of u aanbiedingen en inhoud tijdens het laden van de pagina wilt ophalen. Daarom hebben we dit in onze nieuwste versie duidelijker gemaakt.

### Maakt de globale naam van de box in at.js nog uit?

Klanten kunnen een algemene mbox-naam opgeven via [!UICONTROL Target > Administration > Implementation > Edit at.js Settings]. Deze instelling wordt gebruikt door de [!DNL Target] te vertalen Edge-servers > pageLoad om de algemene naam van het selectievakje in het dialoogvenster [!DNL Target] UI. Hierdoor kunnen klanten API&#39;s aan de serverzijde, de op formulieren gebaseerde composer, profielscripts blijven gebruiken en een publiek maken met de algemene mbox-naam. Wij adviseren sterk u ook ervoor zorgt de zelfde globale naam van mbox op wordt gevormd [!UICONTROL Administration > Visual Experience Composer] pagina, ook als u nog pagina&#39;s hebt die at.js 1 gebruiken.*x*, zoals in de volgende afbeeldingen wordt getoond.

![Dialoogvenster Wijzigen bij.js](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/assets/modify-atjs.png)

en

![Aangepaste algemene mbox](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/assets/custom-global-mbox.png)

### Moet de instelling voor automatisch maken van globale mbox worden ingeschakeld voor at.js 2.*x*?

In de meeste gevallen ja. Deze instelling vertelt at.js 2.*x* om een verzoek in te dienen bij de [!DNL Target] Edge-servers bij het laden van de pagina. Omdat globale mbox wordt vertaald om uit te voeren > pageLoad, en als u een verzoek op paginading wilt in werking stellen, dan zou deze het plaatsen moeten zijn.

### Zal de bestaande activiteiten VEC blijven werken, hoewel de doel globale mbox naam niet van at.js 2 wordt gespecificeerd.*x*?

Ja, omdat execute > pageLoad wordt verwerkt op de [!DNL Target] achterzijde `target-global-mbox`.

### Als mijn op formulieren gebaseerde activiteiten gericht zijn op de `target-global-mbox`, zullen deze activiteiten blijven functioneren?

Ja, omdat execute > pageLoad wordt verwerkt op de [!DNL Target] Edge-servers, zoals `target-global-mbox`.

### Ondersteund en niet-ondersteund at.js 2.*x* Instellingen

| Instelling | Ondersteund? |
| --- | --- |
| X-domein | Nee |
| Globale box automatisch maken | Ja |
| Algemene naam van box | Ja |

### Ondersteuning voor interdomeintracering in at.js 2.x {#cross-domain}

Met interdomeinspatiëring kunt u bezoekers aan elkaar koppelen in verschillende domeinen. Omdat voor elk domein een nieuwe cookie moet worden gemaakt, is het moeilijk bezoekers bij te houden wanneer ze van domein naar domein navigeren. Voor het bijhouden van andere domeinen, [!DNL Target] gebruikt een cookie van derden om bezoekers in verschillende domeinen bij te houden. Op deze manier kunt u een doelactiviteit maken die meerdere `siteA.com` en `siteB.com` en bezoekers blijven in dezelfde ervaring wanneer ze door unieke domeinen navigeren. Deze functionaliteit is verbonden met het gedrag van cookies van derden en van andere bedrijven.

>[!NOTE]
>
>Uit het vak in at.js 2 wordt geen ondersteuning geboden voor het bijhouden van domeinoverschrijdingen.*x*. Interdomeintracering wordt ondersteund in at.js 2.*x* via de Experience Cloud ID-bibliotheek v4.3.0+.

Bij Doel wordt het cookie van de andere fabrikant opgeslagen in `<CLIENTCODE>.tt.omtrdc.net`. Het cookie van de eerste partij wordt opgeslagen in `clientdomain.com`. De eerste aanvraag retourneert HTTP-antwoordheaders die proberen cookies van derden met de naam in te stellen `mboxSession` en `mboxPC`, terwijl een omleidingsverzoek wordt teruggestuurd met een extra parameter (`mboxXDomainCheck=true`). Als de browser cookies van derden accepteert, bevat de omleidingsaanvraag deze cookies en wordt de ervaring geretourneerd. Dit werkschema is mogelijk omdat wij de methode van de GET van HTTP gebruiken.

In punt 2.js.*x*, wordt de GET van HTTP niet meer gebruikt en in plaats daarvan gebruiken wij de POST van HTTP. HTTP-POST wordt nu gebruikt via at.js 2.*x* om JSON-nuttige taken naar Target Edge-servers te verzenden. Dit betekent dat de omleidingsaanvraag om te controleren of een browser cookies van derden ondersteunt, nu wordt afgebroken. Dit komt doordat HTTP-GET-aanvragen epidemiologische transacties zijn, terwijl HTTP-POST niet-epidemiologisch is en niet willekeurig mag worden herhaald. Daarom is het volgen tussen domeinen in at.js 2.*x* wordt niet meer ondersteund vanuit het vak. Alleen om.js 1.*x* heeft out-of-box steun voor dwars-domein het volgen.

Als u interdomeintracering wilt gebruiken, moet u het dialoogvenster [ECID-bibliotheek v4.3.0+](https://experienceleague.adobe.com/docs/id-service/using/release-notes/release-notes.html) in combinatie met at.js 2.*x*. De ECID-bibliotheek bestaat voor het beheer van permanente id&#39;s waarmee een bezoeker zelfs in verschillende domeinen kan worden geïdentificeerd.

>[!NOTE]
>
>Na installatie van de ECID-bibliotheek v4.3.0+ en at.js 2.*x* kunt u activiteiten maken die zich uitstrekken over unieke domeinen en gebruikers bijhouden. Het is belangrijk om op te merken dat deze functionaliteit slechts werkt nadat de zitting verloopt.

### Automatisch globale box maken wordt ondersteund

Deze instelling vertelt at.js 2.*x* om een verzoek in te dienen bij de [!DNL Target] Edge-servers bij het laden van de pagina. Omdat het globale mbox wordt vertaald om > pageLoad uit te voeren, en dit wordt geïnterpreteerd door [!DNL Target] Edge-servers moeten klanten deze optie inschakelen als ze een aanvraag willen indienen bij het laden van een pagina.

### Algemene naam van box wordt ondersteund

Klanten kunnen een algemene mbox-naam opgeven via [!UICONTROL Target > Administration > Implementation > Edit]. Deze instelling wordt gebruikt door de [!DNL Target] Edge-servers die moeten worden vertaald, uitvoeren > pageLoad naar de ingevoerde algemene naam van het selectievakje. Hierdoor kunnen klanten API&#39;s aan de serverzijde, de op formulieren gebaseerde composer, profielscripts blijven gebruiken en een publiek maken dat zich richt op de algemene box.

### Zijn de onderstaande aangepaste gebeurtenissen om.js van toepassing op `triggerView()` of is het alleen bedoeld voor `applyOffer()` of `applyOffers()`?

* `adobe.target.event.CONTENT_RENDERING_FAILED`
* `adobe.target.event.CONTENT_RENDERING_SUCCEEDED`
* `adobe.target.event.CONTENT_RENDERING_NO_OFFERS`
* `adobe.target.event.CONTENT_RENDERING_REDIRECT`

Ja, de aangepaste gebeurtenissen at.js zijn van toepassing op `triggerView()` ook.

### Het zegt wanneer ik bel `triggerView()` met &amp;accolade;`“page” : “true”`&amp;Broce; hiermee wordt een bericht verzonden naar de [!DNL Target] de indruk vergroten. Zorgt het er ook voor dat de profielscripts worden uitgevoerd?

Wanneer een prefetch vraag aan wordt gemaakt [!DNL Target] als achtergrond, worden de profielmanuscripten uitgevoerd. Daarna worden de profielgegevens gecodeerd en teruggestuurd naar de clientzijde. Na `triggerView()` with `{"page": "true"}` wordt aangeroepen, wordt een melding samen met de gecodeerde profielgegevens verzonden. Dit is wanneer de [!DNL Target] backend zal dan de profielgegevens decrypteren en in de gegevensbestanden opslaan.

### Moeten wij pre-verbergende code toevoegen alvorens te roepen `triggerView()` om flikkering te beheren?

Nee, u hoeft geen code toe te voegen die voor het aanroepen verborgen is `triggerView()`. te.js 2.*x* beheert de logica voor het vooraf verbergen en flikkeren voordat de weergave wordt weergegeven en toegepast.

### welke om.js 1.*x* parameters voor het maken van soorten publiek worden niet ondersteund in at.js 2.*x*? {#audience-parameters}

De volgende parameters at.js 1.x zijn *NOT* momenteel ondersteund voor het maken van publiek bij gebruik van at.js 2.*x*:

* browserHeight
* browserWidth
* browserTimeOffset
* screenHeight
* screenWidth
* screenOrientation
* colorDepth
* devicePixelRatio
* vst.* parameters ([zie hieronder](#vst))

### te.js 2.*x* biedt geen ondersteuning voor het maken van soorten publiek met behulp van vst.* parameters {#vst}

Klanten op om.js 1.*x* kon vst gebruiken.* mbox-parameters om een publiek te maken. Dit was een onbedoeld neveneffect van hoe at.js 1.*x* mbox-parameters naar de [!DNL Target] back-end. Na het migreren naar om.js 2.*x* kunt u geen publiek meer maken met deze parameters omdat at.js 2.*x* verzendt de parameters mbox verschillend.

## at.js-compatibiliteit

In de volgende tabellen wordt om .js uitgelegd. 2.*x* compatibiliteit met verschillende typen activiteiten, integraties, functies en at.js-functies.

### Typen activiteiten {#types}

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
>Auto-Target activiteiten worden gesteund door at.js 2.*x* en de VEC wanneer alle wijzigingen op de `Page Load Event`. Als er wijzigingen worden toegevoegd aan bepaalde weergaven, worden alleen de activiteiten A/B Test, Auto-Allocate en Experience Targeting (XT) ondersteund.

### Integraties {#integrations}

| Type | Ondersteund? |
| --- | --- |
| Analyses voor doel (A4T) | Ja |
| Soorten publiek | Ja |
| Klantkenmerken | Ja |
| Fragmenten voor AEM | Ja |
| [!DNL Adobe Experience Platform] extension | [Ja](https://developer.adobe.com/target/implement/client-side/atjs/how-to-deployatjs/implement-target-using-adobe-launch/) |
| Foutopsporing | Ja |
| Auditor | De regels zijn nog niet bijgewerkt voor om.js 2.*x* |
| Inschakelen | Nee. Ondersteuning voor Inschakelen voor [GDPR](https://developer.adobe.com/target/before-implement/privacy/cmp-privacy-and-general-data-protection-regulation/) wordt ondersteund in [at.js versie 2.1.0](https://developer.adobe.com/target/implement/client-side/atjs/target-atjs-versions/). |
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
| methoden at.js | Alles wordt ondersteund, behalve voor<br>`mboxCreate()`<br>`mboxUpdate()`<br>`mboxDefine()`<br>die de standaardinhoud zal weergeven. |

### Parameters van queryreeks

| Parameter | Ondersteund? |
| --- | --- |
| `?mboxDisable` | Ja |
| `?mboxDisable` | Ja |
| `?mboxTrace` | Ja |
| `?mboxSession` | Nee |
| `?mboxOverride.browserIp` | Ja |

## Reactietokens {#response-tokens}

te.js 2.*x*, net als bij.js 1.*x* gebruikt u de aangepaste gebeurtenis `at-request-succeeded` op tokens voor oppervlakreactie. Voor codevoorbeelden met de `at-request-succeeded` aangepaste gebeurtenis, zie [Reactietokens](/help/main/administrating-target/response-tokens.md).

## te.js 1.*x* parameters tot at.js 2.*x* lading toewijzen {#payload-mapping}

In deze sectie worden de toewijzingen tussen at.js 1 beschreven.*x* en te.js 2.*x*.

Voordat u gaat overstappen op parametertoewijzing, zijn de eindpunten die in deze bibliotheekversies worden gebruikt, gewijzigd:

* te.js 1.*x* - `http://<client code>.tt.omtrdc.net/m2/<client code>/mbox/json`
* te.js 2.*x* - `http://<client code>.tt.omtrdc.net/rest/v1/delivery`

Een ander belangrijk verschil is dat:

* te.js 1.*x* - Clientcode maakt deel uit van het pad
* te.js 2.*x* - Clientcode wordt verzonden als een querytekenreeksparameter, zoals:
   `http://<client code>.tt.omtrdc.net/rest/v1/delivery?client=democlient`

De volgende secties maken een lijst van elk bij.js 1.*x* parameter, de beschrijving ervan en de bijbehorende 2.*x* JSON-lading (indien van toepassing):

### at_property

(te.js 1.*x* parameter)

Gebruikt voor [Machtigingen voor zakelijke gebruikers](/help/main/administrating-target/c-user-management/property-channel/property-channel.md).

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

(te.js 1.*x* parameter)

Het domein van de pagina waarop de doelbibliotheek wordt uitgevoerd.

te.js 2.*x* JSON-lading:

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

(te.js 1.*x* parameter)

De WEB GL-renderermogelijkheden van de browser. Dit wordt gebruikt door het detectiemechanisme van het apparaat om te bepalen of het apparaat van de bezoeker een bureaublad, iPhone, Android, enz. is.

te.js 2.*x* JSON-lading:

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

(te.js 1.*x* parameter)

De pagina-URL.

te.js 2.*x* JSON-lading:

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

(te.js 1.*x* parameter)

De paginareferentie.

te.js 2.*x* JSON-lading:

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

(te.js 1.*x* parameter)

Delivery API heeft niet langer een globaal mbox-concept. In de JSON-payload moet u `execute > pageLoad`.

te.js 2.*x* JSON-lading:

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

### mbox (de naam) is *niet* gelijk aan global mbox

(te.js 1.*x* parameter)

Als u de naam van een vak wilt gebruiken, geeft u deze door aan `execute > mboxes`. Een box vereist een index en een naam.

te.js 2.*x* JSON-lading:

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

(te.js 1.*x* parameter)

Niet meer gebruikt.

### mboxCount

(te.js 1.*x* parameter)

Niet meer gebruikt.

### mboxRid

(te.js 1.*x* parameter)

Id van verzoek die door stroomafwaartse systemen wordt gebruikt om met het zuiveren te helpen.

te.js 2.*x* JSON-lading:

```
{
  "requestId": "2412234442342"
  ....
}
```

### mboxTime

(te.js 1.*x* parameter)

Niet meer gebruikt.

### mboxSession

(te.js 1.*x* parameter)

Sessie-id wordt verzonden als een querytekenreeks-parameter (`sessionId`) naar het API-eindpunt van de levering.

### mboxPC

(te.js 1.*x* parameter)

De TNT-id wordt doorgegeven aan `id > tntId`.

te.js 2.*x* JSON-lading:

```
{
  "id": {
    "tntId": "ca5ddd7e33504c58b70d45d0368bcc70.21_3"
  }
  ....
}
```

### mboxMCGVID

(te.js 1.*x* parameter)

Bezoeker-id van Marketing Cloud wordt doorgegeven aan `id > marketingCloudVisitorId`.

te.js 2.*x* JSON-lading:

```
{
  "id": {
    "marketingCloudVisitorId": "797110122341429343505"
  }
  ....
}
```

### `vst.aaaa.id` en `vst.aaaa.authState`

(te.js 1.*x* parameters)

Klant-id&#39;s moeten worden doorgegeven aan `id > customerIds`.

te.js 2.*x* JSON-lading:

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

(te.js 1.*x* parameter)

Id van derde partij van klant die wordt gebruikt om verschillende doel-id&#39;s te koppelen.

te.js 2.*x* JSON-lading:

```
{
  "id": {
    "thirdPartyId": "1232312323123"
  }
  ....
}
```

### mboxMCSDID

(te.js 1.*x* parameter)

SDID, ook wel Supplemental Data ID genoemd. Moet worden doorgegeven aan `experienceCloud > analytics > supplementalDataId`.

te.js 2.*x* JSON-lading:

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

(te.js 1.*x* parameter)

Analytics tracking-server. Moet worden doorgegeven aan `experienceCloud > analytics > trackingServer`.

te.js 2.*x* JSON-lading:

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

(te.js 1.*x* parameter)

Beveiliging van de analytische trackingserver. Moet worden doorgegeven aan `experienceCloud > analytics > trackingServerSecure`.

te.js 2.*x* JSON-lading:

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

(te.js 1.*x* parameter)

Tip voor locatie van Audience Manager. Moet worden doorgegeven aan `experienceCloud > audienceManager > locationHint`.

te.js 2.*x* JSON-lading:

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

(te.js 1.*x* parameter)

Audience Manager blob. Moet worden doorgegeven aan `experienceCloud > audienceManager > blob`.

te.js 2.*x* JSON-lading:

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

(te.js 1.*x* parameter)

Versie wordt verzonden als parameter van het vraagkoord via de versieparameter.

## Trainingsvideo: te.js 2.*x* architectuurdiagram ![Overzicht badge](/help/main/assets/overview.png)

te.js 2.*x* verbetert Adobe Target-ondersteuning voor SPA en integreert deze met andere Experience Cloud-oplossingen. In deze video wordt uitgelegd hoe alles bij elkaar komt.

>[!VIDEO](https://video.tv.adobe.com/v/26250)

Zie [Begrijpen hoe at.js 2.*x* werken](https://helpx.adobe.com/target/kt/using/atjs20-diagram-technical-video-understand.html) voor meer informatie .
