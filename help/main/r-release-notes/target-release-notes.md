---
keywords: releaseopmerkingen;releases;updates;toekomstige release;verbeteringen;nieuwe functies;oplossingen;updates;vooruitgave;vroege toegang
description: Leer over de nieuwe eigenschappen, de verhogingen, en de moeilijke situaties inbegrepen in de aanstaande versie van  [!DNL Target], met inbegrip van SDKs, APIs, en de bibliotheken van JavaScript.
title: Welke Nieuwe Eigenschappen en de Verbeteringen worden omvat in de aanstaande  [!DNL Target]  Versie?
feature: Release Notes
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
source-git-commit: be371f3631d79c65c632a23776ab08de21b031eb
workflow-type: tm+mt
source-wordcount: '2610'
ht-degree: 0%

---

# [!DNL Target] releaseopmerkingen (pre-release)

Dit artikel bevat pre-releasegegevens voor komende [!DNL Adobe Target] versies, waaronder SDK&#39;s, API&#39;s en JavaScript-bibliotheken.

**Laatst bijgewerkt: 27 augustus 2025**

>[!NOTE]
>
>* Releasedatums, -functies en andere informatie kunnen zonder voorafgaande kennisgeving worden gewijzigd. De informatie in dit artikel wordt regelmatig bijgewerkt, vooral vóór versies.
>
>* Om informatie over de huidige versie te bekijken, zie {de Nota&#39;s van de Versie van het 0} Doel [.](release-notes.md)
>
>* De uitgiftenummers tussen haakjes zijn bedoeld voor intern gebruik door [!DNL Adobe] .

## [!DNL Target Standard/Premium] 25.8.4 (28 augustus 2025)

Deze release bevat de volgende updates en oplossingen:

**[!UICONTROL Activities]**

+++Zie details
* **Vaste een kwestie waar de geplande activiteiten verkeerd een &quot;[!UICONTROL Live]&quot;status in bijgewerkte UI tijdens het activiteit-creeer proces** getoond: De activiteiten met toekomstige activeringsdata tonen nu correct een &quot;[!UICONTROL Scheduled]&quot;status. (TGT-53187)
* **Geplande activiteiten vertoonde verkeerd a [!UICONTROL Live] status tot de pagina werd verfrist**: De klanten rapporteerden dat wanneer het plannen van een activiteit om op een toekomstige datum en tijd te gaan Levend, de status aanvankelijk als [!UICONTROL Live] in plaats van [!UICONTROL Scheduled] verscheen. Dit veroorzaakte verwarring ondanks het bevestigingsbericht die op het correcte planningsgedrag wijzen. De activiteitsstatus geeft direct na het opslaan de waarde [!UICONTROL Scheduled] correct weer, zonder dat een pagina moet worden vernieuwd. (TGT-52937)
* **Veranderingen in gedupliceerde ervaringen beïnvloedden onbedoeld de originele ervaring**: De klanten rapporteerden dat wanneer het dupliceren van een ervaring binnen een activiteit en het toewijzen van een nieuw publiek, om het even welke veranderingen die aan gedupliceerde ervaring-zoals ontwerp of criterium-werden aangebracht ook in de originele ervaring werden weerspiegeld. Dit voorkwam het ontstaan van onafhankelijke variaties en beïnvloedde productiewerkstromen. Gedupliceerde ervaringen kunnen nu afzonderlijk worden bewerkt zonder dat dit van invloed is op de oorspronkelijke versie. (TGT-53361)
* **Vaste een kwestie die klanten verhinderde een activiteit toe te schrijven aan een `InvalidProperty.Json` fout** op te slaan: Eerder, ontmoetten de klanten een &quot;Ongeldige fout van de gebruikersinvoer&quot;wanneer het proberen om een activiteit te bewaren zonder veranderingen aan te brengen. De fout is veroorzaakt door een niet-herkende eigenschapsnaam &#39;content&#39; in de JSON-payload. Dit probleem is opgelost en activiteiten kunnen nu met succes worden opgeslagen in de bijgewerkte gebruikersinterface, zelfs als er geen wijzigingen worden aangebracht. (TGT-53513)

+++

**Analytics voor Doel (A4T)**

+++Zie details
* **kan de namen van de rapportreeksen niet typen wanneer het creëren van A4T activiteiten**: De klanten konden niet in [!UICONTROL Report Suite] drop-down typen wanneer het selecteren van [!UICONTROL Analytics] als rapporteringsbron in bijgewerkte UI.  Dit maakte het moeilijk om specifieke rapportesuites te vinden, vooral voor organisaties met grote lijsten. Het keuzemenu ondersteunt nu typen en zoeken op naam, waardoor het proces voor het maken van activiteiten efficiënter wordt. (TGT-53345)

+++

**[!UICONTROL Audiences]**

+++Zie details
* **Verlopen &quot;het Frame van de Tijd&quot;publiek geblokkeerde activiteit die sparen zelfs na verwijdering** bespaart: Eerder, konden de klanten een activiteit niet bewaren als het eerder een verlopen &quot;Kader van de Tijd&quot;publiek-zelfs nadat dat publiek werd verwijderd had omvat. Dit probleem werd veroorzaakt door het feit dat de validatie voor alleen de activiteit werd voortgezet, waardoor er nog steeds fouten werden gegenereerd. Activiteiten kunnen nu worden opgeslagen zoals u had verwacht nadat het verlopen publiek is verwijderd. (TGT-53517)
* **de Extra pagina&#39;s en de veelvoudige publiek verdwenen na het bewaren van een activiteit**: Eerder, de klanten die een [!UICONTROL A/B Test] activiteit in het activiteit-creeer proces creëren ervaren een verlies van gevormde extra pagina&#39;s en veelvoudige publiek na het bewaren. Dit gedrag was onverwacht en veroorzaakte verwarring tijdens opstelling. Deze configuraties blijven nu correct na het opslaan van de activiteit. (TGT-52357)

+++

**de aanbiedingen van het Besluit**

+++Zie details
* **Onbekwaam om besluitaanbiedingen uit te geven of specifieke paginaelementen in bijgewerkte VEC** te selecteren: De klanten ontmoetten veelvoudige kwesties in bijgewerkte UI die hun capaciteit om bestaande activiteiten bij te werken of nieuwe te creëren blokkeerden:

   * Beslissingsvoorstellen werden onjuist weergegeven als HTML-voorstellen, waardoor bewerkingen werden voorkomen.
   * Kan geen specifieke pagina-elementen selecteren in de VEC.
   * Wijzigingen die tijdens het bewerken zijn aangebracht, zijn niet opgeslagen.
   * Bepaalde regionale URL&#39;s zijn niet correct geladen in de VEC, waardoor handmatige cookieaanpassingen nodig zijn.

  Klanten kunnen nu beslissingsvoorstellen bewerken, pagina-elementen nauwkeurig selecteren en wijzigingen naar behoren opslaan. Regionale pagina&#39;s worden ook correct geladen in VEC. (TGT-53425)

* **de selecteurs van het Besluit van de Aanbieding konden niet onverwacht worden gewijzigd en worden veranderd na sparen**: De klanten rapporteerden dat wanneer het toepassen van de Besluiten van de Aanbieding in bijgewerkte UI, selecteur niet van zijn standaardwaarde kon worden veranderd. Pogingen om de kiezer te wijzigen (bijvoorbeeld in `#tf-cq-hr or body` ) werden genegeerd en nadat de activiteit was opgeslagen, werd de kiezer vervangen door een algemene waarde zoals `#cdq_element_0` . Deze kwestie veroorzaakte de aanbieding om van Visual Experience Composer (VEC) te verdwijnen en blokkeerde verdere uitgeeft. Klanten kunnen nu de kiezers voor het besluit van het voorstel naar wens wijzigen en opgeslagen kiezers blijven correct zonder onverwachte wijzigingen. (TGT-53433)
* **Besluiten van de Aanbieding verdwenen van activiteiten na sparen**: De klanten rapporteerden dat de Besluiten van de Aanbieding die op paginaelementen in bijgewerkte UI werden toegepast niet meer zichtbaar na het bewaren van de activiteit waren. In sommige gevallen, werd de selecteur onverwachts veranderd, en de aanbieding slaagde er niet in om in VEC na het heruitgeven terug te geven. De Besluiten van het aanbod blijven nu correct na sparen, en de selecteurs blijven stabiel, ervoor zorgen de aanbiedingen zichtbaar en editable zoals verwacht zijn. (TGT-53434)

+++

**Fragmenten van de Ervaring**

+++Zie details
* **Klanten ontvingen een fout toen het opnemen van [!UICONTROL Experience Fragments] gebruikend [!UICONTROL Insert Before] of[!UICONTROL Insert After]**: Klanten ontmoetten een fout toen het proberen om [!UICONTROL Experience Fragments] in een activiteit op te nemen gebruikend [!UICONTROL Insert Before] of [!UICONTROL Insert After] opties in bijgewerkte UI. Het weergegeven foutbericht was:

  &quot;Inhoud van aanbieding moet precies één HTML-element bevatten.&quot;

  Deze kwestie was specifiek voor de bijgewerkte UI en kwam niet voor in de vorige versie. Het probleem is nu opgelost en klanten kunnen [!UICONTROL Experience Fragments] zonder deze fout in te voegen. (TGT-53432)

* **het bericht van de Fout wanneer het toevoegen van een [!UICONTROL Experience Fragment] aan een activiteit**: Eerder, probeerden de klanten om [!UICONTROL Experience Fragment] op te nemen gebruikend [!UICONTROL Insert Before] of [!UICONTROL Insert After] optie ondervond de fout: &quot;de inhoud van de aanbieding moet precies één element van HTML bevatten.&quot; Deze fout is opgetreden ondanks het feit dat het fragment geldig was en werd geaccepteerd in de oudere UI, die een schakeloptie bevatte ter ondersteuning van deze configuratie. Het probleem is opgelost in de bijgewerkte VEC. (TGT-53442)

+++

**Localization**

+++Zie details
* **Toast berichten in de [!UICONTROL Goals & Settings] stap werden niet gelokaliseerd**: Eerder, ontmoetten de klanten een niet gelokaliseerd pop-bericht toen het ingaan van niet gestaafd karakter-zulke zoals emojis-op het [!UICONTROL Objective] gebied tijdens het activiteit-creeer proces. Toast berichten worden nu correct gelokaliseerd in alle ondersteunde talen, zodat klanten overal ter wereld een consistente en toegankelijke ervaring hebben. (TGT-52251)
* **een koord van A in de [!UICONTROL Create Audience] dialoog werd niet gelokaliseerd**: Eerder, verscheen het bericht &quot;verkies minstens een begin of einddatum voor &quot;niet herhaalt&quot;&quot;niet gelokaliseerd in [!UICONTROL Create Audience] modaal toen het vormen van tijd-kader attributen. De tekenreeks wordt nu correct gelokaliseerd in alle ondersteunde talen, zodat klanten overal ter wereld dezelfde ervaring hebben in de [!UICONTROL Audiences] -workflow. (TGT-52253)
* **tooltip in de [!UICONTROL Create Audience] dialoog werd niet gelokaliseerd**: Eerder, toen de klanten over de foutentooltip na het ingaan van niet gestaafde karakters-zulke zoals emojis-op het gebied van de publieksnaam hielden, leek tooltip unlocalized. De knopinfo geeft nu correct gelokaliseerde berichten in alle ondersteunde talen weer, zodat een consistente en toegankelijke ervaring in de [!UICONTROL Audiences] -workflow wordt gegarandeerd. (TGT-52254)

+++

**[!DNL Recommendations]**

+++Zie details
* **Onbekwaam om [!UICONTROL Front Promotion] in levende activiteit** onbruikbaar te maken: Vaste een kwestie waar de klanten [!UICONTROL Front Promotion] in levende activiteiten niet konden onbruikbaar maken gebruikend bijgewerkte UI. Wijzigingen die tijdens het proces voor het maken van activiteiten in de sectie Promotie zijn aangebracht, blijven nu zoals verwacht behouden en zorgen voor een nauwkeurige configuratie van live activiteiten in [!UICONTROL Product Catalog Search] . (TGT-53231)
* **het uitgeven van de aanbeveling van een gedupliceerde ervaring beïnvloedde de originele ervaring**: De klanten rapporteerden dat wanneer het dupliceren van een ervaring binnen een activiteit en het wijzigen van het aanbevelingsontwerp of de criteria in duplicaat, die veranderingen onbedoeld op de originele ervaring werden toegepast.  Dit probleem voorkwam het ontstaan van onafhankelijke variaties en verstoorde het verwachte gedrag in het bijgewerkte proces voor het maken van activiteiten. Gedupliceerde ervaringen kunnen nu afzonderlijk worden bewerkt zonder dat dit van invloed is op de oorspronkelijke versie. (TGT-53369)
* **kan niet de productlijst bekijken wanneer het uitgeven van een inzameling of een uitsluiting in [!UICONTROL Recommendations] lusje** eerder, was de productlijst die door toegepaste regels wordt gefiltreerd niet zichtbaar in uitgeeft modaal, die het voor klanten moeilijk maken om te bevestigen welke producten inbegrepen of uitgesloten waren. De productlijst wordt nu correct weergegeven en in real-time bijgewerkt wanneer de regels worden gewijzigd. Hierdoor wordt de zichtbaarheid en bruikbaarheid van de bijgewerkte gebruikersinterface van [!DNL Recommendations] verbeterd. (TGT-53481)
* **werkte de lay-out van de [!UICONTROL View Details] dialoog in het [!UICONTROL Recommendations] lusje** bij: Eerder, ontbrak de [!UICONTROL View Details] dialoog een duidelijke structuur, die het voor klanten moeilijk maakt om tot punt-specifieke en inventaris-verwante informatie toegang te hebben. De layout is bijgewerkt en bevat nu twee tabbladen: op een tabblad worden de details van het geselecteerde item weergegeven en op het tweede tabblad wordt de inventaris weergegeven die is gefilterd door de huidige regels voor de verzameling of uitsluiting. Deze verbetering verbetert de helderheid en bruikbaarheid in de bijgewerkte gebruikersinterface van [!DNL Recommendations] . (TGT-53503)
* **Klanten konden rapportsuites in [!UICONTROL Goals & Settings] drop-down** niet zoeken: Eerder, steunden de drop-down van de rapportsuites in de [!UICONTROL Goals & Settings] sectie van het activiteit-creeer proces geen tekstinput voor het zoeken, die het voor klanten met grote aantallen rapportsuites moeilijk maken om van correcte de plaats te bepalen. Deze functionaliteit, die beschikbaar is in de oudere gebruikersinterface, is hersteld. Klanten kunnen nu op efficiëntere wijze naar de gewenste pakketten typen en deze selecteren. (TGT-53514)
* **Klanten kunnen de douanecriteria CSV in [!DNL Recommendations] UI** niet downloaden: Eerder, klikkend de downloadverbinding voor douane criteria CSVs in het [!UICONTROL Recommendations] lusje teruggekeerde een 404 fout en ontbrak om in een nieuw lusje te openen. De downloadkoppeling wordt nu op een nieuw tabblad geopend en dient correct in het CSV-bestand, waardoor de toegankelijkheid en bruikbaarheid voor klanten die aangepaste criteria beheren, worden verbeterd. (TGT-51966)
* **toelatend a [!UICONTROL Recommendations] bevordering zonder inputgegevens teweegbracht een generisch foutenbericht**: Eerder, klanten toelatend een voor- of achterbevordering in een geadviseerde  actiesactiviteit zonder vereiste gebieden te specificeren ondervonden een vage &quot;Ongeldige inputfout&quot;met de code `error.restapi.missingFields`. Het systeem biedt nu een duidelijk en activeerbaar foutbericht dat aangeeft welke velden ontbreken, waardoor de bruikbaarheid wordt verbeterd en verwarring tijdens het proces van het maken van activiteiten wordt verminderd. (TGT-52616)
* **de duimnagels en de beelden van het product werden niet constant geladen in[!UICONTROL Catalog Search]**: De klanten meldden dat de productduimnagels en de full-size beelden in [!UICONTROL Catalog Search] periodiek mist of gebroken, vooral na het navigeren of het wijzigen van kolomzichtbaarheid. Miniaturen en afbeeldingen worden nu betrouwbaar geladen, ongeacht de kolominstellingen of het navigatiefunctie, waardoor de algehele ervaring in de [!UICONTROL Recommendations] -workflow verbetert. (TGT-52778)
* **Onbekwaam om [!UICONTROL Designs] en [!UICONTROL Criteria] in het [!UICONTROL Stage] milieu** tot stand te brengen: De klanten ontmoetten een &quot;Ongeldige fout van de input van de Gebruiker&quot;toen het proberen om [!UICONTROL Designs] of [!UICONTROL Criteria] in het [!UICONTROL Recommendations] lusje op het [!UICONTROL Stage] milieu tot stand te brengen. Klanten kunnen nu [!UICONTROL Designs] en [!UICONTROL Criteria] zonder fouten maken in de [!UICONTROL Stage] -omgeving. (TGT-53205)
* **[!UICONTROL Promotions]zijn niet verwijderd uit [!UICONTROL Recommendations] -activiteiten nadat ze waren opgeslagen** : klanten melden dat promoties die aan [!DNL Recommendation] -activiteiten zijn toegevoegd, ook na het verwijderen en opslaan nog steeds worden weergegeven. Dit probleem betrof zowel testomgevingen als productieomgevingen en bleef bestaan bij meerdere opslagpogingen. De bevorderingen weerspiegelen nu correct veranderingen die tijdens activiteit het uitgeven in het bijgewerkte activiteit-creeer proces worden aangebracht. (TGT-53490)

+++

**[!UICONTROL Reports]**

+++Zie details
* **[!UICONTROL Automated Segments]toonde een ongeldig publiek in activiteitenrapporten**: De klanten merkten op dat wanneer het bekijken [!UICONTROL Automated Segments] in de [!UICONTROL Reports] sectie van een activiteit, het publieksgebied als ongeldig leek, alhoewel de geldige segmentgegevens werden verwacht. Dit probleem had invloed op de zichtbaarheid van doelgroepen en de nauwkeurigheid van de rapportage. [!UICONTROL Automated Segments] geeft nu de bijbehorende publieksinformatie correct weer in activiteitenrapporten. (TGT-52793)
* **de rapporten van de Activiteit slaagden er niet in in formaat CSV** te downloaden: De klanten die activiteitenrapporten van het [!UICONTROL Reports] lusje proberen uit te voeren ontmoetten een mislukking toen het selecteren van de CSV downloadoptie. Dit probleem betrof zowel de standaardrapporten als de export van ordergegevens. Rapporten worden nu correct gedownload in CSV-indeling. (TGT-53464)

+++

**Enige Toepassingen van de Pagina (SPAs)**

+++Zie details
* **schakelde tussen [!UICONTROL Browse] en [!UICONTROL Design] wijzen terugstellen enig-paginatoepassingsstaten (SPA) in de Webredacteur**: De klanten rapporteerden dat het schakelen tussen [!UICONTROL Browse] en [!UICONTROL Design] wijzen in VEC de Webredacteur veroorzaakte om opnieuw te laden, de staat van het KUUROORD terug te stellen en het activiteit-creeer proces te verstoren. De redacteur bewaart nu de de navigatiestatus van het KUUROORD wanneer omschakelingswijzen, die een vlottere en consistentere het uitgeven ervaring verzekeren. (TGT-53074)

+++

**[!UICONTROL Visual Experience Composer (VEC)]**

+++Zie details
* **het anders noemen van een plaats in een [!UICONTROL Automated Personalization] (AP) of [!UICONTROL Multivariate Test] (MVT) activiteit bleef niet na het navigeren aan de [!UICONTROL Targeting] stap en het terugkeren.** Klanten kunnen nu namen van locaties bewerken en opslaan, en de wijzigingen blijven zichtbaar tijdens het maken van activiteiten. (TGT-52367)
* **erfenisVEC UI die op huurders in het [!UICONTROL Stage] milieu** wordt getoond: Vaste een kwestie wanneer de toegang tot van bepaalde huurders in het [!UICONTROL Stage] milieu verkeerd werd getoond erfenis UI in plaats van bijgewerkte VEC. Deze kwestie was reproduceerbaar over veelvoudige login wegen en beïnvloedde de [!UICONTROL Activities] sectie. De bijgewerkte interface wordt nu correct weergegeven voor beide huurders in de [!UICONTROL Stage] -omgeving. (TGT-52261)
* **het Selecteren van een achtergrondkleur veroorzaakte de pagina om in bijgewerkte VEC** te crashen:
Probleem verholpen waarbij het selecteren van een achtergrondkleur in het deelvenster [!UICONTROL Style] in de bijgewerkte VEC ertoe leidde dat de pagina vastliep en blanco ging. Consolefouten duiden op een fout bij het lezen van eigenschappen van een niet-gedefinieerd element, dat specifiek gerelateerd is aan `querySelector` . Klanten kunnen nu veilig achtergrondkleuren selecteren zonder dat dit tot gevolg heeft dat de toepassing vastloopt. (TGT-53561)
* **de Activiteiten konden niet wegens een ongeldige fout van de gebruikersinput** worden bewaard: Vaste een fout toen het proberen om bestaande activiteiten in bijgewerkte VEC te bewaren. De fout werd alleen tijdens bewerkingen weergegeven, niet tijdens het maken van nieuwe activiteiten met dezelfde eigenschap. Het foutbericht is opgenomen:

  `Invalid Json. Unrecognized property name 'content'. Location: line - 1, column - 432.`

  Activiteiten die gebruikmaken van de desbetreffende eigenschap kunnen nu met succes worden opgeslagen nadat ze zijn bewerkt. (TGT-53507)

* **de Transparante beelden omvatten niet meer de &quot;fmt=png-alpha&quot;parameter in bijgewerkte VEC**: De klanten rapporteerden dat wanneer het vervangen van beelden in bijgewerkte UI, de transparante achtergronden niet meer werden bewaard. De afbeelding-URL&#39;s die door de bijgewerkte VEC zijn gegenereerd, hebben de parameter `fmt=png-alpha` weggelaten, die eerder transparantie in de oude UI zorgde. De bijgewerkte gebruikersinterface voegt nu correct de parameter `fmt=png-alpha` toe voor transparante afbeeldingen en herstelt het verwachte rendergedrag. (TGT-52615)
* **Klanten konden niet aan het richten sectie in AP activiteiten te werk gaan zonder twee plaatsen** toe te voegen: Klanten die [!UICONTROL Automated Personalization] (AP) activiteiten in bijgewerkte UI creëren konden niet aan het richten sectie te werk gaan tenzij twee plaatsen werden toegevoegd. Dit gedrag verschilde van de vorige UI, waar één enkele plaats voldoende was. Het probleem blokkeerde het creëren van activiteit en het opslaan voor klanten die verkiezen om slechts één plaats te gebruiken. Klanten kunnen nu AP-activiteiten richten en opslaan op één locatie, waardoor de verwachte functionaliteit wordt hersteld. (TGT-53426)
* **HTML biedt gedupliceerde aanbiedingen in de werkruimte wanneer het schakelen ervaringen**: Eerder, klanten die HTML voorstellen in ervaren gedupliceerde inhoud in de werkruimte na omschakeling tussen ervaringen opnemen. Dit probleem heeft er ook toe geleid dat de werkruimte niet-schuifbaar is geworden, wat gevolgen heeft voor de bruikbaarheid. HTML-aanbiedingen worden niet meer gedupliceerd en de werkruimte blijft schuifbaar wanneer er in de bijgewerkte VEC wordt geschakeld. (TGT-53487)
* **veroorzaakte manueel het bijwerken van een CSS selecteur het scherm VEC om leeg te gaan**: De klanten rapporteerden dat terwijl het uitgeven van een aanbieding in VEC, manueel het bijwerken van CSS selecteerde een leeg scherm teweegbracht, zelfs wanneer de selecteur geldig was en op de pagina aanwezig was. Het VEC-scherm blijft nu stabiel wanneer kiezers handmatig worden bijgewerkt tijdens het activity-create proces. (TGT-53553)
* **Uitgave van de afkapping op het gebied van de Datum van het Begin wanneer het selecteren van &quot;gespecificeerde datum en tijd&quot;in[!UICONTROL Goals & Settings]**: De klanten ervoeren een afbreekprobleem op het [!DNL Start date] gebied wanneer het kiezen van de gespecificeerde datum en tijdoptie in de duursectie van de [!UICONTROL Goals & Settings] pagina tijdens activiteitenverwezenlijking. De volledige datum en tijd worden nu correct weergegeven voor alle ondersteunde landinstellingen. (TGT-47843)
* **pictogram van de Filter verdween wanneer het minimaliseren van browser in [!UICONTROL Manage Content] spoor**: De klanten rapporteerden dat het filterpictogram in [!UICONTROL Manage Content] spoor van [!UICONTROL Automated Personalization] activiteit-creeer stroom verdween wanneer het browser venster resized of geminimaliseerd werd. Het filterpictogram blijft nu zichtbaar en toegankelijk, ongeacht de grootte van de browser, wat de bruikbaarheid op de verschillende schermresoluties ten goede komt. (TGT-51449)

+++

**[!UICONTROL Workspaces]**

+++Zie details
* **Klanten beperkt tot één enkele werkruimte konden activiteiten van andere werkruimten** bekijken: De klanten met toegang beperkt tot een specifieke werkruimte konden [!UICONTROL All Workspaces] nog selecteren in bijgewerkte UI en activiteiten van andere werkruimten bekijken. Dit gedrag vormde een risico van onbedoelde veranderingen in de live activiteiten buiten het toegewezen bereik. Workspace-beperkingen worden nu correct toegepast en klanten kunnen activiteiten alleen weergeven binnen de toegewezen werkruimte. (TGT-53101)
* **Klanten konden activiteiten van [!UICONTROL Default Workspace] zonder toegang** bekijken: De klanten konden activiteiten van [!UICONTROL Default Workspace] ondanks het hebben van geen toegang tot het zien. Workspace-machtigingen worden nu correct afgedwongen in de bijgewerkte gebruikersinterface, zodat klanten alleen activiteiten zien die aan hun toegewezen werkruimte zijn gekoppeld. (TGT-53297)

+++

## Aanvullende opmerkingen bij de release en versiedetails

| Bron | Details |
|--- |--- |
| [ de nota&#39;s van de Versie: Het Web SDK van de Ervaring van het Platform van Adobe Target ] (https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=e n) | Details over veranderingen in elke versie van het Web SDK van het Platform. |
| [ at.js versiedetails ](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html){target=_blank} | Informatie over de wijzigingen in elke versie van de JavaScript-bibliotheek [!DNL Adobe Target] at.js. |

## Prerelease-informatie {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Als u geavanceerde meldingen wilt ontvangen over aanstaande productverbeteringen in [!DNL Target] en andere [!DNL Adobe Experience Cloud] -oplossingen, meldt u zich aan voor [!DNL Adobe Priority Product Update] :

[ https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
