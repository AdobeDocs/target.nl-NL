---
keywords: at.js faq;at.js veelgestelde vragen;faq;flicker;loader;page loader;cross domain;file size;x-domain;at.js en mbox.js;x alleen;cross domain;safari;single page app;missing selectors;single page application;tt.omtr dc.net;spa;Adobe Experience Manager;AEM;ip adres, alleen;HttpOnly;secure;ip;cookie domain
description: Reantwoorden lezen op veelgestelde vragen over de Adobe [!DNL Target] at.js JavaScript-bibliotheek.
title: Wat zijn algemene vragen en antwoorden over at.js?
feature: at.js
role: Developer
exl-id: 937f880a-1842-4655-be44-0a5614c2dbcc
source-git-commit: b1e8ea2370fc15f4bfcd960ab2960cafe2db92b8
workflow-type: tm+mt
source-wordcount: '2565'
ht-degree: 0%

---

# om.js Veelgestelde Vragen

Antwoorden op veelgestelde vragen over de [!DNL Adobe Target] at.js JavaScript-bibliotheek.

## Wat zijn de voordelen om at.js tegenover mbox.js te gebruiken? {#section_FE30D01A577C46ACB0F787B85F5E0F6B}

De [!DNL at.js] bibliotheek vervangt [!DNL mbox.js]. De [!DNL mbox.js] bibliotheek wordt niet meer ondersteund. Voor de meeste mensen echter [!DNL at.js] biedt voordelen boven [!DNL mbox.js].

Onder andere voordelen [!DNL at.js] Hiermee verbetert u de laadtijden voor webimplementaties, verbetert u de beveiliging en biedt u betere implementatieopties voor toepassingen van één pagina.

In het volgende diagram worden de prestaties bij het laden van een pagina geïllustreerd met mbox.js versus at.js.

![](assets/atjs_vesus_mboxjs.png)

Zoals hierboven is geïllustreerd, is met mbox.js de pagina-inhoud pas na de gebeurtenis [!DNL Target] de vraag is volledig. Wanneer u at.js gebruikt, wordt pagina-inhoud geladen wanneer de [!DNL Target] de vraag wordt in werking gesteld en wacht niet tot de vraag volledig is.

## Wat is het effect van at.js en mbox.js op pagina-ladingstijd? {#page-load}

Veel klanten en consultants willen weten wat de gevolgen zijn van [!DNL at.js] en [!DNL mbox.js] op pagina-laadtijd, vooral in de context van nieuwe of terugkerende gebruikers. Helaas is het moeilijk om concrete getallen te meten en te geven over hoe [!DNL at.js] of [!DNL mbox.js] beïnvloedt de pagina-lading tijd toe te schrijven aan de implementatie van elke klant.

Als de API voor bezoekers echter aanwezig is op de pagina, [!DNL Target] kan beter begrijpen hoe [!DNL at.js] en [!DNL mbox.js] invloed op de laadtijd van de pagina.

>[!NOTE]
>
>De Bezoeker-API en [!DNL at.js] of [!DNL mbox.js] hebben alleen invloed op de laadtijd van de pagina wanneer u de globale box gebruikt (vanwege de techniek voor het verbergen van het lichaam). De regionale mboxes worden niet beïnvloed door de integratie van de Bezoeker API.

De volgende secties beschrijven de opeenvolging van acties voor nieuwe en terugkerende bezoekers:

### Nieuwe bezoekers

1. De bezoeker-API wordt geladen, geparseerd en uitgevoerd.
1. at.js / mbox.js wordt geladen, geparseerd en uitgevoerd.
1. Als Automatisch maken van globale box is ingeschakeld, wordt de JavaScript-doelbibliotheek gebruikt:

   * Instantieert het object Visitor.
   * De [!DNL Target] bibliotheek probeert op te halen [!DNL Experience Cloud Visitor ID] gegevens.
   * Omdat deze bezoeker een nieuwe bezoeker is, leidt de bezoeker-API een aanvraag voor een ander domein in naar demdex.net.
   * Na [!DNL Experience Cloud Visitor ID] gegevens worden opgehaald, een verzoek aan [!DNL Target] wordt afgegaan.

### Bezoekers terugsturen

1. De bezoeker-API wordt geladen, geparseerd en uitgevoerd.
1. at.js / mbox.js wordt geladen, geparseerd en uitgevoerd.
1. Als de optie voor automatisch maken van globale mbox is ingeschakeld, wordt de [!DNL Target] JavaScript-bibliotheek:

   * Instantieert het object Visitor.
   * De [!DNL Target] bibliotheek probeert op te halen [!DNL Experience Cloud Visitor ID] gegevens.
   * De bezoeker-API haalt gegevens op uit cookies.
   * Na [!DNL Experience Cloud Visitor ID] gegevens worden opgehaald, een verzoek aan [!DNL Target] wordt afgegaan.

>[!NOTE]
>
>Voor nieuwe bezoekers, wanneer de API voor bezoekers aanwezig is, [!DNL Target] moet over de draad veelvoudige tijden gaan om ervoor te zorgen dat [!DNL Target] verzoeken bevatten [!DNL Experience Cloud Visitor ID] gegevens. Voor terugkerende bezoekers [!DNL Target] gaat over de draad slechts aan [!DNL Target] om de gepersonaliseerde inhoud op te halen.

## Waarom lijkt het alsof ik langzamere reactietijden na bevordering van een vorige versie van at.js aan versie 1.0.0 zie? {#section_DFBA5854FFD142B49AD87BFAA09896B0}

[!DNL at.js] in versie 1.0.0 en hoger worden alle aanvragen parallel afgehandeld . Eerdere versies voeren de aanvragen opeenvolgend uit, wat betekent dat de aanvragen in een wachtrij worden geplaatst en [!DNL Target] wacht op eerste verzoek om te voltooien alvorens op het volgende verzoek over te gaan.

De manier waarop vorige versies van [!DNL at.js] uitvoerverzoeken zijn vatbaar voor de zogenaamde &quot;hoofd van lijnblokkering.&quot; In [!DNL at.js] 1.0.0 en hoger, [!DNL Target] geschakeld naar parallelle uitvoering van aanvragen.

Als u de waterval van het netwerklusje controleert voor [!DNL at.js] 0.9.1, bijvoorbeeld, zult u dat volgende zien [!DNL Target] De aanvraag start pas nadat de vorige is voltooid. Deze volgorde is niet van toepassing op [!DNL at.js] 1.0.0 en later, waar alle aanvragen in feite tegelijkertijd beginnen.

Vanuit het perspectief van de reactietijd, wiskundig, kan deze opeenvolging als dit worden samengevoegd

<ul class="simplelist"> 
 <li> om.js 0.9.1: Responstijd van alle [!DNL Target] verzoeken = som van verzoeken, reactietijd </li> 
 <li> in.js 1.0.0 en hoger: Responstijd van alle [!DNL Target] verzoeken = maximum van verzoeken reactietijd </li> 
</ul>

De [!DNL at.js] met versie 1.0.0 van de bibliotheek worden de aanvragen sneller voltooid. Daarnaast [!DNL at.js] aanvragen zijn asynchroon, dus [!DNL Target] blokkeert geen paginerendering. Zelfs als verzoeken seconden duren, wordt de weergegeven pagina nog steeds weergegeven. Alleen bepaalde delen van de pagina worden gewist tot [!DNL Target] krijgt een antwoord van [!DNL Target] rand.

## Kan ik de [!DNL Target] asynchroon bibliotheek? {#section_AB9A0CA30C5440C693413F1455841470}

Met de release van at.js 1.0.0 kunt u de [!DNL Target] bibliotheek asynchroon.

Zo laadt u at.js asynchroon:

* De aanbevolen aanpak is via tags in [!DNL Adobe Experience Platform].
* U kunt ook asynchroon laden bij .js door het asynchrone attribuut aan de manuscriptmarkering toe te voegen die at.js laadt. Gebruik iets als dit:

   ```
   <script src="<URL to at.js>" async></script>
   ```

* U kunt ook asynchroon laden bij .js met deze code:

   ```
   var script = document.createElement('script'); 
   script.async = true; 
   script.src = "<URL to at.js>"; 
   document.head.appendChild(script);
   ```

Het asynchroon laden van at.js is een goede manier om te voorkomen dat de browser de rendering blokkeert. deze techniek kan echter tot flikkering op de webpagina leiden .

U kunt flikkering vermijden door een vooraf verborgen fragment te gebruiken dat de pagina (of gespecificeerde gedeelten) verbergt en het dan onthult nadat om.js en het globale verzoek hebben geladen. Het fragment moet worden toegevoegd voordat u het bestand at.js laadt.

Als u at.js door asynchroon opstelt [!DNL Adobe Experience Platform] implementatie, zorg ervoor dat u het vooraf verborgen fragment direct op uw pagina&#39;s opneemt, voordat u het implementeert [!DNL Target] gebruiken [!DNL Adobe Experience Platform] Code insluiten.

Als u at.js door een synchrone implementatie DTM opstelt, kan het pre-verbergende fragment worden toegevoegd door een lijn van de Lading van de Pagina die bij de bovenkant van de pagina wordt teweeggebracht.

Zie voor meer informatie [Hoe at.js flikkering beheert](https://developer.adobe.com/target/implement/client-side/atjs/how-atjs-works/manage-flicker-with-atjs/).

## Is at.js compatibel met [!DNL Adobe Experience Manager] integratie (Experience Manager)? {#section_6177AE10542344239753764C6165FDDC}

[!DNL Adobe Experience Manager] 6.2 met FP-11577 (of later) steunt nu [!DNL at.js] uitvoering met het [!UICONTROL Adobe Target Cloud Services] integratie.

## Hoe kan ik flikkering tijdens het laden van pagina&#39;s voorkomen met at.js? {#section_4D78AAAE73C24E578C974743A3C65919}

Doel biedt verschillende manieren om flikkering bij het laden van pagina&#39;s te voorkomen. Zie voor meer informatie [Flikkering voorkomen met at.js](https://developer.adobe.com/target/implement/client-side/atjs/how-atjs-works/manage-flicker-with-atjs/).

## Wat is de bestandsgrootte van at.js? {#section_6A25C9A14C66441785A7635FEF5C4475}

Het bestand at.js is ongeveer 109 kB wanneer het wordt gedownload. Omdat de meeste servers bestanden echter automatisch comprimeren om de bestandsgrootte te verkleinen, is at.js ongeveer 34 kB bij het comprimeren (met GZIP of een andere methode) op uw server en het laden als gebruikers uw website bezoeken. De compressie-instellingen op de server waarop u .js hebt geïnstalleerd, bepalen de werkelijke gecomprimeerde grootte.

## Waarom is at.js groter dan mbox.js? {#section_AA1C43897E46448FA3E26EEC10ED7E51}

at.js-implementaties gebruiken één bibliotheek ( [!DNL at.js]), terwijl mbox.js-implementaties eigenlijk twee bibliotheken gebruiken ( [!DNL mbox.js] en [!DNL target.js]). Een eerlijkere vergelijking is dus at.js versus mbox.js *en* `target.js`. Wanneer de gezipte grootten van de twee versies worden vergeleken, is versie 1.js 1.2 34 kB en versie 63 mbox.js 26,2 kB. &quot;

at.js is groter omdat het veel meer DOM ontleedt in vergelijking met mbox.js. Dit is vereist omdat at.js &quot;onbewerkte&quot;gegevens in de reactie JSON krijgt en het moet zinvol maken. mbox.js gebruikt `document.write()` en al het parseren werd gedaan door browser.

Ondanks de grotere bestandsgrootte geven onze tests aan dat pagina&#39;s sneller worden geladen met at.js versus mbox.js. Ook, is at.js superieur vanuit veiligheidsperspectief omdat het geen extra dossiers dynamisch laadt of gebruikt `document.write`.

## Heeft at.js er jQuery in? Kan ik dit deel van at.js verwijderen omdat ik al jQuery op mijn website heb? {#section_E4604E46E7B34460B8DD6A78D9B476F9}

at.js gebruikt momenteel delen van jQuery en dus ziet u de MIT-licentiemelding boven aan at.js. jQuery wordt niet weergegeven en heeft geen invloed op de jQuery-bibliotheek die u al op de pagina hebt, wat een andere versie kan zijn. Het verwijderen van de jQuery-code in at.js wordt niet ondersteund.

## Biedt at.js ondersteuning voor Safari en cross domain ingesteld op x-only? {#section_114EC271A6E045E1B2183B66F1B71285}

Nee, als cross-domain is ingesteld op x-only en Safari cookies van derden heeft uitgeschakeld, dan zijn beide [!DNL mbox.js] en at.js plaatst een gehandicapte koekje en geen mbox verzoeken worden uitgevoerd voor het domein van die bepaalde cliënt.

Om Safari bezoekers te ondersteunen, zou een beter X-Domein &quot;gehandicapt&quot;zijn (plaatst slechts een eerste-partijkoekje) of &quot;toegelaten&quot;(plaatst slechts een eerste-partijkoekje op Safari, terwijl het plaatsen van eerste en derdekoekjes op andere browsers).

## Kan ik de [!DNL Target] Visual Experience Composer (VEC) in mijn single-page toepassingen? {#section_459C1BEABD4B4A1AADA6CF4EC7A70DFB}

Ja, u kunt VEC voor uw SPA gebruiken als u at.js 2.x gebruikt. Zie voor meer informatie [Single Page (SPA) Visual Experience Composer](/help/main/c-experiences/spa-visual-experience-composer.md).

## Kan ik de [!DNL Adobe Experience Cloud] Foutopsporing met implementaties van at.js? {#section_FF3CF4C5FD2F4DB1BF1A6B39DA161637}

Ja. U kunt mboxTrace voor het zuiveren doeleinden of de Hulpmiddelen van de Ontwikkelaar van uw browser ook gebruiken om de verzoeken van het Netwerk te inspecteren, filtrerend aan &quot;mbox&quot;om mbox vraag te isoleren.

## Kan ik speciale karakters in mbox namen met at.js gebruiken? {#section_8E31D2E8A27642098934D7DACFB2A600}

Ja, hetzelfde als met mbox.js.

## Waarom worden mijn dozen niet op mijn webpagina&#39;s geactiveerd? {#section_4BA5DA424B734324AAB51E4588FA50F5}

[!DNL Target] klanten gebruiken soms cloudgebaseerde instanties met [!DNL Target] voor tests of eenvoudige concepttest. Deze en vele andere domeinen maken deel uit van de [Lijst met openbare achtervoegsels](https://publicsuffix.org/list/public_suffix_list.dat).

Moderne browsers slaan cookies niet op als u deze domeinen gebruikt, tenzij u de opties `cookieDomain` instellen met targetGlobalSettings(). Zie voor meer informatie [Op cloud gebaseerde instanties gebruiken met het doel](https://developer.adobe.com/target/implement/client-side/target-debugging-atjs/targeting-using-cloud-based-instances/).

## Kunnen IP adressen als koekjesdomein worden gebruikt wanneer het gebruiken van at.js? {#section_8BEEC91A3410459D9E442840A3C88AF7}

Ja, als u [at.js versie 1.2 of hoger](https://developer.adobe.com/target/implement/client-side/atjs/target-atjs-versions/). [!DNL Adobe] Het is echter van belang dat u de nieuwste versie blijft gebruiken.

>[!NOTE]
>
>De volgende voorbeelden zijn niet nodig als u at.js versie 1.2 of later gebruikt.

Afhankelijk van hoe u [targetGlobalSettings](https://developer.adobe.com/target/implement/client-side/atjs/atjs-functions/targetglobalsettings/), moet u mogelijk aanvullende wijzigingen in de code aanbrengen nadat u het bestand at.js hebt gedownload. Als u bijvoorbeeld iets andere instellingen voor uw [!DNL Target] implementaties op verschillende websites die deze instellingen niet dynamisch kunnen definiëren met behulp van aangepaste JavaScript, deze aanpassingen handmatig uitvoeren nadat het bestand is gedownload en voordat het bestand naar de desbetreffende website wordt geüpload.

In de volgende voorbeelden kunt u de `targetGlobalSettings()` de functie at.js om een codefragment op te nemen om IP adressen te steunen:

Dit voorbeeld is voor één enkel IP adres:

```
if (window.location.hostname === '123.456.78.9') { 
    window.targetGlobalSettings = window.targetGlobalSettings || {}; 
    window.targetGlobalSettings.cookieDomain = window.location.hostname; 
}
```

Dit voorbeeld is voor een waaier van IP adressen:

```
if (/^123\.456\.78\..*/g.test(window.location.hostname)) { 
    window.targetGlobalSettings = window.targetGlobalSettings || {}; 
    window.targetGlobalSettings.cookieDomain = window.location.hostname; 
}
```

## Waarom zie ik waarschuwingsberichten, zoals &quot;acties met ontbrekende kiezers&quot;? {#section_C36BED5B16634361A1BA46FCB731489D}

Deze berichten hebben geen betrekking op [!DNL at.js] functionaliteit. De [!DNL at.js] De bibliotheek probeert om het even wat te melden die niet in DOM kan worden gevonden.

Als dit waarschuwingsbericht wordt weergegeven, zijn de volgende mogelijke hoofdoorzaken:

* De pagina wordt dynamisch samengesteld en at.js kan het element niet vinden.
* De pagina wordt langzaam samengesteld (vanwege een traag netwerk) en at.js kan de kiezer niet vinden in de DOM.
* De paginastructuur die actief is[!UICONTROL y is running on has been changed. If you reopen the activity in the ]Visual Experience Composer (VEC), zou u een waarschuwingsbericht moeten krijgen. Werk de activiteit bij zodat alle noodzakelijke elementen kunnen worden gevonden.
* De onderliggende pagina is onderdeel van een [!UICONTROL Single Page Application] (SPA) of de pagina bevat elementen die verderop op op de pagina en de [!DNL at.js] Deze elementen kunnen niet worden gevonden door middel van een &#39;kiezeropiniepeilingsmechanisme&#39;. De `selectorsPollingTimeout` zou kunnen helpen. Zie voor meer informatie [targetGlobalSettings()](https://developer.adobe.com/target/implement/client-side/atjs/atjs-functions/targetglobalsettings/).
* Om het even welke klik-volgende metrisch probeert om aan elke pagina toe te voegen, ongeacht URL waarop metrisch opstelling was. Hoewel onschuldig, maakt deze situatie veel van deze berichten tonen.

   Download en gebruik de nieuwste versie van [!DNL at.js]. Zie voor meer informatie [at.js - Versiedetails](https://developer.adobe.com/target/implement/client-side/atjs/target-atjs-versions/) en [Downloaden om.js](https://developer.adobe.com/target/implement/client-side/atjs/how-to-deployatjs/implement-target-without-a-tag-manager/).

## Wat is het domein tt.omtr dc.net dat [!DNL Target] serveraanroepen gaan naar? {#section_999C29940E8B4CAD8A957A6B1D440317}

[!DNL tt.omtrdc.net] is de domeinnaam voor Adobe EDGE netwerk, dat wordt gebruikt om alle vraag naar Doel te ontvangen.

## Waarom gebruikt at.js altijd vlaggen van het Toegangske- en Veilige koekje HttpOnly? {#section_74527E3B41B54B0A83F217C3E664ED1F}

HttpOnly kan alleen worden ingesteld via code op de server. [!DNL Target] cookies, zoals mbox, worden gemaakt en opgeslagen via JavaScript-code, zodat [!DNL Target] Kan de koekjesvlag niet gebruiken HttpOnly. [!DNL Target] Hierbij wordt HttpOnly ingesteld voor cookies van derden die vanaf de server worden ingesteld wanneer cross-domain is ingeschakeld.

Beveiliging kan alleen via JavaScript worden ingesteld wanneer de pagina via HTTPS is geladen. Als de pagina voor het eerst wordt geladen via HTTP, kan JavaScript deze markering niet instellen. Als de markering Beveiligen wordt gebruikt, is de cookie bovendien alleen beschikbaar op HTTPS-pagina&#39;s. Voor pagina&#39;s die via HTTPS worden geladen, [!DNL Target] Hiermee worden de kenmerken Secure en SameSite=None ingesteld.

Om ervoor te zorgen dat [!DNL Target] gebruikers goed kunnen volgen en omdat de cookies op de client worden gegenereerd, [!DNL Target] gebruikt geen van beide vlaggen behalve in de hierboven vermelde situaties.

## Hoe vaak brand at.js een netwerkverzoek? {#section_57C5235DF7694AF093A845D73EABADFD}

[!DNL Target] voert al zijn besluit op de server uit. Dit betekent dat at.js elke keer dat de pagina opnieuw wordt geladen of een openbare API van at.js wordt aangeroepen, een netwerkverzoek in werking stelt.

## In het beste geval, kunnen wij verwachten dat de gebruiker geen zichtbare gevolgen op paginading met betrekking tot het verbergen van, het vervangen van, en het tonen van inhoud ervaart? {#section_CB3C566AD61F417FAC0EC5AC706723EB}

at.js probeert pre-verbergen HTML BODY of andere DOM elementen voor een langere periode te vermijden, maar dit hangt van netwerkvoorwaarden en activiteitenopstelling af. at.js biedt [instellingen](https://developer.adobe.com/target/implement/client-side/atjs/atjs-functions/targetglobalsettings/) U kunt de LICHAAM die CSS-stijl verbergt, aanpassen, zodat u in plaats van de hele HTML BODY te lekken, slechts enkele delen van de pagina kunt voorverbergen. De verwachting is dat die onderdelen DOM-elementen bevatten die &quot;gepersonaliseerd&quot; moeten worden.

## Wat is de opeenvolging van gebeurtenissen in een gemiddeld scenario waar een gebruiker voor een activiteit kwalificeert? {#section_56E6F448E901403FB77DF02F44C44452}

Het verzoek at.js is een asynchroon `XMLHttpRequest`, dus voeren we de volgende stappen uit:

1. De pagina wordt geladen.
1. at.js prehides the HTML BODY. Er is een instelling voor het vooraf verbergen van een bepaalde container in plaats van de HTML BODY.
1. De aanvraag at.js wordt geactiveerd.
1. Na de [!DNL Target] antwoord ontvangen; [!DNL Target] Hiermee worden de CSS-kiezers geëxtraheerd.
1. CSS-kiezers gebruiken [!DNL Target] maakt STIJL-tags om de DOM-elementen die worden aangepast, vooraf te verbergen.
1. De vooraf verborgen STIJL voor het HTML-LICHAAM wordt verwijderd.
1. [!DNL Target] start opiniepeiling voor DOM-elementen.
1. Als een DOM-element wordt gevonden, [!DNL Target] past DOM-wijzigingen toe en de vooraf verborgen STIJL van het element wordt verwijderd.
1. Als DOM-elementen niet worden gevonden, verbergt een algemene time-out de elementen om te voorkomen dat een pagina wordt verbroken.

## Hoe vaak wordt de inhoud van de pagina volledig geladen en zichtbaar wanneer at.js definitief het element ontverbergt de activiteit verandert? {#section_01AFF476EFD046298A2E17FE3ED85075}

Gezien het bovenstaande scenario, hoe vaak wordt de inhoud van de pagina volledig geladen en zichtbaar wanneer at.js definitief het element ontverbergt de activiteit verandert? Met andere woorden, de pagina is volledig zichtbaar behalve de inhoud van de activiteit, die dan lichtjes na de rest van de inhoud wordt onthuld.

at.js blokkeert niet dat de pagina wordt weergegeven. Een gebruiker kan enkele lege gebieden op de pagina opmerken die elementen vertegenwoordigen die zijn aangepast door [!DNL Target]. Als de toe te passen inhoud niet vele verre activa, zoals SCRIPTs of IMGs bevat, zou alles snel moeten teruggeven.

## Hoe zou een volledig caching pagina het bovengenoemde scenario beïnvloeden? Zou het waarschijnlijker zijn dat de inhoud van de activiteit merkbaar zichtbaar wordt nadat de rest inhoud van de pagina laadt? {#section_CE76335A3E0B41CB8253DEE5E060FCDA}

Als een pagina in de cache wordt geplaatst op een CDN die dicht bij de locatie van de gebruiker staat, maar niet bij de locatie [!DNL Target] Edge, kan de gebruiker enige vertragingen zien. [!DNL Target] de randen zijn over de hele wereld goed verdeeld , dus dit is niet de meeste tijd een probleem .

## Is het mogelijk dat een hoofdafbeelding na een korte vertraging wordt weergegeven en vervolgens wordt omgewisseld? {#section_C25B07B25B854AAE8DEE1623D0FA62A3}

Met het volgende scenario:

De [!DNL Target] time-out is vijf seconden. Een gebruiker laadt een pagina die een activiteit heeft om een hoofdafbeelding aan te passen. at.js verzendt het verzoek om te bepalen als er een activiteit is om toe te passen, maar er is geen aanvankelijke reactie. Stel dat de gebruiker de reguliere inhoud van de hoofdafbeelding ziet, omdat er geen reactie is ontvangen van [!DNL Target] met betrekking tot de vraag of er een verwante activiteit is. Na vier seconden [!DNL Target] retourneert een reactie met de inhoud van de activiteit.

Zou het in dit stadium mogelijk zijn de alternatieve versie te tonen? Na vier seconden kon de hoofdafbeelding worden omgewisseld en kon de gebruiker deze afbeeldingswisseling zien?

In eerste instantie is het DOM-element voor de held van de afbeelding verborgen. Na een reactie van [!DNL Target] ontvangen, past at.js de DOM-wijzigingen toe, zoals het vervangen van de IMG en het weergeven van de aangepaste hoofdafbeelding.

## Welk HTML doctype vereist at.js?

at.js vereist HTML 5 doctype.

Deze syntaxis is:

`<!DOCTYPE html>`

Het documenttype HTML 5 zorgt ervoor dat de pagina in de standaardmodus wordt geladen. Bij het laden in de modus Kirken zijn sommige JS API&#39;s waarvan at.js afhankelijk is, uitgeschakeld. [!DNL Target] Schakelt in de modus kirken de modus at.js uit.