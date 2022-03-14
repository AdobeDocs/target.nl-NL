---
keywords: doel implementeren;implementatie;implementatie uitvoeren op.js;tagbeheer;apparaatbeslissingen;op apparaatbeslissingen
description: Leer hoe u de instellingen opgeeft (accountgegevens, implementatiemethoden, enz.) de Adobe [!DNL Target] bibliotheek at.js zonder een tagbeheer te gebruiken.
title: Kan ik implementeren [!DNL Target] zonder tagbeheer?
feature: Implement Server-side
role: Developer
exl-id: cb57f6b8-43cb-485d-a7ea-12db8170013f
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '1630'
ht-degree: 3%

---

# Implementeren [!DNL Target] zonder tagbeheer

Informatie over de uitvoering [!DNL Adobe Target] zonder gebruik te maken van tagbeheer of tags in [!DNL Adobe Experience Platform].

>[!NOTE]
>
>Tags in [Adobe Experience Platform](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/cmp-implementing-target-using-adobe-launch.md#topic_5234DDAEB0834333BD6BA1B05892FC25) is de voorkeursmethode voor de implementatie [!DNL Target] en de bibliotheek at.js. De volgende informatie is niet van toepassing wanneer u tags gebruikt in [!DNL Adobe Experience Platform] uitvoeren [!DNL Target].

Om toegang te krijgen tot [!UICONTROL Implementation] pagina, klikt u op **[!UICONTROL Administration]** > **[!UICONTROL Implementation]**.

U kunt de volgende instellingen opgeven op deze pagina:

* Accountgegevens
* Implementatiemethoden
* Profiel-API
* Foutopsporingsgereedschappen
* Privacy

>[!NOTE]
>
>U kunt instellingen in de bibliotheek at.js overschrijven in plaats van de instellingen in het dialoogvenster [!DNL Target Standard/Premium] UI of door REST APIs te gebruiken. Zie voor meer informatie [targetGlobalSettings()](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/targetgobalsettings.md).

## Accountgegevens

U kunt de volgende accountdetails weergeven. Deze instellingen kunnen niet worden gewijzigd.

| Instelling | Beschrijving |
| --- | --- |
| [!UICONTROL Client Code] | De clientcode is een clientspecifieke reeks tekens die vaak vereist zijn bij het gebruik van de [!DNL Target] API&#39;s. |
| [!UICONTROL IMS Organization ID] | Deze id koppelt uw implementatie aan uw [!DNL Adobe Experience Cloud] account. |
| [!UICONTROL On-Device Decisioning] | Schuif de schakeloptie naar de stand &quot;aan&quot; om de apparaatbesturing in te schakelen.<br>Op apparaat beslissend laat u uw A/B en in het voorgeheugen onderbrengen [!UICONTROL Experience Targeting] (XT) voert campagnes op uw server en in-geheugenbesluit bij bijna-nul latentie uit. Zie voor meer informatie [Inleiding tot apparaatbeslissingen](https://adobetarget-sdks.gitbook.io/docs/on-device-decisioning/introduction-to-on-device-decisioning) in de *[!DNL Adobe Target]SDK&#39;s* hulplijn. |
| [!UICONTROL Include all existing on-device decisioning qualified activities in the artifact.] | (Voorwaardelijk) Deze optie wordt weergegeven als u het bepalen op het apparaat inschakelt.<br>Schuif de schakeloptie naar de positie &quot;aan&quot; als u wilt dat al uw live doelactiviteiten die in aanmerking komen voor beslissingen op het apparaat automatisch worden opgenomen in het artefact.<br>Als u deze schakeloptie uitschakelt, moet u alle beslissingsactiviteiten op het apparaat opnieuw maken en activeren, zodat deze worden opgenomen in het gegenereerde regelartefact. |

## Implementatiemethoden

U kunt de volgende instellingen configureren in het deelvenster Implementatiemethoden:

### Algemene instellingen

>[!NOTE]
>
>Deze instellingen worden toegepast op alle [!DNL Target] .js-bibliotheken. Nadat u wijzigingen hebt aangebracht in de sectie Implementatiemethoden, moet u de bibliotheek downloaden en bijwerken in uw implementatie.

| Instelling | Beschrijving |
| --- | --- |
| Laden van pagina ingeschakeld (Automatisch een globaal selectievakje maken | Geef op of u de algemene mbox-aanroep in het bestand at.js wilt insluiten om automatisch op elke pagina te starten. |
| Globale mbox | Selecteer een naam voor het globale vakje. Deze naam is standaard target-global-mbox.<br>Speciale tekens, zoals ampersands (&amp;), kunnen worden gebruikt in mbox-namen met at.js. |
| Time-out (seconden) | Indien [!DNL Target] reageert niet met inhoud binnen de gedefinieerde periode, de wachttijden van de serveraanroep zijn verstreken en de standaardinhoud wordt weergegeven. Aanvullende aanroepen worden nog steeds geprobeerd tijdens de sessie van de bezoeker. De standaardwaarde is 5 seconden.<br>De bibliotheek at.js gebruikt de time-outinstelling in `XMLHttpRequest`. De time-out begint wanneer de aanvraag wordt geactiveerd en stopt wanneer [!DNL Target] krijgt een reactie van de server. Zie voor meer informatie [XMLHttpRequest.timeout](https://developer.mozilla.org/en-US/docs/Web/API/XMLHttpRequest/timeout) op het Mozilla Developer Network.<br>Als de opgegeven time-out optreedt voordat de reactie wordt ontvangen, wordt standaardinhoud weergegeven en wordt de bezoeker wellicht geteld als een deelnemer aan een activiteit omdat alle gegevensverzameling plaatsvindt op het tabblad [!DNL Target] rand. Als de aanvraag de [!DNL Target] edge, de bezoeker wordt geteld.<br>Denk aan het volgende wanneer u de time-outinstelling configureert:<ul><li>Als de waarde te laag is, kunnen gebruikers de standaardinhoud het grootste deel van de tijd zien, hoewel de bezoeker als deelnemer aan de activiteit kon worden geteld.</li><li>Als de waarde te hoog is, kunnen bezoekers lege gebieden op uw webpagina of lege pagina&#39;s zien als u de hoofdtekst langere tijd verbergt.</li></ul>Om een beter inzicht in mbox reactietijden te krijgen, bekijk het lusje van het Netwerk in de Hulpmiddelen van de Ontwikkelaar van uw browser. U kunt ook controlehulpmiddelen voor webprestaties van derden gebruiken, zoals Catchpoint.<br>**Opmerking**: De [bezoekerApiTimeout](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/targetgobalsettings.md) het plaatsen zorgt ervoor dat [!DNL Target] wacht niet te lang op de reactie van de bezoeker-API. Deze instelling en de instelling Time-out voor at.js die hier wordt beschreven, zijn niet van invloed op elkaar. |
| Profiellevensduur | Deze instelling bepaalt hoe lang bezoekersprofielen worden opgeslagen. Profielen worden standaard twee weken opgeslagen. Deze instelling kan tot 90 dagen worden verhoogd.<br>Als u de instelling voor de levensduur van het profiel wilt wijzigen, neemt u contact op met [Clientservice](https://helpx.adobe.com/nl/contact/enterprise-support.ec.html). |

### Hoofduitvoeringsmethode

>[!IMPORTANT]
>
>Het team van het Doel steunt allebei at.js 1.*x* en te.js 2.*x*. Voer een upgrade uit naar de meest recente update van een van de belangrijkste versies van at.js om ervoor te zorgen dat u een ondersteunde versie uitvoert.

Klik op de betreffende toepassing om de gewenste versie van at.js te downloaden. **[!UICONTROL Download]** knop.

Klik op **[!UICONTROL Edit]** naast de gewenste versie at.js.

>[!IMPORTANT]
>
>Voordat u deze standaardinstellingen wijzigt, moet u eerst contact opnemen met [Clientservice](/help/main/cmp-resources-and-contact-information.md) dus u heeft geen invloed op uw huidige implementatie.

Naast de hierboven beschreven instellingen zijn ook de volgende specifieke instellingen van at.js beschikbaar:

| Instelling | Beschrijving |
|--- |--- |
| Aangepaste bibliotheekkoptekst | Voeg aangepaste JavaScript toe die u boven aan de bibliotheek wilt opnemen. |
| Aangepaste bibliotheekvoettekst | Voeg aangepaste JavaScript toe die u onder aan de bibliotheek wilt opnemen. |

### Profiel-API

Schakel verificatie voor batchupdates via API in of uit en genereer een profielverificatietoken.

Zie voor meer informatie [Profiel-API-instellingen](/help/main/c-implementing-target/c-considerations-before-you-implement-target/c-methods-to-get-data-into-target/profile-api-settings.md).

### Foutopsporingsgereedschappen

Genereer een machtigingstoken voor geavanceerd gebruik [!DNL Target] foutopsporingsgereedschappen. Klik op **[!UICONTROL Generate New Authentication Token]**.

![Nieuwe verificatietoken genereren](/help/main/c-implementing-target/c-considerations-before-you-implement-target/c-methods-to-get-data-into-target/assets/debugger-auth-token.png)

### Privacy

Met deze instellingen kunt u [!DNL Target] in overeenstemming met de toepasselijke wetgeving inzake gegevensbescherming.

Kies het gewenste plaatsen van de IP van de Bezoeker van de Verduistering adresdrop-down lijst:

* Recentste octet-verduistering
* Volledige IP-verduistering
* Geen

Zie voor meer informatie [Privacy](/help/main/c-implementing-target/c-considerations-before-you-implement-target/c-privacy/privacy.md).

>[!NOTE]
>
>De optie Verouderde browserondersteuning was beschikbaar in versie 0.js 0.9.3 en eerder. Deze optie is verwijderd in versie 0.js 0.9.4. Voor een lijst met browsers die door at.js worden ondersteund, raadpleegt u [Ondersteunde browsers](/help/main/c-implementing-target/c-considerations-before-you-implement-target/supported-browsers.md).<br>Verouderde browsers zijn oudere browsers die geen volledige ondersteuning bieden voor CORS (Cross Origin Resource Sharing). Deze browsers zijn: Browsers van Internet Explorer ouder dan versie 11 en Safari versies 6 en lager. Als ondersteuning voor verouderde browsers was uitgeschakeld, heeft Target geen inhoud geleverd of heeft Target geen bezoekers geteld in rapporten over deze browsers. Als deze optie is ingeschakeld, wordt u aangeraden kwaliteitsborging toe te passen in alle oudere browsers, zodat de klant er optimaal van profiteert.

## Downloaden om.js {#concept_1E1F958F9CCC4E35AD97581EFAF659E2}

Instructies om de bibliotheek te downloaden met de [!DNL Target] of de Download API.

>[!NOTE]
>
>* [[!DNL Adobe Experience Platform]](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/cmp-implementing-target-using-adobe-launch.md#topic_5234DDAEB0834333BD6BA1B05892FC25) is de voorkeursmethode voor de implementatie [!DNL Target] en de bibliotheek at.js. De volgende informatie is niet van toepassing wanneer u tags gebruikt in [!DNL Adobe Experience Platform] uitvoeren [!DNL Target].
>
>* De [!DNL Target] team steunt allebei at.js 1.*x* en te.js 2.*x*. Voer een upgrade uit naar de meest recente update van een van de belangrijkste versies van at.js om ervoor te zorgen dat u een ondersteunde versie uitvoert. Voor meer informatie over wat in elke versie is, zie [at.js - Versiedetails](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md#reference_DBB5EDB79EC44E558F9E08D4774A0F7A).


### Download om.js met de [!DNL Target] interface {#section_1F5EE401C2314338910FC57F9592894E}

Downloaden [!DNL at.js] van de [!DNL Target] interface:

1. Klik op **[!UICONTROL Administration]** > **[!UICONTROL Implementation]**.
1. Van de [!UICONTROL Implementation methods] klikt u op de **[!UICONTROL Download]** naast de gewenste versie at.js.

### Download om.js met de [!DNL Target] API downloaden {#section_C0D9D2A9068144708D08526BA5CA10D0}

Downloaden [!DNL at.js] met de API.

1. Haal uw clientcode op.

   Uw clientcode is beschikbaar boven aan het dialoogvenster **[!UICONTROL Administration]** > **[!UICONTROL Implementation]** pagina van de [!DNL Target] interface.

1. Haal uw beheerdersnummer op.

   Deze URL laden:

   ```
   https://admin.testandtarget.omniture.com/rest/v1/endpoint/<varname>client code</varname>
   ```

   Vervangen `client code` met de clientcode uit stap 1.

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

   * Vervangen `admin number` met uw beheerdersnummer.
   * Vervangen `client code` met de clientcode uit stap 1.
   * Vervangen `version number` met het gewenste at.js versienummer (bijvoorbeeld 2.2).

   >[!IMPORTANT]
   >
   >Het team van het Doel handhaaft slechts twee versies [!DNL at.js]—de huidige versie en de tweede nieuwste versie. Voer een upgrade uit [!DNL at.js] om ervoor te zorgen dat u een ondersteunde versie uitvoert. Voor meer informatie over wat in elke versie is, zie [at.js - Versiedetails](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md#reference_DBB5EDB79EC44E558F9E08D4774A0F7A).

   Wanneer u deze URL laadt, wordt het downloaden van uw aangepaste [!DNL at.js] bestand.

## at.js-implementatie {#concept_03CFA86973A147839BEB48A06FEE5E5A}

te.js moet worden geïmplementeerd in de `<head>` element van elke pagina van uw website.

Een standaardimplementatie van Doel waarbij geen tagbeheer wordt gebruikt, zoals tags in [[!DNL Adobe Experience Platform]](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/cmp-implementing-target-using-adobe-launch.md#topic_5234DDAEB0834333BD6BA1B05892FC25) ziet er als volgt uit:

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

* Het HTML5 Doctype (bijvoorbeeld `<!doctype html>`) moet worden gebruikt. Niet-ondersteunde of oudere documenttypen kunnen ertoe leiden dat Target geen aanvraag kan indienen.
* De opties Preconnect en Prefetch zijn opties die u kunnen helpen uw webpagina&#39;s sneller te laden. Als u deze configuraties gebruikt, zorg ervoor dat u vervangt `<client code>` met uw eigen clientcode, die u kunt verkrijgen via de **[!UICONTROL Administration]** > **[!UICONTROL Implementation] pagina.
* Als u een gegevenslaag hebt, kunt u het beste zo veel mogelijk definiëren in het dialoogvenster `<head>` van uw pagina&#39;s voordat om.js wordt geladen. Deze plaatsing verstrekt de maximumcapaciteit om deze informatie in Doel voor verpersoonlijking te gebruiken.
* Speciale doelfuncties, zoals `targetPageParams()`, `targetPageParamsAll()`, gegevensleveranciers, en `targetGlobalSettings()` moet worden gedefinieerd na de gegevenslaag en voordat at.js wordt geladen. U kunt deze functies ook opslaan in het dialoogvenster [!UICONTROL Library Header] van de [!UICONTROL Edit at.js Settings] en wordt opgeslagen als onderdeel van de bibliotheek at.js zelf. Zie voor meer informatie over deze functies [at.js-functies](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/cmp-atjs-functions.md).
* Als u JavaScript-hulplijnbibliotheken gebruikt, zoals jQuery, neemt u deze vóór Target op, zodat u de syntaxis en methoden van deze bibliotheken kunt gebruiken wanneer u Target-ervaringen opstelt.
* Omvat om.js in `<head>` van uw pagina&#39;s.

## Omzettingen bijhouden {#task_E85D2F64FEB84201A594F2288FABF053}

In het vak Bevestiging van bestelling worden gegevens over bestellingen op uw site vastgelegd en wordt rapportage op basis van inkomsten en bestellingen toegestaan. Met het selectievakje Order Confirmation (Bevestiging bestellen) kunt u ook aanbevelingen uitvoeren, zoals &quot;People that purchase product x also purchase product y.&quot; (Personen die het product hebben gekocht).

>[!NOTE]
>
>Als gebruikers aankopen doen op uw website, raadt Adobe u aan een bevestigingsvak voor bestellingen te implementeren, zelfs als u Analytics for Target (A4T) gebruikt voor uw rapportage.

1. Voeg op de pagina met orderdetails het mbox-script in volgens het onderstaande model.
1. Vervang de WOORDEN IN KAPITAALLETTERS door dynamische of statische waarden uit de catalogus.

   >[!NOTE]
   >
   >Gebruik komma&#39;s als scheidingsteken om meerdere product-id&#39;s van elkaar te scheiden.

   **Tip:** U kunt ook ordergegevens in een willekeurige box doorgeven (er hoeft geen naam aan te worden gegeven) `orderConfirmPage`). U kunt ook ordergegevens in meerdere vakken in dezelfde campagne doorgeven.

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
