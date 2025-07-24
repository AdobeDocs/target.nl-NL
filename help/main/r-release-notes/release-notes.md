---
keywords: releaseopmerkingen;nieuwe functies;releases;updates;update;release;verbetering;verbeteringen;correcties;foutoplossingen;updates;huidige updates
description: Leer over de nieuwe eigenschappen, de verhogingen, en de moeilijke situaties inbegrepen in de huidige versie van  [!DNL Adobe Target], met inbegrip van SDKs, APIs, en de bibliotheken van JavaScript.
landing-page-description: Leer over de nieuwe eigenschappen, de verhogingen, en de moeilijke situaties inbegrepen in de huidige versie van  [!DNL Adobe Target].
short-description: Leer over de nieuwe eigenschappen, de verhogingen, en de moeilijke situaties inbegrepen in de huidige versie van  [!DNL Adobe Target].
title: Wat is inbegrepen in de huidige Versie?
feature: Release Notes
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
source-git-commit: 265108dbb0a459e1b111fda01a35042170f05562
workflow-type: tm+mt
source-wordcount: '4383'
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

## [!DNL Target Standard/Premium] 25.7.3 (24 juli 2025)

Vanwege recente problemen die zijn vastgesteld en die voornamelijk verband houden met complexe klantaanpassingen, bevat deze release de volgende oplossingen en updates:

**Activiteiten**

+++Zie details
* Probleem verholpen waarbij de methode `buildViews` in de klasse builder `viewMaxLocalId` onjuist instelde op het totale aantal weergaven in plaats van op het hoogste toegewezen `viewLocalId` . (TGT-53207)
* Correctie van een probleem in de bijgewerkte gebruikersinterface van [!DNL Target] waarbij verwijderde aanbiedingen in [!UICONTROL Automated Personalization] (AP)-activiteiten werden weergegeven als `Deleted option with ID: X` in plaats van als de oorspronkelijke namen (bijvoorbeeld `Offer Name [Deleted]` zoals weergegeven in de oudere gebruikersinterface). Met deze oplossing herstelt u betekenisvolle etikettering voor verwijderde aanbiedingen, waardoor de duidelijkheid wordt verbeterd en de rapportage nauwkeuriger en gebruiksvriendelijker wordt. (TGT-52921)
* Probleem verholpen waarbij bepaalde activiteiten die van [!DNL Target] frontend naar [!DNL Target] Central werden gemigreerd inconsistente metrische configuraties hadden als gevolg van een eerder opgeloste synchronisatiefout. Specifiek, behielden de activiteiten die oorspronkelijk een omzettingsmetrisch gebruikten en later aan analytisch-gebaseerde metrisch werden bijgewerkt achterhaalde waarden op `primaryMetricType` en `successCriteria` gebieden. (TGT-52643)
* Probleem verholpen waarbij de volledige inhoud van een voorvertoningspagina voor kwaliteitscontrole bewerkbaar werd vanwege de onbedoelde opname van het kenmerk `contentEditable` in HTML-wijzigingen. Hierdoor konden gebruikers op tekst op de pagina klikken en deze bewerken, waardoor layoutproblemen en verwarring tijdens kwaliteitscontrole konden ontstaan. (TGT-53247)
* Probleem verholpen waarbij het verplaatsen van een wijziging van [!DNL Page Load] naar een [!UICONTROL View] ertoe leidde dat de wijziging werd gedupliceerd, en dat deze in [!UICONTROL Page Load] bleef terwijl deze ook in de [!UICONTROL View] werd weergegeven. Bovendien, zou het verwijderen van de wijziging uit [!UICONTROL View] het verkeerd ook verwijderen uit [!UICONTROL Page Load]. (TGT-53270)

+++

**APIs**

+++Zie details
* Probleem verholpen in de achtergrondpersistentielaag waarbij verwijderde opties correct waren opgeslagen, maar niet toegankelijk waren via bestaande API-eindpunten. Dientengevolge, konden de frontend toepassingen geen zinvolle namen voor geschrapte opties terugwinnen, die historische rapporteringsmeningen beïnvloeden. Met deze correctie wordt ervoor gezorgd dat behouden verwijderde optiegegevens nu op de juiste wijze kunnen worden weergegeven in de gebruikersinterface. (TGT-52973)
* Een nieuw migratieeindpunt geïmplementeerd ter ondersteuning van de overdracht van opties voor verwijderde activiteit van op JCR gebaseerde activiteiten naar [!DNL Target] Central. Deze functionaliteit maakt consistente tracering en rapportage mogelijk voor alle systemen. Met deze functie zorgt u ervoor dat verwijderde opties behouden blijven en gesynchroniseerd blijven op de voorzijde en achterzijde van [!DNL Target] , waardoor de historische rapportage en gegevensintegriteit worden verbeterd. (TGT-53217)
* Introduceerde een nieuw API eindpunt dat gebruikers toestaat om eerder geschrapte activiteitenopties van een secundair gegevensbestand te herstellen. Deze functionaliteit maakt gebruik van de bestaande infrastructuur die door de klassen `RemovedCampaignElements` en `RemovedOptionInfo` wordt geboden, zodat verwijderde opties naadloos kunnen worden geïntegreerd in actieve activiteiten. (TGT-52903)
* Probleem verholpen waarbij [!DNL Recommendations] -activiteiten met metrische namen van meer dan 25 tekens niet konden worden geopend of bewerkt vanwege API-beperkingen. Deze correctie zorgt voor compatibiliteit met metrische namen die de tekenlimiet overschrijden en herstelt volledige toegang tot de desbetreffende activiteiten. (TGT-52839)

+++

**vorm-Gebaseerde Composer van de Ervaring**

+++Zie details
* Oplossing een kwestie in [!UICONTROL Form-Based Experience Composer] die de redacteur aan neerstorting na het klikken van het **[!UICONTROL Manage Content]** pictogram ( ![ leidt het pictogram van de Inhoud ](/help/main/assets/icons/Experience.svg)) toen het creëren van of het uitgeven van een [!UICONTROL Automated Personalization] (AP) activiteit veroorzaakte. (TGT-53047)

+++

**Aanbevelingen**

+++Zie details
* Probleem verholpen waarbij [!UICONTROL Catalog Search] geen extra resultaten kon laden wanneer naar de onderkant van de lijst werd geschoven en het gedrag werd hersteld in overeenstemming met de oudere gebruikersinterface. (TGT-53088)
* Probleem verholpen waarbij het verwijderen van items uit het dialoogvenster [!UICONTROL Criteria Details] werd geblokkeerd. (TGT-53245)
* Probleem verholpen waardoor het openen van producten zonder naam niet mogelijk was. Dit probleem is opgetreden bij het selecteren van omgevingen die onbenoemde resultaten hebben opgeleverd, waardoor toegang tot productdetails niet mogelijk was. (TGT-53007)
* Probleem verholpen waarbij de pagina [!UICONTROL Catalog Search] vastliep en een leeg scherm werd weergegeven wanneer bepaalde producten werden geselecteerd. (TGT-53087)
* Probleem verholpen waarbij gebruikers de site_cart_z1 [!DNL Recommendation] -activiteit niet konden bewerken in de gebruikersinterface van [!DNL Target] . Als u de activiteit probeerde te openen, werd een fout op de pagina [!UICONTROL Overview] gegenereerd, waardoor de toegang tot de editor werd geblokkeerd. (TGT-53221)

+++

**Meldend**

+++Zie details
* Probleem verholpen waarbij het sandboxveld in de activiteitsdatabase niet werd gewist toen de rapportbron werd overgeschakeld van [!DNL Customer Journey Analytics] naar [!DNL Analytics] . [!DNL Target] Eerder heeft de gebruikersinterface de sandbox correct verzonden: null, maar de back-end heeft deze waarde genegeerd, waardoor verouderde sandboxgegevens op zijn plaats blijven. De backend ontruimt nu behoorlijk het zandbakgebied wanneer ongeldig wordt ontvangen. (TGT-52798)
* Implementeer de verwijderde optiepersistentielaag opnieuw in de doelachtergrond om nauwkeurige historische rapportage in [!UICONTROL Automated Personalization] (AP)-activiteiten te ondersteunen. Eerder, toen een optie werd geschrapt, werd zijn naam verloren, die het moeilijk maken om vroegere prestatiesgegevens te interpreteren.

  **Zeer belangrijke Verbeteringen**:

   * Verwijderde opties worden nu bijgehouden met behulp van de bestaande `RemovedCampaignElements` - en `RemovedOptionInfo` -infrastructuur.
   * Wanneer een optie uit een AP-activiteit wordt verwijderd, blijven de metagegevens (bijvoorbeeld ID en naam) behouden.
   * De rapportinterface kan nu de oorspronkelijke optienaam (bijvoorbeeld `Option Name [Deleted]` ) naast historische metriek weergeven, waardoor de duidelijkheid en bruikbaarheid worden verbeterd.

  Deze update zorgt voor consistente en betekenisvolle rapportage, zelfs nadat opties uit een activiteit zijn verwijderd. (TGT-52986)

+++

**Visuele Composer van de Ervaring (VEC)**

+++Zie details

* Probleem verholpen in de VEC waarbij het toepassen van een wijziging op een weergave dubbel werk veroorzaakte en een fout met &#39;Ongeldige gebruikersinvoer&#39; veroorzaakte. (TGT-52886)
* Probleem verholpen met [!UICONTROL Undo] functionaliteit voor de opties [!UICONTROL Insert Before] en [!UICONTROL Insert After] bij het configureren van afbeeldingsaanbiedingen in de VEC.

  Eerder leidde het ongedaan maken van een [!UICONTROL Insert Before] - of [!UICONTROL Insert After] -actie op afbeeldingsaanbiedingen tot inconsequent gedrag of tot het niet correct herstellen van de wijziging, vooral in activiteiten die zijn gemaakt in de oudere [!DNL Target] -gebruikersinterface. Dit probleem is opgelost om ervoor te zorgen dat acties voor ongedaan maken nu betrouwbaar werken voor deze wijzigingen. (TGT-52809)

* Probleem verholpen waarbij het kenmerk `contentEditable` onbedoeld werd ingesteld op true en bleef bestaan in opgeslagen HTML-inhoud. Deze update zorgt voor schonere, verwachte HTML-uitvoer zonder onbedoeld bewerkingsgedrag. (TGT-52319)
* Om permanent verlies van geschrapte opties te verhinderen en verenigbaar gedrag over de diensten te verzekeren, is de zachte schrappingsfunctionaliteit uitgevoerd voor opties in UI en verwante microservices.

  **Zeer belangrijke Veranderingen**:

   * De opties worden niet meer permanent verwijderd. In plaats daarvan worden ze gemarkeerd met een nieuwe verwijderde: ware markering in het XML-parameterobject.
   * Deze markering wordt alleen gebruikt door de bijgewerkte [!DNL Target] UI om verwijderde opties uit te sluiten van rendering en te voorkomen dat deze naar Edge-services worden verzonden.
   * Verwijderde opties blijven deel uitmaken van de taakbelasting tijdens bewerkingen, waardoor de traceerbaarheid wordt gewaarborgd en niet-bestaande opties aan klanten worden geleverd.

  Deze update verbetert de gegevensintegriteit en past de beste praktijken voor het beheren van schrappingen in verdeelde systemen aan. (TGT-52726)

+++

**Werkruimten**

+++Zie details
* Probleem verholpen bij het kopiëren van een activiteit van een niet-standaard naar een standaardwerkruimte of tussen niet-standaardwerkruimten. Aanbiedingen worden nu gedupliceerd met verbeterde tracking en naming om conflicten te voorkomen.

  **Zeer belangrijke Verbeteringen**:
   * Aanbiedingen worden opnieuw gemaakt in de doelwerkruimte met bijgewerkte id&#39;s en metagegevens.
   * De naam van gekopieerde voorstellen wordt gewijzigd in de indeling: &quot;Naam van voorstel kopiëren&quot; plus een willekeurig nummer of tijdstempel om ervoor te zorgen dat deze voorstellen uniek zijn.
   * De systeemupdates bieden de status van de activiteit en weerspiegelen deze met de nieuwe id&#39;s.
   * Deze functie voorkomt fouten die worden veroorzaakt door meerdere identieke namen voor &quot;Offertes kopiëren&quot; tijdens herhaalde kopieerhandelingen.
   * Aanbiedingen worden mogelijk niet direct weergegeven in de lijst met aanbiedingen van de doelwerkruimte, maar worden op de juiste wijze verwerkt en weergegeven.

  Deze update verbetert de betrouwbaarheid en traceerbaarheid bij het beheren van aanbiedingen in meerdere werkruimten. (TGT-53080)

+++

## [!DNL Target Standard/Premium] 25.7.2 (18 juli 2025)

Vanwege recente problemen die zijn vastgesteld en die voornamelijk verband houden met complexe klantaanpassingen, bevat deze release de volgende oplossingen en updates:

**Activiteiten**

+++Zie details
* Er is een extra bevestigingswaarschuwing toegevoegd bij het annuleren van bewerkingen met niet-opgeslagen wijzigingen: &quot;Wilt u deze activiteit echt opslaan? Als u niet opslaat, gaan alle wijzigingen verloren.&quot; Met dit bericht voorkomt u dat gegevens per ongeluk verloren gaan. (TGT-52865)
* De oude functionaliteit is hersteld naar de schuifregelaar [!UICONTROL Priority] in [!UICONTROL Goals & Settings] , zodat klanten direct een numerieke waarde kunnen invoeren. Dit wordt ondersteund in de oudere gebruikersinterface. (TGT-53185 &amp; TGT-53219)

+++

**Soorten publiek**

+++Zie details
* Probleem verholpen waarbij het opslaan of bewerken van activiteiten met aangepast publiek werd voorkomen. Klanten hebben het foutbericht &quot;We kunnen uw verzoek niet voltooien. Neem contact op met [!DNL Adobe Client Care] als het probleem zich blijft voordoen.&quot; wanneer u probeert wijzigingen in bepaalde activiteiten op te slaan, of zelfs zonder wijzigingen op te slaan. (TGT-53189)

+++

**[!UICONTROL Analytics for Target] (A4T)**

+++Zie details
* Probleem verholpen waarbij klanten rapporten voor specifieke activiteiten op de pagina [!UICONTROL Goals & Settings] weergeven, wordt met de koppeling [!UICONTROL View in Analytics] onjuist verwezen naar de QA-omgeving in plaats van naar de productieomgeving. (TGT-53163)

+++

**[!UICONTROL Experiences]en[!UICONTROL Offers]**

+++Zie details
* Probleem verholpen waarbij het aanroepen van `triggerView` via aangepaste code een oneindige lus veroorzaakte. (TGT-52885)
* Probleem verholpen waarbij een probleem optrad dat niet overeenkomt met de verschillen tussen de definities in `LocalIds` die zijn gedefinieerd voor activiteiten en die in `LocalIds` die worden gebruikt in ervaringsdefinities. (TGT-52669)
* Probleem verholpen waarbij de metrische namen ontbraken op de pagina activity [!UICONTROL Overview] en alleen &#39;Offer&#39; in plaats van de juiste metrische naam werden weergegeven. (TGT-53054)

+++

**vorm-Gebaseerde Composer van de Ervaring**

+++Zie details
* Probleem verholpen in de [!UICONTROL Form-Based Experience Composer] die het opslaan van activiteiten verhinderde en het foutbericht activeerde: &quot;Kan eigenschappen van undefined niet lezen (lees &#39;map&#39;)&quot;. (TGT-53145)

+++

**Aanbevelingen**

+++Zie details
* Probleem verholpen waarbij door te klikken op een product uit [!UICONTROL Catalog Search] de fout &#39;&#39;Kan de productdetails niet ophalen&#39;&#39; werd weergegeven en een modaal zonder sluitoptie werd geopend. (TGT-53082)
* Oplossing voor een probleem waarbij [ aanbevelingen als aanbiedingen ](/help/main/c-recommendations/recommendations-as-an-offer.md) in [!UICONTROL A/B Test] activiteiten niet correct bleven wanneer het veranderen van inzamelingen of bevorderingen. (TGT-52884)
* Probleem verholpen waarbij in de productieomgeving werd geklikt op een entiteit in de bijgewerkte interface en de fout werd weergegeven: &quot;Kan de productdetails niet ophalen. Neem contact op met [!DNL Adobe Client Care] als dit probleem zich blijft voordoen.&quot; (TGT-53071)

+++

**Rapporten**

+++Zie details
* Oplossing van een probleem waarbij het opslaan van ordergegevens naar een CSV-bestand resulteerde in een leeg bestand. (TGT-5225)

+++

**[!UICONTROL Visual Experience Composer] (VEC)**

+++Zie details
* Het probleem op de pagina [!UICONTROL Goals & Settings] waarbij kiezers die in meerdere ervaringen werden gebruikt, niet altijd als geselecteerd werden gemarkeerd, is opgelost. (TGT-53062)
* Probleem verholpen waarbij het bewerken van activiteiten werd verhinderd en het foutbericht werd geactiveerd: &quot;Kan de eigenschappen van undefined (lezen van &#39;map&#39;) niet lezen.&quot; (TGT-53161)

+++

**Werkruimten**

+++Zie details
* Verbeterde afhandeling van ad-hocaanbiedingen bij het schakelen tussen werkruimten.
   * Wanneer u van de standaardwerkruimte overschakelt op een niet-standaardwerkruimte (of tussen niet-standaardwerkruimten), worden de ad-hocaanbiedingen nu op de juiste wijze gekopieerd. Tijdens initialisatie, wordt de werkruimtecontext bijgewerkt en een nieuwe identiteitskaart wordt toegewezen aan de aanbieding om uniciteit te verzekeren.
   * Er treden geen wijzigingen op wanneer u binnen dezelfde werkruimte blijft. (TGT-53079)
* Vaste een kwestie die klanten verhinderde [ het kopiëren activiteiten tussen verschillende werkruimten ](/help/main/c-activities/edit-activity.md#section_45A92E1DD3934523B07E71EF90C4F8B6). (TGT-52753 &amp; TGT-47094)
* Probleem verholpen bij het wijzigen van eigenschappen tussen werkruimten.
   * Als de huidige eigenschap in de doelwerkruimte bestaat, blijft de eigenschap behouden wanneer wordt geschakeld tussen de standaardwerkruimte en een niet-standaardwerkruimte.
   * Als in de lijst [!UICONTROL Properties] een waarschuwing wordt weergegeven (die sommige eigenschappen mogelijk niet compatibel maakt) en de klant op [!UICONTROL Add] of [!UICONTROL Remove] klikt en vervolgens op [!UICONTROL Save] klikt, worden alle eigenschappen die zich niet in de doelwerkruimte bevinden, verwijderd. Als de klant op [!UICONTROL Cancel] klikt, blijven alle eigenschappen behouden, zelfs als ze niet bestaan in de doelwerkruimte. (TGT-47094)
   * Als u in dezelfde werkruimte blijft of van een niet-standaardwerkruimte overschakelt op de standaardwerkruimte of op een andere werkruimte, blijft alles ongewijzigd. (TGT-53078)
* Bijgewerkte logica voor entiteitsvalidatie om de oorspronkelijke werkruimtecontext van de activiteit te respecteren. Entiteiten zoals [!UICONTROL Experience Fragments] (XFs) worden nu gevalideerd op basis van de werkruimte waarin de activiteit oorspronkelijk is gemaakt. Als er bijvoorbeeld een XF-bestand aanwezig is in de standaardwerkruimte en de activiteit wordt gekopieerd van werkruimte X naar werkruimte Y, gaat de validatie nog steeds door zolang de XF-waarde geldig is in de oorspronkelijke (standaard)werkruimte. (TGT-53196)
* Verbeterde ondersteuning voor het kopiëren van ad-hocdoelgroepen tijdens dubbel werk.
   * Ad-hocdoelgroepen, zoals metriek, rapportage, pagina en alleen-activiteit, worden nu automatisch gekopieerd in de volgende scenario&#39;s:
      * Bij het kopiëren van een activiteit van de standaardwerkruimte naar een niet-standaardwerkruimte.
      * Bij het kopiëren van een activiteit binnen dezelfde werkruimte. (TGT-53197)

+++

## [!DNL Target Standard/Premium] 25.7.1 (11 juli 2025)

Vanwege recente problemen die zijn vastgesteld en die voornamelijk verband houden met complexe klantaanpassingen, bevat deze release de volgende oplossingen en updates:

**Activiteiten**

+++Zie details
* Probleem verholpen waarbij de URL van [!UICONTROL Activity QA] een overbodige queryparameter bevatte: `at_preview_evaluate_as_true_audience_ids` . (TGT-52907)
* Probleem verholpen waarbij voorvertoning-URL&#39;s ten onrechte meer soorten publiek bevatte dan expliciet door de gebruiker werd getypt. Dit gedrag is gecorrigeerd om ervoor te zorgen dat alleen het opgegeven publiek wordt toegepast wanneer een koppeling voor een kwaliteitscontrole of voorvertoning wordt gegenereerd. (TGT-52912)
* Probleem verholpen waardoor gebruikers [!UICONTROL Auto-Target] (AT)-activiteiten niet konden maken als [!UICONTROL Auto-Allocate] (AA) als eerste is geselecteerd tijdens de installatie van de verkeerstoewijzing. Dit probleem heeft geresulteerd in een validatiefout voor de back-end en voorkomt dat de activiteit wordt opgeslagen. (TGT-53096)

+++

**Soorten publiek**

+++Zie details
* Probleem verholpen waarbij gebruikers met de rol [!UICONTROL Approver] geen publieksverfijningen met alleen activiteit konden toevoegen of opslaan. Het proberen dit te doen resulteerde in een 403 Verboden fout, die dat het &quot;[ redacteur ]&quot;voorrecht werd vereist, alhoewel de gebruiker voldoende toestemmingen had om activiteiten goed te keuren en te beheren. (TGT-52984)
* Probleem verholpen waarbij een activiteitsspecifiek publiek werd verwijderd met de optie [!UICONTROL Remove Audience Refinement] , wordt het publiek niet langer weergegeven in de publiekslijst voor herselectie binnen dezelfde activiteit. Dit gedrag verhindert gebruikers het zelfde publiek opnieuw toe te voegen tenzij het van kras wordt ontspannen. (TGT-52979)
* Probleem verholpen waarbij de alleen voor activiteit bedoelde publieksverfijningen direct uit de gebruikersinterface verdwenen nadat ze van een locatie waren verwijderd, zelfs voordat de activiteit was opgeslagen. Dit gedrag druist in tegen de verwachte functionaliteit en de knopinfo-richtlijnen, die als volgt luiden: &quot;Alle ongebruikte soorten publiek uit deze bibliotheek worden verwijderd wanneer de activiteit wordt opgeslagen.&quot; (TGT-52982)
* Probleem verholpen bij pogingen om een ander publiek dan [!UICONTROL All Visitors] toe te wijzen aan een activiteit. Na het opslaan wordt het volgende foutbericht weergegeven: &quot;We kunnen uw verzoek niet voltooien. Neem contact op met [!UICONTROL Adobe Client Care] als het probleem zich blijft voordoen.&quot; (TGT-53008)
* Probleem verholpen waarbij het opslaan van een activiteit werd geblokkeerd na het maken en toewijzen van een nieuw publiek in de activity editor. Het weergegeven foutbericht was: &quot;We kunnen uw verzoek niet voltooien. Neem contact op met [!UICONTROL Adobe Client Care] als het probleem zich blijft voordoen.&quot; (TGT-52977)

+++

**[!UICONTROL Analytics for Target] (A4T)**

+++Zie details
* Probleem verholpen waarbij het kopiëren van een bestaande activiteit en het wijzigen van de rapportbron in [!DNL Adobe Analytics] (A4T) zou resulteren in een fout met betrekking tot &quot;Ongeldige gebruikersinvoer&quot;. De fout werd geactiveerd wanneer bepaalde metrische handelingen die niet compatibel zijn met [!DNL Analytics] -rapportage, zoals `restart_same_experience` , `restart_random_experience` en `restart_new_experience` , niet in de oorspronkelijke activiteit zijn opgenomen. (TGT-52900)
* Probleem verholpen waarbij klanten werden verhinderd een activiteit te maken of op te slaan wanneer ze [!DNL Adobe Analytics] (A4T) als rapportbron in de stap [!UICONTROL Goals & Settings] selecteerden. Het probleem is specifiek opgetreden bij het selecteren van een [!UICONTROL Custom Event] metrische waarde (bijvoorbeeld &#39;Aangepaste gebeurtenis 16&#39;). Dit heeft de volgende fout tot gevolg: &#39;Ongeldige gebruikersinvoer&#39;. (TGT-52910)
* Probleem verholpen waarbij gebruikers door te klikken op de koppeling &quot;[!UICONTROL View in Analytics]&quot; werden omgeleid naar de startpagina in plaats van naar het bedoelde [!DNL Analytics] -dashboard. (TGT-53092 &amp; TGT-53093)
  <!-- * Fixed an issue when cloning an existing activity and changing the reporting source from [!DNL Target] to [!DNL Adobe Analytics], users encounter a "400 - Invalid User Input" error, preventing the activity from being saved. (TGT-52875)-->
* Probleem verholpen waarbij een [!DNL Recommendations] -activiteit in de bijgewerkte [!UICONTROL Overview] UI werd weergegeven. De sectie [!UICONTROL Goals & Settings] wordt niet geladen wanneer [!DNL Adobe Analytics] (A4T) als rapportbron is geselecteerd. Het volgende foutbericht werd weergegeven: &quot;Er is iets misgegaan. Je aanvraag kan niet worden voltooid. Neem contact op met de Adobe Client Care als het probleem zich blijft voordoen.&quot; (TGT-52999)

+++

**[!UICONTROL Experiences]en[!UICONTROL Offers]**

+++Zie details
<!-- * Fixed an issue where using the [!UICONTROL Manage Content] feature in [!UICONTROL Automated Personalization] (AP) activities caused the page to crash and remain blank. This issue occurred after clicking [!UICONTROL Done] in the content manager, particularly in activities created or edited in the updated UI. (TGT-53047)-->
* Probleem verholpen waarbij de functie [!UICONTROL Manage Content] de status van een locatie niet correct valideerde nadat alle inhoudsopties waren verwijderd. Dit probleem kan leiden tot inconsistente gedragingen of fouten bij het opslaan of doorgaan met de activiteitenconfiguratie. (TGT-52801)
* Probleem verholpen waarbij gebruikers een &#39;&#39;Ongeldige invoerfout&#39;&#39; tegenkwamen bij het toevoegen van een nieuwe pagina en het verwijderen van specifieke elementen uit verschillende ervaringen. De fout wordt veroorzaakt door dubbel `LocalIds` die tijdens elementmanipulatie wordt geproduceerd, vooral wanneer het schakelen tussen ervaringen en het wijzigen van gedeelde paginastructuren. (TGT-52720)
* Het probleem waarbij het gebruik van de functie [!UICONTROL Generate Adhoc Offer] tot ongedefinieerde locaties in het deelvenster [!UICONTROL Manage Content] leidde, is opgelost. (TGT-53076 &amp; TGT-53070)
* Verduidelijkt het gedrag voor de klant waar wijzigingen die met een HTML-aanbieding zijn aangebracht, mogelijk ontbreken wanneer u van de stap [!UICONTROL Targeting] terug naar [!UICONTROL Experiences] navigeert. Voor deze klant heeft de desbetreffende website dynamisch meerdere DOM-kiezers gegenereerd die zijn gewijzigd bij het laden van elke pagina. Hierdoor kan de kiezer die oorspronkelijk voor de wijziging is gebruikt, niet worden gevonden wanneer de editor opnieuw wordt geopend, waardoor de wijziging ontbreekt of ongeldig wordt weergegeven. Dit scenario werkt zoals ontworpen. Om ervoor te zorgen dat de wijzigingen in de redacteur visueel blijven, adviseert men dat de cliënten stabiele, verenigbare selecteurs gebruiken die niet over paginaatherladingen veranderen. (TGT-52874)
* Probleem verholpen waarbij het verwijderen of deactiveren van een aanbieding die deel uitmaakte van een uitgesloten ervaring, leidde tot een fout met betrekking tot &quot;Ongeldige gebruikersinvoer&quot;. Dit probleem kwam aan de orde, ook al werd het aanbod niet actief gebruikt in de meegeleverde ervaringen. (TGT-52917)

+++

**vorm-Gebaseerde Composer van de Ervaring**

+++Zie details
* Probleem verholpen met op formulieren gebaseerde activiteiten waarbij het dupliceren van een ervaring en het bewerken van de aangepaste code in een van de gedupliceerde ervaringen onbedoeld deze wijzigingen op alle gedupliceerde ervaringen toepast. Elke ervaring behoudt nu zijn eigen aangepaste code onafhankelijk na duplicatie. (TGT-51600)

+++

**Localization**

+++Zie details
* Bijgewerkte lokalisatietekenreeksen in nieuwe UI voor Frans (fr_FR), Duits (de_DE), Italiaans (it_IT), Koreaans (ko_KO), en Vereenvoudigd Chinees (zh_CN).

+++

**[!DNL Recommendations]**

+++Zie details
* Toegevoegd een nieuwe [!DNL Recommendations] voer [ status ](/help/main/c-recommendations/c-products/feeds.md#status): [!UICONTROL Partial Import Failed]. (kB-2215)
* Probleem verholpen dat invloed had op de workflow voor het maken van activiteiten tijdens het toevoegen van [!DNL Recommendations] met [!UICONTROL promotions] . Wanneer de gebruikers &quot; [!UICONTROL Promote by Attribute]&quot;selecteerden en een het filtreren regel (bijvoorbeeld, [!UICONTROL Parameter Matching]) toevoegden, werden het geselecteerde regeltype en de operandwaarden niet bewaard na het bewaren en het heruitgeven van de activiteit. Bij het opnieuw openen zou het filterregeltype onverwacht veranderen en zouden operandwaarden ontbreken. (TGT-53059)
* Probleem verholpen in de gebruikersinterface van [!DNL Recommendations] waarbij een promotie die met één regel is gemaakt, onjuist werd geïnterpreteerd en weergegeven als een promotietype Lijst met objecten, ongeacht de logica van de regel. (TGT-53063)
* Oplossing een kwestie toen het gebruiken van bijgewerkte [!UICONTROL Overview] UI, de &quot;[!UICONTROL Download Recommendations Data]&quot;knoop mist voor [!UICONTROL Experience Targeting] (XT) activiteiten die [!DNL Recommendations] omvatten. (TGT-52730 &amp; TGT-52756)
* Eerder werd in de gebruikersinterface van Aanbevelingen alleen het aantal entiteiten weergegeven dat is geïmporteerd uit een feed. De indeling voor achterste berichten bevat echter zowel het aantal geïmporteerde entiteiten als het totale aantal entiteiten in de notatie: `# of entities imported / # of total entities` . Door deze discrepantie zagen gebruikers alleen de eerste waarde (geïmporteerd aantal) in de gebruikersinterface, wat tot verwarring leidde. In de gebruikersinterface worden nu beide getallen weergegeven. (TGT-53073)
* Oplossing een kwestie waar de klanten een het filtreren regel niet konden bewaren wanneer het vormen van een &quot;[!UICONTROL Promote by attribute]&quot;bevordering in een op vorm-gebaseerde activiteit A/B met aanbevelingen. Na het opslaan en opnieuw openen van de activiteit, ontbrak de het filtreren regel, en de activiteit kon niet met succes worden bewaard. (TGT-53057)

+++

**Rapporten**

+++Zie details
* Probleem verholpen waarbij door het selecteren van &quot;[!UICONTROL Export order details to CSV]&quot; op de [!UICONTROL Reports] -pagina een leeg bestand werd gedownload. Deze kwestie kwam zelfs voor wanneer de geldige ordegegevens in de activiteit aanwezig waren. (TGT-5225)
* Probleem verholpen tijdens het opslaan van een activiteit na het maken en toewijzen van een nieuw rapportagepubliek. Het geretourneerde foutbericht is: &quot;Toegang geweigerd. Om deze verrichting uit te voeren, worden alle volgende voorrechten vereist: [ redacteur ].&quot; Dit probleem is opgetreden ondanks het feit dat de gebruiker toegang op goedkeuringsniveau heeft. (TGT-53103)

+++

**[!UICONTROL Visual Experience Composer] (VEC)**

+++Zie details
* Oplossing voor een probleem waarbij het toepassen van een wijziging op een weergave ertoe zou leiden dat de weergave wordt gedupliceerd en dat de activiteit een fout met &quot;Ongeldige gebruikersinvoer&quot; retourneert. Met deze correctie zorgt u ervoor dat weergavewijzigingen correct worden toegepast zonder dat er fouten optreden bij het dupliceren of valideren. (TGT-52886)
* Probleem verholpen waarbij aangepaste codewijzigingen onjuist werden weergegeven voor een verkeerde ervaring. Met name veranderingen die voor één ervaring bedoeld waren, werden in een andere ervaring aangetoond, wat tot verwarring en mogelijke verkeerde configuratie van de activiteiten in het leven heeft geleid. (TGT-52776)
* Probleem verholpen waarbij het bewerken of opslaan van aangepaste codewijzigingen in de nieuwe VEC-interface werd voorkomen. Specifiek:

   * Nadat u een aangepast codeblok hebt bewerkt en opgeslagen, zijn de wijzigingen niet doorgevoerd in de gebruikersinterface of in de voorvertoning van de kwaliteitscontrole.
   * In sommige gevallen kunnen wijzigingen alleen worden verwijderd als de activiteit wordt gesloten en opnieuw wordt geopend.
   * Als tussenoplossing moesten gebruikers de code kopiëren, de wijziging verwijderen en handmatig opnieuw maken met de bijgewerkte inhoud. (TGT-53072)

* Probleem verholpen waarbij het bewerken en opslaan van aangepaste code ertoe leidde dat het deelvenster [!UICONTROL Modifications] niet meer reageerde. (TGT-53075)
* Correctie van een probleem waarbij wijzigingen die in ervaringen met varianten in aangepaste code zijn aangebracht, onbedoeld in de [!UICONTROL Control] -ervaring werden doorgevoerd. Dit leidde tot onbedoelde veranderingen in het gedrag van de bevalling. De ervaring van [!UICONTROL Control] blijft nu geïsoleerd van aangepaste code-bewerkingen die op andere ervaringen zijn toegepast. (TGT-52413)
* Probleem verholpen waarbij wijzigingen die zijn aangebracht in een ervaring (bijvoorbeeld Experience B) per ongeluk werden gedupliceerd naar een andere ervaring (Experience A) als de gebruiker op de tweede ervaring had geklikt voordat de editor volledig geladen was. Dit gedrag kan er ook toe leiden dat wijzigingen verloren gaan als de oorspronkelijk geselecteerde ervaring geen wijzigingen bevat. (TGT-52597)
* Correctie van een probleem waarbij wijzigingen die zijn aangebracht in de stap [!UICONTROL Modifications] voor het maken van activiteiten, niet consistent werden opgeslagen. In sommige gevallen zou het aangepaste script dat u in de sectie [!UICONTROL Save] hebt toegevoegd, na alle stappen te hebben voltooid en op [!UICONTROL Modifications] te hebben geklikt, niet meer op de livesite worden weerspiegeld, ondanks geen zichtbare fouten tijdens het opslagproces. (TGT-52661)
* Probleem verholpen waarbij wijzigingen in aangepaste code niet correct werden opgeslagen en onbedoeld werden weerspiegeld in meerdere ervaringen binnen dezelfde activiteit. Bovendien stuitten gebruikers op toegangsproblemen bij het openen of vernieuwen van bepaalde activiteiten, wat leidde tot lege schermen. Deze problemen zijn nu opgelost om te zorgen voor een stabiele bewerking van activiteiten en een nauwkeurige isolatie van ervaringen. (TGT-52594)
* Probleem verholpen waarbij gebruikers in [!UICONTROL Browse Mode] niet naar een andere URL konden bladeren. Hierdoor konden testers en editors geen alternatieve pagina&#39;s valideren of voorvertonen binnen dezelfde activiteitensessie. (TGT-53052)
* Probleem verholpen waarbij meerdere [!UICONTROL Visual Experience Composer] (VEC) instanties tegelijkertijd werden geopend tijdens het maken van activiteiten. Dit probleem is opgetreden wanneer gebruikers [!UICONTROL Enhanced Experience Composer] (EEC) hadden uitgeschakeld en de slash van de URL van de website in de stap [!UICONTROL Page Delivery] hadden verwijderd. (TGT-52782)
* Probleem verholpen waarbij de [!UICONTROL Revenue] metrische vervolgkeuzelijst in de stap [!UICONTROL Goals & Settings] onjuist zou worden standaard op [!UICONTROL Revenue per Visit] (RPVISIT), zelfs nadat de gebruiker een andere maatstaf had geselecteerd.  Het probleem trad op bij het samenvouwen en opnieuw uitvouwen van het configuratievenster voor metrische gegevens, waardoor de eerder geselecteerde waarde opnieuw werd ingesteld. (TGT-52811 &amp; TGT-52878)
* Oplossing voor verschillende problemen in de workflow voor het maken van activiteiten met betrekking tot het aanbieden van naamgeving en het vertalen van inhoud in [!UICONTROL Automated Personalization] (AP)- en [!UICONTROL Multivariate Testing] (MVT)-activiteiten:

  Belangrijkste problemen opgelost:

   * Het maken van meerdere HTML-aanbiedingen met dezelfde naam (bijvoorbeeld &#39;Experience&#39;) heeft geleid tot de fout &#39;Dubbele aanbiedingsnamen zijn niet toegestaan&#39;, maar de interface gaf niet duidelijk aan welke aanbiedingen het conflict veroorzaakten.
   * Als de naam van aanbiedingen wordt gewijzigd via het rechterdeelvenster, wordt de naam bijgewerkt in de gebruikersinterface, maar de wijziging wordt niet doorgevoerd op het tabblad [!UICONTROL Manage Content] of [!UICONTROL Offers] , waardoor er permanente validatiefouten optreden.
   * In MVT-activiteiten bleef de fout met de dubbele naam weliswaar niet bestaan na het wijzigen van de naam, maar de interface gaf nog steeds geen consistente weerspiegeling van bijgewerkte aanbiedingsnamen op de verschillende tabbladen. (TGT-52933)

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
