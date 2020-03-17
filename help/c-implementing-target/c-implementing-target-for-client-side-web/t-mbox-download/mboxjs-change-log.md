---
keywords: mbox.js changes;mbox.js versions
description: Op deze pagina worden wijzigingen in elke versie van mbox.js weergegeven.
title: mbox.js, versiedetails
subtopic: Getting Started
uuid: 5f8e0511-637b-4c17-bb19-aa7f4d7c98ea
translation-type: tm+mt
source-git-commit: 217ca811521e67dcd1b063d77a644ba3ae94a72c

---


# mbox.js, versiedetails{#mbox-js-version-details}

Op deze pagina worden wijzigingen in elke versie van mbox.js weergegeven.

>[!NOTE]
>
>We raden alle gebruikers van mbox.js aan een upgrade naar versie 57 of hoger uit te voeren. Sommige gebruikers hebben time-outproblemen ervaren wanneer deze `target.js` niet konden worden geladen. Versie 57 heeft dat probleem opgelost. Als u echter de [!DNL Experience Cloud Visitor ID] service gebruikt, is versie 58 of hoger vereist.

De manier waarop Doel reageert op aanroepen vanuit uw pagina is afhankelijk van de versie van de doelbibliotheek die u gebruikt, of de implementatie van de bezoekersidentiteitskaart aanwezig is en of de bezoekersidentiteitskaart bestaat. Voor informatie, zie de Reacties van de Vraag van het [Doel door de Versie](../../../c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/call-responses-library-version.md#concept_A95A4758A1E7405D947E9B4BCB5D62F0)van de Bibliotheek.

>[!NOTE]
>
>De bibliotheek mbox.js wordt niet meer ontwikkeld. Alle klanten moeten van mbox.js naar at.js migreren. Zie [Migreren naar at.js vanuit mbox.js voor meer informatie](../../../c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-target-atjs-implementation/target-migrate-atjs.md#task_DE55DCE9AC2F49728395665DE1B1E6EA).

## mbox.js versie 63 {#section_ED8EFCF653A845ED8927F759578C4A33}

**Doelversie:** 17.7.1

[!DNL mbox.js] versie 63 is nu beschikbaar. Zie [Download mbox.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/target-download-config-mbox.md)voor meer informatie.

De volgende verbeteringen en correcties zijn opgenomen in [!DNL mbox.js] versie 63:

* Oplossing voor een probleem met het genereren van SDID&#39;s bij gebruik `mboxDefine()` en `mboxUpdate()`. Dit is alleen van toepassing op clients met de API voor bezoekers op de pagina.

## mbox.js versie 62 {#section_723A9119FE204183847D3B0929A99B41}

* Problemen met flikkering bij omleidingsactiviteiten zijn opgelost bij weergave in Google Chrome-browsers.
* Toegevoegde `secureOnly` instelling die aangeeft of mbox.js alleen HTTPS mag gebruiken of mag schakelen tussen HTTP en HTTPS op basis van het paginaprotocol. Dit is een geavanceerde instelling die standaard op Onwaar wordt ingesteld.

## mbox.js versie 61 {#section_F3B59C5578B64883AE013B9342151193}

**Doelversie:** 16.7.2.

**Releasedatum:** 28 juli 2016

mbox.js versie 61 bevat de volgende verbeteringen:

* Het generatiealgoritme van de id mboxSession in de JavaScript Date-API genereert nu een willekeurige tekenreeks in plaats van een tijdstempel plus een willekeurige tekenreeks.
* De volgende details zijn alleen van toepassing als u de API voor bezoekers op de pagina hebt:

   * [!DNL mbox.js] versie 61 heeft geen voorrang op de `loadTimeout` eigenschap van de Bezoeker-API. Clients kunnen de integratie van de Bezoeker-API beheren met `visitorApiTimeout` + `visitorApiPageDisplayTimeout` .
   * Er is een `optoutEnabled` instelling toegevoegd ter ondersteuning van de toekomstige functie voor het uitschakelen van Adobe Experience Cloud. De standaardwaarde is false. Als dit bezit wordt toegelaten, voeren alle verzoeken asynchroon tegen het [!DNL /ajax] eindpunt, enkel als versie 60 uit.
   * Het verbergen van de hoofdtekst wordt standaard uitgeschakeld. Het doel gebruikt body Hide alleen wanneer global mbox auto-create is ingeschakeld en body-hide is ingeschakeld.
   * Als er geen Experience Cloud Visitor ID-cookies zijn, worden alle aanvragen asynchroon uitgevoerd op basis [!DNL /ajax] van het laden van de eerste pagina. Bij het laden van de tweede pagina gebruikt Target de normale flow, omdat er al waarden voor de bezoeker-id aanwezig zijn.
   * Als u Adobe Analytics gebruikt als bron voor rapportage van uw activiteit, hoeft u tijdens het maken van activiteiten geen trackingserver op te geven als u mbox.js versie 61 (of hoger) of versie 0.9.1 (of hoger) gebruikt. De bibliotheek mbox.js of at.js verzendt automatisch het volgen serverwaarden naar [!DNL Target]. Tijdens het maken van activiteiten kunt u het [!UICONTROL Tracking Server] veld leeg laten op de [!UICONTROL Goals & Settings] pagina.

## mbox.js versie 60 {#section_3BDAB885FA13444A8D35940A4BFF5825}

**Doelversie:** 16.4.1.

**Releasedatum:** 21 april 2016

Pagina-inhoud is standaard niet verborgen. Versie 60 verbergt alleen de pagina-inhoud wanneer de optie Globale box automatisch maken is ingeschakeld. De CSS- `opacity:0` eigenschap wordt gebruikt voor pagina verbergen in plaats van `display:none`. Dit verzekert juiste levering voor ontvankelijke plaatsen en richt zich op [!DNL at.js].

U kunt het verbergen van het lichaam inschakelen door twee instellingen te gebruiken:

* `bodyHidingEnabled` De standaardwaarde is false, wat betekent dat de HTML-BODY niet verborgen is.

* bodyHiddenStyle

   De standaardwaarde is `body{opacity:0}`. Deze waarde kan worden gewijzigd in iets anders, bijvoorbeeld `body{display:none}`.

U kunt deze instellingen negeren door bijvoorbeeld de volgende instellingen op te nemen:

```
<script> 
window.targetGlobalSettings = { 
 bodyHidingEnabled: true, 
 bodyHiddenStyle: "body{opacity:0}", 
 visitorApiPageDisplayTimeout: 2000 
}; 
</script>
```

De techniek voor het verbergen van pagina&#39;s maakt gebruik van stijllabels om stijlen toe te voegen en te verwijderen. Zo zorgt u ervoor dat de stijlen van de site ongewijzigd blijven nadat de code voor het verbergen van de pagina is uitgevoerd.

**DTM-gebruikers:** Merk op dat dit u zal verhinderen de Automatische invoeroptie te gebruiken aangezien er geen manier is om de bovengenoemde configuratie in het Doel UI op te slaan. U dient de bovenstaande instructies te gebruiken en de inhoud vervolgens in het codevak van de optie Aangepast hosten te plakken.

Ook in Versie 60, als het [!DNL visitorAPI.js] dossier voor de dienst van identiteitskaart van de Bezoeker van de Wolk van de Ervaring aanwezig is, worden alle dozen gevraagd via een eindpunt AJAX. Dit is vereist omdat de API-methoden van de bezoeker asynchroon zijn. Een voordeel van deze aanpak is dat de tijd van Rendering starten aanzienlijk is verminderd, omdat aanvragen voor een box de rendering niet blokkeren. Dit betekent echter ook dat alle [!DNL Target] aanbiedingsinhoud asynchroon loopt, zodat alle aanbiedingscode dienovereenkomstig moet worden geschreven. Aanbiedingen met code `document.write` en andere code die ervan uitgaat dat deze worden uitgevoerd bij het laden van de eerste pagina, worden niet uitgevoerd zoals verwacht.

* asynchrone aanroepen van V60

   Wanneer u v60 gebruikt met de service bezoekersidentiteitskaart, worden alle mbox-aanroepen asynchroon uitgevoerd. Dit is een verandering van hoe dozen altijd hebben gewerkt, dus voorzie als het bevorderen aan deze versie. Herzie de [Asynchrone sectie van Overwegingen](../../../c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-target-atjs-implementation/target-atjs-limitations.md#section_B586360A3DD34E2995AE25A18E3FB953) van de [!DNL at.js] documentatie ( [!DNL at.js] gebruikt ook asynchrone vraag) om enkele risico&#39;s te begrijpen.
* Nieuwe bezoekersscenario&#39;s kunnen flikkeren

   Wanneer u v58 tot v60 gebruikt met de service bezoekersidentiteitskaart, wachten mbox-aanroepen tot de bezoekersidentiteitskaart is ingesteld voordat deze wordt geactiveerd (of tot er een time-out is opgetreden). Dit gebeurt bij het laden van de eerste pagina van een nieuwe bezoeker.

## mbox.js versie 59 {#section_FF0E70C4C17E402D8374DE428C5D996E}

**Doelversie:** 16.2.1.

**Releasedatum:** 17 februari 2016

mbox.js versie 59 bevat de volgende verbeteringen:

* Mbox uitgeschakeld is tot 30 minuten verkleind
* Een probleem met betrekking tot het verbergen/verbergen van pagina&#39;s is opgelost

   In plaats van de pagina `display:none` te verbergen zoals in versie 58, wordt `opacity:0` gebruikt. Dit verhelpt problemen met responsieve sites die het gevolg zijn van de vorige methode om de pagina te verbergen.

## mbox.js, versie 58 {#section_5070B0D1C87F4937BB97727923DD36C7}

**Doelversie:** 15.7.1

**Releasedatum:** 30 juli 2015

Deze versie van mbox.js wordt vereist als u Analytics als rapporteringsbron voor Doel gebruikt en hoogst geadviseerd voor Profielen en Soorten publiek.

Versie 58 van mbox.js verzekert de dienst van identiteitskaart van de Bezoeker van de Wolk van de Ervaring met een bezoekersidentiteitskaart alvorens de vraag van het Doel wordt gemaakt. Dit zorgt ervoor dat de publieksgegevens die door de de kerndienst van Profielen en van het publiek worden gedeeld beschikbaar voor de eerste vraag van het Doel in de zitting van de bezoeker zijn. Als u wilt voorkomen dat de standaardinhoud wordt geflikkerd voordat de testinhoud wordt geretourneerd, verbergt Target de inhoud `<BODY>` totdat de bezoekersidentiteitsservice wordt geretourneerd. `display:none` wordt gebruikt om de pagina te verbergen.

Deze update verhelpt ook een probleem bij het gebruik van Analytics als rapportagebron voor Target die ertoe heeft geleid dat een opgeblazen aantal bezoekers in Analytics is gerapporteerd voor bezoeken die slechts één pagina bevatten.

Mbox.js stelt time-outwaarden in voor het geval de bezoeker-id-service niet wordt geretourneerd. De standaardtime-out voor de service bezoekersidentiteitskaart is 500 ms (0,5 seconden). Met een extra time-out stelt u de bovengrens in voor de tijd dat de `<BODY>` tag wordt verborgen. Deze standaardwaarde is 500 ms (0,5 seconden). Deze onderbrekingen kunnen worden gewijzigd door de volgende code vóór de verwijzing mbox.js op elke pagina in te voegen:

```
<script> 
window.targetGlobalSettings = { 
 visitorApiTimeout: 500, 
 visitorApiPageDisplayTimeout: 500 
}; 
</script> 
```

Versie 58 en hoger van Mbox.js voert niet-JavaScript inhoud voor globale mbox onmiddellijk uit nadat de markering van HTML aanwezig is. `BODY` JavaScript-inhoud binnen `<script>` tags voor de globale box wordt uitgevoerd nadat de `DOMContentLoaded` gebeurtenis is geactiveerd. Deze volgorde van levering van inhoud zorgt ervoor dat JavaScript-inhoud voor de globale box correct wordt geleverd en weergegeven.

## mbox.js versie 57 {#section_6BA1CDBF75B14A94B59E8624ACF583D4}

**Doelversie:** 15.4.1.

**Releasedatum:** 21 april 2015

De volgende wijzigingen zijn aangebracht in deze versie:

* Auto-created global mbox response for Target Standard gebruikt document.write() niet meer of maakt een <div> element.

   Hierdoor wordt de vereiste dat het bestand mbox.js het laatste item in het dialoogvenster <head><meta http-equiv="Content-Type" content="text/html; charset=UTF-8"> van de pagina. Sterke QA wordt geadviseerd wanneer het bevorderen aan deze nieuwe versie.

   Deze verandering zou veranderingen in gedrag kunnen veroorzaken wanneer het leveren van sommige aanbiedingstypes. Hieronder volgen de specifieke omstandigheden die in overweging moeten worden genomen:

   * De HTML-inhoud die wordt geretourneerd als onderdeel van een &quot;insteekmodule-aanbieding&quot; wordt niet correct gerenderd, maar JavaScript in de aanbiedingen wordt naar behoren uitgevoerd.
   * JavaScript-aanbiedingen die worden geretourneerd aan de globale box, kunnen de JavaScript-code bevatten die is ingesloten in de `<script>` tag of waarnaar wordt verwezen door een `src` kenmerk.

      Om dit te doen, voeg de `async` attributen aan de manuscriptvraag toe, als volgt:

      `<script src='external-url' async='true'></script>`

      Merk op dat het `async` attribuut beperkte steun in Internet Explorer (details hier: [https://developer.mozilla.org/en/docs/Web/HTML/Element/script#Browser_compatibility](https://developer.mozilla.org/en/docs/Web/HTML/Element/script#Browser_compatibility)) moet u dus bezoekers die oudere IE-versies gebruiken uitsluiten van tests die deze scripts van derden bevatten.

* Oplossing voor problemen die in versie 56 werden gemeld als gevolg van wijzigingen in de sectie Extra JavaScript van mbox.js. Alle code in de sectie Extra JavaScript is opnieuw beschikbaar in het algemene bereik.

De volgende functionaliteit wordt niet ondersteund in mbox.js versie 57:

* Een automatisch gemaakt algemeen mbox dat is gegenereerd in Target Standard, werkt niet met gehoste aanbiedingstypen uit Target Classic. Tot de soorten gehoste voorstellen behoren &quot;voorstel op uw site&quot; en &quot;voorstel buiten Test&amp;Target.&quot;

   Dit betekent dat u in Target Classic de automatisch gemaakte globale box niet moet selecteren vanuit Target Standard wanneer een van deze aanbiedingen vereist is.
* Alleen JavaScript-insteekmodules worden ondersteund.

   Als in de aanbieding van een plug-in JavaScript-code en HTML worden gecombineerd, wordt de JavaScript-code uitgevoerd, maar wordt de HTML-inhoud niet weergegeven.

mbox.js versie 57 bevat ook belangrijke oplossingen:

* Probleem verholpen waarbij de SiteCatalyst-plug-in niet werkte in mbox.js v56.
* Probleem verholpen waarbij extra JavaScript-fouten zijn opgetreden als gevolg van bereikwijziging.
* Wijzigingen in constructor van mboxFactory herstellen.

## mbox.js, versie 56 {#section_C4F4A53584B741FF9FD907D81CB7E164}

**Doelversie:** 15.1.2.

**Releasedatum:** 17 februari 2015

>[!NOTE]
>
>Sommige gebruikers hebben time-outproblemen ervaren wanneer deze `target.js` niet konden worden geladen. Versie 57 heeft dat probleem opgelost. Als u echter de [!DNL Experience Cloud Visitor ID] service gebruikt, is versie 58 of hoger vereist.

De volgende wijzigingen zijn aangebracht in deze versie:

* Wijzigingen voor Premium-aanbevelingen ter ondersteuning van het doorgeven van parameters in algemene mbox
* Voegt een 5 tweede onderbreking aan de target.js ladingsvraag toe. In het zeldzame geval dat het dossier niet laadt, zal de pagina teruggeven en geen activiteiten van de Norm van het Doel zullen tonen.
* &quot;extra JavaScript&quot; verplaatst om te worden uitgevoerd vóór globale box

   Alle instellingen in v56+ hebben een naamruimte. Als er functies zijn gedeclareerd in &quot;extra JavaScript&quot;, moeten deze vooraf worden ingesteld `window`.

   Bijvoorbeeld:

   `function foo {`

   `}`

   Wordt:

   `window.foo = function() {`

   `}`

   Ook variabelen die algemeen toegankelijk moeten zijn, moeten vooraf worden vastgelegd `window`.

* Er is een cookie met de naam &quot;em-disabled&quot; toegevoegd die mbox.js aan de gebruiker geeft wanneer target.js niet kan worden geladen tijdens de levering. Dit koekje verhindert aanbiedingen die gebruikend de Visuele Composer van de Ervaring worden gecreeerd op de plaats terug te geven. Gebruikers met dit cookie zien de testinhoud niet en worden niet meegeteld in deze activiteitenrapporten. Alle andere aanbiedingsinhoud (bijvoorbeeld uit campagnes in Target Classic) wordt verder geladen. De cookie heeft een levensduur van 30 minuten vanaf het moment dat het laden mislukt.

## mbox versie 55

**Doelversie:** 15,1

**Releasedatum:** 19 januari 2015

Hiermee wijzigt u versie 53 met IE-oplossingen.

## mbox versie 54

**Doelversie:** 14.9.2.

**Releasedatum:** 30 september 2014

Verandert de globale mbox implementatie in AJAX van document.write. Hierdoor wordt de vereiste dat het bestand mbox.js het laatste item in de pagina moet zijn, verwijderd <head><meta http-equiv="Content-Type" content="text/html; charset=UTF-8"> sectie. Deze versie is alleen beschikbaar via de API. Clients kunnen het bestand downloaden en dit bestand mbox.js gebruiken. Sommige sites ervaren inhoud die met deze implementatie flikkert. Controleer daarom de integratie op uw site.

## mbox versie 53

**Doelversie:** 14.9.1

**Releasedatum:** 14 september 2014

Probleem verholpen waarbij de parameters van de doelpagina niet correct in Internet Explorer werden afgespeeld.

## mbox versie 52

**Doelversie:** 14,8

**Releasedatum:** 14 augustus 2014

De functie mboxParameter werkt nu in Target Standard en Premium.

Probleem opgelost waarbij Analytics tracking niet meer werkte in IE 9 &amp; 11. Deze wijziging is alleen van toepassing op gebruikers van Analytics.

Nu kunt u parameters [](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-understanding-global-mbox/pass-parameters-to-global-mbox.md) doorgeven als een array, als een JSON-object of als een door komma&#39;s gescheiden lijst (voorheen ondersteund) naar target-global-mbox met behulp van de functie targetPageParams().

Naam gewijzigd in M2PcId en alles wat te maken heeft met de VisitorId.

De defaultDiv van een geregistreerd selectievakje mag worden gewist.

## mbox versie 51

**Doelversie:** 14,6

**Releasedatum:** 25 juni 2014

Het probleem waarbij een onjuist cookie werd ingesteld in sites met twee tekens in het bovenste domein, is opgelost.

Probleem verholpen waarbij een kleine fout in mbox.js werd opgelost die ertoe leidde dat hashtagwaarden werden geretourneerd.

## mbox versie 50

Verbeterde synchronisatie tussen Target Standard en Target Classic.

## mbox versie 49

Verbeterde Internet Explorer 10-ondersteuning voor geneste vakken.

## mbox versie 48

Extra ondersteuning voor Adobe Analytics als rapportbron voor Target.

## mbox versie 47

mbox.js ondersteunt nu het gebruik van een aangepaste globale naam voor Target Standard.

## mbox versie 46

Volledige ondersteuning toegevoegd voor de service Experience Cloud-bezoekersidentiteitskaart voor de implementatie van één regel code door Target Standard. Hierdoor wordt integratie van Adobe Analytics op de server en het gedeelde Experience Cloud-profiel ingeschakeld.

Oplossing voor een probleem met het leveren van inhoud in IE10 in documentmodus.

## mbox versie 45

Volledige ondersteuning toegevoegd voor de service Experience Cloud-bezoekersidentiteitskaart Hierdoor wordt integratie van Adobe Analytics op de server en het gedeelde Experience Cloud-profiel ingeschakeld.

## mbox versie 44

Nieuwe parameter toegevoegd in URL door mboxVizTarget:

mboxDOMLoaded

## mbox versie 43

Toegevoegde ondersteuning voor doelstandaard.

## mbox versie 42

Aanvankelijke ondersteuning toegevoegd voor Experience Cloud-service voor gedeelde bezoekers-id.

## mbox versie 41

* Zelfs bij de instelling x-only schakelt u het cookie van de eerste partij uit om de laadtijd te verbeteren en te voorkomen dat de pagina doorlopend wordt vernieuwd

   Een onderbrekingskoekje wordt geplaatst als de vraag aan Doel er niet in slaagt op tijd terug te keren. Dit is een snellere methode dan alleen het cookie van derden. Met alleen het cookie van derden wordt de pagina voortdurend vernieuwd in afwachting van een goede reactie van de servers van Target.

* Vaste verkeersbeperking die alleen optreedt wanneer mbox.js is ingeschakeld

   Deze kwestie kwam voor als een klant een verkeersbeperking op hun mbox.js had, veroorzakend het onderbrekingsplaatsen om niet te werken. Dit resulteerde in het verfrissen van de pagina terwijl het wachten op een goede reactie van de servers van het Doel.

* Vaste SiteCalyst-plug-in om altijd de Ajax-fetcher te gebruiken

   Vóór deze wijziging waren er enkele situaties voor gebruikers van de plug-in Test&amp;Target naar SiteCatalyst waarin, afhankelijk van het moment waarop de plug-in is geladen, een document.write kon worden geactiveerd die de pagina zou wissen.

## mbox versie 38

Toegevoegde ondersteuning voor op pagina gebaseerde SiteCatalyst voor test&amp;Target-integratie (moet zijn ingeschakeld)

## mbox versie 37

Gecodeerde URL-sleutels

## mbox versie 36

Veranderd mbox in gebruik tt.omtr dc.net

## mbox versie 35

* Mbox debug is nu altijd extern
* De parameter mboxTime toegevoegd. Deze parameter is de tijd zoals de gebruiker het ziet, in ms sinds het tijdperk, GMT. Dit wordt slechts eenmaal berekend.

## mbox versie 34

* Probeer altijd de nieuwste standaard div op te halen in plaats van naar een versie in de cache te verwijzen.

   Hiermee wordt een probleem verholpen waarbij de standaardinhoudsdiv in de cache zich niet in de DOM bevindt als gevolg van een mboxUpdate, die de inhoud voor de standaarddiv bevat.

* mbox.getDefaultDiv heeft een nieuwe optionele booleaanse parameter. Indien waar (true), wordt het huidige standaarddiv geretourneerd. Indien false, wordt het laatste standaard div-element in de cache geretourneerd.
* Bijgewerkt mbox.loaded voor ondersteuning van Ajax-belasting
* De parameter mboxURL is nu gecodeerd met encodeURIComponent in plaats van escape
* Test of encodeURIComponent door browser wordt gesteund en toon standaardinhoud als het niet is. Verwijderde ook de volgende mbox.js config opties:
   * encode\_mbox\_parameters
   * mbox\_signal\_support
