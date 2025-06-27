---
keywords: releaseopmerkingen;nieuwe functies;releases;updates;update;release;verbetering;verbeteringen;correcties;foutoplossingen;updates,huidige updates
description: Leer over de nieuwe eigenschappen, de verhogingen, en de moeilijke situaties inbegrepen in de huidige versie van  [!DNL Adobe Target], met inbegrip van SDKs, APIs, en de bibliotheken van JavaScript.
landing-page-description: Leer over de nieuwe eigenschappen, de verhogingen, en de moeilijke situaties inbegrepen in de huidige versie van  [!DNL Adobe Target].
short-description: Leer over de nieuwe eigenschappen, de verhogingen, en de moeilijke situaties inbegrepen in de huidige versie van  [!DNL Adobe Target].
title: Wat is inbegrepen in de huidige Versie?
feature: Release Notes
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
source-git-commit: f8e91caa133a1addc12ab1834d7e178df7e7a3ce
workflow-type: tm+mt
source-wordcount: '2725'
ht-degree: 0%

---

# [!DNL Target] releaseopmerkingen (huidig)

Ontdek de nieuwste functies, verbeteringen en oplossingen in [!DNL Adobe Target] . Deze versienota&#39;s behandelen ook updates aan [!DNL Target] APIs, SDKs, A [!DNL dobe Experience Platform Web SDK], at.js, en andere platformcomponenten wanneer toepasselijk.

(De uitgiftenummers tussen haakjes zijn bedoeld voor intern gebruik door [!DNL Adobe] .)

## [!DNL Target Standard/Premium] 25.6.4 (27 juni 2025)

Deze release bevat de volgende correcties en updates:

* De optie [!UICONTROL Rearrange] is toegevoegd aan de bijgewerkte interface van [!UICONTROL Visual Experience Composer] (VEC), zodat deze kan worden uitgelijnd met de functionaliteit die beschikbaar is in de oudere VEC. (TGT-46957 &amp; TGT-52876)
* Correctie van een probleem waarbij wijzigingen die zijn aangebracht in ervaringen met varianten (bijvoorbeeld Experience B) in een [!UICONTROL A/B Test] -activiteit niet werden behouden. Na omschakeling tussen ervaringen, zouden de veranderingen in de variant verdwijnen. Dit probleem had geen invloed op de ervaring met controle. (TGT-52664)
* Probleem verholpen waarbij bepaalde klanten geen activiteiten konden maken of opslaan, terwijl andere klanten dezelfde acties zonder problemen konden uitvoeren. Het probleem was inconsistent tussen de accounts.(TGT-52842)
* Probleem verholpen waarbij gebruikers in de bijgewerkte VEC geen wijzigingen konden verplaatsen naar de [!UICONTROL Page Load event] , een mogelijkheid die bestond in de oudere gebruikersinterface. (TGT-52617)
* Probleem verholpen waarbij [!UICONTROL page load] -gebeurtenissen niet zichtbaar waren in [!DNL Target] tijdens het maken van wijzigingen. Updates worden alleen toegepast op weergaven. (TGT-52604)
* Probleem verholpen waardoor sommige wijzigingen in de activiteit niet correct werden weergegeven in de bijgewerkte VEC. (TGT-52818)
* Oplossing voor een null pointer-uitzondering die optrad bij het ophalen van rapportgegevens voor [!UICONTROL Automated Personalization] (AP)-activiteiten. (TGT-52362)
* Probleem verholpen waarbij details op aanbiedingsniveau niet konden worden weergegeven in het CSV-bestand voor [!UICONTROL Automated Personalization] (AP)-activiteiten. (TGT-52675)
* Correctie van een probleem bij het toepassen van wijzigingen in de bijgewerkte VEC, worden wijzigingen in eerste instantie correct weergegeven, inclusief de verwachte [!UICONTROL Experience Fragment] . Nochtans, na omschakelingservaringen of het aanbrengen van extra uitgeeft, ontbreken sommige veranderingen om toe te passen toe te schrijven aan selecteurkwesties. (TGT-52679)
* Probleem verholpen waarbij de pagina-URL&#39;s van de oorspronkelijke activiteit niet werden behouden wanneer een nieuwe activiteit werd gemaakt door een bestaande activiteit te klonen. Dit probleem is nu opgelost. (TGT-52775)
* Probleem opgelost waarbij [!UICONTROL On-device Decisioning] per ongeluk niet beschikbaar was in de bijgewerkte VEC. (TGT-52371)
* Probleem verholpen waarbij het bewerken van een product [!DNL Recommendations] -activiteit werd verhinderd. Wanneer u via de doelinterface toegang probeert te krijgen tot de VEC, verschijnt er een fout op de pagina [!UICONTROL Overview] , waardoor bewerkingen worden voorkomen. (TGT-52823)
* Probleem verholpen waarbij het opslaan van een [!DNL Recommendations] -activiteit werd voorkomen wanneer namen langer dan 50 tekens voorkomen. (TGT-52619)
* Probleem verholpen waarbij klanten geen activiteit met aanbevelingen konden opslaan nadat ze de criteria in de nieuwe gebruikersinterface hadden gewijzigd. De kwestie lijkt op toestemming-verwant te zijn en beïnvloedt niet alle gebruikers met gelijkaardige rollen. (TGT-52816)
* Probleem verholpen waarbij gebruikers met de rol [!UICONTROL Editor] een [!DNL Recommendations] -activiteit niet konden bewerken. Het proberen om het ontwerp te veranderen en de activiteit te bewaren resulteerde in een 403 Verboden fout, verklarend dat &quot;[ redacteur ]&quot;voorrecht werd vereist, alhoewel de gebruiker reeds die rol in de relevante werkruimte had. (TGT-52836)

## [!DNL Target Standard/Premium] 25.6.3 (20 juni 2025)

Deze release bevat de volgende correcties en updates:

* Probleem verholpen waarbij het kopiëren van een activiteit van de ene werkruimte naar een andere werkruimte tot fouten leidde zoals &quot;mag niet null zijn&quot; of &quot;Er is iets fout gegaan&quot;. (TGT-52474)
* Probleem verholpen waarbij [!UICONTROL Automated Segments] - en [!UICONTROL Important Attributes] -rapporten niet werden gegenereerd voor bepaalde activiteiten. (TGT-52904)
* Probleem verholpen in de bijgewerkte VEC waarbij de standaardverwerking van inhoud in [!UICONTROL Automated Personalization] (AP)-activiteiten niet overeenkwam met de oudere UI. Het systeem voegt nu automatisch de standaardwaarde `optionGroup` &quot;Standaardinhoud&quot; toe aan `optionGroupLocalId = 0` wanneer er geen groep expliciet wordt toegevoegd. Deze groep bevat de standaardoptie (bijvoorbeeld `optionLocalId: 0` ). Als de standaardinhoud wordt verwijderd, wordt ook de corresponderende optiegroep verwijderd. (TGT-52651)
* Probleem verholpen met [!UICONTROL Multivariate Test] (MVT)-activiteiten waarbij het hergebruik van een `experienceLocalId` uit eerder verwijderde ervaringen onjuist werd verboden. (TGT-52672)
* Probleem verholpen waarbij kopiëren of bewerken van activiteiten met een ervaringsfragment werd voorkomen. Dit heeft de fout veroorzaakt: `Enum "AemOfferType" cannot represent value: "html"`. (TGT-52635)
* Probleem verholpen waarbij URL&#39;s op activiteitenlocaties geen queryparameters konden weergeven vanwege ongeldige tekens, zoals schuine strepen (/). (TNT52845)
* Het foutbericht voor de validatie van [!DNL A/B Test] activity updates via de back-end API is verbeterd. Wanneer dubbele locatienamen aanwezig zijn, staat nu duidelijk in het bericht: &quot;Dubbele namen zijn niet toegestaan&quot; voor `locations.selectors` . (TGT-52589)
* Oplossing voor een fout die optrad bij het bijwerken van een live [!UICONTROL Recommendations] -activiteit vanwege een niet-herkende eigenschap in de payload van de aanvraag. Het systeem handelt nu correct de &quot;Ongeldige JSON. Niet-herkende eigenschapsnaam&quot;. (TGT-52723)
* Probleem verholpen waarbij het maken van een [!DNL Recommendations] -ontwerp werd voorkomen. Als u op [!UICONTROL Create] klikt, wordt het bericht geactiveerd: &quot;Er moet ten minste één entiteitsvariabele in het script worden gebruikt.&quot; (TGT-52395 &amp; TGT-52899)
* Probleem opgelost waarbij het opnieuw opslaan van een [!DNL Recommendations] -ontwerp zonder wijzigingen werd geblokkeerd. (TGT-52879)
* Probleem verholpen met een validatiefout aan de achterkant die een fout van het type &quot;400 Onjuist verzoek&quot; veroorzaakte bij het opslaan van een [!UICONTROL Recommendations] -activiteit. (TGT-52716)
* Probleem verholpen in [!UICONTROL Form-Based Experience Composer] waarbij het aanwijzen van de muisaanwijzer over een box met speciale tekens in de vervolgkeuzelijst [!UICONTROL Location] ertoe leidde dat de editor leeg ging en dat er een &#39;QuerySelector&#39; kon niet worden uitgevoerd op &#39;Element&#39;. fout. (TGT-52717)
* Verbeterde nauwkeurigheid van de voederstatus met een nieuwe indicator &quot;PARTIALLY_IMPORTED&quot;. Eerder werden feeds gemarkeerd als &quot;succes&quot;, zelfs als niet alle rijen in een bestand werden geïmporteerd, wat misleidend was. (TGT-52892)
* Probleem verholpen waarbij bepaalde API-aanroepen naar `/admin/rest/ui/v1/campaigns` na de migratie naar AP V2 fouten aan de clientzijde (HTTP 4xx) veroorzaakten. (TGT-52721)

## Bijgewerkt: [!DNL Target] afschrijving van versiesamenstelling voor gebruikersinterface (17 juni 2025) {#revised}

Vanaf 17 juni 2025 moeten alle IMS-organisaties zijn ingeschakeld voor de bijgewerkte [!DNL Target] -gebruikersinterface, voor specifieke gebruikers of voor de hele organisatie, om de nieuwe ervaring te testen.

Vanwege recente problemen die zijn vastgesteld, voornamelijk in verband met complexe klantaanpassingen, heeft het team van [!DNL Target] de tijdlijn voor de afschrijving aangepast:

* **Juni 30, 2025**: [ bijgewerkte  [!DNL Target]  UI ](/help/main/c-intro/understand-the-target-ui.md) zal de standaardervaring voor alle IMS Orgs worden die de UI versieknevel hebben toegelaten.

   * Klanten die momenteel de verouderde UI zien, door gebrek, zullen nu bijgewerkte UI bij login zien.
   * De UI versiesknevel zal beschikbaar blijven tegen eind Juli, toestaand gebruikers om terug te schakelen indien nodig.

  >[!IMPORTANT]
  >
  > [!DNL Adobe] raadt u ten zeerste aan de bijgewerkte gebruikersinterface van [!DNL Target] te gebruiken. Schakel alleen terug naar de oudere gebruikersinterface als er een probleem met een blokkering optreedt. Zie {de versie van 0} UI van knevel afschrijving (23 mei, 2025) [&#128279;](/help/main/r-release-notes/release-notes-for-previous-releases.md#toggle) in de versienota&#39;s voor vorige versies voor belangrijke informatie over knevel.[!DNL Target] 

* **15 juli tot 30 juli, 2025**: De de versiesknevel van UI zal permanent in fasen onbruikbaar worden gemaakt. Betrokken IMS Orgs kunnen niet meer terugkeren naar de oudere UI.

   * Uitzonderingen zullen per geval worden herzien.
   * Vertragingen bij de tijdelijke vervanging van de knevel worden slechts kort (een paar dagen) toegestaan, terwijl problemen met blokkeringen worden opgelost.

Gelieve te contacteren [&#128279;](/help/main/cmp-resources-and-contact-information.md#/help/main/cmp-resources-and-contact-information.md) van de Klant van 0&rbrace; Adobe met om het even welke zorgen of als u kwesties tijdens deze overgang verwacht.

## [!DNL Target Standard/Premium] 25.6.2 (12 juni 2025)

Deze release bevat de volgende correcties en updates:

* Toegevoegd a [ nieuw artikel van Veelgestelde vragen ](/help/main/c-intro/updated-ui-faq.md) om gemeenschappelijke vragen over bijgewerkte [!DNL Target] UI en [!UICONTROL Visual Experience Composer] (VEC) te richten.
* Probleem verholpen waarbij de regel &quot;[!UICONTROL URL - does not contain]&quot; in [!UICONTROL Page Delivery] niet werkte, zodat inhoud ook kon worden weergegeven wanneer deze geblokkeerd had moeten zijn. (TGT-52754)
* Correctie van een probleem waarbij het foutbericht in [!UICONTROL Page Delivery] onjuist werd weergegeven: &quot;Dubbele pagina-URL&#39;s zijn niet toegestaan. (TGT-52765)
* Probleem verholpen waarbij publiek voor [!UICONTROL Page Delivery] URL&#39;s met ervaringsfragmenten werd gemaakt met # onjuist toegevoegd. (TGT-52786)
* Probleem verholpen waarbij het kopiëren van een activiteit en het bewerken van instellingen op de pagina [!UICONTROL Goals and Settings] ertoe leidde dat de gebruikersinterface van [!DNL Target] niet meer reageerde. (TGT-52797)
* Probleem verholpen in de bijgewerkte versie van [!UICONTROL Visual Experience Composer] (VEC) die het ten onrechte mogelijk maakte een extra pagina in een [!UICONTROL A/B Test] -activiteit om te leiden naar dezelfde URL. (TGT-51838)
* Correctie van een probleem waarbij wijzigingen in metriek op de pagina [!UICONTROL Goals and Settings] niet werden opgeslagen tijdens het bewerken van een activiteit. (TGT-52799)
* Probleem verholpen waarbij het toevoegen van een nieuwe ervaring terwijl de webeditor nog bezig was met laden, ertoe leidde dat de nieuwe ervaring inhoud uit de vorige ervaring dupliceerde. (TGT-51397)
* De mogelijkheid om aangepaste code buiten de tag `<head>` te gebruiken is hersteld, een functie die voorheen beschikbaar was in de oudere doelinterface. (TGT-52304 &amp; TGT-52300)
* Overbodige validatie is verwijderd bij het selecteren van de standaardwerkruimte tijdens het maken van activiteiten. De verplichte validatie van eigenschappen is niet meer van toepassing op de standaardwerkruimte, maar blijft wel van kracht voor niet-standaardwerkruimten. (TGT-52449)
* Probleem verholpen in de bijgewerkte versie van [!UICONTROL Visual Experience Composer] (VEC), waarbij `triggerView()` -aanroepen niet werden gedetecteerd. (TGT-52575)
* Probleem verholpen in de bijgewerkte versie van [!UICONTROL Visual Experience Composer] (VEC) die verhinderde dat gebruikers wijzigingen konden toevoegen aan [!UICONTROL Single Page Application] (SPA)-weergaven. (TGT-52556)
* Probleem verholpen in de bijgewerkte gebruikersinterface van [!DNL Target] die ervoor zorgde dat klanten de details van de aanbieding niet konden weergeven. (TGT-52607)
* Correctie van een probleem waarbij updates van aanbiedingen in [!UICONTROL Offers Library] niet werden weerspiegeld in de bijgewerkte versie van [!UICONTROL Visual Experience Composer] (VEC). (TGT-52637)
* Probleem verholpen waardoor de sectie Aanbiedingen tijdens het maken van een activiteit niet correct kon worden weergegeven. (TGT-52773)
* Toegevoegde validatie om ervoor te zorgen dat alle `optionLocalIds` waarnaar wordt verwezen in `optionGroups` , aanwezig zijn in de optiesarray. Ongeldige verwijzingen worden automatisch verwijderd tijdens het maken van activiteiten. (TGT-52687)
* Probleem verholpen waarbij rapportagegroepen en uitsluitingen niet werden behouden na toevoeging van een nieuwe aanbieding. (TGT-52728)
* Probleem verholpen waarbij activiteiten zonder de knop [!UICONTROL Activity QA] een lege optieselectie weergaven. (TGT-52733)
* Probleem verholpen waarbij met QA-koppelingen de inhoud niet correct werd gerenderd. (TGT-52718)
* Probleem verholpen waarbij het vervangen van een element door een ervaringsfragment de wijzigingen in de QA-omgeving niet correct weerspiegelde. (TGT-52762)
* Probleem verholpen in de bijgewerkte versie van [!UICONTROL Visual Experience Composer] (VEC) die een fout met betrekking tot &quot;Ongeldige invoer&quot; veroorzaakte wanneer gebruikers probeerden ervaringsfragmenten toe te voegen. (TGT-52701)
* Probleem verholpen waarbij het modaal &#39;Publiek bewerken&#39; leeg leek te zijn tijdens het bewerken van doelgroepen in het bijgewerkte [!UICONTROL Visual Experience Composer] (VEC). (TGT-52749)
* Er is een bericht toegevoegd om gebruikers te informeren wanneer een entiteit niet toegankelijk is in de geselecteerde werkruimte. (TGT-52767)
* Probleem verholpen waarbij de interface het handmatig toewijzen van een milieu-id aan een criterium niet toestaat. In plaats daarvan wordt standaard de id voor de [!UICONTROL Product Catalog Search] -hostgroep gebruikt. Deze oplossing zorgt ervoor dat de wijzigingen in de criteria nu worden toegepast in alle omgevingen en niet alleen in de standaardomgeving. (TGT-52817)
* Correctie van een probleem waarbij de optie &quot;[!UICONTROL Download Recommendations data]&quot; ontbrak voor [!UICONTROL Experience Targeting] (XT)-activiteiten met aanbevelingen. (TGT-52730 &amp; TGT-52756)

## [!DNL Target Standard/Premium] 25.6.1 (6 juni 2025)

Deze release bevat de volgende correcties en updates:

* Probleem verholpen waarbij QA-koppelingen niet de juiste ervaring voor de bijbehorende activiteit hebben opgeleverd. (TGT-52163 &amp; TGT-52790)
* Probleem opgelost waarbij voor QA-koppelingen de bijbehorende gebruikers-id ontbrak. (TGT-52722)
* Probleem verholpen om ervoor te zorgen dat ervaringen alleen worden opgedaan wanneer de geconfigureerde URL voor het leveren van pagina&#39;s correct is voldaan. (TGT-52696)
* Probleem verholpen waardoor klanten geen [!DNL Recommendations] -ontwerpsjabloon konden maken. Als u een sjabloon probeerde te maken, werd de fout geactiveerd: &quot;Er moet ten minste één entiteitsvariabele in het script worden gebruikt.&quot; (TGT-52395)
* Probleem verholpen waarbij het opslaan van [!DNL Recommendations] -ontwerpen met behulp van snelheidsarrays werd voorkomen. Het foutbericht &quot;Er moet ten minste één entiteitsvariabele in het script worden gebruikt&quot; is onjuist geactiveerd. (TGT-52734)
* Correctie van een probleem waarbij wijzigingen niet toegankelijk waren in de map [!UICONTROL Visual Experience Composer] (VEC) wanneer de pagina niet kon worden geladen voor interne webpagina&#39;s. (TGT-52488 &amp;TGT-52470)
* Probleem verholpen waarbij het deelvenster [!UICONTROL Modifications] niet zichtbaar was op kleinere schermgrootten in de VEC. (TGT-52470)
* Probleem verholpen in de bijgewerkte VEC waarbij het overschakelen van de modus [!UICONTROL Browse] naar de modus [!UICONTROL Design] een consolefout veroorzaakte en verdere interactie werd voorkomen. (TGT-52532)
* Probleem verholpen waarbij het klikken op bepaalde elementen per ongeluk de grootte ervan uitbreidde. (TGT-52497)
* Probleem verholpen waarbij bepaalde pagina-elementen niet konden worden geladen of herkend in de VEC, waardoor interactie zoals het selecteren van knoppen of banners en het verstoren van het nauwkeurig bijhouden van gebeurtenissen in activiteiten werd voorkomen. (TGT-52663)
* Probleem verholpen waardoor klanten aanbiedingen in [!UICONTROL Automated Personalization] (AP)-activiteiten niet konden verwijderen of verwijderen. (TGT-52690)
* Probleem verholpen dat inconsistente kwalificatiegedrag van activiteiten in activiteiten met meerdere pagina&#39;s veroorzaakte. (TGT-52694)
* Probleem verholpen waarbij op de pagina [!UICONTROL Overview] van de activiteit een ongeldige URL voor de [!UICONTROL Activity Location] werd weergegeven. (TGT-52695)
* Probleem verholpen in de bijgewerkte gebruikersinterface van [!DNL Target] die ervoor zorgde dat dubbele items werden weergegeven voor activiteitenlocaties. (TGT-52693)
* Probleem verholpen dat een `getAudiencesV3` -fout veroorzaakte, waardoor klanten activiteiten niet konden bewerken of kopiëren. (TGT-52709)
* Probleem verholpen dat een ongeldige payload-fout veroorzaakte bij het toevoegen van [!UICONTROL Experience Fragments] - of HTML-aanbiedingen aan een activiteit. (TGT-52779 &amp; TGT-52773)
* Probleem verholpen waarbij E [!UICONTROL xperience Fragments] niet correct werd weergegeven vanwege een ongeldige invoerfout in de bijgewerkte [!DNL Target] UI. (TGT-52701)
* Probleem verholpen waardoor klanten hun activiteiten in de [!UICONTROL Form-based Experience Composer] niet konden bewerken vanwege een ongeldige gebruikersfout. (TGT-52470)
* Probleem met lokalisatie in de Koreaanse taal verholpen waarbij in eerdere vertalingen tekens werden gebruikt buiten het meertalige basisvlak. In de bijgewerkte vertaling worden de juiste tekens gebruikt die de bedoelde betekenis nauwkeurig aangeven. (TGT-52508 &amp; TGT-52509)
* Probleem met lokalisatie in de Koreaanse taal verholpen waarbij de vertaling voor &quot;date&quot; inconsistent was bij het selecteren van begin- en einddatums voor een activiteit. (TGT-52510)

## [!DNL Target] Vervalsing van interfaceversie in-/uitschakelen (23 mei 2025) {#toggle}

>[!IMPORTANT]
>
>Het team van [!DNL Target] heeft de tijdlijn voor de afgekeurde versie van de gebruikersinterface aangepast. Zie [ Bijgewerkt: [!DNL Target]  de versie van UI knevel afschrijving (17 Juni, 2025) ](#revised) voor meer informatie.

De uitrol van het nieuwe [!DNL Target] gebruikersinterface zal tegen **27 mei, 2025** volledig zijn. Op dat punt, zullen alle klanten toegang tot de recentste versie UI hebben.

Beginnend **Juni 22, 2025**, zal de knevel van de versie UI worden verwijderd. Alle gebruikers gaan permanent over naar de nieuwe interface, zonder optie om naar de vorige versie terug te keren.

>[!NOTE]
>
>Klanten met speciale gevallen die na 22 juni de schakeloptie moeten behouden, kunnen voor hulp contact opnemen met de klantenservice van Adobe.

### Belangrijke informatie over de knevel van de versie UI

We bieden een tijdelijke functie waarmee u met een schakelknop kunt schakelen tussen de bijgewerkte [!DNL Target] interface en de oudere versie. Deze optie is beschikbaar slechts tijdens de definitieve fase van de rollout UI.

![ de versiesknevel van het Doel UI ](/help/main/r-release-notes/assets/toggle.png)

Zodra de rollout volledig is, zal de knevel worden verwijderd, en alle gebruikers zullen permanent naar bijgewerkte UI op **Juni 22, 2025** overgaan. Adobe raadt aan vooruit te plannen, aangezien deze functie binnenkort wordt afgebouwd.

### Beperkingen van het gedrag van de UI-schakelfunctie

* **Zichtbaarheid van nieuwe activiteiten**: De activiteiten die in bijgewerkte UI worden gecreeerd zullen niet zichtbaar zijn als u terug naar erfenisUI schakelt.
* **het uitgeven van bestaande activiteiten**: De veranderingen die aan bestaande activiteiten (oorspronkelijk in erfenis UI) worden aangebracht terwijl het gebruiken van bijgewerkte UI zullen worden gepubliceerd aan uw website. Deze updates zijn echter niet zichtbaar in de oudere UI als u terugschakelt. Alleen de laatste updates die zijn uitgevoerd vanuit de oudere UI worden daar weergegeven.
* **Consistentie van activiteitendetails**: De meest recente veranderingen, ongeacht welke UI u gebruikt, zullen op uw levende website worden weerspiegeld. In de oudere gebruikersinterface worden echter alleen de laatste wijzigingen weergegeven die in die versie zijn aangebracht. Dit zou verwarring kunnen veroorzaken als de activiteiten die in bijgewerkte UI worden uitgegeven verschillend kijken dan wat u in erfenisUI ziet.

### Meer informatie over de bijgewerkte gebruikersinterface

* [[!DNL Target Standard/Premium]  25.2.1 (17 februari, 2025) versienota&#39;s ](/help/main/r-release-notes/release-notes-for-previous-releases.md#ui-update-2): Verstrekt een samenvatting van de belangrijkste veranderingen UI in [!DNL Target] voor [!UICONTROL Activities], [!UICONTROL Recommendations], en [!UICONTROL Visual Experience Composer] (VEC).

* [[!DNL Target Standard/Premium]  25.1.1 (9 Januari, 2025) versienota&#39;s ](/help/main/r-release-notes/release-notes-for-previous-releases.md#ui-update-1): Verstrekt een samenvatting van de belangrijkste veranderingen UI in [!DNL Target] voor [!UICONTROL Offers Library].

* [ begrijp  [!DNL Target]  UI ](/help/main/c-intro/understand-the-target-ui.md): Verstrekt een kort overzicht om u te helpen vertrouwd worden met [!DNL Target] en verleent verbindingen voor meer diepgaande informatie en geleidelijke instructies.

* [[!UICONTROL Visual Experience Composer] changes ](/help/main/c-experiences/c-visual-experience-composer/vec-changes.md) : In de release [!DNL Adobe Target Standard/Premium] 25.2.1 (17 februari 2015) wordt een bijgewerkte versie van [!UICONTROL Visual Experience Composer] (VEC) geïntroduceerd. Dit artikel verklaart de verschillen tussen de erfenis en bijgewerkte versies van VEC.

* [[!UICONTROL Visual Experience Composer] opties ](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md): Dit artikel verklaart bijgewerkte UI VEC en zijn opties.

* [[!DNL Target]  UI update FAQs ](/help/main/c-intro/updated-ui-faq.md): Deze veelgestelde vragen behandelt gemeenschappelijke vragen over nieuwe [!DNL Target] UI en [!UICONTROL Visual Experience Composer] (VEC), met inbegrip van navigatieveranderingen, eigenschapplaatsen, en de veroudering van de tijdelijke UI versiesknevel. Of u nu een markeerteken, ontwikkelaar of beheerder bent, deze veelgestelde vragen helpen u een vloeiende overgang te maken en de bijgewerkte gebruikersinterface optimaal te benutten.

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
