---
keywords: known issues;resolved issues;release notes;bugs;issues;fixes
description: Informatie over bekende problemen voor deze release van Adobe Target. Bevat ook informatie over problemen die zijn opgelost.
title: Bekende problemen en opgeloste problemen in Adobe Target
uuid: f8e8e057-1842-4922-ab7f-4d5441048573
translation-type: tm+mt
source-git-commit: 270fc448eb4d3a13d6593b45a0956edfa72f58c5
workflow-type: tm+mt
source-wordcount: '3327'
ht-degree: 0%

---


# Bekende problemen en opgeloste problemen{#known-issues-and-resolved-issues}

Informatie over bekende problemen voor deze release van Target. Bevat ook informatie over problemen die zijn opgelost.

>[!NOTE]
>
>De uitgiftenummers tussen haakjes zijn bedoeld voor intern gebruik van Adobe.

## Bekende problemen {#section_AEDC98B67CF24C9F8E0CF0D2EB9ACAEF}

In de volgende secties worden de bekende problemen voor [!DNL Target]:

### Paginalevering {#page-delivery}

Als u een sjabloonregel toevoegt, zoals de URL (/checkout, /cart) in [paginalevering](/help/c-activities/t-experience-target/t-xt-create/xt-activity-url.md), worden extra spaties aan uw regels toegevoegd. Dit is een cosmetische kwestie en heeft geen invloed op het creëren van publieksdefinities en het aanbieden van levering. (TGT-35916)

### Koppelingen voor QA-voorvertoningen voor activiteit {#preview}

[De QA-voorbeeldkoppelingen voor activiteit](/help/c-activities/c-activity-qa/activity-qa.md) voor opgeslagen activiteiten worden mogelijk niet geladen als uw account te veel opgeslagen activiteiten bevat. Het opnieuw proberen van de voorvertoningskoppelingen zou moeten werken. Als u wilt voorkomen dat dit gebeurt, archiveert u opgeslagen activiteiten die niet meer actief worden gebruikt. (TNT-32697)

### Aanbiedingen omleiden {#redirect}

Hier volgen bekende problemen met omleidingsvoorstellen:

* Onder bepaalde omstandigheden heeft een beperkt aantal klanten een hogere mate van variatie in de verkeersverdeling gemeld bij het gebruik van een omleidingsaanbod in activiteiten die met Analytics for Target (A4T) zijn geconfigureerd. Adobe engineers werken momenteel aan dit probleem.
* De omleiding van activiteiten in implementaties at.js zou de voorproef URL kunnen veroorzaken om in een lijn in te gaan (de aanbieding wordt herhaaldelijk geleverd). In plaats daarvan kunt u de modus [](../c-activities/c-activity-qa/activity-qa.md#concept_9329EF33DE7D41CA9815C8115DBC4E40) QA gebruiken om de voorvertoning en QA uit te voeren. Deze kwestie heeft geen invloed op de daadwerkelijke levering van het aanbod. (TGT-23019)

### Grafiekrapport voor een Auto-Target-activiteit kan niet worden gerenderd wanneer een aangepaste ervaring als besturingselement wordt gebruikt

In het grafiekrapport voor een Auto-Target-activiteit worden geen &quot;differentiële&quot; modi (Gemiddelde optillen en Dagelijkse optillen) weergegeven als er geen gegevens (0 bezoeken) in enige ervaring zijn. Deze situatie kan zich voordoen tijdens de vroege fase van een activiteit als de controleervaring aan douane wordt geplaatst. Voor de andere wijzen (het Lopen Gemiddelde Controle en Gericht, Dagelijkse Controle en Gericht, en Bezoek) werkt het fijn. Zodra er gegevens zijn (bezoeken die niet gelijk zijn aan nul), wordt het rapport weergegeven zoals verwacht.

### Het laden van een pagina in de VEC annuleren {#cancel}

* Het volgende bekende probleem bestaat momenteel wanneer het annuleren van het laden van een [!UICONTROL A/B Test] [!UICONTROL Experience Targeting] (XT) activiteit binnen VEC die een omleidingsURL bevat.

   In stap één van de driedelige geleide workflow binnen VEC, wanneer u het laden van pagina&#39;s annuleert, wordt het [!UICONTROL Modifications] deelvenster in de VEC weergegeven en wordt de omleiding naar URL-sjabloon toegepast op de ervaring (bijvoorbeeld &#39;Experience B&#39;). Wanneer u naar stap twee of drie gaat en vervolgens terugkeert naar stap één, doet zich de volgende situatie voor.

   Bij &quot;Experience B&quot; wordt standaard de sjabloon voor het laden van de geannuleerde website weergegeven en is het [!UICONTROL Modifications] deelvenster toegankelijk. Dit is niet het geval omdat er een omleiding naar de URL-sjabloon is toegepast. De omleiding naar URL-sjabloon moet worden weergegeven.

   Om de juiste stand van de ervaring in de VEC aan te tonen:

   Als u overschakelt naar een andere ervaring en vervolgens terugschakelt naar &quot;Experience B&quot;, wordt de omleiding naar de URL-sjabloon weergegeven die op deze ervaring is toegepast en is het [!DNL Target] [!UICONTROL Modifications] deelvenster niet toegankelijk. (TGT-32138)

* Bij de websites van de toepassing Eén pagina (SPA) kunt u door het annuleren van het laden geen handelingen bewerken in het [!UICONTROL Modifications] deelvenster.

### Ondersteuning voor Enterprise-machtigingen in Target API&#39;s {#api}

Codeaanbiedingen die zijn gemaakt vanuit de gebruikersinterface van Target in de bibliotheek met aanbiedingen, worden mogelijk weergegeven in de standaardwerkruimte als de lijst met aanbiedingen wordt opgehaald met GET-API&#39;s. Deze kwestie zal in de eerste week van maart 2019 worden geregeld. Nadat deze oplossing is ingesteld, worden de codeaanbiedingen in de juiste werkruimte weergegeven wanneer ze van API&#39;s worden gehaald. Dit probleem heeft *geen* invloed op aanbiedingen die met API&#39;s zijn gemaakt. Codeaanbiedingen die zijn gemaakt op basis van API&#39;s worden bijvoorbeeld weergegeven in de werkruimte waarin ze zijn gemaakt, ongeacht of ze zijn opgehaald met GET-API&#39;s of vanuit de gebruikersinterface van Target.

### Recommendations

Hier volgen enkele bekende problemen met Recommendations-activiteiten:

* Entiteiten zijn na 60 dagen na ontvangst van geen updates via feed of API correct verlopen. de verlopen entiteiten worden echter niet na het verlopen van de zoekindex van de catalogus verwijderd. (IRI-857)
* De &quot;Gebruiksinformatie&quot;-overlays voor Criteria en Ontwerpen weerspiegelen hun gebruik in A/B en de Ervaring gerichte activiteiten (TGT-34331) niet
* Recommendations-aanbiedingen in A/B en Experience Targeting-activiteiten tonen geen visuele voorvertoning van de Recommendations-lade (TGT-33426)
* Verzamelingen, uitsluitingen, criteria en ontwerpen die via de API zijn gemaakt, zijn niet zichtbaar in de Target-gebruikersinterface en kunnen alleen via de API worden bewerkt. (TGT-35777)
* Recommendations-activiteiten die via API zijn gemaakt, kunnen in de gebruikersinterface worden weergegeven, maar kunnen alleen via API worden bewerkt.
* De voedingsstatus van de aangepaste criteria die wordt weergegeven in de weergave Criteria (kaart), wordt elke tien minuten vernieuwd en kan in zeldzame gevallen meer dan tien minuten verouderd zijn. De status die wordt weergegeven in de bewerkingsweergave Aangepaste criteria wordt opgehaald in real-time en is altijd up-to-date. (TGT-35896, TGT-36173)

### MVT-activiteiten (Multivariate Test)

In een MVT-activiteit is de winnaar die in de tabel en grafiek wordt weergegeven, niet consistent bij het controleren van de meetwaarden. Dit komt voor als een gebruiker van Samenvatting aan de Mening van de Grafiek schakelt, dan terug naar Samenvattingsmening, metrisch verandert en dan aan de Mening van de Grafiek schakelt. Wanneer dit probleem optreedt, wordt in de overzichtsweergave altijd de juiste winnaar weergegeven. Als de gebruiker nooit schakelt tussen de overzichtsweergave, wordt in de grafiekweergave de juiste winnaar weergegeven.

### at.js {#atjs}

De volgende problemen zijn bekend met at.js:

* Als u versies at.js gebruikt die ouder zijn dan 2.2.0, worden conversies in Analytics for Target (A4T) niet gerapporteerd als er geen Adobe Analytics-code aanwezig is op pagina-elementen (zoals knoppen). In 0.js 2.2.0 is een oplossing voor dit probleem geïntroduceerd. [Voer een upgrade uit naar de nieuwste versie](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md) van .js als dit probleem optreedt.
* Als u een ervaring zonder wijzigingen maakt met behulp van at.js 2.1.1 of eerder (bijvoorbeeld een standaardeigenschap), wordt de ervaring mogelijk niet meegeteld in rapporten, Analytics for Target (A4T), Adobe Analytics of Google Analytics. Bovendien werkt de [ttMeta-plug-in](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-target-atjs-implementation/target-atjs-plugins.md) mogelijk niet correct.

   Als oplossing gebruikt u een witruimte in de ervaringsinhoud. (TNT-33366)

   >[!NOTE]
   >
   >Een oplossing voor dit probleem is opgenomen in at.js 2.2.0. U zou aan de [recentste versie of at.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md) moeten bevorderen of de oplossing gebruiken bovengenoemde slechts voor at.js versies vroeger dan 2.2.0.

* Wanneer een pagina in Visuele Composer van de Ervaring (VEC) wordt geladen, moet Target bepalen als globale mbox het plaatsen wordt toegelaten of onbruikbaar gemaakt en of entiteitID of categoryID aanwezig is op de plaats waar de gebruiker probeert om de aanbeveling in VEC toe te passen. Op basis van deze informatie wordt de lijst met criteria gefilterd. De standaardlijst bevat gefilterde algoritmen, maar met het selectievakje [](/help/c-recommendations/t-create-recs-activity/algo-select-recs.md) Compatible kunt u de lijst met volledige algoritmen weergeven.

   Als u at.js gebruikt, is het selectievakje Compatibiliteit verborgen, zodat incompatibele algoritmen niet zichtbaar zijn.

   Deze kwestie geldt alleen voor Recommendations-activiteiten die gebruikmaken van de VEC.

   **Oplossing**: Schakel de [!UICONTROL Filter Incompatible Criteria] optie in [!UICONTROL Recommendations > Settings]. Nadat u deze instelling hebt uitgeschakeld, worden alle (compatibele en niet-compatibele) criteria weergegeven in de kiezer voor criteria. (TGT-25949)

* Mboxen die niet worden geactiveerd in Microsoft Explorer 11-browsers na de upgrade naar at.js versie 1.0 vanwege de interactie tussen at.js en Visitor API 2.2.0. Dit probleem is van toepassing op versie 0.js 0.9.6 en hoger. (TNT-27600)
* at.js werkt mogelijk niet met Cordova/Hybrid-apps omdat cookies van de eerste partij momenteel niet in deze toepassingen worden ondersteund. (TNT-26166)

   **Oplossing**: Vorm at.js met de &quot;x-slechts&quot;toegelaten optie en ga `mboxThirdPartyId` in vraag over om gebruikers te beheren.

### mbox.js

De bibliotheek mbox.js ondersteunt geen sjabloontalen aan de clientzijde, zoals Handlebars en Mustache. De bibliotheek at.js *ondersteunt deze talen* niet.

**Opmerking**: De bibliotheek mbox.js wordt niet meer ontwikkeld. Alle klanten moeten van mbox.js naar at.js migreren. Zie [Migreren naar at.js vanuit mbox.js voor meer informatie](../c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-target-atjs-implementation/target-migrate-atjs.md#task_DE55DCE9AC2F49728395665DE1B1E6EA).

### Implementatie: Automatisch een globale box maken

Op het lusje van de Implementatie ([!UICONTROL Administration > Implementation]) zal het [!UICONTROL Global Mbox Auto Create] gebied &quot;vals&quot;door gebrek voor een onlangs provisioned huurder zijn.

Wanneer mbox.js voor het eerst na levering wordt gedownload, wordt het [!UICONTROL Global Mbox Auto Create] gebied geplaatst aan &quot;waar&quot;in het gedownloade mbox.js- dossier en in het [!DNL Target] achtereind, maar het zal als &quot;vals&quot;op de [!UICONTROL Implementation] pagina in UI blijven tonen tot de pagina wordt verfrist (nadat de pagina wordt verfrist, zal de status &quot;waar&quot;zijn).

at.js zal met `global_mbox_autocreate = false` voor een onlangs provisioned huurder worden gedownload. Als mbox.js eerst wordt gedownload, global\_mbox\_autocreate is set to &quot;waar&quot;en at.js zullen ook met `global_mbox_autocreate = true`. worden gedownload. (TGT-15929)

### Succeswaarden

De metriek van het succes met de geavanceerde optie &quot;hoe de telling&quot;zal worden verhoogd geplaatst aan &quot;elke indruk&quot;of &quot;elke indruk (met uitzondering van verfrissingen)&quot;kan niet als succes worden gebruikt metrisch dat een andere metrisch afhangt.

Wanneer een succes metrisch op elke indruk wordt gezet, telt Target opnieuw de bezoeker telkens als de bezoeker dit succes metrisch bezoekt. Target herstelt dan het succes metrische &quot;lidmaatschap&quot;aan 0 zodat kan het opnieuw op de volgende indruk tellen. Aldus, als een andere metrisch vereist deze metrisch om eerst te zijn gezien, zal Target nooit erkennen dat de gebruiker eerste metrisch heeft gezien.

### Analytics voor Target (A4T)

Target-activiteitindrukkingen en -conversies worden momenteel onjuist geteld in Analysis Workspace.

Als oplossing kunt u gebruikmaken van A4T-gegevens in Rapporten en Analytics totdat dit probleem is opgelost.

### Target API&#39;s

Klanten kunnen geen CRUD-bewerkingen uitvoeren op activiteiten voor automatisch toewijzen via de v3-versie van de API voor A/B-activiteiten op Adobe I/O.

### GEO gericht

Op 10 mei 2020 hebben we onze bestanden van de GEO-provider bijgewerkt, waardoor enkele inconsistenties zijn ontstaan. Sommige waarden met komma&#39;s zijn bijvoorbeeld toegevoegd. hoewel de waarden bij het bestaande publiek geen komma hebben . Deze wijziging had geen invloed op al onze leveringsservers. Dientengevolge hebben de kijkers die dergelijke waarden gebruiken, tussen 10 mei en 22 juli 2020 mogelijk niet alle juiste bezoekers gekwalificeerd.

### Afbeelding 0biedt label voor &quot;Verwerking&quot;

Afbeeldingsaanbiedingen op de pagina Aanbiedingen behouden soms het label &quot;Verwerking&quot; enkele uren nadat de afbeeldingen zijn geüpload. In de meeste gevallen is dit alleen een probleem met het etiket: de beeldaanbiedingen kunnen nog steeds worden gebruikt in activiteiten en worden geleverd . In sommige gevallen is een afbeeldingsaanbieding echter mogelijk niet beschikbaar voor de actie Inhoud vervangen > Afbeelding. Als dit gebeurt, moet u het afbeeldingsaanbod opnieuw uploaden en na een paar uur controleren of het aanbod van de afbeelding beschikbaar is voor vervanging. (TGT-37458)

## Opgeloste problemen {#section_FD2FC86E7C734D60B1EDC9DEF60E1014}

Aangezien de bekende problemen hierboven zijn opgelost, worden ze verplaatst naar de volgende secties en worden zo nodig aanvullende opmerkingen toegevoegd.

### Rapportage en extreme orders

Van 25 november 2019 tot 26 april 2020 heeft één Target-server een probleem ervaren dat ertoe heeft geleid dat extreme orderwaarden werden meegeteld in rapporteringsmetriek op basis van inkomsten (AOV, RPV). Van 19 december 2019 tot 23 april 2020 kreeg een andere server hetzelfde probleem. Dit probleem had geen invloed op alle Target-servers of op alle Target-klanten.

U had *geen* invloed als:

* Uw Target-implementatie gebruikt verschillende servers.
* In uw rapporten zijn extreme bestellingen niet uitgesloten.
* U hebt een omzettingsmaatstaf gebruikt om uw activiteiten te meten.
* Uw Target-activiteiten maken gebruik van Analytics for Target (A4T).
* U bevindt zich in de regio Azië-Pacific (APAC).

Neem contact op met de [klantenservice](/help/cmp-resources-and-contact-information.md#concept_34A1CA16F2244D42930BB77846A5ABBB)om te bepalen of dit probleem gevolgen heeft voor uw Target-rapportage.

### Recommendations

* Recommendations feed-index kan &#39;Waiting for index&#39; weergeven als de items in de feed gelijk zijn aan de items in de vorige run. De inname van het product voor levering heeft geen invloed op het product. (RECS-6663)

   Dit probleem is opgelost in de Target-versie 19.4.2.

* Het verwerken van Recommendations-feeds duurt langer dan u had verwacht. (COR-2836)

   Opgelost in Target 16.10.1.

* De interface van de Beelden van de Aanbeveling toont niet het correcte statuut van indexeren. De back-endtaken werken correct, maar de interface kan de huidige status niet ophalen en weergeven.

   Dit probleem is opgelost in de release 17.10.1.

### Aanbiedingen omleiden

Een zeldzame omstandigheid op uw pagina kan ertoe leiden dat paginaweergaven op de oorspronkelijke pagina en op de pagina voor omleiding worden geteld. De implementatie van at.js zal worden bijgewerkt om ervoor te zorgen dat deze rasvoorwaarde kan worden vermeden.

Dit probleem is opgelost in 1.js 1.6.3.

### Uitsluitingsgroepen

* Wanneer auto-dedupe na het creëren van uitsluitingsgroepen wordt toegepast, zou de telling op het activiteitendiagram in UI onjuist kunnen zijn.
* Wanneer bestaande activiteit met de Groep van de Uitsluiting wordt uitgegeven, zouden de handopneming niet correct in UI kunnen worden weerspiegeld.

Deze problemen zijn opgelost.

### Target API&#39;s

v1-versie van de API&#39;s voor aanbiedingen op Adobe I/O behandelt alle aanbiedingen die via Target zijn gemaakt, in de standaardwerkruimte. (TTTEAM-41957)

Dit probleem is opgelost.

### at.js

Mboxen die niet worden geactiveerd in Microsoft Explorer 11-browsers na de upgrade naar at.js versie 1.0 vanwege de interactie tussen at.js en Visitor API 2.2.0. Dit probleem is van toepassing op versie 0.js 0.9.6 en hoger. (TNT-27600)

Opgelost met de release van API 2.3.0 of hoger.

### Geo targeting

Het zoeken naar een tekenreeks die speciale tekens bevat (zoals een spatie of komma) werkt momenteel niet wanneer u doelgroepen maakt. Dit probleem doet zich bijvoorbeeld voor bij het creëren van publiek op basis van steden, staten, landen, enz. Wanneer u bijvoorbeeld zoekt naar &quot;new york&quot;, retourneert de zoekopdracht geen geldige resultaten.

Vast in november 2018.

### at.js

Bij gebruik van at.js versie 1.6.0 vindt een omleiding van Analytics for Target (A4T) plaats, maar zonder kwalificatie van de activiteit.

Correctie met de release van at.js 1.6.2.

### Activiteiten, werkruimten en activiteit-API verwijderen

Activiteiten in de standaardwerkruimte die via de API zijn verwijderd, worden nog steeds weergegeven in de gebruikersinterface van Target. Als tussenoplossing verwijdert u alle activiteiten in de standaardwerkruimte met de gebruikersinterface van Target. (TGT-31315)

Vast 25 oktober 2018

### Automated Personalization (AP)-rapportage op aanbodniveau

Wanneer u op de beoogde ervaring in een rapport van een Automated Personalization-activiteit (AP) klikt om rapportage op aanbiedingsniveau weer te geven, ziet u momenteel lege resultaten, een foutbericht of een draaiend pictogram. (TNT-30695)

Vast op 27 september 2018.

### Code-editor

Als u VEC op stap 1 van de driestapige geleide werkstroom opnieuw laadt terwijl het werken met de Redacteur van de Code in Firefox en Internet Explorer, geeft het lusje van Wijzigingen niet behoorlijk terug; de functionaliteit van VEC wordt echter niet beïnvloed. (TGT-28730)

Dit probleem is opgelost in de release 18.9.1.

### Recommendations-activiteit die een kenmerkpromotieregel gebruikt

Wanneer u een Recommendations-activiteit bewerkt of kopieert die gebruikmaakt van een kenmerkpromotieregel, wordt de fout &quot;Heeft ontbrekend veld&quot; weergegeven wanneer u op Opslaan klikt.

Dit probleem is opgelost in de release 17.8.1.

### Backup Recommendations

Back-upaanbevelingen geven ten onrechte &quot;Enabled&quot; weer op de onlangs bekeken itemkaarten in de gebruikersinterface van Target. (TGT-29308)

Dit probleem is opgelost in de release 18.4.1, zodat &quot;Uitgeschakeld&quot; wordt weergegeven.

### Auto-Target-activiteiten en rapportagepubliek

Wanneer de naam van een rapportagepubliek die in een Auto-Target-activiteit wordt gebruikt, wordt gewijzigd, kunnen verdere updates van Target voor die activiteit mislukken met een foutbericht.

Dit probleem is opgelost met de release van Target 18.5.1 (22 mei 2018).

### at.js

Het algoritme voor het extraheren van het domein op hoofdniveau dat moet worden gebruikt bij het opslaan van cookies is gewijzigd in versie 0.js 0.9.6. Vanwege deze wijziging kunnen cookies niet worden opgeslagen naar adressen die IP gebruiken. Meestal worden IP-adressen gebruikt voor testdoeleinden, maar als tijdelijke oplossingen kunt u DNS-vermeldingen gebruiken, het hostbestand op een lokaal vak aanpassen of de functie targetGlobalSettings() at.js gebruiken om een codefragment in te voegen ter ondersteuning van IP-adressen.

Dit probleem is opgelost in at.js versie 1.2.

### Gebruikersrechten voor Target Premium

Als onderdeel van de migratie naar Enterprise-machtigingen is al het gebruikersbeheer van Target Premium verplaatst van de gebruikersinterface van Adobe Target naar Adobe Admin Console.

Als gevolg van de migratie zijn er twee mogelijke problemen die u dient te kennen:

* Gebruikers die geen beheerder zijn, hebben een e-mail ontvangen waarin wordt aangegeven dat ze nu toegang hebben tot Adobe Target. Dit wijst erop dat de migratie voor uw organisatie werd voltooid. De e-mail zelf kan buiten beschouwing worden gelaten.
* Na de migratie zijn er meldingen geweest dat eerder uitgeschakelde gebruikers opnieuw in de Adobe Admin Console verschenen. Dit kan een probleem voor uw organisatie zijn als gehandicapte gebruikers in de Adobe Admin Console nog steeds op uw gebruikerslijst in Target staan vóór de migratie. Wij adviseren dat de beheerders de lijst van gebruikers in Admin Console herzien om toegang te bevestigen.

Dit probleem is opgelost op 30 augustus 2017

### Activiteiten maken

Een probleem met de release 17.6.2 kan van invloed zijn geweest op activiteiten die zijn gemaakt en/of bijgewerkt tussen 22 juni 2017 en 29 juni 2017. De volgende activiteiten werden beïnvloed:

* Ervaringen die opnieuw zijn gerangschikt in Experience Targeting (XT), zouden terugkeren naar de oorspronkelijke volgorde
* Om het even welke segmentregels lokaal aan de activiteit (niet bewaard binnen een publiek) zouden verloren zijn gegaan: gecombineerde doelgroepen, verfijningen van locaties en regels voor succesmetriek.

Dit had geen gevolgen voor andere activiteiten.

**Belangrijk**: Dit probleem wordt niet automatisch opgelost. U moet alle betrokken activiteiten opnieuw opslaan om het probleem op te lossen.

Dit probleem is op 29 juni 2017 opgelost

### Formuliergebaseerde Experience Composer

De volgende bekende problemen zijn gemeld bij gebruik van de Form-Based Experience Composer:

* Als u de Form-Based Composer van de Ervaring met een doos buiten auto-gecreeerde globale mbox ( doel-globaal-mbox) gebruikt, en dan kiest metrisch als succes metrisch, de metrische verhogingen slechts op pagina&#39;s die de mbox hebben die in de activiteit wordt gebruikt. Als uw box bijvoorbeeld homepage\_mbox is, is de metrische waarde Pagina&#39;s per bezoek het aantal hits op de startpagina\_mbox tijdens dat bezoek. (TGT-22789)
* Er wordt een JavaScript-uitzondering gegenereerd wanneer u tijdens stap 1 van het proces een ervaring verwijdert die betrekking heeft op een Experience Targeting-activiteit (XT) wanneer u de Form-Based Experience Composer gebruikt. (TGT-24366)

Het eerste probleem is opgelost in de Target-versie van 17.3.1 (maart 2017).

Het tweede probleem is opgelost in de Target-versie van 17.6.1 (juni 2017).

### at.js

Sinds de versie van Target 17.4.1 (27 april 2017), die de actie van het Beeld van het Tussenvoegsel in Visual Experience Composer (VEC) gebruikt veroorzaakt dat de aanbiedingsinhoud niet wordt geleverd wanneer het gebruiken van de bibliotheek at.js.

Er is een oplossing voor dit probleem gevonden voor versie 0.js van 22 mei 2017.

### Rapportage: Activiteiten in het kader van A/B en Experience Targeting (XT)

Tussen 27 april om 29.00 uur PST en 5 mei om 6:00 uur PST, A/B en XT activiteiten die met om het even welke metriek worden gecreeerd of worden uitgegeven gebruikend de &quot;Bekeken een actie van de Pagina&quot;omzetting (die niet op andere metriek gebaseerd waren), zouden verkeerd geregistreerde omzettingen kunnen hebben. Dit probleem is nu opgelost. de rapportage over de conversieactie &quot;Bekeken een pagina&quot; voor deze activiteiten tijdens de betrokken periode is echter wellicht niet correct en kan helaas niet worden gecorrigeerd. We raden u aan om voor beslissingen die zijn gebaseerd op conversieacties voor &quot;Bekeken een pagina&quot; voor deze activiteiten alleen te vertrouwen op gegevens die zijn vastgelegd voor of na de betreffende periode.

Rapportage van gegevens voor andere metriek kan nog steeds worden gebruikt omdat ze geen effect hadden.

Opgelost in de hotfix voor Target 17.4.3.

### Voorstellen: Activiteiten in het kader van A/B en Experience Targeting (XT)

De levering en voorvertoning werden beïnvloed voor aanbiedingen in A/B- en XT-activiteiten met ten minste twee ervaringen die zijn gemaakt of bewerkt met behulp van de Form-Based Experience Composer tussen vrijdag 28 april (28.00 uur PT) en maandag 1 mei (28.00 uur PT). Er zijn alleen voorstellen met standaardinhoud weergegeven.

Opgelost in de hotfix voor Target 17.4.3.

### at.js

De volgende acties veroorzaakten de aanbieding om niet te worden geleverd wanneer het gebruiken van Visual Experience Composer (VEC) en at.js: Verplaatsen en opnieuw rangschikken.

Er is een oplossing voor dit probleem gemaakt voor versie 0.js 0.9.6.

### Rapporten

De mogelijkheid om meerdere metrische gegevens in een rapport weer te geven, die zijn opgenomen in de Target 17.3.1-release (30 maart 2017), is verwijderd vanwege onverwacht gedrag. Deze functie is in een volgende release weer beschikbaar.

De mogelijkheid om meerdere metriek in een rapport weer te geven, is opgenomen in de Target 17.4.1-release (27 april 2017).

### Aanbiedingen

Afbeeldingen die zijn verwijderd uit de bibliotheek met afbeeldingsaanbiedingen ( \> Afbeeldingsaanbiedingen ) blijven zichtbaar in de gebruikersinterface. In een volgende versie worden deze verwijderde afbeeldingen niet meer weergegeven. Ondertussen worden verwijderde afbeeldingen weergegeven in de gebruikersinterface, maar hebben ze de status Verwijderd. (TGT-23793)

Opgelost in de Target 17.4.1-release (27 april 2017).

### Aanbiedingen omleiden

Voor recent bekeken criteria, op entiteit gebaseerde dynamische regels zullen tot geen aanbeveling leiden als de parameter entity.id niet in het mbox verzoek wordt overgegaan. (RECS-6241)

Dit probleem is opgelost na de release van Recommendations (22 maart 2018). Na de release van Recommendations slaat Target de op entiteit gebaseerde dynamische regels over als entity.id niet wordt doorgegeven in de mbox-aanvraag.

### at.js

Wanneer gebruikers proberen om te.js van de de detailpagina van Implementaties na het bijwerken van om.js montages te downloaden, mbox.js wordt gedownload in plaats van at.js. (TGT-23069)

Opgelost in de Target 17.3.1-release (30 maart 2017).

### Algemene uitsluitingsregels

De wereldwijde uitsluitingsregels duren 10 tot 20 minuten om zich aan de rand van Premium Recommendations te verspreiden. (RECS-5270)

Opgelost in de Recommendations 17.2.2.0-release (6 maart 2017).

### Rapportering Analytics for Target (A4T)

De rapporten worden niet bijgewerkt wanneer rapporteringsmetrisch wordt geschakeld. Dit is een UI-probleem. Er is geen invloed op het verzamelen of leveren van gegevens. (TGT-22970)

Opgelost in de Target 17.2.2.0-release (24 februari 2017).

### CSV-rapporten

Gedownloade rapporten voldoen niet aan de instelling Extreme Orders uitsluiten. (TGT-21871)

Opgelost in Target 17.2.1.0.
