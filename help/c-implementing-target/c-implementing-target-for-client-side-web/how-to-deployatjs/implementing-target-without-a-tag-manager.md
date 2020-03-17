---
keywords: order confirmation;orderConfirmPage
description: Informatie over het implementeren van Adobe Target zonder een tagbeheer (Adobe Launch of Dynamic Tag Management).
title: Doel implementeren zonder tagbeheer
subtopic: Getting Started
topic: Standard
uuid: 3ecc041a-42d8-40f8-90be-7856e1d3d080
translation-type: tm+mt
source-git-commit: c6ae795eceaecad73cdbad520712f1fba1eb7c8a

---


# Doel implementeren zonder tagbeheer{#implement-target-without-a-tag-manager}

Informatie over het implementeren [!DNL Adobe Target] zonder gebruik te maken van een tagbeheer (Adobe Launch of Dynamic Tag Management).

## Doel implementeren zonder tagbeheer {#topic_397FFA3D6918456BBE02A9FBE9537894}

Informatie over het implementeren van Adobe Target zonder een tagbeheer (Adobe Launch of Dynamic Tag Management).

>[!NOTE]
>
>[Adobe Launch](../../../c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/cmp-implementing-target-using-adobe-launch.md#topic_5234DDAEB0834333BD6BA1B05892FC25) is de voorkeursmethode voor de implementatie van Target en de bibliotheek at.js. De volgende informatie is niet van toepassing wanneer u Adobe Launch gebruikt om Target te implementeren.

## at.js-configuraties {#concept_2FA0456607D04F82B0539C5BF5309812}

Informatie die u helpt bij het instellen van verschillende instellingen op de pagina Instellingen at.js.

>[!NOTE]
>
>[Adobe Launch](../../../c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/cmp-implementing-target-using-adobe-launch.md#topic_5234DDAEB0834333BD6BA1B05892FC25) is de voorkeursmethode voor de implementatie van Target en de bibliotheek at.js. De volgende informatie is niet van toepassing wanneer u Adobe Launch gebruikt om Target te implementeren.

>[!NOTE]
>
>U kunt instellingen in de bibliotheek at.js overschrijven in plaats van de instellingen in de gebruikersinterface van Target Standard/Premium te configureren of REST API&#39;s te gebruiken. Zie [targetGlobalSettings()](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetgobalsettings.md)voor meer informatie.

De [!UICONTROL Settings] pagina openen:

1. Klik op **[!UICONTROL Setup]** > **[!UICONTROL Implementation]**.
1. Selecteer **[!UICONTROL at.js]** > **[!UICONTROL Edit at.js Settings]**.

## Instellingen voor levering van inhoud {#section_118D290DFC444509AD8E4AE86C9D92C0}

Raadpleeg de klantenservice voordat u deze instellingen wijzigt. Deze instellingen zijn vereist voor de meeste implementaties.

| Instelling | Beschrijving |
|--- |--- |
| Globale mbox automatisch maken | Geef op of u de algemene mbox-aanroep in het bestand at.js wilt insluiten om automatisch op elke pagina te starten.<br>Het wijzigen van deze instelling heeft invloed op zowel at.js als mbox.js. |
| Algemene naam van box | Selecteer een naam voor het globale vakje. Deze naam is standaard target-global-mbox.<br>Speciale tekens, zoals ampersands (&amp;), kunnen worden gebruikt in mbox-namen met at.js.<br>Het wijzigen van deze instelling heeft invloed op zowel at.js als mbox.js. |

## Geavanceerde instellingen {#section_33B697B77BA64A01B5939D7EC75231F2}

| Instelling | Beschrijving |
|--- |--- |
| Clientcode | De clientcode is een clientspecifieke reeks tekens die vaak vereist zijn bij het gebruik van de doel-API&#39;s.<br>Deze instelling kan niet worden gewijzigd. |
| IMS Organisatie-id | Deze id koppelt uw implementatie aan uw [!DNL Adobe Experience Cloud] account.<br>Deze instelling kan niet worden gewijzigd. |
| Profiellevensduur | Deze instelling bepaalt hoe lang bezoekersprofielen worden opgeslagen. Profielen worden standaard twee weken opgeslagen. Dit kan tot 90 dagen worden verhoogd.<br>Als u de instelling voor de levensduur van het profiel wilt wijzigen, neemt u contact op met de [klantenservice](https://helpx.adobe.com/contact/enterprise-support.ec.html). |
| X-domein | Bepaalt of browser koekjes in uw eigen domein (1st partijkoekjes), het domein van het Doel, of allebei plaatst.<br>Het wijzigen van deze instelling heeft invloed op zowel at.js als mbox.js. |
| Time-out | Als [!DNL Target] niet binnen de gedefinieerde periode met inhoud reageert, worden de wachttijden van de serveraanroep en de standaardinhoud weergegeven. Aanvullende aanroepen worden nog steeds geprobeerd tijdens de sessie van de bezoeker. De standaardwaarde is 5 seconden.<br>Het wijzigen van deze instelling heeft invloed op zowel at.js als mbox.js.<br>De bibliotheek at.js gebruikt de time-outinstelling in `XMLHttpRequest`. De time-out begint wanneer de aanvraag wordt geactiveerd en stopt wanneer Target een reactie van de server krijgt. For more information, see [XMLHttpRequest.timeout](https://developer.mozilla.org/en-US/docs/Web/API/XMLHttpRequest/timeout) on the Mozilla Developer Network.<br>Als de opgegeven time-out optreedt voordat de reactie wordt ontvangen, wordt standaardinhoud weergegeven en wordt de bezoeker mogelijk geteld als een deelnemer aan een activiteit omdat alle gegevensverzameling aan de [!DNL Target] rand plaatsvindt. Als de aanvraag de [!DNL Target] rand bereikt, wordt de bezoeker geteld.<br>Denk aan het volgende wanneer u de time-outinstelling configureert:<ul><li>Als de waarde te laag is, kunnen gebruikers de standaardinhoud het grootste deel van de tijd zien, hoewel de bezoeker als deelnemer aan de activiteit kon worden geteld.</li><li>Als de waarde te hoog is, kunnen bezoekers lege gebieden op uw webpagina of lege pagina&#39;s zien als u de hoofdtekst langere tijd verbergt.</li></ul>Om een beter inzicht in mbox reactietijden te krijgen, bekijk het lusje van het Netwerk in de Hulpmiddelen van de Ontwikkelaar van uw browser. U kunt ook controlehulpmiddelen voor webprestaties van derden gebruiken, zoals Catchpoint.<br>**Opmerking **: De instelling[bezoekerApiTimeout](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetgobalsettings.md)zorgt ervoor dat[!DNL Target]niet te lang op de reactie van de bezoeker-API wordt gewacht. Deze instelling en de instelling Time-out voor at.js die hier wordt beschreven, zijn niet van invloed op elkaar. |
| Ondersteuning voor oudere browsers | **Opmerking**: De optie Verouderde browserondersteuning is beschikbaar in versie 0.js 0.9.3 en eerder. Deze optie is verwijderd in versie 0.js 0.9.4. Zie [Ondersteunde browsers](/help/c-implementing-target/c-considerations-before-you-implement-target/supported-browsers.md)voor een lijst met browsers die worden ondersteund door at.js.<br>Verouderde browsers zijn oudere browsers die geen volledige ondersteuning bieden voor CORS (Cross Origin Resource Sharing). Deze browsers zijn: Browsers van Internet Explorer ouder dan versie 11 en Safari versies 6 en lager. Als ondersteuning voor verouderde browsers is uitgeschakeld, levert Target geen inhoud of telt Target geen bezoekers in rapporten over deze browsers. Als deze optie is ingeschakeld, is het raadzaam om in oudere browsers kwaliteitsborging toe te passen om een goede klantervaring te garanderen. |

## Codeinstellingen {#section_D41C905D0F8149949F525C85F2CCFF7F}

| Instelling | Beschrijving |
|--- |--- |
| Bibliotheekkoptekst | Voeg aangepaste JavaScript toe die u boven aan de bibliotheek wilt opnemen. |
| Bibliotheekvoettekst | Voeg aangepaste JavaScript toe die u onder aan de bibliotheek wilt opnemen. |

## Downloaden om.js {#concept_1E1F958F9CCC4E35AD97581EFAF659E2}

Instructies voor het downloaden van de bibliotheek met behulp van de doelinterface of de download-API.

<!-- 

ov2/c_target-configure-atjs.xml

 -->

>[!NOTE]
>
>[Adobe Launch](../../../c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/cmp-implementing-target-using-adobe-launch.md#topic_5234DDAEB0834333BD6BA1B05892FC25) is de voorkeursmethode voor de implementatie van Target en de bibliotheek at.js. De volgende informatie is niet van toepassing wanneer u Adobe Launch gebruikt om Target te implementeren.

>[!IMPORTANT]
>
>Het team van het Doel handhaaft slechts twee versies van [!DNL at.js]-de huidige versie en de tweede-recentste versie. Voer [!DNL at.js] indien nodig een upgrade uit om ervoor te zorgen dat u een ondersteunde versie gebruikt. Voor meer informatie over wat in elke versie is, zie [bij.js de Details](../../../c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md#reference_DBB5EDB79EC44E558F9E08D4774A0F7A)van de Versie.

## Download at.js gebruikend de interface van het Doel {#section_1F5EE401C2314338910FC57F9592894E}

Downloaden [!DNL at.js] vanaf de [!DNL Target] interface:

1. Klik op **[!UICONTROL Setup]** > **[!UICONTROL Implementation]**.
1. Selecteer **[!UICONTROL at.js]**.
1. Klik op **[!UICONTROL Download at.js]**.

## Download at.js met de API voor doeldownloaden {#section_C0D9D2A9068144708D08526BA5CA10D0}

Downloaden [!DNL at.js] met de API.

1. Haal uw clientcode op.

   De clientcode is beschikbaar boven aan de pagina **[!UICONTROL Setup]** > **[!UICONTROL Implementation]** > **[!UICONTROL Edit at.js Settings]** van de [!DNL Target] interface.

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
   https://admin<varname>admin number</varname>>.testandtarget.omniture.com/admin/rest/v1/libraries/atjs/download?client=<varname>client code </varname>version=<version number>
   ```

   * Vervangen `admin number` door uw beheerdersnummer.
   * Vervangen `client code` door de clientcode uit stap 1.
   * Vervangen `version number` door het gewenste at.js versienummer (bijvoorbeeld 2.2).
   >[!IMPORTANT]
   >
   >Het team van het Doel handhaaft slechts twee versies van [!DNL at.js]-de huidige versie en de tweede-recentste versie. Voer [!DNL at.js] indien nodig een upgrade uit om ervoor te zorgen dat u een ondersteunde versie gebruikt. Voor meer informatie over wat in elke versie is, zie [bij.js de Details](../../../c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md#reference_DBB5EDB79EC44E558F9E08D4774A0F7A)van de Versie.

   Wanneer u deze URL laadt, wordt het downloaden van uw aangepaste [!DNL at.js] bestand gestart.

## at.js-implementatie {#concept_03CFA86973A147839BEB48A06FEE5E5A}

at.js moet worden geïmplementeerd in het `<head>` element van elke pagina van uw website.

Een standaardimplementatie van Target die geen tagbeheer zoals [Adobe Launch](../../../c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/cmp-implementing-target-using-adobe-launch.md#topic_5234DDAEB0834333BD6BA1B05892FC25) of [Dynamic Tag Management](../../../c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/implementing-target-using-dynamic-tag-management.md#concept_3A40AF6FFC0E4FD2AA81B303A79D0B96) gebruikt, ziet er als volgt uit:

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
* De opties Preconnect en Prefetch zijn opties die u kunnen helpen uw webpagina&#39;s sneller te laden. Als u deze configuraties gebruikt, zorg ervoor dat u `<client code>` met uw eigen cliëntcode vervangt, die u van **[!UICONTROL Setup]** > **[!UICONTROL Implementation]** **[!UICONTROL Edit at.js Settings]** > pagina kunt verkrijgen.
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