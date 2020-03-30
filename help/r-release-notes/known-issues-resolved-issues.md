---
keywords: known issues;resolved issues;release notes;bugs;issues;fixes
description: Informatie over bekende problemen voor deze release van Adobe Target. Bevat ook informatie over problemen die zijn opgelost.
title: Bekende problemen en opgeloste problemen in Adobe Target
uuid: f8e8e057-1842-4922-ab7f-4d5441048573
translation-type: tm+mt
source-git-commit: 68a158b76db8d13f68c40385a227d44bac172b3e

---


# Bekende problemen en opgeloste problemen{#known-issues-and-resolved-issues}

Informatie over bekende problemen voor deze release van Target. Bevat ook informatie over problemen die zijn opgelost.

>[!NOTE]
>
>De nummer van de uitgave tussen haakjes is bedoeld voor intern gebruik door Adobe.

## Bekende problemen {#section_AEDC98B67CF24C9F8E0CF0D2EB9ACAEF}

In de volgende secties worden de bekende problemen voor [!DNL Target]:

### Paginalevering {#page-delivery}

Als u een sjabloonregel toevoegt, zoals de URL (/checkout, /cart) in [paginalevering](/help/c-activities/t-experience-target/t-xt-create/xt-activity-url.md), worden extra spaties aan uw regels toegevoegd. Dit is een cosmetische kwestie en heeft geen invloed op het creëren van publieksdefinities en het aanbieden van levering. (TGT-35916)

### Koppelingen voor QA-voorvertoningen voor activiteit {#preview}

[De QA-voorbeeldkoppelingen voor activiteit](/help/c-activities/c-activity-qa/activity-qa.md) voor opgeslagen activiteiten worden mogelijk niet geladen als uw account te veel opgeslagen activiteiten bevat. Het opnieuw proberen van de voorvertoningskoppelingen zou moeten werken. Als u wilt voorkomen dat dit gebeurt, archiveert u opgeslagen activiteiten die niet meer actief worden gebruikt. (TNT-32697)

### Aanbiedingen omleiden {#redirect}

Hier volgen bekende problemen met omleidingsvoorstellen:

* Onder sommige omstandigheden heeft een beperkt aantal klanten hogere mate van variatie in verkeersdistributie gemeld bij het gebruik van een omleidingsaanbod in activiteiten die zijn geconfigureerd met Analytics for Target (A4T). Adobe-technici werken momenteel aan dit probleem.
* De omleiding van activiteiten in implementaties at.js zou de voorproef URL kunnen veroorzaken om in een lijn in te gaan (de aanbieding wordt herhaaldelijk geleverd). In plaats daarvan kunt u de modus [](../c-activities/c-activity-qa/activity-qa.md#concept_9329EF33DE7D41CA9815C8115DBC4E40) QA gebruiken om de voorvertoning en QA uit te voeren. Deze kwestie heeft geen invloed op de daadwerkelijke levering van het aanbod. (TGT-23019)

### Grafiekrapport voor een activiteit Auto-Doel ontbreekt teruggeven wanneer het gebruiken van een douaneervaring als controle

Het grafiekrapport voor een activiteit auto-Doel ontbreekt om voor &quot;differentiële&quot;wijzen (Gemiddelde Lift en Dagelijkse Lift) terug te geven als er geen gegevens (0 bezoeken) in om het even welke ervaring zijn. Deze situatie kan zich voordoen tijdens de vroege fase van een activiteit als de controleervaring aan douane wordt geplaatst. Voor de andere wijzen (het Lopen Gemiddelde Controle en Gericht, Dagelijkse Controle en Gericht, en Bezoek) werkt het fijn. Zodra er gegevens zijn (bezoeken die niet gelijk zijn aan nul), wordt het rapport weergegeven zoals verwacht.

### Het laden van een pagina in de VEC annuleren {#cancel}

* Het volgende bekende probleem bestaat momenteel wanneer het annuleren van het laden van een [!UICONTROL A/B Test] of [!UICONTROL Ervaring gericht] (XT) activiteit binnen VEC die een omleiding URL bevat.

   In stap één van de driedelige geleide werkschema binnen VEC, wanneer u het laden van de pagina annuleert, wordt het paneel van [!UICONTROL Aanpassingen] in de vertoningen VEC en het omleiden aan malplaatje URL toegepast op de ervaring (bijvoorbeeld, &quot;Ervaring B). Wanneer u naar stap twee of drie gaat en vervolgens terugkeert naar stap één, doet zich de volgende situatie voor.

   Bij &quot;Experience B&quot; wordt standaard de sjabloon voor het laden van de geannuleerde website weergegeven en is het deelvenster [!UICONTROL Wijzigingen] toegankelijk, wat niet het geval moet zijn omdat er een omleiding naar de URL-sjabloon is toegepast. De omleiding naar URL-sjabloon moet worden weergegeven.

   Om de juiste stand van de ervaring in de VEC aan te tonen:

   Als u overschakelt naar een andere ervaring en vervolgens terugschakelt naar &quot;Experience B&quot;, wordt de omleiding naar de URL-sjabloon weergegeven die op deze ervaring is toegepast en is het deelvenster [!DNL Target] Wijzigingen  niet toegankelijk. (TGT-32138)

* Als u voor de websites van de toepassing Eén pagina (SPA) het laden annuleert, kunt u geen handelingen bewerken in het deelvenster [!UICONTROL Wijzigingen] .

### Ondersteuning voor Enterprise-machtigingen in doel-API&#39;s {#api}

Codeaanbiedingen die zijn gemaakt vanuit de doelinterface in de bibliotheek met aanbiedingen, worden mogelijk weergegeven in de standaardwerkruimte als de lijst met aanbiedingen wordt opgehaald met GET API&#39;s. Deze kwestie zal in de eerste week van maart 2019 worden geregeld. Nadat deze oplossing is ingesteld, worden de codeaanbiedingen in de juiste werkruimte weergegeven wanneer ze van API&#39;s worden gehaald. Dit probleem heeft *geen* invloed op aanbiedingen die met API&#39;s zijn gemaakt. Codeaanbiedingen die zijn gemaakt van API&#39;s worden bijvoorbeeld weergegeven in de werkruimte waarin ze zijn gemaakt, ongeacht of ze zijn opgehaald met GET API&#39;s of vanuit de doelinterface.

### Aanbevelingen

Hier volgen enkele bekende problemen met activiteiten in het kader van Aanbevelingen:

* Entiteiten zijn na 60 dagen na ontvangst van geen updates via feed of API correct verlopen. de verlopen entiteiten worden echter niet na het verlopen van de zoekindex van de catalogus verwijderd. (IRI-857)
* De &quot;Gebruiksinformatie&quot;-overlays voor Criteria en Ontwerpen weerspiegelen hun gebruik in A/B en de Ervaring gerichte activiteiten (TGT-34331) niet
* Aanbevelingen Aanbiedingen in A/B en Ervaring gerichte activiteiten tonen geen visuele voorvertoning van de bak met aanbevelingen (TGT-33426)
* Verzamelingen, uitsluitingen, criteria en ontwerpen die via de API zijn gemaakt, zijn niet zichtbaar in de doelgebruikersinterface en kunnen alleen via de API worden bewerkt. (TGT-35777)
* Activiteiten van aanbevelingen die via API zijn gemaakt, kunnen in de gebruikersinterface worden weergegeven, maar kunnen alleen via API worden bewerkt.
* De voedingsstatus van de aangepaste criteria die wordt weergegeven in de weergave Criteria (kaart), wordt elke tien minuten vernieuwd en kan in zeldzame gevallen meer dan tien minuten verouderd zijn. De status die wordt weergegeven in de bewerkingsweergave Aangepaste criteria wordt opgehaald in real-time en is altijd up-to-date. (TGT-35896, TGT-36173)

### MVT-activiteiten (Multivariate Test)

In een MVT-activiteit is de winnaar die in de tabel en grafiek wordt weergegeven, niet consistent bij het controleren van de meetwaarden. Dit komt voor als een gebruiker van Samenvatting aan de Mening van de Grafiek schakelt, dan terug naar Samenvattingsmening, metrisch verandert en dan aan de Mening van de Grafiek schakelt. Wanneer dit probleem optreedt, wordt in de overzichtsweergave altijd de juiste winnaar weergegeven. Als de gebruiker nooit schakelt tussen de overzichtsweergave, wordt in de grafiekweergave de juiste winnaar weergegeven.

### at.js {#atjs}

De volgende problemen zijn bekend met at.js:

* Als u versies van at.js gebruikt die ouder zijn dan 2.2.0, worden conversies niet gerapporteerd in Analytics for Target (A4T) als Adobe Analytics-code niet aanwezig is op pagina-elementen (zoals knoppen). In 0.js 2.2.0 is een oplossing voor dit probleem geïntroduceerd. [Voer een upgrade uit naar de nieuwste versie](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md) van .js als dit probleem optreedt.
* Als u een ervaring zonder wijzigingen maakt met behulp van at.js 2.1.1 of eerder (bijvoorbeeld een standaardeigenschap), wordt de ervaring mogelijk niet meegerekend in rapporten, Analytics voor Target (A4T), Adobe Analytics of Google Analytics. Bovendien werkt de [ttMeta-plug-in](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-target-atjs-implementation/target-atjs-plugins.md) mogelijk niet correct.

   Als oplossing gebruikt u een witruimte in de ervaringsinhoud. (TNT-33366)

   >[!NOTE]
   >
   >Een oplossing voor dit probleem is opgenomen in at.js 2.2.0. U zou aan de [recentste versie of at.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md) moeten bevorderen of de oplossing gebruiken bovengenoemde slechts voor at.js versies vroeger dan 2.2.0.

* Wanneer een pagina in Visuele Composer van de Ervaring (VEC) wordt geladen, moet het Doel bepalen als globale mbox het plaatsen wordt toegelaten of onbruikbaar gemaakt en of entiteitID of categoryID aanwezig is op de plaats waar de gebruiker probeert om de aanbeveling in VEC toe te passen. Op basis van deze informatie wordt de lijst met criteria gefilterd. De standaardlijst bevat gefilterde algoritmen, maar met het selectievakje [](/help/c-recommendations/t-create-recs-activity/algo-select-recs.md) Compatible kunt u de lijst met volledige algoritmen weergeven.

   Als u at.js gebruikt, is het selectievakje Compatibiliteit verborgen, zodat incompatibele algoritmen niet zichtbaar zijn.

   Deze kwestie is slechts op de activiteiten van Aanbevelingen van toepassing die VEC gebruiken.

   **Oplossing**: Schakel de optie Niet-compatibele criteria  filteren uit in [!UICONTROL Aanbevelingen > Instellingen]. Nadat u deze instelling hebt uitgeschakeld, worden alle (compatibele en niet-compatibele) criteria weergegeven in de kiezer voor criteria. (TGT-25949)

* Mboxen die niet worden geactiveerd in Microsoft Explorer 11-browsers na de upgrade naar at.js versie 1.0 vanwege de interactie tussen at.js en Visitor API 2.2.0. Dit probleem is van toepassing op versie 0.js 0.9.6 en hoger. (TNT-27600)
* at.js werkt mogelijk niet met Cordova/Hybrid-apps omdat cookies van de eerste partij momenteel niet in deze toepassingen worden ondersteund. (TNT-26166)

   **Oplossing**: Vorm at.js met de &quot;x-slechts&quot;toegelaten optie en ga `mboxThirdPartyId` in vraag over om gebruikers te beheren.

### mbox.js

De bibliotheek mbox.js ondersteunt geen sjabloontalen aan de clientzijde, zoals Handlebars en Mustache. De bibliotheek at.js *ondersteunt deze talen* niet.

**Opmerking**: De bibliotheek mbox.js wordt niet meer ontwikkeld. Alle klanten moeten van mbox.js naar at.js migreren. Zie [Migreren naar at.js vanuit mbox.js voor meer informatie](../c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-target-atjs-implementation/target-migrate-atjs.md#task_DE55DCE9AC2F49728395665DE1B1E6EA).

### Implementatie: Automatisch een globale box maken

Op het lusje van de Implementatie ([!UICONTROL Opstelling > Implementatie]) zal het [!UICONTROL Globale Auto creëren] gebied &quot;vals&quot;door gebrek voor een onlangs provisioned huurder zijn.

Wanneer mbox.js voor het eerst na levering wordt gedownload, wordt het [!UICONTROL Globale AutoCreate] gebied van Mbox geplaatst aan &quot;waar&quot;in het gedownloade mbox.js- dossier en in het [!DNL Target] achterste deel, maar het zal op de pagina van de [!UICONTROL Implementatie] in UI blijven tonen tot de pagina wordt verfrist (nadat de pagina wordt verfrist, zal de status &quot;waar&quot; zijn.)

at.js zal met `global_mbox_autocreate = false` voor een onlangs provisioned huurder worden gedownload. Als mbox.js eerst wordt gedownload, global\_mbox\_autocreate is set to &quot;waar&quot;en at.js zullen ook met `global_mbox_autocreate = true`. worden gedownload. (TGT-15929)

### Succeswaarden

De metriek van het succes met de geavanceerde optie &quot;hoe de telling&quot;zal worden verhoogd geplaatst aan &quot;elke indruk&quot;of &quot;elke indruk (met uitzondering van verfrissingen)&quot;kan niet als succes worden gebruikt metrisch dat een andere metrisch afhangt.

Wanneer een succes metrisch wordt geplaatst om op elke indruk worden verhoogd, telt Target opnieuw de bezoeker telkens als de bezoeker dit succes metrisch bezoekt. Het doel stelt dan het succes metrische &quot;lidmaatschap&quot;aan 0 terug zodat kan het op de volgende indruk opnieuw tellen. Aldus, als een andere metrisch vereist dat metrisch eerst is gezien, zal het Doel nooit erkennen dat de gebruiker eerste metrisch heeft gezien.

### Analyses voor doel (A4T)

Impressies en conversies van doelactiviteiten worden momenteel onjuist geteld in de analysewerkruimte.

Als oplossing kunt u gebruikmaken van A4T-gegevens in rapporten en analyses totdat dit probleem is opgelost.

### Doel-API&#39;s

Klanten kunnen geen CRUD-bewerkingen uitvoeren op activiteiten voor automatisch toewijzen via de v3-versie van de API voor A/B-activiteiten op Adobe I/O.

## Opgeloste problemen {#section_FD2FC86E7C734D60B1EDC9DEF60E1014}

Aangezien de bekende problemen hierboven zijn opgelost, worden ze verplaatst naar de volgende secties en worden zo nodig aanvullende opmerkingen toegevoegd.

### Aanbevelingen

* De de voederindex van aanbevelingen kan &quot;die op index wachten&quot;tonen als de punten in het voer het zelfde als in de vorige looppas zijn. De inname van het product voor levering heeft geen invloed op het product. (RECS-6663)

   Dit probleem is opgelost in de doelversie 19.4.2.

* Het verwerken van aanbevolen feeds duurt langer dan u had verwacht. (COR-2836)

   Correctie in de doelversie 16.10.1.

* De interface van de Beelden van de Aanbeveling toont niet het correcte statuut van indexeren. De back-endtaken werken correct, maar de interface kan de huidige status niet ophalen en weergeven.

   Dit probleem is opgelost in de release 17.10.1.

### Aanbiedingen omleiden

Een zeldzame omstandigheid op uw pagina kan ertoe leiden dat paginaweergaven op de oorspronkelijke pagina en op de pagina voor omleiding worden geteld. De implementatie van at.js zal worden bijgewerkt om ervoor te zorgen dat deze rasvoorwaarde kan worden vermeden.

Dit probleem is opgelost in 1.js 1.6.3.

### Uitsluitingsgroepen

* Wanneer auto-dedupe na het creëren van uitsluitingsgroepen wordt toegepast, zou de telling op het activiteitendiagram in UI onjuist kunnen zijn.
* Wanneer bestaande activiteit met de Groep van de Uitsluiting wordt uitgegeven, zouden de handopneming niet correct in UI kunnen worden weerspiegeld.

Deze problemen zijn opgelost.

### Doel-API&#39;s

v1-versie van de API&#39;s voor aanbiedingen op Adobe I/O behandelt alle aanbiedingen die via Target zijn gemaakt, in de standaardwerkruimte. (TTTEAM-41957)

Dit probleem is opgelost.

### at.js

Mboxen die niet worden geactiveerd in Microsoft Explorer 11-browsers na de upgrade naar at.js versie 1.0 vanwege de interactie tussen at.js en Visitor API 2.2.0. Dit probleem is van toepassing op versie 0.js 0.9.6 en hoger. (TNT-27600)

Opgelost met de release van API 2.3.0 of hoger.

### Geo targeting

Het zoeken naar een tekenreeks die speciale tekens bevat (zoals een spatie of komma) werkt momenteel niet wanneer u doelgroepen maakt. Dit probleem doet zich bijvoorbeeld voor bij het creëren van publiek op basis van steden, staten, landen, enz. Wanneer u bijvoorbeeld zoekt naar &quot;new york&quot;, retourneert de zoekopdracht geen geldige resultaten.

Vast in november 2018.

### at.js

Wanneer u at.js versie 1.6.0 gebruikt, vindt een omleiding van Analytics voor Target (A4T) plaats, maar zonder activiteitkwalificatie.

Correctie met de release van at.js 1.6.2.

### Activiteiten, werkruimten en activiteit-API verwijderen

De activiteiten in de standaardwerkruimte die via API worden verwijderd, worden nog steeds weergegeven in de doelinterface. Als tussenoplossing, schrap alle activiteiten in de standaardwerkruimte gebruikend het Doel UI. (TGT-31315)

Vast 25 oktober 2018

### Geautomatiseerde Personalisatie (AP) aanbieding-vlakke rapportering

Wanneer u de gerichte ervaring in een Geautomatiseerd rapport van de Personalisatieactiviteit (AP) klikt om aanbieding-vlakke rapportering te bekijken, momenteel ziet u lege resultaten, een foutenmelding, of een het draaien pictogram. (TNT-30695)

Vast op 27 september 2018.

### Code-editor

Als u VEC op stap 1 van de driestapige geleide werkstroom opnieuw laadt terwijl het werken met de Redacteur van de Code in Firefox en Internet Explorer, geeft het lusje van Wijzigingen niet behoorlijk terug; de functionaliteit van VEC wordt echter niet beïnvloed. (TGT-28730)

Dit probleem is opgelost in de release 18.9.1.

### De activiteit van aanbevelingen die een regel van de Bevordering van Attributen gebruikt

Wanneer u een activiteit van Aanbevelingen uitgeeft of kopieert die een regel van de Bevordering van Attributen gebruikt, toont de &quot;Heeft ontbrekend gebied&quot;fout wanneer het klikken sparen.

Dit probleem is opgelost in de release 17.8.1.

### Back-upaanbevelingen

Back-upaanbevelingen geven ten onrechte &quot;Ingeschakeld&quot; weer op recent bekeken itemkaarten in de interface van het doel. (TGT-29308)

Dit probleem is opgelost in de release 18.4.1, zodat &quot;Uitgeschakeld&quot; wordt weergegeven.

### Auto-Target activiteiten en rapportagepubliek

Wanneer de naam van een rapportpubliek in een auto-Doel activiteit wordt gebruikt wordt veranderd, zouden de verdere updates van Doel voor die activiteit met een foutenmelding kunnen ontbreken.

Dit probleem is opgelost met de Target 18.5.1-release (22 mei 2018).

### at.js

Het algoritme voor het extraheren van het domein op hoofdniveau dat moet worden gebruikt bij het opslaan van cookies is gewijzigd in versie 0.js 0.9.6. Vanwege deze wijziging kunnen cookies niet worden opgeslagen naar adressen die IP gebruiken. Meestal worden IP-adressen gebruikt voor testdoeleinden, maar als tijdelijke oplossingen kunt u DNS-vermeldingen gebruiken, het hostbestand op een lokaal vak aanpassen of de functie targetGlobalSettings() at.js gebruiken om een codefragment in te voegen ter ondersteuning van IP-adressen.

Dit probleem is opgelost in at.js versie 1.2.

### Gebruikersmachtigingen voor doelversie

Als onderdeel van de migratie naar Enterprise-machtigingen is al het gebruikersbeheer voor Target Premium verplaatst van de gebruikersinterface van Adobe Target naar Adobe Admin Console.

Als gevolg van de migratie zijn er twee mogelijke problemen die u dient te kennen:

* Gebruikers die geen beheerder zijn, hebben een e-mail ontvangen met de melding dat ze nu toegang hebben tot Adobe Target. Dit wijst erop dat de migratie voor uw organisatie werd voltooid. De e-mail zelf kan buiten beschouwing worden gelaten.
* Na de migratie zijn er enkele meldingen geweest dat eerder uitgeschakelde gebruikers opnieuw werden weergegeven in de Adobe Admin Console. Dit kan een probleem voor uw organisatie zijn als uitgeschakelde gebruikers in de Adobe Admin Console vóór de migratie nog steeds op uw gebruikerslijst in Target staan. We raden beheerders aan de lijst met gebruikers in de beheerconsole te controleren om de toegang te valideren.

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

De eerste kwestie is vastgelegd in de Target 17.3.1-release (maart 2017).

De tweede kwestie is vastgelegd in de Target 17.6.1-release (juni 2017).

### at.js

Sinds de versie van Doel 17.4.1 (27 april, 2017), die de actie van het Beeld van het Tussenvoegsel in Visuele Composer van de Ervaring (VEC) gebruikt veroorzaakt dat de aanbiedingsinhoud niet wordt geleverd wanneer het gebruiken van de bibliotheek at.js.

Er is een oplossing voor dit probleem gevonden voor versie 0.js van 22 mei 2017.

### Rapportage: Activiteiten in het kader van A/B en Experience Targeting (XT)

Tussen 27 april om 29.00 uur PST en 5 mei om 6:00 uur PST, A/B en XT activiteiten die met om het even welke metriek worden gecreeerd of worden uitgegeven gebruikend de &quot;Bekeken een actie van de Pagina&quot;omzetting (die niet op andere metriek gebaseerd waren), zouden verkeerd geregistreerde omzettingen kunnen hebben. Dit probleem is nu opgelost. de rapportage over de conversieactie &quot;Bekeken een pagina&quot; voor deze activiteiten tijdens de betrokken periode is echter wellicht niet correct en kan helaas niet worden gecorrigeerd. We raden u aan om voor beslissingen die zijn gebaseerd op conversieacties voor &quot;Bekeken een pagina&quot; voor deze activiteiten alleen te vertrouwen op gegevens die zijn vastgelegd voor of na de betreffende periode.

Rapportage van gegevens voor andere metriek kan nog steeds worden gebruikt omdat ze geen effect hadden.

Opgelost in de hotfix Doel 17.4.3.

### Voorstellen: Activiteiten in het kader van A/B en Experience Targeting (XT)

De levering en voorvertoning werden beïnvloed voor aanbiedingen in A/B- en XT-activiteiten met ten minste twee ervaringen die zijn gemaakt of bewerkt met behulp van de Form-Based Experience Composer tussen vrijdag 28 april (28.00 uur PT) en maandag 1 mei (28.00 uur PT). Er zijn alleen voorstellen met standaardinhoud weergegeven.

Opgelost in de hotfix Doel 17.4.3.

### at.js

De volgende acties veroorzaakten de aanbieding om niet te worden geleverd wanneer het gebruiken van Visual Experience Composer (VEC) en at.js: Verplaatsen en opnieuw rangschikken.

Er is een oplossing voor dit probleem gemaakt voor versie 0.js 0.9.6.

### Rapporten

De capaciteit om veelvoudige metriek in een rapport te bekijken, inbegrepen in Doelversie 17.3.1 (30 maart, 2017) is verwijderd toe te schrijven aan onverwacht gedrag. Deze functie is in een volgende release weer beschikbaar.

De capaciteit om veelvoudige metriek in een rapport te bekijken was inbegrepen in Doelversie 17.4.1 (27 april 2017).

### Aanbiedingen

Afbeeldingen die zijn verwijderd uit de bibliotheek met afbeeldingsaanbiedingen ( \> Afbeeldingsaanbiedingen ) blijven zichtbaar in de gebruikersinterface. In een volgende versie worden deze verwijderde afbeeldingen niet meer weergegeven. Ondertussen worden verwijderde afbeeldingen weergegeven in de gebruikersinterface, maar hebben ze de status Verwijderd. (TGT-23793)

Opgelost in de doelversie 17.4.1 (27 april 2017).

### Aanbiedingen omleiden

Voor recent bekeken criteria, op entiteit gebaseerde dynamische regels zullen tot geen aanbeveling leiden als de parameter entity.id niet in het mbox verzoek wordt overgegaan. (RECS-6241)

Dit probleem is opgelost na de mededeling met aanbevelingen (22 maart 2018). Na de versie van Aanbevelingen, slaat Doel de op entiteit-gebaseerde dynamische regels over als entity.id niet in het mbox verzoek wordt overgegaan.

### at.js

Wanneer gebruikers proberen om te.js van de de detailpagina van Implementaties na het bijwerken van om.js montages te downloaden, mbox.js wordt gedownload in plaats van at.js. (TGT-23069)

Vast in de Target 17.3.1-release (30 maart 2017).

### Algemene uitsluitingsregels

De wereldwijde uitsluitingsregels duren 10 tot 20 minuten voordat ze aan de rand van de Premium-aanbevelingen worden doorgegeven. (RECS-5270)

Vast in de Aanbeveling 17.2.2.0 release (6 maart 2017).

### Analyses voor doelrapportage (A4T)

De rapporten worden niet bijgewerkt wanneer rapporteringsmetrisch wordt geschakeld. Dit is een UI-probleem. Er is geen invloed op het verzamelen of leveren van gegevens. (TGT-22970)

Vast in de Target 17.2.2.0-release (24 februari 2017).

### CSV-rapporten

Gedownloade rapporten voldoen niet aan de instelling Extreme Orders uitsluiten. (TGT-21871)

Correctie in de doelversie 17.2.1.0.
