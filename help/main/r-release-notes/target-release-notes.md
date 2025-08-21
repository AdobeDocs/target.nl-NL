---
keywords: releaseopmerkingen;releases;updates;toekomstige release;verbeteringen;nieuwe functies;oplossingen;updates;vooruitgave;vroege toegang
description: Leer over de nieuwe eigenschappen, de verhogingen, en de moeilijke situaties inbegrepen in de aanstaande versie van  [!DNL Target], met inbegrip van SDKs, APIs, en de bibliotheken van JavaScript.
title: Welke Nieuwe Eigenschappen en de Verbeteringen worden omvat in de aanstaande  [!DNL Target]  Versie?
feature: Release Notes
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
source-git-commit: 95d8bd994ffdb1d256b7eb0aea1a2462b40ce530
workflow-type: tm+mt
source-wordcount: '2221'
ht-degree: 0%

---

# [!DNL Target] releaseopmerkingen (pre-release)

Dit artikel bevat pre-releasegegevens voor komende [!DNL Adobe Target] versies, waaronder SDK&#39;s, API&#39;s en JavaScript-bibliotheken.

**Laatst bijgewerkt: 21 augustus 2025**

>[!NOTE]
>
>* Releasedatums, -functies en andere informatie kunnen zonder voorafgaande kennisgeving worden gewijzigd. De informatie in dit artikel wordt regelmatig bijgewerkt, vooral vóór versies.
>
>* Om informatie over de huidige versie te bekijken, zie {de Nota&#39;s van de Versie van het 0} Doel [.](release-notes.md)
>
>* De uitgiftenummers tussen haakjes zijn bedoeld voor intern gebruik door [!DNL Adobe] .

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

## Aanvullende opmerkingen bij de release en versiedetails

| Bron | Details |
|--- |--- |
| [ de nota&#39;s van de Versie: Het Web SDK van de Ervaring van het Platform van Adobe Target ] (https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=e n) | Details over veranderingen in elke versie van het Web SDK van het Platform. |
| [ at.js versiedetails ](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html?lang=nl-NL){target=_blank} | Informatie over de wijzigingen in elke versie van de JavaScript-bibliotheek [!DNL Adobe Target] at.js. |

## Prerelease-informatie {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Als u geavanceerde meldingen wilt ontvangen over aanstaande productverbeteringen in [!DNL Target] en andere [!DNL Adobe Experience Cloud] -oplossingen, meldt u zich aan voor [!DNL Adobe Priority Product Update] :

[ https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
