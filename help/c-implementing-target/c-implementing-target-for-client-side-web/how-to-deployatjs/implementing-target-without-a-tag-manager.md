---
keywords: implement target;implementation;implement at.js;tag manager
description: Informatie over het implementeren van Adobe Target zonder gebruik te maken van een tagbeheer (Adobe starten of Dynamisch tagbeheer).
title: Doel implementeren zonder tagbeheer
feature: implementation general
subtopic: Getting Started
topic: Standard
uuid: 3ecc041a-42d8-40f8-90be-7856e1d3d080
translation-type: tm+mt
source-git-commit: 95450abc32be19d04b791af3c62673e9411ab53c
workflow-type: tm+mt
source-wordcount: '1514'
ht-degree: 4%

---


# Doel implementeren zonder tagbeheer{#implement-target-without-a-tag-manager}

Informatie over het implementeren [!DNL Adobe Target] zonder gebruik te maken van een tagbeheer ([!DNL Adobe Launch] of [!DNL Dynamic Tag Manager]).

>[!NOTE]
>
>[Adobe Launch](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/cmp-implementing-target-using-adobe-launch.md#topic_5234DDAEB0834333BD6BA1B05892FC25) is de voorkeursmethode voor het implementeren van Target en de bibliotheek at.js. De volgende informatie is niet van toepassing wanneer het gebruiken van de Lancering van Adobe om Doel uit te voeren.

Als u de [!UICONTROL Implementation] pagina wilt openen, klikt u op **[!UICONTROL Administration]** > **[!UICONTROL Implementation]**.

U kunt de volgende instellingen opgeven op deze pagina:

* Accountgegevens
* Implementatiemethoden
* Profiel-API
* Foutopsporingsgereedschappen
* Privacy

>[!NOTE]
>
>U kunt instellingen in de bibliotheek at.js overschrijven in plaats van de instellingen in de gebruikersinterface van Target Standard/Premium te configureren of REST API&#39;s te gebruiken. Zie [targetGlobalSettings()](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetgobalsettings.md)voor meer informatie.

## Accountgegevens

U kunt de volgende accountdetails weergeven. Deze instellingen kunnen niet worden gewijzigd.

| Instelling | Beschrijving |
| --- | --- |
| Clientcode | De clientcode is een clientspecifieke reeks tekens die vaak vereist zijn bij het gebruik van de doel-API&#39;s. |
| IMS Organisatie-id | Deze id koppelt uw implementatie aan uw [!DNL Adobe Experience Cloud] account. |

## Implementatiemethoden

U kunt de volgende instellingen configureren in het deelvenster Implementatiemethoden:

### Algemene instellingen

>[!NOTE]
>
>Deze instellingen worden toegepast op alle .js- [!DNL Target] bibliotheken. Nadat u wijzigingen in de [!UICONTROL Implementation methods] sectie hebt uitgevoerd, moet u de bibliotheek downloaden en bijwerken in de implementatie.

| Instelling | Beschrijving |
| --- | --- |
| Laden van pagina ingeschakeld (Automatisch een globaal selectievakje maken | Geef op of u de algemene mbox-aanroep in het bestand at.js wilt insluiten om automatisch op elke pagina te starten. |
| Globale mbox | Selecteer een naam voor het globale vakje. Deze naam is standaard target-global-mbox.<br>Speciale tekens, zoals ampersands (&amp;), kunnen worden gebruikt in mbox-namen met at.js. |
| Time-out (seconden) | Als [!DNL Target] niet binnen de gedefinieerde periode met inhoud reageert, worden de wachttijden van de serveraanroep en de standaardinhoud weergegeven. Aanvullende aanroepen worden nog steeds geprobeerd tijdens de sessie van de bezoeker. De standaardwaarde is 5 seconden.<br>De bibliotheek at.js gebruikt de time-outinstelling in `XMLHttpRequest`. De time-out begint wanneer de aanvraag wordt geactiveerd en stopt wanneer een reactie van de server wordt [!DNL Target] opgehaald. For more information, see [XMLHttpRequest.timeout](https://developer.mozilla.org/en-US/docs/Web/API/XMLHttpRequest/timeout) on the Mozilla Developer Network.<br>Als de opgegeven time-out optreedt voordat de reactie wordt ontvangen, wordt standaardinhoud weergegeven en wordt de bezoeker mogelijk geteld als een deelnemer aan een activiteit omdat alle gegevensverzameling aan de [!DNL Target] rand plaatsvindt. Als de aanvraag de [!DNL Target] rand bereikt, wordt de bezoeker geteld.<br>Denk aan het volgende wanneer u de time-outinstelling configureert:<ul><li>Als de waarde te laag is, kunnen gebruikers de standaardinhoud het grootste deel van de tijd zien, hoewel de bezoeker als deelnemer aan de activiteit kon worden geteld.</li><li>Als de waarde te hoog is, kunnen bezoekers lege gebieden op uw webpagina of lege pagina&#39;s zien als u de hoofdtekst langere tijd verbergt.</li></ul>Om een beter inzicht in mbox reactietijden te krijgen, bekijk het lusje van het Netwerk in de Hulpmiddelen van de Ontwikkelaar van uw browser. U kunt ook controlehulpmiddelen voor webprestaties van derden gebruiken, zoals Catchpoint.<br>**Opmerking**: De instelling [bezoekerApiTimeout](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetgobalsettings.md) zorgt ervoor dat [!DNL Target] niet te lang op de reactie van de bezoeker-API wordt gewacht. Deze instelling en de instelling Time-out voor at.js die hier wordt beschreven, zijn niet van invloed op elkaar. |
| Profiellevensduur | Deze instelling bepaalt hoe lang bezoekersprofielen worden opgeslagen. Profielen worden standaard twee weken opgeslagen. Dit kan tot 90 dagen worden verhoogd.<br>Als u de instelling voor de levensduur van het profiel wilt wijzigen, neemt u contact op met de [klantenservice](https://helpx.adobe.com/nl/contact/enterprise-support.ec.html). |

### Hoofduitvoeringsmethode

>[!IMPORTANT]
>
>Het team van het Doel steunt allebei at.js 1.*x* en at.js 2.*x*. Voer een upgrade uit naar de meest recente update van een van de belangrijkste versies van at.js om ervoor te zorgen dat u een ondersteunde versie uitvoert.

Klik op de desbetreffende **[!UICONTROL Download]** knop om de gewenste versie van at.js te downloaden.

Als u de instellingen bij .js wilt bewerken, klikt u **[!UICONTROL Edit]** naast de gewenste versie bij.js.

>[!IMPORTANT]
>
>Voordat u deze standaardinstellingen wijzigt, moet u eerst de [klantenservice](/help/cmp-resources-and-contact-information.md) raadplegen, zodat de huidige implementatie niet wordt beïnvloed.

Naast de hierboven beschreven instellingen zijn ook de volgende specifieke instellingen van at.js beschikbaar:

| Instelling | Beschrijving |
|--- |--- |
| Aangepaste bibliotheekkoptekst | Voeg aangepaste JavaScript toe die u boven aan de bibliotheek wilt opnemen. |
| Aangepaste bibliotheekvoettekst | Voeg aangepaste JavaScript toe die u onder aan de bibliotheek wilt opnemen. |

### Profiel-API

Schakel verificatie voor batchupdates via API in of uit en genereer een profielverificatietoken.

Zie [Profiel-API-instellingen](/help/c-implementing-target/c-considerations-before-you-implement-target/c-methods-to-get-data-into-target/profile-api-settings.md)voor meer informatie.

### Foutopsporingsgereedschappen

Genereer een machtigingstoken om geavanceerde [!DNL Target] foutopsporingsgereedschappen te gebruiken. Klik op **[!UICONTROL Generate New Authentication Token]**.

![Nieuwe verificatietoken genereren](/help/c-implementing-target/c-considerations-before-you-implement-target/c-methods-to-get-data-into-target/assets/debugger-auth-token.png)

### Privacy

Met deze instellingen kunt u gegevens gebruiken in overeenstemming [!DNL Target] met de toepasselijke privacywetgeving.

Kies het gewenste plaatsen van de IP van de Bezoeker van de Verduistering adresdrop-down lijst:

* Recentste octet-verduistering
* Volledige IP-verduistering
* Geen

Zie [Privacy](/help/c-implementing-target/c-considerations-before-you-implement-target/c-privacy/privacy.md)voor meer informatie.

>[!NOTE]
>
>De optie Verouderde browserondersteuning was beschikbaar in versie 0.js 0.9.3 en eerder. Deze optie is verwijderd in versie 0.js 0.9.4. Zie [Ondersteunde browsers](/help/c-implementing-target/c-considerations-before-you-implement-target/supported-browsers.md)voor een lijst met browsers die worden ondersteund door at.js.<br>Verouderde browsers zijn oudere browsers die geen volledige ondersteuning bieden voor CORS (Cross Origin Resource Sharing). Deze browsers zijn: Browsers van Internet Explorer ouder dan versie 11 en Safari versies 6 en lager. Als ondersteuning voor verouderde browsers was uitgeschakeld, heeft Target geen inhoud geleverd of heeft Target geen bezoekers geteld in rapporten over deze browsers. Als deze optie is ingeschakeld, wordt u aangeraden kwaliteitsborging toe te passen in alle oudere browsers, zodat de klant er optimaal van profiteert.

## Downloaden om.js {#concept_1E1F958F9CCC4E35AD97581EFAF659E2}

Instructies om de bibliotheek te downloaden met de [!DNL Target] interface of de download-API.

>[!NOTE]
>
>* [Adobe Launch](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/cmp-implementing-target-using-adobe-launch.md#topic_5234DDAEB0834333BD6BA1B05892FC25) is de voorkeursmethode voor het implementeren van Target en de bibliotheek at.js. De volgende informatie is niet van toepassing wanneer het gebruiken van de Lancering van Adobe om Doel uit te voeren.
   >
   >
* Het team van het Doel steunt allebei at.js 1.*x* en at.js 2.*x*. Voer een upgrade uit naar de meest recente update van een van de belangrijkste versies van at.js om ervoor te zorgen dat u een ondersteunde versie uitvoert. Voor meer informatie over wat in elke versie is, zie [bij.js de Details](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md#reference_DBB5EDB79EC44E558F9E08D4774A0F7A)van de Versie.


### Download at.js gebruikend de interface van het Doel {#section_1F5EE401C2314338910FC57F9592894E}

Downloaden [!DNL at.js] vanaf de [!DNL Target] interface:

1. Klik op **[!UICONTROL Administration]** > **[!UICONTROL Implementation]**.
1. Klik in de [!UICONTROL Implementation methods] sectie op de **[!UICONTROL Download]** knop naast de gewenste versie at.js.

### Download at.js met de API voor doeldownloaden {#section_C0D9D2A9068144708D08526BA5CA10D0}

Downloaden [!DNL at.js] met de API.

1. Haal uw clientcode op.

   De clientcode is beschikbaar boven aan de pagina **[!UICONTROL Administration]** > **[!UICONTROL Implementation]** van de [!DNL Target] interface.

1. Haal uw beheerdersnummer op.

   Deze URL laden:

   ```
   https://admin.testandtarget.omniture.com/rest/v1/endpoint/<varname>client code</varname>
   ```

   Vervangen `client code` door de clientcode uit stap 1.

   Het resultaat van het laden van deze URL moet er ongeveer als volgt uitzien:

   ```
   { 
     "api": "https://admin6.testandtarget.omniture.com/admin/rest/v1" 
   }
   ```

   In dit voorbeeld is &#39;6&#39; het beheerdersnummer.

1. Downloaden [!DNL at.js].

   Laad deze URL met de volgende structuur:

   ```
   https://admin<varname>admin number</varname>.testandtarget.omniture.com/admin/rest/v1/libraries/atjs/download?client=<varname>client code</varname>&version=<version number>
   ```

   * Vervangen `admin number` door uw beheerdersnummer.
   * Vervangen `client code` door de clientcode uit stap 1.
   * Vervangen `version number` door het gewenste at.js versienummer (bijvoorbeeld 2.2).

   >[!IMPORTANT]
   >
   >Het team van het Doel handhaaft slechts twee versies van [!DNL at.js]-de huidige versie en de tweede-recentste versie. Voer [!DNL at.js] indien nodig een upgrade uit om ervoor te zorgen dat u een ondersteunde versie gebruikt. Voor meer informatie over wat in elke versie is, zie [bij.js de Details](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md#reference_DBB5EDB79EC44E558F9E08D4774A0F7A)van de Versie.

   Wanneer u deze URL laadt, wordt het downloaden van uw aangepaste [!DNL at.js] bestand gestart.

## at.js-implementatie {#concept_03CFA86973A147839BEB48A06FEE5E5A}

at.js moet worden geïmplementeerd in het `<head>` element van elke pagina van uw website.

Een typische implementatie van Doel die geen markeringsmanager zoals [Adobe Lancering](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/cmp-implementing-target-using-adobe-launch.md#topic_5234DDAEB0834333BD6BA1B05892FC25) of [Dynamisch Beheer](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/implementing-target-using-dynamic-tag-management.md#concept_3A40AF6FFC0E4FD2AA81B303A79D0B96) van de Markering gebruikt ziet als volgt uit:

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
* De opties Preconnect en Prefetch zijn opties die u kunnen helpen uw webpagina&#39;s sneller te laden. Als u deze configuraties gebruikt, zorg ervoor dat u `<client code>` met uw eigen cliëntcode vervangt, die u van de **[!UICONTROL Administration]** > **[!UICONTROL Implementation] pagina kunt verkrijgen.
* Als u een gegevenslaag hebt, is het beter om zoveel mogelijk in de pagina&#39;s te definiëren voordat at.js wordt geladen. `<head>` Deze plaatsing verstrekt het maximumvermogen om deze informatie in Doel voor verpersoonlijking te gebruiken.
* Speciale doelfuncties, zoals `targetPageParams()`, `targetPageParamsAll()`Data Providers, en `targetGlobalSettings()` moeten worden gedefinieerd na de gegevenslaag en voordat at.js wordt geladen. U kunt deze bestanden ook opslaan in de [!UICONTROL Library Header] sectie van de [!UICONTROL Edit at.js Settings] pagina en opslaan als onderdeel van de bibliotheek at.js zelf. Zie [at.js voor meer informatie over deze functies](/help/c-implementing-target/c-implementing-target-for-client-side-web/cmp-atjs-functions.md).
* Als u JavaScript-hulplijnbibliotheken gebruikt, zoals jQuery, neemt u deze op voordat u Target gaat gebruiken, zodat u de syntaxis en methoden van deze bibliotheken kunt gebruiken wanneer u Target-ervaringen opstelt.
* Neem om.js op in de `<head>` pagina&#39;s.

## Omzettingen bijhouden {#task_E85D2F64FEB84201A594F2288FABF053}

In het vak Bevestiging van bestelling worden gegevens over bestellingen op uw site vastgelegd en wordt rapportage op basis van inkomsten en bestellingen toegestaan. Met het selectievakje Order Confirmation (Bevestiging bestellen) kunt u ook aanbevelingen uitvoeren, zoals &quot;People that purchase product x also purchase product y.&quot; (Personen die het product hebben gekocht).

>[!NOTE]
>
>Als gebruikers aankopen doen op uw website, raden we u aan een bevestigingsvak voor bestellingen te implementeren, zelfs als u Analytics for Target (A4T) gebruikt voor uw rapportage.

1. Voeg op de pagina met orderdetails het mbox-script in volgens het onderstaande model.
1. Vervang de WOORDEN IN KAPITAALLETTERS door dynamische of statische waarden uit de catalogus.

   >[!NOTE]
   >
   >Gebruik komma&#39;s als scheidingsteken om meerdere product-id&#39;s van elkaar te scheiden.

   **Tip:** U kunt ook ordergegevens in een willekeurige box doorgeven (hiervoor hoeft geen naam te worden gegeven `orderConfirmPage`). U kunt ook ordergegevens in meerdere vakken in dezelfde campagne doorgeven.

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