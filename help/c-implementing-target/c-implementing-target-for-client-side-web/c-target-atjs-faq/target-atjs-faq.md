---
keywords: at.js faq;at.js frequently asked questions;faq;flicker;loader;page loader;cross domain;file size;filesize;x-domain;at.js and mbox.js;x only;cross domain;safari;single page app;missing selectors;selectors;single page application;tt.omtrdc.net;spa;Adobe Experience Manager;AEM;ip address;httponly;HttpOnly;secure;ip;cookie domain
description: Antwoorden op veelgestelde vragen over de JavaScript-bibliotheek van Adobe Target at.js.
title: Adobe Target om.js Veelgestelde vragen
feature: client-side
subtopic: Getting Started
uuid: 1fcd3984-7c6d-4619-953e-3e28eb0d015a
translation-type: tm+mt
source-git-commit: 95450abc32be19d04b791af3c62673e9411ab53c
workflow-type: tm+mt
source-wordcount: '2656'
ht-degree: 0%

---


# om.js Veelgestelde Vragen{#at-js-frequently-asked-questions}

Antwoorden op veelgestelde vragen over at.js.

## Wat zijn de voordelen om at.js tegenover mbox.js te gebruiken? {#section_FE30D01A577C46ACB0F787B85F5E0F6B}

Hoewel [!DNL at.js] deze optie wordt vervangen [!DNL mbox.js], [!DNL mbox.js] blijft deze worden ondersteund. Voor de meeste mensen [!DNL at.js] biedt dit echter meer voordelen dan [!DNL mbox.js].

Verbeter onder andere de laadtijden voor webimplementaties, verbeter de beveiliging en biedt betere implementatieopties voor toepassingen van één pagina. [!DNL at.js]

In het volgende diagram worden de prestaties bij het laden van een pagina geïllustreerd met mbox.js versus at.js.

![](assets/atjs_vesus_mboxjs.png)

Zoals hierboven geïllustreerd, gebruikend mbox.js, begint de pagina inhoud niet te laden tot nadat de [!DNL Target] vraag volledig is. Gebruikend at.js, begint de pagina inhoud ladend wanneer de [!DNL Target] vraag in werking wordt gesteld en wacht niet tot de vraag volledig is.

## Wat is het effect van at.js en mbox.js op pagina-ladingstijd? {#page-load}

Veel klanten en consultants willen weten wat de impact is van [!DNL at.js] en [!DNL mbox.js] op de laadtijd van pagina&#39;s, met name in de context van nieuwe gebruikers of gebruikers die terugkeren. Jammer genoeg, is het moeilijk om concrete aantallen betreffende te meten en te geven hoe [!DNL at.js] of [!DNL mbox.js] beïnvloedt pagina-lading tijd toe te schrijven aan de implementatie van elke klant.

Als de API voor bezoekers echter aanwezig is op de pagina, kunnen we beter begrijpen hoe [!DNL at.js] en [!DNL mbox.js] invloed deze tijd heeft.

>[!NOTE]
>
>De API voor bezoekers en [!DNL at.js] of [!DNL mbox.js] hebben alleen invloed op de laadtijd van de pagina wanneer u de globale box gebruikt (vanwege de techniek voor het verbergen van de hoofdtekst). De regionale mboxes worden niet beïnvloed door de integratie van de Bezoeker API.

De volgende secties beschrijven de opeenvolging van acties voor nieuwe en terugkerende bezoekers:

### Nieuwe bezoekers

1. De bezoeker-API wordt geladen, geparseerd en uitgevoerd.
1. at.js / mbox.js wordt geladen, geparseerd en uitgevoerd.
1. Als Automatisch maken van globale box is ingeschakeld, wordt de JavaScript-doelbibliotheek gebruikt:

   * Instantieert het object Visitor.
   * De doelbibliotheek probeert de gegevens van de Experience Cloud Visitor-id op te halen.
   * Omdat dit een nieuwe bezoeker is, leidt de bezoeker-API een aanvraag voor een ander domein in naar demdex.net.
   * Nadat de gegevens van de identiteitskaart van de Bezoeker van Experience Cloud worden teruggewonnen, wordt een verzoek aan Doel in brand gestoken.

### Bezoekers terugsturen

1. De bezoeker-API wordt geladen, geparseerd en uitgevoerd.
1. at.js / mbox.js wordt geladen, geparseerd en uitgevoerd.
1. Als Automatisch maken van globale box is ingeschakeld, wordt de JavaScript-doelbibliotheek gebruikt:

   * Instantieert het object Visitor.
   * De doelbibliotheek probeert de gegevens van de Experience Cloud Visitor-id op te halen.
   * De bezoeker-API haalt gegevens op uit cookies.
   * Nadat de gegevens van de identiteitskaart van de Bezoeker van Experience Cloud worden teruggewonnen, wordt een verzoek aan Doel in brand gestoken.

>[!NOTE]
>
>Voor nieuwe bezoekers, wanneer de Bezoeker-API aanwezig is, moet Target meerdere keren over de kabel gaan om ervoor te zorgen dat de doelaanvragen gegevens van de Experience Cloud Bezoeker-id bevatten. Voor terugkerende bezoekers, gaat het Doel over de draad slechts aan Doel om de gepersonaliseerde inhoud terug te winnen.

## Waarom lijkt het alsof ik langzamere reactietijden na bevordering van een vorige versie van at.js aan versie 1.0.0 zie? {#section_DFBA5854FFD142B49AD87BFAA09896B0}

[!DNL at.js] in versie 1.0.0 en hoger worden alle aanvragen parallel afgehandeld . Eerdere versies voeren de verzoeken opeenvolgend uit, wat betekent dat de verzoeken in een rij worden gezet en het Doel wacht op eerste verzoek om te voltooien alvorens op het volgende verzoek over te gaan.

De manier vorige versies van verzoeken [!DNL at.js] uitvoeren is vatbaar voor de zogenaamde &quot;hoofd van lijn het blokkeren.&quot; In [!DNL at.js] 1.0.0 en later schakelde Target over naar de uitvoering van parallelle verzoeken.

Als u de waterval van het netwerklusje voor [!DNL at.js] 0.9.1 controleert, bijvoorbeeld, zult u zien dat het volgende verzoek van het Doel niet begint tot vorige is gebeëindigd. Dit is niet het geval met [!DNL at.js] 1.0.0 en later, waar alle verzoeken in wezen tegelijkertijd beginnen.

Vanuit het perspectief van de reactietijd, wiskundig, kan dit als dit worden samengevat

<ul class="simplelist"> 
 <li> om.js 0.9.1: De tijd van de reactie van alle verzoeken van het Doel = som van de tijd van de verzoekreactie </li> 
 <li> in.js 1.0.0 en hoger: De tijd van de reactie van alle verzoeken van het Doel = maximum van de tijd van de verzoekreactie </li> 
</ul>

Zoals u kunt zien, zal [!DNL at.js] 1.0.0 de verzoeken sneller voltooien. Bovendien zijn [!DNL at.js] verzoeken asynchroon, zodat blokkeert Doel paginerendering niet. Zelfs als verzoeken seconden duren om te voltooien, ziet u nog steeds de gerenderde pagina, worden slechts enkele delen van de pagina gewist totdat Doel een reactie krijgt van de rand van het Doel.

## Kan ik de doelbibliotheek asynchroon laden? {#section_AB9A0CA30C5440C693413F1455841470}

Met de release at.js 1.0.0 kunt u de doelbibliotheek asynchroon laden.

Zo laadt u at.js asynchroon:

* De aanbevolen aanpak vindt u via een tagbeheer, zoals Adobe Launch of Adobe Dynamic Tag Manager (DTM). Zie de [Add Adobe Target](https://docs.adobe.com/content/help/en/experience-cloud/implementing-in-websites-with-launch/implement-solutions/target.html) les van het [Uitvoeren van de Experience Cloud in Websites met de zelfstudie van de Lancering](https://docs.adobe.com/content/help/en/experience-cloud/implementing-in-websites-with-launch/index.html) voor meer informatie.
* U kunt ook asynchroon laden bij .js door het asynchrone attribuut aan de manuscriptmarkering toe te voegen die at.js laadt. Je moet iets als dit gebruiken:

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

U kunt flikkering vermijden door een vooraf verborgen fragment te gebruiken dat de pagina (of gespecificeerde gedeelten) verbergt en het dan onthult nadat om.js en het globale verzoek volledig geladen hebben. Het fragment moet worden toegevoegd voordat u het bestand at.js laadt.

Als u at.js door een asynchrone implementatie van de Lancering opstelt, ben zeker om het pre-verbergen fragment op uw pagina&#39;s direct te omvatten, vóór de Lanceer bed code, zoals die in de [Add wordt beschreven het Doel pre-Hiding sectie van het Fragment](https://docs.adobe.com/content/help/en/experience-cloud/implementing-in-websites-with-launch/implement-solutions/target.html#add-the-target-pre-hiding-snippet) van het [Uitvoeren van de Experience Cloud in Websites met het Lanceerprogramma](https://docs.adobe.com/content/help/en/experience-cloud/implementing-in-websites-with-launch/index.html)wordt beschreven.

Als u at.js door een synchrone implementatie DTM opstelt, kan het pre-verbergende fragment worden toegevoegd door een lijn van de Lading van de Pagina die bij de bovenkant van de pagina wordt teweeggebracht.

Zie [Hoe at.js flikkering](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/manage-flicker-with-atjs.md)beheert voor meer informatie.

## Is at.js verenigbaar met de integratie van Adobe Experience Manager (AEM)? {#section_6177AE10542344239753764C6165FDDC}

[!DNL Adobe Experience Manager] 6.2 met FP-11577 (of later) steunt nu [!DNL at.js] implementaties met zijn [!UICONTROL Adobe Target Cloud Services] integratie. Zie [Feature Packs](https://docs.adobe.com/docs/en/aem/6-2/release-notes/feature-packs.html) en [Integrating with Adobe Target](https://docs.adobe.com/docs/en/aem/6-2/administer/integration/marketing-cloud/target.html) in de documentatie van *Adobe Experience Manager 6.2* voor meer informatie.

## Hoe kan ik flikkering tijdens het laden van pagina&#39;s voorkomen met at.js? {#section_4D78AAAE73C24E578C974743A3C65919}

Doel biedt verschillende manieren om flikkering bij het laden van pagina&#39;s te voorkomen. Zie [Flikkering met at.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/manage-flicker-with-atjs.md#concept_AA168574397D4474B993EEAB90865EBA)voorkomen voor meer informatie.

## Wat is de bestandsgrootte van at.js? {#section_6A25C9A14C66441785A7635FEF5C4475}

Het bestand at.js is ongeveer 109 kB wanneer het wordt gedownload. Omdat de meeste servers bestanden echter automatisch comprimeren om de bestandsgrootte te verkleinen, is at.js ongeveer 34 kB bij het comprimeren (met GZIP of een andere methode) op uw server en het laden als gebruikers uw website bezoeken. De compressie-instellingen op de server waarop u .js hebt geïnstalleerd, bepalen de werkelijke gecomprimeerde grootte.

## Waarom is at.js groter dan mbox.js? {#section_AA1C43897E46448FA3E26EEC10ED7E51}

bij.js de implementaties gebruiken één enkele bibliotheek ( [!DNL at.js]), terwijl mbox.js de implementaties eigenlijk twee bibliotheken ( [!DNL mbox.js] en [!DNL target.js]) gebruiken. Een eerlijkere vergelijking is at.js versus mbox.js *en* `target.js`. Wanneer de gezipte grootten van de twee versies worden vergeleken, is versie 1.js 1.2 34 kB en versie 63 mbox.js 26,2 kB. &quot;

at.js is groter omdat het veel meer DOM ontleedt in vergelijking met mbox.js. Dit is vereist omdat at.js &quot;onbewerkte&quot;gegevens in de reactie JSON krijgt en het moet zinvol maken. mbox.js gebruikt `document.write()` en al het ontleden wordt gedaan door browser.

Ondanks de grotere bestandsgrootte geven onze tests aan dat pagina&#39;s sneller worden geladen met at.js versus mbox.js. Daarnaast is at.js vanuit het oogpunt van beveiliging superieur omdat het geen extra bestanden dynamisch laadt of gebruikt `document.write`.

## Heeft at.js er jQuery in? Kan ik dit deel van at.js verwijderen omdat ik al jQuery op mijn website heb? {#section_E4604E46E7B34460B8DD6A78D9B476F9}

at.js gebruikt momenteel delen van jQuery en zo ziet u de MIT-licentiemelding boven aan at.js. jQuery wordt niet weergegeven en heeft geen invloed op de jQuery-bibliotheek die u al op de pagina hebt, wat een andere versie kan zijn. Het verwijderen van de jQuery-code in at.js wordt niet ondersteund.

## Biedt at.js ondersteuning voor Safari en cross domain ingesteld op x-only? {#section_114EC271A6E045E1B2183B66F1B71285}

Nee, als cross-domain is ingesteld op x-only en Safari cookies van andere leveranciers heeft uitgeschakeld, wordt zowel [!DNL mbox.js] als at.js een uitgeschakelde cookie ingesteld en worden geen box-aanvragen uitgevoerd voor het domein van die client.

Om Safari bezoekers te ondersteunen, zou een beter X-Domein &quot;gehandicapt&quot;zijn (plaatst slechts een eerste-partijkoekje) of &quot;toegelaten&quot;(plaatst slechts een eerste-partijkoekje op Safari, terwijl het plaatsen van eerste en derdekoekjes op andere browsers).

## Kan ik bij.js en mbox.js naast elkaar lopen? {#section_4DCAF38DBAEB430CA486FAEFAE0E0A29}

Niet op dezelfde pagina. Nochtans, terwijl het uitvoeren en het testen [!DNL at.js], kunt u [!DNL at.js] op sommige pagina&#39;s en [!DNL mbox.js] op andere pagina&#39;s lopen tot u volledig bevestigd hebt [!DNL at.js].

## Kan ik de Composer van de Ervaring van het Doel Visuele in mijn enig-paginatoepassingen gebruiken? {#section_459C1BEABD4B4A1AADA6CF4EC7A70DFB}

Ja, u kunt VEC voor uw SPA gebruiken als u at.js 2.x gebruikt. Voor meer informatie, zie [Enige Pagina (SPA) Visuele Composer](/help/c-experiences/spa-visual-experience-composer.md)van de Ervaring.

## Kan ik de Adobe Experience Cloud Debugger gebruiken met at.js implementaties? {#section_FF3CF4C5FD2F4DB1BF1A6B39DA161637}

Ja. U kunt mboxTrace voor het zuiveren doeleinden of de Hulpmiddelen van de Ontwikkelaar van uw browser ook gebruiken om de verzoeken van het Netwerk te inspecteren, filtrerend aan &quot;mbox&quot;om mbox vraag te isoleren.

## Kan ik speciale karakters in mbox namen met at.js gebruiken? {#section_8E31D2E8A27642098934D7DACFB2A600}

Ja, hetzelfde als met mbox.js.

## Waarom worden mijn dozen niet op mijn webpagina&#39;s geactiveerd? {#section_4BA5DA424B734324AAB51E4588FA50F5}

De doelklanten gebruiken soms op wolk-gebaseerde instanties met [!DNL Target] voor het testen of eenvoudige proef-van-concept doeleinden. Deze domeinen, en vele anderen, maken deel uit van de [Openbare Lijst](https://publicsuffix.org/list/public_suffix_list.dat)van het Achtervoegsel.

Moderne browsers slaan cookies niet op als u deze domeinen gebruikt, tenzij u de `cookieDomain` instelling aanpast met targetGlobalSettings(). Zie Op cloud gebaseerde instanties [gebruiken met Doel](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-target-debugging-atjs/targeting-using-cloud-based-instances.md#concept_A2077766948F4EA081CE592D8998F566)voor meer informatie.

## Kunnen IP adressen als koekjesdomein worden gebruikt wanneer het gebruiken van at.js? {#section_8BEEC91A3410459D9E442840A3C88AF7}

Ja, als u [at.js versie 1.2 of later](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md#reference_DBB5EDB79EC44E558F9E08D4774A0F7A)gebruikt. We raden u echter ten zeerste aan de nieuwste versie bij te houden.

>[!NOTE]
>
>De volgende voorbeelden zijn niet nodig als u at.js versie 1.2 of later gebruikt.

Afhankelijk van hoe u [targetGlobalSettings](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetgobalsettings.md)gebruikt, zou u extra wijzigingen in de code kunnen moeten aanbrengen na het downloaden at.js. Als u bijvoorbeeld iets verschillende instellingen voor uw [!DNL Target] implementaties op verschillende websites nodig hebt en deze instellingen niet dynamisch kunt definiëren met behulp van aangepaste JavaScript, kunt u deze aanpassingen handmatig doorvoeren nadat u het bestand hebt gedownload en voordat u het bestand uploadt naar de desbetreffende website.

In de volgende voorbeelden kunt u de functie `targetGlobalSettings()` at.js gebruiken om een codefragment in te voegen ter ondersteuning van IP-adressen:

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

Dit bericht heeft geen betrekking op [!DNL at.js] functionaliteit. De [!DNL at.js] bibliotheek probeert om het even wat te melden die niet in DOM kan worden gevonden.

Als dit waarschuwingsbericht wordt weergegeven, zijn de volgende mogelijke hoofdoorzaken:

* De pagina wordt dynamisch samengesteld en at.js kan het element niet vinden.
* De pagina wordt langzaam samengesteld (vanwege een traag netwerk) en at.js kan de kiezer niet vinden in de DOM.
* De paginastructuur waarop de activiteit wordt uitgevoerd, is gewijzigd. Als u de activiteit in de Visuele Composer van de Ervaring (VEC) heropent, zou u een waarschuwingsbericht moeten krijgen. U moet de activiteit bijwerken zodat alle noodzakelijke elementen kunnen worden gevonden.
* De onderliggende pagina maakt deel uit van een toepassing voor één pagina (SPA) of de pagina bevat elementen die verder naar beneden op de pagina worden weergegeven en het [!DNL at.js] &quot;opiniepeilingsmechanisme voor kiezers&quot; kan die elementen niet vinden. Het `selectorsPollingTimeout` kan helpen om de snelheid te verhogen. Zie [targetGlobalSettings()](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetgobalsettings.md)voor meer informatie.
* Om het even welke klik-volgende metrisch probeert om aan elke pagina toe te voegen, ongeacht URL waarop metrisch opstelling was. Hoewel onschuldig, maakt deze situatie veel van deze berichten tonen.

   Voor de beste resultaten downloadt en gebruikt u de nieuwste versie van [!DNL at.js]. Voor meer informatie, zie [bij.js de Details](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md#reference_DBB5EDB79EC44E558F9E08D4774A0F7A) van de Versie en [Download bij.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/implementing-target-without-a-tag-manager.md#concept_1E1F958F9CCC4E35AD97581EFAF659E2).

## Wat is het domein tt.omtr dc.net dat de servervraag van het Doel gaat? {#section_999C29940E8B4CAD8A957A6B1D440317}

[!DNL tt.omtrdc.net] is de domeinnaam voor Adobe EDGE netwerk, dat wordt gebruikt om alle vraag naar Doel te ontvangen.

## Waarom gebruiken at.js en mbox.js geen vlag HttpOnly en Veilige koekjes? {#section_74527E3B41B54B0A83F217C3E664ED1F}

HttpOnly kan alleen worden ingesteld via code op de server. Doelcookies, zoals mbox, worden gemaakt en opgeslagen via JavaScript-code, zodat Target de Cookie-vlag HttpOnly niet kan gebruiken.

Beveiliging kan alleen via JavaScript worden ingesteld wanneer de pagina via HTTPS is geladen. Als de pagina voor het eerst wordt geladen via HTTP, kan JavaScript deze markering niet instellen. Als de markering Beveiligen wordt gebruikt, is de cookie bovendien alleen beschikbaar op HTTPS-pagina&#39;s.

Om ervoor te zorgen dat Doel gebruikers correct kan volgen, en omdat de koekjes cliënt-kant worden geproduceerd, gebruikt Target geen van beide vlaggen.

## Hoe vaak brand at.js een netwerkverzoek? {#section_57C5235DF7694AF093A845D73EABADFD}

Adobe Target voert al zijn besluiten op de server uit. Dit betekent dat at.js elke keer dat de pagina opnieuw wordt geladen of een openbare API van at.js wordt aangeroepen, een netwerkverzoek in werking stelt.

## In het beste geval, kunnen wij verwachten dat de gebruiker geen zichtbare gevolgen op paginading met betrekking tot het verbergen van, het vervangen van, en het tonen van inhoud ervaart? {#section_CB3C566AD61F417FAC0EC5AC706723EB}

at.js probeert te vermijden pre-verbergend het LICHAAM of andere DOM elementen voor een lange periode, maar dit hangt van netwerkvoorwaarden en activiteitenopstelling af. at.js bevat [instellingen](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetgobalsettings.md) waarmee u de BODY-verbergende CSS-stijl kunt aanpassen. In plaats van de volledige HTML-BODY te blanco, kunt u alleen bepaalde delen van de pagina vooraf verbergen. De verwachting is dat die onderdelen DOM-elementen bevatten die &quot;gepersonaliseerd&quot; moeten worden.

## Wat is de opeenvolging van gebeurtenissen in een gemiddeld scenario waar een gebruiker voor een activiteit kwalificeert? {#section_56E6F448E901403FB77DF02F44C44452}

Het verzoek at.js is een async `XMLHttpRequest`, zodat voeren wij de volgende stappen uit:

1. De pagina wordt geladen.
1. at.js prehides the HTML BODY. Er is een instelling voor het vooraf verbergen van een bepaalde container in plaats van de HTML-BODY.
1. De aanvraag at.js wordt geactiveerd.
1. Nadat het doelantwoord is ontvangen, extraheert Target de CSS-kiezers.
1. Met CSS-kiezers maakt Target STIJL-tags om de DOM-elementen die worden aangepast, vooraf te verbergen.
1. De vooraf verborgen STIJL voor het HTML-LICHAAM wordt verwijderd.
1. Doel start opiniepeiling voor DOM-elementen.
1. Als een DOM-element wordt gevonden, past Target DOM-wijzigingen toe en wordt de vooraf verborgen STIJL van het element verwijderd.
1. Als DOM-elementen niet worden gevonden, worden de elementen tijdens een algemene time-out niet verborgen om te voorkomen dat een pagina wordt verbroken.

## Hoe vaak wordt de inhoud van de pagina volledig geladen en zichtbaar wanneer at.js definitief het element ontverbergt de activiteit verandert? {#section_01AFF476EFD046298A2E17FE3ED85075}

Gezien het bovenstaande scenario, hoe vaak wordt de inhoud van de pagina volledig geladen en zichtbaar wanneer at.js definitief het element ontverbergt de activiteit verandert? Met andere woorden, de pagina is volledig zichtbaar behalve de inhoud van de activiteit, die dan lichtjes na de rest van de inhoud wordt onthuld.

at.js blokkeert niet dat de pagina wordt weergegeven. Een gebruiker zou sommige lege gebieden op de pagina kunnen opmerken die elementen vertegenwoordigen die door Doel zullen worden aangepast. Als de toe te passen inhoud niet vele verre activa, zoals SCRIPTs of IMGs bevat, zou alles snel moeten teruggeven.

## Hoe zou een volledig caching pagina het bovengenoemde scenario beïnvloeden? Zou het waarschijnlijker zijn dat de inhoud van de activiteit merkbaar zichtbaar wordt nadat de rest inhoud van de pagina laadt? {#section_CE76335A3E0B41CB8253DEE5E060FCDA}

Als een pagina in het cachegeheugen is opgeslagen op een CDN die zich dicht bij de locatie van de gebruiker bevindt, maar niet bij de rand van het doel, kan die gebruiker enige vertragingen zien. De doelranden zijn goed over de hele wereld verdeeld, dus dit is niet de meeste tijd een kwestie.

## Is het mogelijk dat een hoofdafbeelding na een korte vertraging wordt weergegeven en vervolgens wordt omgewisseld? {#section_C25B07B25B854AAE8DEE1623D0FA62A3}

Met het volgende scenario:

De time-out Doel is vijf seconden. Een gebruiker laadt een pagina die een activiteit heeft om een hoofdafbeelding aan te passen. at.js verzendt het verzoek om te bepalen als er een activiteit is om toe te passen, maar er is geen aanvankelijke reactie. Veronderstel de gebruiker de regelmatige inhoud van het heldenbeeld ziet, omdat geen reactie van Target werd ontvangen betreffende of er een bijbehorende activiteit is. Na vier seconden, keert het Doel een reactie met de activiteiteninhoud terug.

Zou het in dit stadium mogelijk zijn de alternatieve versie te tonen? Na vier seconden kon de hoofdafbeelding worden omgewisseld en kon de gebruiker deze afbeeldingswisseling zien?

In eerste instantie is het DOM-element voor de held van de afbeelding verborgen. Nadat een reactie van Doel is ontvangen, past at.js de DOM-wijzigingen toe, zoals het vervangen van de IMG en het weergeven van de aangepaste hoofdafbeelding.

## Welk HTML-doctype vereist at.js?

at.js vereist het HTML 5-documenttype.

Deze syntaxis is:

`<!DOCTYPE html>`

Het HTML 5-documenttype zorgt ervoor dat de pagina in de standaardmodus wordt geladen. Bij het laden in de modus Kirken zijn sommige JS API&#39;s waarvan at.js afhankelijk is, uitgeschakeld. Doel schakelt in de modus Kirken de optie at.js uit.
