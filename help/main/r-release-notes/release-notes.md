---
keywords: releaseopmerkingen;nieuwe functies;releases;updates;update;release;verbetering;verbeteringen;correcties;foutoplossingen;updates;huidige updates
description: Leer over de nieuwe eigenschappen, de verhogingen, en de moeilijke situaties inbegrepen in de huidige versie van  [!DNL Adobe Target], met inbegrip van SDKs, APIs, en de bibliotheken van JavaScript.
landing-page-description: Leer over de nieuwe eigenschappen, de verhogingen, en de moeilijke situaties inbegrepen in de huidige versie van  [!DNL Adobe Target].
short-description: Leer over de nieuwe eigenschappen, de verhogingen, en de moeilijke situaties inbegrepen in de huidige versie van  [!DNL Target].
title: Wat is inbegrepen in de huidige Versie?
feature: Release Notes
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
source-git-commit: 223a0f62bcd9a52bd9181e0a439e02164abbfec4
workflow-type: tm+mt
source-wordcount: '7159'
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

## [!DNL Target Standard/Premium] 25.8.4 (1 september 2025)

Deze release bevat de volgende updates en oplossingen:

**[!UICONTROL Activities]**

+++Zie details
* **Klanten konden activiteit of documentnamen van[!UICONTROL Activity Overview]** niet kopiëren: Eerder, konden de klanten niet de naam van een activiteit of de bijbehorende aanbieding/document direct van [!UICONTROL Activity overview] in het bijgewerkte activiteit-creeer proces kopiëren. Deze beperking beïnvloedde de bruikbaarheid, vooral op kleinere schermen. Klanten kunnen nu gemakkelijk zowel activiteit- als documentnamen kopiëren zonder tijdelijke oplossingen. (TGT-51850)
* **Proactieve opname van gebogen [!DNL Target] klantengegevens tijdens activiteitenverwezenlijking**: Verbeter de activiteit-creeer proces door de pro-actieve inzameling van rapporten, inhoud, en screenshots van [!DNL Target] klanten toe te laten. Deze verbetering verhelpt gegevenshiaten die in bestaande gebruiksgevallen worden geïdentificeerd en helpt nauwkeurigere inzichten tijdens activiteit en experimenteeropstelling te verzekeren. (TGT-52415)
* **AP de activiteiten haalden model-klaar geen gegevens in de [!UICONTROL Reports] sectie**: De klanten die de activiteiten van Automated Personalization (AP) in de [!UICONTROL Reports] sectie bekijken konden model-klaar indicatoren op de rapportgroep en aanbiedingsniveau niet zien. Dit probleem is opgetreden omdat modelgegevens niet correct vanaf de achtergrond werden opgehaald. De functionaliteit is hersteld en modelgegevens worden nu op de verwachte manier weergegeven. (TGT-53600 &amp; TGT-53601)
* **Activiteiten die voor de toekomst worden gepland vertoonde verkeerd een &quot;[!UICONTROL Live]&quot;status in het [!UICONTROL Activity] overzicht**: De klanten merkten op dat de activiteiten die in de toekomst zouden beginnen verkeerd werden gemerkt als &quot;[!UICONTROL Live]&quot;in het [!UICONTROL Activity] overzicht. Deze statuswanverhouding werd opgelost, en de geplande activiteiten tonen nu correct als &quot;[!UICONTROL Scheduled]&quot;zonder te vereisen pagina verfrist zich. (TGT-52835)

+++

**[!UICONTROL Recommendations]**

+++Zie details
* **lijst van het Product was niet zichtbaar in de [!UICONTROL View Collection] dialoog:** Eerder, konden de klanten niet de productlijst zien wanneer het bekijken van een inzameling in [!UICONTROL Recommendations] tabel. In het dialoogvenster [!UICONTROL View Collection] worden nu correct de bijbehorende producten weergegeven, waardoor de transparantie en bruikbaarheid in de bijgewerkte gebruikersinterface van [!UICONTROL Recommendations] worden verbeterd. (TGT-50531)
* **Vaste een kwestie die case-sensitive het filtreren in [!UICONTROL Product Catalog Search] geavanceerde onderzoek** veroorzaakte: Het geavanceerde onderzoek het filtreren in de [!UICONTROL Product Catalog Search] pagina negeert nu correct casegevoeligheid, die op het gedrag van zowel de backend als de diensten van GraphQL richt. Deze update zorgt voor consistente en nauwkeurige resultaten voor suggesties voor klanten, ongeacht de tekstbehuizing. (TGT-53585)
* **het Geavanceerde onderzoek in bijgewerkte [!UICONTROL Product Catalog Search] UI verstrekte geen suggesties**: De klanten die de geavanceerde onderzoekseigenschap in bijgewerkte [!UICONTROL Product Catalog Search] UI gebruiken werden vereist om nauwkeurige waarden met correcte spelling in te gaan, aangezien geen suggesties werden getoond. Door deze kwestie werd het moeilijk om producten efficiënt te vinden. Suggesties worden nu op de verwachte manier weergegeven tijdens geavanceerde zoekinvoer. (TGT-52008)
* **Sommige fiatteurs konden geen producten in[!UICONTROL Product Catalog Search]** bekijken: Klanten met [!UICONTROL Approver] toestemmingen konden geen producten in [!UICONTROL Product Catalog Search] zien, ondanks andere gebruikers met identieke rollen die toegang hebben. Dit probleem is veroorzaakt door een inconsistentie in machtigingen die invloed heeft op de zichtbaarheid van de catalogus. Alle fiatteurs kunnen nu naar behoren producten in de sectie [!UICONTROL Recommendations] bekijken. (TGT-53617)

+++

**[!UICONTROL Reports]**

+++Zie details
* **de Rapporten slaagden er niet in om voor het publiek van de Desktop wegens een ongeldige fout van de publieksnaam** te laden: De klanten ontmoetten een fout van GraphQL toen het proberen om rapporten voor één publiek in activiteit-creeer proces te bekijken. Het systeem heeft een bericht &quot;Invalid publieksnaam: XXXXX&quot; geretourneerd, waardoor toegang tot rapportgegevens wordt voorkomen. Rapporten worden nu correct geladen voor het desktoppubliek. (TGT-53371)
* **de Omschakeling publiek op de pagina van Rapporten veroorzaakte fouten in het Doel UI**: De klanten ontmoetten fouten wanneer het selecteren van bepaalde soorten publiek in de [!UICONTROL Reports] sectie. Dit probleem werd veroorzaakt door een ongeldige verwerking van het publiek in GraphQL-aanroepen met een achtergrond, met onverwachte fouten en ontbrekende gegevens als gevolg. Het probleem is opgelost en het bureaubladpubliek wordt nu zonder fouten geladen, zelfs als er geen gegevens beschikbaar zijn. (TGT-53370)
* **[!UICONTROL Graph view]in de [!UICONTROL Reports] sectie toonde geen waarden van[!DNL Analytics]**: Klanten die tot [!UICONTROL Graph view] in de Re  havensectie toegang hebben ontleenden gegevens, met alle waarden die als nul verschijnen. Dit probleem is veroorzaakt door onjuiste gegevens die zijn opgehaald uit [!UICONTROL Analytics] . In [!UICONTROL Graph view] worden nu de juiste waarden weergegeven. (TGT-52792)
+++

**[!UICONTROL Visual Experience Composer] (VEC)**

+++Zie details
* **klikkend &quot;Accept Cookies&quot;gebruikend [!UICONTROL Enhanced Experience Composer] (EEG) ontbroken toe te schrijven aan een ontbrekende functie**: De klanten rapporteerden dat het proberen om koekjes via EEG goed te keuren in een consolefout resulteerde: `handleclickAcceptAllButton is not defined`. De functionaliteit voor het accepteren van cookies werkt nu zoals u had verwacht en zorgt voor een vloeiender ervaring tijdens het maken van activiteiten in de bijgewerkte gebruikersinterface. (TGT-52794)
* **Nieuwe E.E.G. UI slaagde er niet in om bepaalde pagina&#39;s te laden die eerder in erfenis UI** werden gesteund: De klanten rapporteerden dat nieuwe EEG sommige pagina&#39;s niet kon laden, die in erfenis UI ondanks iframe-het bouwen code aanwezig op de plaats toegankelijk waren. Het bijgewerkte activity-create proces ondersteunt nu het laden van deze pagina&#39;s en het herstellen van compatibiliteit voor workflows voor het maken van activiteiten. (TGT-53061)
* **VEC toonde een leeg wit scherm wanneer het uitgeven van ervaringen**: De klanten van een bepaalde huurder rapporteerden dat het scherm VEC leeg ging wanneer het proberen om ervaringen in bijgewerkte VEC uit te geven. Deze kwestie beïnvloedde zowel nieuw gecreëerde als oudere activiteiten, die werkschemacontinuïteit verhinderen. VEC laadt nu correct, toestaand klanten om ervaringen zonder onderbreking uit te geven. (TGT-53547)
* **VEC crashte en toonde een leeg scherm wanneer het laden van bepaalde activiteiten**: De klanten van een bepaalde huurder rapporteerden dat VEC er niet in slaagde om specifieke activiteiten te laden. De ervaringseditor bleef vastzitten op &quot;Aanvankelijke wijzigingen toepassen&quot; voordat deze vastliep en een leeg scherm weergaf. Consolefouten duiden op een fout bij het lezen van niet-gedefinieerde eigenschappen. De redacteur laadt nu betrokken activiteiten zonder fouten in bijgewerkte VEC. (TGT-53548)
* **het ontruimen van alle datumwaarden die Backspace gebruiken veroorzaakte de pagina om te crashen**: Klanten die activiteiten in de [!UICONTROL Goals & Settings] sectie plannen ervoeren een neerstorting wanneer het gebruiken van Backspace om alle waarden van &quot;[!UICONTROL Specified Date & Time]&quot;gebieden te ontruimen. Deze kwestie werd veroorzaakt door een ongeldige verwijzingsfout in de datum-behandelende logica. De pagina verwerkt lege datuminvoer probleemloos zonder vast te lopen. (TGT-53624)
* **Geen producten verschenen in [!UICONTROL Product Catalog Search] toe te schrijven aan een ongeldige lading**: De klanten die tot de [!UICONTROL Recommendations] sectie in [!UICONTROL Product Catalog Search] toegang hebben ondervonden lege resultaten die door een ongeldige lading van GraphQL worden veroorzaakt. Door deze backendfout konden de productgegevens niet correct worden geladen. Producten worden nu weergegeven zoals u had verwacht in de bijgewerkte gebruikersinterface. (TGT-53630)
* **[!DNL Scene7]-afbeeldingen zijn met een lagere resolutie opgeslagen in de bijgewerkte VEC** : klanten die ervaringen in de bijgewerkte VEC hebben bewerkt, hebben gemerkt dat [!UICONTROL Scene7] -afbeeldings-URL&#39;s zijn opgeslagen zonder resolutieparameters, waardoor afbeeldingen van lagere kwaliteit worden geleverd (400×400 in plaats van de beoogde 800×800). URL&#39;s van afbeeldingen behouden nu de juiste parameters voor een juiste resolutie. (TGT-52631)
* **de levende activiteiten konden nog in VEC** worden uitgegeven: De klanten konden tot bewerkingsopties voor levende activiteiten in bijgewerkte VEC toegang hebben, die tot onbedoelde veranderingen kon leiden. Dit probleem is opgelost door de bewerkingsfunctionaliteit voor live activiteiten uit te schakelen. De bewerkingsknoppen zijn nu verborgen in de activiteitenlijst en het overzicht voor editors, terwijl fiatteurs en andere rollen ongewijzigd blijven. (TGT-53055)
* **werd buiten bedrijf gesteld [!UICONTROL Failed] en [!UICONTROL Draft] activiteitensectie in bijgewerkte VEC**: [!UICONTROL Failed] en [!UICONTROL Draft] activiteitenopties zijn verwijderd uit bijgewerkte VEC. De nieuwe interface ondersteunt geen conceptframes meer en mislukte campagnes worden niet opgeslagen op de achtergrond. Deze opties zijn niet langer relevant. Verwante filters en achterste velden (bijvoorbeeld `uiSyncFailed` , `errorMessage` ) zijn ook verwijderd om activiteitsbeheer te stroomlijnen. (TGT-53150)
* **Onbekwaam aan login aan VEC voor een activiteit**: De klanten die aan login aan hun plaats door VEC probeerden opnieuw gericht aan de login pagina, verhinderend toegang tot activiteit het uitgeven. Dit probleem kon intern niet worden gereproduceerd en had mogelijk betrekking op de verwerking van sessies aan de site. De aanmeldstroom is gestabiliseerd en klanten hebben nu toegang tot de VEC zonder omleidingsfouten. (TGT-53524)
* **die tweemaal op de achterknoop op [!UICONTROL Browse] wijze drukken veroorzaakte VEC om te crashen**: Klanten die door [!UICONTROL Browse] wijze in VEC navigeren ervaren crashes wanneer tweemaal het drukken van de achterknoop van browser. Dit probleem heeft ertoe geleid dat de editor vastloopt en dat een pagina moet worden vernieuwd. De redacteur behandelt nu navigatie betrouwbaar terug zonder het crashen. (GT-53568)
* **de Activiteiten konden niet worden uitgegeven toe te schrijven aan niet bepaalde plaatstoewijzingen**: De klanten ontmoetten een fout toen het proberen om activiteiten uit te geven, die door ongedefinieerde plaats IDs in de `LocationMapping.behaviorTargetedActivity` logica wordt veroorzaakt. Deze kwestie resulteerde in een 400 fout en geblokkeerde activiteitenupdates. Activiteiten kunnen nu worden bewerkt zonder validatiefouten die betrekking hebben op de locatie. (TGT-53607)
* **het Opslaan activiteiten teweegbrachten een ongeldige fout van de gebruikersinput**: De klanten ontmoetten een ongeldige fout van de gebruikersinput wanneer het proberen om activiteiten na het maken van minder belangrijke wijzigingen in bijgewerkte VEC te bewaren. De fout is veroorzaakt door onjuiste locatietoewijzingen in de achtergrondvalidatielogica. Activiteiten kunnen nu met succes worden opgeslagen zonder locatiefouten te veroorzaken. (TGT-53603)

+++

## [!DNL Target Standard/Premium] 25.8.3 (21 augustus 2025)

Deze release bevat de volgende updates en oplossingen:

**[!UICONTROL Activities]**

+++Zie details
* **Vaste een kwestie waar de besparingsactiviteiten een ongeldige fout van de gebruikersinput toe te schrijven aan misvormde bezitsgegevens** teweegbrachten: De klanten ontmoetten een kritieke fout toen het proberen om bestaande activiteiten te bewaren. Het foutbericht gaf ongeldige gebruikersinvoer aan, met name door te verwijzen naar een niet-herkende eigenschapsnaam-inhoud in de JSON-payload. Met name werden nieuwe activiteiten met dezelfde eigenschap opgeslagen, wat erop wijst dat het probleem geïsoleerd was voor gegevens over oudere activiteiten. Het activity-create proces behandelt nu correct verouderde bezitsconfiguraties, die ongeldige inputfouten verhinderen en verenigbaar sparen gedrag over nieuwe en bestaande activiteiten verzekeren. (TGT-53507)
* **Vaste een kwestie die klanten verhinderde een activiteit toe te schrijven aan een fout te bewaren InvalidProperty.Json**: De klanten ontmoetten een fout toen het proberen om een activiteit in bijgewerkte UI, zelfs zonder enige wijzigingen te maken. Het foutbericht geeft een ongeldige JSON-structuur aan: &quot;Invalid Json. Niet-herkende eigenschapsnaam &#39;content&#39;. Locatie: regel - 1, kolom - 432.&quot; Dit probleem is veroorzaakt door een niet-herkende eigenschap in de payload van het verzoek en is nu opgelost. Klanten kunnen activiteiten opslaan zonder deze fout te ervaren. (TGT-53513)
* **Vaste een kwestie waar de geplande activiteiten verkeerd een [!UICONTROL Live] status tot pagina verfrissen zich**: De klanten merkten op dat wanneer het plannen van een activiteit om op een toekomstige datum en tijd te leven, de status onmiddellijk als [!UICONTROL Live] in plaats van [!UICONTROL Scheduled] verscheen. Dit heeft tot verwarring geleid, hoewel het bevestigingsbericht juist aangeeft dat de activiteit gepland was. De statusweergave is verbeterd door de pagina te vernieuwen. Dit probleem is nu opgelost, en de geplande activiteiten tonen correct de Geplande status zonder te vereisen verfrist zich. (TGT-52937)

+++

**[!UICONTROL Analytics for Target] (A4T)**

+++Zie details
* **Vaste een kwestie waar de klanten geen namen van de rapportreeks tijdens activiteit-creeer proces** konden typen: De klanten die [!DNL Adobe Analytics] als rapporteringsbron tijdens het activiteit-creeer proces gebruiken konden niet in de [!UICONTROL Report Suite] drop-down lijst typen om naar specifieke rapportsuites te zoeken. Dit beïnvloedde werkstromen voor organisaties met grote aantallen rapportreeksen, waar het handscrollen beduidend opstelling vertraagde. De vervolgkeuzelijst is niet alfabetisch geordend en reageerde niet consistent op getypte invoer, waardoor het moeilijk werd om rapportsuites zoals &quot;Office + Store - Web - Prod.&quot; op te zoeken. Dit probleem is opgelost en klanten kunnen nu efficiënt zoeken door namen van rapportsuite te typen. (TGT-53345)

+++

**[!UICONTROL Audiences]**

+++Zie details
* **Vaste een kwestie waar het verlopen &quot;Kader van de Tijd&quot;publiek activiteit blokkeerde opslaan zelfs na verwijdering**: De klanten konden activiteiten in bijgewerkte UI wegens een fout met betrekking tot verlopen &quot;Kader van de Tijd&quot;publiek niet bewaren. Zelfs na het verwijderen van het betrokken publiek bleef het foutbericht bestaan: &quot;Activiteit bevat publiek met een ongeldig tijdkader.&quot; Dit probleem is opgetreden omdat het systeem het alleen-activiteit publiek bleef valideren, zelfs als het niet langer in gebruik was. Het gedrag werd nog gecompliceerd door verschillen in de tijdzone. De validatielogica is gecorrigeerd en klanten kunnen nu activiteiten opslaan zonder deze fout te ondervinden. (TGT-53517)

+++

**[!UICONTROL Experience Fragment]s**

+++Zie details
* **Vaste een kwestie die klanten verhinderde fragmenten van de Ervaring op te nemen gebruikend [!UICONTROL Insert Before] of [!UICONTROL Insert After] in UI** Klanten ontmoetten een fout toen het proberen om [!UICONTROL Experience Fragments] in een activiteit op te nemen gebruikend &quot;Tussenvoegsel vóór&quot;of &quot;Tussenvoegsel na&quot;opties in bijgewerkte UI. Het weergegeven foutbericht was: &quot;De inhoud van het voorstel moet precies één HTML-element bevatten.&quot; Deze kwestie was specifiek voor de bijgewerkte UI en kwam niet voor in de vorige versie. Dit probleem is nu opgelost en klanten kunnen [!UICONTROL Experience Fragments] met succes invoegen zonder deze fout te ondervinden. (TGT-53442)

+++

**[!UICONTROL Offer decisions]**

+++Zie details
* **Vaste een kwestie die klanten verhinderde besluitaanbiedingen uit te geven en specifieke paginaelementen in bijgewerkte UI** te selecteren: In het bijgewerkte activiteit-creeer proces, konden de klanten bestaande besluitaanbiedingen niet uitgeven of specifieke paginaelementen in de Visuele Composer van de Ervaring (VEC) selecteren. Beslissingsvoorstellen zijn onjuist weergegeven als HTML-voorstellen en wijzigingen die tijdens het bewerken zijn aangebracht, zijn niet opgeslagen. Bovendien zijn bepaalde regionale URL&#39;s, zoals de Japan-site, niet correct geladen in VEC, waardoor het maken van activiteiten en updates worden geblokkeerd. Beslissingen worden nu correct weergegeven, pagina-elementen kunnen worden geselecteerd zoals u had verwacht en regionale URL&#39;s worden correct geladen in de VEC, zodat de volledige bewerkingsfunctionaliteit wordt hersteld. (TGT-53425)
* **Vaste een kwestie waar [!UICONTROL Offer Decision] selecteurs niet onverwacht konden worden gewijzigd en worden veranderd na sparen**: In het bijgewerkte activiteit-creeer proces, konden de klanten niet [!UICONTROL Offer Decision] selecteur wijzigen zoals bedoeld. Pogingen om de kiezer te wijzigen zijn mislukt en de kiezer heeft na het opslaan weer een onjuiste waarde ingesteld. Dit gedrag veroorzaakte de besluitaanbieding om uit Visual Experience Composer (VEC) te verdwijnen, die verdere uitgeeft blokkeert. Wijzigingen in kiezers blijven nu op de juiste wijze behouden en aanbiedingen voor beslissingen blijven zichtbaar en kunnen na het opslaan worden bewerkt in de VEC.(TGT-53433)
* **Vaste een kwestie waar [!UICONTROL Offer Decisions] van de activiteit na sparen** verdween: [!UICONTROL Offer Decisions] toegevoegd tijdens het activiteit-creeer proces werd niet bewaard na het bewaren en het heropenen van de activiteit. Dit probleem is opgetreden tijdens het bewerken van dynamische inhoud en het invoegen van [!UICONTROL Offer Decisions] met specifieke kiezers en eigenschappen. [!UICONTROL Offer Decisions] blijft nu correct na het opslaan en de kiezers blijven intact, zodat ze zich consistent kunnen richten en bewerken. (TGT-53434)

+++

**[!DNL Recommendations]**

+++Zie details
* **Vaste kwestie in [!DNL Recommendations] UI waar de download van douanecriteria CSV 404 fout** terugkeerde: Vaste een kwestie waar de klanten de douanecriteria CSV in activiteit-creeer proces niet konden downloaden. De downloadkoppeling werkt nu correct, zodat klanten aangepaste criteria kunnen exporteren zoals verwacht. (TGT-51966)
* **Vaste inconsistente beeld die in[!UICONTROL Catalog Search]** laadt: Vaste een kwestie waar de duimnagels en de beelden in [!UICONTROL &#x200B; Catalog Search] niet constant in activiteit-creeer proces laadden. Afbeeldingen kunnen alleen worden weergegeven als de kolom &quot;URL miniatuur&quot; zichtbaar is en sommige productafbeeldingen geheel of gedeeltelijk zijn geladen na navigatie- of zoekacties. Het gedrag voor het laden van afbeeldingen is gestabiliseerd en de miniaturen worden nu betrouwbaar weergegeven, ongeacht de zichtbaarheid van de kolom of de navigatiehandelingen. (TGT-52778)
* **Vaste een kwestie waar het uitgeven van een aanbeveling in een gedupliceerde ervaring beïnvloedde de originele ervaring**: De klanten rapporteerden dat het wijzigen van een aanbeveling in een gedupliceerde ervaring onbedoeld de originele ervaring veranderde. Na het dupliceren van Experience B in het activity-create proces en het bewerken van het ontwerp of de criteria, werden dezelfde wijzigingen weerspiegeld in de oorspronkelijke Experience B, hoewel ze afzonderlijke entiteiten waren. Bij gedupliceerde ervaringen blijven er nu afzonderlijke configuraties behouden, zodat bewerkingen op één ervaring geen invloed hebben op het origineel. (TGT-53369)
* **Vaste een kwestie waar de veranderingen in een gedupliceerde ervaring onbedoeld de originele ervaring in een activiteit** beïnvloedden: De klanten rapporteerden dat wanneer het dupliceren van een ervaring binnen een activiteit en het toewijzen van een nieuw publiek, om het even welke veranderingen die in het gedupliceerde ontwerp of de criteria van de ervaring werden aangebracht ook in de originele ervaring werden weerspiegeld. Dit probleem is opgetreden, ook al zijn er geen bewerkingen rechtstreeks aangebracht in de oorspronkelijke versie, wat van invloed is op de mogelijkheid om onafhankelijke variaties binnen dezelfde activiteit te maken. Het activity-create proces isoleert nu correct gedupliceerde ervaringen, die ervoor zorgen dat uitgeeft aan één ervaring niet origineel beïnvloedt. (TGT-53361)
* **Vaste een kwestie waar [!UICONTROL Recommendation Catalog] met tussenpozen er niet in slaagde om volledige gegevens van productattributen** te tonen: In bijgewerkte [!DNL Recommendations] UI, ervoeren de klanten een kwestie waar bepaalde productattributen, zoals bericht, niet constant in de [!UICONTROL Catalog Search] resultaten werden getoond, alhoewel de gegevens in het voer bestonden. In dit geval moesten klanten de zichtbaarheid van de kolommen handmatig opnieuw configureren om de ontbrekende waarden op te halen. [!UICONTROL Catalog Search] geeft nu betrouwbaar alle geconfigureerde kenmerken weer, zodat de kolom niet handmatig hoeft opnieuw te worden ingesteld. (TGT-52769)
* **Vaste een kwestie waar a [!UICONTROL Front Promotion] niet in een levende activiteit** kon worden onbruikbaar gemaakt: De pogingen om a [!UICONTROL Front Promotion] in een levende activiteit onbruikbaar te maken werden niet bewaard. Nadat u [!UICONTROL Change Promotion] hebt geselecteerd en uitgeschakeld, is de promotie actief gebleven bij het opnieuw bewerken van de activiteit, zodat updates van aanbevolen configuraties niet meer mogelijk zijn. De montages van de bevordering sparen nu correct, toestaand klanten om bevorderingen in levende activiteiten onbruikbaar te maken of te wijzigen zoals verwacht. (TGT-53231)
* **Vaste een kwestie waar het toelaten van a [!DNL Recommendations] [!UICONTROL Promotion] zonder gegevens een onduidelijk foutenmelding** teweegbracht: Het toelaten van a [!UICONTROL Front] of [!UICONTROL Back Promotion] in een [!DNL Recommendations] activiteit zonder vereiste waarden te specificeren resulteerde in een generisch &quot;Ongeldige inputfout&quot;bericht. De onderliggende kwestie was een ontbrekend configuratiegebied, maar het foutenbericht gaf niet duidelijk de oorzaak aan, die het oplossen van problemen bemoeilijkt. Het activity-create proces geeft nu een duidelijk en actionable foutenmelding wanneer de vereiste gebieden, zoals `collectionId` of regels, ontbreken, die klanten helpen configuratiekwesties snel identificeren en oplossen. (TGT-52616)
* **Vaste een kwestie die [!UICONTROL Product] verhinderde lijst in [!UICONTROL Edit] modaal binnen het [!UICONTROL Recommendations] lusje** te tonen: De klanten konden niet de gefiltreerde productlijst bekijken wanneer het uitgeven van [!UICONTROL collection] of [!UICONTROL exclusion] in [!UICONTROL Recommendations] tabel. Van de lijst werd verwacht dat deze in real time zou worden bijgewerkt op basis van toegepaste regels, maar het werd niet weergegeven zoals bedoeld. Dit probleem is opgelost en de productlijst wordt nu correct weergegeven en wordt dynamisch bijgewerkt naarmate de regels worden gewijzigd. (TGT-53481)
* **Vaste een kwestie met de lay-out van de dialoog van de Details van de Mening in bijgewerkte UI**: De lay-out van het modaal van de Details van de Mening in bijgewerkte UI is gewijzigd om duidelijkheid en bruikbaarheid te verbeteren. Het dialoogvenster bevat nu twee tabbladen:
   * [!UICONTROL Details] tabblad: geeft alle relevante informatie voor het geselecteerde item weer.
   * [!UICONTROL Inventory] tabblad: geeft alle producten weer die zijn gefilterd door de huidige regel voor verzameling en uitsluiting.

  Deze verbetering helpt klanten gemakkelijker te navigeren en item-specifieke gegevens en inventariscontext binnen activiteit-creeert proces te begrijpen. (TGT-53503)

   * **Vaste een kwestie waar verwijderde bevorderingen in aanbevelingsactiviteiten na sparen** opnieuw verschenen: De klanten meldden dat toen [!UICONTROL front] of [!UICONTROL back] bevorderingen van [!DNL Recommendations] activiteiten werden verwijderd en de activiteit werd bewaard, de bevorderingen bij het opnieuw openen bleven verschijnen. Dit probleem trad op in zowel testomgevingen als productieomgevingen en betrof het bijgewerkte proces voor het maken van activiteiten. Het probleem is opgelost. Promoties die uit een activiteit zijn verwijderd, blijven nu correct na het opslaan. (TGT-53490)

+++

**Rapporten**

+++Zie details
* **Vaste een kwestie waar het [!UICONTROL Automated Segments] rapport ongeldige publiekswaarden** toonde: De klanten rapporteerden dat [!UICONTROL Automated Segments] in activiteitenrapporten ongeldig voor publieksgegevens tonen, die nauwkeurige analyse van segmentprestaties verhinderen. Dit probleem is opgetreden tijdens het openen van de sectie [!UICONTROL Reports] en het selecteren van [!UICONTROL Automated Segments] , ook al werden geldige publieksgegevens verwacht. [!UICONTROL Automated Segments] geeft nu correct de publiekswaarden weer, zodat betrouwbare rapportage- en segmentatiedetails worden weergegeven. (TGT-52793)

+++

**de Toepassingen van de Pagina van de Rand (SPAs)**

+++Zie details
* **Vaste een kwestie waar de omschakeling tussen [!UICONTROL Browse] en [!UICONTROL Design] wijzen terugstellen de staat van het KUUROORD in bijgewerkte UI**: De klanten rapporteerden dat het schakelen tussen [!UICONTROL Browse] en [!UICONTROL Design] wijzen in bijgewerkte UI de Webredacteur veroorzaakte om opnieuw te laden, die de staat van SPAs terugstelde. Dit probleem heeft de workflows verstoord en klanten gedwongen om informatie opnieuw in te voeren. Het probleem is opgelost. De staat van het KUUROORD wordt nu bewaard wanneer het schakelen tussen wijzen, die een vlottere en consistentere ervaring tijdens activiteitenverwezenlijking verzekeren. (TGT-53074)

+++

**[!UICONTROL Visual Experience Composer] (VEC)**

+++Zie details
* **Vaste kwestie in activiteit-creeer proces dat vooruitgang aan de [!UICONTROL Targeting] stap in AP activiteiten** blokkeerde: Vaste een kwestie in activiteit-creeert proces waar de klanten niet aan de [!UICONTROL Targeting] stap in [!UICONTROL Automated Personalization] (AP) activiteiten konden te werk gaan tenzij twee plaatsen werden toegevoegd. Dit gedrag verschilde van de vorige ervaring, waar één enkele plaats met veelvoudige aanbiedingen voldoende was. Deze vereiste is gecorrigeerd, zodat klanten de Single-location-instellingen kunnen blijven gebruiken in hun AP-workflows. (TGT-53426)
* **Vaste een kwestie waar het nieuwe activiteit-creeert proces niet de fmt=png-alpha- parameter voor transparante beelden** plaatste: In bijgewerkte UI, worden de beelden opgenomen tijdens het activiteit-creeer proces niet meer inbegrepen de `fmt=png-alpha` parameter door gebrek, resulterend in verlies van transparantie. Dit gedrag verschilde van de vorige UI, die automatisch de parameter aan beeld URLs toevoegde, die transparante achtergronden handhaaft. Tijdens het proces voor het maken van activiteiten wordt de parameter `fmt=png-alpha` nu correct toegepast op afbeeldings-URL&#39;s wanneer transparantie vereist is, zodat transparante elementen consistent worden weergegeven. (TGT-52615)
* **Vaste een kwestie die klanten verhinderde rapportreeksen in bijgewerkte UI** te zoeken: In bijgewerkte UI, [!UICONTROL Report Suites] drop-down lijst in de [!UICONTROL Goals & Settings] sectie stond klanten niet toe om te typen en te zoeken, makend het moeilijk om van specifieke rapportsuites, vooral voor huurders met een groot aantal ingangen de plaats te bepalen. In tegenstelling tot de vorige interface, werd de lijst niet gesorteerd en geen input-based filtreren. Dit probleem is opgelost. Klanten kunnen nu typen om te zoeken naar en te filteren op rapportreeksen, waarbij de functionaliteit wordt hersteld die beschikbaar is in de oudere gebruikersinterface. (TGT-53514)

+++

**[!UICONTROL Workspaces]**

+++Zie details
* **Vaste een kwestie waar een klant tot één enkele werkruimte beperkt activiteiten van andere werkruimten** kon bekijken: De klanten met toegang die tot één werkruimte wordt beperkt waren onverwacht in staat om activiteiten over alle werkruimten te bekijken wanneer het selecteren [!UICONTROL All Workspaces] in activiteit-creeer proces. Deze zichtbaarheid vormde een risico op onbedoelde wijzigingen in de live activiteiten in andere werkruimten, hetgeen mogelijk van invloed was op de prestaties van de website. De toegangscontroles van Workspace zijn versterkt om ervoor te zorgen dat klanten slechts activiteiten binnen hun toegewezen werkruimte kunnen bekijken en met elkaar in wisselwerking staan. (TGT-53101)
* **Vaste een kwestie waar een klant activiteiten van [!UICONTROL Default Workspace] kon bekijken zonder toegang te hebben:** een klant met toegang die tot de het opvoeren werkruimte wordt beperkt kon activiteiten van [!UICONTROL Default Workspace] bekijken via het activiteit-creeer proces. Dit gedrag kwam ondanks correcte achtergrondconfiguratie en toegangsrechten voor. De toegangscontroles van Workspace zijn versterkt om ervoor te zorgen dat klanten activiteiten slechts binnen hun toegewezen werkruimte kunnen bekijken.(TGT-53297)

+++

## [!DNL Target Standard/Premium] 25.8.2 (14 augustus 2025)

Deze release bevat de volgende correcties en updates:

**[!UICONTROL Activities]**

+++Zie details
* **Vaste activiteit-ladende kwestie in bijgewerkte [!DNL Target] UI**: Oplossing een kwestie in bijgewerkte [!DNL Target] UI waar bepaalde activiteiten er niet in slaagden toen het proberen uit te geven. Dit probleem heeft ertoe geleid dat klanten gebruikers in een onbepaald laadscherm hebben verlaten. Deze kwestie had gevolgen voor meerdere activiteiten en zou onsamenhangend zijn voor alle klanten. Met deze oplossing worden de betrokken activiteiten nu correct geladen, zodat ze naadloos kunnen worden bewerkt en de workflows met activiteiten minder worden verstoord. (TGT-53209)
* **Vaste sparen fout in activiteit-creeer proces toe te schrijven aan `optionLocalId` bevestiging**: Vaste een kwestie in het activiteit-creeer proces dat klanten verhinderde veranderingen toe te schrijven aan een fout van de achterste plaatsbevestiging: `OptionLocalIdReferentialIntegrity.ABActivity - Invalid optionLocalIds:` Deze kwestie kwam voor wanneer het wijzigen van specifieke elementen binnen een activiteit, resulterend in ontbroken sparen verrichting. De oplossing zorgt ervoor dat `optionLocalId` -verwijzingen nu correct worden gevalideerd, zodat klanten activiteiten kunnen opslaan zonder deze fout te ondervinden. (TGT-53293)
* **Vaste neerstorting in activiteit-creeer proces dat door ongeldige optieverwijzingen wordt veroorzaakt wanneer het schakelen van pagina&#39;s**: Vaste een kwestie in het activiteit-creeer proces dat UI veroorzaakte om na het schakelen van pagina&#39;s drie keer tijdens het uitgeven te crashen. Het neerstorten werd teweeggebracht door ongeldige optieverwijzingen, resulterend in consolefouten zoals &quot;Optie met localId &quot;7&quot;niet gevonden.&quot; Met deze update kunnen klanten nu schakelen tussen pagina&#39;s en wijzigingen toepassen zonder systeemfouten of onderbrekingen te ondervinden. (TGT-53295)
* **Vaste sparen fout in activiteit-creeer proces dat door ongeldige gebruikersinput wordt veroorzaakt wanneer het uitgeven van ervaringen**: Vaste een kwestie in het activiteit-creeer proces waar de klanten veranderingen in een activiteit niet konden bewaren toe te schrijven aan een ongeldige fout van de gebruikersinput. De fout kwam bij het wijzigen van ervaringen in bijgewerkte UI voor, die updates verhinderen worden begaan. De activiteit kan nu met succes worden bewaard, toestaand klanten om zonder onderbreking uit te geven en te publiceren. (TGT-53267)
* **Vaste ladingskwestie in activiteit-creeer proces dat het blokkeerde uitgeven in bijgewerkte UI**: Vaste een kwestie in activiteit-creeert proces waar de klanten geen activiteiten in bijgewerkte UI wegens een ononderbroken ladingsscherm konden uitgeven. Klanten kunnen nu activiteiten openen en wijzigen zonder dat er problemen optreden bij het laden. (TGT-53415)
* **Vaste kwestie van het ervaringsvereiste in activiteit-creeer proces voor AP activiteiten in bijgewerkte UI**: Vaste een kwestie in activiteit-creeer proces waar [!UICONTROL Automated Personalization] (AP) activiteiten twee plaatsen in plaats van twee ervaringen in bijgewerkte UI vereiste. Door dit gedrag werden gebruiksgevallen geblokkeerd waarbij klanten één locatie met meerdere aanbiedingen configureren, hetgeen eerder werd ondersteund. Het vereiste is gecorrigeerd om de originele functionaliteit aan te passen, die klanten toestaat om met AP activiteiten te werk te gaan gebruikend twee ervaringen ongeacht plaatstelstelling. (TGT-53429)
* **Vast gevolgd gedrag van het elementengebied op de wijze van het Spoor van de Klik om niet bewaarde input te verhinderen en duidelijkheid** te verbeteren: Vaste een kwestie in activiteit-creeert proces waar het [!UICONTROL Tracked Element] gebied op [!DNL Click Track] wijze editable was maar niet de ingegaan naam bewaarde, veroorzakend verwarring voor klanten. Het veld is nu uitgeschakeld om niet-opgeslagen invoer te voorkomen en de naamgeving van geselecteerde elementen is verduidelijkt om de doelconfiguratie en de nauwkeurigheid van het bijhouden van gegevens te verbeteren.** (TGT-53458)
* **Vaste kwestie in activiteit-creeer proces dat het blokkeren van het noemen van gevolgde componenten op [!UICONTROL Click Track] wijze**: Vaste een kwestie in activiteit-creeert proces waar de klanten niet bijgehouden componenten op [!UICONTROL Click Track] wijze konden noemen. Nadat u een naam hebt ingevoerd, is het veld bewerkbaar weergegeven, maar heeft het de invoer niet behouden. Standaard worden generieke labels zoals &quot;MY PRIMARY GOAL 0&quot; in de bewerkingsmodus gebruikt. Het bijgehouden elementveld is nu uitgeschakeld en het gedrag voor naamgeving is verduidelijkt om de doelinstelling en -volgnauwkeurigheid te verbeteren. (TGT-51396)

+++

**Fragmenten van de Ervaring (XFs)**

+++Zie details
* **Vaste kwestie in activiteit-creeer proces dat onbedoelde het uitgeven van HTML van AEM-Uitgevoerde fragmenten** toeliet: Vaste een kwestie in activiteit-creeer proces dat klanten toeliet om HTML van [!DNL Experience Fragments] (XFs) uit [!DNL Adobe Experience Manager] (AEM) binnen uit te geven [!DNL Target]. Dit gedrag was onbedoeld, aangezien XFs voor het uitgeven zou moeten gesloten blijven zodra gepubliceerd van AEM. De oplossing zorgt ervoor dat de optie HTML bewerken niet langer beschikbaar is voor AEM-geëxporteerde fragmenten, zodat de integriteit van de inhoud en het verwachte beheer behouden blijven. (TGT-53286)
* **Vaste intermitterende voorproefkwestie voor inhoud XF in activiteit-creeer proces binnen bijgewerkte UI**: Vaste een kwestie in het activiteit-creeer proces waar de inhoud XF periodiek om op voorproefwijze binnen bijgewerkte UI te teruggeven ontbrak. Hoewel de inhoud correct is geleverd, is de voorvertoning niet consistent weergegeven, waardoor het voor klanten moeilijk is om de setup van de aanbieding te valideren. XF-voorvertoningen worden nu betrouwbaar geladen, waardoor het vertrouwen en de efficiëntie tijdens de activiteitenconfiguratie worden verbeterd. (TGT-53318)

+++

**wijze QA**

+++Zie details
* **Vaste kwestie in activiteit-creeer proces waar de belangrijke ruimten in URLs gebroken verbindingen QA** veroorzaakte: Vaste een kwestie in activiteit-creeer proces waar de belangrijke ruimten in de activiteit URL niet behoorlijk werden bijgesneden toen het bewaren. Dit veroorzaakte ongeldige verbindingen QA en onjuiste formatteren in het achterste eind. Na de update, worden URLs nu bewaard zuiverder, verhinderend gebroken verbindingen en verbeterend de betrouwbaarheid van QA werkschema&#39;s voor klanten. (TGT-53427)

+++

**[!UICONTROL Recommendations]**

+++Zie details
* **Vaste kwestie in catalogusonderzoek UI waar het geavanceerde onderzoek er niet in slaagde om suggesties** te verstrekken: Oplossing een kwestie in nieuwe [!UICONTROL Catalog Search] UI waar de [!UICONTROL Advanced Search] eigenschap geen suggesties kon verstrekken. De gebruikers werden vereist om nauwkeurige waarden met nauwkeurige spelling in te voeren, die de onderzoekservaring omslachtig en fout-gevoelig maken. Met deze oplossing biedt [!UICONTROL Advanced Search] nu relevante suggesties zoals gebruikers typen, die bruikbaarheid verbeteren en wrijving bij het zoeken naar producten verminderen. (TGT-52008)
* **lost veelvoudige UI en het filtreren kwesties op om ontvankelijkheid en entiteitinteractie te verbeteren**: Oplossing verscheidene kwesties, met inbegrip van slechte ontvankelijkheid van criteria details op klein-schermapparaten, gebrek aan resultaten wanneer het selecteren van &quot;Alle gastheergroepen&quot;in de filter van het Milieu, en onvermogen om met entiteiten op te treden die geen naam hebben. Deze correcties verbeteren de bruikbaarheid in verschillende schermgrootten, zorgen voor nauwkeurige filtering en maken volledige interactie met alle productentiteiten mogelijk, waardoor de algemene gebruikerservaring wordt verbeterd. (TGT-52992)
* **Vaste ontbrekende product IDs in de gedetailleerde mening van Aanbevelingen tijdens activiteitenverwezenlijking**: Vaste een kwestie in [!DNL Recommendations] activiteit-creeer proces waar product IDs van het scherm van het productdetail mist, die het voor klanten moeilijk maken om product IDs tijdens werkschema&#39;s te kopiëren of van verwijzingen te voorzien. De product-id&#39;s worden nu duidelijk weergegeven in de gedetailleerde weergave, waardoor de zichtbaarheid wordt verbeterd en een efficiënter productbeheer voor klanten wordt ondersteund. (TGT-51964)
* **Vaste kwestie in activiteit-creeer proces waar de productberichten om in aanbevelingen mening** ontbraken te tonen: Vaste een kwestie in het activiteit-creeer proces waar de [!UICONTROL Message] kolom in de [!DNL Recommendations] mening productgegevens niet vertoonde, alhoewel de berichten aanwezig waren. Klanten moesten de kolom handmatig verwijderen en opnieuw toevoegen om de inhoud tijdelijk weer te geven. Deze verdwijnt vaak weer wanneer ze schuiven of zoeken. Deze update herstelt consistente zichtbaarheid van productberichten, waardoor de workflows voor catalogusnavigatie en -revisie worden verbeterd. (TGT-52777)
* **Vaste kwestie in activiteit-creeer proces waar het selecteren van &quot;Alle gastheergroepen&quot;geen resultaten in aanbevelingen terugkeerde mening**: Vaste een kwestie in activiteit-creeer proces waar het selecteren van het &quot;Alle gastheergroepenmilieu in de [!DNL Recommendations] mening geen resultaten terugkeerde. Klanten kunnen productgegevens nu op alle hostgroepen weergeven zoals verwacht, waardoor de zichtbaarheid en filternauwkeurigheid tijdens het instellen van de activiteit worden verbeterd. (TGT-53006)
* **Vaste kwestie in activiteit-creeer proces waar de voorpromotieknevel niet na sparen** voorthield: Vaste een kwestie in het activiteit-creeer proces waar het onbruikbaar maken van de voorbevorderingsknevel in activiteitenmontages niet na besparing voorhield. Klanten die probeerden de frontbevordering te verwijderen, vonden de knevel opnieuw-toegelaten na het herzien van de activiteit, die correcte aanpassing verhinderden. Met deze update kunnen wijzigingen op betrouwbare wijze worden opgeslagen, zodat klanten de volledige controle hebben over instellingen voor speciale acties. (TGT-53215)
* **Vaste inconsistente sortering door [!UICONTROL Last Updated] kolom:** Vaste een kwestie in activiteit-creeer proces waar het sorteren van de catalogus door de [!UICONTROL Last updated] kolom inconsistente resultaten produceerde. Klanten konden productgegevens niet betrouwbaar organiseren op basis van updatetijdstempels, waardoor het reviseren en beheren van catalogi moeilijker werd. Sorteren werkt nu zoals verwacht, waardoor de nauwkeurigheid en bruikbaarheid in de bijgewerkte gebruikersinterface worden verbeterd. (TGT-53116)

+++

**Visuele Composer van de Ervaring (VEC)**

+++Zie details
* **Vaste activiteit ladend en [!UICONTROL Cancel] knoopkwesties in activiteit-creeer proces**: Vaste een kwestie in activiteit-creeer proces waar bepaalde activiteiten er niet in slaagden, verlatend klanten niet tot wijzigingen kunnen toegang hebben. Bovendien reageerde de knop [!UICONTROL Cancel] niet, waardoor klanten het laadproces niet konden stoppen of de bewerkingsweergave konden verlaten. Deze correctie zorgt ervoor dat activiteiten nu betrouwbaar worden geladen en dat de knop [!UICONTROL Cancel] naar behoren functioneert, wat de algehele stabiliteit en gebruikerservaring in de Visual Experience Composer verbetert. (VEC)(TGT-53218)
* **Vaste kwestie van de ervaringsomschakeling in bijgewerkte VEC UI die het uitgeven en gehandicapten [!UICONTROL Cancel] knoop** blokkeerde: Vaste een kwestie in bijgewerkte VEC UI waar de wijzigingen ontbraken om te laden wanneer het schakelen tussen ervaringen in een Ervaring richtend (XT) activiteit. Klanten konden de ervaringen die ze oorspronkelijk hadden ingevoerd, niet bewerken en de knop [!UICONTROL Cancel] ontbreekt of reageert niet. Deze correctie zorgt ervoor dat wijzigingen nu correct worden geladen over alle ervaringen en dat de knop [!UICONTROL Cancel] betrouwbaar werkt, zelfs zonder de Helper-extensie, waardoor bewerkingsworkflows worden verbeterd en frustratie wordt verminderd. (TGT-53256)
* **Vaste witte het schermkwestie wanneer het schakelen tussen veelvoudige ervaringen in activiteit-creeer proces**: Vaste een kwestie waar het schakelen tussen veelvoudige ervaringen een wit scherm veroorzaakte. Probleem verholpen tijdens het &#39;activity-create&#39;-proces waarbij klanten een wit scherm tegenkwamen bij het wijzigen van meerdere ervaringen binnen een activiteit. Dit probleem is opgetreden nadat u wijzigingen hebt aangebracht in twee ervaringen en vervolgens een derde ervaring hebt gekozen, waardoor verdere bewerkingen zijn voorkomen. De update zorgt voor vloeiende overgangen tussen ervaringen, waardoor klanten zonder onderbreking wijzigingen kunnen aanbrengen. (TGT-53266)
* **Vaste kwestie in VEC waar de veranderingen van de douanecode niet betrouwbaar over het uitgeven zittingen** werden bewaard: Vaste een kwestie waar de wijzigingen van de douanecode die in Visuele Composer van de Ervaring (VEC) werden aangebracht niet betrouwbaar in één enkele poging werden bewaard. Klanten meldden dat wijzigingen, zoals styling updates of HTML-bewerking, periodiek ontbraken van de website en QA-URL&#39;s, zelfs nadat ze zowel de [!UICONTROL Edit Content] - als de laatste [!UICONTROL Save] -knoppen hadden gebruikt. Deze regressie is opgelost, zodat alle wijzigingen in de aangepaste code tijdens de bewerkingssessies ongewijzigd blijven.** (TGT-53418)
* **Vaste ontbrekende `triggerViews` in bijgewerkte UI tijdens activiteitenverwezenlijking**: Vaste een kwestie in activiteit-creeer proces waar `triggerViews` niet in bijgewerkte UI verscheen, alhoewel zij correct werden uitgevoerd op de pagina. Dit beïnvloedde veelvoudige klanten en maakte het moeilijk om op mening-gebaseerde trekkers tijdens activiteitenopstelling te bevestigen. `TriggerViews` wordt nu naar behoren weergegeven, zodat klanten hun configuraties op betrouwbare wijze kunnen voltooien en testen. (TGT-53239)
* **Vaste mening-ladende kwestie in activiteit-creeer proces voor specifieke webpagina&#39;s in bijgewerkte UI**: Vaste een kwestie in het activiteit-creeer proces waar de meningen niet in bijgewerkte UI voor specifieke webpagina&#39;s geladen, ondanks correct uitgevoerd en zichtbaar in levering of interactie vraag. Dit beïnvloedde veelvoudige klanten en maakte het moeilijk om op mening-gebaseerde het richten te bevestigen. Weergaven worden nu consistent op alle ondersteunde pagina&#39;s weergegeven, wat de betrouwbaarheid tijdens het instellen van de activiteit verbetert. (TGT-53246)
* **Vaste intermitterende mening ladende kwestie in activiteit-creeer proces in bijgewerkte UI**: Vaste een kwestie in activiteit-creeer proces waar de meningen periodiek om in bijgewerkte UI tijdens activiteit het uitgeven ontbraken te verschijnen. Hoewel de correcte meningsnaam in de netwerklading aanwezig was, werd het niet constant erkend in de interface, die klanten&#39; vermogen beïnvloedt om op mening-gebaseerde verpersoonlijking te vormen. Weergaven worden nu betrouwbaar weergegeven en ondersteunen naadloze workflows voor installatie en validatie. (TGT-53223)
* **Vaste kwestie in activiteit-creeer proces waar de gevolgde actienamen niet in bijgewerkte UI** werden bewaard: Vaste een kwestie in het activiteit-creeer proces waar de gevolgde actiemetriek niet in bijgewerkte UI kon worden bewaard. Na het noemen van een gevolgd element en het bewaren van de activiteit, zou de naam aan een standaardetiket terugstellen wanneer opnieuw geopend, veroorzakend verwarring en ontwrichtend doelconfiguratie. De bijgehouden acties behouden nu hun toegewezen namen, waardoor klanten conversiemetriek nauwkeurig kunnen instellen en beheren. (TGT-53453)

+++

## [!DNL Target Standard/Premium] 25.8.1 (7 augustus 2025)

Deze release bevat de volgende verbeteringen en oplossingen:

**Activiteiten**

+++Zie details
* Oplossing voor verschillende problemen met de bijgewerkte interface, waaronder fouten bij het verwijderen van paginatypen als gevolg van de afstand in invoerwaarden, onbetrouwbare kopiëren van activiteiten tussen werkruimten en slecht functionerende regels voor het leveren van pagina&#39;s in QA-omgevingen. (TGT-52703)
* Probleem verholpen in de bijgewerkte gebruikersinterface van [!DNL Target] waar gebruikers met de [!UICONTROL Editor] -rol live activiteiten konden openen en proberen te bewerken. Dit probleem moet worden beperkt. De activiteitenlijst en overzichtsschermen onjuist weergegeven bewerkingsopties voor live activiteiten, wat tot mogelijk onbedoelde wijzigingen leidt. (TGT-53055)
* Probleem verholpen waarbij het selecteren van de operatoren &quot;value is present&quot; of &quot;value is not present&quot; in de gebruikersinterface van [!UICONTROL Advanced Search] ertoe leidde dat gebruikers een operand wilden invoeren die niet vereist was voor deze voorwaarden. (TGT-51961)
* Probleem verholpen in de bijgewerkte gebruikersinterface waarbij pogingen om activiteiten van de werkruimte van de testfase naar de productiewerkruimte consistent te kopiëren, zelfs in sandboxomgevingen, zijn mislukt. De klanten ontmoetten diverse foutenmeldingen, met inbegrip van &quot;Anoniem publiek dat reeds door de activiteit&quot;en &quot;Ongeldige publiek identiteitskaart,&quot;ondanks het gebruiken van geldige configuraties en het hebben van aangewezen werkruimtemachtigingen wordt gebruikt. (TGT-52394)

+++

**Fragmenten van de Ervaring (XFs)**

+++Zie details
* Probleem verholpen waarbij XF-inhoud (Experience Fragment) niet wordt gerenderd in de voorvertoning [!UICONTROL Visual Experience Composer] (VEC), ondanks het correct werken in de levering van inhoud. (TGT-53318)

+++

**Localization**

+++Zie details
* Probleem met lokalisatie verholpen waarbij de knop &quot;Promotie toevoegen&quot; in de sectie &quot;Promoties&quot; niet gelokaliseerd leek voor meerdere taalomgevingen in de QA-gebruiker. (TGT-53263)

+++

**Aanbiedingen**

+++Zie details
* Probleem verholpen waarbij tijdens het bewerken van een bestaand HTML-aanbod via Visual Experience Composer (VEC) alle wijzigingen werden verwijderd uit de levering van inhoud. De wijzigingen worden grijs weergegeven op het tabblad Wijzigen en worden niet weerspiegeld in QA-voorvertoningen, ondanks dat ze correct worden toegepast in de oudere gebruikersinterface. (TGT-52863)
* Probleem verholpen in de bijgewerkte gebruikersinterface van [!DNL Target] , waarbij HTML wijzigingen aanbiedt die in [!UICONTROL Visual Experience Composer] (VEC) zijn aangebracht, maar niet meer voorkomen nadat u van de tab [!UICONTROL Targeting] terug naar [!UICONTROL Experiences] bent genavigeerd. (TGT-52874)
* Probleem verholpen in de bijgewerkte gebruikersinterface van [!DNL Target] waarbij het invoegen van één HTML-aanbieding voor en een ander na dezelfde kiezer tot onjuiste locatiegeneratie leidde. Wanneer klanten van het tabblad [!UICONTROL Targeting] naar het tabblad [!UICONTROL Experience] zijn teruggekeerd, is slechts één kiezer behouden gebleven, wat heeft geleid tot verloren wijzigingen en een verbroken levering van inhoud. Dit gedrag verschilde van erfenis UI, die correct beide wijzigingen met verschillende plaatsherkenningstekens handhaaft. (TGT-52891)
* Probleem verholpen in de bijgewerkte gebruikersinterface van [!DNL Target] , waarbij het klikken op een toegevoegde aanbieding in de [!UICONTROL Modifications] rail ertoe leidde dat het rechterdeelvenster [!UICONTROL Configuration] af en toe werd weergegeven en verdwijnt, waardoor interactie met de aanbiedingsinstellingen moeilijk werd. (TGT-53288)
* Probleem verholpen waarbij HTML-aanbiedingen die binnen een activiteit aan publiekspecifieke variaties zijn toegevoegd, niet consistent werden opgeslagen of in de wijzigingssectie werden weergegeven. Nadat tijdens het bewerken is geschakeld tussen het publiek, zijn eerder toegepaste aanbiedingen soms verdwenen of zijn ze niet weergegeven, waardoor de validatie wordt verstoord en de gereedheid van de activiteit wordt vertraagd. (TGT-53440)
* Probleem verholpen waarbij door het kopiëren van een activiteit die aanbiedingen bevatte, dubbele aanbiedingen werden gemaakt in de nieuwe activiteit. Dit gedrag veroorzaakte onnodige verwarring en verwarring, vooral wanneer het bewegen van activiteiten tussen werkruimten. De oplossing zorgt ervoor dat [!DNL Target] -aanbiedingen nu correct en zonder duplicatie naar de doelwerkruimte worden gekopieerd, zodat het activiteitsbeheer wordt gestroomlijnd en de efficiëntie van de workflow wordt verbeterd. (TGT-53454)

+++

**Enige Toepassingen van de Pagina (SPAs)**

+++Zie details
* Oplossing voor een probleem in de bijgewerkte VEC dat ervoor zorgde dat klanten geen wijzigingen konden toepassen op [!UICONTROL Single Page Application] (SPA)-weergaven. Terwijl de activiteiten die in oude UI werden gecreeerd mening-specifiek het richten steunden, nieuwe UI niet om te ontdekken of toe te staan uitgeeft aan die meningen, met de mening-omschakeling controles die gehandicapt lijken. (TGT-52556)

+++

**Visuele Composer van de Ervaring (VEC)**

+++Zie details
* Correctie van een probleem waarbij wijzigingen in ervaringen binnen [!UICONTROL Visual Experience Composer] niet zichtbaar waren of inconsistent optraden in de gebruikersinterface. (TGT-TGT-53381)
* Probleem verholpen in de bijgewerkte VEC waarbij de sectie [!UICONTROL Manage Content] geen alternatieve tekst kon weergeven voor ervaringsminiaturen. Hierdoor konden gebruikers documenten moeilijk herkennen, vooral als bestandsnamen lang of ingekort waren. (TGT-52291)
* Probleem verholpen waarbij klanten onjuiste validatiefouten tegenkwamen bij het configureren van [!UICONTROL page delivery] -regels in VEC-activiteiten. Operatoren als &quot;is gelijk aan een van de items&quot; en &quot;is niet gelijk aan een van de items&quot; die worden geactiveerd &quot;Ongeldige invoer voor het operatortype&quot; bij het invoeren van tekstwaarden, ook al moet tekst worden ondersteund. (TGT-52629)
* Oplossing voor verschillende problemen die een inconsistent gedrag veroorzaakten in het deelvenster [!UICONTROL Modifications] van de bijgewerkte gebruikersinterface bij het selecteren van aanbiedingen met de knop &quot;Een aanbieding selecteren&quot;. In plaats van de bestaande aanbieding te vervangen, heeft de gebruikersinterface een duplicaat toegevoegd en geprobeerd om met een van beide aanbiedingen te communiceren, heeft dit geleid tot consolefouten zoals `selectorNotFound` . Bovendien wordt in sommige aanbiedingen de knop &quot;Een aanbieding selecteren&quot; niet weergegeven en worden alleen bewerkbare eigenschappen weergegeven. (TGT-53321)
* Probleem verholpen in de bijgewerkte gebruikersinterface van [!DNL Target] waarbij wijzigingen in de HTML-code die tijdens het instellen van de activiteit zijn aangebracht, niet meer voorkomen op variatiepagina&#39;s, ook al zijn deze op de juiste wijze opgeslagen voor controlegroepen. Ondanks meerdere pogingen en het opnieuw maken van tests zonder paginagroepen, konden de variatiepagina&#39;s voortdurend geen wijzigingen behouden, wat invloed had op de levering van inhoud en de validatie van de kwaliteitscontrole. (TGT-53436)
* Probleem verholpen in de bijgewerkte VEC waarbij de operator &quot;equals of&quot; in de leveringsregels voor pagina&#39;s geen invoerwaarden accepteerde. Wanneer het vormen van klantenparameters over alle dozen, resulteerde het selecteren van deze exploitant in een &quot;Ongeldige Input&quot;fout, verhinderend regelverwezenlijking. (TGT-52623)

+++

**Werkruimten**

+++Zie details
* Verbeterde workflow bij het kopiëren van activiteiten tussen werkruimten. De activiteiten van het exemplaar tussen werkruimten leidden eerder tot synchronisatiefouten toe te schrijven aan ontbrekend publiek en niet toegewezen eigenschappen. Deze update introduceert een slimmere, intuïtievere workflow die ervoor zorgt dat gekopieerde activiteiten correct zijn geconfigureerd en klaar zijn voor publicatie. (TGT-47094)
* Probleem verholpen waarbij klanten geen activiteiten konden kopiëren tussen werkruimten vanwege een fout in de mutatie `copyActivityBatchOperations` . Pogingen om activiteiten te dupliceren resulteerden in een serverfout (500) en een lege antwoordlading. (TGT-52405)
* Probleem verholpen waarbij activiteiten niet konden worden gesynchroniseerd wanneer aanbiedingen waarnaar in de configuratie wordt verwezen niet toegankelijk waren binnen de geselecteerde werkruimte. Hierdoor zijn publicatiefouten en linkactiviteiten mislukt. (TGT-52535)
* Meerdere problemen verholpen tijdens het kopiëren van activiteiten tussen werkruimten in de bijgewerkte gebruikersinterface van [!DNL Target] . De klanten ontmoetten fouten met betrekking tot publiekstoegang, met name met levende activiteiten, en onjuiste voorrechtbevestiging, zelfs wanneer de gebruiker &quot;[!UICONTROL Approver]&quot;rollen in zowel bron als bestemmingswerkruimten had. (TGT-53002)
* Probleem verholpen in de bijgewerkte gebruikersinterface waarbij het kopiëren van activiteiten binnen dezelfde werkruimte nodeloos gekoppelde aanbiedingen en soorten publiek dupliceerde. (TGT-53457)
* Probleem verholpen waarbij ad-hocpubliek (anoniem) niet correct werd gekopieerd tussen niet-standaardwerkruimten of van niet-standaard naar standaardwerkruimten. Terwijl de vroegere updates correcte duplicatie voor gebrek-aan-niet gebrek en zelfde-werkruimtescenario&#39;s zorgden, concentreerde deze verbetering zich op het bewaren van gecombineerde publieksconfiguraties die veelvoudige werkruimten overspannen. Deze oplossing zorgt voor consistent gedrag van het publiek en een nauwkeurige afstemming op alle overgangen in de werkruimte. (TGT-53268)

+++

## Aanvullende opmerkingen bij de release en versiedetails

| Bron | Details |
|--- |--- |
| [ de nota&#39;s van de Versie: De Ervaring van het Platform van Adobe Target Web SDK ](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=nl-NL) | Details over veranderingen in elke versie van het Web SDK van het Platform. |
| [ at.js versiedetails ](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html?lang=nl-NL){target=_blank} | Informatie over de wijzigingen in elke versie van de JavaScript-bibliotheek [!DNL Adobe Target] at.js. |

## Documentatiewijzigingen, Opmerkingen bij de vorige release en Opmerkingen bij de release van Experience Cloud

Naast de notities voor elke release bevatten de volgende bronnen aanvullende informatie:

| Bron | Details |
|--- |--- |
| [ Veranderingen van de Documentatie ](/help/main/r-release-notes/doc-change.md) | Gedetailleerde informatie weergeven over updates van deze handleiding die niet zijn opgenomen in deze releaseopmerkingen. |
| [ de nota&#39;s van de Versie voor vorige versies ](/help/main/r-release-notes/release-notes-for-previous-releases.md). | Informatie weergeven over nieuwe functies en verbeteringen in vorige versies van Target Standard en Target Premium. |
| [ de Nota&#39;s van de Versie van Adobe Experience Cloud ](https://experienceleague.adobe.com/docs/release-notes/experience-cloud/current.html?lang=nl-NL){target=_blank} | Bekijk de nieuwste releaseopmerkingen voor de Adobe Experience Cloud-oplossingen. |

## Prerelease-informatie {#section_5D588F0415A2435B851A4D0113ACA3A0}

De volgende middelen laten u zien wat in de volgende versie van het Doel komt.

| Bron | Details |
|--- |--- |
| [ de Prioritaire Update van het Product van Adobe ](https://www.adobe.com/subscription/priority-product-update.html){target=_blank} | Ontvang voorafgaande meldingen over aanstaande productverbeteringen voor [!DNL Target] en andere [!DNL Adobe Experience Cloud] -oplossingen. |
| [ de Nota&#39;s van de Versie van het Doel - preRelease ](/help/main/r-release-notes/target-release-notes.md){target=_blank} | Informatie over de versies van het Doel van de huidige maand, met inbegrip van pre-releaseinformatie. |
