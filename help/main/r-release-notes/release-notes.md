---
keywords: releaseopmerkingen;nieuwe functies;releases;updates;update;release;verbetering;verbeteringen;correcties;foutoplossingen;updates;huidige updates
description: Leer over de nieuwe eigenschappen, de verhogingen, en de moeilijke situaties inbegrepen in de huidige versie van  [!DNL Adobe Target], met inbegrip van SDKs, APIs, en de bibliotheken van JavaScript.
landing-page-description: Leer over de nieuwe eigenschappen, de verhogingen, en de moeilijke situaties inbegrepen in de huidige versie van  [!DNL Adobe Target].
short-description: Leer over de nieuwe eigenschappen, de verhogingen, en de moeilijke situaties inbegrepen in de huidige versie van  [!DNL Target].
title: Wat is inbegrepen in de huidige Versie?
feature: Release Notes
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
source-git-commit: 405faeac7fc633a64c441edeb2a95d90d896b21d
workflow-type: tm+mt
source-wordcount: '5412'
ht-degree: 0%

---

# [!DNL Target] releaseopmerkingen (huidig)

Ontdek de nieuwste functies, verbeteringen en oplossingen in [!DNL Adobe Target] . Deze releaseopmerkingen hebben ook betrekking op updates van [!DNL Target] API&#39;s, SDK&#39;s, de [!DNL Adobe Experience Platform Web SDK] , at.js en andere platformcomponenten, indien van toepassing.

(De uitgiftenummers tussen haakjes zijn bedoeld voor intern gebruik door [!DNL Adobe] .)

## Tijdgevoelige updates die u moet weten {#time-sensitive}

[!BADGE &#x200B; Belangrijk &#x200B;]{type=Informative}

Voor tijdgevoelige updates met betrekking tot [!DNL Adobe Target] en uw implementatie, [!DNL Adobe] verstrekt gedetailleerde versienota&#39;s en documentatie door [!UICONTROL Experience League]. Hier volgen enkele belangrijke punten die relevant zijn voor uw implementatie:

### Veroudering van interfaceversie [!DNL Target] in-/uitschakelen

+++Zie details
Het team van [!DNL Target] biedt een tijdelijke functie waarmee u met een schakelknop kunt schakelen tussen de bijgewerkte [!DNL Target] -gebruikersinterface en de oudere versie. Deze optie is beschikbaar slechts tijdens de definitieve fase van de rollout UI.

![ de versiesknevel van het Doel UI ](/help/main/r-release-notes/assets/toggle.png)

Zodra de rollout volledig is, zal de knevel worden verwijderd, en alle gebruikers overgang permanent aan bijgewerkte UI. [!DNL Adobe] raadt u aan vooruit te plannen, aangezien deze functie binnenkort wordt uitgeschakeld.

#### Tijdlijn van verdringing

Vanwege recente problemen die zijn vastgesteld, voornamelijk in verband met complexe klantaanpassingen, heeft het team van [!DNL Target] de tijdlijn voor de afschrijving aangepast:

* **17 Juni, 2025**: Alle organisaties IMS zijn toegelaten voor bijgewerkte [!DNL Target] UI, of voor specifieke gebruikers of organisatie-breed, beginnen het testen van de nieuwe ervaring.

* **Juni 30, 2025**: [ bijgewerkte  [!DNL Target]  UI ](/help/main/c-intro/understand-the-target-ui.md) werd de standaardervaring voor alle IMS Orgs die de UI versieknevel hebben toegelaten.

   * Klanten die momenteel de oudere UI zien, door gebrek, zien nu bijgewerkte UI bij login.
   * De UI versiesknevel blijft beschikbaar door eind Juli, die gebruikers toestaat om terug te schakelen indien nodig.

  >[!IMPORTANT]
  >
  > [!DNL Adobe] raadt u ten zeerste aan de bijgewerkte gebruikersinterface van [!DNL Target] te gebruiken. De schakelaar terug naar erfenis UI slechts als een blokkeerkwestie voorkomt, toe te schrijven aan [ beperkingen van het knevel schakelaargedrag ](#limitations).

* **15 juli tot 30 juli, 2025**: De de versiesknevel van UI zal permanent in fasen onbruikbaar worden gemaakt. Betrokken IMS-instellingen kunnen niet meer terugkeren naar de oudere gebruikersinterface.

   * Uitzonderingen worden per geval beoordeeld.
   * Vertragingen bij de tijdelijke verwijdering van de knevel worden slechts kort toegestaan (een paar dagen), terwijl problemen met blokkeringen worden opgelost.

De Zorg van de Klant van Adobe van het contact [ met om het even welke zorgen of als u kwesties tijdens deze overgang verwacht.](/help/main/cmp-resources-and-contact-information.md#/help/main/cmp-resources-and-contact-information.md)

#### Beperkingen van het gedrag van de UI-schakelfunctie {#limitations}

De volgende informatie beschrijft de beperkingen die u bewust zou moeten zijn wanneer het kiezen om de versiesknevel te gebruiken:

* **Zichtbaarheid van nieuwe activiteiten**: De activiteiten die in bijgewerkte UI worden gecreeerd zullen niet zichtbaar zijn als u terug naar erfenisUI schakelt.
* **het uitgeven van bestaande activiteiten**: De veranderingen die aan bestaande activiteiten (oorspronkelijk in erfenis UI) worden aangebracht terwijl het gebruiken van bijgewerkte UI worden gepubliceerd aan uw website. Nochtans, zijn deze updates niet zichtbaar in erfenis UI als u terug schakelt; slechts de laatste die updates van erfenisUI worden gemaakt verschijnen daar.
* **Consistentie van activiteitendetails**: De meest recente veranderingen, ongeacht welke UI u gebruikt, worden weerspiegeld op uw levende website. In de oudere gebruikersinterface worden echter alleen de meest recente wijzigingen weergegeven die in die versie zijn aangebracht. Deze situatie zou verwarring kunnen veroorzaken als de activiteiten die in bijgewerkte UI worden uitgegeven verschillend kijken dan wat u in erfenisUI ziet.

#### Meer bronnen voor meer informatie over de bijgewerkte gebruikersinterface

* [[!DNL Target]  UI update FAQs ](/help/main/c-intro/updated-ui-faq.md): Deze veelgestelde vragen behandelt gemeenschappelijke vragen over nieuwe [!DNL Target] UI en [!UICONTROL Visual Experience Composer] (VEC), met inbegrip van navigatieveranderingen, eigenschapplaatsen, en de veroudering van de tijdelijke UI versiesknevel. Of u nu een markeerteken, ontwikkelaar of beheerder bent, deze veelgestelde vragen helpen u een vloeiende overgang te maken en de bijgewerkte gebruikersinterface optimaal te benutten.
* [[!DNL Target Standard/Premium]  25.2.1 (17 februari, 2025) versienota&#39;s ](/help/main/r-release-notes/release-notes-for-previous-releases.md#ui-update-2): Verstrekt een samenvatting van de belangrijkste veranderingen UI in [!DNL Target] voor [!UICONTROL Activities], [!UICONTROL Recommendations], en [!UICONTROL Visual Experience Composer] (VEC).
* [[!DNL Target Standard/Premium]  25.1.1 (9 Januari, 2025) versienota&#39;s ](/help/main/r-release-notes/release-notes-for-previous-releases.md#ui-update-1): Verstrekt een samenvatting van de belangrijkste veranderingen UI in [!DNL Target] voor [!UICONTROL Offers Library].
* [ begrijp  [!DNL Target]  UI ](/help/main/c-intro/understand-the-target-ui.md): Verstrekt een kort overzicht om u te helpen vertrouwd worden met [!DNL Target] en verleent verbindingen voor meer diepgaande informatie en geleidelijke instructies.
* [[!UICONTROL Visual Experience Composer] changes ](/help/main/c-experiences/c-visual-experience-composer/vec-changes.md) : In de release [!DNL Adobe Target Standard/Premium] 25.2.1 (17 februari 2015) wordt een bijgewerkte versie van [!UICONTROL Visual Experience Composer] (VEC) geïntroduceerd. Dit artikel verklaart de verschillen tussen de erfenis en bijgewerkte versies van VEC.
* [[!UICONTROL Visual Experience Composer] opties ](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md): Dit artikel verklaart bijgewerkte UI VEC en zijn opties.

+++

## [!DNL Target Standard/Premium] 25.9.3 (30 september 2025)

Deze versie bevat de volgende verbeteringen en oplossingen.

+++[!UICONTROL Audiences]

* **de uitsluitingsregels van het publiek werden verkeerd getoond als opneming in [!DNL Target] UI.** Met uitsluitingsregels geconfigureerde soorten publiek werden als onderdeel van de bewerking voor het maken van doelen in een activiteit weergegeven. Hoewel de uitsluitingslogica correct werd toegepast tijdens uitvoering, slaagde UI er niet in de regel correct te weerspiegelen, die het &quot;exclusief&quot;etiket weglaat. In de gebruikersinterface van [!DNL Target] worden nu correct uitsluitingsregels weergegeven in zowel publieksconfiguratie als doelworkflows, zodat duidelijke en consistente instellingen voor de campagne mogelijk zijn. (TGT-53808)
* **de [!UICONTROL Targeting] sectie gaf niet aan dat een publieksregel werd geplaatst om uit te sluiten.** Met uitsluitingslogica geconfigureerde soorten publiek werden onjuist weergegeven als onderdeel van de sectie [!UICONTROL Targeting] van de interface voor het maken van activiteiten. Hoewel de backend correct de uitsluitingsregel toepaste, slaagde UI er niet in om het visueel te vertegenwoordigen, die het etiket &quot;uitsluiten&quot;weglaten en verwarring tijdens campagneopstelling veroorzaken. In de sectie [!UICONTROL Targeting] worden nu duidelijk uitsluitingsregels weergegeven, zodat de configuratie van de doelgroep consistent is en de visualisatie wordt afgestemd. (TGT-53809)

+++

+++Lokalisatie

* **Vaste een terminologische inconsistentie in de Vereenvoudigde Chinese vertaling van &quot;Volledige detailmening.&quot;**
Eerder werd de term &quot;Details&quot; onjuist vertaald als &quot;详 情&quot; in de landinstelling Vereenvoudigd Chinees (zh_CN), wat in strijd is met de gevestigde terminologierichtlijnen. Dit is gecorrigeerd naar &quot;详 细 信 息&quot; om consistentie met de termbase te waarborgen. (TGT-53741)

+++

+++[!UICONTROL Recommendations]

* **de dozen van de Aanbeveling waren moeilijk om van en in VEC de plaats te bepalen.** Na het toevoegen van een adviesaanbieding in (VEC), klikte het klikken van de wijziging in het linkerpaneel niet of scrolde aan het overeenkomstige aanbevelingsvakje op de pagina. Hierdoor was het moeilijk om het aanbod te vinden en te bewerken, vooral als het onder kiezers is verborgen of minimaal is vormgegeven. Als u op een aanbevolen wijziging klikt, wordt het bijbehorende element gemarkeerd en naar het bijbehorende element geschoven. Hierdoor wordt de bruikbaarheid verbeterd en wordt de efficiëntie van het bijgewerkte proces voor het maken van activiteiten verbeterd. (TGT-52571)
* **de selecteurs van de Aanbeveling werden verkeerd herschreven na het bewaren van een activiteit.** Wanneer het toevoegen van een aanbeveling aan een element in VEC, was selecteur aanvankelijk correct, maar na het bewaren van en het heropenen van de activiteit, veranderde het in een generische selecteur. Pogingen om de oorspronkelijke kiezer handmatig te herstellen, resulteerden in validatiefouten. De selecteurs van de aanbeveling blijven nu nauwkeurig na sparen, die betrouwbare het richten en editability in het bijgewerkte activiteit-creeert proces verzekeren. (TGT-53709)
* **de inhoud van Criteria kon niet worden uitgegeven wanneer het wijzigen van een bestaande activiteit.** Tijdens het bewerken van een activiteit werd de sectie [!UICONTROL Criteria] -inhoud uitgeschakeld. De knoppen werden grijs weergegeven en reageren niet. Dit probleem is opgelost door ervoor te zorgen dat configuraties van [!UICONTROL Criteria] volledig bewerkbaar zijn tijdens het bijwerken van activiteiten. Klanten kunnen nu [!UICONTROL Criteria] -inhoud wijzigen zonder dat ze hoeven over te schakelen op andere selecties of tijdelijke oplossingen te gebruiken, waardoor ze flexibeler en bruikbaarder worden in het bijgewerkte activity-create proces. (TGT-53812)
* **de Criteria konden niet binnen een activiteit worden uitgegeven.** De opties [!UICONTROL Edit Criteria] en [!UICONTROL Remove Criteria] zijn uitgeschakeld wanneer u criteria benadert vanuit een activiteit. Dezelfde criteria kunnen echter wel met succes worden bewerkt via het tabblad [!UICONTROL Recommendations] . De criteria kunnen nu volledig worden bewerkt, zowel vanuit de workflow voor bewerken van activiteiten als vanuit het tabblad [!UICONTROL Recommendations] . Hierdoor wordt een consistente en efficiënte bewerkingservaring gegarandeerd. (TGT-53814)

+++

+++[!UICONTROL Reports]

* **producerend ad-hoc aanbiedingen in A [!UICONTROL utomated Personalization] activiteiten veroorzaakte rapporteringsinconsistenties.** Het gebruik van de functie Ad-hocaanbiedingen genereren in [!UICONTROL Automated Personalization] -activiteiten (AP) leidde tot onjuiste rapportage. De aanbod-id&#39;s zijn hergebruikt op verschillende locaties, waardoor rapportgegevens onjuist zijn toegewezen of worden overschreven. Ad-hoc aanbiedingen produceren nu met verschillende herkenningstekens per plaats, die nauwkeurige het volgen en het melden over alle gevormde ervaringen verzekeren. (TGT-53757)
* **de rapporten van de Activiteit slaagden er niet in toe te schrijven aan een fout van JavaScript.** Klanten kregen een melding &quot;Er is iets fout gegaan&quot; tijdens het openen van het tabblad [!UICONTROL Reports] voor bepaalde activiteiten. De fout is veroorzaakt door een JavaScript-uitzondering: kan geen eigenschappen lezen van undefined (lezen &#39;indexOf&#39;), die worden geactiveerd tijdens de `getAnalyticsReportSummary` GraphQL-aanroep. Rapporten worden nu correct geladen en foutafhandeling is verbeterd om vergelijkbare fouten in de bijgewerkte workflow voor het maken van activiteiten te voorkomen. (TGT-53797)
* **de Rapporten crashten na het in wisselwerking staan met scrollbar.** Wanneer u op de schuifbalk op het tabblad [!UICONTROL Reports] klikt, loopt de pagina vast, samen met een JavaScript-fout:
  `SyntaxError: Failed to execute 'querySelector' on 'Element': '[data-key="a-currentcopy"hiretalent""]' is not a valid selector.` Rapporten worden nu correct geladen en geschoven zonder fouten of vastlopen te veroorzaken. (TGT-53828)
* **de rapporten gaven niet primaire metrisch.** Primaire metrische waarde, die als omzettingsmetrisch gebruikend mbox wordt gevormd ontbrak in de activiteitenrapporten. Als u naar de naam van de metrische waarde of de box zoekt, heeft dit geen resultaat opgeleverd, zodat belangrijke prestatiegegevens niet zichtbaar zijn. De primaire meetgegevens worden nu correct weergegeven op het tabblad [!UICONTROL Reports] , zodat u de prestaties van de campagne nauwkeurig kunt bijhouden en analyseren. (TGT-53773)
* **het [!UICONTROL Reports] lusje in bijgewerkte UI crashte wanneer het in wisselwerking staan met de horizontale rolbar.** De weergave van [!UICONTROL Reports] is periodiek vastgelopen met de fout &quot;Er is iets misgegaan&quot; wanneer de horizontale schuifbalk wordt gebruikt om metrische gegevens weer te geven als deze niet zichtbaar zijn. De schuifbalk werkt nu betrouwbaar, zodat klanten alle metriek kunnen bekijken en analyseren zonder dat er werkgrenzen nodig zijn, zoals uitzoomen of Shift-scroll. (TGT-53824)

+++

+++[!UICONTROL Visual Experience Composer] (VEC)

* **klikkende broodkruimels in VEC niet constant tonen uitgeeft menu.**
Als u HTML-elementen selecteert via de breadcrumbs in VEC (breadcrumbs), wordt het bewerkingsmenu soms niet weergegeven of verdwijnt het snel, waardoor de selectie van elementen onbetrouwbaar wordt. Het bewerkingsmenu wordt nu consistent weergegeven wanneer u navigeert via broodkruimels, waardoor de workflow voor het selecteren van elementen in het bijgewerkte activity-create proces wordt verbeterd. (TGT-52873)
* **het contextmenu is periodiek er niet in geslaagd om in VEC te verschijnen.** Het contextmenu in de bijgewerkte VEC-gebruikersinterface werd niet altijd weergegeven wanneer u op elementen klikte, waardoor het moeilijk was om bewerkingsopties te openen. Het contextmenu wordt nu betrouwbaar weergegeven op basis van de selectie van elementen, waardoor de bewerkingsworkflow en de algemene bruikbaarheid in het bijgewerkte activity-create proces worden verbeterd. (TGT-53015)
* **het contextmenu slaagde er niet in om voor bepaalde elementen in VEC te verschijnen.** Het contextmenu werd niet weergegeven wanneer u specifieke elementen in de bijgewerkte VEC selecteerde, waardoor het moeilijk was om wijzigingen toe te passen. Het contextmenu wordt nu consistent weergegeven voor alle ondersteunde elementen, waardoor de betrouwbaarheid en bruikbaarheid van de bewerkervaring in de bijgewerkte workflow voor het maken van activiteiten worden verbeterd. (TGT-53248)
* **het menu van de Context verdween op de eerste klik wanneer het gebruiken van broodkruimels in VEC.** Door een bovenliggend element via de broodkruimels in VEC te selecteren, werd het contextmenu kort weergegeven en verdwenen het, waardoor het moeilijk werd om bewerkingsopties te openen. Het contextmenu blijft nu zichtbaar en functioneel wanneer u door elementen door broodkruimels navigeert, wat de betrouwbaarheid van de workflow voor elementselectie in het bijgewerkte activity-create proces verbetert. (TGT-53424)
* **het contextmenu verscheen niet voor top-level elementen in VEC.** Het selecteren van elementen op hoofdniveau, zoals `<div>` - of `<main>` -tags, via de breadcrumbs in de VEC heeft het contextmenu niet geactiveerd, waardoor verdere bewerkhandelingen niet mogelijk zijn. Het contextmenu wordt nu consistent weergegeven voor alle ondersteunde elementen, inclusief containers op hoofdniveau, waardoor de workflow voor het maken van activiteiten flexibeler en gebruiksvriendelijker wordt. (TGT-53770)
* **Elementen op een specifieke pagina waren niet editable in VEC.** Bepaalde elementen op de pagina kunnen niet worden geselecteerd of bewerkt in de bijgewerkte VEC. Deze uitgave is geïsoleerd voor die pagina en heeft geen invloed op andere pagina&#39;s binnen dezelfde account. Alle elementen op de pagina zijn nu selecteerbaar en bewerkbaar zoals u had verwacht, zodat de volledige functionaliteit van de workflow voor het maken van activiteiten wordt hersteld. (TGT-53353)
* **verbeterde het werkschema wanneer het bekijken van kindelementen tijdens elementenselectie in VEC.** Om de bruikbaarheid en nauwkeurigheid tijdens het maken van activiteiten te verbeteren, geeft de VEC nu onderliggende elementen weer wanneer u de muisaanwijzer op een bovenliggend HTML-element plaatst of dit selecteert. Dankzij deze verbetering kunnen klanten de structuur van de pagina beter begrijpen en nauwkeurigere wijzigingen aanbrengen, waardoor de bewerkingsworkflow in de bijgewerkte gebruikersinterface wordt gestroomlijnd. (TGT-53416)
* **Elementen in bestaande activiteiten konden niet worden uitgegeven gebruikend de wijzigingsbar.** Tijdens het bewerken van eerder gemaakte activiteiten kon de wijzigingsbalk niet worden geactiveerd voor bepaalde elementen op de pagina, waardoor updates werden voorkomen. Dit probleem werd voornamelijk in gewijzigde activiteiten waargenomen en was moeilijk te reproduceren in nieuw opgerichte activiteiten. De wijzigingsbalk geeft nu consistent alle ondersteunde elementen weer en staat het bewerken toe, waardoor de betrouwbaarheid en bruikbaarheid in de bijgewerkte workflow voor het maken van activiteiten worden verbeterd. (TGT-53013)

+++

+++[!UICONTROL Workspaces]

* **het Klonen van een activiteit aan een verschillende werkruimte teweegbracht een &quot;Ongeldige fout van de Input van de Gebruiker&quot;teweeg.** Als u een activiteit probeert te klonen van de ene werkruimte naar de andere, is er een fout opgetreden: &quot;InvalidProperty.Json - Unrecognized property name &#39;content&#39;. Dit probleem is veroorzaakt door een onjuiste verwerking van metagegevens over activiteiten tijdens het klonen. De activiteiten kunnen nu met succes over werkruimten worden gekloond zonder bevestigingsfouten teweeg te brengen, die vlottere werkschema&#39;s van de activiteitenplaatsing verzekeren. (TGT-53731 &amp; TGT-53736)

+++

## [!DNL Target Standard/Premium] 25.9.2 (22 september 2025)

Deze release bevat de volgende correcties en verbeteringen:

**[!UICONTROL Audiences]**

+++Zie details
* **Vaste een kwestie waar de activiteiten niet wegens ongeldige publiek IDs konden worden gekopieerd.** Klanten die activiteiten in het bijgewerkte activity-create proces proberen te kopiëren, hebben een fout aangetroffen die wordt veroorzaakt door ongeldige gebruikers-id&#39;s (bijvoorbeeld -1752722444307). Door dit probleem van backend-validatie zijn dubbele activiteiten binnen dezelfde werkruimte voorkomen. Dit probleem is opgelost en activiteiten kunnen nu met succes worden gekopieerd zonder publieksfouten. (TGT-53717)
* **verholpen een kwestie waar de ongeldige fouten van de gebruikersinput voor activiteit-slechts publiek in [!UICONTROL Automated Personalization] activiteiten [!UICONTROL Manage Content] modaal verschenen.** Klanten ondervonden ongeldige fouten bij gebruikersinvoer tijdens het configureren van alleen-activiteit publiek in het modaal [!UICONTROL &#x200B; Manage Content] voor AP-activiteiten. Dit probleem is opgetreden ondanks het feit dat het publiek voorheen correct werd gebruikt. Gecombineerde publieksconfiguraties besparen nu correct zonder validatiefouten te veroorzaken. (TGT-53749)

+++

**Documentatie**

+++Zie details
* **Verplaatste doel-specifieke de documentatiepagina&#39;s van SDK van het Web naar de bewaarplaats van Adobe Target.** Als deel van de de documentatieherstructurering van SDK van het Web, [!DNL Target] - specifieke inhoud is gemigreerd van de algemene documenten van SDK van het Web aan de [!DNL Adobe Target] [ gids van de Ontwikkelaar ](https://experienceleague.adobe.com/en/docs/target-dev/developer/a4t/overview-a4t?lang=en){target=_blank}. Deze verandering verbetert inhoudsontdekkingsbaarheid en zorgt ervoor dat oplossing-specifieke begeleiding door het aangewezen productteam wordt gehandhaafd. (TGT-53374)

+++

**[!UICONTROL Offer Decisions]**

+++Zie details
* **de optie van het Besluit van de aanbieding nu constant zichtbaar tijdens aanvankelijke activiteitenverwezenlijking.** Oplossing voor een probleem in de bijgewerkte gebruikersinterface waarbij de optie [!UICONTROL Offer Decision] niet werd weergegeven tijdens de eerste aanmaakstroom voor A/B-activiteiten, met name als deze optie wordt geopend in de incognitomodus bij huurders waarvoor de optie Aanbiedingsbesluiten is ingeschakeld. De optie werd alleen weergegeven nadat u naar de stap [!UICONTROL Targeting] ging en weer terug naar [!UICONTROL Experiences] . Deze correctie zorgt ervoor dat de optie [!UICONTROL Offer Decision] direct beschikbaar is tijdens de eerste installatie, waardoor de bruikbaarheid wordt verbeterd en verwarring wordt verminderd. (TGT-51888)

+++

**[!UICONTROL Offers]**

+++Zie details
* **Oplossing voor een probleem waarbij omleidingsvoorstellen `redirectOptions` niet in de payload hadden opgenomen wanneer `includeContent=true` .** Klanten die omleidingsvoorstellen ophalen met `includeContent=true ` ontbraken het veld `redirectOptions` in de antwoordlading. Deze inconsistentie beïnvloedde werkstromen, zoals het aanbieden kopiëren en het creëren van activiteit. Omleidingsvoorstellen bevatten nu correct `redirectOptions` wanneer inhoud wordt aangevraagd. (TGT-53737)

+++

**[!DNL Recommendations]**

+++Zie details
* **klik het volgen herstelde voor [!UICONTROL Recommendations] activiteiten die in bijgewerkte UI worden gecreeerd.** Oplossing voor een probleem waarbij [!UICONTROL Recommendations] -activiteiten die in de bijgewerkte gebruikersinterface zijn gemaakt, kliktracking niet konden registreren. Dit leidde tot nul gerapporteerde conversies. De activiteiten die in de erfenis UI worden gebouwd volgden correct kliks en rapporteerden omzettingen zoals verwacht. Deze correctie zorgt ervoor dat de activiteiten van Aanbevelingen die in de bijgewerkte UI worden gecreeerd nu de correcte volgende attributen omvatten, herstellend omzetting rapportering en groepering met metriek A4T. (TGT-53287)
* **klik het volgen hersteld voor de activiteiten van de Aanbeveling.** Oplossing voor een probleem waarbij [!UICONTROL Recommendations] -activiteiten die in de bijgewerkte gebruikersinterface zijn gemaakt, kliktracking niet konden registreren. Dit leidde tot nul gerapporteerde conversies. De oudere UI paste correct een volgende identiteitskaart (`at-track-click`) op [!UICONTROL Recommendations] inhoud toe, terwijl bijgewerkte UI per ongeluk placeholder (`__recsClickTrackIdPlaceholder__`) opnam, verhinderend achterste het volgen. Met deze correctie zorgt u ervoor dat [!DNL Recommendations] -inhoud nu de juiste tracking-id bevat en dat de conversierapportage en de uitlijning met A4T-meetgegevens worden hersteld. (TGT-53496)
* **de redacteur van de Inzameling crashte in bijgewerkte UI.** Oplossing voor een probleem in de bijgewerkte gebruikersinterface van [!UICONTROL Visual Experience Composer] (VEC) waarbij het openen van een verzameling in het deelvenster Editor ertoe heeft geleid dat de pagina vastliep met een TypeError: Kan de eigenschappen van undefined niet lezen (met &#39;customLocale&#39;). Deze fout is opgetreden bij meerdere typen activiteit, waaronder [!UICONTROL Recommendations] - en A/B-tests. (TGT-53703)
* **Optie om geselecteerde inzameling te verwijderen die in VEC wordt hersteld.** Oplossing voor een probleem in de VEC waarbij gebruikers een geselecteerde verzameling alleen in een [!UICONTROL Recommendations] -activiteit konden vervangen, maar dit niet volledig konden verwijderen. Door deze beperking werden gebruiksgevallen geblokkeerd die een schone verwijdering van de collectie zonder vervanging vereisen. Deze correctie introduceert een duidelijke optie om de geselecteerde inzameling te verwijderen, die grotere flexibiliteit in activiteitenopstelling en groepering met verouderd gedrag UI toestaat. (TGT-53652)
* **de de criteria van de Douane inzamelingen tonen nu correct in [!UICONTROL Recommendations] UI.** Oplossing voor een probleem in de interface Aanbevelingen waarbij verzamelingen die zijn gemaakt op basis van aangepaste criteria, de productresultaten niet konden weergeven. Terwijl de standaard op attribuut-gebaseerde inzamelingen zoals verwacht werkten, die douanefilters gebruikten &quot;Geen Resultaten die&quot;ondanks geldige catalogusgelijken terugkwamen. Deze correctie zorgt ervoor dat verzamelingen die aangepaste kenmerken gebruiken, nu correct worden gevuld op het tabblad [!UICONTROL Product] en dat de volledige functionaliteit voor workflows met gepersonaliseerde aanbevelingen wordt hersteld. (TGT-53653)
* **verholpen een kwestie waar de inzamelingen geen producten toen eerste het openen van de [!UICONTROL Products] pagina tonen.** Klanten die in de sectie [!UICONTROL Recommendations] verzamelingen openen, hebben lege productresultaten ervaren bij het openen van de pagina [!UICONTROL Products] . Dit probleem is veroorzaakt door een backendfout in de GraphQL-query, die productgegevens voor verzamelingen met aangepaste criteria niet heeft geladen. Het probleem is opgelost en producten worden nu correct weergegeven zonder dat het omschakelen naar een andere omgeving vereist is. (TGT-53694)
* **verholpen een kwestie waar de inzamelingen niet in op vorm-gebaseerde [!UICONTROL Recommendations] activiteiten konden worden verwijderd.** Klanten die [!UICONTROL Recommendations] -activiteiten maken met [!UICONTROL Form-Based Experience Composer] , kunnen de selectie van een eerder gekozen verzameling niet opheffen. In de gebruikersinterface moest een verzameling worden geselecteerd voordat deze kon worden opgeslagen, zodat gebruikers niet konden terugkeren naar &quot;Alle verzamelingen&quot;. Dit gedrag is bijgewerkt om de functionaliteit aan te passen VEC, toestaand klanten om zonder een geselecteerde inzameling te bewaren en het gebrek aan &quot;Alle Verzamelingen&quot;zoals verwacht. (TGT-53708)
* **Vaste een kwestie waar de bevorderingen niet door attribuut wegens ontbrekende inzameling of het filtreren regelwaarden konden worden geplaatst.** Klanten die bevorderingen door attribuut in activiteit-creeren proces vormden ondervonden een fout verklarend dat een bevordering of een inzamelingsidentiteitskaart of het filtreren regelwaarden mist. Deze validatie blokkeerde progressie, zelfs als de installatie volledig leek. De bevorderingen kunnen nu met succes worden bewaard wanneer gevormd door attribuut. (TGT-53750)
* **verholpen een kwestie waar de activiteiten niet wegens dubbele ervaringsnamen konden worden bewaard.** Klanten hebben een ongeldige fout met gebruikersinvoer aangetroffen bij het opslaan van activiteiten die specifieke combinaties van criteria en ontwerpen bevatten. De fout werd teweeggebracht door dubbele ervaringsnamen, zelfs toen de opstelling geldig leek. Activiteiten met verschillende configuraties kunnen nu worden opgeslagen zonder conflicten te benoemen. (TGT-53805)
* **Vaste een kwestie waar de bevestiging ongeldig bleef voor bevorderingen die door attribuut worden gevormd.** Klanten stuitten permanente validatiefouten bij het instellen van promoties per kenmerk tijdens het maken van activiteiten, zelfs als alle vereiste velden correct zijn ingevuld. Dit probleem is veroorzaakt door onjuiste validatielogica in de [!UICONTROL Recommendations] -workflow. Op kenmerken gebaseerde promoties valideren en opslaan nu naar behoren. (TGT-53811)
* **Oplossing een kwestie waar het toepassen van een bevordering op een levende [!UICONTROL Recommendations] activiteit een fout teweegbracht.** Klanten vonden de fout &quot;Een Bevordering mist of een identiteitskaart van de Inzameling of het filtreren regelwaarden&quot;wanneer het proberen om een voorbevordering op een levende [!UICONTROL Recommendations] activiteit toe te passen, zelfs na het verstrekken van geldige configuratiedetails. Promoties kunnen nu met succes worden toegepast op live-activiteiten zonder validatiefouten te veroorzaken, zodat de bijgewerkte interface voor het maken van activiteiten vloeiender wordt. (TGT-53738)
* **verholpen een kwestie waar de producten niet zichtbaar in inzamelingen binnen [!UICONTROL Recommendations] UI waren.** Klanten van één huurder hebben gemeld dat productlijsten niet konden worden geladen wanneer ze bepaalde verzamelingen in het gedeelte [!UICONTROL Recommendations] van de nieuwe gebruikersinterface konden weergeven. Het probleem is tijdelijk opgelost door van omgeving te veranderen, maar dit probleem heeft tot een slechte gebruikerservaring geleid. Productentiteiten worden nu consistent geladen zonder dat omgevingsschakelingen vereist zijn. (TGT-53783)
* **Vaste een kwestie waar de criteria en de ontwerpen niet op één lijn in activiteit-creeer UI werden getoond.** Eerder werden criteria en ontwerpen in het activity-create proces weergegeven in een gecomprimeerde indeling, waardoor het voor klanten moeilijk was om afzonderlijke items weer te geven en te beheren. Elk criterium en ontwerp worden nu op een eigen regel weergegeven, waardoor de leesbaarheid en bruikbaarheid in de bijgewerkte gebruikersinterface worden verbeterd. (TGT-53818)

+++

**Rapporten**

+++Zie details
* **[!UICONTROL Total Revenue]is nu opgenomen in CSV-exportbewerkingen van activiteitenrapporten.** Oplossing voor een probleem in de bijgewerkte [!UICONTROL Overview] UI waarbij de totale opbrengsten correct werden weergegeven in de weergave Activiteitenrapport, maar die ontbraken in de CSV-export, met $0. Door deze discrepantie konden gebruikers niet vertrouwen op geëxporteerde gegevens voor offline analyse en rapportage. (TGT-53325)
* **[!UICONTROL Total Sales]is nu opgenomen in CSV-exportbewerkingen van activiteitenrapporten.** Oplossing voor een probleem in de bijgewerkte gebruikersinterface waarin [!UICONTROL Total Sales] correct werd weergegeven in de weergave Activiteitenrapport, maar dat niet aanwezig was in de CSV-export. Door deze discrepantie hebben gebruikers geen toegang tot volledige prestatiegegevens in gedownloade rapporten. Deze correctie zorgt ervoor dat [!UICONTROL Total Sales] -waarden nu op de juiste wijze worden opgenomen in CSV-export, zodat de consistentie tussen in-app-rapportage en offline-analyse wordt hersteld. (TGT-5330)
* **Verbeterd foutenoverseinen voor [!UICONTROL Graph View] wanneer de metriek niet worden toegelaten.** Oplossing voor een probleem in de VEC waarbij [!UICONTROL Graph View] een algemeen bericht &#39;Er is iets fout gegaan&#39; weergaf wanneer een gevraagde metrische waarde niet was ingeschakeld in de bijbehorende [!DNL Analytics] rapportsuite. Dit probleem is veroorzaakt door een `not_enabled_metric` -fout in het GraphQL-antwoord op de achtergrond. Deze correctie vervangt de vage fout door een informatieve boodschap die gebruikers helpt configuratieproblemen in [!DNL Analytics] te identificeren, die verwarring en onnodige ondersteuningsescalaties verminderen. (TGT-53577)
* **Vaste een kwestie waar de rapportduur de gesteunde grens van 90 dagen overschreed.** Klanten die het filter &quot;[!UICONTROL Last X Days]&quot; in de sectie [!UICONTROL Reports] gebruiken, konden een langere periode dan 90 dagen selecteren, wat tot prestatieproblemen en onvolledige gegevens kon leiden. Het filter is bijgewerkt om een maximumbereik van 90 dagen te handhaven, zodat consistente en betrouwbare rapportage wordt gegarandeerd. (TGT-53795)
* **Vaste een kwestie waar de prestatiesCSV rapporten werden geproduceerd gebruikend het standaardmilieu in plaats van geselecteerde.** Eerder, toen klanten de omgeving in rapportinstellingen veranderden en een prestatierapport genereerden, bevatte de resulterende CSV gegevens van de standaardomgeving in plaats van de geselecteerde.  De gebruikersinterface geeft nu correct de parameter `environmentId` door, zodat in het rapport de gekozen omgeving wordt weergegeven. Bovendien is de foutafhandeling verbeterd. Als GraphQL-fouten optreden tijdens het genereren van CSV-bestanden, wordt in de gebruikersinterface nu een duidelijk foutbericht weergegeven in plaats van een leeg CSV-bestand te maken. (TGT-53064)
* **verholpen een kwestie waar de Analytics voor Doel (A4T) het melden er niet in slaagde om gegevens in [!UICONTROL Graph View] te tonen.** Klanten die [!DNL Target] met integratie A4T gebruiken ondervonden een fout &quot;Er is iets fout gegaan&quot;toen het schakelen naar de Mening van de Grafiek op het lusje van de Rapportering van A/B testactiviteiten. Hoewel [!UICONTROL Table View] correct is geladen, kon [!UICONTROL Graph View] geen metrische trends renderen over het geselecteerde tijdbereik. [!UICONTROL Graph View] geeft nu de verwachte prestatiegegevens weer voor alle ondersteunde metingen, waardoor de zichtbaarheid en de rapportnauwkeurigheid in de bijgewerkte gebruikersinterface worden verbeterd. (TGT-53573)

+++

**Visuele Composer van de Ervaring (VEC)**

+++Zie details
* **de meta-gegevens van het Element is nu zichtbaar op omslag in het broodkruimelmenu.** Het menu breadcrumb in de VEC is verbeterd en bevat nu meer elementdetails, zoals id, klasse en naam wanneer u de muisaanwijzer op een item plaatst. Deze verbetering helpt gebruikers elementen gemakkelijker identificeren en onderscheiden tijdens activiteitenopstelling. (TGT-53409)
* **Breadcrumb hover benadrukt nu het overeenkomstige element in VEC.** Verbeterd [!UICONTROL Visual Experience Composer] om het overeenkomende element in de editor te markeren wanneer u de muisaanwijzer op items in het menu breadcrumb plaatst. Het elementtype wordt ook weergegeven, zoals container, vette tekst of knop. Dit gedrag is van toepassing op elementen op hetzelfde niveau en sluit niet-ondersteunde typen uit, zoals SVG, op basis van de validatielijst. (TGT-53411)
* **Unsaved veranderingsalarm die in de veranderingswerkschema&#39;s wordt hersteld VEC.** Oplossing voor een probleem in de VEC waarbij gebruikers niet meer op de hoogte werden gesteld van niet-opgeslagen wijzigingen in aangepaste codewijzigingen. In tegenstelling tot de oudere UI, ontbrak de nieuwe ervaring herinneringen wanneer het navigeren weg of het sluiten van de verpersoonlijkingsredacteur, die tot toevallig verlies van vooruitgang leidde. Met deze correctie worden waarschuwingen voor alle wijzigingstypen, inclusief aangepaste code, hersteld en wordt ervoor gezorgd dat gebruikers worden gewaarschuwd voordat ze afsluiten zonder op te slaan. (TGT-53435).
* **de codeveranderingen van de Douane blijven nu tijdens pagina verfrissen in VEC.** Oplossing voor een probleem in de VEC waarbij wijzigingen in aangepaste code verloren gingen tijdens het vernieuwen van de website. Dit probleem is opgetreden op pagina&#39;s met meerdere herladingen, waardoor de editor niet-opgeslagen wijzigingen opnieuw kon instellen en herstellen. De correctie zorgt ervoor dat aangepaste codebewerkingen intact blijven, zelfs als de pagina tijdens het bewerken opnieuw wordt geladen, zodat er geen onbedoeld verlies van voortgang optreedt. (TTGT-53501)
* **Login probleem dat voor plaatstoegang binnen VEC wordt opgelost.** Oplossing voor een probleem waarbij gebruikers zich niet konden aanmelden bij hun site terwijl ze deze via de VEC opvroegen. De aanmeldstroom heeft gebruikers herhaaldelijk omgeleid naar de aanmeldingspagina, waardoor het instellen en voorvertonen van activiteiten niet mogelijk is. Deze moeilijke situatie zorgt ervoor dat VEC niet meer met login gedrag interfereert, die verwachte toegang voor voor authentiek verklaarde gebruikers herstellen. (TGT-53524)
* **de kwestie van de duplicaties van het Koekje die in uitbreiding VEC Helper wordt opgelost.** Oplossing voor een probleem waarbij de [!UICONTROL Adobe Experience Cloud Visual Editing Helper] -extensie het `at_qa_mode` -cookie tijdens QA dupliceerde via voorbeeldkoppelingen. Wanneer handmatig van voorvertoningsindexen wordt gewisseld, zijn er meerdere cookies gemaakt met conflicterende waarden in verschillende domeinen, zodat testers niet op betrouwbare wijze van variant kunnen wisselen. Dit gedrag werd zelfs buiten de interface van het Doel waargenomen en beïnvloedde zowel interne als cliëntrekeningen. Deze oplossing zorgt voor een consistente verwerking van cookies door dubbele vermeldingen te voorkomen en het domeinbereik uit te lijnen, zodat u naadloze variantschakelingen kunt uitvoeren zonder handmatig cookie op te ruimen. (TGT-53579)
* **Vaste een kwestie waar het klikken van elementen op een bepaalde homepage geheugenlekken veroorzaakte.** Klanten die activiteiten op deze website maken, hebben geheugenlekken ervaren tijdens het werken met pagina-elementen. De kwestie werd verbonden aan bovenmatige consolewaarschuwingen en stijgend geheugengebruik in subframes, met name met betrekking tot misvormde prijszetattributen. Geheugengebruik blijft nu stabiel tijdens interactie. (TGT-53761)
* **Vaste een kwestie waar VEC vastliep en een leeg scherm toonde toen het laden van bepaalde activiteiten.** Klanten van een specifieke huurder hebben gemeld dat de editor specifieke activiteiten niet heeft geladen. De VEC bleef vastzitten op &quot;Aanvankelijke wijzigingen toepassen&quot; alvorens te crashen en een leeg scherm te tonen. De VEC laadt nu betrokken activiteiten zonder fouten in het bijgewerkte activity-create proces. (TGT-52932)
* **Oplossing voor een probleem waarbij de [!UICONTROL Manage Content] rail in [!UICONTROL Automated Personalization] -activiteiten inconsistente plaatslabels weergeven.** Klanten hebben gemeld dat in de [!UICONTROL Manage Content] -rail onjuist overeenkomende locatienummers op de tabbladen [!UICONTROL Experiences] en [!UICONTROL Offers] werden weergegeven. (bijvoorbeeld, Plaats 2 en Plaats 4 in Ervaring, en Plaats 1 en Plaats 2 in Aanbieding) zelfs wanneer slechts twee plaatsen werden gevormd. De etiketten van de plaats zijn nu verenigbaar en nauwkeurig in kaart gebracht aan wijzigingen, die helderheid en bruikbaarheid in activiteit-creeer proces verbeteren. (TGT-52934)
* **Vaste een kwestie waar de wijzigingen in VEC na sparen werden verloren.** Klanten hebben gemeld dat de pagina na het opslaan van een wijziging in de VEC zou worden vernieuwd en de wijziging zou terugkeren naar de vorige versie. Dit probleem heeft ertoe geleid dat de meest recente updates verloren zijn gegaan, tenzij de volledige activiteit onmiddellijk werd opgeslagen. Wijzigingen blijven nu correct na het opslaan behouden en de editor keert wijzigingen niet meer onverwacht terug, zodat een betrouwbare ervaring in de workflow voor het maken van activiteiten wordt gegarandeerd. (TGT-53500)
* **Verbeterde elementselectie in VEC door elementtype op te tonen over aanwijzen en selectie.** Om de bruikbaarheid tijdens het maken van activiteiten te verbeteren, simuleert VEC nu HTML-elementen met het type wanneer deze worden aangeroepen of geselecteerd. Deze verbetering helpt klanten gemakkelijker de correcte elementen identificeren en selecteren. Geselecteerde elementen worden gemarkeerd met een duidelijke kleur en aangehechte elementen worden omlijnd in blauw. Het elementtype wordt ook weergegeven, zodat de context tijdens het bewerken duidelijker wordt. (TGT-53502)

+++

## DataStream-updates (19 september 2025)

De combinatie van gegevensstroom-id en sandbox moet uniek zijn voor [!DNL Adobe Target] -doelverbindingen.

Bijgewerkte validatielogica voor [!DNL Target] -doelverbindingen om te zorgen dat de combinatie van de gegevensstroom-id en de naam van de sandbox uniek moet zijn binnen een IMS-organisatie. Dit betekent:

* Dezelfde gegevensstroom-id + naamcombinatie van sandbox kan niet opnieuw worden gebruikt via meerdere [!DNL Target] doelverbindingen.
* Dezelfde gegevensstroom-id kan alleen voor verschillende verbindingen worden gebruikt als deze in verschillende sandboxen zijn geconfigureerd.
* Deze regel is van toepassing op alle gegevensstroomselecties, ook wanneer Geen is geselecteerd.

Deze update zorgt voor een consistente configuratie en voorkomt conflicten in omgevingen met meerdere sandboxen. Voor meer informatie, zie [ verbinding van Adobe Target ](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/catalog/personalization/adobe-target-connection){target=_blank} in de *3&rbrace; gids van de Doelen van Experience Platform &lbrace;.*

## [!DNL Target Standard/Premium] 25.9.1 (5 september 2025)

Deze release bevat de volgende updates en oplossingen:

**[!UICONTROL Experience Fragments]**

+++Zie details
* **Verbeterde gebruikerstoewijzing voor [!UICONTROL AEM Experience Fragment] aanbiedingen.** Oplossing voor een probleem in VEC waarbij het veld [!UICONTROL Last updated] voor [!UICONTROL AEM Experience Fragment] (XF) een code-id onjuist weergeeft in plaats van de gebruikersnaam. Deze discrepantie kwam tijdens aanbiedingsselectie in bijgewerkte UI voor, die tot inconsistentie met de erfenis UI en aanbiedingen van HTML leidt, die correct de naam van de laatste redacteur toonde. Deze correctie zorgt voor consistente toewijzing van gebruikers over aanbiedingstypen, waardoor de transparantie en de uitlijning met het verwachte gedrag worden verbeterd. (TGT-52880 &amp; TGT-52898)

+++

**Offer Decisioning**

+++Zie details
* **de fout van het Besluit van de Aanbieding wordt opgelost voor de aanbiedingen van ODE.** Oplossing voor een probleem waarbij ODE-aanbiedingen (Offer Decision Engine) die via [!DNL Target] zijn geïnjecteerd, een fout van 400 hebben geretourneerd omdat metagegevens over indelingen ontbreken. Het foutbericht geeft aan dat het MIME-type null is, waardoor succesvolle verwerking van biedingsbesluiten wordt voorkomen. Deze oplossing zorgt voor een juiste verwerking van de metagegevens van de aanbieding, herstelt functionaliteit voor levering van gepersonaliseerde inhoud en maakt het mogelijk dat marketingcampagnes zonder onderbreking worden uitgevoerd. (TGT-53635)
* **ODS biedt het teruggeven probleem opgelost aan.** Het volgende probleem is opgelost: [!DNL Offer Decision Service] (ODS)-aanbiedingen die via [!DNL Adobe Journey Optimizer] (AJO) zijn gemaakt, worden niet gerenderd wanneer activiteiten met behulp van de VEC in de bijgewerkte gebruikersinterface zijn gemaakt. Dezelfde configuratie werkte correct in de oudere gebruikersinterface, wat tot verwarring en een geblokkeerde uitvoering van de campagne leidde. Deze oplossing zorgt voor een consistente levering van de aanbieding in beide gebruikersinterfaceversies en herstelt het verwachte gedrag voor AJO-gedreven personalisatie.

+++

**Rapporten**

+++Zie details
* **optie van de Download wordt hersteld in rapportensectie van de bijgewerkte overzichtsUI van Rapporten.** Oplossing voor een probleem in de nieuwe interface voor het overzicht waarin de knop [!UICONTROL Download] ontbreekt in de sectie Rapporten, zodat gebruikers geen scores voor kenmerkbelang kunnen exporteren. Deze update herstelt de volledige exportfunctionaliteit, waardoor gestroomlijnde toegang tot downloadbare gegevens voor analyse en rapportage mogelijk is. (TGT-53222)
* **[!UICONTROL Download full CSV report]wordt hersteld in de weergave [!UICONTROL Important attributes] .** Oplossing voor een probleem in de bijgewerkte interface voor het maken van activiteiten waarbij de knop [!UICONTROL Download full CSV report] ontbreekt in de sectie [!UICONTROL Important Attributes] in de rapportweergave. Met deze oplossing herstelt u de toegang tot downloadbare inzichten en zorgt u voor consistente functionaliteit voor zowel de bijgewerkte als de verouderde gebruikersinterface. (TGT-53238)
* **Opgeloste kwesties UI die [!UICONTROL Auto Target] rapportering in bijgewerkte overzichtsUI beïnvloeden.** Oplossing voor meerdere problemen met de gebruikersinterface in de bijgewerkte interface die gevolgen hebben voor de [!UICONTROL Auto Target] -rapportage. Deze correcties zijn onder andere:

   * Ontbrekende cijfers over lift en betrouwbaarheid in samenvattingsrapporten
   * Onjuiste kleurindicator voor het selectievakje &quot;Modellen gebouwd&quot;
   * Niet-functioneel grafiekrapport ondanks verschillen in gegevens [!DNL Analytics]
   * Ontbrekende downloadkoppeling voor [!UICONTROL Automated Segments] - en [!UICONTROL Important Attributes] -rapporten
   * Verbroken [!UICONTROL Automated Segments] rapportweergave

  Met deze correcties wordt het verwachte rapportgedrag hersteld en wordt de zichtbaarheid van [!UICONTROL Auto Target] -prestaties in de bijgewerkte gebruikersinterface verbeterd. (TGT-53484)

+++

**[!UICONTROL Visual Experience Composer]**

+++Zie details
* **Bevestiging van de Vorm die voor de voorwaarden van de parameteraanwezigheid in bijgewerkte UI wordt verbeterd.** Oplossing voor een probleem in bijgewerkte UI waar het selecteren van &quot; [!UICONTROL Custom mbox parameter value is present]&quot;of &quot;[!UICONTROL Parameter is present]&quot;klanten verkeerd vereiste om een waarde in te gaan. Dit gedrag was in strijd met de bedoelde logica, die eenvoudig controleert of een parameter bestaat, ongeacht de waarde ervan. Met deze correctie wordt formuliervalidatie uitgelijnd op het verwachte gedrag, waardoor de activiteiten vloeiender kunnen worden ingesteld en de bijgewerkte gebruikersinterface volledig kan worden toegepast. (TGT-53638)
* **logica van de Vorm die voor de regels van de parameteraanwezigheid in paginalevering wordt verbeterd.&quot;** Oplossing een kwestie in bijgewerkte UI waar het selecteren van de regels van de paginalevering zoals &quot;[!UICONTROL Parameter is present],&quot;[!UICONTROL Parameter is not present],&quot;[!UICONTROL Parameter value is present],&quot; of &quot;[!UICONTROL Parameter value is not present]&quot;verkeerd vereiste gebruikers om een extra parameterwaarde in te gaan. Dit gedrag was inconsistent met de oudere UI en drukte de voorgenomen logica tegen om parameteraanwezigheid te ontdekken zonder een waarde te specificeren. Deze moeilijke situatie herstelt het verwachte gedrag van de regelconfiguratie, stroomlijnt activiteitenopstelling en verbetert bruikbaarheid. (TGT-53640)
* **de logica van de Bevestiging verbeterde voor multi-page regelbouwer in bijgewerkte UI.** Meerdere validatieproblemen in de builder van meerdere pagina&#39;s in de bijgewerkte gebruikersinterface opgelost. Deze correcties zijn onder andere:

   * Het voorkomen van het maken van regels wanneer de parameter mbox leeg is
   * De juiste foutberichten voor ongeldige regelstatussen weergeven
   * Validatielogica corrigeren voor unaire operatoren en operatoren op basis van parameters die geen operandwaarden vereisen
   * Hash-fragmentregels inschakelen met unaire operatoren door functie voor opslaan te herstellen

  Deze updates verzekeren nauwkeurige regelconfiguratie en verbeteren bruikbaarheid over de complexe scenario&#39;s van de paginalevering. (TGT-53722)
* **het anders noemen van plaats probleem dat in A/B en activiteiten MVT wordt opgelost.** Oplossing voor een fout in de bijgewerkte gebruikersinterface waarbij de naam van een locatie in een [!UICONTROL A/B Test] - of [!UICONTROL Multivariate Test] -activiteit (MVT) niet werd gewijzigd nadat was genavigeerd tussen de lijst met locaties, de locatie van de doellocatie en de locatie van de gebruiker. Deze update zorgt ervoor dat wijzigingen in de locatienaam worden opgeslagen en consistent worden weerspiegeld in de gehele werkstroom. (TGT-52367)
* **de naampersistentie van de Plaats die voor activiteiten MVT en AP in bijgewerkte UI wordt bevestigd.** Oplossing voor een probleem in de bijgewerkte gebruikersinterface waarbij locatienamen die werden bewerkt in [!UICONTROL Multivariate Test] (MVT)- en [!UICONTROL Automated Personalization] (AP)-activiteiten niet correct werden opgeslagen. Nadat de naam van een locatie was gewijzigd, werd door navigatie tussen tabbladen, zoals [!UICONTROL Targeting] en [!UICONTROL Experiences] , de vorige status van de namen hersteld. Deze moeilijke situatie verzekert verenigbare plaats het noemen over lusjes en verbetert betrouwbaarheid tijdens activiteitenopstelling. (TGT-52927)
* **het etiketteren van de Plaats die in het beheer ervaringspaneel voor MVT activiteiten wordt verbeterd.** Oplossing voor een probleem in de bijgewerkte gebruikersinterface waarbij in het deelvenster [!UICONTROL Manage Experiences] in [!UICONTROL Multivariate Test] -activiteiten (MVT) inconsistente plaatsnummering werd weergegeven. Deze correctie zorgt ervoor dat locatielabels opeenvolgend zijn en correct zijn uitgelijnd met door de gebruiker gedefinieerde wijzigingen, waardoor de helderheid en bruikbaarheid tijdens het instellen van de ervaring worden verbeterd. (TGT-52929)

+++

## Aanvullende opmerkingen bij de release en versiedetails

| Bron | Details |
|--- |--- |
| [ de nota&#39;s van de Versie: De Ervaring van het Platform van Adobe Target Web SDK ](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=en) | Details over veranderingen in elke versie van het Web SDK van het Platform. |
| [ at.js versiedetails ](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html){target=_blank} | Informatie over de wijzigingen in elke versie van de JavaScript-bibliotheek [!DNL Adobe Target] at.js. |

## Documentatiewijzigingen, Opmerkingen bij de vorige release en Opmerkingen bij de release van Experience Cloud

Naast de notities voor elke release bevatten de volgende bronnen aanvullende informatie:

| Bron | Details |
|--- |--- |
| [ Veranderingen van de Documentatie ](/help/main/r-release-notes/doc-change.md) | Gedetailleerde informatie weergeven over updates van deze handleiding die niet zijn opgenomen in deze releaseopmerkingen. |
| [ de nota&#39;s van de Versie voor vorige versies ](/help/main/r-release-notes/release-notes-for-previous-releases.md). | Informatie weergeven over nieuwe functies en verbeteringen in vorige versies van Target Standard en Target Premium. |
| [ de Nota&#39;s van de Versie van Adobe Experience Cloud ](https://experienceleague.adobe.com/docs/release-notes/experience-cloud/current.html){target=_blank} | Bekijk de nieuwste releaseopmerkingen voor de Adobe Experience Cloud-oplossingen. |

## Prerelease-informatie {#section_5D588F0415A2435B851A4D0113ACA3A0}

De volgende middelen laten u zien wat in de volgende versie van het Doel komt.

| Bron | Details |
|--- |--- |
| [ de Prioritaire Update van het Product van Adobe ](https://www.adobe.com/subscription/priority-product-update.html){target=_blank} | Ontvang voorafgaande meldingen over aanstaande productverbeteringen voor [!DNL Target] en andere [!DNL Adobe Experience Cloud] -oplossingen. |
| [ de Nota&#39;s van de Versie van het Doel - preRelease ](/help/main/r-release-notes/target-release-notes.md){target=_blank} | Informatie over de versies van het Doel van de huidige maand, met inbegrip van pre-releaseinformatie. |
