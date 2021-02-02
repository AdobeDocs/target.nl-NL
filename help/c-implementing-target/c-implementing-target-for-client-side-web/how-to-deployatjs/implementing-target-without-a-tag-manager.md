---
keywords: doel implementeren;implementatie;uitvoeren op.js;tagbeheer
description: Informatie over het implementeren van Adobe Target zonder gebruik te maken van een tagbeheer (Adobe starten of Dynamisch tagbeheer).
title: Implementeren zonder tagbeheer
feature: Implement Server-side
translation-type: tm+mt
source-git-commit: 48b94f967252f5ddb009597456edf0a43bc54ba6
workflow-type: tm+mt
source-wordcount: '1520'
ht-degree: 4%

---


# Doel implementeren zonder tagbeheer

Informatie over het implementeren van [!DNL Adobe Target] zonder een tagmanager ([!DNL Adobe Launch] of [!DNL Dynamic Tag Manager]).

>[!NOTE]
>
>[Adobe ](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/cmp-implementing-target-using-adobe-launch.md#topic_5234DDAEB0834333BD6BA1B05892FC25) Launchis de aangewezen methode om Doel en de at.js bibliotheek uit te voeren. De volgende informatie is niet van toepassing wanneer het gebruiken van de Lancering van Adobe om Doel uit te voeren.

Als u de pagina [!UICONTROL Implementation] wilt openen, klikt u op **[!UICONTROL Administration]** > **[!UICONTROL Implementation]**.

U kunt de volgende instellingen opgeven op deze pagina:

* Accountgegevens
* Implementatiemethoden
* Profiel-API
* Foutopsporingsgereedschappen
* Privacy

>[!NOTE]
>
>U kunt instellingen in de bibliotheek at.js overschrijven in plaats van de instellingen in de gebruikersinterface van Target Standard/Premium te configureren of REST API&#39;s te gebruiken. Zie [targetGlobalSettings()](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetgobalsettings.md) voor meer informatie.

## Accountgegevens

U kunt de volgende accountdetails weergeven. Deze instellingen kunnen niet worden gewijzigd.

| Instelling | Beschrijving |
| --- | --- |
| Clientcode | De clientcode is een clientspecifieke reeks tekens die vaak vereist zijn bij het gebruik van de doel-API&#39;s. |
| IMS Organisatie-id | Deze id koppelt uw implementatie aan uw [!DNL Adobe Experience Cloud]-account. |

## Implementatiemethoden

U kunt de volgende instellingen configureren in het deelvenster Implementatiemethoden:

### Algemene instellingen

>[!NOTE]
>
>Deze instellingen worden toegepast op alle .js-bibliotheken van [!DNL Target]. Nadat u wijzigingen hebt aangebracht in de sectie [!UICONTROL Implementation methods], moet u de bibliotheek downloaden en bijwerken in de implementatie.

| Instelling | Beschrijving |
| --- | --- |
| Laden van pagina ingeschakeld (Automatisch een globaal selectievakje maken | Geef op of u de algemene mbox-aanroep in het bestand at.js wilt insluiten om automatisch op elke pagina te starten. |
| Globale mbox | Selecteer een naam voor het globale vakje. Deze naam is standaard target-global-mbox.<br>Speciale tekens, zoals ampersands (&amp;), kunnen worden gebruikt in mbox-namen met at.js. |
| Time-out (seconden) | Als [!DNL Target] niet reageert met inhoud binnen de gedefinieerde periode, wordt de wachttijd van de serveraanroep en de standaardinhoud weergegeven. Aanvullende aanroepen worden nog steeds geprobeerd tijdens de sessie van de bezoeker. De standaardwaarde is 5 seconden.<br>De bibliotheek at.js gebruikt de time-outinstelling in  `XMLHttpRequest`. De time-out wordt gestart wanneer het verzoek wordt geactiveerd en stopt wanneer [!DNL Target] een reactie van de server krijgt. Zie [XMLHttpRequest.timeout](https://developer.mozilla.org/en-US/docs/Web/API/XMLHttpRequest/timeout) op het Mozilla Developer Network voor meer informatie.<br>Als de opgegeven time-out optreedt voordat de reactie wordt ontvangen, wordt standaardinhoud weergegeven en wordt de bezoeker mogelijk geteld als een deelnemer aan een activiteit omdat alle gegevensverzameling aan de  [!DNL Target] rand plaatsvindt. Als het verzoek de [!DNL Target] rand bereikt, wordt de bezoeker geteld.<br>Denk aan het volgende wanneer u de time-outinstelling configureert:<ul><li>Als de waarde te laag is, kunnen gebruikers de standaardinhoud het grootste deel van de tijd zien, hoewel de bezoeker als deelnemer aan de activiteit kon worden geteld.</li><li>Als de waarde te hoog is, kunnen bezoekers lege gebieden op uw webpagina of lege pagina&#39;s zien als u de hoofdtekst langere tijd verbergt.</li></ul>Om een beter inzicht in mbox reactietijden te krijgen, bekijk het lusje van het Netwerk in de Hulpmiddelen van de Ontwikkelaar van uw browser. U kunt ook controlehulpmiddelen voor webprestaties van derden gebruiken, zoals Catchpoint.<br>**Opmerking**: De  [](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetgobalsettings.md) bezoekerApiTimeoutsetting zorgt ervoor dat  [!DNL Target] niet te lang op de reactie van de Bezoeker API wacht. Deze instelling en de instelling Time-out voor at.js die hier wordt beschreven, zijn niet van invloed op elkaar. |
| Profiellevensduur | Deze instelling bepaalt hoe lang bezoekersprofielen worden opgeslagen. Profielen worden standaard twee weken opgeslagen. Dit kan tot 90 dagen worden verhoogd.<br>Als u de instelling voor de levensduur van het profiel wilt wijzigen, neemt u contact op met de  [klantenservice](https://helpx.adobe.com/nl/contact/enterprise-support.ec.html). |

### Hoofduitvoeringsmethode

>[!IMPORTANT]
>
>Het team van het Doel steunt allebei at.js 1.** xand at.js 2.*x*. Voer een upgrade uit naar de meest recente update van een van de belangrijkste versies van at.js om ervoor te zorgen dat u een ondersteunde versie uitvoert.

Als u de gewenste versie at.js wilt downloaden, klikt u op de juiste **[!UICONTROL Download]**-knop.

Als u de instellingen bij .js wilt bewerken, klikt u op **[!UICONTROL Edit]** naast de gewenste versie bij.js.

>[!IMPORTANT]
>
>Voordat u deze standaardinstellingen wijzigt, moet u eerst [Client Care](/help/cmp-resources-and-contact-information.md) raadplegen, zodat u de huidige implementatie niet kunt beïnvloeden.

Naast de hierboven beschreven instellingen zijn ook de volgende specifieke instellingen van at.js beschikbaar:

| Instelling | Beschrijving |
|--- |--- |
| Aangepaste bibliotheekkoptekst | Voeg aangepaste JavaScript toe die u boven aan de bibliotheek wilt opnemen. |
| Aangepaste bibliotheekvoettekst | Voeg aangepaste JavaScript toe die u onder aan de bibliotheek wilt opnemen. |

### Profiel-API

Schakel verificatie voor batchupdates via API in of uit en genereer een profielverificatietoken.

Zie [Profiel-API-instellingen](/help/c-implementing-target/c-considerations-before-you-implement-target/c-methods-to-get-data-into-target/profile-api-settings.md) voor meer informatie.

### Foutopsporingsgereedschappen

Genereer een machtigingstoken om geavanceerde [!DNL Target] het zuiveren hulpmiddelen te gebruiken. Klik op **[!UICONTROL Generate New Authentication Token]**.

![Nieuwe verificatietoken genereren](/help/c-implementing-target/c-considerations-before-you-implement-target/c-methods-to-get-data-into-target/assets/debugger-auth-token.png)

### Privacy

Met deze instellingen kunt u [!DNL Target] gebruiken in overeenstemming met de toepasselijke wetten inzake gegevensprivacy.

Kies het gewenste plaatsen van de IP van de Bezoeker van de Verduistering adresdrop-down lijst:

* Recentste octet-verduistering
* Volledige IP-verduistering
* Geen

Zie [Privacy](/help/c-implementing-target/c-considerations-before-you-implement-target/c-privacy/privacy.md) voor meer informatie.

>[!NOTE]
>
>De optie Verouderde browserondersteuning was beschikbaar in versie 0.js 0.9.3 en eerder. Deze optie is verwijderd in versie 0.js 0.9.4. Zie [Ondersteunde browsers](/help/c-implementing-target/c-considerations-before-you-implement-target/supported-browsers.md) voor een lijst met browsers die worden ondersteund door at.js.<br>Verouderde browsers zijn oudere browsers die geen volledige ondersteuning bieden voor CORS (Cross Origin Resource Sharing). Deze browsers zijn: Browsers van Internet Explorer ouder dan versie 11 en Safari versies 6 en lager. Als ondersteuning voor verouderde browsers was uitgeschakeld, heeft Target geen inhoud geleverd of heeft Target geen bezoekers geteld in rapporten over deze browsers. Als deze optie is ingeschakeld, wordt u aangeraden kwaliteitsborging toe te passen in alle oudere browsers, zodat de klant er optimaal van profiteert.

## Downloaden om.js {#concept_1E1F958F9CCC4E35AD97581EFAF659E2}

Instructies om de bibliotheek te downloaden met de [!DNL Target]-interface of de Download API.

>[!NOTE]
>
>* [Adobe ](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/cmp-implementing-target-using-adobe-launch.md#topic_5234DDAEB0834333BD6BA1B05892FC25) Launchis de aangewezen methode om Doel en de at.js bibliotheek uit te voeren. De volgende informatie is niet van toepassing wanneer het gebruiken van de Lancering van Adobe om Doel uit te voeren.
   >
   >
* Het team van het Doel steunt allebei at.js 1.** xand at.js 2.*x*. Voer een upgrade uit naar de meest recente update van een van de belangrijkste versies van at.js om ervoor te zorgen dat u een ondersteunde versie uitvoert. Voor meer informatie over wat in elke versie is, zie [at.js de Details van de Versie](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md#reference_DBB5EDB79EC44E558F9E08D4774A0F7A).


### Download at.js gebruikend de interface van het Doel {#section_1F5EE401C2314338910FC57F9592894E}

[!DNL at.js] downloaden van de [!DNL Target] interface:

1. Klik op **[!UICONTROL Administration]** > **[!UICONTROL Implementation]**.
1. Klik in de sectie [!UICONTROL Implementation methods] op de knop **[!UICONTROL Download]** naast de gewenste versie at.js.

### Download at.js met de doel-API {#section_C0D9D2A9068144708D08526BA5CA10D0}

[!DNL at.js] downloaden met behulp van de API.

1. Haal uw clientcode op.

   Uw clientcode is beschikbaar boven aan de pagina **[!UICONTROL Administration]** **[!UICONTROL Implementation]** van de [!DNL Target]-interface.

1. Haal uw beheerdersnummer op.

   Deze URL laden:

   ```
   https://admin.testandtarget.omniture.com/rest/v1/endpoint/<varname>client code</varname>
   ```

   Vervang `client code` door de clientcode uit stap 1.

   Het resultaat van het laden van deze URL moet er ongeveer als volgt uitzien:

   ```
   { 
     "api": "https://admin6.testandtarget.omniture.com/admin/rest/v1" 
   }
   ```

   In dit voorbeeld is &#39;6&#39; het beheerdersnummer.

1. [!DNL at.js] downloaden.

   Laad deze URL met de volgende structuur:

   ```
   https://admin<varname>admin number</varname>.testandtarget.omniture.com/admin/rest/v1/libraries/atjs/download?client=<varname>client code</varname>&version=<version number>
   ```

   * Vervang `admin number` door uw beheerdersnummer.
   * Vervang `client code` door de clientcode uit stap 1.
   * Vervang `version number` door het gewenste at.js versienummer (bijvoorbeeld 2.2).

   >[!IMPORTANT]
   >
   >Het team van het Doel handhaaft slechts twee versies van [!DNL at.js]-de huidige versie en de tweede-recentste versie. Upgrade [!DNL at.js] indien nodig om ervoor te zorgen dat u een ondersteunde versie gebruikt. Voor meer informatie over wat in elke versie is, zie [at.js de Details van de Versie](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md#reference_DBB5EDB79EC44E558F9E08D4774A0F7A).

   Wanneer u deze URL laadt, wordt het aangepaste [!DNL at.js]-bestand gedownload.

## at.js-implementatie {#concept_03CFA86973A147839BEB48A06FEE5E5A}

at.js moet worden geïmplementeerd in het `<head>`-element van elke pagina van uw website.

Een typische implementatie van Doel die geen markeringsmanager zoals [Adobe Launch](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/cmp-implementing-target-using-adobe-launch.md#topic_5234DDAEB0834333BD6BA1B05892FC25) of [Dynamisch het Beheer van de Markering](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/implementing-target-using-dynamic-tag-management.md#concept_3A40AF6FFC0E4FD2AA81B303A79D0B96) gebruikt ziet als volgt uit:

```
<!doctype html> 
<html> 
<head> 
    <meta charset="utf-8"> 
    <title>Title of the Page</title> 
    <!--Preconnect and DNS-Prefetch to improve page load time--> 
    <link rel="preconnect" href="//<client code>.tt.omtrdc.net"> 
    <link rel="dns-prefetch" href="//<client code>.tt.omtrdc.net"> 
    <!--/Preconnect and DNS-Prefetch--> 
    <!--Data Layer to enable rich data collection and targeting--> 
    <script> 
        var digitalData = { 
            "page": { 
                "pageInfo": { 
                    "pageName": "Home" 
                } 
            } 
        }; 
    </script> 
    <!--/Data Layer--> 
    <!-- targetPageParams(), targetPageParamsAll(), Data Providers or targetGlobalSettings() functions to enrich the visitor profile or modify the library settings--> 
    <script> 
        targetPageParams = function() { 
            return { 
                "a": 1, 
                "b": 2, 
                "pageName": digitalData.page.pageInfo.pageName, 
                "profile": { 
                    "age": 26, 
                    "country": { 
                        "city": "San Francisco" 
                    } 
                } 
            }; 
        }; 
    </script> 
    <!--/targetPageParams()--> 
 
    <!--jQuery or other helper libraries should be implemented before at.js if you would like to use their methods in Target--> 
    <script src="jquery-3.3.1.min.js"></script> 
    <!--/jQuery--> 
    <!--Target's JavaScript SDK, at.js--> 
    <script src="at.js"></script> 
    <!--/at.js--> 
</head>
<body> 
    The default content of the page 
</body> 
</html>
```

Houd rekening met de volgende belangrijke opmerkingen:

* Het HTML5-document (bijvoorbeeld `<!doctype html>`) moet worden gebruikt. Niet-ondersteunde of oudere documenttypen kunnen ertoe leiden dat Target geen aanvraag kan indienen.
* De opties Preconnect en Prefetch zijn opties die u kunnen helpen uw webpagina&#39;s sneller te laden. Als u deze configuraties gebruikt, zorg ervoor dat u `<client code>` met uw eigen cliëntcode vervangt, die u van **[!UICONTROL Administration]** > **[!UICONTROL Implementation] pagina kunt verkrijgen.
* Als u een gegevenslaag hebt, is het beter om zoveel mogelijk van het in `<head>` van uw pagina&#39;s te bepalen alvorens om.js laadt. Deze plaatsing verstrekt het maximumvermogen om deze informatie in Doel voor verpersoonlijking te gebruiken.
* Speciale doelfuncties, zoals `targetPageParams()`, `targetPageParamsAll()`, Data Providers en `targetGlobalSettings()` moeten worden gedefinieerd na de gegevenslaag en voordat at.js wordt geladen. U kunt deze bestanden ook opslaan in de sectie [!UICONTROL Library Header] van de pagina [!UICONTROL Edit at.js Settings] en opslaan als onderdeel van de bibliotheek at.js zelf. Voor meer informatie over deze functies, zie [at.js functies](/help/c-implementing-target/c-implementing-target-for-client-side-web/cmp-atjs-functions.md).
* Als u JavaScript-hulplijnbibliotheken gebruikt, zoals jQuery, neemt u deze op voordat u Target gaat gebruiken, zodat u de syntaxis en methoden van deze bibliotheken kunt gebruiken wanneer u Target-ervaringen opstelt.
* Neem om .js op in de `<head>` van uw pagina&#39;s.

## Conversies bijhouden {#task_E85D2F64FEB84201A594F2288FABF053}

In het vak Bevestiging van bestelling worden gegevens over bestellingen op uw site vastgelegd en wordt rapportage op basis van inkomsten en bestellingen toegestaan. Met het selectievakje Order Confirmation (Bevestiging bestellen) kunt u ook aanbevelingen uitvoeren, zoals &quot;People that purchase product x also purchase product y.&quot; (Personen die het product hebben gekocht).

>[!NOTE]
>
>Als gebruikers aankopen doen op uw website, raden we u aan een bevestigingsvak voor bestellingen te implementeren, zelfs als u Analytics for Target (A4T) gebruikt voor uw rapportage.

1. Voeg op de pagina met orderdetails het mbox-script in volgens het onderstaande model.
1. Vervang de WOORDEN IN KAPITAALLETTERS door dynamische of statische waarden uit de catalogus.

   >[!NOTE]
   >
   >Gebruik komma&#39;s als scheidingsteken om meerdere product-id&#39;s van elkaar te scheiden.

   **Tip:** U kunt ook ordergegevens in een willekeurige box doorgeven (hiervoor hoeft geen naam te worden gegeven  `orderConfirmPage`). U kunt ook ordergegevens in meerdere vakken in dezelfde campagne doorgeven.

   ```
   <script type="text/javascript"> 
   adobe.target.trackEvent({ 
       "mbox": "orderConfirmPage", 
       "params":{  
           "orderId": "ORDER ID FROM YOUR ORDER PAGE",  
           "orderTotal": "ORDER TOTAL FROM YOUR ORDER PAGE",  
           "productPurchasedId": "PRODUCT ID FROM YOUR ORDER PAGE, PRODUCT ID2, PRODUCT ID3"  
       } 
   }); 
   </script> 
   ```

In het bevestigingsvak Volgorde worden de volgende parameters gebruikt:

| Parameter | Beschrijving |
|--- |--- |
| orderId | Unieke waarde om een order voor het tellen van conversies te identificeren.<br>De `orderId` moet uniek zijn. Dubbele orders worden genegeerd in rapporten. |
| orderTotal | Monetaire waarde van de aankoop.<br>Geef het valutasymbool niet door. Gebruik een decimaalteken (geen komma) om decimale waarden aan te geven. |
| productPurchasedId (optioneel) | Door komma&#39;s gescheiden lijst met product-id&#39;s die in de order zijn aangeschaft.<br>Deze product-id&#39;s worden in het auditrapport weergegeven ter ondersteuning van aanvullende rapportanalyse. |