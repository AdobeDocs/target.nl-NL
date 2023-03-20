---
keywords: Opmerkingen bij de release;pre-releaseopmerkingen;toekomstige verbeteringen;toekomstige correcties;toekomstige functies;aanstaande release
description: Een lijst weergeven met functies, verbeteringen en oplossingen die zijn opgenomen in eerdere versies van Adobe Target.
title: Welke functies zijn opgenomen in vorige releases?
feature: Release Notes
exl-id: e4d261a1-d3aa-46ea-b1ce-efa76a90dc71
source-git-commit: b9dd74e40e1c7a4eeafc749aca585aa538511c70
workflow-type: tm+mt
source-wordcount: '35428'
ht-degree: 0%

---

# Opmerkingen bij de release van vorige releases

Opmerkingen bij de release van vorige [!DNL Adobe Target] releases, inclusief releaseopmerkingen voor [!DNL Target Standard/Premium]de [!DNL Target] en de [!DNL Target] Javascript-bibliotheek (at.js).

Opmerkingen bij de release worden in aflopende volgorde weergegeven per maand en jaar van de release.

>[!NOTE]
>
>Zie [Opmerkingen bij de doelversie (huidig)](/help/main/r-release-notes/release-notes.md#reference_8FE40B43A5A34DDF8F26A53D55EE036A) voor informatie over de Target-releases van de huidige maand (platform en Target Standard/Premium).

## Opmerkingen bij de release - 2023

### [!DNL Target] Standard/Premium 22.15.1 (8 en 9 maart 2023)

Deze release is beschikbaar volgens het volgende schema:

* **8 maart**: Amerikaanse regio
* **9 maart**: Europa, Midden-Oosten en Afrika (EMEA)
* **9 maart**: Regio Azië-Stille Oceaan (APAC)

>[!NOTE]
>
>Vanwege problemen die sindsdien zijn verholpen, zijn de &quot;Geoptimaliseerde A4T metriek voor [!UICONTROL Auto-Allocate] en [!UICONTROL Auto-Target]De functie &quot; die op 8 en 9 maart is uitgebracht, is tijdelijk verwijderd. Na verdere interne tests wordt de functie in de komende weken opnieuw vrijgegeven.

Deze versie bevat de volgende oplossingen:

* Updates voor het ontwerpen van aangepaste webcomponenten met de [!UICONTROL Visual Experience Composer] (VEC):

   * De Vaste de elementenselectie van de Schaduw DOM in VEC door het auteursproces te verbeteren zodat is er geen afhankelijkheid van [!DNL Target] implementatietype bij het ontwerpen van de schaduwhoofdmap. Het selecteren van Schaduw-DOM-elementen in de VEC werkt nu voor elke website.
   * Probleem opgelost waarbij het laden van HTML-elementen met #Shadow DOM in de VEC werd voorkomen. (TGT-35801)
   * VEC-problemen met SPA websites opgelost met ShadowDOM. (TGT-43169)
   * Probleem verholpen met de optimalisatiedoelstelling: &quot;clicked an element&quot; dat de CSS-kiezer niet correct identificeerde in ShadowDOM.

>[!NOTE]
>
>Zorg ervoor dat u een [!DNL Target] SDK ([at.js](https://developer.adobe.com/target/implement/client-side/atjs/target-atjs-versions/){target=_blank} or [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html){target=_blank} (alloy.js) met een versie groter dan 2.8.

**Bekend probleem**: Klikken en volgen op een schaduwbasiselement bij gebruik [!DNL Adobe Experience Platform Web SDK] werkt niet correct. (TNT-47012)

### at.js versie 2.10.2 (7 maart 2023)

* Het probleem dat de oorzaak was van de `trackEvent` om altijd een fout te retourneren.

Voor informatie over alle versies at.js, zie [details van de at.js-versie](https://developer.adobe.com/target/implement/client-side/atjs/target-atjs-versions/){target=_blank} in the [Adobe Target Developer Guide](https://developer.adobe.com/target/){target=_blank}.

### [!DNL Target] Standard/Premium 22.14.5 (13-15 februari 2023)

Deze release is beschikbaar volgens het volgende schema:

* **13 februari**: Amerikaanse regio
* **15 februari**: Europa, Midden-Oosten en Afrika (EMEA)
* **15 februari**: Regio Azië-Stille Oceaan (APAC)

Deze versie bevat de volgende oplossingen:

* Probleem verholpen dat het volgende foutbericht veroorzaakte, ook al was een eigenschap opgegeven in Automated Personalization (AP)-activiteiten: &quot;Fouten: Minstens één eigenschap moet tot een niet-standaardwerkruimte&quot; (TGT-44607) behoren
* Oplossing voor een mogelijk beveiligingsprobleem dat gevolgen had voor Recommendations-feeds aan de serverzijde. (TGT-43769)

### at.js versie 2.10.1 (2 februari 2023)

* Probleem verholpen waarbij activiteiten waarbij publieksregels betrokken waren die parameters met punten in hun namen bevatten, niet de verwachte ervaring retourneren, voor het bepalen van het apparaat.
* Oplossing voor een bug die in at.js 2.6.0 werd geïntroduceerd waarin at.js een leveringsvraag, zelfs afvuurde wanneer `mboxDisable` is ingeschakeld.

Voor informatie over alle versies at.js, zie [details van de at.js-versie](https://developer.adobe.com/target/implement/client-side/atjs/target-atjs-versions/){target=_blank} in the [Adobe Target Developer Guide](https://developer.adobe.com/target/){target=_blank}.

### [!DNL Target] Standard/Premium 22.13.3 (25-26 januari 2023)

Deze release is beschikbaar volgens het volgende schema:

* **25 januari**: Europa, Midden-Oosten en Afrika (EMEA)
* **25 januari**: Regio Azië-Stille Oceaan (APAC)
* **26 januari**: Amerikaanse regio

Deze release bevat de volgende nieuwe functies, verbeteringen en oplossingen:

| Functie | Details |
| --- | --- |
| [JSON-aanbieding](/help/main/c-experiences/c-manage-content/create-json-offer.md) ondersteuning in Automated Personalization (AP) | Extra ondersteuning voor JSON-aanbiedingen in [!UICONTROL Automated Personalization] (AP) activiteiten met behulp van de Form-Based Experience Composer. (TGT-41460) |
| [AEM ervaren fragmenten](/help/main/c-experiences/c-manage-content/aem-experience-fragments.md) | De mogelijkheid toegevoegd om onderscheid te maken tussen [!DNL Adobe Experience Manager] fragmenttypen (AEM XF) die worden geëxporteerd naar [!DNL Target]. In plaats van de optie Fragment ervaren, [!DNL Target] kunt u nu filteren en zoeken op &quot;HTML XF&quot; en &quot;JSON XF&quot;. (TGT-44132) |

* Probleem verholpen waarbij de fout &quot;500&quot; werd veroorzaakt in [!UICONTROL A/B Test] en [!UICONTROL Experience Targeting] (XT) activiteiten die aanbevelingen bevatten. Dit probleem is ontstaan toen [!DNL Target] heeft niet correct criteria-objecten uit het [!DNL Target] UI en [!DNL Recommendations] back-end die niet meer in gebruik zijn. (TGT-44383)
* De locatie is verwijderd uit de naam van de weergegeven aanbieding in het dialoogvenster [!UICONTROL Offer Level] verslag voor [!UICONTROL Automated Personalization] activiteiten. Deze wijziging maakt het verslag leesbaarder. (TGT-44294)
* De kalenderopties van 45 dagen en 90 dagen zijn verwijderd uit het toegangspunt en [!UICONTROL Auto-Target] [!UICONTROL Personalization Insights] en [!UICONTROL Important Attributes] in de [!DNL Target] UI. Vanwege gebruikspatronen en om de prestaties te verbeteren, zijn deze datumbereiken afgekeurd. De interface is bijgewerkt om de momenteel toegestane bereiken te weerspiegelen: 15, 30 en 60 dagen. (TGT-39357)
* De mogelijkheid om de [!UICONTROL Same as Optimization Goal] instellen op de [!UICONTROL Goals & Settings] pagina nadat de activiteit live is. (TGT-43923)
* Probleem verholpen dat problemen veroorzaakte met de standaardwerkplek in de [!DNL Target] back-end bij upgrade vanaf [!DNL Target Standard] tot [!DNL Target Premium]. (TGT-44081 &amp; TGT-44306)
* Een wijziging aanbrengen om toe te staan [!DNL Analytics] rapporteert versies met een puntteken &quot;.&quot; in de namen die in de [!DNL Target] UI voor het maken van [!DNL Analytics] classificatieffeeds.
* De koppeling op het tabblad [!UICONTROL Implementation] pagina ([!UICONTROL Administration] > [!UICONTROL Implementation]) voor &quot;Implementatiemethodes met Apparaatbesluit&quot; om te verwijzen naar de pagina met uitleg over het gebruik van apparaatbeslissingen voor alle ondersteunde SDK&#39;s: Node.js, Java, .NET, en Python. Zie voor meer informatie [Aan de slag met doel-SDK&#39;s](https://developer.adobe.com/target/implement/server-side/sdk-guides/getting-started/){target=_blank} in the [Adobe Target Developer Guide](https://developer.adobe.com/target/){target=_blank}.
* Probleem verholpen die bij het gebruik van bestanden problemen bij het uploaden veroorzaakte. [!DNL Scene7] en [!DNL Target].
* De toegankelijkheid van de [!DNL Target] UI voor personen met een handicap door resultaten van een interne bruikbaarheidscontrole te gebruiken. Deze toegankelijkheidsverbeteringen omvatten toegang tot functies die voorheen niet via het toetsenbord toegankelijk waren, alt-tekstverbeteringen, de mogelijkheid om te zoomen op onderdelen van de gebruikersinterface om bruikbaarder te zijn, verbeterde toetsenbordfocus en meer.   (TGT-42759)
* Verschillende lokalisatieoplossingen in de hele [!DNL Target] UI.

## Opmerkingen bij de release - 2022

### Models API-release (23 november 2022)

De nieuwe [!DNL Adobe Target] De model API, ook genoemd de Lijst van gewezen personen API, laat gebruikers de lijst van eigenschappen bekijken en beheren die in machine het leren modellen worden gebruikt voor [!UICONTROL Automated Personalization] (AP) en [!UICONTROL Auto-Target] (AT) activiteiten.

Zie voor meer informatie [Modellen API - Overzicht](https://developer.adobe.com/target/before-administer/models-api/){target=_blank} in de *Adobe Target Developer Guide*.

### [!DNL Target] Standard/Premium 22.10.3 (gefaseerde release 25-27 oktober 2022)

Deze versie bevat de volgende oplossingen:

* Extra knopinfo in het dialoogvenster [!DNL Target] UI om klanten te helpen efficiënter navigeren de publieksbouwer en te leren hoe te om eigenschappen te gebruiken die onvertrouwd zouden kunnen zijn. (TGT-44139)
* Extra functionaliteit om te voorkomen dat klanten een activiteit bewerken die door [!DNL Target] omdat er niet-ondersteunde meetgegevens worden gebruikt. Een bericht in UI geeft klanten de opdracht om de activiteit te dupliceren en dan omzettings metrisch bij te werken.

   Met deze release `averagetimespentonsite`, `bouncerate`, en `entries` maatstaven in [!DNL Target] de activiteiten zullen worden vervangen voor nieuwe activiteiten . Bestaande activiteiten kunnen deze cijfers tot mei 2023 blijven gebruiken.

* Knopinfo toegevoegd in het dialoogvenster [!DNL Target] UI om klanten te helpen een optimalisatiecriteria te selecteren terwijl het creëren van of het uitgeven van een [!UICONTROL Auto-Target] activiteit die A4T gebruikt.

### [!DNL Target] Standard/Premium 22.10.1 (gefaseerde release 10-13 oktober 2022)

Deze release bevat de volgende nieuwe functies, verbeteringen en oplossingen:

| Functie | Details |
| --- | --- |
| [!DNL Adobe Experience Manager] (AEM) fragmenten ervaren | Tot de updates voor de functie voor fragmenten met AEM ervaring behoren:<ul><li>De mogelijkheid om te filteren AEM ervaringsfragmenten op type (HTML of JSON) in de [!UICONTROL Offers] lijst. (TGT-43121)</li><li>Probleem verholpen waarbij klanten JSON konden invoegen. [!UICONTROL Experience Fragment] biedt aan wanneer het gebruiken van VEC, dat niet wordt gesteund. JSON-aanbiedingen kunnen alleen worden ingevoegd wanneer u de [!UICONTROL Form-Based Experience] composer. (TGT-43846)</li></ul>Zie AEM voor meer informatie [ervaringsfragmenten](/help/main/c-experiences/c-manage-content/aem-experience-fragments.md). |
| Nieuw [!UICONTROL Visual Experience Composer] extensie voor Google Chrome | Een nieuwe [!DNL Adobe Target] [!UICONTROL Visual Experience Composer] (VEC) extensie voor Chrome is beschikbaar in de Chrome Web Store.<br>Vanaf januari 2023 wordt de huidige [!DNL Target] De extensie VEC Helper werkt niet meer in Google Chrome omdat Google extensies niet toestaat met Manifest V2. Download de nieuwe extensie om uw websites visueel te blijven ontwerpen in [!DNL Target] vanaf het nieuwe jaar.<br>De volgende koppelingen tonen de twee extensies in de Chrome Web Store:<ul><li>[Nieuwe extensie](https://chrome.google.com/webstore/detail/adobe-experience-cloud-vi/kgmjjkfjacffaebgpkpcllakjifppnca){target=_blank}</li><li>[Oude extensie](https://chrome.google.com/webstore/detail/adobe-target-vec-helper/ggjpideecfnbipkacplkhhaflkdjagak){target=_blank}</li></ul>Zie voor meer informatie [De extensie Visuele bewerkingshulp](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/visual-editing-helper-extension.md). |
| Documentatie-updates | De belangrijkste documentatieupdates omvatten het volgende:<ul><li>Nieuw en bijgewerkt [Adobe Target Admin en Reporting API-documentatie](https://developer.adobe.com/target/administer/admin-api/){target=_blank} includes comprehensive coverage of Admin and Reporting API endpoints, including properties, offers, hosts, environments, clients, audiences, activities, and more.<br>See this and additional developer content in the [[!DNL Adobe Target] [!UICONTROL Developer Guide]](https://developer.adobe.com/target/){target=_blank}.</li><li>[Statistische berekeningen voor A/Bn-tests](/help/main/c-reports/statistical-methodology/statistical-calculations.md)<br>In dit artikel worden de gedetailleerde statistische berekeningen beschreven die in de handmatige A/Bn-tests in [!DNL Adobe Target].<br>De informatie in dit artikel vervangt de *Adobe Target-berekeningen voor A/B-tests* pdf-bestand dat eerder beschikbaar was voor downloaden op deze site.</li></ul> |

* Probleem verholpen waardoor de publieksregelgegevens niet correct konden worden weergegeven in het dialoogvenster [!UICONTROL Audiences Refinements] informatievenster. (TGT-43917)
* De prestaties van de [!DNL Target] UI bij het laden van publiek dat de [aanbevolen limiet voor doelgroepregels](/help/main/r-troubleshooting-target/target-limits.md#targeting-rules). (TGT-43675)
* Probleem verholpen waarbij sommige componenten niet correct werden weergegeven in het dialoogvenster [!UICONTROL Modifications] op het [!UICONTROL Experiences] pagina wanneer het creëren van of het uitgeven van activiteiten in VEC na omschakeling van [!UICONTROL Compose] tot [!UICONTROL Browse] in. (TGT-43300)
* Probleem verholpen waardoor sommige klanten niet konden archiveren [!UICONTROL A/B Test] activiteiten die [!UICONTROL Auto-Target]. (TGT-40978)
* De mogelijkheid toegevoegd om automatisch één aanbieding te gebruiken op meerdere locaties binnen één rapportagegroep. (TGT-40689)

### [!DNL Target] Standard/Premium 22.9.1 (gefaseerde release 13-15 september 2022)

Deze release is beschikbaar volgens het volgende schema:

* **13 september**: Europa, Midden-Oosten en Afrika (EMEA)
* **14 september**: Amerikaanse regio
* **15 september**: Regio Azië-Stille Oceaan (APAC)

Deze versie bevat de volgende verbeteringen en oplossingen:

* Toegevoegde [!UICONTROL Cross-Domain] tijdens het downloaden naar .js 2.10.0 (en hoger) om het instellen van cookies van derden toe te staan of uit te schakelen. (TGT-43674)
* Bijgewerkte meldingen in de [!DNL Target] UI om klanten te informeren als de invoer van [!DNL Recommendations] feeds mislukt. (TGT-35811)
* Probleem verholpen dat ertoe heeft geleid [!UICONTROL Decision Offers] niet naar behoren binnen de [!UICONTROL Visual Experience Composer] (VEC). (TGT-43866)
* Probleem verholpen waarbij een foutbericht werd weergegeven wanneer u het selectievakje [!UICONTROL Clicked an Element] conversiedoel tijdens het maken van een [!UICONTROL Multivariate Testing] (MVT) activiteit. (TGT-43842)
* Het probleem dat ervoor zorgde dat de [!UICONTROL Impressions] kolom van het tonen in het gedownloade CSV- rapportdossier voor [!UICONTROL Automated Personalization] (AP) activiteiten. (TGT-43780)
* Probleem verholpen waardoor klanten HTML/JSON-aanbiedingen niet konden bewerken na het dupliceren van ervaringen tijdens het gebruik van de [!UICONTROL Form-Based Experience Composer]. (TGT-43633)
* Probleem verholpen waardoor klanten een [!UICONTROL A/B Test] van een niet-standaardwerkruimte naar een andere niet-standaardwerkruimte. (TGT-41910)
* Probleem verholpen om ervoor te zorgen dat klanten het gebruik van [!DNL Recommendations] objecten (ontwerpen, criteria, verzamelingen, enzovoort) in [!UICONTROL A/B Test] en [!UICONTROL Experience Targeting] (XT) activiteiten die aanbevelingen bevatten en criteria ook schrappen hebben bezwaar die niet meer in gebruik van [!DNL Target] UI en [!DNL Recommendations] achterkant. (TGT-42331)
* Oplossing voor een probleem dat ertoe heeft geleid dat een waarschuwing voor een netwerktime-out wordt weergegeven in het dialoogvenster [!DNL Target] UI bij het ophalen van parameters. (TGT-43737)
* UI-updates zijn gemaakt om ervoor te zorgen dat bepaalde acties voor slepen en neerzetten via het toetsenbord toegankelijk zijn. (TGT-42969)
* UI-updates zijn gemaakt om ervoor te zorgen dat tekstinstellingen correct zijn gelokaliseerd.

### at.js versie 2.10.0 (13 september 2022)

* Toegevoegde [!UICONTROL Cross-Domain] tijdens het downloaden naar .js 2.10.0 (en hoger) om het instellen van cookies van derden toe te staan of uit te schakelen. (TGT-43674)

### [!DNL Target Standard/Premium] 22.8.1 (gespreide release 17-18 augustus 2022)

Deze onderhoudrelease bevat oplossingen voor back-end en lokalisatie.

### [!DNL Target] platformrelease (20 juli 2022)

Deze versie bevat de volgende functies, verbeteringen en oplossingen:

| Functie | Beschrijving |
| --- | --- |
| Verbeterde nauwkeurigheid van de publieksevaluatie en verminderde latentie van de eindgebruiker door IPv6 steun (TNT-43364, TNT-44692) | De geo-plaatsen van bezoekers worden nu bepaald door IPv6 adressen, als beschikbaar, in tegenstelling tot slechts IPv4 adressen. De levering APIs steunt ook IPv6 inputparameters. Het filteren en toestaan-lijst steunen zowel IPv4 als IPv6 adressen. De IPv6-ondersteuning in deze release betekent dat bezoekers nauwkeuriger worden opgenomen in het publiek (kwalificeer nauwkeuriger voor activiteiten of worden opgenomen in filtercriteria). Het verbetert ook gegevenslatentie, aangezien de cliënten IPv6 rechtstreeks zullen leiden, vermijdend de overheadkosten van de gateway IPv6-aan-IPv4. |
| Vast probleem met de afhandeling van betalingen aan de client-side A4T (TNT-44926) | Met integratie op de server-side van A4T, als Adobe Target een verzoek als afkomstig van beide identificeert, stuurt het niet de nuttige lading naar Analytics, en er is geen mod_stats gebeurtenis in geregistreerd in [!DNL Target] logboeken. Met deze versie, is het cliënt-zijregistreren A4T verbeterd zodat het gedrag met betrekking tot de A4T lading het zelfde als met server-kant A4T is: Bezoekers die als bots zijn geïdentificeerd, worden uitgesloten van [!DNL Target] tellen/rapporteren. (Let op: het probleem in kwestie was beperkt tot implementaties die gebruik maakten van client-side payload handling; server-kant niet beïnvloed. Met deze release is het gedrag nu consistent voor zowel server-side als client-side payload-afhandeling.) |

### [!DNL Target Standard/Premium] 22.6.2 (30 juni 2022)

Deze versie bevat de volgende functies, verbeteringen en oplossingen:

| Functie | Beschrijving |
| --- | ---  |
| Meldingen in producten | Verkrijg de volgende relevante in-product berichten:<ul><li>**Activiteiten**: Meldingen voor alle soorten activiteiten wanneer een activiteit handmatig wordt goedgekeurd of gedeactiveerd of wanneer de begin- of einddatum wordt bereikt. Het bericht bevat de naam van de activiteit met een koppeling naar de overzichtspagina van de activiteit.</li><li>**Profielscripts** Meldingen wanneer een profielscript handmatig of door Doel is geactiveerd of gedeactiveerd.</li><li>**Recommendations feeds**: Meldingen wanneer een Recommendations-feed handmatig of via Target is geactiveerd of gedeactiveerd. Meldingen worden ook verzonden wanneer een Recommendations-feed mislukt.</li></ul> Standaard worden meldingen ontvangen door productbeheerders, uitgevers en fiatteurs. Meldingen kunnen worden geconfigureerd in de voorkeuren voor Experience Cloud.<br>Zie voor meer informatie [Meldingen en aankondigingen](/help/main/c-intro/understand-the-target-ui.md#notifications-announcements). |
| *Adobe Target Developer Guide* | De *Adobe Target Developer Guide* consolideert alles [!DNL Target] ontwikkelaarsinhoud in één handige handleiding. De gids bevat informatie over de implementatie [!DNL Target] en [!DNL Recommendations], [!DNL Target] SDK&#39;s, en [!DNL Target] API&#39;s.<br>Zie voor meer informatie [Adobe Target Developer Guide](https://developer.adobe.com/target/){target=_blank}. |

* Gebruikers met de [!UICONTROL Editor] rol kan het publiek in live activiteiten niet meer bewerken. (TGT-43582)
* Een waarschuwingsbericht wordt weergegeven als een klant een publiek probeert op te slaan met een uitroepteken ( ! ) als het eerste teken van de naam van het publiek (bijvoorbeeld !Londen). (TGT-43643)
* Probleem verholpen waarbij definitiedetails voor bepaalde klanten werden veroorzaakt om aan te geven dat een beëindigde activiteit nog steeds actief is. (TGT-43527)

### [!DNL Target Standard/Premium] 22.6.1 (gefaseerde release: (7-9 juni 2022)

Deze release is beschikbaar volgens het volgende schema:

* **7 juni**: Regio Azië-Stille Oceaan (APAC)
* **8 juni**: Amerikaanse regio
* **9 juni**: Europa, Midden-Oosten en Afrika (EMEA)

Deze versie bevat de volgende verbeteringen en oplossingen:

* Er is een verbetering voor de nieuwe [!UICONTROL Audiences] pagina om een inconsistente staat tussen het oude gegevensbestand te verhinderen waar het publiek in het verleden en de nieuwe architectuur werd opgeslagen die de informatie direct van het achtereind terugwint. (TGT-43552)
* Probleem verholpen waardoor sommige klanten geen gecombineerd publiek konden opslaan dat was veroorzaakt door het maken van &quot;lege&quot; containers in de doelgebruikersinterface. (TGT-43588)

### Doelplatformversie (25 mei 2022)

Deze versie bevat de volgende verbeteringen en oplossingen:

* Toegevoegd [Clienttips van gebruikersagent](https://developer.adobe.com/target/implement/client-side/atjs/user-agent-and-client-hints/){target=_blank} ondersteuning.
* Probleem verholpen waarbij periodiek time-outs werden veroorzaakt tijdens het renderen [!UICONTROL Offer Decisions] in [!UICONTROL Experience Targeting] (XT) activiteiten. (TNT-44611)

### at.js versie 2.9.0 (27 mei 2022)

* Toegevoegd [Clienttips van gebruikersagent](https://developer.adobe.com/target/implement/client-side/atjs/user-agent-and-client-hints/){target=_blank} ondersteuning.
* Probleem verholpen waarbij meerdere mbox-aanvragen op dezelfde pagina verschillende beeld-id&#39;s hebben.

### [!DNL Target Standard/Premium] 22.5.1 (gespreide vrijgave; mei (11-13 mei 2022)

Deze release is beschikbaar volgens het volgende schema:

* **11 mei**: Regio Azië-Stille Oceaan (APAC)
* **12 mei**: Amerikaanse regio
* **13 mei**: Europa, Midden-Oosten en Afrika (EMEA)

Deze versie bevat de volgende verbeteringen en oplossingen:

* Probleem verholpen dat een JavaScript-fout veroorzaakte en sommige klanten de toegang tot de activiteitsgegevens voor bepaalde [!UICONTROL Automated Personalization] (AP) activiteiten. (TGT-43526)
* Probleem verholpen waardoor sommige klanten geen specifieke aanbieding aan een AP-activiteit konden toevoegen (of bewerken). (TGT-43503)
* Probleem opgelost in het dialoogvenster [!DNL Target] UI die het volgende foutenbericht toonde: &quot;Uw globale box is mogelijk niet synchroon. Probeer het opnieuw op te slaan.&quot; Dit probleem betrof een UI-probleem en had geen invloed op de implementaties van klanten. (TGT-43475)
* Probleem verholpen waardoor één klant geen verfijningen en publiek op ervaringsniveau kon bewerken voor een activiteit als de verfijningen en het publiek vóór de nieuwe [!UICONTROL Audiences] UI is geïmplementeerd. (TGT-43433)
* Het probleem waarbij klanten dubbele gegevens konden selecteren, is opgelost. [!DNL Adobe Audience Manager] (AAM) publiek tijdens het bewerken van het rapportagepubliek voor een activiteit. (TGT-43430)
* Probleem verholpen waardoor klanten geen dubbel publiek konden maken, maar in verschillende werkruimten. (TGT-43423)
* Probleem verholpen waardoor klanten geen locaties konden verwijderen die ad-hocaanbiedingen hadden in activiteiten die in het dialoogvenster [!UICONTROL Form-Based Experience Composer]. (TGT-43315)
* Probleem verholpen waarbij klanten geen toegang kregen tot de aangeboden code nadat ze op de aanbiedingen voor afbeeldingen hadden geklikt en de interface vervolgens hadden vernieuwd. (TGT-43566)
* Probleem verholpen waarbij tijdens het bewerken van profielscripts het oorspronkelijke, onbewerkte script werd hersteld nadat het script was bewerkt, geactiveerd en vervolgens gedeactiveerd. Het profielscript blijft nu in de bewerkte status staan. (TGT-43249)
* Probleem verholpen waarbij de volgende fout is opgetreden bij een poging een publiek naar een andere werkruimte te verplaatsen: &quot;We kunnen je aanvraag niet voltooien. Neem contact op met de Adobe Client Care als het probleem zich blijft voordoen.&quot; (TGT-43212)
* Correctie van een fout die een fout veroorzaakte bij het klonen van aangepaste codewijzigingen voor App-pagina&#39;s (SPA) van één pagina. (TGT-43137)
* Probleem verholpen waarbij de oorspronkelijke aanbieding werd beïnvloed nadat een ervaring was gedupliceerd en de promotie vervolgens was bewerkt. (TGT-41775)

### [!DNL Target Standard/Premium] 22.4.1 (28 april 2022)

Deze versie bevat de volgende oplossing:

* Probleem verholpen waarbij drie op een kar gebaseerde algoritmen dezelfde voorwaarde voor kopen en kopen gebruikten op de knop [!DNL Target] achterkant. (TGT-43456)
* Ingeschakeld [!DNL Target] UI-token vernieuwt voor organisaties die zijn ingeschakeld met [Zakelijke id-accounts](https://helpx.adobe.com/enterprise/using/identity.html){target=_blank} en beleidsgebaseerde verificatie (PBA). (TGT-42590)

### [!DNL Target] platformrelease (27 april 2022)

Deze release bevat de volgende wijziging:

* Met deze release kunt u inhoud vooraf instellen voor [!UICONTROL Auto Personalization] (AP) en [!UICONTROL Auto-Target] (AT) activiteiten (voorheen niet teruggegeven door [!DNL Target]). Dit zou de ervaringen kunnen veranderen het eind - de gebruikers zien in het geval van een pre-fetch vraag (geen veranderingen in &quot;uitvoeren&quot;stroom) als een AP/AT activiteit op de leveringsweg is en hoger in prioriteit dan andere activiteiten AB/XT is die de zelfde plaats voor inhoudslevering gebruiken.

### [!DNL Target] platformrelease (30 maart)

Deze release bevat de volgende verbeteringen:

* De metriek van het klik-spoor zal analytische lading in levering API verzoeken voor activiteiten omvatten die Analytics als rapporteringsbron (A4T) en procesgebeurtenissen op cliënt-kant gebruiken. (TNT-43073)

### [!DNL Target Standard] Vernieuwen van soorten publiek (28 maart)

Deze release bevat de volgende update:

* De nieuwe [!UICONTROL Audiences] De interface wordt voor iedereen ingeschakeld [!DNL Target Standard] klanten.

### Oplossingen voor technische oplossingen voor doelklanten/Premium (22 maart 2022)

Deze onderhoudrelease bevat de volgende verbeteringen:

* Toegevoegde functionaliteit die moet worden geretourneerd [!DNL Analytics] ladingsgegevens voor `prefetch` weergaven en `pageLoad` klik op Metriek wanneer u de [!UICONTROL Delivery API] met activiteiten die [!UICONTROL Analytics as the reporting source] (A4T). (TNT-43198)
* Bijgewerkt de beide het filtreren lijst van gebruikersagent om een browser type toe te staan dat algemeen in Japan wordt gebruikt. (TNT-43867)

### Target Standard/Premium 22.2.1 (1 februari 2022)

Deze onderhoudsversie bevat de volgende oplossingen en verbeteringen voor de nieuwe [!UICONTROL Audiences] UI die in de Versie van het Doel Standard/Premium 22.1.2 wordt aangekondigd die aan klanten over alle gebieden in de volgende zes weken uitrolt. Met deze correcties lijnt u de functionaliteit uit van publiek dat is gemaakt in [!DNL Adobe Target Standard/Premium].

* Probleem verholpen waarbij geïmporteerd publiek werd verhinderd [!DNL Adobe Experience Platform], [!DNL Adobe Experience Cloud], en [!DNL Adobe Target Classic] worden toegewezen als rapportagepubliek. (TGT-43140)
* Toegevoegde [!UICONTROL Delete] in de [!UICONTROL Audiences] lijst voor geïmporteerde soorten publiek uit [!DNL Adobe Experience Platform], [!DNL Adobe Experience Cloud], en [!DNL Adobe Target Classic]. Ook functionaliteit voor bulksgewijs verwijderen toegevoegd. (TGT-42914)

### at.js versie 2.8.1 (28 januari 2022)

* Vast `pageLoad` niet toegewezen aan target-global-mbox in [!UICONTROL On Device Decisioning] (ODD) hybride uitvoeringsmodus.
* Probleem verholpen met analytische details voor mbox-aanvraag.
* Verbeterde dev-afhankelijkheden om beveiligingskwetsbaarheden te verhelpen.

### [!DNL Target Standard/Premium] 22.1.2 (26 januari 2022)

| Functie | Details |
| --- | --- |
| [!DNL Adobe Experience Platform] publiek in [!DNL Target] | U kunt nu consumeren en gebruiken [!DNL Adobe Experience Platform] publiek in [!DNL Target]. De [!DNL Target] team, [!DNL Experience Platform] [!DNL Destinations] en de [!DNL Unified Profile Service] -team is verheugd de algemene beschikbaarheid van de gebruiksgevallen &quot;Zelfde pagina/Volgende pagina aanpassen&quot; aan te kondigen.<br>Het publiek gebruiken dat is gemaakt in [!DNL Adobe Experience Platform] Verstrek rijkere klantengegevens die tot uitvoerigere verpersoonlijking leiden. De [Real-time Customer Data Platform](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/overview.html){target=_blank} (RTCP), built on [!DNL Adobe Experience Platform] helps companies bring together known and anonymous data from multiple enterprise sources to create customer profiles that can be used to provide personalized customer experiences across all channels and devices in real time.<br>For more information, see [Use audiences from Adobe Experience Platform](/help/main/c-target/c-audiences/audiences.md#aep) in *Create audiences*.<br>Be sure to read the Adobe blog and watch the video: [[!DNL Adobe] announces Same Page Enhanced Personalization with [!DNL Adobe Target] and [!DNL Real-time Customer Data Platform]](https://blog.adobe.com/en/publish/2021/10/05/adobe-announces-same-page-enhanced-personalization-with-adobe-target-real-time-customer-data-platform){target=_blank}. |
| [!UICONTROL Audiences] UI vernieuwen | Als onderdeel van het [!DNL Adobe Target] de voortdurende inspanning van het team om de gebruiker-ervaring voor te verbeteren [!DNL Target] gebruikers, deze versie vernieuwt de [!UICONTROL Audiences] en [!UICONTROL Profile Scripts] pagina&#39;s in het dialoogvenster [!DNL Target] UI. Deze update verenigt en normaliseert ontwerppatronen die eerder inconsistent waren, terwijl het toevoegen van nieuwe verhogingen, zoals:<ul><li>De mogelijkheid om meerdere soorten publiek tegelijk te selecteren en te verwijderen</li><li>Een vernieuwd [ontwerp van publiek builder](/help/main/c-target/c-audiences/create-audience.md)</li><li>Ondersteuning voor uitsluitingsregels in het dialoogvenster [!UICONTROL Audience] bibliotheekregelbouwer</li><li>Een nieuw filter &quot;Bron publiek&quot;, waarmee u sneller uw doelgroep kunt detecteren</li><li>Opties voor permanent zoeken en filteren tijdens sessies</li><li>De mogelijkheid om het publiek tussen werkruimten te verplaatsen voor [!DNL Target Premium] klanten.</li></ul>Zie voor meer informatie [Soorten publiek](/help/main/c-target/target.md).<br>**OPMERKING**: Deze functie wordt de komende acht weken uitgerold naar klanten in verschillende regio&#39;s. |
| [!UICONTROL Profile Scripts] UI vernieuwen | De [!UICONTROL Profile Scripts] De bibliotheek is ook bijgewerkt en bevat een vernieuwde interface en diverse productiviteitsupdates:<ul><li>De mogelijkheid om meerdere profielscripts tegelijk te selecteren en te verwijderen</li><li>Een nieuwe code-editor voor profielscripts</li><li>Syntaxis markeren en fout controleren in de code-editor</li><li>Automatisch aanvullen van tokens (mbox of profiel) via sneltoetsen</li></ul>Zie voor meer informatie [Bezoekerprofielen](/help/main/c-target/c-visitor-profile/visitor-profile.md).<br>**OPMERKING**: Deze functie wordt de komende acht weken uitgerold naar klanten in verschillende regio&#39;s. |

### [!DNL Target Standard/Premium] 22.1.1 (12 januari 2022)

Deze release bevat foutoplossingen en de vereiste functies voor toekomstige integratie.

### Doelversie van Platform (13 april 2022)

Deze release bevat de volgende update:

* Probleem opgelost om ervoor te zorgen dat het laatste octet van IP-adressen behoorlijk wordt verduisterd wanneer deze worden vastgelegd met profielscripts. (TNT-44076)

### [!DNL Target Standard/Premium] 22.3.1 (5 april 2022)

Deze release bevat de volgende wijzigingen en verbeteringen:

* Het probleem dat de oorzaak was van de [!UICONTROL Include] en [!UICONTROL Exclude] opties die bij het bewerken van een activiteit moeten worden uitgeschakeld voor een gecombineerd publiek. (TGT-43422)
* Probleem verholpen waardoor sommige klanten de lijst met beschikbare soorten publiek niet konden zien tijdens het bewerken van een activiteit. (TGT-43404)
* Probleem verholpen waardoor sommige klanten een IP-adres niet konden verwijderen van &quot;[!UICONTROL IPs to exclude from [!DNL Target] reporting data]&quot; lijst in [!UICONTROL Administration] > [!UICONTROL Reporting]. (TGT-43384)
* Probleem verholpen waarbij het gebruik van negatieve getallen in publiekscriterium werd voorkomen waarmee werd gecontroleerd of een variabele &quot;groter dan&quot;, &quot;groter dan of gelijk aan&quot;, &quot;kleiner dan&quot; of &quot;kleiner dan of gelijk aan&quot; is. (TGT-43367)
* Probleem verholpen waardoor klanten de [!UICONTROL Audience Details] kaart bij het maken van een gecombineerd publiek. (TGT-43303)

### at.js versie 2.8.0 (7 januari 2022)

De [!DNL Target] in de JavaScript-bibliotheek at.js worden nu gegevens over het gebruik van functies en de prestaties van telemetriegegevens verzameld. Persoonlijke gegevens worden niet verzameld. Afmelden voor deze functie is beschikbaar door de instelling `telemetryEnabled` naar false in `targetGlobalSettings`. Zie voor meer informatie [telemetryEnabled in targetGlobalSettings](https://developer.adobe.com/target/implement/client-side/atjs/atjs-functions/targetglobalsettings/){target=_blank}.

## Opmerkingen bij de release - 2021

### at.js versie 2.7.0 (28 oktober 2021)

Deze release bevat de volgende verbeteringen:

* Extra ondersteuning voor [Webcomponenten](https://developer.mozilla.org/en-US/docs/Web/Web_Components). Deze versie van at.js wordt vereist om gepersonaliseerde ervaringen en aanbiedingen op douaneelementen en op elementen binnen douaneelementen tot stand te brengen en te testen. Deze functionaliteit is opgenomen in de [!DNL Target Standard/Premium] Release 21.10.5.

### [!DNL Target Standard/Premium] 21.10.5 (28 oktober 2021)

Deze onderhoudrelease bevat de volgende verbeteringen:

| Functie | Details |
| --- | --- |
| [!UICONTROL Visual Experience Composer] (VEC) | Extra ondersteuning voor [Webcomponenten](https://developer.mozilla.org/en-US/docs/Web/Web_Components). U kunt persoonlijke ervaringen en aanbiedingen maken en testen op aangepaste elementen en op elementen in aangepaste elementen.<br>Zie voor meer informatie [Opties voor Visual Experience Composer](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md#custom). |

### [!DNL Target Standard/Premium] 21.10.4 (21 oktober 2021)

Deze onderhoudrelease bevat de volgende verbeteringen:

| Functie | Details |
| --- | --- |
| Recommendations op basis van winkelwagentjes | Er is een nieuwe reeks algoritmen toegevoegd om aanbevelingen te doen op basis van de inhoud van het winkelwagentje van de bezoeker.<br>Zie &quot;Op winkelwagentje gebaseerd&quot; in [Criteria maken](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md), &quot;Winkelwagentjes toevoegen/winkelwagentjes weergeven/uitchecken van pagina&#39;s&quot; en &quot;Items uitsluiten die zich al in de winkelwagentje van de bezoeker bevinden&quot; in [Recommendations plannen en implementeren](https://developer.adobe.com/target/implement/recommendations/){target=_blank}en op basis van winkelwagentje in [De aanbeveling baseren op een aanbevelingen](/help/main/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md). |

### [!DNL Target Standard/Premium] 21.10.3 (19 oktober 2021)

Deze onderhoudrelease bevat de volgende verbeteringen, correcties en wijzigingen:

* Opgeloste problemen waardoor klanten de [!UICONTROL A4T] in [!DNL Analysis Workspace] door op de knop [!UICONTROL View in Analytics] knop in [!DNL Target] activiteitenrapportage. (TGT-42099, TGT-42100)
* Het probleem dat de oorzaak was van de [!UICONTROL Edit Design] knop niet weergeven tijdens bewerken [!UICONTROL A/B Test] en [!UICONTROL Experience Targeting] (XT) activiteiten die de [!UICONTROL Form-Based Experience Composer]. (TGT-41980)
* Het probleem dat ervoor zorgde dat de [!UICONTROL Compatible] selectievakje van weergave in selectie criteria tijdens het maken van een nieuwe [!UICONTROL Recommendations] activiteit. (TGT-42053)
* Probleem verholpen waarbij een foutbericht werd weergegeven dat niet kon worden geselecteerd [!DNL Analytics] als rapportagebron (A4T) wegens gebrek aan [!DNL Analytics] machtigingen. (TGT-41954)
* Geïmplementeerde veelvoudige toegankelijkheidsmoeilijke situaties om toetsenbordnavigatie over de [!DNL Target] UI.

### [!DNL Target Standard/Premium] 21.10.2 (13 oktober 2021)

De volgende verbeteringen zijn toegevoegd tijdens het gebruik [!DNL Target] [!UICONTROL Audiences] met de [!DNL Adobe Experience Platform Web SDK]:

* Er zijn waarschuwingspictogrammen, popovers en berichten toegevoegd op verschillende plaatsen in het dialoogvenster [!DNL Target] UI om aan te geven dat het publiek bij de bron is verwijderd en niet langer beschikbaar is voor gebruik in [!DNL Target] activiteiten.

   In de volgende afbeeldingen ziet u een aantal plaatsen waar de pictogrammen, popovers en berichten worden weergegeven:

   * [!UICONTROL Activity] lijstpagina

      ![Publiek verwijderd bij bronbericht op pagina Activiteiten](assets/deleted-at-source-audiences-list.png)

   * Activiteit [!UICONTROL Overview] pagina&#39;s:

      ![Publiek verwijderd bij bronbericht op overzichtspagina](assets/deleted-at-source-overview.png)

   * [!UICONTROL Experiences] stap van de workflow voor het maken van activiteiten:

      ![Publiek verwijderd bij bronbericht op [!UICONTROL Experiences] page](assets/deleted-at-source-experiences.png)

   * [!UICONTROL Targeting] stap van de workflow voor het maken van activiteiten:

      ![Publiek verwijderd bij bronbericht op [!UICONTROL Targeting] page](assets/deleted-at-source-targeting.png)

   * [!UICONTROL Goals & Settings] stap van de workflow voor het maken van activiteiten:

      ![Publiek verwijderd bij bronbericht op de [!UICONTROL Goals & Settings] page](assets/deleted-at-source-goals-settings.png)

   * Poortverfijningen ([!UICONTROL Replace Audience] op de [!UICONTROL Targeting] stap van de workflow voor het maken van activiteiten):

* Als u de functie Soorten publiek combineren probeert te gebruiken en een van de soorten publiek bij de bron is verwijderd, [!UICONTROL Save] is uitgeschakeld.

### [!DNL Target Standard/Premium] 21.10.1 (6 oktober 2021)

Deze release bevat de volgende nieuwe functies:

| Functie | Details |
| --- | --- |
| [!UICONTROL Audiences] UI vernieuwen | Als onderdeel van het [!DNL Adobe Target] de voortdurende inspanning van het team om de gebruiker-ervaring voor te verbeteren [!DNL Target] gebruikers, deze versie vernieuwt de [!UICONTROL Audiences] en [!UICONTROL Profile Scripts] pagina&#39;s in het dialoogvenster [!DNL Target] UI. Deze update verenigt en normaliseert ontwerppatronen die eerder inconsistent waren, terwijl het toevoegen van nieuwe verhogingen, zoals:<ul><li>De mogelijkheid om meerdere soorten publiek tegelijk te selecteren en te verwijderen</li><li>Een vernieuwd [ontwerp van publiek builder](/help/main/c-target/c-audiences/create-audience.md)</li><li>Ondersteuning voor uitsluitingsregels in het dialoogvenster [!UICONTROL Audience] bibliotheekregelbouwer</li><li>Een nieuw filter &quot;Bron publiek&quot;, waarmee u sneller uw doelgroep kunt detecteren</li><li>Opties voor permanent zoeken en filteren tijdens sessies</li></ul>Zie voor meer informatie [Soorten publiek](/help/main/c-target/target.md). |
| [!UICONTROL Profile Scripts] UI vernieuwen | De [!UICONTROL Profile Scripts] De bibliotheek is ook bijgewerkt en bevat een vernieuwde interface en diverse productiviteitsupdates:<ul><li>De mogelijkheid om meerdere profielscripts tegelijk te selecteren en te verwijderen</li><li>Een nieuwe code-editor voor profielscripts</li><li>Syntaxis markeren en fout controleren in de code-editor</li><li>Automatisch aanvullen van tokens (mbox of profiel) via sneltoetsen</li></ul>Zie voor meer informatie [Bezoekerprofielen](/help/main/c-target/c-visitor-profile/visitor-profile.md). |
| [!BADGE Premium]{type=Positive url="/help/main/c-intro/intro.md#premium newtab=true" tooltip="Zie wat er in Target Premium is opgenomen."} | De [!UICONTROL Recommendations Criteria] de workflow voor het maken en bewerken van bestanden is gestroomlijnd om het kiezen van het juiste algoritme en de juiste instellingen voor het uitvoeren van aanbevelingen te vereenvoudigen.<br>Zie voor meer informatie [Criteria maken](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md). |
| ![Premium badge](/help/main/assets/premium.png) Verbeteringen in de snelheid van Recommendations-terugzoekvensters en -algoritmes | U kunt de algoritmen &quot;Meest bekeken&quot; en &quot;Hoogste verkopers&quot; nu uitvoeren met een terugkijkvenster van zes uur om de inhoud vast te leggen die het laatst wordt doorzocht. Wanneer het terugkijkvenster van zes uur wordt geselecteerd, worden uw aanbevelingen resultaten bijgewerkt om de 3-6 uur door de dag.<br>Zie voor meer informatie [Gegevensbron](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md#data-source) in *Criteria maken*. |

### [!DNL Target Standard/Premium] 21.9.1 (14 september 2021)

Deze onderhoudsversie bevat de volgende verbeteringen, correcties en wijzigingen.

* Problemen verholpen waardoor klanten zich niet konden aanmelden bij de [!UICONTROL Visual Experience Composer] (VEC) vanwege het nieuwe beveiligingsbeleid voor cookies van derden in sommige webbrowsers. Dit probleem is besproken in &quot;Pagina&#39;s die niet worden geladen in Visual Experience Composer (VEC) of Enhanced Experience Composer (EEC) bij gebruik van Google Chrome versie 80+&quot; in [Problemen oplossen met betrekking tot Visual Experience Composer en Enhanced Experience Composer](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/issues-related-to-the-visual-experience-composer-vec-and-enhanced-experience-composer-eec.md).
* Probleem verholpen waarbij aanbiedingsnamen in de VEC het pad van de aanbieding weergeven in plaats van de vriendelijke naam van de aanbieding. (TGT-41300)
* Ervaringsnamen worden nu weerspiegeld in [!DNL Analysis Workspace] voor A4T-activiteiten (TGT-38674)
* Probleem opgelost in [!DNL Recommendations] die ten onrechte een entiteit-id heeft toegepast, wijzigt een promotie in een gedupliceerde activiteit in de oorspronkelijke activiteit. (TGT-41482)
* Probleem verholpen waardoor de knop &quot;Criteria bewerken&quot; niet correct werd weergegeven op de knop [!UICONTROL Experiences] pagina voor [!DNL Recommendations] activiteiten in de VEC. (TGT-39512)
* Probleem verholpen waarbij synchronisatie van activiteiten tijdens het dupliceren en kopiëren naar een testwerkruimte werd voorkomen. (TGT-40686)
* Probleem verholpen waardoor wijzigingen in een kiezer met [ervaringsfragmenten](/help/main/c-experiences/c-manage-content/aem-experience-fragments.md) wanneer u &quot;[!UICONTROL Insert After]&quot; in de VEC. (TGT-41802)
* Probleem verholpen waarbij lege JSON-inhoud in een aanbieding niet naar de achtergrond kon worden verzonden. [!DNL Target] verzendt nu het JSON-object, ook al is het leeg. (TGT-41555)
* Probleem verholpen dat veroudering veroorzaakte. [!DNL Analytics] rapporteren om te openen in plaats van [!DNL Analysis Workspace] wanneer klanten op &quot;[!UICONTROL View in Analytics]&quot; tijdens het bekijken van een rapport. (TGT-41867)
* Extra verduidelijking toegevoegd aan het weergegeven UI-bericht wanneer een klant probeert [!DNL Analytics] als bron voor de rapportage (A4T) voor een [!UICONTROL Automated Personalization] activiteit. In het bericht staat: &quot;[!DNL Target] is de enige ondersteunde bron voor [!UICONTROL Automated Personalization] activiteiten.&quot; (TGT-41954)
* Er is extra verduidelijking toegevoegd aan het foutbericht wanneer klanten proberen hosts te scheiden met &quot;newline&quot; in plaats van met komma&#39;s. (TGT-40671)
* Het probleem dat sommige activiteiten veroorzaakte, is opgelost. &quot;[!UICONTROL Last Updated]&quot; datums die moeten verschillen van de Engelse gebruikersinterface voor Spaanse en Japanse klanten (wanneer de gebruikersinterface wordt weergegeven in het Spaans en Japans). (TGT-38980)

### om 2.6.1.2021 (16 augustus 2021)

* Bugcorrectie voor &quot;Geen artefact in cache beschikbaar voor hybride modus&quot; bij gebruik van apparaatbeslissingen.

### [!DNL Target] node.js SDK 2.2.0 (11 augustus 2021)

* Toegevoegde SDK-telemetriegegevensverzameling
* Automated Delivery API client openapi-codegen

Voor meer informatie over deze en vorige versies raadpleegt u de [Logbestand wijzigen](https://github.com/adobe/target-nodejs-sdk/blob/main/CHANGELOG.md) in de [Doelnode.js SDK-documentatie](https://github.com/adobe/target-nodejs-sdk) op Github.

### [!DNL Target Standard/Premium] 21.8.1 (10 augustus 2021)

Deze onderhoudsversie bevat vele achterste verbeteringen, waaronder de volgende klantgerichte wijziging:

* Probleem verholpen waarbij rapporten werden gegenereerd voor [!UICONTROL Auto Personalization] in de [!UICONTROL Form-Based Experience Composer] om te verwijzen naar verwijderde aanbiedingen in rapporten. Dit gaf het volgende foutenbericht aan vertoning toe, &quot;wij hebben probleem het terugwinnen van gegevens voor dit rapport. Neem contact op met de Adobe Client Care als het probleem zich blijft voordoen.&quot; (TGT-41028)

### API voor doellevering (3 augustus 2021)

Deze release bevat de volgende verbeteringen:

* De limiet voor mbox-parameters is verhoogd tot 100 parameters. De vorige limiet was 50 parameters. (TNT-41717)
* De limiet voor `categoryId` is verhoogd tot 256 tekens. De vorige limiet was 128 tekens.
* Het volgende [!DNL Adobe Audience Manager] (AAM) Er zijn gegevens toegevoegd aan de API voor levering:

   * UUID AAM: De interne AAM-id die wordt gebruikt om een gebruiker op unieke wijze te identificeren.
   * dataPartnerId: Identiteitskaart voor een gegevenspartner.
   * dataPartnerUserId: De gebruikers-id die door een gegevenspartner wordt verstrekt.

   Eerder was de leverings-API inbegrepen `dcsLocationHint` en `blob` alleen. (TNT-41644)

### [!DNL Target Standard/Premium] 21.6.1 (30 juni 2021)

Deze versie bevat de volgende nieuwe functies en verbeteringen. De uitgiftenummers tussen haakjes zijn voor intern [!DNL Adobe] gebruik.

| Functie | Details |
| --- | --- |
| [!UICONTROL Analytics for Target] (A4T) | Klik op de knop &quot;[!UICONTROL View in Analytics]&quot; koppeling op de [!UICONTROL Reports] pagina van een activiteit die gebruikt [!DNL Analytics] als rapportagebron (A4T), [!DNL Analysis Workspace] wordt nu geopend. Eerder werd de koppeling geopend [!DNL Analytics] rapportage. (TGT-36959) |

### Python SDK 1.0.0 (16 juni 2021)

De nieuwe [!DNL Adobe Target] Python SDK met mogelijkheden voor het bepalen van apparaten is nu beschikbaar. Deze nieuwste toevoeging versterkt de [!DNL Target] suite SDK&#39;s aan serverzijde. Met deze SDK&#39;s kunt u integreren [!DNL Target] en versnelt u de waardetijd in de taal van uw keuze. Integraties aan de serverzijde worden een populaire keuze, aangezien de markt verschuift naar een wereld zonder cookie waarin gegevens van de eerste partij waardevol zijn. DoelSDK&#39;s zijn beschikbaar in de populairste programmeertalen op de markt (Python, Java, JavaScript, C# / .Net).

Zie voor meer informatie de [Python SDK-documentatie](https://developer.adobe.com/target/implement/server-side/python/){target=_blank} in the [Adobe Target Developer Guide](https://developer.adobe.com/target/){target=_blank}.

### Target Standard/Premium 21.5.1 (7 juni 2021)

Deze release bevat de volgende verbeteringen:

| Functie | Details |
| --- | --- |
| ![Premium badge](/help/main/assets/premium.png) [!DNL Recommendations] [!UICONTROL Catalog Search] API | Zoeken in uw [!DNL Recommendations] product- en inhoudscatalogus worden via de API programmatisch weergegeven om items te identificeren die voldoen aan een zoekcriterium en om het beheer van uw catalogus te vereenvoudigen.<br>**Beperkingen en opmerkingen**:<ul><li>Cataloguszoekopdrachten via API worden niet ondersteund voor omgevingen met meer dan 2.000.000 items.</li><li>Zoekresultaten voor catalogi via de API worden sneller bijgewerkt dan zoekresultaten voor catalogi via de [!DNL Target] UI. De cataloguszoekopdracht in het dialoogvenster [!DNL Target] De gebruikersinterface kan extra tijd vergen om de meest recente resultaten weer te geven.</li></ul>Zie voor meer informatie [Zoeken in entiteiten](https://developers.adobetarget.com/api/recommendations/#tag/Searching-Entities) in de *[!DNL Adobe Target][!DNL Recommendations] API* hulplijn. |

Deze release voor onderhoudsdoeleinden bevat de volgende oplossingen.

* Probleem verholpen waarbij de standaardwerkruimte werd gewijzigd in een andere werkruimte tijdens het vernieuwen van de [!UICONTROL Audiences] pagina. (TGT-38871)
* Probleem opgelost in [!UICONTROL Administration] > [!UICONTROL Implementation] soms is er een foutbericht opgetreden met de tekst &#39;&#39;Uw globale box is mogelijk niet synchroon. Probeer het opnieuw op te slaan.&quot;

### ![Adobe Experience Platform Web SDK-badge](/help/main/assets/platform.png) [!DNL Adobe Experience Platform Web SDK] versie 2.5.0 (1 juni 2021)

Deze release van de [!DNL Platform Web SDK] omvat ondersteuning voor:

| Functie | Details |
| --- | --- |
| Ondersteuning omleiden met [!UICONTROL Analytics for Target] (A4T) | De SDK van het Web Platform ondersteunt nu [!DNL Target] omleidingen bij gebruik [A4T](/help/main/c-integrating-target-with-mac/a4t/a4t.md).<br>Zie voor meer informatie [Analyses voor [!DNL Target] uitvoering](/help/main/c-integrating-target-with-mac/a4t/a4timplementation.md). |

### at.js versie 2.5.0 (13 mei 2021)

Deze versie van at.js bevat de volgende verbeteringen en wijzigingen:

* [Apparaatbeslissingen](https://developer.adobe.com/target/implement/client-side/atjs/on-device-decisioning/on-device-decisioning/){target=_blank} ondersteuning voor at.js.
* [Koppelingen voorvertonen](/help/main/c-activities/c-activity-qa/activity-qa.md) ondersteuning van Automated Personalization-activiteiten

Deze release verwijdert ook ondersteuning voor Microsoft Internet Explorer 10, Internet Explorer 11 en alle oudere versies. Microsoft Edge wordt nog steeds ondersteund in om.js 2.5.0 en hoger.

### Target Standard/Premium 21.4.1 (19 april 2021)

Deze versie bevat de volgende nieuwe functies en verbeteringen. De uitgiftenummers tussen haakjes zijn voor intern [!DNL Adobe] gebruik.

| Functie | Details |
| --- | --- |
| Ondersteuning voor apparaatbeslissingen voor at.js<br>(Aankondigde datum) | Met apparaatbeslissingen kunnen marketers en ontwikkelaars experimenten en personalisatie uitvoeren in de browser van een gebruiker bij bijna-nullatentie.<br>Zie voor meer informatie [Apparaatbeslissingen voor at.js.](https://developer.adobe.com/target/implement/client-side/atjs/on-device-decisioning/on-device-decisioning/){target=_blank} |
| ![Premium](/help/main/assets/premium.png) Op List gebaseerde operatoren voor filterregels voor entiteiten | [!DNL Target Recommendations] steunt nieuwe op lijst-gebaseerde exploitanten voor entiteit het filtreren regels. (TGT-39234)<br>Nieuw toegevoegde operatoren zijn onder andere:<br><ul><li>Is opgenomen in lijst</li><li>Is niet opgenomen in lijst</li><li>Lijst bevat een item in</li><li>Lijst bevat geen item in</li><li>Lijst bevat alle items in</li><li>Lijst bevat niet alle items in</li></ul>Zie &quot;Beschikbare operatoren&quot; in [Regels voor dynamische en statische integratie gebruiken](/help/main/c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md#operators). |

Deze versie bevat de volgende oplossingen.

* Probleem verholpen waardoor een activiteit niet kon worden gesynchroniseerd nadat het publiek was gewijzigd in [!UICONTROL All Visitors]. (TGT-40259)
* Probleem verholpen waardoor dubbele aanbiedingen niet mogelijk waren wanneer ze op verschillende locaties werden gebruikt in [!UICONTROL Automated Personalization] ondanks de [!UICONTROL Disallow Duplicates] is ingeschakeld. (TGT-39567)
* Het probleem dat ervoor zorgde dat de [!UICONTROL Administration] > [!UICONTROL Scene7 configuration] pagina wordt geladen. (TGT-39918)
* Probleem verholpen waarbij eigenschappen werden toegewezen aan de onjuiste werkruimte. (TGT-39869)
* Probleem verholpen waarbij een oneindig laden werd veroorzaakt als de aanvraag mislukt nadat de omgeving was gewijzigd en een uitsluiting voor aanbevelingen werd gemaakt. (TGT-39948)

### te.js 2.4.1 (23 maart 2021)

Deze versie van at.js is een onderhoudsrelease en bevat de volgende verbeteringen en oplossingen:

* Probleem verholpen met `targetPageParams` worden opgenomen in mbox-aanvragen. `targetPageParams` dient te worden opgenomen in `pageLoad` alleen aanvragen. (TNT-40247)
* Probleem verholpen met globale document- en vensterobjecten in het dialoogvenster [!DNL Adobe Experience Platform Launch] extensie door de algemene objectafhankelijkheden van de Platform launch te vervangen door directe verwijzingen ernaar. (TNT-37124)

### IP adresveranderingen voor de server van Recommendations feed-processing (16 maart 2021)

De [!DNL Target Recommendations] IP-adressen van servers voor verwerking van bestandsgegevens zijn bijgewerkt op 16 maart 2021. Zie voor meer informatie [IP-adressen die worden gebruikt door Recommendations-voederverwerkingsservers](/help/main/c-recommendations/c-recommendations-faq/ip-addresses-marketing-cloud.md).

### Target Standard/Premium 21.2.1 (9 maart 2021)

Deze onderhoudsversie bevat de volgende verbeteringen, correcties en wijzigingen.

De uitgiftenummers tussen haakjes zijn voor intern [!DNL Adobe] gebruik.

* De toegestane aanbiedingsgrootte is vergroot (TGT-38304):

   | Type | Vorige limiet | Nieuwe limiet |
   | --- | --- | --- |
   | HTML | 256 kB | 1024 kB |
   | Visuele aanbiedingen van het Doel UI | 64 kB | 1024 kB voor elke ervaring |
   | Via API | 512 kB | 1024 kB |

* [!UICONTROL Personalization Insights] rapporten voor [!UICONTROL Auto-Target] (AT) en [!UICONTROL Automated Personalization] (AP) activiteiten worden nu dagelijks geproduceerd. U kunt een rapport kiezen dat [!UICONTROL Automated Segments] of [!UICONTROL Important Attributes] gedurende de laatste 15, 30 en 60 dagen. De opties van 45 dagen en 90 dagen zijn verwijderd om de andere montages van het terugkijkvenster toe te laten om dagelijks te lopen. (TGT-39472)
* Probleem opgelost waarbij de huidige afhankelijkheid niet werd weergegeven wanneer klanten op [!UICONTROL Edit Dependency] op een activiteit [!UICONTROL Goals & Settings] pagina. (TGT-39340)
* Probleem verholpen bij het vernieuwen van werkruimten [!UICONTROL Audience Library]. Vóór verfrist zich, toont het publiek voor de momenteel geselecteerde werkruimte. Na vernieuwen [!UICONTROL Default Workspace] en het publiek. De huidige werkruimte en het publiek blijven nu behouden na het vernieuwen. (TGT-38871)
* Probleem verholpen tijdens het kopiëren van een [!UICONTROL Recommendations] activiteit en later het uitgeven van de originele activiteit door zijn criteria opeenvolging te veranderen. De wijziging in de volgorde van criteria in de oorspronkelijke activiteit werd ook onjuist toegepast op de gekopieerde activiteit. (TGT-39155)
* Probleem verholpen waarbij het onjuiste aantal producten werd weergegeven voor [!UICONTROL Recommendations] uitsluitingen. (TGT-39599)

### Target Standard/Premium 21.1.1 (19 januari 2021)

Deze onderhoudsversie bevat de volgende verbeteringen, correcties en wijzigingen.

De uitgiftenummers tussen haakjes zijn voor intern [!DNL Adobe] gebruik.

* Er is een waarschuwing toegevoegd bij het selecteren van een [!DNL Adobe Analytics] metrisch bij gebruik [!UICONTROL Analytics as the reporting source] (A4T) in een [!UICONTROL Auto-Target] activiteit. [!UICONTROL Auto-Target] modellen zijn geoptimaliseerd om met binaire (op omzetting-gebaseerde) metriek te werken. Het selecteren van een ononderbroken metrische waarde, zoals opbrengst, zou suboptimale resultaten kunnen hebben en [!UICONTROL Personalization Insights] rapporten zijn mogelijk niet correct. (TGT-38926)
* Er is een statuspictogram toegevoegd in het dialoogvenster [!UICONTROL Auto-Target Summary] verslag voor [!UICONTROL Auto-Target] activiteiten die gebruikmaken van A4T. Het groene controlepictogram naast elke ervaring in het rapport geeft aan dat er een gepersonaliseerd model voor machinaal leren is gegenereerd voor die ervaring. Het klokpictogram wijst erop dat niet genoeg verkeer is gediend om het model te bouwen. (TGT-38925)
* De [!UICONTROL Automated Segments] en [!UICONTROL Important Attributes] rapporten voor [!UICONTROL Auto-Target] activiteiten die gebruikmaken van A4T en [!DNL Analytics] conversiemetriek wordt gegenereerd en ziet er hetzelfde uit als wanneer u [!DNL Target] als bron van de rapportage. (TGT-38931)
* Een filteroptie voor de omgeving toegevoegd aan de [!UICONTROL Recommendations] [!UICONTROL Collections] lijst. (TGT-38353)
* Probleem opgelost waarbij het onjuiste aantal producten werd weergegeven in [!UICONTROL Recommendations] verzamelingen. (TGT-39162)
* Toegevoegde [!UICONTROL Last Updated] naar de [!UICONTROL Recommendations] [!UICONTROL Catalog Search]. (TGT-38340)
* Probleem opgelost in [!UICONTROL Recommendations] die de [!UICONTROL Create Sequence] pagina om te hangen na het veranderen van de industrie verticaal. (TGT-38160)
* Probleem verholpen waardoor gebruikers een publiek niet konden verwijderen uit een aanbieding in een [!UICONTROL Automated Personalization] (AP) activiteit. (TGT-39058)
* Probleem opgelost waarbij het onjuiste tijdframe (begin- en einddatum) werd weergegeven in [!UICONTROL Audience Info] voor sommige klanten. (TGT-39150)
* Probleem verholpen waardoor sommige klanten de lijst met activiteiten in de [!UICONTROL Default Workspace]. (TGT-38526)

### om 2.4.0 uur (14 januari 2021)

Deze release van at.js is een onderhoudsrelease en bevat de volgende oplossingen:

* Voegt ondersteuning voor Unified Profile/platform-id toe aan de levering-API van de klant.
* Oplossing voor een ongeldige inspuiting van stijllabels.

## Opmerkingen bij de release - 2020

### Target Standard/Premium 20.10.1 (27 oktober 2020)

Deze release bevat de volgende nieuwe functies:

| Functie | Details |
| --- | --- |
| Apparaatbeslissingen | Bij beslissingen op het apparaat kunnen zowel marketers als productontwikkelaars experimenteren en op machinaal leren gebaseerde personalisatie vanuit het apparaat van de gebruiker, via kanalen, met een bijna-nullatentie.<br>De snelheid en de prestaties zaken-in klanteninzichten en gebruikerstevredenheid.<br>Door op het apparaat te beslissen kunt u belangrijke personalisatie- en experimenteringsinstructies in A/B Test and Experience Targeting (XT) activiteitstypen compileren in &quot;optimalisatieartefacten:&quot;JSON voorwerpen die op klantenapparaten via CDN worden geladen. En omdat beslissingen op het apparaat native verbinding maken met [!DNL Adobe Experience Cloud] producten, [!DNL Target] gebruikers krijgen een snelle analyse en snellere ervaringen.<br>Zie * voor meer informatie[Apparaatbeslissingen voor at.js](https://developer.adobe.com/target/implement/client-side/atjs/on-device-decisioning/on-device-decisioning/){target=_blank} and [Introduction to on-device decisioning](https://developer.adobe.com/target/implement/server-side/sdk-guides/on-device-decisioning/){target=_blank} voor server-kant. |

Deze release bevat de volgende verbeteringen, correcties en wijzigingen:

* Probleem verholpen dat was voorkomen [!UICONTROL Average Lift Confidence Interval] en [!UICONTROL Confidence] van weergave in [!DNL Auto-Target] de [!UICONTROL Total] rij. De metingen worden correct weergegeven voor alle afzonderlijke ervaringen. (TGT-37301)
* Probleem verholpen dat gevolgen had [!DNL Adobe Target Premium] gebruikers [!UICONTROL Auto-Target] rapportage vanaf 15 september, 2:30 uur (PDT) tot 6 oktober, 9:25 (PDT). Wanneer het bekijken van rapporten voor de beïnvloede omzettingsmetriek (gevormd die of &quot;[!UICONTROL Viewed a page]&quot; of &quot;[!UICONTROL Clicked on mbox]&quot; optie), worden de omrekeningskoersen onjuist gerapporteerd. Er is momenteel geen bekend leveringsprobleem.
* Een selecteerbaar item toegevoegd [!UICONTROL Last Updated At] in de [!UICONTROL Catalog Search] tabel en [!UICONTROL Last Updated At] filter. Deze verbetering bespaart tijd en inspanning omdat u niet elk individueel punt moet openen om te zien wanneer het laatst werd bijgewerkt en u kunt filtreren door datum de punten werden laatst bijgewerkt.

   ![Laatst bijgewerkt bij kolom- en filterillustratie](/help/main/r-release-notes/assets/column-and-filter.png)

* Er zijn updates uitgevoerd om de doelgebruikersinterface compatibel te maken met [Richtlijnen voor toegankelijkheid van webinhoud](https://www.w3.org/WAI/standards-guidelines/wcag/) 2.0 Niveau A en A Success Criteria (WCAG 2.0 AA). (TGT-34384 &amp; TGT-24679)
* Verbeterde CSP-functies (Content Security Policy). (TGT-37035)
* Introduceerde een manier om de cliëntcode als parameter voor klanten te specificeren die CNAME gebruiken. (TNT-38571)
* [!DNL Adobe Experience Cloud] documentatie wordt [!DNL Experience League]. In oktober worden alle opmerkingen bij de release, artikelen, video&#39;s en zelfstudies verplaatst van hun huidige locatie op `docs.adobe.com` tot [!DNL Experience League]. Deze beweging zorgt ervoor dat al het leren, zelfhulp, enablement, en communautaire inhoud van één enkele plaats wordt gediend. Wanneer deze wijziging optreedt, hoeft u niets te doen, aangezien alle koppelingen naar [!DNL Experience League]. De opmerkingen bij de release worden bijgewerkt wanneer de cutover begint.

### Target Standard/Premium 20.9.1 (30 september 2020)

Deze onderhoudrelease bevat de volgende verbeteringen, correcties en wijzigingen:

* Verbeterde navigatie en functionaliteit voor gebruikers met alleen toetsenbord. (TGT-34487, TGT-34516, TGT-34517, TGT-34514)
* Toegevoegde labels in de gebruikersinterface voor gebruikers die ondersteunende hulpmiddelen gebruiken. (TGT-34500, TGT-34501, TGT-34502, TGT-24504)
* Verbeterd tekst- en kleurcontrast voor afbeeldingen en tekst in de gebruikersinterface. (TGT-34513)

### Target Standard/Premium 20.8.3 (15 september 2020)

| Functie | Details |
| --- | --- |
| ![Premium badge](/help/main/assets/premium.png) Analyses voor doelondersteuning (A4T) voor activiteiten van Auto-Target | [!UICONTROL Auto-Target] activiteiten worden nu ondersteund [Analyses voor doel](/help/main/c-integrating-target-with-mac/a4t/a4t.md).<br>Dankzij deze integratie kunt u de [!UICONTROL Auto-Target] Schakel het leeralgoritme voor machines in om een beste ervaring voor elke bezoeker te kiezen op basis van hun profiel, gedrag en context.<br>Als je al [geïmplementeerde A4T](/help/main/c-integrating-target-with-mac/a4t/a4timplementation.md) voor gebruik met A/B Test en Ervaring gerichte activiteiten, bent u allen klaar!<br>Zie voor meer informatie [A4T-ondersteuning voor activiteiten voor automatisch toewijzen en automatisch richten](/help/main/c-integrating-target-with-mac/a4t/a4t-at-aa.md). |

### Target Standard/Premium 20.8.2 (10 september 2020)

| Functie | Details |
| --- | --- |
| ![Premium badge](/help/main/assets/premium.png) De aanbevelingen van de controle groeven binnen de opeenvolgingen van criteria | Met Criteria Sequences kunt u nu het aantal sleuven bepalen dat wordt opgenomen door de criteria van elke aanbeveling, zodat u verschillende typen items of een andere algoritme kunt combineren en afstemmen.<br>Zie [Criteria-reeksen maken](/help/main/c-recommendations/c-algorithms/create-criteria-sequence.md#sequence) voor meer informatie. |

### Target Standard/Premium 20.8.1 (2 september 2020)

Deze release bevat de volgende verbeteringen, correcties en wijzigingen:

* Probleem verholpen waarbij fouten werden weergegeven bij het laden van de nieuwe [!UICONTROL Administration] pagina&#39;s na het schakelen tussen organisaties. (TGT-37730)
* Probleem verholpen waarbij de onjuiste clientcode werd weergegeven op het tabblad [!UICONTROL Administration > Implementation] pagina. (TGT-37849)
* Probleem verholpen waardoor gebruikers soms de bewerkingsfuncties in het dialoogvenster [!UICONTROL Visual Experience Composer] (VEC) nadat de VEC met succes is geladen. (TGT-37162)
* Probleem verholpen waardoor pagina&#39;s niet konden worden geladen in de VEC en de Enhanced Experience Composer (EEC), ook al was de extensie VEC Helper geïnstalleerd. Dit was het gevolg van veranderingen in Google Chrome 80+. Download de [bijgewerkte extensie VEC Helper](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/issues-related-to-the-visual-experience-composer-vec-and-enhanced-experience-composer-eec.md). (TGT-37893)
* Probleem verholpen waarbij gebruikers soms werden belet om op .js te downloaden van het tabblad [!UICONTROL Administration > Implementation] pagina na het schakelen tussen organisaties. (TGT-37668)
* De downloadknop at.js is nu uitgeschakeld tijdens het laden om te voorkomen dat [!DNL Target] van het verzenden van veelvoudige verzoeken als de gebruikers de downloadknoop veelvoudige tijden klikken. (TGT-37633)
* Probleem opgelost in [!UICONTROL Experience Targeting] (XT) activiteiten die ervaringen hebben veroorzaakt om &quot;het halen resultaten&quot;voor een lange periode te tonen. (TGT-37684)
* Verbeterde navigatie en functionaliteit voor gebruikers met alleen toetsenbord. (TGT-34479 &amp; TGT-34473)
* Toegevoegde labels in de gebruikersinterface voor gebruikers die ondersteunende hulpmiddelen gebruiken. (TGT-34480)
* Het foutbericht is verbeterd bij het verwijderen van een mobiele viewport die momenteel wordt gebruikt in een activiteit. Het foutbericht luidt nu: &quot;Deze viewport is momenteel gekoppeld aan een of meerdere activiteiten. U moet viewport uit die activiteiten verwijderen alvorens het te kunnen schrappen.&quot; (TGT-37030)
* Toegevoegde steun in VEC om klik het volgen op een css selecteur toe te staan die meer dan één element in de pagina aanpast. (TGT-37323)
* Probleem verholpen waardoor bepaalde gebruikers de [!UICONTROL Activity] lijst. Het volgende foutbericht is weergegeven: &quot;Kan geen URL-suggesties ophalen.&quot; De fout kwam voor gebruikers voor gebruikend wagenterugloop in hun FirstName (FirstName/r/n) in het systeem van de Achterkant van de Adobe. (TGT-37330)
* Probleem verholpen waardoor gebruikers de [!UICONTROL Activity] pagina als de naam van de werkruimte (opgegeven in het dialoogvenster [!UICONTROL Adobe Admin Console for Enterprise]) bevat een apostrof. (TGT-37709)
* Probleem opgelost in [!UICONTROL Auto-Allocate] activiteiten tijdens het selecteren van optimalisatie en omzettingsmetriek waar een foutenmelding verkeerd gebruikers informeerde om een rapportreeks te selecteren, alhoewel een rapportreeks reeds werd gespecificeerd. (TGT-37689)
* Probleem verholpen dat soms metriek veroorzaakte op de [!UICONTROL Goals and Settings] pagina die leeg moet worden gemaakt nadat u naar de [!UICONTROL Targeting] pagina en vervolgens terug. (TGT-37691)
* Probleem verholpen waarbij een onjuiste laatst gewijzigde waarde voor [!DNL Recommendations] criteria. (TGT-37666)
* Probleem verholpen waarbij id&#39;s van een box in de vervolgkeuzelijst Mboxes werden weergegeven in plaats van namen van een box. (TGT-37739)

### te.js 2.3.2 (24 juli 2020)

Deze release van at.js is een onderhoudsrelease en bevat de volgende oplossing:

* Het probleem is opgelost wanneer een script of code een standaardeigenschap aan het venster of document toevoegt.

### Target Standard/Premium 20.7.1 (27 juli 2020)

Deze release bevat de volgende wijzigingen:

#### [!UICONTROL Administration] sectie-UI vernieuwen

We herschrijven geleidelijk de hele [!DNL Target] UI die een nieuwe technologiestapel gebruikt om betere prestaties te kunnen aanbieden, de vereiste onderhoudstijd te verminderen wanneer het vrijgeven van nieuwe eigenschappen, en de gebruikerservaring over het product te verbeteren. De eerste sectie die is vernieuwd, is de [!UICONTROL Setup] , waarvan de naam is gewijzigd [!UICONTROL Administration].

Als onderdeel van deze vernieuwing kunt u gemakkelijk een groot aantal handelingen uitvoeren met de pagina&#39;s in het dialoogvenster [!UICONTROL Administration] , zoals:

* Download het nieuwste bestand at.js van de [!UICONTROL Implementation] tab (**[!UICONTROL Administration]** > **[!UICONTROL Implementation]**).
* Pas de instellingen op at.js aan en bekijk uw wijzigingen eenvoudig (**[!UICONTROL Administration]** > **[!UICONTROL Implementation]**).
* Wijzig verbeterde rapporteringsmontages, zoals de standaardmunt en tijdzone, IPs om van rapportering uit te sluiten, etc. (**[!UICONTROL Administration]** > **[!UICONTROL Reporting]**)
* IP-adressen van bezoekers verduisteren om privacyredenen (**[!UICONTROL Administration]** > **[!UICONTROL Implementation]**)
* Bekijk de bestaande lijst met gebruikers per werkruimte en hun rollen, voordat u ze beheert in Adobe Admin Console (**[!UICONTROL Administration]** > **[!UICONTROL Users]**).
* Alle tabellen in de [!UICONTROL Administration] sectie.

Zie voor meer informatie [Doeloverzicht beheren](/help/main/administrating-target/administrating-target.md).

#### Verbeteringen, correcties en wijzigingen

Deze release bevat de volgende verbeteringen, correcties en wijzigingen:

* Probleem verholpen waarbij sitevoorkeuren niet konden worden behouden na vernieuwen. (TGT-37239)
* Probleem verholpen dat was voorkomen [!UICONTROL Insert After] > [!UICONTROL Image] werken met Scalable Vector Graphics (SVG)-afbeeldingen. (TGT-37242)
* Probleem verholpen met de [!UICONTROL Publisher] rol die de schrapping van ontwerp - activiteiten heeft voorkomen . (TGT-37358)
* Probleem verholpen waardoor gebruikers een activiteit niet konden bewerken [!UICONTROL All My Workspaces] is geselecteerd. (TGT-37276)

### Target Standard/Premium 20.5.1 (17 juni 2020)

| Functie/verbetering | Beschrijving |
| --- | --- |
| Ondersteuning voor Analytics voor Target (A4T) voor [!UICONTROL Auto-Allocate] activiteiten | [!UICONTROL Auto-Allocate] activiteiten worden nu ondersteund [Analyses voor doel](/help/main/c-integrating-target-with-mac/a4t/a4t.md).<br>Dankzij deze integratie kunt u de [!UICONTROL Auto-Allocate] meervoudig bewapende bandit vermogen om verkeer naar het winnen van ervaringen te drijven, terwijl het gebruiken van een [!UICONTROL Adobe Analytics] doel metrisch en/of [!UICONTROL Adobe Analytics] rapportage- en analysemogelijkheden.<br>Als je al [geïmplementeerde A4T](/help/main/c-integrating-target-with-mac/a4t/a4timplementation.md) voor gebruik met A/B Test en Ervaring gerichte activiteiten, bent u allen klaar!<br>Zie voor meer informatie [A4T-ondersteuning voor activiteiten voor automatisch toewijzen en automatisch richten](/help/main/c-integrating-target-with-mac/a4t/a4t-at-aa.md). |
| De tokens van de reactie voor de Methode van de Toewijzing van het Verkeer voor auto-Doel en de activiteiten van Automated Personalization | Twee [reactietokens](/help/main/administrating-target/response-tokens.md) zijn toegevoegd aan [!UICONTROL Auto-Target] en [!UICONTROL Automated Personalization] activiteiten om te kunnen bepalen of een bezoeker een bepaalde ervaring heeft opgedaan als gevolg van zijn toewijzing aan &quot;controle&quot; of &quot;gericht&quot; verkeer.<ul><li>`experience.trafficAllocationId` 0 als een bezoeker ervaring heeft opgedaan met &quot;controle&quot;-verkeer en 1 als een bezoeker een ervaring heeft opgedaan met &quot;gerichte&quot; verkeersdistributie.</li><li>`experience.trafficAllocationType` retourneert &quot;control&quot; of &quot;target&quot;.</li></ul>Voor meer informatie over controle versus gericht verkeer, zie [Selecteer het besturingselement voor uw Automated Personalization- of AutoTarget-activiteit](/help/main/c-activities/t-automated-personalization/experience-as-control.md). |
| [!UICONTROL Publisher] rol | Deze nieuwe rol is vergelijkbaar met de huidige [!UICONTROL Observer] rol (kan activiteiten bekijken, maar kan niet hen creëren of uitgeven). De [!UICONTROL Publisher] de rol heeft de extra toestemming om activiteiten te activeren.<br>Zie voor meer informatie: <ul><li>**Standaarddoelgebruikers**: [Rollen en machtigingen opgeven](/help/main/administrating-target/c-user-management/c-user-management/user-management.md#roles-permissions) in *Gebruikers*.</li><li>**Doelpremiumgebruikers**: [Stap 6: Rollen en machtigingen opgeven](/help/main/administrating-target/c-user-management/property-channel/properties-overview.md#section_8C425E43E5DD4111BBFC734A2B7ABC80) in *Bedrijfsmachtigingen configureren*.</li></ul> |
| A4T-ondersteuning in [!DNL Analysis Workspace]<br>25 juni 2020 | [!UICONTROL Anaytics for Target] (A4T) wordt nu ondersteund in [!DNL Analysis Workspace]. De [!UICONTROL Analytics for Target (A4T) panel] Hiermee kunt u uw [!DNL Adobe Target] activiteiten en ervaringen in [!DNL Analysis Workspace].<br>Zie voor meer informatie [Rapporten in Analytics](/help/main/c-integrating-target-with-mac/a4t/reporting.md) in *A4T-rapportage* en [Analyses voor venster Doel (A4T)](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/panels/a4t-panel.html) in de *Handleiding Analysehulpmiddelen*. |

**Verbeteringen, correcties en wijzigingen**

* Probleem verholpen waarbij de metrische waarde &quot;bezoekers&quot; werd opgeslagen in de definitie van de activiteit in plaats van &quot;UniqueVisitors&quot;. (TGT-37098)
* Probleem opgelost in het dialoogvenster [!DNL Target] UI die ervoor zorgde dat de verticale scrollbar niet correct op het [!UICONTROL Audiences] pagina. (TGT-36968)

### releases (15 juni 2020) om 1.js 1.8.2 en om 2.3.1.

De volgende verbeteringen en correcties zijn aangebracht in de [!DNL Target] bibliotheken at.js:

| Functie/verbetering | Beschrijving |
| --- | --- |
| om.js 1.8.2 | Deze release van at.js is een onderhoudsrelease en bevat de volgende oplossing:<ul><li>Probleem verholpen bij gebruik van CNAME en randoverschrijving, op .js 1.*x* kan het serverdomein onjuist maken, wat tot [!DNL Target] verzoek mislukt. (TNT-35064)</li></ul>Zie voor meer informatie [details van de at.js-versie](https://developer.adobe.com/target/implement/client-side/atjs/target-atjs-versions/){target=_blank}. |
| om.js 2.3.1 | Deze versie van at.js is een onderhoudsrelease en bevat de volgende verbeteringen en oplossingen:<ul><li>De `deviceIdLifetime` overschrijfbaar instellen via [targetGlobalSettings](https://developer.adobe.com/target/implement/client-side/atjs/atjs-functions/targetglobalsettings/){target=_blank}. (TNT-36349)</li><li>Probleem verholpen bij gebruik van CNAME en randoverschrijving, op .js 2.*x* kan het serverdomein onjuist maken, wat tot [!DNL Target] verzoek mislukt. (TNT-35065)</li><li>Probleem verholpen tijdens het gebruik van de [!DNL Target] [!DNL Launch] extensie v2 en de [!DNL Adobe Analytics] [!DNL Launch] uitbreiding, [!DNL Target] de [!DNL Analytics] `sendBeacon` vraag. (TNT-36407, TNT-35990, TNT-36000)</li></ul>Zie voor meer informatie [details van de at.js-versie](https://developer.adobe.com/target/implement/client-side/atjs/target-atjs-versions/){target=_blank}. |

### Wijzigingen in de profielbatchstatus-API v2 (14 mei 2020)

Met de versie van 20 mei, zal de status van de Batch van het Profiel slechts rij-vlakke mislukkingsgegevens terugkeren die door:gaan (de succesgegevens zullen niet worden teruggekeerd). Mislukte profiel-id&#39;s worden door de API geretourneerd.

De vorige en nieuwe API-reacties zijn als volgt:

`ProfileBatchStatus Api`
`http://<<edge>>/m2/<<client>>/profile/batchStatus?batchId=<batchid>`

**Momenteel zien we het antwoord als:**

```
<response>
 
    <batchId>samplebatch-1585929692655-59449976</batchId>
 
    <status>complete</status>
 
    <batchSize>164</batchSize>
 
    <profile>
 
        <id>1514187733806-729395</id>
 
        <status>success</status>
 
    </profile>
 
    <profile>
 
        <id>1573612762055-214017</id>
 
        <status>success</status>
 
    </profile>
 
    <profile>
 
        <id>some profile id</id>
 
        <status>failed</status>
 
    </profile>
 
</response>
```

**Na 4 mei zal het antwoord zijn:**

```
<response>
 
    <batchId>samplebatch-1585929692655-59449976</batchId>
 
    <status>complete</status>
 
    <batchSize>164</batchSize>
 
    <profile>
 
        <id>some profile id</id>
 
        <status>failed</status>
 
    </profile>
 
</response>
```

### Target Standard/Premium 20.4.1 (6 mei 2020)

Deze release bevat de volgende verbeteringen, correcties en wijzigingen:

* Probleem verholpen waarbij een apparaat en browsertype voor een publiek onjuist worden gekwalificeerd. (TGT-36266)
* Probleem verholpen waarbij rapportgegevens niet konden worden weergegeven wanneer ze werden weergegeven op schermen met een breedte van minder dan 963 pixels. (TGT-36549)
* Probleem verholpen waardoor rapporten voor automatische personalisatie niet correct worden weergegeven. (TGT-36619)
* Probleem verholpen waarbij incompatibele metriek kon worden geselecteerd in Auto-Allocate en Auto-Target activiteiten die Analytics voor Doel (A4t) gebruiken. (TGT-36646)
* Probleem verholpen waarbij bepaalde opties in de Visual Experience Composer (VEC) niet correct werden weergegeven. (TGT-36571)
* Probleem verholpen in de doelgebruikersinterface die ertoe heeft geleid dat andere Recommendations-aanbiedingsvoorvertoningen de bewerkte inhoud hebben weergegeven nadat een gebruiker de inhoud in één ervaring heeft vervangen. (TGT-36053 &amp; TGT-36894)
* Probleem verholpen waardoor sommige gebruikers items uit een Recommendations-catalogus konden verwijderen. (TGT-36455)
* Probleem verholpen waardoor gebruikers Recommendations-criteria niet konden opslaan voor activiteiten die uit meerdere pagina&#39;s bestaan. (TGT-36249)
* Probleem verholpen waarbij de keuzerondjes voor de gegevensbron met gedragingen voor een tweede opeenvolgende keer werden verborgen bij het bewerken van de criteria. (TGT-36796)
* Probleem verholpen waarbij een Recommendations-algoritme gedurende een langere periode &quot;ophaalresultaten&quot; liet weergeven. (TGT-36550 &amp; TGT-36551)
* Veel UI-tekenreeksen die in verschillende talen zijn gelokaliseerd, zijn bijgewerkt.

### Doel om.js (25 maart 2020)

De volgende nieuwe versies van de JavaScript-bibliotheken van Target at.js zijn beschikbaar:

* at.js versie 2.3.0
* at.js versie 1.8.1

Zie voor meer informatie [details van de at.js-versie](https://developer.adobe.com/target/implement/client-side/atjs/target-atjs-versions/){target=_blank}.

### Target Standard/Premium 20.2.1 (23 maart 2020)

Deze release bevat de volgende verbeteringen, correcties en wijzigingen:

* Probleem verholpen waarbij klanten een verzameling niet konden selecteren tijdens het uitvoeren van een cataloguszoekopdracht. (TGT-36230)
* Probleem verholpen waarbij een criterium dat via API is gemaakt, maar waarnaar niet wordt verwezen door een activiteit die in de doelinterface is gemaakt, ten onrechte uit de gebruikersinterface kan worden verwijderd. (TGT-35917)
* Geïmplementeerde veiligheidsverbeteringen aan het Beleid van de Veiligheid van de Inhoud (CSP). (TGT-36190)
* Probleem verholpen waarbij &quot;NaN%&quot; werd weergegeven wanneer de percentagebalk voor kenmerkweging naar links werd verschoven. (TGT-36211)
* Opgeloste lokalisatieproblemen zodat de UI-tekst in verschillende talen correct wordt weergegeven.
* We hebben de lijst met beschikbare meetgegevens van Adobe Analytics for Target (A4T)-activiteiten gestandaardiseerd door Adobe Analytics-meetgegevens af te schaffen die niet worden ondersteund in de huidige versie van Adobe Analytics API&#39;s. Hierdoor kunnen we onze A4T-ondersteuning uitbreiden in toekomstige versies van Adobe Target.

   De volgende wijzigingen zijn aangebracht:

   * &quot;Gemiddelde tijd die op pagina wordt besteed&quot; is vervangen door &quot;Gemiddelde tijd die ter plekke wordt besteed.&quot; Om het even welke activiteiten die dit als metrisch metrisch het Primaire Metrische Doel gebruiken zullen &quot;Gemiddelde Tijd die op Plaats wordt uitgegeven&quot;hebben (nota: (gemeten in minuten in plaats van seconden) geselecteerd als Primair doel Metrisch wanneer de activiteit de volgende keer wordt bewerkt.
   * &quot;Bezoekers&quot; is vervangen door &quot;Unieke Bezoekers&quot;. Voor alle activiteiten waarbij deze metrische waarde wordt gebruikt als &#39;Primaire Goal Metric&#39;, worden &#39;Unieke bezoekers&#39; geselecteerd als &#39;Primaire Goal Metric&#39; wanneer de activiteit de volgende keer wordt bewerkt.

* De volgende metriek zijn afgekeurd en kunnen niet meer worden geselecteerd als Primair doel Metrisch wanneer het creëren van een nieuwe activiteit A4T.

   | Vervangen metrisch(e) | Voorgestelde vervangende metrische(n) |
   |--- |--- |
   | Dagelijkse Bezoekers, Uur Bezoekers, Maandelijkse Bezoekers, Driemaandelijkse Bezoekers, Wekelijkse Bezoekers, Jaarlijkse Bezoekers | Unieke bezoekers |
   | Gemiddelde visdiepte | n.v.t. Niet voorgesteld als primair doel metrisch |
   | Bots | n.v.t. Niet voorgesteld als primair doel metrisch |
   | Mobiele crashsnelheid, Mobile Avg vorige sessieduur, Mobile App Store Avg Rank, Mobile App Performance Crash Rate, Mobile App Store Avg Rating | n.v.t. Niet voorgesteld als primair doel metrisch |

### Navigatie door Adobe Experience Cloud (22 februari 2019)

* Wanneer u zich aanmeldt bij de [!DNL Adobe Experience Cloud], wordt u doorgestuurd naar de nieuwe headernavigatie. Het lijkt sterk op de vorige navigatie met de zwarte balk bovenaan, maar biedt de volgende verbeteringen:

   * Eenvoudiger schakelen tussen [!DNL Identity Management System] (IMS) organisaties of een andere oplossing.
   * Verbeterde gebruikershulp: De zoekresultaten bevatten resultaten van het [!DNL Target] productdocumentatie, maar ook communityforums en meer video-inhoud, waardoor u gemakkelijker toegang hebt tot meer inhoud om optimaal te profiteren [!DNL Target]. We hebben ook een feedbackmechanisme toegevoegd in het gedeelte [!UICONTROL Help] , zodat u gemakkelijker problemen kunt melden of uw ideeën kunt delen.

   * Verbeterde NPS-feedbackfunctionaliteit (Net Promoter Score), zodat de enquêtemodale modus uw werkstroom niet verstoort.

   * Meldingen voor [!DNL Target] zijn momenteel niet beschikbaar in het dialoogvenster [!UICONTROL Notifications] in de koptekst.
   >[!NOTE]
   >
   >Tijdens de introductie van de nieuwe navigatiebalk zult u ook enkele URL-wijzigingen zien. Alle vorige bladwijzerkoppelingen werken nog steeds, maar we raden u aan nieuwe bladwijzerkoppelingen te maken om deze sneller te openen.

### Target Standard/Premium 20.1.1 (4 februari 2020)

De Target Standard/Premium 20.1.1-release is een onderhoudrelease en bevat verbeteringen en verbeteringen voor de back-endserver. Daarnaast zijn de volgende correcties opgenomen:

* Probleem verholpen waarbij het veld Adobe Analytics tracking-server leeg was op de pagina Doelstellingen en instellingen voor bestaande activiteiten van Adobe for Target (A4T). (TGT-35960)
* Probleem verholpen in de gebruikersinterface waardoor de selectie in de tweede vervolgkeuzelijst niet werd weergegeven tijdens het maken van een publiek voor categorie-affiniteit. (TGT-36098)

## Opmerkingen bij de release - 2019 {#releases-2019}

### Target Java SDK versie 1.1.0 (16 december 2019)

* Ondersteuning voor proxyconfig toegevoegd vanwege een open-bronbijdrage van @hisham-hassan.

### Doel Java SDK versie 1.0.1 (11 november 2019)

Het volgende probleem is opgelost in versie 1.0.1:

* Stuur een aanvullende gegevens-id in een doelaanvraag, zelfs als er geen bezoeker-API cookie aanwezig is.

### Doelplatform (31 oktober 2019)

| Functie/verbetering | Beschrijving |
| --- | --- |
| Java SDK | De [!DNL Target] Java SDK biedt u de mogelijkheid te implementeren [!DNL Target] op de server. Met deze Java SDK kunt u eenvoudig integreren [!DNL Target] met andere [!DNL Adobe Experience Cloud] oplossingen, zoals de [!DNL Adobe Experience Cloud Identity Service], [!DNL Adobe Analytics], en [!DNL Adobe Audience Manager].<br>De Java SDK introduceert best practices en verwijdert complexiteit bij integratie met [!DNL Target] via onze bezorgings-API zodat uw engineeringteams zich kunnen richten op bedrijfslogica. Hieronder volgen opmerkelijke elementen die we in de nieuwste versie introduceren:<ul><li>Ondersteuning voor prefetching en meldingen waarmee u de prestaties kunt optimaliseren via caching.</li><li>Ondersteuning voor het optimaliseren van prestaties wanneer u een hybride integratie hebt van [!DNL Target] zowel op uw webpagina&#39;s als op de server. We introduceren een instelling met de naam `serverState` dat wordt bevolkt door ervaringen die via server-kant worden teruggewonnen zodat at.js 2.2 geen extra servervraag meer zal maken om de ervaringen terug te winnen. Deze aanpak optimaliseert de prestaties bij het laden van pagina&#39;s.</li><li>Ondersteuning voor het ophalen van VEC-activiteiten via de Java SDK, wat mogelijk wordt gemaakt door de nieuwe Delivery API.</li><li>Open sourcing zodat uw ontwikkelaars kunnen bijdragen aan de [Doel Java SDK](https://github.com/adobe/target-java-sdk).</li></ul>Meer informatie over de Target Java SDK op het Tech Blog van de Adobe - [Server-Side Optimization met de nieuwe Target Java SDK](https://medium.com/adobetech/server-side-optimization-with-the-new-target-java-sdk-421dc418a3f2). |

### Target Standard/Premium 19.10.2 (31 oktober 2019)

| Functie/verbetering | Beschrijving |
| --- | --- |
| ![Premium badge](/help/main/assets/premium.png) Kenmerken met meerdere waarden | Soms wilt u werken met een veld met meerdere waarden. Neem de volgende voorbeelden:<ul><li>U biedt films aan gebruikers aan. Een bepaalde film heeft meerdere acteurs.</li><li>Je verkoopt tickets aan concerten. Een bepaalde gebruiker heeft meerdere favoriete banden.</li><li>Je verkoopt kleding. Een shirt is verkrijgbaar in verschillende formaten.</li></ul>Om aanbevelingen in deze scenario&#39;s te behandelen, kunt u multi-waardegegevens tot Doel Recommendations overgaan en speciale multi-waardeexploitanten gebruiken.<br>Zie voor meer informatie [Werken met kenmerken van meerdere waarden](/help/main/c-recommendations/c-algorithms/work-with-multi-value-attributes.md). |

### Target Standard/Premium 19.10.1 (22 oktober 2019)

| Functie/verbetering | Beschrijving |
| --- | --- |
| ![Premium badge](/help/main/assets/premium.png) Op gebruiker gebaseerde Recommendations<br>(24 oktober 2019) | Aanbevolen objecten op basis van de browsergeschiedenis, weergavegeschiedenis en aankoopgeschiedenis van elke bezoeker. Deze objecten worden doorgaans &#39;Aanbevolen voor je&#39; genoemd.<br>Met deze criteria kunt u persoonlijke inhoud en ervaringen aanbieden aan zowel nieuwe als geretourneerde bezoekers. De lijst met aanbevelingen is gericht op de meest recente activiteit van de bezoeker en wordt tijdens de sessie bijgewerkt en wordt meer gepersonaliseerd naarmate de bezoeker door uw site bladert.<br>Zie voor meer informatie &quot;Op gebruiker gebaseerde Recommendations&quot; in [Criteria/algoritmen](/help/main/c-recommendations/c-algorithms/algorithms.md#criteria-algorithms). |

**Adobe Experience Cloud-navigatie**

* Wanneer u zich aanmeldt bij de [!DNL Adobe Experience Cloud], wordt u doorgestuurd naar de nieuwe headernavigatie. Het lijkt sterk op de vorige navigatie met de zwarte balk bovenaan, maar biedt de volgende verbeteringen:

   * Eenvoudiger schakelen tussen [!DNL Identity Management System] (IMS) organisaties of een andere oplossing.
   * Verbeterde gebruikershulp: De zoekresultaten bevatten resultaten van het [!DNL Target] productdocumentatie, maar ook communityforums en meer video-inhoud, waardoor u gemakkelijker toegang hebt tot meer inhoud om optimaal te profiteren [!DNL Target]. We hebben ook een feedbackmechanisme toegevoegd in het gedeelte [!UICONTROL Help] , zodat u gemakkelijker problemen kunt melden of uw ideeën kunt delen.

   * Verbeterde NPS-feedbackfunctionaliteit (Net Promoter Score), zodat de enquêtemodale modus uw werkstroom niet verstoort.

   * Meldingen voor [!DNL Target] zijn momenteel niet beschikbaar in het dialoogvenster [!UICONTROL Notifications] in de koptekst.
   >[!NOTE]
   >
   >Deze functies worden niet meteen geïmplementeerd en worden ook niet samen aan alle klanten aangeboden. Deze functies zullen de komende weken worden geïmplementeerd, te beginnen met de [!DNL Target Standard/Premium] Release van 19.10.1 (22 oktober 2019).
   >
   >Tijdens de introductie van de nieuwe navigatiebalk zult u ook enkele URL-wijzigingen zien. Alle vorige bladwijzerkoppelingen werken nog steeds, maar we raden u aan nieuwe bladwijzerkoppelingen te maken om deze sneller te openen.

### at.js versie 2.2 en 1.8 (10 oktober 2019)

| Functie/verbetering | Beschrijving |
| --- | --- |
| at.js versie 2.2<br>en<br>at.js versie 1.8 | Deze versies van at.js verstrekken:<ul><li>Betere prestaties bij gebruik van zowel Experience Cloud ID Service (ECID) v4.4 als at.js 2.2 of at.js 1.8 op uw webpagina&#39;s.</li><li>Eerder, maakte ECID twee blokkerende vraag alvorens at.js ervaringen kon halen. Dit is verminderd tot één enkele vraag, die beduidend prestaties verbetert.</li></ul> Om van deze prestatiesverbeteringen voordeel te halen, bevorder aan at.js 2.2 of at.js 1.8 samen met de Bibliotheek van ECID v4.4.<br>at.js 2.2 biedt:<ul><li>**serverState**: Een instelling die beschikbaar is in at.js v2.2+ en die kan worden gebruikt om de paginaprestaties te optimaliseren wanneer een hybride integratie van Target wordt geïmplementeerd. Hybride integratie betekent dat u zowel at.js v2.2+ op de client-kant als de levering-API of een doel-SDK op de server-kant gebruikt om ervaringen te bieden. `serverState` geeft at.js v2.2+ de capaciteit om ervaringen direct van inhoud toe te passen die op de server wordt gehaald en aan de cliënt als deel van de pagina teruggegeven wordt.<br>Zie &quot;serverState&quot; in [targetGlobalSettings](https://developer.adobe.com/target/implement/client-side/atjs/atjs-functions/targetglobalsettings/){target=_blank}.</li></ul> |

### Doelplatform (9 oktober 2019)

| Functie/verbetering | Beschrijving |
| --- | --- |
| Node.js SDK versie 1.0 | Met de SDK van Target Node.js kunt u de doelserver implementeren.<br>Met deze Node.js SDK kunt u Target eenvoudig integreren met andere Experience Cloud-oplossingen, zoals de Adobe Experience Cloud Identity Service, Adobe Analytics en Adobe Audience Manager.<br>De SDK van Node.js introduceert best practices en verwijdert complexiteit bij de integratie met Adobe Target via onze API voor levering, zodat uw engineeringteams zich kunnen richten op bedrijfslogica. Hieronder volgen opmerkelijke elementen die we in de nieuwste versie introduceren:<ul><li>Ondersteuning voor prefetching en meldingen waarmee u de prestaties kunt optimaliseren via caching.</li><li>Ondersteuning voor het optimaliseren van prestaties wanneer u een hybride integratie van Target hebt op zowel uw webpagina&#39;s als op de server. We introduceren een instelling met de naam `serverState` die zal worden bevolkt door ervaringen die via server-kant worden teruggewonnen zodat at.js 2.2 geen extra servervraag meer zal maken om de ervaringen terug te winnen. Deze aanpak optimaliseert de prestaties bij het laden van pagina&#39;s.</li><li> Steun voor het terugwinnen van VEC-gecreeerde activiteiten via Node.js SDK, die door nieuwe Levering API mogelijk wordt gemaakt.</li><li>Open-sourced zodat uw ontwikkelaars een bijdrage kunnen leveren aan de Node.js SDK.</li></ul> |
| Leverings-API | Een geheel nieuw levering API eindpunt (/v1/levering) is beschikbaar in productie. Opmerkelijke functies zijn:<ul><li>Één eindpunt om ervaringen voor één of meerdere dozen terug te winnen.</li><li>Haal VEC-activiteiten op via de API.</li><li>Ondersteuning voor een geheel nieuw object genaamd Weergaven dat wordt gebruikt voor toepassingen voor één pagina (SPA) en mobiele toepassingen.</li></ul> |

### Target Standard/Premium 19.9.2 (30 september 2019)

Deze onderhoudrelease bevat de volgende verbeteringen:

* Verscheidene veiligheidsmoeilijke situaties, met inbegrip van een veiligheidsupdate aan de Rich Text Editor (RTE) in de Visuele Composer van de Ervaring (VEC). (TGT-35383)
* Recommendations-aanbiedingen kunnen nu, naast DIV, worden toegevoegd aan andere elementen dan DIV (bijvoorbeeld P, UL, H1), in A/B Test and Experience Targeting-activiteiten. (TGT-34333)
* Gebeurtenismeldingen (het belpictogram in de doelgebruikersinterface) zijn niet meer beschikbaar. Binnenkort wordt er een nieuwe zoekfunctie voor meldingen weergegeven.

### Target Standard/Premium 19.9.1 (10 september 2019)

| Functie/verbetering | Beschrijving |
| --- | --- |
| ![Premium badge](/help/main/assets/premium.png) Bedrijfsmachtigingen | Met de Target-release van september 2019 bieden Enterprise-machtigingen klanten de volgende toegangsopties:<UL><li>U kunt de werkruimten kiezen waarop de integratie kan worden toegepast.</li><li>U kunt een rol op de integratie van Adobe I/O toepassen: Fiatteur, Editor of waarnemer.</li></ul>Voor stapsgewijze instructies en meer informatie raadpleegt u [Toegang tot werkruimten voor Adobe I/O-integratie verlenen en rollen toewijzen](/help/main/administrating-target/c-user-management/property-channel/configure-adobe-io-integration.md). |

### Target Standard/Premium 19.7.1 (24 juli 2019) {#tgt-19-7-1}

Deze release bevat de volgende nieuwe functies en verbeteringen:

(De uitgiftenummers tussen haakjes zijn bedoeld voor intern gebruik van Adobe.)

| Functie/verbetering | Beschrijving |
| --- | --- |
| ![Premium badge](/help/main/assets/premium.png)<br>Recommendations in A/B Test and Experience Targeting (XT)-activiteiten | De Recommendations-aanbiedingsstatus (algoritme) wordt weergegeven op de overzichtspagina voor A/B Test- en XT-activiteiten die Recommendations-aanbiedingen bevatten. Voorbeelden van statussen zijn: Resultaten gereed, resultaten niet gereed en Feed-fout. (TGT-33649)<br>Zie [Recommendations als voorstel](/help/main/c-recommendations/recommendations-as-an-offer.md#status). |
| Ondersteuning voor interdomeintracering voor at.js 2.0+ via de Experience Cloud ID-bibliotheek (ECID) | Eerder werd interdomeintracering niet ondersteund in at.js 2.*x*. Met deze release kunnen klanten die at.js 2.0 of hoger gebruiken nu interdomeintracering gebruiken via de ECID-bibliotheek. De ECID-bibliotheek moet op de pagina worden geïnstalleerd in combinatie met at.js 2.0 of hoger om interdomeintracering mogelijk te maken. [Experience Cloud ID-bibliotheek 4.3.0+](https://experienceleague.adobe.com/docs/id-service/using/release-notes/release-notes.html) worden gebruikt.<br>Zie [Ondersteuning voor interdomeintracering in at.js 2.x](https://developer.adobe.com/target/implement/client-side/atjs/target-atjs-versions/){target=_blank}. |
| Doelondersteuning voor Apple ITP 2.1 en ITP 2.2 via de Experience Cloud ID-bibliotheek 4.3 | Vandaag, kunnen de klanten van het Doel Apple ITP 2.1 en ITP 2.2 door Adobe CNAME certificatieprogramma leveraging beperken.<br>Met deze release introduceert Target een naadloze integratie met de ECID-bibliotheek 4.3, die een servercookie gebruikt om ITP 2.1 en ITP 2.2 te beperken. Het wordt ten zeerste aanbevolen dat doelklanten [ECID-bibliotheek 4.3+](https://experienceleague.adobe.com/docs/id-service/using/release-notes/release-notes.html) in combinatie met de JavaScript-bibliotheek van Target om eventuele toekomstige ITP-releases te beperken. De ECID-bibliotheek blijft verbeterde functies implementeren die een robuuste oplossing bieden voor het voortdurend veranderende beleid van cookies dat door browsers wordt geïntroduceerd.<br>Zie [Apple Intelligent Tracking Prevention (ITP) 2.x](https://developer.adobe.com/target/before-implement/privacy/apple-itp-2x/){target=_blank}. |

**Verbeteringen, correcties en wijzigingen**

* Probleem verholpen waarbij werd voorkomen dat uitsluitingswaarden in Recommendations-activiteiten werden gewist bij het toevoegen van dubbele waarden. (TGT-34996)
* U kunt nu een ontwerp in een Recommendations-activiteit verwijderen van de doelpagina (stap 2 van de driedelige geleide workflow). Als u een ontwerp wilt verwijderen, moet er meer dan één ontwerp zijn geselecteerd. (TGT-35118)
* Probleem verholpen waarbij aangepaste criteria niet konden worden gebruikt voor het correct laden van bepaalde klanten in de interface van het doel of om te kunnen worden bewerkt. (TGT-35170)

### at.js versie 2.1.1 (24 juli 2019)

Deze versie van at.js is een onderhoudsrelease en bevat de volgende verbeteringen en oplossingen:

(De uitgiftenummers tussen haakjes zijn bedoeld voor intern gebruik van Adobe.)

* Oplossing een kwestie die veelvoudige bakens aan brand veroorzaakte toen het gebruiken van de Metrisch van het Volgen van de Klik op de pagina van Doelstellingen &amp; van Montages in Visual Experience Composer (VEC). (TNT-32812)
* Probleem verholpen dat ertoe heeft geleid `triggerView()` om aanbiedingen niet meer dan één keer te renderen. (TNT-32780)
* Probleem verholpen met `triggerView()` om ervoor te zorgen dat het verzoek Marketing Cloud-ID (MCID)-informatie bevat. (TNT-32776)
* Het probleem dat ervoor zorgde dat de `triggerView()` bericht wordt afgevuurd, zelfs als er geen opgeslagen weergaven zijn. (TNT-32614)
* Probleem verholpen die een fout veroorzaakte door het gebruik van de decodeURIcomponent die problemen veroorzaakte wanneer de URL een onjuist gevormde parameter van het vraagkoord bevat. (TNT-32710)
* De bakenvlag wordt nu geplaatst aan &quot;waar&quot;in de context van leveringsverzoeken die via `Navigator.sendBeacon()` API. (TNT-32683)
* Probleem opgelost waarbij Recommendations-aanbiedingen voor een paar klanten niet konden worden weergegeven op websites. Klanten konden de inhoud van de aanbieding zien in de levering API vraag maar de aanbieding werd niet toegepast op de website. (TNT-32680)
* Probleem verholpen waarbij klikken-volgen over meerdere ervaringen ertoe leidde dat het programma niet naar behoren functioneerde. (TNT-32644)
* Probleem verholpen waardoor at.js de tweede metrische waarde niet kon toepassen na het renderen van de eerste metrische waarde. (TNT-32628)
* Probleem verholpen bij passeren `mboxThirdPartyId` met de `targetPageParams` functie die ertoe leidde dat de verzoeklading om niet in of de vraagparameters of in de verzoeklading aanwezig was. (TNT-32613)
* Probleem verholpen waardoor de weergave werd geblokkeerd en op reacties op meldingen werd geklikt in browsers op basis van chroom (inclusief Google Chrome). (TNT-32290)

Voor informatie over dit en vorige versies van at.js, zie [details van de at.js-versie](https://developer.adobe.com/target/implement/client-side/atjs/target-atjs-versions/){target=_blank}.

### Target Standard/Premium 19.6.1 (26 juni 2019) {#tgt-19-6-1-historical}

Deze release bevat de volgende nieuwe functies en verbeteringen:

(De uitgiftenummers tussen haakjes zijn bedoeld voor intern gebruik van Adobe.)

| Functie/verbetering | Beschrijving |
| --- | --- |
| Visual Experience Composer (VEC) | **Nieuwe VEC-menuopties**: Wanneer u een paginaelement in VEC klikt, toont een menu de opties die voor dat elementtype beschikbaar zijn.<ul><li>U kunt nu de opdracht [!UICONTROL Styles > Background] om de achtergrondafbeelding en -kleur voor het geselecteerde element te wijzigen. (TGT-15001)</li></ul>Zie *Stijlen* in [Opties voor visuele ervaring](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md#styles).<br>**Verbeteringen voor bijhouden van klikken**: Wij hebben het proces verbeterd om klik het volgen binnen VEC en de Enige Toepassing van de Pagina (SPA) VEC te vormen.<ul><li>Als u elementen selecteert die u wilt gebruiken bij het bijhouden van klikken, worden de namen van alle beschikbare elementen aan de rechterkant weergegeven in het deelvenster Wijzigingen, zodat u snel en gemakkelijk de gewenste elementen kunt selecteren.</li><li>De [!UICONTROL Goals & Settings] op de pagina met instructies-workflows met drie delen wordt een nummer weergegeven dat het aantal elementen vertegenwoordigt dat is geselecteerd voor het bijhouden van klikken. U kunt de muisaanwijzer op dit nummer plaatsen om de namen van alle geselecteerde elementen weer te geven. (TGT-33878)</li></ul>Zie [Klikken bijhouden](/help/main/c-activities/r-success-metrics/click-tracking.md). |
| Single Page App Visual Experience Composer (SPA VEC) | **Workflow met instructies**: Een nieuwe geleide werkstroom helpt u begrijpen hoe pagina-levering-regel montages zou moeten worden gevormd om een activiteit voor uw Enige Pagina App met succes uit te voeren en in werking te stellen. (TGT-33718)<br> Zie [Single Page App (SPA) Visual Experience Composer](/help/main/c-experiences/spa-visual-experience-composer.md#page-delivery-settings).<br>**Kloonwijzigingen**: U kunt nu een wijziging definiëren met de SPA VEC en die wijziging vervolgens klonen voor gebruik in andere weergaven in de app voor één pagina. (TGT-33882)<br>Zie [Single Page App (SPA) Visual Experience Composer](/help/main/c-experiences/spa-visual-experience-composer.md). |
| ![Premium badge](/help/main/assets/premium.png) Automated Personalization (AP) en Auto-Target | **Specifieke ervaring als controle**: U kunt een ervaring selecteren die als controle moet worden gebruikt terwijl het creëren van een AP of een auto-Doel activiteit. Deze eigenschap laat u het volledige controleverkeer aan een specifieke ervaring leiden, die op het percentage van de verkeerstoewijzing wordt gebaseerd dat in de activiteit wordt gevormd. U kunt de prestatiesrapporten van het gepersonaliseerde verkeer tegen controleverkeer aan die één ervaring dan evalueren. De huidige controleoptie (willekeurig bediende ervaringen) zal beschikbaar blijven. (TGT-32801, TGT-26572, &amp; TGT-26571)<br>Zie [Selecteer het besturingselement voor uw Automated Personalization- of Auto-Target-activiteit](/help/main/c-activities/t-automated-personalization/experience-as-control.md).<br>**Persoonlijkheidsrapporten**: De markeringsvriendelijke naamgeving voor kenmerken wanneer een bezoeker een bepaald stuk inhoud op een specifieke locatie ziet, levert zinvollere informatie op. (TGT-33421 &amp; TGT-34957)<br>Zie [Gegevensverzameling voor de personalisatiealgoritmen van het Doel](/help/main/c-activities/t-automated-personalization/ap-data.md). |
| ![Premium badge](/help/main/assets/premium.png) Recommendations | U kunt de optie Aanbevolen eerder aangeschafte items gebruiken tijdens het maken van de logica Onlangs bekeken items. (TGT-34030)<br>Zie voor meer informatie [Onlangs bekeken objecten](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md#previously-purchased) in &quot;Criteria maken&quot;. |
| Beleid voor cookies van Google Chrome SameSite | Google heeft onlangs aangekondigd dat ontwikkelaars vanaf Chrome 76, die is gepland voor een release van 30 juli 2019, expliciet moeten opgeven welke cookies op verschillende websites kunnen werken en welke cookies gebruikers kunnen volgen.<br>Aangezien de industrie streeft naar het creëren van een veiliger web voor consumenten, is Target absoluut geëngageerd om persoonlijke ervaringen te leveren terwijl aan de privacyverwachtingen van bezoekers wordt voldaan en deze wordt overschreden.<br>Zie [Beleid voor cookies van Google Chrome SameSite](https://developer.adobe.com/target/before-implement/privacy/google-chrome-samesite-cookie-policies/){target=_blank}. |

### at.js versie 2.1.0 (3 juni 2019) {#atjs-210}

We zijn blij om de volgende spannende functies aan te kondigen in at.js 2.1.0:

| Functie/verbetering | Beschrijving |
| --- | --- |
| Ondersteuning voor Adobe Opt-in | Adobe Opt-In is een manier om de integratie van Adobe-oplossingen met toestemmingsbeheerplatforms te vereenvoudigen.<br>Voor meer informatie over Adobe Opt-in, zie [Privacy en algemene gegevensbeschermingsverordening (GDPR)](https://developer.adobe.com/target/before-implement/privacy/cmp-privacy-and-general-data-protection-regulation/){target=_blank}. |
| Compatibel met industriestandaard CSP | at.js gebruikt eval() niet meer om JavaScript uit te voeren. |
| Logboekregistratie voor analyses op de client | Biedt klanten volledige controle over hoe ze analysegegevens naar Adobe Analytics willen verzenden, zowel op de client als op de server.<br>Zie voor meer informatie [Logboekregistratie voor clientanalyse](/help/main/c-integrating-target-with-mac/a4t/before-implement.md#client-side) in *Voordat u implementeert*. |
| Meldingen verzenden | Staat ontwikkelaars toe om berichten te verzenden wanneer een ervaring door hun code in plaats van het gebruiken wordt teruggegeven `applyOffer()` of `applyOffers()`.<br>Zie voor meer informatie [adobe.target.sendNotifications(options)](https://developer.adobe.com/target/implement/client-side/atjs/atjs-functions/adobe-target-sendnotifications-atjs-21/){target=_blank}. |
| Beperkte bestandsgrootte | De grootte van at.js wordt verminderd met ~24%. De kleinere bestandsgrootte verbetert de laadprestaties van de pagina en verkort de downloadtijd op .js op de pagina. |
| op.js documentatie updates | Voor een volledige lijst van alle artikelen die zijn bijgewerkt vanwege de release van at.js 2.1.0, raadpleegt u de vermeldingen op 3 juni 2019 in [Documentatiewijzigingen](/help/main/r-release-notes/doc-change.md). |

### [!DNL Target] Standard/Premium 19.5.1 (21 mei 2019) {#tgt-19-5-1-historical}

(De uitgiftenummers tussen haakjes zijn voor intern [!DNL Adobe] gebruiken.)

#### Functie-updates

| Functie/verbetering | Beschrijving |
| --- | --- |
| Single Page App Visual Experience Composer (SPA VEC) | De SPA VEC bevat de volgende verbeteringen om uw werk sneller en efficiënter te maken:<ul><li>Wanneer u op een handeling in de SPA klikt, wordt het element op de site gemarkeerd waarop deze handeling wordt toegepast. Elke VEC-actie die onder een weergave wordt gemaakt, heeft vier corresponderende pictogrammen: Informatie, Bewerken, Verplaatsen en Verwijderen. Met de nieuwe functie &quot;Verplaatsen&quot; in deze release kunt u de handeling verplaatsen naar een gebeurtenis Pagina laden of een andere weergave die al bestaat in het deelvenster Wijzigingen. (TGT-33746)</li><li>U kunt vele acties uitvoeren alvorens de pagina in VEC laadt, of zelfs als de pagina er niet in slaagt volledig te laden (bijvoorbeeld, is de douanecode niet meer operationeel). Handelingen die niet kunnen worden bewerkt voordat de site wordt geladen, worden uitgeschakeld in de doelinterface. (TGT-33851 &amp; TGT-34149)</li></ul>Zie voor meer informatie [Single Page App (SPA) Visual Experience Composer](/help/main/c-experiences/spa-visual-experience-composer.md). |

#### Verbeteringen, correcties en wijzigingen

* De pictogrammen van de werkbalk worden correct weergegeven nadat u het laden van een pagina in de VEC hebt geannuleerd. Als specifieke handelingen pas kunnen worden uitgevoerd nadat de pagina volledig is geladen, worden de bijbehorende werkbalkpictogrammen uitgeschakeld. (TGT-33811)

### [!DNL Target] Standard/Premium 19.4.2 (30 april 2019) {#release-19-4-2}

Deze release bevat de volgende functies, wijzigingen en verbeteringen:

(De uitgiftenummers tussen haakjes zijn voor intern [!DNL Adobe] gebruiken.)

#### Functie-updates

| Functie/verbetering | Beschrijving |
| --- | --- |
| [!UICONTROL Visual Experience Composer] | De [!UICONTROL Visual Experience Composer] (VEC) bevat de volgende verbeteringen om uw werk sneller en efficiënter te maken:<ul><li>De DOM-padfunctie is nu beschikbaar wanneer u klikt op bijhouden.<br>Zie voor meer informatie [klikken op bijhouden](/help/main/c-activities/r-success-metrics/click-tracking.md#considerations).</li><li>In het deelvenster Stijlen kunt u de waarde van bestaande stijlen voor het geselecteerde element weergeven of bewerken. U kunt ook extra stijlen toevoegen.<br>Als u het deelvenster Stijlen wilt openen, klikt u vanuit de VEC op een pagina-element en vervolgens klikt u op [!UICONTROL Edit] > [!UICONTROL Styles].<br>Het deelvenster Stijlen wordt rechts van de VEC weergegeven. Het deelvenster bevat een lijst met stijlen waarmee u het geselecteerde element kunt bewerken of uitbreiden. Met een real-time CSS-editor kunt u wijzigingen weergeven en stijlen toevoegen als u dit comfortabel vindt met CSS (Cascading Style Sheets) of als u code van uw ontwikkelaar ontvangt.<br>Zie voor meer informatie [Stijlen](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md#styles) in *Opties voor composer visuele ervaring*.</li><li>De rijke Redacteur van de Tekst steunt nu genestelde HTML5 elementen.<br>HTML5-specificaties maken nieuwe combinaties van tags voor nesten mogelijk. De vorige versie van de rijke teksteditor ondersteunt geen nieuwe nesting van tags, zoals is toegestaan door de HTML5-specificatie. Dientengevolge, werden om het even welke genestelde die elementen in VEC werden geselecteerd niet behoorlijk behandeld, die tot ongewenste HTML veranderingen leidden. (TGT-33618)<br>Zie voor meer informatie [Tekst/HTML bewerken](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md#edit-text-html) in *Opties voor Visual Experience Composer*.</li> |

#### Verbeteringen, correcties en wijzigingen

* We hebben de workflow verbeterd wanneer u elementen verwijdert met de VEC. Verwijderde elementen worden nu verwijderd uit de [!UICONTROL Offers library] en van [!DNL Scene7] (indien van toepassing). Verwijderde elementen worden niet meer weergegeven in zoekresultaten. (TGT-31981)
* U kunt nu elementmappen verwijderen, zelfs als deze afbeeldingen bevatten (niet-lege mappen). (TGT-33265)

   Eerder kon u een niet-lege map niet verwijderen uit de bibliotheek met doelafbeeldingsaanbiedingen ([!UICONTROL Offers] > [!UICONTROL Image Offers]). Er wordt dan een &#39;&#39;Map is niet leeg!&#39;&#39; weergegeven bericht wanneer u probeert de map te verwijderen uit de gebruikersinterface.  Met deze functie voegen we de mogelijkheid toe om het verwijderen van mappen uit te voeren en een volledige map te verwijderen die een willekeurig aantal elementen en submappen in de map bevat. Deze functie is beschikbaar in de interface Doel en in de gebruikersinterface van Adobe Experience Cloud Assets.

   * U kunt niet-lege mappen uit de bibliotheek met afbeeldingsaanbiedingen verwijderen. Als in geen enkele activiteit naar alle afbeeldingen in de map wordt verwezen, worden de volledige map en de inhoud ervan verwijderd. Als er in een willekeurige activiteit naar bepaalde afbeeldingen in de map wordt verwezen, worden alle afbeeldingen zonder referenties verwijderd, maar blijven de afbeeldingen en mappen waarin naar wordt verwezen, behouden.
   * Het renderen van afbeeldingsaanbiedingen in de Afbeeldingselementkiezer gaat sneller en efficiënter.

   Zie voor meer informatie [Werken met inhoud in de bibliotheek](/help/main/c-experiences/c-manage-content/assets-working.md). (TGT-32897)

* We hebben de rendering van afbeeldingsaanbiedingen verbeterd in de middelenkiezer. Het weergeven en selecteren van aanbiedingen voor afbeeldingen gaat nu sneller en efficiënter. (TGT-32897)
* We hebben de verwerking van omleidingen naar URL&#39;s verbeterd wanneer u het laden van een pagina in de VEC annuleert. (TGT-33815)
* Nadat u een [!UICONTROL Recommendations] verzameling in de verzamelingskiezer, moet u nu op de knop [!UICONTROL Save] knop. Deze workflow is consistent met andere workflows binnen [!DNL Target]. (TGT-33205)
* Probleem verholpen waarbij een kleine set inzichtsrapporten 0% omzettingspercentages retourneerde in plaats van de werkelijke omrekeningskoersen. (TNT-32125)

### [!DNL Target] Standard/Premium 19.4.1 (15 april 2019) {#release-19-4-1}

Deze release is een onderhoudrelease en bevat de volgende wijziging:

(De uitgiftenummers tussen haakjes zijn voor intern [!DNL Adobe] gebruiken.)

* De [!DNL Adobe Experience Cloud] UI om de branding en productveranderingen te weerspiegelen. (TGT-33546, TGT-33272, en TGT-33331)

#### [!DNL Target] Standard/Premium 19.3.1 (29 maart 2019) {#release-19-3-1}

Deze release bevat de volgende functies, wijzigingen en verbeteringen:

(De uitgiftenummers tussen haakjes zijn voor intern [!DNL Adobe] gebruiken.)

| Functie/verbetering | Beschrijving |
| --- | --- |
| Visual Experience Composer | Visual Experience Composer (VEC) omvat de volgende verhogingen om uw werk sneller en efficiënter te maken:<ul><li>U kunt het laden van een website in VEC nu annuleren om het bewerken van een activiteit te deblokkeren. Deze verbetering is bijvoorbeeld handig als u een kleine bewerking wilt uitvoeren op de activiteit, de instellingen wilt controleren of aangepaste code wilt toevoegen en u niet wilt wachten tot de site is geladen. (TGT-31288)<br>Zie [Het laden van een pagina in de VEC annuleren](/help/main/c-experiences/c-visual-experience-composer/visual-experience-composer.md#cancel-loading).</li><li>U kunt vele acties uitvoeren alvorens de pagina in VEC laadt, of zelfs als de pagina er niet in slaagt volledig te laden (bijvoorbeeld, is de douanecode niet meer operationeel). Handelingen die niet kunnen worden bewerkt voordat de site wordt geladen, worden uitgeschakeld in de doelinterface. (TGT-31288, TGT-31611, en TGT-32602)<br>Zie [Een pagina bewerken terwijl de pagina wordt geladen of nadat de pagina niet is geladen](/help/main/c-experiences/c-visual-experience-composer/visual-experience-composer.md#loading).</li><li>De VEC geeft het DOM-pad weer, zodat u het juiste element eenvoudig kunt selecteren tijdens het maken of bewerken van ervaringen. (TGT-13422)<br>Zie [Navigeren door elementen met het DOM-pad](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md#dom-path).</li></ul> |

### at.js versie 2.0.1 (19 maart 2019) {#atjs201}

Dit is een onderhoudrelease met de volgende verbeteringen en oplossingen:

(De uitgiftenummers tussen haakjes zijn voor intern [!DNL Adobe] gebruiken.)

* Probleem verholpen met een zeldzame omstandigheid in de opiniepeilingscode voor DOM die JavaScript-uitzonderingen voor bepaalde klanten veroorzaakte. (TNT-31869)
* Meldingen dat weergaven werden gerenderd, zijn losgekoppeld van gebeurtenishandlers voor het bijhouden van klikken. In eerste instantie heeft Target geen meldingen verzonden als click-event-handlers die tot een weergegeven weergave behoren, niet konden worden gekoppeld. Het doel verzendt nu een meningsbericht zelfs wanneer de klikelementen niet worden gevonden. (TNT-31969)
* Probleem verholpen waarbij de omleidingsvlag voor de gebeurtenis die na het verzoek werd uitgevoerd, altijd werd ingesteld op true. (TNT-31907)
* Probleem opgelost dat ertoe leidde dat VEC opnieuw rangschikte actie als succes werd geregistreerd, zelfs wanneer de elementen ontbraken. (TNT-31924)
* Probleem opgelost waarbij meldingen voor bepaalde klanten werden verzonden om de eigenschappentoken voor Enterprise-machtigingen niet te bevatten. (TNT-31999)

>[!NOTE]
>
>Als u [!DNL Adobe] De opt-in steun voor de Algemene Verordening van de Bescherming van Gegevens (GDPR), zou u bij.js 1.7.1 moeten uitvoeren. Ondersteuning voor aanmelden wordt momenteel niet ondersteund in at.js 2.*x*.

### at.js versie 1.7.1 (19 maart 2019) {#atjs171}

Dit is een onderhoudrelease met de volgende oplossing:

(De uitgiftenummers tussen haakjes zijn voor intern [!DNL Adobe] gebruiken.)

* Probleem verholpen met een zeldzame omstandigheid in de opiniepeilingscode voor DOM die JavaScript-uitzonderingen voor bepaalde klanten veroorzaakte. (TNT-31869)

### Wijzigingen in Platform (19 februari 2019) {#atjs2}

| Functie/verbetering | Beschrijving |
| --- | --- |
| at.js versie 2.0.0<br>19 februari 2019 | at.js 2.x is nu beschikbaar.<br>De nieuwste versie van at.js verstrekt rijke eigenschapreeksen die uw zaken uitrusten om verpersoonlijking op volgende generatie cliënt-zijtechnologieën uit te voeren. Deze nieuwe versie is gericht op het upgraden van at.js voor harmonieuze interacties met toepassingen van één pagina (SPA).<br>Hier volgen enkele voordelen van het gebruik van at.js 2.x die niet beschikbaar zijn in eerdere versies:<ul><li>De capaciteit om alle aanbiedingen op paginading in het voorgeheugen onder te brengen om veelvoudige servervraag aan één enkele servervraag te verminderen.</li><li>Verbeter de ervaringen van uw eindgebruikers op uw site aanzienlijk, omdat aanbiedingen direct via het cachegeheugen worden weergegeven zonder vertraging die traditionele serveraanroepen introduceren.</li><li>Eenvoudige one-line van code en éénmalige ontwikkelaarsopstelling om uw marketers toe te laten om A/B en de activiteiten van de Ervaring (XT) via Visual Experience Composer (VEC) op uw enige paginatoepassingen tot stand te brengen en in werking te stellen.</li></ul>at.js 2.x introduceert de volgende nieuwe functies:<ul><li>getOffers()</li><li>applyOffers()</li><li>triggerView()</li></ul>De volgende functies zijn vervangen door de introductie van at.js 2.x:<ul><li>mboxCreate()</li><li>mboxDefine</li><li>registerExtension()</li></ul>Zie voor meer informatie [Bijwerken van at.js 1.x naar at.js 2.x](https://developer.adobe.com/target/implement/client-side/atjs/target-atjs-versions/){target=_blank} and [at.js functions](https://developer.adobe.com/target/implement/client-side/atjs/atjs-functions/atjs-functions/){target=_blank}.<br>**Note**: If you require Adobe Opt-in support for the [General Data Protection Regulation](https://developer.adobe.com/target/before-implement/privacy/cmp-privacy-and-general-data-protection-regulation/){target=_blank} (GDPR){target=_blank}, moet u momenteel gebruiken om .js 1.7.0. Ondersteuning voor aanmelden wordt niet ondersteund in at.js 2.x. |
| at.js versie 1.7.0<br>14 februari 2019 | om.js 1.7.0 is beschikbaar.<br>Deze release biedt ondersteuning voor Adobe Opt-In. Adobe Opt-In is een manier om de integratie van Adobe-oplossingen met toestemmingsbeheerplatforms te vereenvoudigen.<br>Voor meer informatie over Adobe Opt-in, zie [Privacy en algemene gegevensbeschermingsverordening](https://developer.adobe.com/target/before-implement/privacy/cmp-privacy-and-general-data-protection-regulation/){target=_blank} (GDPR){target=_blank}.<br>This release also fixes an issue where Target might override redirect URL parameters with parameters that are coming from the redirect URL.<br>**Note**: If you require Adobe Opt-in support for GDPR, you must currently use at.js 1.7.0. Opt-in support is not supported in at.js 2.x.<br>For a list of all versions, see [at.js version details](https://developer.adobe.com/target/implement/client-side/atjs/target-atjs-versions/){target=_blank}. |

### [!DNL Target] Standard/Premium 19.2.1 (19 februari 2019) {#target-19-2-1}

Deze release bevat de volgende functies, wijzigingen en verbeteringen:

(De uitgiftenummers tussen haakjes zijn voor intern [!DNL Adobe] gebruiken.)

| Functie/verbetering | Beschrijving |
| --- | --- |
| Single Page App Visual Experience Composer | Met Visual Experience Composer (VEC) voor Single Page Apps (SPA) kunnen marketers tests maken en inhoud personaliseren op SPA op een doe-het-zelfmanier zonder voortdurende ontwikkelingsafhankelijkheden. VEC kan worden gebruikt om activiteiten op populaire kaders, zoals React en Angular tot stand te brengen. (TGT-27916)<br>Zie voor meer informatie [Single Page App (SPA) Visual Experience Composer](/help/main/c-experiences/spa-visual-experience-composer.md) en [Integratie van toepassing met één pagina](https://developer.adobe.com/target/implement/client-side/atjs/how-to-deployatjs/target-atjs-single-page-application/){target=_blank}.<br>Naast het bovenstaande artikel zijn er veel onderwerpen die te maken hebben met SPA en at.js die betrekking hebben op deze functie en hoe deze te implementeren. Zie voor meer informatie [Documentatiewijzigingen](/help/main/r-release-notes/doc-change.md). |
| Visual Experience Composer | Visual Experience Composer (VEC) omvat de volgende verhogingen om uw werk sneller en efficiënter te maken:<ul><li>U kunt nu de opties Invoegen voor en Invoegen na in de VEC gebruiken tijdens het invoegen [AEM ervaren fragmenten](/help/main/c-experiences/c-manage-content/aem-experience-fragments.md). Zie [Opties voor Visual Experience Composer](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md). (TGT-32385)</li><li>De [!DNL Adobe Target] Met de VEC Helper-browserextensie voor Google Chrome kunt u websites betrouwbaar laden binnen de VEC zodat u snel een product kunt ontwerpen en een kwaliteitscontrole kunt gebruiken. Zie [Helpextensie Visual Experience Composer](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/vec-helper-browser-extension.md). (TGT-32746)</li></ul> |
| ![Premium badge](/help/main/assets/premium.png)<br>Recommendations in [!UICONTROL A/B Test] en [!UICONTROL Experience Targeting] activiteiten | U kunt nu aanbevelingen opnemen in [!UICONTROL A/B Test] (inclusief [!UICONTROL Auto-Allocate] en [!UICONTROL Auto-Target]) en [!UICONTROL Experience Targeting] (XT) activiteiten. Dit opent volledig nieuwe mogelijkheden, zoals:<ul><li>Test- en doelaanbevelingen en niet-aanbevolen inhoud binnen dezelfde activiteit.</li><li>Experimenteer eenvoudig met het plaatsen van aanbevelingen op de pagina, inclusief de volgorde van meerdere aanbevelingen.</li><li>Druk automatisch het verkeer aan de best presterende aanbevelingen ervaring gebruikend [!UICONTROL Auto-Allocate].</li><li>Wijs bezoekers dynamisch toe aan op maat gemaakte aanbevelingen op basis van hun individuele profielen en gebruik daarbij [!UICONTROL Auto-Target].</li></ul>Om aan de slag te gaan, maakt u een [!UICONTROL A/B Test] of [!UICONTROL Experience Targeting] activiteit met behulp van de VEC en gebruik de [!UICONTROL Insert Before], [!UICONTROL Insert After], of [!UICONTROL Replace With] actie om aanbevelingen aan een ervaring toe te voegen. (RECS-6166)<br>Zie voor meer informatie [Recommendations als voorstel](/help/main/c-recommendations/recommendations-as-an-offer.md). |
| ![Premium badge](/help/main/assets/premium.png)<br>Ondersteuning voor Enterprise-machtigingen in doel-API&#39;s | [Adobe Target Admin API&#39;s](https://developers.adobetarget.com/api/#admin-apis) zal nu ten volle profiteren van dezelfde mogelijkheden voor Enterprise-machtigingen die in de doelinterface zijn gevonden. Starten **21 feb. 2019** systeembeheerders hebben via programmacode toegang tot rapportgegevens en kunnen activiteiten, aanbiedingen en soorten publiek in elke werkruimte maken en beheren. Deze acties waren voorheen beperkt tot de standaardwerkruimte. De ondersteuning van Automated Personalization-activiteiten (AP) zal in een toekomstige release plaatsvinden. |

**Verbeteringen, correcties en wijzigingen**

* Om de veiligheid te verbeteren, [!DNL Target] voorkomt u nu dat eindpunten van Amazon Web Services-metagegevens (AWS) worden geopend tijdens het laden van de VEC. (TGT-33129)

### Wijzigingen in Platform (januari 2019) {#platform-19-1-previous}

| Functie/verbetering | Beschrijving |
| --- | --- |
| Doelstelling<br>25 januari 2019 | Wijzigingen aangebracht in de manier waarop &#39;target&#39; overeenkomt met functie voor &#39;equals&#39;-vergelijkingen met niet-decimale en decimale waarden die worden geretourneerd door profielscripts of een andere invoerbron, zoals mbox-parameters, profielparameters, enz.<br>Zie voor meer informatie [Doelstellingen en doelgroepen](/help/main/c-target/c-troubleshooting-targets-and-audiences/troubleshooting-targets-and-audiences.md) Veelgestelde vragen. |
| Profielscripts<br>17 januari 2019 | Om prestatieredenen raden we een geretourneerde waarde aan die niet langer is dan 256 tekens.<br>Als de geretourneerde waarde van een tekenreeks groter is dan 2048 tekens, wordt het script door het systeem uitgeschakeld.<br>Als voor een geretourneerde waarde van een array de grootte van de samengevoegde waarden van de array groter is dan 2048 tekens, wordt het script door het systeem uitgeschakeld.<br>Voor meer informatie over de tekenlimieten en andere limieten (grootte, publiek, profielen, waarden, parameters, enz.) die van invloed zijn op activiteiten en andere elementen in Target, zie [Limieten](/help/main/r-troubleshooting-target/target-limits.md). |
| at.js<br>16 januari 2019 | at.js 1.6.4 is een onderhoudsrelease en behandelt de volgende problemen:<ul><li>Probleem verholpen waarbij zich in Microsoft Internet Explorer 11 een zeldzame omstandigheid manifesteerde die dubbele aanbiedingen tot gevolg had. (TNT-31374)</li><li>Probleem verholpen dat invloed had op het bijhouden van klikken als er een standaardaanbieding is met een click-token en HTML-aanbiedingen. (TNT-31493)</li><li>Het mboxEdgeCluster-cookie is uitgebreid met elke doelaanvraag. Dit wordt alleen gebruikt wanneer mboxEdgeOverride is ingeschakeld. (TNT-31485)</li></ul> |

### [!DNL Target] Standard/Premium 19.1.1 (22 januari 2019) {#release-19-1-1-previous}

Deze release bevat de volgende functies, wijzigingen en verbeteringen:

(De uitgiftenummers tussen haakjes zijn bedoeld voor intern gebruik van Adobe.)

| Functie/verbetering | Beschrijving |
| --- | --- |
| ![Doel Premium-badge](/help/main/assets/premium.png)<br/>[!UICONTROL Enterprise Permissions] ondersteuning in [!DNL Target] API&#39;s | [Adobe Target Admin API&#39;s](https://developers.adobetarget.com/api/#admin-apis) zal nu ten volle profiteren van dezelfde mogelijkheden voor Enterprise-machtigingen die in de doelinterface zijn gevonden. Starten **21 feb. 2019**, zullen de systeembeheerders tot rapportgegevens programmatically kunnen toegang hebben evenals activiteiten, aanbiedingen, en publiek binnen om het even welke werkruimte creëren en beheren. Deze acties waren voorheen beperkt tot de standaardwerkruimte. De ondersteuning van Automated Personalization-activiteiten (AP) zal in een toekomstige release plaatsvinden. |
| ![Doel Premium-badge](/help/main/assets/premium.png)<br/>[!UICONTROL Recommendations]: filterverzamelingen en -uitsluitingen naar omgeving (hostgroep) | U kunt nu een voorvertoning weergeven van de inhoud van [!UICONTROL Recommendations] verzamelingen en uitsluitingen voor een geselecteerde omgeving (hostgroep).<br/>Eerder, toen u een inzameling of een uitsluiting bekeken, waren de getoonde punten bevatte resultaten voor de standaardgastheergroep (die in wordt gespecificeerd [!UICONTROL Recommendations > Settings > Default Host Group]).<br/>Wanneer u nu een verzameling of uitsluiting maakt of bijwerkt, kunt u de opdracht [!UICONTROL Environment] om de omgeving te kiezen waarvoor u de resultaten wilt bekijken. De nieuwe [!UICONTROL Environment] bespaart u tijd en moeite, omdat u niet meer naar de [!UICONTROL Settings] pagina om de juiste standaardhostgroep te selecteren voordat u verzamelingen en uitsluitingen maakt of bewerkt.<br/>**Opmerking:** Nadat u de geselecteerde omgeving hebt gewijzigd, klikt u op [!UICONTROL Search] om de geretourneerde resultaten bij te werken.<br/>De nieuwe [!UICONTROL Environment] is beschikbaar op de volgende plaatsen in het dialoogvenster [!DNL Target] UI:<ul><li>[!UICONTROL Catalog Search] ([!UICONTROL Recommendations > Catalog Search])</li><li>[!UICONTROL Create Collection] dialoogvenster ([!UICONTROL Recommendations > Collections > Create New])</li><li>[!UICONTROL Update Collection] dialoogvenster ([!UICONTROL Recommendations > Collections > Edit])</li><li>[!UICONTROL Create Exclusion] dialoogvenster ([!UICONTROL Recommendations > Exclusions > Create New])</li><li>[!UICONTROL Update Exclusion] dialoogvenster ([!UICONTROL Recommendations > Exclusions > Edit])</li></ul><br>Raadpleeg de volgende onderwerpen voor meer informatie:<uL><li>[Verzamelingen](/help/main/c-recommendations/c-products/collections.md)</li><li>[Uitsluitingen](/help/main/c-recommendations/c-products/exclusions.md)</li><li>[Catalogus zoeken](/help/main/c-recommendations/c-products/catalog-search.md)</li><li>[Instellingen](https://developer.adobe.com/target/implement/recommendations/){target=_blank}</li><li>[Recommendations: filterverzamelingen en -uitsluitingen naar omgeving (hostgroep)](/help/main/administrating-target/hosts.md)</li></ul>(TGT-20622)</ul> |

**Verbeteringen, correcties en wijzigingen**

* Probleem verholpen waarbij de knop Opslaan uitgeschakeld bleef wanneer de gebruiker zich bij het verlopen van de sessie aanmeldt bij het dialoogvenster voor aanmelding tijdens het bewerken van een publiek. (TGT-32722)

## Opmerkingen bij de release - 2018 {#reference_36ACC83E135A41F28104C44755C26D5B}

### Platform (15 november 2018) {#section_484A56774E004282B98FFFF851E4E670}

<table id="table_7320E43397D2471FA313A9D6FC21E55F"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Functie/verbetering </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>om.js 1.6.3 </p> </td> 
   <td colname="col2"> <p>at.js versie 1.6.3 is nu beschikbaar. </p> <p> 
     <ul id="ul_2C7CB74B1AAF4B52B6EB382977F7DC28"> 
      <li id="li_07CF8EDB25E24A7AB9B7A0F3402BAEB1"> <p>Kiezers hebben nu een CSS-escape-teken als ze id's of CSS-klassen bevatten die beginnen met een cijfer, twee afbreekstreepjes of een afbreekstreepje gevolgd door een cijfer (bijvoorbeeld #-123). (TNT-31061) </p> </li> 
      <li id="li_6504E90D7C534A1BB9A2DE8510CE3B90"> <p>Probleem verholpen dat werd geïntroduceerd met at.js 1.6.2, waarbij VEC-aanbiedingen (Visual Experience Composer) uit verschillende activiteiten die van toepassing zijn op dezelfde CSS-kiezer de prioriteit van de activiteit niet respecteerde. (TNT-31052) </p> </li> 
      <li id="li_D347CA513F1240E4BF79D757287AB30C"> <p>Probleem verholpen waarbij een belofte werd nagekomen in omgevingen waar geen native ondersteuning voor beloften bestond. (TNT-30974) </p> </li> 
      <li id="li_17F41A84CCFF41D7993E35DE10F87066"> <p>Problemen worden nu correct vastgelegd en gerapporteerd via de gebeurtenis content-rendering mislukt. Eerder werd mogelijk gemeld dat JavaScript goed was uitgevoerd, zelfs als dat niet het geval was. (TNT-30599) </p> </li> 
     </ul> </p> <p>Zie voor meer informatie <a href="https://developer.adobe.com/target/implement/client-side/atjs/target-atjs-versions/" format="dita" scope="local"> at.js - Versiedetails</a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

### Target Standard/Premium 18.11.1 (12 november 2018) {#section_6BBA8B1EE9D241C28E12856A375E97F6}

De [!DNL Target] Standard/Premium-release op 12 november bevat back-endverbeteringen, oplossingen en wijzigingen. De [!UICONTROL Personalization Insights] De verslagen zullen op 14 november beschikbaar zijn.

<table id="table_EF529199D1C741F7BDBC9C41A37B7D26"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Functie/verbetering </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1" class="premium"> <p>Persoonlijkheidsrapporten </p> <p> <p>Opmerking: Beschikbaar op 14 november 2018. </p> </p> </td> 
   <td colname="col2"> <p>Gebruikers van <span class="wintitle"> Automated Personalization (AP)</span> en <span class="wintitle"> Auto-Target (AT)</span> activiteiten: </p> <p> 
     <ul id="ul_C338AC34C57C49E1A8DFA471167EC40A"> 
      <li id="li_2329BFC8CC524EBBA99C2F8EDC745B90"> <p><b><span class="wintitle"> Geautomatiseerde segmenten</span>:</b> Verschillende bezoekers reageren anders op de aanbiedingen/ervaringen in uw AP/AT-activiteit. Dit rapport laat zien hoe verschillende geautomatiseerde segmenten die door de personalisatiemodellen van Target worden gedefinieerd, op de aanbiedingen/ervaringen in de activiteit hebben gereageerd. </p> </li> 
      <li id="li_48556C9BAD48476DA00DD666F5265E2B"> <p><b><span class="wintitle"> Belangrijke kenmerken</span>:</b> In verschillende activiteiten zijn verschillende kenmerken meer of minder belangrijk voor de manier waarop het model beslist om zich aan te passen. Dit rapport toont de belangrijkste kenmerken die het model en hun relatieve belang beïnvloedden. </p> </li> 
     </ul> </p> <p>Zie <a href="/help/main/c-reports/c-personalization-insights-reports/personalization-insights-reports.md#concept_A897070E1EDC403EB84CFB7A6ECAD767" format="dita" scope="local"> Persoonlijkheidsrapporten</a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

### Target Standard/Premium 18.10.1 (24 oktober 2018) {#section_FA37BF4E840B424E8BC4791D7234FE2A}

Deze release bevat de volgende functies en verbeteringen:

(De uitgiftenummers tussen haakjes zijn bedoeld voor intern gebruik van Adobe.)

<table id="table_B1911F55CCE1428881D258380A8254A9"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Functie/verbetering </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Ervaringen </p> </td> 
   <td colname="col2"> <p>U kunt nu een ervaring kopiëren in een Experience Targeting-activiteit (XT), zodat u er kleine wijzigingen in kunt aanbrengen zonder dat u de ervaring helemaal opnieuw hoeft te maken. Deze mogelijkheid was al beschikbaar voor A/B-tests. (TGT-31504) </p> <p>Zie <a href="https://experienceleague.adobe.com/docs/target/using/activities/experience-targeting/create-targeting/xt-add-experience.html" format="html" scope="external"> Ervaring maken </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p>Aanbiedingen in Automated Personalization (AP)-activiteiten </p> </td> 
   <td colname="col2"> <p>In de release van september 2018 hebben we een verbetering toegevoegd waarmee u aanbiedingen kunt filteren op rapportagegroepen. U kunt nu filteren op Niet toegewezen aanbiedingen zodat u een rapportgroep kunt toewijzen aan een aanbieding die momenteel niet aan een rapportgroep is toegewezen. (TGT-31882) </p> <p>Zie <a href="https://experienceleague.adobe.com/docs/target/using/activities/automated-personalization/create-ap-activity.html" format="html" scope="external"> Een Automated Personalization-activiteit maken </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Rapportage bron voor activiteiten </p> </td> 
   <td colname="col2"> <p>In <span class="wintitle"> Beheer </span> &gt; <span class="wintitle"> Visual Experience Composer </span>kunt u de rapportbron voor uw activiteiten selecteren. <span class="keyword"> Doel </span> of <span class="keyword"> Adobe Analytics </span>. U kunt ook de rapportbron per activiteit selecteren. </p> <p>Beginnend met deze versie, zijn er sommige belangrijke werkschemaoverwegingen u zich van bewust zou moeten zijn wanneer u de rapporteringsbron in kiest <span class="wintitle"> Voorkeuren </span> of per activiteit.</p></td> 
  </tr> 
 </tbody> 
</table>

**Verbeteringen, correcties en wijzigingen**

Dit [!DNL Target] de release bevat de volgende verbeteringen, oplossingen en wijzigingen:

* Verbeterde verwerking van publiek waarnaar wordt verwezen in Target-activiteiten die zijn verwijderd in Adobe Audience Manager (AAM). (TGT-2338)

   * Als een publiek in AAM is verwijderd, verschijnt er een waarschuwingspictogram in het dialoogvenster [!UICONTROL Audience] wordt weergegeven. Een hulpmiddel-uiteinde in UI wijst ook erop dat het publiek in AAM werd geschrapt.
   * Als u meerdere soorten publiek probeert te combineren met een verwijderd publiek of als u een activiteit probeert op te slaan die verwijst naar een verwijderd publiek, wordt een waarschuwingsbericht weergegeven.

   Zie [Informatie over publiek](https://experienceleague.adobe.com/docs/target/using/audiences/create-audiences/audiences.html).

* Probleem verholpen waardoor gebruikers in bepaalde situaties geen activiteit konden maken toen Adobe Analytics als bron voor rapportage op de [!UICONTROL Administration] pagina. Gebruikers zagen een bericht &quot;Selecteer een rapportsuite&quot;, ook al kregen ze niet de mogelijkheid om de rapportsuite te selecteren. (TGT-31968)

### Platform (19 oktober 2018)

<table id="table_7320E43397D2471FA313A9D6FC21E55F"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Functie/verbetering </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>om.js 1.6.2 </p> </td> 
   <td colname="col2"> <p>Dit is een onderhoudsrelease en het volgende probleem wordt opgelost: </p> <p> 
     <ul id="ul_2C7CB74B1AAF4B52B6EB382977F7DC28"> 
      <li id="li_07CF8EDB25E24A7AB9B7A0F3402BAEB1"> <p>Probleem verholpen waarbij sites van bepaalde klanten tot een oneindige 'async'-lus leiden. </p> </li> 
     </ul> </p> <p> <p>Belangrijk: Daarnaast bevat at.js versie 1.6.2 ook alle verbeteringen en correcties die zijn opgenomen in at.js versie 1.6.1 en 1.6.0. Deze versies kunnen niet meer worden gedownload. We raden u aan een upgrade naar versie 1.6.2 uit te voeren als u 1.6.1 of 1.6.0 gebruikt. </p> </p> <p>Zie voor meer informatie <a href="https://experienceleague.adobe.com/docs/target/using/implement-target/client-side/target-atjs-versions.html" format="html" scope="external"> at.js - Versiedetails </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

### Target Standard/Premium 18.9.1 (26 september 2018) {#section_95CF405C95E44DBEA3CB308FDD5071CD}

<!-- 

target/r_release-notes-2018.xml

 -->

Deze release bevat de volgende functies en verbeteringen:

>[!NOTE]
>
>De uitgiftenummers tussen haakjes zijn bedoeld voor intern gebruik van Adobe.

<table id="table_7ABC8E7477194D4C8C9E82ECE60E3498"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Functie/verbetering </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1" class="premium"> <p>Aanbiedingen in Automated Personalization (AP)-activiteiten </p> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_9C39ACD865CE4167BDBAA093EDFD3B68"> 
      <li id="li_19710BA5965E4F858B128E1E9FF89471"> <p>U kunt nu meerdere voorstellen van dezelfde locatie in een uitsluitingsgroep gebruiken. Voor een groot aantal uitsluitingen (in volgorde van 1000) ziet u ook hoe sneller het dialoogvenster Inhoud beheren en de pagina met voorvertoningen worden geladen wanneer u een Automated Personalization-activiteit (AP) ontwerpt. (TGT-31329) Zie <a href="/help/main/c-activities/t-automated-personalization/managing-exclusions.md#topic_30B4E4F89C914EB2B20B038C0299ED2E" format="dita" scope="local"> Uitsluitingen beheren </a>. </p> </li> 
      <li id="li_542C66E2998541BC87D0A96F4672C665"> <p>U kunt voorstellen nu filteren door groepen te melden. (TGT-31643) Zie <a href="/help/main/c-activities/t-automated-personalization/create-ap-activity.md#task_8AAF837796D74CF893CA2F88BA1491C9" format="dita" scope="local"> Automated Personalization-activiteiten maken </a>. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Visual Experience Composer (VEC) </p> </td> 
   <td colname="col2"> <p>We hebben een <span class="wintitle"> Invoegen voor </span> actie aan de (VEC). Dit is vergelijkbaar met het bestaande <span class="wintitle"> Invoegen na </span> optie. Wanneer u een element op de pagina selecteert, kunt u klikken <span class="wintitle"> Invoegen voor </span> en kiest u of u een afbeelding, HTML of tekst wilt invoegen. Het ingevoegde element wordt vóór het geselecteerde element weergegeven. (TGT-30473) Zie <a href="/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md#reference_3BD1BEEAFA584A749ED2D08F14732E81" format="dita" scope="local"> Opties voor composer visuele ervaring </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Verbeteringen, correcties en wijzigingen**

Dit [!DNL Target] de release bevat de volgende verbeteringen, oplossingen en wijzigingen:

* We hebben de look and feel van de Criteria cards bijgewerkt om intuïtiever en gebruiksvriendelijker te zijn. (TGT-30469)
* Prestatieverbeteringen in de gebruikersinterface voor sneller laden van pagina&#39;s.

### Target Standard/Premium 18.8.1 (21 augustus 2018) {#section_66A0030993D54565BE30E56AC9CAC1DA}

Deze release bevat de volgende functies en verbeteringen:

>[!NOTE]
>
>De uitgiftenummers tussen haakjes zijn bedoeld voor intern gebruik van Adobe.

<table id="table_4785030753B24AA1A973E1DF790B83DD"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Functie/verbetering </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1" class="premium"> <p>Persoonlijkheidsrapporten </p> </td> 
   <td colname="col2"> <p>Toegang tot gespecialiseerde rapporten voor uw Automated Personalization (AP) en Auto-Target (AT) activiteiten: </p> <p> 
     <ul id="ul_54652C5AE0984657BB9A0E46673CB2F1"> 
      <li id="li_0807959BA7D94114BE47A43D3454CAB4"> <p><b>Geautomatiseerde segmenten:</b> Zie hoe de verschillende geautomatiseerde segmenten die door de verpersoonlijkingsmodellen van Target worden bepaald op aanbiedingen/ervaringen in uw activiteit antwoorden. </p> </li> 
      <li id="li_48210B1E4EB24288B96CDECAF1CEE34A"> <p><b>Waardering modelkenmerk:</b> Zie de hoogste attributen die de personalisatiemodellen van het Doel en het relatieve belang van elk attribuut beïnvloedden. </p> </li> 
     </ul> </p> <p> <p>Opmerking: Deze functie is binnenkort beschikbaar. Blijf op de hoogte voor een aankondiging van de exacte datum waarop deze functie klaar is voor gebruik. </p> </p> <p>Zie <a href="/help/main/c-reports/c-personalization-insights-reports/personalization-insights-reports.md#concept_A897070E1EDC403EB84CFB7A6ECAD767" format="dita" scope="local"> Persoonlijkheidsrapporten </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Visual Experience Composer (VEC) </p> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_406B95728467496CA6CC5892F88B69FE"> 
      <li id="li_6D717868FB204A3A95832E709773B424"> <p>U kunt het deelvenster Wijzigingen verticaal aan de zijkant van de doelinterface koppelen of horizontaal aan de onderkant. </p> <p>Zie <a href="/help/main/c-experiences/c-visual-experience-composer/c-vec-code-editor/vec-code-editor.md#concept_B3A6E9EE3A60406DB640E205EA1745B5" format="dita" scope="local"> Wijzigingen </a>. </p> </li> 
      <li id="li_27750AFBCB3E4CB8B0B53592B2447E59"> <p>We hebben verschillende VEC-acties gegroepeerd om uw werk sneller en efficiënter te maken. (TGT-30472) </p> <p>Zie <a href="/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md#reference_3BD1BEEAFA584A749ED2D08F14732E81" format="dita" scope="local"> Opties voor composer visuele ervaring </a>. </p> </li> 
      <li id="li_27FEBEE245E64ADF9ADF561C6CBBDE8F"> <p>U kunt aanbiedingen efficiënter bewerken dankzij een groter bewerkingsvenster. (TGT-31052) </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Tips en trucs </p> </td> 
   <td colname="col2"> <p>Haal het meeste uit Adobe Target door meer te leren over verschillende functies en te zien waarom je ze een poging moet doen. De functies Tips en trucs worden weergegeven op de pagina Activiteiten en bevatten koppelingen naar video's, gebruiksscenario's, blogs, documentatie en nog veel meer. Word een doelenergiegebruiker! </p> <p>Zie <a href="/help/main/c-activities/activities.md#section_F77F30A246A14B538D9363B7F3639F97" format="dita" scope="local"> Tips en trucs </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Doelbasis van de webinarreeks </p> </td> 
   <td colname="col2"> <p>Neem deel aan de nieuwe Webinar Reeks van de Grondbeginselen van het Doel, een Reeksen van het Succes van de Klant Webinar die aan u door de Gemeenschap wordt gebracht. </p> <p> De volgende webinar, Best Practices in Reporting &amp; Value Socialization, is gepland voor 22 augustus 2018 van 8 tot 9.00 uur. (PDT). </p> <p>Zie <a href="/help/main/cmp-resources-and-contact-information.md#concept_11902FAC95C64479AABE020557A7EEE4" format="dita" scope="local"> Doelbasis van de webinarreeks </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Verbeteringen, correcties en wijzigingen**

Dit [!DNL Target] de release bevat de volgende verbeteringen, oplossingen en wijzigingen:

* We hebben verschillende verbeteringen toegevoegd om Target nog veiliger te maken dan voorheen. (TGT-31090, TGT-31089, TGT-31143)

### Target Standard/Premium 18.7.1 (25 juli 2018) {#section_A4A9C20EB677455F84FF0BA389F645E5}

Deze release bevat de volgende functies en verbeteringen:

>[!NOTE]
>
>De uitgiftenummers tussen haakjes zijn bedoeld voor intern gebruik van Adobe.

<table id="table_7E3513EABA4948DC92EADCCE0234A9FF"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Functie/verbetering </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Activiteiten in het kader van A/B en Experience Targeting (XT) </p> </td> 
   <td colname="col2"> <p>Bewerk en verwijder ervaringen rechtstreeks uit het activiteitendiagram. Nu kunt u in de Visuele Composer van de Ervaring (VEC) voor een specifieke ervaring springen of een ervaringsrecht van het diagram schrappen. </p> <p> <img src="assets/experience_edit.png" id="image_FA6E5F07B04A4B4BA02EA71EDB6908A7" /> </p> <p>Zie: </p> <p> 
     <ul id="ul_CB0C1146716F4C09BF924CF3DFA7DC1A"> 
      <li id="li_3767DD36F597481FB312CC577CD668F0"> <p>A/B-activiteit: <a href="/help/main/c-activities/t-test-ab/t-test-create-ab/ab-add-experience.md#task_454646F2895242D3B92DC395A0CE1A00" format="dita" scope="local"> Ervaring toevoegen </a> </p> </li> 
      <li id="li_E2990CA178C6446BA7206643A3164FEF"> <p>XT-activiteit: <a href="/help/main/c-activities/t-experience-target/t-xt-create/xt-add-experience.md#task_454646F2895242D3B92DC395A0CE1A00" format="dita" scope="local"> Ervaring maken </a> </p> </li> 
     </ul> </p> <p>(TGT-30229) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Soorten publiek </p> </td> 
   <td colname="col2"> <p>Vergelijk een profielkenmerk met een ander profielkenmerk in plaats van met een statisch getal. </p> <p>Zie <a href="/help/main/c-target/c-audiences/creating-a-profile-attribute-comparison-audience.md#concept_4C2124B79A5B4556A6C1D10C0F5E40A0" format="dita" scope="local"> Het creëren van een publiek van de Vergelijking van de Attributen van het Profiel </a>. </p> <p> (TGT-28406) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Aangepaste code </p> </td> 
   <td colname="col2"> <p>'Aangepaste code' is nu beschikbaar in het deelvenster 'Wijzigingen toevoegen' in plaats van een eigen tabblad. U kunt ook meer dan één aangepaste code toevoegen en elke aangepaste code optioneel een naam geven. (TGT-28504) </p> <p>Zie <a href="/help/main/c-experiences/c-visual-experience-composer/c-vec-code-editor/vec-code-editor.md#concept_B3A6E9EE3A60406DB640E205EA1745B5" format="dita" scope="local"> Wijzigingen </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p>Recommendations </p> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_371C18DFC6D24E94B3D4FFFD83FC8D3A"> 
      <li id="li_9D11939014E7479AB7FD8910852A5386"> <p>Een lijst met activiteiten weergeven die verwijzen naar een geselecteerde criteria op de bijbehorende Criteria-kaart. De kaart vermeldt actieve en inactieve activiteiten. (TGT-27672) </p> </li> 
      <li id="li_B97BF9305EB04F6D8B1F6178B2E0CB34"> <p>In het activiteitendiagram worden nu Criteria-kaarten weergegeven wanneer de resultaten gereed zijn om te worden weergegeven. (TGT-27673) </p> <p>Zie <a href="/help/main/c-recommendations/c-algorithms/algorithms.md" format="dita" scope="local"> Criteria </a>. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Experience Templates </p> </td> 
   <td colname="col2"> <p>De Malplaatjes van de Ervaring van Adobe Target zijn vooraf gecodeerde aanbiedingssteekproeven met configureerbare input die in Doel moet worden gebruikt om sommige gemeenschappelijke gevallen van het marktorgebruik uit te voeren. Deze ervaringsmalplaatjes worden verstrekt vrij aan ontwikkelaars en verkopers als uitgangspunt om sommige gemeenschappelijke externe gebruiksgevallen in Adobe Target uit te voeren - of via Visual Experience Composer of op vorm-Gebaseerde Composer van de Ervaring. Mogelijk moet u de configuratie aanpassen om de integratie met uw webpagina- of platformarchitectuur te voltooien. </p> <p>Zie <a href="/help/main/c-experiences/c-visual-experience-composer/c-vec-code-editor/experience-templates.md#concept_109BBD7EABC04DD39E6B7B1687786652" format="dita" scope="local"> Experience Templates </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Doelbasis van de webinarreeks </p> </td> 
   <td colname="col2"> <p>Deelnemen aan het nieuwe <a href="/help/main/cmp-resources-and-contact-information.md#concept_11902FAC95C64479AABE020557A7EEE4" format="dita" scope="local"> Doelbasis van de webinarreeks </a>, een Webinar-reeks voor succes van de klant die u van de Gemeenschap hebt ontvangen. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Verbeteringen, correcties en wijzigingen**

Dit [!DNL Target] de release bevat de volgende verbeteringen, oplossingen en wijzigingen:

* De modale grootte van de Rich Text Editor is groter geworden voor betere bruikbaarheid. (TGT-24775)
* De diagrammen in de stap Doel (stap 2 van de driestappenworkflow met instructies) voor de activiteiten Automated Personalization (AP) en Multivariate Test (MVT) zijn opnieuw ontworpen met het oog op meer consistentie met de ontwerpen die worden gebruikt voor de activiteiten A/B, Experience Targeting (XT) en Recommendations. (TGT-30712)
* De metrische waarde voor het MVT-rapport (Multivariate Test Location Contribution) is nu consistenter met de waarden voor andere metriek, die tot twee decimalen wordt afgerond. (TGT-30921)

### at.js versie 1.5.0 (22 juni 2018) {#section_53C622F4978F4BC9ACD932D4B7194C12}

<table id="table_B332A93D4A6E4568BA3F7FA8EC0787F4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Functie/verbetering </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>at.js </p> </td> 
   <td colname="col2"> <p>at.js versie 1.5.0 is nu beschikbaar. </p> <p> <p>Opmerking: De uitgiftenummers tussen haakjes zijn bedoeld voor intern gebruik van Adobe. </p> </p> <p> 
     <ul id="ul_41FE0EED2D8B4ADE84FC4CA0FA0CE8A0"> 
      <li id="li_2DC17381CB7949AFA35B054B9CA723FA"> <p>De details van de <span class="codeph"> op verzoek, opgevolgd </span> -gebeurtenis bevat de omleidingsvlag. Met deze markering kunt u bepalen of de pagina wordt omgeleid naar een andere URL. Als u de URL wilt weten, meldt u zich aan <span class="codeph"> at-content-rendering-redirect </span>. (TNT-29834) </p> </li> 
      <li id="li_2852878862724BB2BD475C8FC7BF20DA"> <p>Probleem verholpen dat ertoe heeft geleid <span class="codeph"> window.targetGlobalSettings.enabled </span> mislukt met een runtime-uitzondering als deze is ingesteld op false. (TNT-29829) </p> </li> 
      <li id="li_96E5E409B36444F1B0E3E2606DC03996"> <p>Probleem verholpen die ertoe leidde dat de pagina mislukte tijdens het laden in Visual Experience Composer (VEC) als het gebruiken van douanecode aan een brand globale mbox verzoek en het gebruiken van lichaam het verbergen. (TNT-29795) </p> </li> 
      <li id="li_818AA4EDDAC04D8B9BB4BA708D6BEF99"> <p>Extra ondersteuning voor <span class="codeph"> screenOrientation </span>, <span class="codeph"> devicePixelRatio </span>, en <span class="codeph"> webGLRenderer </span>. Deze nieuwe parameters van het Verzoek van het Doel worden gebruikt voor iPhone X en andere moderne apparatenopsporing. Zie voor meer informatie <a href="/help/main/c-target/c-audiences/c-target-rules/mobile.md#concept_2A794199DC1A4D349FFFBC7DCF1FEB89" format="dita" scope="local"> Mobiel </a>. (TNT-29781) </p> </li> 
      <li id="li_87E3FB8B423C472AB1EE0DF2D7C64885"> <p>Probleem verholpen waarbij de locatie-hint van de Adobe Audience Manager (AAM) niet altijd werd verzonden. (TNT-29695) </p> </li> 
      <li id="li_E9E5A5035AC24F54ADEF5447E3F15D3B"> <p>Voor browsers die dit ondersteunen, schakelt at.js 1.5.0 over naar MutationObserver voor kiezersopiniepeiling. In versies vóór at.js 1.0.0 werd een MutationObserver-polyfill gebruikt, wat problematisch bleek te zijn. Om de polyfill problemen te voorkomen, gebruikt versie 1.5.0 de volgende pseudo-code om te bepalen welk planningsmechanisme moet worden gebruikt: </p> <p> 
        <code>
          if MutationObserver is supported scheduler = MutationObserver else if document is visible scheduler = requestAnimationFrame else scheduler = setTimeout 
        </code> </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

### Target Standard/Premium 18.6.1 (20 juni 2018) {#section_B63C660815B245DA9922BE33E03734A1}

Deze release bevat de volgende functies en verbeteringen:

>[!NOTE]
>
>De uitgiftenummers tussen haakjes zijn bedoeld voor intern gebruik van Adobe.

<table id="table_5A60FFE5E86148F4BDC6A7031D03D6BA"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Functie/verbetering </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Visual Experience Composer (VEC) </p> </td> 
   <td colname="col2"> <p>Wanneer u in het deelvenster Wijzigingen op een handeling klikt, schuift de VEC automatisch door de webpagina en wordt het bijbehorende element gemarkeerd. U hoeft niet meer handmatig omlaag te schuiven om het HTML-element te zoeken dat door de wijziging is gewijzigd. </p> <p> <img src="assets/modifications_panel.png" id="image_6E01280636E34ADDA9527AD18A34310B" /> </p> <p>(TGT-30441) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Ondersteunde browsers </p> </td> 
   <td colname="col2"> <p>Toegevoegde Microsoft Edge-ondersteuning voor de doelgebruikersinterface en voor het leveren van inhoud. </p> <p>Zie voor meer informatie. <a href="https://developer.adobe.com/target/before-implement/supported-browsers/" format="dita" scope="local"> Ondersteunde browsers </a> (TGT-14102) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p>Recommendations </p> </td> 
   <td colname="col2"> <p>De criteria voor onlangs bekeken objecten geven nu resultaten die specifiek zijn voor een bepaalde <a href="/help/main/administrating-target/hosts.md#concept_516BB01EBFBD4449AB03940D31AEB66E" format="dita" scope="local"> milieu </a>. Als twee sites tot verschillende omgevingen behoren en een bezoeker tussen de twee sites schakelt, worden op elke site alleen recent bekeken items van de desbetreffende site weergegeven. Als twee sites zich in dezelfde omgeving bevinden en een bezoeker schakelt tussen de twee sites, ziet de bezoeker dezelfde onlangs weergegeven items voor beide sites. </p></td> 
  </tr> 
 </tbody> 
</table>

**Verbeteringen, correcties en wijzigingen**

Dit [!DNL Target] de release bevat de volgende verbeteringen, oplossingen en wijzigingen:

* De back-uprij van de CSV-download van Recommendations heeft nu een regelafstand &quot;&#42;&quot; (dubbele aanhalingstekens met een sterretje) in plaats van &#42; (één sterretje).
* De bovenste rij Verkocht / Bovenste bekeken rij in de Recommendations CSV-download heeft niet langer een komma vooraan.

### Wijziging van het Platform (19 juni 2018) {#section_0638BD69F3C640479A2A258AD78C0884}

Deze release bevat de volgende verbeteringen:

>[!NOTE]
>
>De uitgiftenummers tussen haakjes zijn bedoeld voor intern gebruik van Adobe.

* Bijgewerkt de apparatenlijst om de recentste telefoonmodellen te omvatten. De mogelijkheid om gerichte inhoud te leveren aan specifieke iPhone-modellen is toegevoegd met de marketingnaam of het apparaatmodel van het apparaat.

   Klanten die de SDK voor mobiele apparaten gebruiken, hoeven niets te doen om deze functionaliteit te benutten. Klanten die at.js gebruiken, moeten een upgrade uitvoeren naar at.js versie 1.5.0.

   Zie voor meer informatie [Mobiel](/help/main/c-target/c-audiences/c-target-rules/mobile.md#concept_2A794199DC1A4D349FFFBC7DCF1FEB89). (TNT-26714 &amp; TNT-28288)

### Doel-API voor downloaden (5 juni 2018) {#section_B8729DA10F18433C8D8E01B04F308ED2}

U kunt de aanbevelingen downloaden API om uw aanbevelingen in een .CSV dossier te downloaden dat in een spreadsheet of een tekstredacteur kan worden bekeken. Voor verbeterde beveiliging, vanaf **5 juni 2018**, zal Target HTTP-aanvragen blokkeren en alleen HTTPS-aanvragen toestaan.

### Target Standard/Premium 18.5.1 (22 mei 2018) {#section_7C1427793C2A48DBAC39F8290717DC5B}

Deze release bevat de volgende functies en verbeteringen:

>[!NOTE]
>
>De uitgiftenummers tussen haakjes zijn bedoeld voor intern gebruik van Adobe.

<table id="table_1C51F61184684072BC69AD15BA68BEBB"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Functie </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Rapporten </p> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_8D08FE4AC7D748EFB2BBFF87DBDC5CE5"> 
      <li id="li_B8929C19276D42168A28A3775CDEDFB3"> <p>U kunt maximaal tien verschillende voorinstellingen van een activiteitenrapport opslaan nadat u het rapport naar wens hebt geconfigureerd (metriek, publiek, geavanceerde instellingen, enzovoort). Alle gebruikers van het Doel kunnen, de diverse vooraf instelt tonen uitgeven en schrappen, ongeacht wie hen creeerde. (TGT-21268) </p> </li> 
      <li id="li_7ADA62F2ACA049C9B4A8986B09A9F4AA"> <p>U kunt het rapport van een individuele activiteit vormen zoals gewenst en dan die configuratie opslaan als uw gebrek/favoriete voorinstelling. Dit is de mening die toont wanneer u het rapport van die activiteit vooruitgaat. (TGT-10082) </p> </li> 
      <li id="li_DC63C04F3A884BDDA55B5515E4643B7B"> <p>Het alarm en de berichten binnen rapporten laten u weten of één (of meerdere) publiek, metrisch, gastheergroep, of ervaring van een eerder gevormd vooraf ingesteld rapport is geschrapt. Met de waarschuwing of het bericht kunt u een ander publiek, een ander metrisch publiek, een andere hostgroep of een andere ervaring kiezen om opnieuw een voorinstelling te maken. (TGT-29424) </p> </li> 
     </ul> </p> <p>Zie de sectie Voorinstelling doel in <a href="/help/main/c-reports/c-report-settings/report-settings.md#concept_3A80D5A394EC4B639DC715E06085BDB0" format="dita" scope="local"> Rapportinstellingen </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Profielscripts </p> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_F382C8E7708846A08676E1534BC92878"> 
      <li id="li_70E89504525C4119B588C230DCE772E8"> <p>U kunt pop-upkaarten met profielscriptinformatie weergeven, vergelijkbaar met informatiekaarten. Met deze informatiekaarten voor profielscripts kunt u een lijst weergeven met activiteiten die verwijzen naar het geselecteerde profielscript, samen met andere nuttige metagegevens. (TGT-28253) </p> <p>Zie voor meer informatie de sectie View Profile Script Information Cards in <a href="/help/main/c-target/c-visitor-profile/profile-parameters.md#concept_8C07AEAB0A144FECA8B4FEB091AED4D2" format="dita" scope="local"> Profielscriptkenmerken </a>. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Soorten publiek </p> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_DFEB778393024E3EBBC482F31A5B39BC"> 
      <li id="li_4049E334A38F4F94842FF1E35F177FE9"> <p>De verwezenlijking van de Audience van de douane staat nu het gebruiken van de mbox parameter direct toe zonder het moeten verplicht de mbox naam specificeren. De naam van het selectievakje is nu optioneel. Met deze wijziging kunt u parameters uit meerdere vakken gebruiken of verwijzen naar een parameter die nog niet op de rand is opgenomen. U kunt ook op de parameter mbox filteren met het naamfilter van de box. </p> <p>Dezelfde verbetering geldt ook voor Recommendations-criteria, Recommendations-promoties en regels voor het testen van sjablonen. </p> </li> 
     </ul> </p> <p>Zie voor meer informatie <a href="/help/main/c-target/c-audiences/c-target-rules/custom-parameters.md#concept_C4C6E00D7C5A4BE9B72D471DB2E3027B" format="dita" scope="local"> Aangepaste parameters </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p>Recommendations </p> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_7765B69E679D4C94B1E863E340DFDE15"> 
      <li id="li_F2AF7E1AFBD6461990EF1D83D1989582"> <p>Bij het selecteren van Recommendations-criteria in de Form-Based Experience Composer is er nu een directe koppeling naar de geselecteerde Criteria Card zodat u de criteria snel en eenvoudig kunt bewerken. (TGT-28483) </p> <p>Zie voor meer informatie <a href="/help/main/c-experiences/form-experience-composer.md#task_FAC842A6535045B68B4C1AD3E657E56E" format="dita" scope="local"> Formuliergebaseerde Experience Composer </a>. </p> </li> 
      <li id="li_517F0A174587416B8621D6F710C1AC48"> <p>Met Recommendations-criteria, Recommendations-aanbiedingen en regels voor het testen van sjablonen kunt u nu de parameter mbox rechtstreeks gebruiken zonder dat u verplicht de naam van het selectievakje hoeft op te geven. De naam van het selectievakje is nu optioneel. Met deze wijziging kunt u parameters uit meerdere vakken gebruiken of verwijzen naar een parameter die nog niet op de rand is opgenomen. U kunt ook op de parameter mbox filteren met het naamfilter van de box. </p> <p>Deze verbetering is ook uitgebreid tot het creëren van de Audience van de Douane. </p> <p>Zie voor meer informatie <a href="/help/main/c-recommendations/c-recommendations-faq/recommendations-faq.md#concept_EF272DE4AC6C47B19026BFBE816F5DB8" format="dita" scope="local"> Veelgestelde vragen over Recommendations </a>. </p> </li> 
      <li id="li_AAB242830D1E47B78E58A980B717C736"> <p>De gebruikersinterface voor Recommendations Design-kaarten is bijgewerkt. </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

**Verbeteringen, correcties en wijzigingen**

Dit [!DNL Target] de release bevat de volgende verbeteringen, oplossingen en wijzigingen:

* Bijgewerkt UI voor Stap 2 van het Doel driestapel geleide werkschema dat wordt gebruikt om een Test A/B, Ervaring te creëren of uit te geven richt (XT), of activiteit van Recommendations. (TGT-18911)

### Target Standard/Premium 18.4.1 (25 april 2018) {#section_445DBC5402BA456BAF2D24AEA33A91C9}

Deze release bevat de volgende functies en verbeteringen:

>[!NOTE]
>
>De uitgiftenummers tussen haakjes zijn bedoeld voor intern gebruik van Adobe.

<table id="table_6D99C48B72D24728BF623608053931D3"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Functie </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Adobe Experience Manager (AEM) Experience Fragments </p> </td> 
   <td colname="col2"> <p>Door ervaringsfragmenten te gebruiken die zijn gemaakt in AEM in doelactiviteiten kunt u het gebruiksgemak en de kracht van AEM combineren met de krachtige mogelijkheden van Automated Intelligence (AI) en Machine Learning (ML) in Target om ervaringen op schaal te testen en te personaliseren.&amp;nbsp;&amp;nbsp; </p> <p>AEM brengt al uw inhoud en middelen in een centrale plaats samen om uw verpersoonlijkingsstrategie te voeden. Met AEM kunt u eenvoudig inhoud voor desktops, tablets en mobiele apparaten op één locatie maken zonder dat u code hoeft te schrijven. Het is niet nodig om pagina's te maken voor elk apparaat—AEM past automatisch elke ervaring aan met uw inhoud. </p> <p> Met Doel kunt u gepersonaliseerde ervaringen op schaal bieden op basis van een combinatie van op regels gebaseerde en op AI gebaseerde methoden voor het leren van machines die gedrags-, context- en offlinevariabelen bevatten.&amp;nbsp; Met Doel kunt u eenvoudig A/B- en Multivariate-activiteiten instellen en uitvoeren om de beste aanbiedingen, inhoud en ervaringen te bepalen. </p> <p>De fragmenten van de ervaring vertegenwoordigen een enorme stap voorwaarts om de tevreden/ervaringsscheppers en managers aan de optimalisering en verpersoonlijkingsberoeps te verbinden die bedrijfsresultaten gebruikend Doel drijven. </p> <p>Zie voor meer informatie <a href="/help/main/c-experiences/c-manage-content/aem-experience-fragments.md#topic_1E1E4EA01F074349B2CF8785387B5FE8" format="dita" scope="local"> Fragmenten voor AEM </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Rapporten </p> </td> 
   <td colname="col2"> 
    <ul id="ul_EAB90C510EA04D6A8AEFF23A77DB2337"> 
     <li id="li_47DA6EB92CC84FFDBFDC9CC9386AF654"> <p>U kunt een rapport nu verfrissen om de lijst en grafiekmening van het rapport bij te werken zonder de volledige pagina, zijn configuratie, of zijn datumwaaier te verfrissen. (TGT-28125) </p> <p>Zie voor meer informatie <a href="/help/main/c-reports/c-report-settings/report-settings.md#concept_3A80D5A394EC4B639DC715E06085BDB0" format="dita" scope="local"> Rapportinstellingen </a>. </p> </li> 
     <li id="li_AB2DE7A45D914FD7AEB0832187AF3844"> <p>De kalender in rapporten bevat nu vooraf gedefinieerde datumbereiken, zoals Laatste 7 dagen, Laatste 15 dagen enzovoort. (TGT-29171) </p> <p>Zie voor meer informatie <a href="/help/main/c-reports/c-report-settings/report-settings.md#concept_3A80D5A394EC4B639DC715E06085BDB0" format="dita" scope="local"> Rapportinstellingen </a>. </p> </li> 
     <li id="li_46DF9037E0ED4935B3BCDB35E8BED065"> <p>De kolombreedte van de tabelweergave is gewijzigd om horizontaal schuiven te beperken wanneer meerdere maateenheden worden toegepast. (TGT-26575) </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>UI-lokalisatie </p> </td> 
   <td colname="col2"> <p>De doelinterface is nu beschikbaar in de volgende talen: </p> <p> 
     <ul id="ul_DB6C771FCFDF43F498F8754920A70BCD"> 
      <li id="li_A65D07DF66844AC8BEEC1D413F214191"> <p>Vereenvoudigd Chinees </p> </li> 
      <li id="li_5986DD06AF5B4F76B3A02CFBF2DC3644"> <p>Traditioneel Chinees </p> </li> 
      <li id="li_341FDC1CEC2B4C4BBD45CB2A0A54F2A3"> <p>Koreaans </p> </li> 
      <li id="li_A4C31539B98E42348D5F1A18C63EAB6C"> <p>Italiaans </p> </li> 
      <li id="li_97E3E0A916B64601BBF601AAED581174"> <p>Portugees </p> </li> 
     </ul> </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Soorten publiek </p> </td> 
   <td colname="col2"> <p>Wanneer u een aangepast publiek maakt op basis van een mbox-parameter, <span class="codeph"> mboxParameter </span> vraagt u niet meer om <span class="codeph"> mboxName </span>. mbox name is nu optioneel. Met deze wijziging kunt u parameters uit meerdere vakken gebruiken of verwijzen naar een parameter die nog niet op de rand is opgenomen. (TGT-25807) </p> <p> <p>Opmerking: Deze functie is zichtbaar in de doelinterface, maar is momenteel uitgeschakeld. Deze functie wordt binnenkort ingeschakeld (datum waarop moet worden gecommuniceerd). </p> </p> 
  </td> 
  </tr> 
 </tbody> 
</table>

**Verbeteringen, correcties en wijzigingen**

Dit [!DNL Target] de release bevat de volgende verbeteringen, oplossingen en wijzigingen:

* De Veiligheid van de Laag van het vervoer (TLS) is het wijdst opgestelde veiligheidsprotocol dat vandaag voor Webbrowsers en andere toepassingen wordt gebruikt die gegevens vereisen om veilig over een netwerk worden geruild. Adobe beschikt over normen voor beveiligingscompatibiliteit die het einde van de levensduur van oudere protocollen vereisen en die het gebruik van TLS 1.2 verplicht stellen om de meest actuele en veilige versie in gebruik te hebben. Vanaf de doelversie 18.4.1 (25 april 2018) zal Adobe Target stappen ondernemen om de codering van TLS 1.2 te bevorderen en de ondersteuning voor TLS 1.0-codering volledig te beëindigen tegen 12 september 2018. Het is belangrijk dat u de details doorloopt en de wijzigingen uitwerkt voor een vloeiende overgang. Zie voor meer informatie [Wijzigingen in TLS-codering (Transport Layer Security)](https://developer.adobe.com/target/before-implement/tls-transport-layer-security-encryption/){target=_blank}.
* De gebruikersinterface voor Recommendations Criteria Cards is verbeterd en is nu gebruiksvriendelijker. (TGT-27829)

### om.js (3 april 2018) {#section_932DF1004F4648668FE4984BFAF2EC49}

Deze release bevat de volgende functies en verbeteringen:

<table id="table_76576D9D931B4DA99900F2C03175938E"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Functie </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>at.js </p> </td> 
   <td colname="col2"> <p>at.js versie 1.3.0 is nu beschikbaar. Zie voor meer informatie <a href="https://developer.adobe.com/target/implement/client-side/atjs/how-to-deployatjs/implement-target-without-a-tag-manager/" format="dita" scope="local"> Downloaden om.js </a> en <a href="https://developer.adobe.com/target/implement/client-side/atjs/target-atjs-versions/" format="dita" scope="local"> at.js - Versiedetails </a>. </p> <p> 
     <ul id="ul_349BEB37B6C94FF0801F121042037803"> 
      <li id="li_4C2F82F4DD394ED5A0BFF978B15FEDDF"> <p>De volgende nieuwe gebeurtenissen zijn beschikbaar om u te helpen bij het traceren, opsporen van fouten en het aanpassen van interactie met at.js: </p> <p> 
        <ul id="ul_EFF7E2FCEA0D42298779DDE13B54503F"> 
         <li id="li_6A2B06A522004EDE96D9A552571A7C30"> <p>LIBRARY_LOADED </p> </li> 
         <li id="li_61AA203A21DF4B7EAE075374A09C8FF0"> <p>REQUEST_START </p> </li> 
         <li id="li_DAF9CC1E86834C62B93419429B43A2CB"> <p>CONTENT_RENDERING_START </p> </li> 
         <li id="li_A52DC337115248A1BE5AF5B358BE5A9A"> <p>CONTENT_RENDERING_NO_OFFERS </p> </li> 
         <li id="li_7D71E48016B1446995493EBBF7D32447"> <p>CONTENT_RENDERING_REDIRECT </p> </li> 
        </ul> </p> <p>Zie voor meer informatie <a href="https://developer.adobe.com/target/implement/client-side/atjs/atjs-functions/atjs-functions/" format="dita" scope="local"> at.js, aangepaste gebeurtenissen </a>. </p> </li> 
      <li id="li_E2704294F8BA47FFAABE7572F67FB5C0"> <p>U kunt een verzoek at.js met extra parameters uitbreiden die uit gegevensleveranciers komen. Gegevensleveranciers moeten worden toegevoegd aan <span class="codeph"> window.targetGlobalSettings </span> onder de <span class="codeph"> dataProviders-sleutel </span>. </p> <p>Zie "Gegevensleveranciers" in <a href="https://developer.adobe.com/target/implement/client-side/atjs/atjs-functions/atjs-functions/" format="dita" scope="local"> targetGlobalSettings() </a>. </p> </li> 
      <li id="li_02EAFE6DA0D44CF88980184FD14226A5"> <p>bij.js-aanvragen wordt nu GET gebruikt, maar er wordt overgeschakeld naar POST wanneer de URL groter is dan 2048 tekens. Er is een nieuwe eigenschap met de naam <span class="codeph"> urlSizeLimit </span> waar u de maximale grootte indien nodig kunt verhogen. Dankzij deze wijziging kan Target worden uitgelijnd op .js naar AppMeasurement, die dezelfde techniek gebruikt. </p> </li> 
      <li id="li_43363A4F3A764394AA88D2595F93D8C0"> <p>Doel dwingt nu <span class="codeph"> mbox </span> in de <span class="codeph"> adobe.target.applyOffer(opties) </span> wordt gebruikt. Deze sleutel is in het verleden vereist, maar Doel dwingt nu zijn gebruik af om ervoor te zorgen dat Doel juiste bevestiging heeft en klanten correct de functie gebruiken. </p> <p>Zie voor meer informatie <a href="https://developer.adobe.com/target/implement/client-side/atjs/atjs-functions/atjs-functions/" format="dita" scope="local"> adobe.target.applyOffer(opties) </a> . </p> </li> 
      <li id="li_7336D8D48A894291A378E0BB212B7F9B"> <p>at.js heeft de functie voor het bijhouden van gebeurtenissen verbeterd en klikt op tracking. at.js gebruikt <span class="codeph"> navigator.sendBeacon() </span> om gegevens voor het bijhouden van gebeurtenissen te verzenden en wordt teruggevallen naar synchrone XHR wanneer <span class="codeph"> navigator.sendBeacon() </span> wordt niet ondersteund. Deze fallback heeft vooral invloed op Internet Explorer 10 en 11 en op sommige versies van Safari. Safari voegt ondersteuning toe voor <span class="codeph"> navigator.sendBeacon() </span> in de iOS 11.3-release. </p> </li> 
      <li id="li_28D7324137B14C75BF6F1EA0B2487C9B"> <p>Met at.js kunt u nu aanbiedingen renderen, zelfs als een pagina wordt geopend op tabbladen op de achtergrond. Sommige klanten van het Doel ontmoetten een kwestie toen <span class="codeph"> requestAnimationFrame() </span> is uitgeschakeld vanwege het browsergedrag voor achtergrondtabbladen. </p> </li> 
      <li id="li_3278979E1C6C41DEA7E8025AEB337985"> <p>Deze versie voegt vele prestatiesverbeteringen, met inbegrip van kortere callstacks toe wanneer het inspecteren van een profiel van Chrome cpu. </p> </li> 
      <li id="li_AAA9C0DCC3354DFA8907968C8E6427F6"> <p>at.js 1.3.0 biedt geen ondersteuning meer voor de levering van inhoud in Microsoft Internet Explorer 9. Voor een lijst met ondersteunde browsers raadpleegt u <a href="https://developer.adobe.com/target/before-implement/supported-browsers/" format="dita" scope="local"> Ondersteunde browsers </a>. Alle aanvragen worden uitgevoerd via <span class="codeph"> XMLHttpRequest </span> met CORS-ondersteuning zonder JSONP-verzoeken. Deze wijziging verbetert de veiligheid aanzienlijk. </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

### Target Standard/Premium 18.3.1 (20 maart 2018) {#section_880706BE15544A03A2C951F267F4AEC5}

Deze release bevat de volgende functies en verbeteringen:

>[!NOTE]
>
>De uitgiftenummers tussen haakjes zijn bedoeld voor intern gebruik van Adobe.

<table id="table_AE38682151A948AEA21E35A353F18D76"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Functie </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1" class="premium"> <p>Populariteit op kenmerk Entiteit </p> </td> 
   <td colname="col2"> <p><b>Nieuw: 22 maart 2018</b> </p> <p>U kunt nu het kenmerk Populariteit op entiteit in de bestaande stroom kiezen wanneer een kenmerk Aangepast als de sleutel wordt geselecteerd. </p> <p>Na het selecteren van de gewenste sleutel (in dit geval, een attribuut van het douaneprofiel), voor "de Logica van de Aanbeveling,"kunt u twee nieuwe opties kiezen: </p> <p> 
     <ul id="ul_7A6F2398ADE846EF8A7A3110C2736BF7"> 
      <li id="li_66BFF016564749B298B88F6B9638B64E"> <p>Meest bekeken </p> </li> 
      <li id="li_937FE5C40ED8471391B282D1ACE8C133"> <p>Topverkopers </p> </li> 
     </ul> </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Soorten publiek </p> </td> 
   <td colname="col2"> <p>Terwijl het bekijken van de definities pop-up kaart van een publiek (bijvoorbeeld, van de Bibliotheek van de Publiek), kunt u andere activiteiten nu zien die van dat publiek van verwijzingen voorzien, als toepasselijk. Op deze manier kunt u onbedoelde gevolgen voor activiteiten tijdens het bewerken van soorten publiek voorkomen. </p> <p>Eerder, toen u probeerde om een publiek te schrappen dat door activiteiten van verwijzingen werd voorzien, toonde een waarschuwing die u erop deelde dat het publiek niet met maximaal 10 activiteiten kon worden geschrapt die het publiek van verwijzingen voorzien. </p> <p>Zie voor meer informatie <a href="/help/main/c-target/c-audiences/audiences.md#concept_65BE870D290E412D8BBF557EEA67C271" format="dita" scope="local"> Over soorten publiek </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Rapporten </p> </td> 
   <td colname="col2"> <p>Verbeterde de informatie over de lift en de begrenzingen in rapporten om deze uitgebreider en handiger te maken, inclusief knopinfo waarin wordt uitgelegd hoe de grenzen worden berekend. (TGT-28729) </p> <p>Zie voor meer informatie <a href="/help/main/c-reports/statistical-methodology/statistical-calculations.md" format="dita" scope="local"> Gemiddelde optillen, Lift Bounds en het Interval van het Vertrouwen </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p>Automated Personalization (AP) en Auto-Target activiteiten </p> </td> 
   <td colname="col2"> <p>De extra begeleiding is beschikbaar in UI en in Hulp om u te helpen verkeerspercentages in Automated Personalization (AP) en Auto-Target activiteiten effectiever toewijzen. </p> <p>Zie voor meer informatie <a href="/help/main/c-activities/auto-target/auto-target-to-optimize.md" format="dita" scope="local"> Verkeerstoewijzing bepalen </a> en <a href="/help/main/c-activities/t-automated-personalization/create-ap-activity.md#task_8AAF837796D74CF893CA2F88BA1491C9" format="dita" scope="local"> Automated Personalization-activiteiten maken </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p>Recommendations: Opnameregels, verzamelingen en uitsluitingen voor aangepaste criteria </p> </td> 
   <td colname="col2"> <p>U kunt het filtreren in real time bovenop uw eigen output van douanecriteria nu uitvoeren. U kunt bijvoorbeeld de aanbevolen objecten beperken tot objecten van de favoriete rubriek of het favoriete merk van een bezoeker. Dit geeft u de macht om off-line berekeningen met het filtreren in real time te combineren. </p> <p>Met de toevoeging van inclusieregels op de Criteria van de Douane, verandert dit anders statische aanbevelingen in dynamische aanbevelingen gebaseerd op de belangen van een bezoeker. </p> <p> 
     <ul id="ul_BDD55AB34F4A43C691D2399C16AA3D6C"> 
      <li id="li_133C33E0D02E4861A4C855BD8A492E69"> <p>Aangepaste criteria kunnen nu worden geconfigureerd, net als andere criteria in aanbevelingen. </p> </li> 
      <li id="li_AC201F0917BF465C985E8947635F762E"> <p>U kunt inzamelingen, uitsluitingen, en opneming (met inbegrip van de speciale regels voor Prijs en Voorraad) op de zelfde manier gebruiken zoals om het even welke andere criteria. Verzamelingen en uitsluitingen werden al ondersteund. In deze release worden invoegingen toegevoegd. </p> </li> 
     </ul> </p> <p>Zie voor meer informatie <a href="/help/main/c-recommendations/c-algorithms/algorithms.md" format="dita" scope="local"> Criteria </a>. </p> <p>(TGT-28488) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p>Recommendations: Opnameregels, verzamelingen en uitsluitingen voor recent bekeken criteria </p> </td> 
   <td colname="col2"> <p>Onlangs bekeken items kunnen nu worden gefilterd, zodat alleen items met een bepaald kenmerk worden weergegeven. Een multinationaal bedrijf met meerdere bedrijven kan bijvoorbeeld items van de bezoekersweergave over meerdere digitale eigenschappen hebben. In dit geval kunt u de onlangs weergegeven items beperken tot weergave voor de desbetreffende eigenschap waar deze is weergegeven. Hiermee voorkomt u dat onlangs bekeken items worden weergegeven op de site van een andere digitale eigenschap. </p> <p> 
     <ul id="ul_A2D260F01CA047EEA72EF56BD0EE88FA"> 
      <li id="li_DB107DD357B741CCB2B7A4FDAD16F9D6"> <p>De onlangs bekeken Criteria zijn nu configureerbaar, zoals andere criteria in aanbevelingen. </p> </li> 
      <li id="li_85452C03F0924D4C8D854509F1293021"> <p>U kunt inzamelingen, uitsluitingen, en opneming (met inbegrip van de speciale regels voor Prijs en Voorraad) op de zelfde manier gebruiken zoals om het even welke andere criteria. Verzamelingen en uitsluitingen werden al ondersteund. In deze release worden invoegingen toegevoegd. </p> </li> 
     </ul> </p> <p>Zie voor meer informatie <a href="/help/main/c-recommendations/c-algorithms/algorithms.md" format="dita" scope="local"> Criteria </a>. </p> <p>(TGT-22843) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Doelextensie voor starten van Adobe </p> </td> 
   <td colname="col2"> <p>Starten is de volgende generatie mogelijkheden voor tagbeheer van Adobe. De lancering geeft klanten een eenvoudige manier om alle analytische, marketing, en reclame markeringen noodzakelijk om relevante klantenervaringen op te stellen en te beheren. </p> <p>Met de extensie Doel kunt u Doel snel en eenvoudig implementeren in uw omgeving. </p> <p>Zie voor meer informatie <a href="https://developer.adobe.com/target/implement/client-side/atjs/how-to-deployatjs/implement-target-using-adobe-launch/" format="dita" scope="local"> Doel implementeren met Adobe Launch </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Verbeteringen, correcties en wijzigingen**

Dit [!DNL Target] de release bevat de volgende verbeteringen, oplossingen en wijzigingen:

* Wanneer het creëren van of het uitgeven van A/B en Ervaring richtend (XT) activiteiten, behoudt Doel informatie over de laatste geopende ervaring, pagina, of ervaringsversie (via veelvoudige publiekseigenschap) en opent de aangewezen pagina de volgende tijd u het Doel UI opent. (TGT-28225)
* Voor compatibiliteitsdoeleinden zijn beveiligingscorrecties aangebracht.

### Target Standard/Premium 18.2.1 (15 februari 2018) {#section_837CBBB7A89D45D99855A8C5F5E7BFFB}

Deze release bevat de volgende functies en verbeteringen:

<table id="table_1C7A462AE8D4492FA5555F060031F665"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Functie </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>De Adobe Marketing Cloud is gehermerkt en heet nu de Adobe Experience Cloud. </p> </td> 
   <td colname="col2"> <p>De Experience Cloud is een geïntegreerde Adobe van digitale marketingoplossingen. Het is ook een intuïtieve interface waarmee u snel toegang hebt tot uw cloudoplossingen en kernservices. </p> <p>Wijzigingen voor herbranding en gebruikersinterface: Adobe Marketing Cloud is gehermerkt en heet nu de Adobe Experience Cloud. Bovendien zult u veranderingen UI in de interface van het Doel en in de Schakelaar van de Oplossing zien. </p></td> 
  </tr> 
 </tbody> 
</table>

**Verbeteringen, correcties en wijzigingen**

Dit [!DNL Target] de versie omvat sommige achterste-eindverhogingen, moeilijke situaties, en veranderingen.

### Platform van doel (18 januari 2018) {#section_F6A0DC31636D403F92BDB9DCE7A3F6ED}

Deze release bevat de volgende functies en verbeteringen:

<table id="table_0F5BF9370E214302BDFE0AC2D66EC773"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Functie </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>at.js </p> </td> 
   <td colname="col2"> <p>at.js 1.2.3 voegt ondersteuning toe voor JSON-aanbiedingen. JSON-aanbiedingen worden alleen ondersteund in activiteiten die zijn gemaakt met de Form-based Experience Composer. De enige manier om JSON-aanbiedingen te gebruiken is momenteel via directe API-aanroepen. Zie <a href="/help/main/c-experiences/c-manage-content/create-json-offer.md#concept_63C7BEE1F0DB4A7596D997219B7C136D" format="dita" scope="local"> JSON-aanbieding maken </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Overige wijzigingen </p> </td> 
   <td colname="col2"> <p>Uitsluitingsregels, catalogi, regels voor het opnemen van algoritmen en het filteren van runtimeprogramma zijn nu hoofdlettergevoelig. </p> </td> 
  </tr> 
 </tbody> 
</table>

### Target Standard/Premium 18.1.1 (23 januari 2018) {#section_3A2216543B064D6F82EC03E1F8AEC74D}

Deze release bevat de volgende functies en verbeteringen:

>[!NOTE]
>
>De uitgiftenummers tussen haakjes zijn bedoeld voor intern gebruik van Adobe.

<table id="table_872FE2BE61CC4A5CA369D9A6C730686E"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Functie </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Soorten publiek </p> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_42D7C86043C94A7BBA5ED405B2902E3A"> 
      <li id="li_50F2A7D05AB244E18D263A476BD906B3"> <p>U kunt nu tijdkadersoorten maken zonder begin- of einddatum. Hierdoor kunt u hetzelfde publiek in meerdere activiteiten gebruiken (zonder een kopie van het publiek te maken) en tegelijk de begin- en einddatums op activiteitsniveau beheren. Zie <a href="/help/main/c-target/c-audiences/c-target-rules/time-frame.md#concept_0FE1E8DACD104F8B870B0BADE3197F0A" format="dita" scope="local"> Tijdschema </a>. (TGT-25975) </p> </li> 
      <li id="li_6F08D63BC4F040859D51C47C3521C5E1"> <p>De functies Kopiëren en Bewerken zijn alleen beschikbaar voor gebruikers die alleen actief zijn wanneer u de muisaanwijzer op de pagina Publiek kiezen &gt; Alleen activiteit plaatsen boven een publiek. Eerder bestond deze functionaliteit alleen voor bibliotheekpubliek. Zie <a href="/help/main/c-target/creating-activity-only-audience.md#concept_A6BADCF530ED4AE1852E677FEBE68483" format="dita" scope="local"> Een alleen-actief publiek maken </a>. (TGT-27410) </p> </li> 
      <li id="li_A8CF45E6DC37401AA273F7D6CF617524"> <p>Activiteits-slechts publiek over activiteiten kan de zelfde naam hebben. Eerder, zouden de dubbele namen in de toevoeging van tijdstempels resulteren - een dubbel publiek genoemd "Doel op Weekdag"zou als "Doel op Weekdag-1456732099201 worden bewaard." </p> <p>Voor bibliotheekpubliek zijn nog steeds unieke namen vereist. (TGT-17967) </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Rapporten </p> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_C595EEF916494342AD99FF0FDF999927"> 
      <li id="li_8C74478D3480406591DC876F69C19329"> <p>U kunt nu betrouwbaarheidsintervallen voor doorlopende variabelen weergeven. (TGT-22085) </p> </li> 
      <li id="li_21B31F91685C46CAA47688FDE5735312"> <p>Doel geeft nu liftgrenzen weer wanneer dit statistisch significant is in rapporten.(TGT-27301, TGT-27794, en TGT-26387) </p> </li> 
     </ul> </p> <p>Zie <a href="/help/main/c-reports/c-report-settings/report-settings.md#concept_4BB6A7FDAB6F4806A632F9CD989B8BFA" format="dita" scope="local"> Rapportinstellingen </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Aanbiedingen </p> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_BD0C5B260E7E4F139FBC1FBA286C0B81"> 
      <li id="li_FCDBABE6C5034A3596F5BBF024245FB9"> <p>Doel ondersteunt nu het maken van JSON-aanbiedingen in de aanbiedingsbibliotheek voor gebruik in de Form-Based Experience Composer. Zie <a href="/help/main/c-experiences/c-manage-content/create-json-offer.md#concept_63C7BEE1F0DB4A7596D997219B7C136D" format="dita" scope="local"> JSON-aanbieding maken </a>. (TGT-27064) </p> </li> 
      <li id="li_5500AE7DCF4146E88E4619382CE8E836"> <p>U kunt nu de activiteiten bekijken die verwijzen naar een codeaanbieding in de definitie pop-up kaart van elke aanbieding. Deze functionaliteit is niet van toepassing op afbeeldingsaanbiedingen. Zie <a href="/help/main/c-experiences/c-manage-content/manage-content.md#concept_17874A6FCBB743AA84C5988E8571CCF3" format="dita" scope="local"> Aanbiedingen </a>. (TGT-26277) </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p>Recommendations </p> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_63613AD2D744442AA12CD23F4DAC75B4"> 
      <li id="li_4DD5CF06D93A4083BCB34A4FFA293C89"> <p>In de gebruikersinterface wordt nu de status weergegeven van het uploaden van aangepaste algoritmegegevens voor aanbevelingen. Zie <a href="/help/main/c-recommendations/c-algorithms/recommendations-csv.md#task_1BBA49883E794670A09F0ABE1B3F4288" format="dita" scope="local"> Aangepaste criteria uploaden </a>. (TGT-23891) </p> </li> 
      <li id="li_14FCFDD0A0E84B47AF1488DB4DDF197B">De waarde is Aanwezig en de Waarde is niet Huidige exploitanten zijn nu beschikbaar terwijl het creëren van de regels van de algoritmeopneming. Zie <a href="/help/main/c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md#concept_4CB5C0FA705D4E449BD0B37B3D987F9F" format="dita" scope="local"> Dynamische en statische insluitingsregels gebruiken </a>. (TGT-24110) </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Adobe Target Insider nieuwsbrief </p> </td> 
   <td colname="col2"> <p>De Adobe Target Insider is een maandelijkse nieuwsbrief voor leden van de Adobe Target-gemeenschap. Meer informatie over productupdates en toekomstige plannen, tips en trucs voor personalisatie en optimalisatie, successen van klanten, aanstaande gebeurtenissen, whitepapers met informatie, populaire blogberichten en nog veel meer. Lees de <a href="https://theblog.adobe.com/stay-optimized-adobe-target-insider-newsletter/" format="https" scope="external"> aankondiging </a> voor meer informatie. </p> <p> <a href="https://www.adobe.com/subscription/adobe_target_newsletter.html" format="html" scope="external"> Abonneren op de nieuwsbrief </a> om u te helpen de uitzonderlijke klantenervaringen leveren die bedrijfssucces drijven. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Verbeteringen, correcties en wijzigingen**

Dit [!DNL Target] De release bevat de volgende klantgerichte verbeteringen, oplossingen en wijzigingen:

* U kunt nu door de pagina bladeren terwijl u de ervaringen met stap 2 van de driestapige workflow met instructies opnieuw indeelt terwijl u activiteiten maakt. (TGT-27652)
* U kunt met de rechtermuisknop op een activiteit in de Activiteitenlijst klikken om de activiteit op een nieuw tabblad te openen. Klik in Firefox bijvoorbeeld met de rechtermuisknop op de gewenste activiteit > Koppeling openen op nieuw tabblad. (TGT-27409)
* Verbeterde prestaties op de pagina Ontwerpen (Recommendations > Ontwerpen). De weergave- en zoeksnelheid voor ontwerpen is verbeterd. (TGT-21792)
* at.js is nu de standaardimplementatieoptie om te downloaden. (TGT-24676)
* Bij URL-validatie kunt u nu dubbele afbreekstreepjes gebruiken in de URL. Eerder, kon een URL met dubbele koppeltekens niet in Visual Experience Composer (VEC) worden geladen. (TGT-28176)
* Meerdere oplossingen voor de lokalisatie van de gebruikersinterface voor ondersteunde talen.

## Uitzettingen 2017 {#reference_59C7622A111C4147804A8AAC6D27BB8D}

### Doel Platform (8 november 2017) {#section_536B3C0F32ED441C8D82704B94F6AF7E}

Deze release bevat de volgende functies en verbeteringen:

<table id="table_793CDDF1BD9E48BDBABBF6CD979BE186"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Functie </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>at.js </p> </td> 
   <td colname="col2"> <p>at.js versie 1.2.2 is nu beschikbaar. Zie voor meer informatie <a href="https://developer.adobe.com/target/implement/client-side/atjs/how-to-deployatjs/implement-target-without-a-tag-manager/" format="dita" scope="local"> Downloaden om.js </a>. </p> <p> 
     <ul id="ul_3C4C9385A0F3489AA2137A2C88AE93CF"> 
      <li id="li_E658799D930547E6901ACFBF7C541F1F"> <p>Probleem verholpen waarbij een JavaScript-fout werd geretourneerd wanneer de doelbibliotheek in de QUIRKS-modus op een pagina werd geladen. (TNT-28312) </p> </li> 
      <li id="li_050620115ED84CBDA736D94E9AAC6550"> <p>Oplossing een kwestie die Doel veroorzaakte klikken het volgen om de vraag van de gegevensinzameling van de Analyse te breken. (TNT-28261) </p> </li> 
      <li id="li_97BC1B7295364ACDAD3FB07005ED592F"> <p>Probleem verholpen dat ertoe heeft geleid <span class="codeph"> getOffer()-params </span> om te mislukken wanneer <span class="codeph"> targetPageParams() </span> retourneert een lege tekenreeks. (TNT-28359) </p> </li> 
      <li id="li_B542D4A4E37141BA8BE79D416E1B58DB"> <p>Probleem verholpen met genereren van sessie-id bij gebruik van alleen x. (TNT-28361) </p> </li> 
     </ul> </p> <p>De standaardonderbreking voor at.js wordt veranderd van 15 seconden in 5 seconden. </p> <p>Als uw huidige instelling 15 seconden was, wordt deze bijgewerkt naar de nieuwe standaardinstelling van 5 seconden. Als u deze eerder hebt gewijzigd in iets anders, heeft dit geen invloed op de instelling. </p> </td> 
  </tr>  
 </tbody> 
</table>

### Target Standard/Premium 17.11.1 (8 november 2017) {#section_324A9B1DA0B14F5999FEE41F15B13A44}

Deze release bevat de volgende functies en verbeteringen (nummer van de uitgave tussen haakjes is bestemd voor intern gebruik van Adobe):

<table id="table_6ADDF3552AD04666B76F2D3F457BB042"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Functie </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Aanbiedingen </p> </td> 
   <td colname="col2"> <p> Als een gebruiker de toestemming van de "Redacteur"heeft, kan die gebruiker geen aanbieding uitgeven die aan een levende of geplande activiteit van verwijzingen wordt voorzien. </p> <p> <p>Opmerking: Voor Target Premium-klanten die <a href="https://experienceleague.adobe.com/docs/target/using/administer/manage-users/enterprise/property-channel.html" format="html" scope="external"> Machtigingen voor zakelijke gebruikers </a>Als een gebruiker de optie Alle werkruimten selecteert, gebruikt Doel de hoogste toestemming van de gebruiker over werkruimten. Als de hoogste toestemming "Redacteur is,"Doel beperkt het uitgeven zoals hierboven vermeld </p>. </p> <p>Deze beperkingen gelden voor alle aanbiedingen, niet alleen voor aanbiedingen die zijn gemaakt met Target. (TGT-27276) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Reactietokens </p> </td> 
   <td colname="col2"> <p>De volgende ingebouwde parameters zijn toegevoegd: </p> <p> 
     <ul id="ul_17AD5B9788514E9DB14ED435A4224BFE"> 
      <li id="li_334F10A5B7934215B4D37278901BAF96"> <p>profile.tntId </p> </li> 
      <li id="li_AA9B4611035344549CC933FFC499289F"> <p>profile.marketingCloudVisitorId </p> </li> 
      <li id="li_DD751027371D4293BF9DB872278BD1B3"> <p>profile.thirdPartyId </p> </li> 
      <li id="li_B6D983A1B68D49AAA40CB401437676F1"> <p>profile.categoryAffinity </p> </li> 
      <li id="li_F5E86BFD14CA4C198F36F3F9987750F9"> <p>profile.categoryAffinities </p> </li> 
     </ul> </p> <p>Zie voor meer informatie <a href="/help/main/administrating-target/response-tokens.md#concept_2B21B222F6A344D68CA5929817E836C4" format="dita" scope="local"> Reactiepunten </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

### Target Standard/Premium 17.10.1 (25 oktober 2017) {#section_EF74751744024C209A02F45322642D37}

Deze release bevat de volgende functies en verbeteringen (nummer van de uitgave tussen haakjes is bestemd voor intern gebruik van Adobe):

<table id="table_307DF0CD143048BC9E419444C556B8FB"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Functie </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Soorten publiek </p> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_6E91AEC68A6E45D8B2907C77E752FEC6"> 
      <li id="li_A5778B528358433DB31D700D8F9BCB79"> <p>U kunt een alleen-activiteit publiek maken vanuit de driestappenworkflow met instructies bij het maken van een activiteit. Dit publiek kan op andere plaatsen binnen de zelfde activiteit worden gebruikt, maar wordt niet opgeslagen in de Bibliotheek van Soorten publiek voor gebruik in andere activiteiten. (TGT-25474) </p> <p> <img src="assets/adhoc_audience.png" id="image_32C7C8B72F51425595A2E266AEFA17E9" /> </p> <p>Zie voor meer informatie <a href="/help/main/c-target/creating-activity-only-audience.md#concept_A6BADCF530ED4AE1852E677FEBE68483" format="dita" scope="local"> Een alleen-actief publiek maken </a>. </p> </li> 
      <li id="li_691812682A5B42C0941324F2BC7D5740"> <p>Voor alle activiteiten, kunt u een succesmetrisch kiezen die de gebruiker voor het publiek kwalificeert. In het verleden, kwalificeerde het Doel gebruikers voor een publiek toen zij de activiteit inging, terwijl nu u kunt kiezen wanneer om het publiek te evalueren door een succes metrisch te kiezen. (TGT-15805) </p> <p> <img src="assets/success_metric.png" id="image_0CEC6015A2C4429790A063FE54CC1A35" /> </p> </li> 
     </ul> </p> <p>Zie voor meer informatie <a href="/help/main/c-target/apply-reporting-audience-success-metric.md#concept_5F11149ACCA84FE79C7B9F766B6B0595" format="dita" scope="local"> Pas een Publiek van de Rapportering op Metrisch Succes toe </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p>Automatisch doel </p> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_6F89BD36373E47C4B3A6F8584D431D82"> 
      <li id="li_5F7B590AF8F24066ADD270E9F75CB12F"> <p>Auto-Target activiteiten steunen nu segment-vlakke rapportering. (TGT-22777) </p> <p>Zie voor meer informatie <a href="/help/main/c-activities/auto-target/auto-target-to-optimize.md" format="dita" scope="local"> Auto-Target voor persoonlijke ervaringen </a>. </p> </li> 
      <li id="li_35042E7D6BB04265B42F08A23A774E92"> <p>U kunt het percentage van de Controle voor Auto-Doelactiviteiten veranderen. (TGT-26467) </p> <p> <img src="assets/auto-target-control-small.png" id="image_81F6F61DB61240C289FB71362851AA53" /> </p> <p>Zie voor meer informatie <a href="/help/main/c-activities/auto-target/auto-target-to-optimize.md" format="dita" scope="local"> Auto-Target voor persoonlijke ervaringen </a>. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Aanbiedingen </p> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_667DDEDDC5284C8393F8BCA5CD9EF12A"> 
      <li id="li_E00DB93297EC4100B46E42D867757DAA"> <p>U kunt nu definitiedetails van voorstellen op een pop-up kaart in de Bibliotheek van Aanbiedingen bekijken zonder de aanbieding te openen. (TGT-26377) </p> <p> <img src="assets/offer-card.png" id="image_1980AE8E9BED424085CC482C773C20EC" /> </p> <p>Zie voor meer informatie <a href="/help/main/c-experiences/c-manage-content/manage-content.md#concept_17874A6FCBB743AA84C5988E8571CCF3" format="dita" scope="local"> Aanbiedingen </a>. </p> </li> 
      <li id="li_F71AC4FDAC0E4BEE81D39490E82686C0"> <p>U kunt aanbiedingen en mappen in de keuzelijst Aanbieding kopiëren en bewerken terwijl u een activiteit maakt. (TGT-26936) </p> <p> <img src="assets/offer-picker.png" id="image_1077A6C7A8DD40FB9370CB55BD7260E5" /> </p> <p>Zie voor meer informatie <a href="/help/main/c-experiences/c-manage-content/manage-content.md#concept_17874A6FCBB743AA84C5988E8571CCF3" format="dita" scope="local"> Aanbiedingen </a>. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Form-based Experience Composer </p> </td> 
   <td colname="col2"> <p>In de Form-based Experience Composer zijn Refinements vervangen door volledige publieksfunctionaliteit. De verfijningen voor bestaande activiteiten zijn gemigreerd naar alleen-activiteiten-publiek. (TGT-13646) </p> <p>Zie voor meer informatie <a href="/help/main/c-experiences/form-experience-composer.md#task_FAC842A6535045B68B4C1AD3E657E56E" format="dita" scope="local"> Formuliergebaseerde Experience Composer </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Reactiepunten </p> </td> 
   <td colname="col2"> <p>U kunt nu responstokens maken van Target zonder te wachten tot deze zijn gemaakt in of geïmporteerd naar Target. Eerder, in de Symbolische UI van de Token van de Reactie, kon u slechts de tokens zien die via API werden gecreeerd. Als u de functie wijzigt, voorkomt u ook duplicaten van reactietokens. (TGT-26534) </p> <p>Zie voor meer informatie <a href="/help/main/administrating-target/response-tokens.md#concept_2B21B222F6A344D68CA5929817E836C4" format="dita" scope="local"> Reactiepunten </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Verbeteringen, correcties en wijzigingen**

Dit [!DNL Target] De release bevat de volgende klantgerichte verbeteringen, oplossingen en wijzigingen:

* U kunt geïmporteerde soorten publiek verwijderen (Klassiek doel, Experience Cloud, enz.) uit de Audience Library. Het doel waarschuwt u als u probeert om een publiek te schrappen dat voor een actieve activiteit wordt gebruikt. (TGT-25171)
* Uit Target Classic geïmporteerde soorten publiek worden nu als Adobe Target Classic gelabeld in de Audience Library. In het verleden maakte de interface geen onderscheid tussen Target Standard/Premium en Target Classic. (TGT-27093)
* Verzamelingen gelden nu voor alle criteria (inclusief onlangs bekeken objecten). (TGT-26646)
* U kunt filteren op Workspace in de Audience Library and Offer Library (van toepassing op Target Premium-gebruikers met Enterprise-gebruikersmachtigingen). (TGT-26813)
* Verbeterde gebruikersinterface voor rapporten voor beter schuiven in tabellen en plaatsen van vervolgkeuzelijsten met filters. (TGT-23713 &amp; TGT-26819)

### Wijziging van streefcijfers voor Platforms (13 oktober 2017) {#section_6C298C5C3D01415CB4B658EB2166096C}

<table id="table_8457FAE3508F454F9DFDEF093FBD7E40"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Wijzigen </th> 
   <th colname="col2" class="entry"> Details </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="filepath"> at.js </span> </p> </td> 
   <td colname="col2"> <p><b>13 oktober 2017</b> </p> <p> <span class="filepath"> at.js </span> versie 1.2.1 is nu beschikbaar. Zie voor meer informatie <a href="https://developer.adobe.com/target/implement/client-side/atjs/target-atjs-versions/" format="dita" scope="local"> at.js - Versiedetails </a>. </p> <p> 
     <ul id="ul_14D6BB3B51974789BBFC036A45B7A56B"> 
      <li id="li_AE9826C8FC4A4DF4BE61BB72C2946C93"> <p>Probleem verholpen wanneer op een koppeling met target="_blank" werd geklikt, zodat Target de koppeling niet op een nieuw tabblad kon openen. </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

### Target Standard/Premium 17.9.1 (25 september 2017 en 12 oktober 2017) {#section_ECC5DD8B6ED443788B46F53E25FC896E}

Deze release bevat de volgende functies en verbeteringen (nummer van de uitgave tussen haakjes is bestemd voor intern gebruik van Adobe):

<table id="table_0A8817F64F434875A485FD671C6988AB"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Functie </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> Voorvertoning van mobiele beleving </p> </td> 
   <td colname="col2"> <p><b>Bijgewerkt: 12 oktober 2017</b> </p> <p> U kunt nu meerdere activiteiten voor mobiele apps selecteren in de gebruikersinterface en deze voorvertonen op uw apparaat. Met deze functie kunt u zich inschrijven voor meerdere ervaringen voor voorvertonen en QA zonder te hoeven vertrouwen op speciale testbuilds en simulators. </p> <p>Deze functie vereist dat u de juiste versie 4.14 (of hoger) van de Adobe Mobile SDK downloadt en installeert. </p> <p>Zie voor meer informatie <a href="https://developer.adobe.com/target/implement/mobile/target-mobile-preview/" format="dita" scope="local"> Doel: mobiele voorvertoning </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Mobiele batchverwerking en Prefetch-levering </p> </td> 
   <td colname="col2"> <p><b>Bijgewerkt: 12 oktober 2017</b> </p> <p> De inhoud voor veelvoudige dozen kan in één enkele vraag worden pre-opgehaald en plaatselijk in het voorgeheugen ondergebracht op het apparaat zonder zich het ongerust maken hoe, wanneer, en als de eindgebruiker de inhoud zal zien. </p> <p>Deze functie vereist dat u de juiste versie 4.14 (of hoger) van de Adobe Mobile SDK downloadt en installeert. </p> <p>Zie voor meer informatie <a href="https://developer.adobe.com/target/implement/mobile/prefetch-offer-content/" format="dita" scope="local"> Inhoud van voorkeursaanbieding </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Activiteiten </p> </td> 
   <td colname="col2"> <p>De volgende verbeteringen zijn doorgevoerd in de workflow voor het maken van activiteiten: </p> <p> 
     <ul id="ul_2D251AC11FC54E86AE84DEFFB6FDF43C"> 
      <li id="li_AB8F12B3CF654120BD16EAE570517741"> <p>Tijdens het bewerken van een activiteit kunt u de gewenste wijzigingen aanbrengen in de momenteel weergegeven stap, klikken op de vervolgkeuzelijst op de splitsknop en vervolgens <span class="wintitle"> Volgende </span> om naar de volgende stap te gaan, klikt u op <span class="wintitle"> Opslaan en sluiten </span> om uw wijzigingen op te slaan en de activiteiten weer te geven <span class="wintitle"> Overzicht </span> pagina, of klik <span class="wintitle"> Opslaan </span> om uw wijzigingen op te slaan en op die stap te blijven. </p> <p> <img src="assets/edit_split_button_2.png" id="image_ABC7EE42F5D341EC88AACC54CA98DA2F" /> </p> <p>Zie voor meer informatie <a href="/help/main/c-activities/edit-activity.md#concept_BB064C0D4A194BD1A1AE7CCA1E6BB8F0" format="dita" scope="local"> Een activiteit bewerken of Opslaan als concept </a>. </p> </li> 
      <li id="li_4C71E2570ECF4BBAB08443D89230CE82"> <p>Tijdens het bewerken van een activiteit kunt u de gewenste workflowstap openen, wijzigingen aanbrengen (bijvoorbeeld percentages, soorten publiek enzovoort) en de activiteit vervolgens opslaan of sluiten zonder de driestappenworkflow met instructies te doorlopen. </p> <p> <img src="assets/edit_activity.png" id="image_0B9A2EF729C34A1D9FA84B8B7B17A3C1" /> </p> <p>Zie voor meer informatie <a href="/help/main/c-activities/edit-activity.md#concept_BB064C0D4A194BD1A1AE7CCA1E6BB8F0" format="dita" scope="local"> Een activiteit bewerken of Opslaan als concept </a>. </p> </li> 
      <li id="li_43C15B13E4F7475E9376A98222AA0253"> <p>Wanneer u een nieuwe activiteit creeert die nog niet is opgeslagen, of u een activiteit uitgeeft die eerder in ontwerp vorm werd opgeslagen, <span class="wintitle"> Concept opslaan </span> worden weergegeven in de knop Splitsen. </p> <p> <img src="assets/save_draft.png" id="image_3975786947CE4E39B900AA81D838B9B3" /> </p> <p>Zie voor meer informatie <a href="/help/main/c-activities/edit-activity.md#concept_BB064C0D4A194BD1A1AE7CCA1E6BB8F0" format="dita" scope="local"> Een activiteit bewerken of Opslaan als concept </a>. </p> </li> 
      <li id="li_36EF9AD13B2D40ADB99343C9F758D5FD"> <p>U kunt een publiek nu bewerken of kopiëren door de muisaanwijzer boven het gewenste publiek in het deelvenster <span class="wintitle"> Publiek kiezen </span> tijdens het kiezen van een doelversie in stap 2 van de driestappenworkflow met instructies. </p> <p> <img src="assets/audience_picker_hover.png" id="image_6DC33A0856A346948E517F0BA4C9039F" /> </p> </li> 
     </ul> </p> <p>Zie voor meer informatie <a href="/help/main/c-activities/t-test-ab/t-test-create-ab/ab-audience.md#concept_A268236C1224451DB7844BF67F41A087" format="dita" scope="local"> Publiek selecteren </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Rapportage </p> </td> 
   <td colname="col2"> <p>De volgende nieuwe functies en verbeteringen zijn beschikbaar voor rapportage: </p> <p> 
     <ul id="ul_2D1AF91D1B4E478FBFFA0B83EE30075E"> 
      <li id="li_98E67A4DA8BF4CFF90C279FAC12F4C54"> <p>U kunt de telmethode voor grafieken kiezen in rapporten. Dit wordt niet ondersteund in Auto-Target- en Automated Personalization (AP)-activiteiten. </p> <p>Zie de rij "Methodologie tellen" in <a href="/help/main/c-reports/c-report-settings/report-settings.md#concept_4BB6A7FDAB6F4806A632F9CD989B8BFA" format="dita" scope="local"> Rapportinstellingen </a>. </p> </li> 
      <li id="li_5803CE90DB764C9E983702CB6C1AFEE3"> <p>U kunt veelvoudige metriek in één enkel rapport voor auto-Doel A/B activiteiten bekijken. (TGT-23464) </p> <p>Zie voor meer informatie <a href="/help/main/c-reports/c-report-settings/view-multiple-metrics.md#concept_9E3C3F6F3EC1412FAF252975AC0720B7" format="dita" scope="local"> Meerdere metriek weergeven in een rapport </a>. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Soorten publiek </p> </td> 
   <td colname="col2"> <p>U kunt nu de definities bekijken van publiek dat is geïmporteerd uit Target Classic of gemaakt via API. (TGT-22630) </p> <p> <img src="assets/imported_mobile_audience_rn.png" id="image_6ED9EA63FD7D440286DBAFDBD696BA64" /> </p> <p>Voor meer informatie, zie "het Bekijken Definities van het Publiek"in <a href="/help/main/c-target/c-audiences/audiences.md#concept_65BE870D290E412D8BBF557EEA67C271" format="dita" scope="local"> Over soorten publiek </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Code-editor </p> </td> 
   <td colname="col2"> <p>De op vorm-gebaseerde Composer van de Ervaring en de HTML biedt redacteur nu de zelfde coderedacteur aan die Visual Experience Composer (VEC) in douanecode gebruikt. (TGT-25808) </p> <p>Deze verbetering geeft u de volgende eigenschappen wanneer het gebruiken van de code redacteur in de Op vorm-gebaseerde Composer van de Ervaring en wanneer het creëren van HTML aanbiedingen: </p> <p> 
     <ul id="ul_CBB17806FBF34774A8160A61204ED014"> 
      <li id="li_22665F583F1742E280D5BC7EC4203007"> <p>Regelnummers zijn nu zichtbaar voor betere bruikbaarheid. </p> </li> 
      <li id="li_B0D863CDAD2E46A4B133BB86886EB527"> <p>Met syntaxismarkering voorkomt u onjuiste syntaxis voor HTML-aanbiedingen. </p> </li> 
     </ul> </p> <p>Zie voor meer informatie <a href="/help/main/c-experiences/c-visual-experience-composer/c-vec-code-editor/vec-code-editor.md#concept_B3A6E9EE3A60406DB640E205EA1745B5" format="dita" scope="local"> Code-editor </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Geo gericht </p> </td> 
   <td colname="col2"> <p>U kunt breedte- en lengtegraad nu gebruiken voor geo-doelen. (TGT-12129) </p> <p>Zie voor meer informatie <a href="/help/main/c-target/c-audiences/c-target-rules/geo.md#concept_5B4D99DE685348FB877929EE0F942670" format="dita" scope="local"> Geo </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Node.JS SDK </p> </td> 
   <td colname="col2"> <p>U kunt de SDK van node.js installeren vanuit <a href="https://www.npmjs.com/package/@adobe/target-node-client" format="https" scope="external"> npm @adobe/target-node-client </a> om server-zijtests op uw node.js toepassingen gemakkelijk uit te voeren en in werking te stellen. De service VisitorID is ingeschakeld in het knooppunt-SDK om al uw Adobe-gegevens te verbinden en u kunt Adobe Analytics gebruiken als uw rapportbron (A4T). </p> </td> 
  </tr> 
 </tbody> 
</table>

**Verbeteringen, correcties en wijzigingen**

Dit [!DNL Target] release bevat de volgende klantgerichte verbeteringen, oplossingen en wijzigingen (nummer van de uitgave tussen haakjes is voor intern gebruik van Adobe):

* Gebruikers met de machtiging fiatteur kunnen nu tokens voor API-profielverificatie genereren en inschakelen. (TGT-24074)

   Zie voor meer informatie [Profiel-API-instellingen](https://developer.adobe.com/target/before-implement/methods-to-get-data-into-target/profile-api-settings/){target=_blank}.

* Wanneer het creëren van een activiteit in de Visuele Composer van de Ervaring en de gebruiker herlaadt de pagina, worden de activiteit URL en bijbehorende eigenschappen behouden in UI. De noodzaak om opnieuw te laden kan voorkomen als de activiteit gemengde inhoud (veilige en onveilige inhoud) gebruikt of er toestemmingskwesties zijn. (TGT-28230)
* Verbeterde berichten wanneer een activiteit gemengde inhoud (veilige en onveilige inhoud) gebruikt. Het bericht bevat informatie waarmee gebruikers de benodigde stappen kunnen uitvoeren die nodig zijn om een HTTP-site of een site met gemengde aanroepen (HTTPS en HTTP) te openen. (TGT-26271)

Zie voor meer informatie [Gemengde inhoud in uw browser inschakelen](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/mixed-content.md#concept_46D022D50280468C9EF6D5DF6EFC911C).

* De workflow is verbeterd wanneer de doelsessietijden van een gebruiker zijn verstreken tijdens het configureren van opties op de pagina&#39;s Beheer, Soorten publiek en Recommendations. Wanneer de gebruiker op Opslaan klikt, wordt het bericht dat de sessie is verlopen weergegeven, maar na het aanmelden, wordt de gebruiker in een dialoogvenster op de hoogte gebracht van een geslaagde aanmelding en blijft de gebruikersinterface op dezelfde pagina in Target staan zonder gegevensverlies. (TGT-2557)

### Wijzigingen in Platform (27 september 2017) {#section_AC32516DFBA64AD2AC9A74171D452778}

<table id="table_701D8D53D1DF4F28ADAC6EC221B0208A"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Wijzigen </th> 
   <th colname="col2" class="entry"> Details </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="filepath"> at.js </span> </p> </td> 
   <td colname="col2"> <p><b>27 september 2017</b> </p> <p> <span class="filepath"> at.js </span> versie 1.2.0 is nu beschikbaar als een onderhoudsversie die meestal foutoplossingen bevat. Zie voor meer informatie <a href="https://developer.adobe.com/target/implement/client-side/atjs/target-atjs-versions/" format="dita" scope="local"> at.js - Versiedetails </a>. </p> <p> 
     <ul id="ul_D11024549C3643C7A756988087498D24"> 
      <li id="li_E1B3994125B64F6AB20B29FE8BCD8459"> <p>Probleem verholpen waarbij standaardhandelingen voor speciale gevallen met klikken werden voorkomen. (TNT-28089) </p> </li> 
      <li id="li_53806C902AA04B31B59AA87A1E707348"> <p>Probleem verholpen waarbij klikken op bijhouden in een koppeling met <span class="codeph"> target="_blank" </span> die ervoor zorgden dat Target de koppeling niet op een nieuw tabblad kon openen. (TNT-28072) </p> </li> 
      <li id="li_94F5794330D14C71BA07B3F17D0705FD"> <p> IP de adressen kunnen als koekjesdomein worden gebruikt. (TNT-28002) </p> </li> 
      <li id="li_7D2A11B17672419583F9632CDA00D28F"> <p>Probleem verholpen dat flikkering veroorzaakte bij omleidingsvoorstellen met een global mbox of andere regionale dozen. (TNT-27978) </p> </li> 
      <li id="li_BA27A749A7A242478080F3D8E04148FC"> <p> Probleem verholpen in Experience Targeting activity setup mislukt binnen de VEC bij het schakelen tussen Bladeren en Samenstellen. (TNT-27942) </p> </li> 
      <li id="li_FA11ABA5B9CD435080426805C5359A51"> <p> Probleem verholpen met onjuiste afhandeling van flikkerstijlklassen voor kliktrackelementen. (TNT-27896) </p> </li> 
      <li id="li_E2DFBAE52FCA4996BA083868CBFCCD10"> <p>Probleem verholpen waarbij algemene mbox-parameters werden gemengd met alle mbox-parameters. (TNT-27846) </p> </li> 
      <li id="li_B3153BBD66AA4D51AE81EF6C903CF78D"> <p>Wijzigingen aangebracht om ervoor te zorgen dat Handlebars, Mustache en andere sjabloonbibliotheken aan de clientzijde correct worden verwerkt door <span class="filepath"> at.js </span>. (TNT-27831) </p> </li> 
      <li id="li_B859939C1B5A4DF78CF8ADF236B88306"> <p>Wijzigingen aangebracht om ervoor te zorgen dat <span class="codeph"> sdidParamExpiry </span> wordt op de juiste wijze geïnitialiseerd en doorgegeven aan de Bezoeker-API. Deze regressie is toegevoegd aan <span class="codeph"> om.js 1.1.0 </span>. Vorige <span class="filepath"> at.js </span> Dit heeft geen invloed op versies. Dit is alleen van invloed op clients die omleidingsaanbiedingen en A4T gebruiken. (TNT-27791) </p> </li> 
      <li id="li_24A748DFB7824AE6AC7331B7EA940BFF"> <p>Wijzigingen aangebracht om ervoor te zorgen dat <span class="codeph"> SCRIPT </span> wordt uitgevoerd ongeacht het type-kenmerk dat wordt gebruikt. (TNT-27865) </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Gericht op ervaring (XT) </p> </td> 
   <td colname="col2"> <p><b>21 september 2017</b> </p> <p>Met de release op 21 september wijzigt Target de manier waarop gebruikers worden geplaatst in Experience Targeting (XT)-activiteiten (Landing Page campagnes in Target Classic). Voor alle nieuwe en bestaande activiteiten in zowel Target Standard/Premium als Target Classic, moeten gebruikers de ervaring naleven die op regels gericht is op elke indruk om de inhoud van de ervaring te blijven zien en in rapporten te worden geteld. Eerder, als de gebruiker niet meer gekwalificeerd voor om het even welke ervaring was, zou de gebruiker de inhoud van blijven zien en in rapporten voor, de laatste ervaring worden geteld die zij kwalificeerden. </p> <p>Deze wijziging wordt automatisch doorgevoerd als onderdeel van de release voor alle bestaande activiteiten en voor alle nieuwe activiteiten die na de release worden gemaakt. Als de vorige methode (van vóór 21 september) gewenst is, kunt u publiek tot stand brengen gebruikend profielmanuscripten zodat een gebruiker slechts aan een voorwaarde moet voldoen één keer om in dat publiek in de toekomst te blijven vallen. Gebruik vervolgens die soorten publiek voor elke ervaring in de activiteit. </p> </td> 
  </tr> 
 </tbody> 
</table>

### Target Standard/Premium 17.8.1 (22 augustus 2017) {#section_71A554D072F04B18B359C1626529E5D8}

<table id="table_AAC16F89060D4CC09762A370B86C0885"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Functie </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1" class="premium"> <p>Gebruikersmachtigingen voor doelversie </p> </td> 
   <td colname="col2"> <p>Maak afzonderlijke werkruimten in Doel en wijs gebruikers verschillende rollen en machtigingen toe voor afzonderlijke digitale eigenschappen. </p> <p>Zie voor meer informatie <a href="/help/main/administrating-target/c-user-management/property-channel/property-channel.md#concept_E396B16FA2024ADBA27BC056138F9838" format="dita" scope="local"> Machtigingen voor zakelijke gebruikers </a>. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>QA-modus </p> </td> 
   <td colname="col2"> <p>Voer gemakkelijke activiteit QA met voorproefverbindingen uit die nooit veranderen, facultatieve publiek richten, en QA rapportering die van levende activiteitengegevens gesegmenteerd blijft. </p> <p>Zie voor meer informatie <a href="/help/main/c-activities/c-activity-qa/activity-qa.md" format="dita" scope="local"> Activiteit QA </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Verbeteringen, correcties en wijzigingen**

Dit [!DNL Target] De release bevat de volgende klantgerichte verbeteringen, oplossingen en wijzigingen: (nummer van de uitgave staat tussen haakjes voor intern gebruik van Adobe):

* We hebben meer plaatsen toegevoegd waar u de details van de publieksdefinitie op een pop-up kaart in het Doel UI kunt bekijken zonder het publiek te openen. Deze functionaliteit is alleen van toepassing op publiek dat is gemaakt in [!DNL Target Standard/Premium. (TGT-25772)]
* U kunt nu definities van ad-hocpubliek weergeven in het maken/overzicht van activiteiten. (TGT-25570)
* De volgende variabelen zijn nu beschikbaar als [Snelheid](/help/main/c-recommendations/c-design-overview/customizing-a-template.md#concept_94F1554C3F2E4CDB9A2C3D78F10EDA59) arrays: `entiites` en `entityN.categoriesList`.

### Wijzigingen in Platform (3 augustus 2017) {#section_FA5BF6808EA74F3A9E8E941530879208}

<table id="table_1B43199F1AE64E69AE65313B23741444"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Wijzigen </th> 
   <th colname="col2" class="entry"> Details </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="filepath"> at.js </span> </p> </td> 
   <td colname="col2"> <p><b>3 augustus 2017</b> </p> <p> <span class="filepath"> at.js </span> versie 1.1 is nu beschikbaar. Zie voor meer informatie <a href="https://developer.adobe.com/target/implement/client-side/atjs/how-to-deployatjs/implement-target-without-a-tag-manager/" format="dita" scope="local"> Downloaden om.js </a>. </p> <p>De volgende verbeteringen en correcties zijn opgenomen in <span class="filepath"> at.js </span> versie 1.1: </p> <p> 
     <ul id="ul_B7408267413347888938E2E7D48ABDBD"> 
      <li id="li_4DDF6DCFE6014C6795B6A9C9DFB54C21"> <p>Toegevoegde verwerking van responstoken. Zie voor meer informatie <a href="/help/main/administrating-target/response-tokens.md#concept_2B21B222F6A344D68CA5929817E836C4" format="dita" scope="local"> Reactiepunten </a>. </p> </li> 
      <li id="li_741CD22B7D074FBA90180B2E36FACE0D"> <p>Het probleem is opgelost zodat <span class="codeph"> document.currentScript, polyfill </span> interfereert niet met Angular 1.X. </p> </li> 
      <li id="li_EF1B3D3DCC7F4D2490D2BFE660EC661C"> <p>Wijzigingen aangebracht om ervoor te zorgen dat het bijhouden van klikken geen invloed heeft op de zichtbaarheidseigenschap. Klik op de volgende elementen om de <span class="codeph"> at-element-klik-tracking </span> CSS-klasse in plaats van <span class="codeph"> at-element-marker </span>. </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

### Target Standard/Premium 17.7.3 (3 augustus 2017) {#section_D90CB766679442C7A0642E5D79657674}

<table id="table_C81EA97B251547169BC9681E5DDB4B8F"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Functie </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Reactiepunten </p> </td> 
   <td colname="col2"> <p>Met responstokens kunt u automatisch in aanmerking komende variabelen (bijvoorbeeld profielkenmerken) uitvoeren in de doelreacties die activiteiten leveren (bijvoorbeeld weergavekaders). De tokens van de reactie kunnen voor het zuiveren doeleinden of voor integratie met derdeleveranciers (zoals Clicktale) worden gebruikt. </p> <p>Reactietokens lijken op <span class="keyword"> Adobe Target Classic </span> serverplug-ins en bieden pariteit tussen de twee oplossingen. </p> <p> <p>Opmerking: Responstokens zijn beschikbaar voor <span class="filepath"> at.js </span> 1.1 of hoger.</span>. </p> </p> <p>Zie voor meer informatie <a href="/help/main/administrating-target/response-tokens.md#concept_2B21B222F6A344D68CA5929817E836C4" format="dita" scope="local"> Reactiepunten </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

### Target Standard/Premium 17.7.2 (27 juli 2017) {#section_6980EC04D3CF4A00919953B9B10BC472}

<table id="table_DB51BD66756F4EBD875ED008B2C7C5D0"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Functie </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1" class="premium"> <p>Automatisch doel </p> </td> 
   <td colname="col2"> <p>Auto-Target nu beschikbaar aan alle klanten van de Premium van het Doel. </p> <p>Auto-Target maakt gebruik van geavanceerd leren van machines om meerdere ervaren die door markters worden gedefinieerd, te identificeren en biedt elke bezoeker de meest op maat gemaakte ervaring op basis van zijn individuele klantprofiel en het gedrag van eerdere bezoekers met vergelijkbare profielen, om inhoud en stationsomzettingen aan te passen. </p> <p>Tijdens het maken van een A/B-activiteit met behulp van de driestappe geleide workflow kunt u ervoor kiezen om verkeer toe te wijzen met behulp van de <span class="wintitle"> Auto-Target voor persoonlijke ervaringen </span> optie: </p> <p> <img src="assets/auto-target-ui-small.png" id="image_DB7899CAD51D411EAB858CE132BECAA5" /> </p> <p>Zie voor meer informatie <a href="/help/main/c-activities/auto-target/auto-target-to-optimize.md" format="dita" scope="local"> Auto-Target voor persoonlijke ervaringen </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

### Target Standard/Premium 17.7.1 (20 juli 2017) {#section_BB75DE30174F4ADD963451909FB81D74}

<table id="table_BCE36E0D56804E7B8861858DCF2F380E"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Functie </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Soorten publiek </p> </td> 
   <td colname="col2"> <p>U kunt nu de definitiedetails van het publiek op een pop-up kaart in diverse plaatsen in het Doel UI bekijken zonder het publiek te openen. Deze functionaliteit is alleen van toepassing op publiek dat is gemaakt in <span class="keyword"> Target Standard/Premium. </span> </p> <p> <img src="assets/audience_details.png" id="image_AD0F411715DA43ACB4A913B1E54C13DC" /> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Succeswaarden </p> </td> 
   <td colname="col2"> <p>Eerder, stond Doel gebiedsdeel op enige metrisch toe en dat metrisch moest worden bereikt alvorens zijn telling werd verhoogd. U kunt gebiedsdeel op veelvoudige metriek samen met de flexibiliteit nu verstrekken om te kiezen of metrisch voor de telling aan toename zou moeten worden bereikt of niet. </p> <p>De multimetrische gebiedsdeelfunctionaliteit wordt niet gesteund voor het volgende: </p> <p> 
     <ul id="ul_EC856F910B704D648065EA7DA13EE5B0"> 
      <li id="li_1A82414FE50B414CAA1A0A88E80BCC1B"> <p>Recommendations-activiteiten. Deze functionaliteit wordt ondersteund voor alle andere typen activiteiten. </p> </li> 
      <li id="li_2D6CF42264D445FCB6C400ED321DE952"> <p>Als u Analytics als uw rapporteringsbron (A4T) gebruikt. </p> </li> 
      <li id="li_E3A983A70BB04AE8B25A7CEC1F5FE1D9"> <p>Het metrische type "Viewed a Page". </p> </li> 
      <li id="li_9AAF6BB275F7489BA691676E308172D5"> <p>Het metrische type "Clicked an Element" voor VEC-activiteiten (Visual Experience Composer). </p> </li> 
     </ul> </p> <p>Raadpleeg de volgende onderwerpen voor meer informatie: </p> <p> 
     <ul id="ul_4B0EFFDD257C42579E19569DCBE15BE3"> 
      <li id="li_2402575F27F547968BD536C460BF81B5"> <p>A/B: <a href="/help/main/c-activities/t-test-ab/t-test-create-ab/ab-goals-and-settings.md#reference_B25389FD6F3A4989801E740364B089CC" format="dita" scope="local"> Doelstellingen en instellingen </a> </p> </li> 
      <li id="li_FB5E7CBC0154406C989F5A5C6CAA0C8F"> <p>Automated Personalization (AP): <a href="/help/main/c-activities/t-automated-personalization/create-ap-activity.md#task_8AAF837796D74CF893CA2F88BA1491C9" format="dita" scope="local"> Automated Personalization-activiteiten maken </a> </p> </li> 
      <li id="li_57C36A7945A24A52BCBD62CA0F15B668"> <p>Gericht op ervaring (XT): <a href="/help/main/c-activities/t-experience-target/t-xt-create/xt-goals-and-settings.md#reference_B25389FD6F3A4989801E740364B089CC" format="dita" scope="local"> Doelstellingen en instellingen </a> </p> </li> 
      <li id="li_06674A3152A547268A1AE5EE818EF1A5"> <p>Multivariatie (MVT): <a href="/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/goals-and-settings.md#reference_B25389FD6F3A4989801E740364B089CC" format="dita" scope="local"> Doelstellingen en instellingen </a> </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Rapportage (automatisch A/B-tests toewijzen) </p> </td> 
   <td colname="col2"> <p>De capaciteit om veelvoudige metriek te bekijken is nu beschikbaar voor auto-Wijs A/B activiteiten. </p> <p>Zie voor meer informatie <a href="/help/main/c-reports/c-report-settings/view-multiple-metrics.md#concept_9E3C3F6F3EC1412FAF252975AC0720B7" format="dita" scope="local"> Meerdere metriek weergeven in een rapport </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Soorten publiek </p> </td> 
   <td colname="col2"> <p>Sitepaginatypen en vergelijkingsoperatoren voor de doelsite komen nu overeen met typen en vergelijkingsoperatoren in Target Classic. </p> <p>U kunt nu het publiek van sitepagina's maken met behulp van uw eigen 'door de gebruiker gedefinieerde queryparameter' of 'door de gebruiker gedefinieerde header'. </p> <p>Zie voor meer informatie <a href="/help/main/c-target/c-audiences/c-target-rules/site-pages.md#concept_6425D5304568490899E8340CC94798A9" format="dita" scope="local"> Sitepagina's </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Activiteiten </p> </td> 
   <td colname="col2"> <p>In de lijst Activiteit kunt u nu filteren op de activiteitstypen Automatisch toewijzen en Automatisch doel. </p> <p>Zie voor meer informatie <a href="/help/main/c-activities/activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03" format="dita" scope="local"> Activiteiten </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p>Recommendations-criteria en -aanbiedingen </p> </td> 
   <td colname="col2"> <p>U kunt lege waarden nu afhandelen door te filteren op Vergelijking kenmerk entiteit, Vergelijking kenmerken profiel en Overeenkomende parameters. </p> <p>Zie voor meer informatie <a href="/help/main/c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md#concept_4CB5C0FA705D4E449BD0B37B3D987F9F" format="dita" scope="local"> Dynamische en statische insluitingsregels gebruiken </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

Dit [!DNL Target] de release bevat de volgende verbeteringen en oplossingen voor de klant: (nummer van de uitgave staat tussen haakjes voor intern gebruik van Adobe):

* De workflow is verbeterd wanneer een gebruiker [!DNL Target] sessietijden uit tijdens het maken of bewerken van een activiteit of aanbieding. Wanneer de gebruiker klikt [!UICONTROL Save], wordt het bericht dat de sessie is verlopen weergegeven, maar nadat u zich weer hebt aangemeld, wordt de gebruiker in een dialoogvenster op de hoogte gebracht van een geslaagde aanmelding en blijft de gebruikersinterface op dezelfde pagina staan in [!DNL Target] zonder gegevensverlies.

   Als een gebruiker een intermitterende actie uitvoert op een [!DNL Target] pagina en ondervindt een sessietime-out. De gebruiker wordt doorgestuurd naar opnieuw aanmelden en vervolgens wordt doorgestuurd naar de laatste pagina die in het dialoogvenster is bewerkt [!DNL Target] UI.

* Probleem verholpen waarbij wijzigingen in aangepaste code verloren gingen als de gebruiker wegbladert (wijzigt ervaringen, wisselpagina, wisselend publiek, klikt op Volgende enz.) en vergeet wijzigingen op te slaan. De gebruiker wordt nu gevraagd de wijzigingen op te slaan. (TGT-23766)
* Wanneer een activiteit wordt gearchiveerd, wordt &quot;Gearchiveerd de activiteit&quot; weergegeven in plaats van &quot;De activiteit bijwerken&quot;. (kB-1517)
* De drop-down kiezer in de volgende plaatsen binnen het Doel UI is vervangen met auto-volledige functionaliteit om snelheid en prestaties te verbeteren: (TGT-22939)

   * Activiteitspagina > *activiteit* > Stap3 > De kiezer van de Reeks rapporteren
   * Soorten publiek > Soorten publiek maken > Bezoekersprofiel
   * Recommendations > Feed Creation > When source type > Analytics > Report Suite picker

* Verbeterd foutbericht wanneer voor een site &quot;X-Frame-options&quot; is ingesteld op SAMEORIGIN en de site niet kan worden geladen in Visual Experience Composer (VEC). Het bericht zet de gebruiker ertoe aan om op Verbeterde Composer van de Ervaring in Beleid > Visuele Composer van de Ervaring over te schakelen. (TGT-17356)
* Rapporten in Standaard/Premium worden nu weergegeven in de tijdzone van uw account in plaats van in de tijdzone van de doelserver (US EST). (TGT-24868)
* Indien activiteiten die in [!DNL Target] worden bijgewerkt van buiten [!DNL Target] (bijvoorbeeld via Adobe I/O) worden de volgende activiteitskenmerken weer geïmporteerd in [!DNL Target]:

   `thirdpartyId`

   `startDate`

   `endDate`

   `status`

   `priority`

   `marketingCloudMetadata(remoteModifiedBy)`

   Deze importtaak wordt uitgevoerd wanneer de activiteitenpagina wordt geopend, met een maximale vertraging van tien minuten. (kB-1526)

### Target Standard/Premium 17.6.2 (22 juni 2017) {#section_F0372B07B56E454CB048CE79FF56E9CD}

<table id="table_8C4DB1B83B874E4C85CE9FF352E7B857"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Functie </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1" class="premium"> <p>Activiteiten van Automated Personalization (AP) </p> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_F5BB1074DD4140C798CB55D68DEEF824"> 
      <li id="li_9596AABA14C64DEEB2E70E8ADED8AA74">Automated Personalization-activiteiten kunnen worden gemaakt met behulp van de op formulieren gebaseerde composer. </li> 
      <li id="li_315F5FF590404670A677FEA6E4E0DF5D">Nieuwe betrouwbaarheidsnummers voor Automated Personalization </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p>Recommendations: Criteria en aanbiedingen </p> </td> 
   <td colname="col2"> <p> U kunt nu dynamische criteria en promoties maken op basis van overeenkomsten tussen profielkenmerken en parameters. </p> <p> <img src="assets/inclusion_rules.png" id="image_D136F75A5C2B428390FE231559AEC2D3" /> </p> <p> <p>Opmerking: Als u vertrouwd met bent hoe de inclusieregels voorafgaand aan Doel 17.6.1 versie (Juni 2017) werden gevormd, zult u merken dat sommige opties en exploitanten zijn veranderd. Alleen de operatoren die van toepassing zijn op de geselecteerde optieweergave en sommige operatoren hebben een andere naam gekregen ("overeenkomsten" zijn nu "gelijk"), zodat ze consistenter en intuïtiever zijn. Alle bestaande uitsluitingsregels die vóór deze release zijn gemaakt, zijn automatisch naar de nieuwe structuur gemigreerd. Van uw kant is geen herstructurering nodig. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Verbeteringen in de VEC Code Editor </p> </td> 
   <td colname="col2"> <p> Als de paginaopmaak verandert en de handelingen niet kunnen worden toegepast, verschijnt nu een waarschuwing naast elke mislukte handeling. Eerder heeft een algemene fout de gebruiker laten weten dat de paginastructuur is gewijzigd. De code-editor markeert nu elke mislukte handeling. </p> </td> 
  </tr> 
 </tbody> 
</table>

Dit [!DNL Target] de release bevat de volgende verbeteringen en oplossingen voor de klant:

* Verbeterde prestaties op hostgroepen en aanbevelingen voor zoekpagina&#39;s van entiteiten.
* Beschrijvende foutberichten voor het hele doel, vooral als deze betrekking hebben op synchronisatiefouten.
* Probleem verholpen waarbij de telling van het activiteitsdiagram soms onjuist was in de gebruikersinterface wanneer automatisch dedupliceren wordt toegepast na het maken van uitsluitingsgroepen.
* Probleem verholpen waarbij handmatige insluitingen mogelijk niet correct worden weergegeven in de gebruikersinterface wanneer een bestaande activiteit met uitsluitingsgroep wordt bewerkt.

### Target Standard/Premium 17.6.1 (8 juni 2017) {#section_1D05FE23CE3744DDB5D28E933341F575}

<table id="table_47117524922A472AA977C652B581B356"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Functie </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Experience Targeting (XT)-activiteiten </p> </td> 
   <td colname="col2"> <p>Met de functie slepen en neerzetten kunt u het publiek en de ervaringen in de gewenste volgorde rangschikken tijdens het maken of bewerken van XT-activiteiten. Bezoekers worden op hun ervaringen beoordeeld, van boven naar beneden. </p> <p> <img src="assets/move_exp.jpg" id="image_0AA2EE2B5B00462C8E125A30F145E654" /> </p> <p>Zie voor meer informatie <a href="/help/main/c-activities/t-experience-target/t-xt-create/xt-add-experience.md#task_454646F2895242D3B92DC395A0CE1A00" format="dita" scope="local"> Ervaring maken </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Rapportage: A/B, XT en Recommendations </p> </td> 
   <td colname="col2"> <p>De rapporten voor A/B, XT, en de activiteiten van Recommendations omvatten visuele vertegenwoordiging die u visueel het betrouwbaarheidsinterval laat zien en optilt zodat u een winnaar nauwkeuriger kunt bepalen. U kunt de muis boven de representaties houden om de werkelijke getallen te zien. Deze functie is niet beschikbaar voor activiteiten die Analytics als rapportagebron (A4T) gebruiken. </p> <p> <img src="assets/whisker.JPG" id="image_DFD8EED61D52497280066D55AD473479" /> </p> <p>Zie voor meer informatie <a href="/help/main/c-reports/c-report-settings/report-settings.md#concept_4BB6A7FDAB6F4806A632F9CD989B8BFA" format="dita" scope="local"> Rapportinstellingen </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p>Activiteiten van Automated Personalization (AP) </p> </td> 
   <td colname="col2"> <p>U kunt uitsluitingsgroepen maken in AP-activiteiten om ervoor te zorgen dat ervaringen met de toegewezen aanbiedingen automatisch worden uitgesloten. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p>Recommendations: Criteria en aanbiedingen </p> </td> 
   <td colname="col2"> <p><b>(Gepland voor vrijgave 22 juni 2017)</b> U kunt nu dynamische criteria en promoties maken op basis van overeenkomsten tussen profielkenmerken en parameters. </p> <p> <img src="assets/inclusion_rules.png" id="image_694305D969AF43F7822012F69614250C" /> </p> <p>Zie voor meer informatie <a href="/help/main/c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md#concept_4CB5C0FA705D4E449BD0B37B3D987F9F" format="dita" scope="local"> Dynamische en statische insluitingsregels gebruiken </a>. </p> <p> <p>Opmerking: Als u vertrouwd met bent hoe de inclusieregels voorafgaand aan Doel 17.6.1 versie (Juni 2017) werden gevormd, zult u merken dat sommige opties en exploitanten zijn veranderd. Alleen de operatoren die van toepassing zijn op de geselecteerde optieweergave en sommige operatoren hebben een andere naam gekregen ("overeenkomsten" zijn nu "gelijk"), zodat ze consistenter en intuïtiever zijn. Alle bestaande uitsluitingsregels die vóór deze release zijn gemaakt, zijn automatisch naar de nieuwe structuur gemigreerd. Van uw kant is geen herstructurering nodig. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Naamgevingsactiviteiten </p> </td> 
   <td colname="col2"> <p>U wordt nu gevraagd de activiteit een naam te geven voordat u deze opslaat. U kunt een activiteit zonder een naam niet opslaan. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Nieuwe locatie voor doelforum </p> </td> 
   <td colname="col2"> <p> Het doelforum is verplaatst naar het nieuwe <a href="https://forums.adobe.com/community/experience-cloud/marketing-cloud/target" format="https" scope="external"> Adobe Community Platform </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

### Target Standard/Premium 17.4.1 (27 april 2017) {#section_24E6889AF1E0405497F6F77A407A9A46}

Deze release bevat de volgende functies en verbeteringen:

<table id="table_9554D0094421417C88548BDC97B710F5"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Functie </th> 
   <th colname="col2" class="entry"> Details </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Rapportage </td> 
   <td colname="col2"> <p><b>Meerdere doelen/cijfers weergeven:</b> U kunt veelvoudige metriek in A/B en Ervaring nu bekijken richtend (XT) activiteiten, met uitzondering van <a href="/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md#concept_A1407678796B4C569E94CBA8A9F7F5D4" format="dita" scope="local"> Automatisch toewijzen </a> en <a href="/help/main/c-activities/auto-target/auto-target-to-optimize.md" format="dita" scope="local"> Automatisch doel </a> A/B-activiteiten. </p> <p>Zie voor meer informatie <a href="/help/main/c-reports/c-report-settings/view-multiple-metrics.md#concept_9E3C3F6F3EC1412FAF252975AC0720B7" format="dita" scope="local"> Meerdere metriek weergeven in een rapport </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

Dit [!DNL Target] release richt zich op back-end oplossingen en bevat de volgende klantgerichte verbeteringen en oplossingen: (nummer van de uitgave staat tussen haakjes voor intern gebruik van Adobe):

* Probleem verholpen waarbij de instelling &quot;Aantal verhogen, Gebruiker vrijgeven &amp; opnieuw invoeren toestaan&quot; in Geavanceerde instellingen ertoe leidde dat activiteiten niet correct zouden werken. (TNT-26556)
* Probleem verholpen waardoor gegevens van kenmerk van klant niet uit Target konden worden verwijderd nadat ze met NULL waren bijgewerkt in de gebruikersinterface van Experience Cloud. (TNT-26462)

### Wijzigingen in Platform (13 april 2017) {#section_B59C26405EB7482AA80820D6D39B9C44}

<table id="table_6167ECB7B44F40DCADF299F46F1F795C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Wijzigen </th> 
   <th colname="col2" class="entry"> Details </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="filepath"> at.js </span> </p> </td> 
   <td colname="col2"> <p> <span class="filepath"> at.js </span> versie 0.9.6 is nu beschikbaar. Zie voor meer informatie <a href="https://developer.adobe.com/target/implement/client-side/atjs/how-to-deployatjs/implement-target-without-a-tag-manager/" format="dita" scope="local"> Downloaden om.js </a>. </p> <p>De volgende verbeteringen en correcties zijn opgenomen in <span class="filepath"> at.js </span> versie 0.9.6: </p> <p> 
     <ul id="ul_108DF85393614C69988E299485D338FD"> 
      <li id="li_4117C900982240B5AFFCFE1B2716A443"> <p>Omleiding biedt ondersteuning voor A4T. Nadat u hebt gedownload en geïnstalleerd <span class="filepath"> at.js </span> versie 0.9.6, kunt u de aanbiedingen van de doorverwijzing in activiteiten gebruiken die <span class="keyword"> Adobe Analytics </span> als rapportbron voor <span class="keyword"> Doel </span> (A4T). Naast <span class="filepath"> at.js </span> versie 0.9.6, zijn er andere minimumvereisten uw implementatie moet voldoen om aanbiedingen van de omleiding en A4T te gebruiken. Voor meer informatie en extra belangrijke informatie zou u moeten weten, zie <a href="/help/main/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-redirect-offers.md#concept_21BF213F10E1414A9DCD4A98AF207905" format="dita" scope="local"> Omleidingsvoorstellen - Veelgestelde vragen A4T </a>. </p> </li> 
      <li id="li_DA5321D72E81496DB7C49D589E1A59C4"> <p>Voor <span class="filepath"> at.js </span> 0.9.6, wanneer de API voor bezoekers aanwezig was op de pagina en de <span class="codeph"> bezoekerApiTimeout </span> het plaatsen was te agressief, kon Doel in een situatie lopen toen geen MCID- gegevens in werden verzonden <span class="keyword"> Doel </span> verzoek. Dit kan leiden tot problemen zoals onsite treffers in <span class="keyword"> Analyse </span> bij gebruik van A4T. </p> <p>Dit gedrag is gewijzigd in <span class="filepath"> at.js </span> 0.9.6, zelfs als de <span class="codeph"> bezoekerApiTimeout </span> wordt geplaatst om 1 ms te zeggen, zal het Doel proberen om SDID, volgende servers, en gegevens van klant IDs te verzamelen en die in het verzoek van het Doel te verzenden. </p> </li> 
      <li id="li_B11CE11D9A594CB1ABB85BD0D93C4A15"> <p>De <span class="codeph"> selectorsPollingTimeout </span> instellen. Zie voor meer informatie <a href="https://developer.adobe.com/target/implement/client-side/atjs/atjs-functions/atjs-functions/" format="dita" scope="local"> targetGlobalSettings() </a>. </p> </li> 
      <li id="li_D6F862099A374FE394F4DA3520A1BBF0"> <p>De indeling van de reactie van <span class="codeph"> getOffer() </span> is gewijzigd. Zie voor meer informatie <a href="https://developer.adobe.com/target/implement/client-side/atjs/atjs-functions/atjs-functions/v" format="dita" scope="local"> adobe.target.getOffer(opties) </a>. </p> </li> 
      <li id="li_80166567ED8945ECB37FEEE2C5F06ACE"> <p>Logboekregistratie voor console is toegevoegd voor niet-ondersteunde <span class="codeph"> &lt;!DOCTYPE&gt; </span> aangiften. </p> </li> 
      <li id="li_02904EBAE8D3400092B762F0B28B0C86"> <p>Probleem verholpen waarbij <span class="keyword"> Doel - Klassiek </span> plug-ins werden niet correct toegepast wanneer meerdere standaardaanbiedingen naar één box werden verzonden. (TGT-22664)</p> </li> 
      <li id="li_7016022D9DDE4529B77984F195825AB7"> <p>Verbeterde cookie-instelling voor twee TLD's (Top-Level-Domain) om ervoor te zorgen dat de cookie van de box correct is ingesteld voor deze domeinen (bijvoorbeeld <span class="filepath"> test.no </span>, <span class="filepath"> autodrives.ca </span>, enzovoort). </p> </li> 
      <li id="li_3B1F618DEC744056B5BB172C4DBB359A"> <p>Het algoritme voor het extraheren van het domein op het hoogste niveau dat moet worden gebruikt bij het opslaan van cookies is gewijzigd in <span class="codeph"> at.js </span> versie 0.9.6. Vanwege deze wijziging kunnen cookies niet worden opgeslagen naar adressen die IP gebruiken. Meestal worden IP-adressen gebruikt voor testdoeleinden, maar als tijdelijke oplossingen kunt u DNS-vermeldingen gebruiken of het hostbestand op een lokaal vak aanpassen. </p> </li> 
      <li id="li_A52181499E63402DB4E16E33E36A9400"> <p>Correctie van het verplaatsen en herschikken van handelingen waarbij eigenschappen tekenreekswaarden zijn in plaats van gehele getallen. </p> </li> 
     </ul> </p> <p>Voor informatie over deze en eerdere versies van <span class="filepath"> at.js </span>, zie <a href="https://developer.adobe.com/target/implement/client-side/atjs/target-atjs-versions/" format="dita" scope="local"> at.js - Versiedetails </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

### Target Standard/Premium 17.3.1 (30 maart 2017 - Bijgewerkt op 13 april 2017) {#section_5C13660A8AA34F35A9CBEFEEC88738D0}

Deze release bevat de volgende functies en verbeteringen:

<table id="table_4BA8DA701BC64427957355E144570EFE"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Functie </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Analyses voor doel (A4T) </p> <p>Omleidingsvoorstellen </p> </td> 
   <td colname="col2"> <p><b>Bijgewerkt op 13 april 2017.</b> </p> <p>Je kunt nu omleidingsvoorstellen gebruiken voor activiteiten die gebruikmaken van <span class="keyword"> Analyse </span> als bron van de rapportage. </p> <p>Deze bibliotheken moeten op de pagina worden opgenomen met het omleidingsvoorstel en de pagina waarnaar de bezoeker wordt omgeleid. Als onderdeel van deze wijziging worden automatisch nieuwe URL-parameters toegevoegd aan uw omleidings-URL's als de service Bezoeker-id op uw site is geïmplementeerd, ongeacht of u Analytics als rapportbron voor die activiteit gebruikt of niet. </p> <p>Zie voor meer informatie <a href="/help/main/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-redirect-offers.md#concept_21BF213F10E1414A9DCD4A98AF207905" format="dita" scope="local"> Omleidingsvoorstellen - Veelgestelde vragen A4T </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Soorten publiek </p> </td> 
   <td colname="col2"> <p>De volgende verbeteringen zijn doorgevoerd voor doelgroepen: </p> <p> 
     <ul id="ul_C920198404654C97A33190A29ACA6990"> 
      <li id="li_DB52EF909C9640649981940460CDF2B5"> <p><b>Wek- en dagscheiding:</b> U kunt instellen <span class="wintitle"> Week- en dagparkeren </span> opties voor het maken van terugkerende patronen voor doelgroepen. </p> <p>Zie voor meer informatie <a href="/help/main/c-target/c-audiences/c-target-rules/time-frame.md#concept_0FE1E8DACD104F8B870B0BADE3197F0A" format="dita" scope="local"> Tijdschema </a>. </p> </li> 
      <li id="li_2541A6EF2D604CE098012A16909C237E"> <p><b> Uitsluitingen bij gecombineerd publiek:</b> U kunt uitsluitingsregels nu toevoegen en het publiek uitsluiten wanneer u meerdere soorten publiek combineert. </p> <p>Zie voor meer informatie <a href="/help/main/c-target/combining-multiple-audiences.md#concept_A7386F1EA4394BD2AB72399C225981E5" format="dita" scope="local"> Meerdere soorten publiek combineren </a>. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p>Recommendations </p> </td> 
   <td colname="col2"> <p><b>Dynamische promoties:</b> Doel Recommendations ondersteunt nu dynamische overeenkomsten voor speciale acties. </p> <p>Zie voor meer informatie <a href="/help/main/c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md#concept_4CB5C0FA705D4E449BD0B37B3D987F9F" format="dita" scope="local"> Dynamische en statische insluitingsregels gebruiken </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>De capaciteit om veelvoudige metriek in een rapport te bekijken, inbegrepen in Doelversie 17.3.1 (30 maart, 2017) is verwijderd toe te schrijven aan onverwacht gedrag. Deze functie is in een volgende release weer beschikbaar.

Dit [!DNL Target] release bevat de volgende verbeteringen en oplossingen: :

* De [!DNL Target] gebruikersinterface is bijgewerkt om aanbiedingen voor omleiding te ondersteunen bij activiteiten die [!UICONTROL Analytics for Target] (A4T) als bron van rapportage. Deze functionaliteit vereist [!DNL at.js] 0.9.6, die binnenkort beschikbaar zal zijn.
* De [!DNL Target] gebruikersinterface is op sommige plaatsen bijgewerkt:

   * In rapporten en activiteiten zijn enkele opties beschikbaar ( [!UICONTROL Edit], [!UICONTROL Share to Feed], [!UICONTROL View Experience URLs], enz.) zijn nu toegankelijk door op de knop [!UICONTROL More Options] icon (  ![icon_more_options-afbeelding](assets/icon_more_options.png)

      ).
   * In de [!UICONTROL Offers] bibliotheek, worden nu in een lijst weergegeven in plaats van als kaarten. In de hele gebruikersinterface zijn andere kleine wijzigingen aangebracht [!UICONTROL Offers] wisselaar-UI.

* De prestaties zijn aanzienlijk verbeterd op de [!UICONTROL Activity] en [!UICONTROL Audience] lijsten. Bovendien worden de laadtijden voor zoekresultaten aanzienlijk sneller weergegeven.
* &quot;Weergaven&quot; is nu &quot;Bezoekingen&quot; in de [!UICONTROL Offer Level Report] for [!UICONTROL Automated Personalization] rapporten.
* [!DNL Target] ondersteunt nu het schakelen tussen omgevingen (hostgroepen) voor [!UICONTROL Automated Personalization] activiteiten.
* [!UICONTROL Automated Personalization] de activiteiten ondersteunen nu hostgroepen .

### Target Standard/Premium 17.2.1 (21 februari 2017) {#section_FC6412353DE64E848FFD5E8EFF72C7C7}

>[!NOTE]
>
>[!DNL Adobe Experience Manager] 6.2 met FP-11577 (of later) steunt nu [!DNL at.js] uitvoering met het [!UICONTROL Adobe Target Cloud Services] integratie. Zie voor meer informatie [Functiepakketten](https://experienceleague.adobe.com/docs/) en [Integreren met Adobe Target](https://experienceleague.adobe.com/docs/) in de *Adobe Experience Manager 6.2* documentatie.

Dit [!DNL Target] release richt zich op verbeteringen op het gebied van bruikbaarheid en prestaties en bevat de volgende verbeteringen en oplossingen (nummer van uitgave tussen haakjes is voor intern gebruik van Adobe):

* Extra items aan het menu Help toegevoegd die vanuit de rechterbovenhoek van het dialoogvenster [!DNL Target] gebruikersinterface. Tot de nieuwe opties behoren: &quot;Blogs&quot; en &quot;Video&#39;s&quot;. De optie Adobe Experience Cloud Status is nu &quot;Adobe Target Standard/Premium Status&quot;. (TGT-22629)
* Wanneer u een publiek verwijdert, [!DNL Target] geeft een lijst weer van activiteiten die naar dat publiek verwijzen. Gebruikers kunnen op elke activiteit in de lijst klikken om de bijbehorende activiteit weer te geven [!UICONTROL Overview] pagina. (TGT-17997)
* Verbeterd `user.activeCampaigns` om de campagne-id te retourneren voor alle campagnes/activiteiten waarin de gebruiker zich bevindt, zelfs als hij of zij in de huidige sessie niet heeft gereageerd op de campagne/activiteit. (TNT-26237)
* De [!UICONTROL Create Activity] op de knop [!UICONTROL Activities] Deze pagina is nu actief voordat alle activiteitennamen in de lijst worden geladen. Deze verbetering laat gebruikers nieuwe activiteiten sneller tot stand brengen, vooral wanneer de rekening vele gevormde activiteiten heeft. (TGT-21470)
* Verbeterde laadtijd voor websites met HTTPS die via proxy kunnen worden benaderd. Dit is een verbetering van de Enhanced Experience Composer (EEC). Het doel haalt geen statische middelen meer via volmacht. (TGT-21793)
* Prestatieverbeteringen aangebracht op de [!UICONTROL Goals & Settings] pagina, vooral laadtijd wanneer er veel metriek zijn gedefinieerd voor een activiteit. (TGT-21654)
* Knopinfo toegevoegd op het tabblad [!UICONTROL Goals & Settings] pagina van alle activiteiten die [!UICONTROL Analytics for Target] (A4T) gebruikers melden dat een trackingserver niet vereist is als de pagina&#39;s van de activiteit op .js (versie 0.9.1 of hoger) zijn geladen. (TGT-22607)
* Metrische namen worden nu weergegeven op het tabblad [!UICONTROL Goals & Settings] pagina zonder dat gebruikers elke metrische waarde moeten uitvouwen om de volledige metrische naam weer te geven. Deze verbetering laat gebruikers metriek sneller en efficiënter uitgeven. (TGT-21276)
* U kunt nu toepassen [!DNL Recommendations] opname van regels naar aangepaste criteria (geüpload via CSV), net als andere criteria. (TGT-21896)
* Verbeterde gebruikersinterface en bruikbaarheid van de [!UICONTROL Offers] pagina, vooral wanneer u mappen maakt of beheert en aanbiedingen maakt. (TGT-22509 en TGT-22187)
* De gebruikerservaring in de [!UICONTROL Visual Experience Composer] (VEC) wanneer u items selecteert die u wilt verbergen.
(TGT-2224)
* De gebruikerservaring is verbeterd bij het maken van activiteiten met de [!UICONTROL Form-Based Experience Composer]. Wanneer u een locatie voor het selectievakje kiest, blijft het validatierand gemarkeerd nadat u op [!UICONTROL Next]. (TGT-2221)
* Verbeterde de gedownloade rapporten om onderscheid te maken tussen actieve en verwijderde aanbiedingen. (TGT-22449)
* Probleem verholpen waardoor oudere elementen niet konden worden weergegeven in de lijst met oneindig schuifbare elementen in de gebruikersinterface van de basisservice Experience Cloud Assets. (TGT-19733)
* Probleem verholpen waarbij de extreme orderinstelling niet in gedownloade CSV-rapporten werd gebruikt. (TGT-21871)
* Het probleem waarbij extreme bestellingen niet correct werden gemarkeerd in het gedownloade bestand, is opgelost. [!UICONTROL Order Details]CSV-rapport. (TGT-22500)
* Probleem verholpen waarbij de onjuiste ordertijd werd weergegeven in het gedownloade bestand. [!UICONTROL Campaign Audit] Het rapport CSV, alhoewel het rapport de correcte ordedatum vertoonde. (TNT-26469)
* Het probleem dat ervoor zorgde dat de [!UICONTROL Disable JavaScript] van het correct werken aan activiteiten met meerdere pagina&#39;s. (TGT-15130)
* Als u de Composer Formuliergebaseerde ervaring gebruikt met een andere box dan de automatisch gemaakte globale box ( `target-global-mbox`) en kies vervolgens een betrokkenheidsmetrische waarde als een succesmetrische waarde, waarbij de metrische waarde alleen wordt verhoogd op pagina&#39;s waarop het selectievakje is gebruikt in de activiteit. Als voorbeeld: als uw box `homepage_mbox`de [!UICONTROL Pages Per Visit] metrisch is het aantal treffers aan `homepage_mbox` tijdens dat bezoek.

   Als u dit niet wilt, kunt u een andere locatie aan de activiteit toevoegen en het globale vakje aan die locatie toewijzen en de standaardinhoud ervan geven. Deze tijdelijke oplossing verbindt globale mbox met de activiteit en staat Doel toe om metrisch voor het melden te tellen.

### Wijzigingen in Platform (18 januari 2017) {#section_EA41802B2B24426FBA88D25E17DBE360}

<table id="table_3A2CD47252894F119B0E60BF6A9285B0"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Wijzigen </th> 
   <th colname="col2" class="entry"> Details </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> at.js </span> versie 0.9.4 </p> </td> 
   <td colname="col2"> <p>18 januari 2017 </p> <p> <span class="codeph"> at.js </span> versie 0.9.4 bevat de volgende wijzigingen: </p> <p> 
     <ul id="ul_8F149C28E2D946B9888B4D2F45167C3C"> 
      <li id="li_93E866BBFE374E93BCDB65BCFAC33B62"> <p> mbox-namen kunnen nu speciale tekens bevatten, waaronder ampersands ( &amp; ). (TNT-26144) </p> <p>Zie voor meer informatie <a href="https://developer.adobe.com/target/implement/client-side/atjs/how-to-deployatjs/implement-target-without-a-tag-manager/" format="dita" scope="local"> at.js Configurations </a>. </p> </li> 
      <li id="li_99309046030B4D93B59113C01A8789DA"> <p>Toegevoegd <span class="codeph"> secureOnly </span> instelling die aangeeft of <span class="codeph"> at.js </span> mag alleen HTTPS gebruiken of mag schakelen tussen HTTP en HTTPS op basis van het paginaprotocol. Dit is een geavanceerde instelling die standaard op Onwaar wordt ingesteld en via <span class="codeph"> targetGlobalSettings </span>. (TNT-26183) </p> <p>Zie voor meer informatie <a href="https://developer.adobe.com/target/implement/client-side/atjs/atjs-functions/atjs-functions/" format="dita" scope="local"> targetGlobalSettings() </a>. </p> </li> 
      <li id="li_D84D578C43A24D4896795999F841CEB8"> <p>De <span class="wintitle"> Ondersteuning voor oudere browsers </span> optie is beschikbaar in <span class="codeph"> at.js </span> versie 0.9.3 en eerder. Deze optie is verwijderd in <span class="codeph"> at.js </span> versie 0.9.4. </p> <p>Zie voor meer informatie <a href="https://developer.adobe.com/target/implement/client-side/atjs/how-to-deployatjs/implement-target-without-a-tag-manager/" format="dita" scope="local"> at.js Configurations </a>. </p> </li> 
     </ul> </p> <p>Voor gedetailleerde informatie over de wijzigingen in elke versie van <span class="codeph"> at.js </span>, zie <a href="https://experienceleague.adobe.com/docs/target/using/implement-target/client-side/target-atjs-versions.html" format="html" scope="external"> at.js - Versiedetails </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

### Target Standard/Premium 17.1.1 (19 januari 2017) {#section_88AFA2F54CF24DF7822CFEBB07DFABE2}

Deze release bevat de volgende functies en verbeteringen:

<table id="table_4F7D4A71F5DF4E8782C7DBEEEF24AD04"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Functie </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Inhoud/aanbiedingen </p> </td> 
   <td colname="col2"> <p>De volgende verbeteringen zijn nu beschikbaar voor aanbiedingen: </p> <p> 
     <ul id="ul_7D8E81443E0F48B6A0C1D1DF6F27D292"> 
      <li id="li_EA529EF4EBC2416E9D3B9E7251E7AAAB"> <p>De naam van de pagina Inhoud is gewijzigd in Aanbiedingen. Bovendien zijn er nu twee tabbladen aan de rechterkant om codes aan te bieden van afbeeldingsaanbiedingen. </p> <p>Als u vóór deze release code en afbeeldingen in dezelfde map had, worden deze door Target gesplitst in twee dubbele mappen. </p> </li> 
      <li id="li_9574FA6BDCFB4BAB938273BF7F4B21C8"> <p>Aanbiedingen die zijn gemaakt via Target Classic, Adobe Experience Manager (AEM), Adobe Mobile Services (AMS) en API's zijn nu zichtbaar in de gebruikersinterface Target Standard/Premium. Aanbiedingen die zijn gemaakt in Target Classic, kunnen worden bewerkt in Target Standard/Premium. (TGT-15738) </p> <p> Aanbiedingen die in de laatste twee jaar met behulp van deze methoden zijn bijgewerkt, zijn zichtbaar in Target Standard/Premium (d.w.z. januari 2015 en daarna). </p> </li> 
      <li id="li_CAD67C9EBB564525ABD2269D918275F8"> <p>U kunt aanbiedingen nu filteren op bron en type. </p> </li> 
     </ul> </p> <p>Zie voor meer informatie <a href="/help/main/c-experiences/c-manage-content/manage-content.md#concept_17874A6FCBB743AA84C5988E8571CCF3" format="dita" scope="local"> Aanbiedingen </a>. </p> <p>De volgende verbeteringen zijn aangebracht op het gebied van geolocatie: </p> <p> 
     <ul id="ul_DD8B50F980B8447A8C37EA96530D8949"> 
      <li id="li_348E04AB29B14E6F83E3A7E7BF7D75B8"> <p>U kunt nu <span class="codeph"> profiel.geolocation </span> worden rechtstreeks als tokens gebruikt in aanbiedingen, plug-ins enzovoort. (TNT-25967) </p> </li> 
     </ul> </p> <p>Zie voor meer informatie <a href="/help/main/c-target/c-audiences/c-target-rules/geo.md#concept_5B4D99DE685348FB877929EE0F942670" format="dita" scope="local"> Geo </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Rapportage </p> <p> <p>Opmerking: Deze verbeteringen zijn niet van toepassing op Analytics for Target (A4T)-rapporten. </p> </p> </td> 
   <td colname="col2"> <p>De volgende rapporteringsverhogingen zijn nu beschikbaar voor de rapporten van het Doel. </p> <p> 
     <ul id="ul_ACFCA821B120419EA252EF5031309D52"> 
      <li id="li_0B634602BB044AEDB26DAF78189AB833"> <p>De gebruikersinterface voor rapporten is opnieuw ontworpen. </p> </li> 
      <li id="li_309435D10AE84E8795C4CCC1F36747F7"> <p>Doelrapporten hebben nu een optie om rapportgegevens opnieuw in te stellen om oude gegevens te verwijderen. (TGT-5933) </p> </li> 
      <li id="li_9D30BFCC4CD6461B9DDCD5797A5E2B3A"> <p>De opties voor de telmethode voor rapportage omvatten Bezoekers (de standaardinstelling), Bezoeken en Activity Impressions. (TGT-10002) </p> </li> 
     </ul> </p> <p>Zie voor meer informatie <a href="/help/main/c-reports/statistical-methodology/statistical-calculations.md" format="dita" scope="local"> Rapportinstellingen </a> en <a href="/help/main/c-reports/statistical-methodology/statistical-calculations.md" format="dita" scope="local"> Telmethode </a>. </p> <p>De volgende rapportverbeteringen zijn nu beschikbaar voor downloadbare CSV-rapporten: </p> <p> 
     <ul id="ul_18B0636A41B94F9F903ABFE3E13285DA"> 
      <li id="li_2422075AA0A34F868809C5D580FC5D4B"> <p>Het CSV-rapport op het niveau van de aanbieding bevat nu aanvullende details over elke aanbieding. (TGT-18995) </p> </li> 
      <li id="li_659D126E846348D4BE4544962F41539F"> <p>Gedownloade CSV-bestanden op aanbiedingsniveau bevatten nu altijd gegevens van besturingselementen en doelsegmenten voor <span class="wintitle"> Automated Personalization </span> rapporten. (TGT-22000) </p> </li> 
     </ul> </p> <p>De volgende rapportverbeteringen zijn nu beschikbaar voor Automated Personalization-rapporten (AP). </p> <p> 
     <ul id="ul_5743684487CD4905BA998C298FD423D7"> 
      <li id="li_EB48BA21E00C4878B4408D24DD23BA9C"> <p>Verbeterde laadtijd voor Automated Personalization-activiteiten. </p> </li> 
      <li id="li_B8ECCE250A674B83A66705AD5C45B9C3"> <p>Het betrouwbaarheidsinterval voor doorlopende variabelen (metrische typen Inkomsten en Betrokkenheid) wordt nu weergegeven in samenvattingsrapporten van Automated Personalization (AP). </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Activiteiten </p> </td> 
   <td colname="col2"> <p>De volgende verbeteringen zijn nu beschikbaar voor doelactiviteiten: </p> <p> 
     <ul id="ul_436556860E6C4AEEB35411A02E78A199"> 
      <li id="li_5CC3B995D0AF4B658B3D6C3F6895AA41"> <p>In <span class="keyword"> Adobe mobiele services </span> nu weergeven in het dialoogvenster <span class="keyword"> Doelstandaard/Premium </span> gebruikersinterface. (TGT-10806) </p> <p>Zie voor meer informatie <a href="/help/main/c-activities/activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03" format="dita" scope="local"> Activiteiten </a>. </p> </li> 
      <li id="li_684F9FC5CF414F4A892E6495352B5939"> <p>Wanneer het creëren van multivariate tests, kunt u meer dan 10 percenten van ervaringen van de test nu uitsluiten, op voorwaarde dat u de waarschuwing erkent dat u dan off-line rapportering voor analyse moet gebruiken. (TGT-21719) </p> <p>Zie voor meer informatie <a href="/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/preview-experiences.md#task_21A700587E88453A9FC2210C0DE53A28" format="dita" scope="local"> Voorvertoning van ervaringen voor een multivariate test </a>. </p> </li> 
      <li id="li_B2FC7414C76848B39AD6EA20EE483F06"> <p>De campagne-id is nu zichtbaar op de overzichtspagina van elke activiteit. Dit is nuttig voor API en het oplossen van problemenverrichtingen. (TGT-20928) </p> </li> 
      <li id="li_5A9880AFE5FB46168D92255AA088B854"> <p>Het ontwerp voor de pagina's van het Logboek van de Aantekeningen en van de Verandering is verbeterd. </p> </li> 
      <li id="li_1489EA6C30C94B2AB394189E5FAFF6F6"> <p>De maximale toegestane lengte van anonieme aanbiedingsnamen in Automated Personalization (AP)-activiteiten is verhoogd van 30 naar 250 tekens. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Soorten publiek </p> </td> 
   <td colname="col2"> <p>De volgende verbeteringen zijn nu beschikbaar voor het publiek: </p> <p> 
     <ul id="ul_F1D1F97266134D4ABE627CF2DCE2C6D4"> 
      <li id="li_99A611FCC1254D229D79B8FD075B952A"> <p> <span class="wintitle"> Marketingnaam apparaat </span> is nu beschikbaar als ingebouwde optie in de vervolgkeuzelijst wanneer u een publiek maakt dat zich richt op mobiele apparaten. </p> <p>Met deze wijziging kunt u eenvoudig de naam van een apparaatmodel kiezen in plaats van te zoeken naar het juiste modelnummer van het apparaat. De naam van het marketingapparaat van Galaxy S7 is bijvoorbeeld "Samsung Galaxy S7 Edge", terwijl het apparaatmodel "SM-G9350" is. (TGT-18393) </p> <p>Zie voor meer informatie <a href="/help/main/c-target/c-audiences/c-target-rules/mobile.md#concept_2A794199DC1A4D349FFFBC7DCF1FEB89" format="dita" scope="local"> Mobiel </a>. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p>Recommendations </p> </td> 
   <td colname="col2"> <p>De volgende verbeteringen zijn doorgevoerd in Recommendations: </p> <p> 
     <ul id="ul_9D3644890C0C472D8B485DE9A52898B3"> 
      <li id="li_1E5662348F6E4ABDB2B74FE3326F2FD3"> <p>De resultaatregel voor Back-upalgoritme is nu opgenomen in de bovenste weergave en de bovenste downloadbestanden voor CSV-bestanden. De back-upaanbeveling begint met "*," </p> </li> 
      <li id="li_91DFD809378D4C20918F8F875747CE07"> <p>De extra statussen laten u de vooruitgang van uw voer van de Aanbeveling weten. </p> <p>Zie voor meer informatie <a href="/help/main/c-recommendations/c-products/feeds.md#concept_1228B31E3D0B483B9DD42C5E2AE436E3" format="dita" scope="local"> Feeds </a>. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Enhanced Visual Experience Composer (VEC) </p> </td> 
   <td colname="col2"> <p>Bijgewerkt de IP adressen voor Verbeterde Visual Experience Composer (VEC). </p> <p>Als u IP adressen voegt op lijst van gewenste personen die voor VEC worden gebruikt, voeg de nieuwe IP adressen toe. </p> <p>Zie voor meer informatie <a href="/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/troubleshoot-composer.md#reference_77743144F10143A3A89D56E116D296E4" format="dita" scope="local"> Het oplossen van problemen de Visuele Composer van de Ervaring </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Uitzettingen 2016 {#reference_607661929B504CCFAB3791B13C0DCDBE}

### Target Standard/Premium 16.10.2 (8 november 2016) {#section_2FDEFB3D56CC4BD7BC04DBEECFF6E942}

**Oplossingen**

Deze release bevat de volgende oplossingen:

* Probleem opgelost in [!DNL Recommendations] waarin geen feeds konden worden gemaakt voor niet-standaardomgevingen (hostgroepen).
* Verschillende verbeteringen zijn aangebracht om syntaxisfouten te reduceren.
* Je kunt geen omleidingsvoorstellen meer maken voor activiteiten die [!DNL Analytics for Target] (A4T).

### Target Standard/Premium 16.10.1 (25 oktober 2016) {#section_F76F7329FCAC452FB88F8BE0BA727044}

Deze release bevat de volgende functies en verbeteringen:

<table id="table_F8C01B2A9F07443490DB3025AC3AAC2A"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Functie </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Automatisch toewijzen: Winnerbadge </td> 
   <td colname="col2"> <p>We hebben het nu eenvoudiger gemaakt om een winnaar te bepalen in een Auto-Allocate A/B-activiteit. </p> <p>Veel marketeers maken de fout om voortijdig een winnende ervaring te declareren voordat de resultaten de duidelijke winnaar aangeven. </p> <p>Wanneer u de <span class="wintitle"> Automatische verkeerstoewijzing </span> functie, <span class="keyword"> Doel </span> toont een badge bij de bovenkant van de pagina van de activiteit erop wijst die "Geen Winner nog"tot de activiteit het minimumaantal omzettingen met voldoende vertrouwen bereikt. Wanneer een duidelijke winnaar wordt uitgeroepen, <span class="keyword"> Doel </span> geeft "Winner: Beleef X." </p> <p>Zie voor meer informatie <a href="/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md#concept_A1407678796B4C569E94CBA8A9F7F5D4" format="dita" scope="local"> Automatische verkeerstoewijzing </a> en <a href="/help/main/c-activities/automated-traffic-allocation/determine-winner.md#concept_5741A89ED7224E1285A3BC34B2CCD0F9" format="dita" scope="local"> Een winnaar bepalen </a>. </p> <p> <p>Opmerking: Automatische toewijzing van A/B-activiteiten wordt niet meer ondersteund in Analytics for Target (A4T) forward. Met deze release worden alle actieve Auto-Allocate A/B-activiteiten waarvoor A4T is ingeschakeld, overgeschakeld op <span class="wintitle"> Handmatig </span> wijze (gelijke verkeerstoewijzing). </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Mobiele apparaten zoeken op drager </td> 
   <td colname="col2"> <p>Maak een publiek voor mobiele apparaten die zich op mobiele dragers richten (Verizon, Sprint, AT&amp;T, T-Mobile, enz.). De <span class="wintitle"> Mobiele vervoerder </span> is onder de <span class="wintitle"> Geo </span> instellingen. </p> <p>Zie voor meer informatie <a href="/help/main/c-target/c-audiences/c-target-rules/geo.md#concept_5B4D99DE685348FB877929EE0F942670" format="dita" scope="local"> Geo </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> MboxTrace-verificatietoken genereren vanuit de gebruikersinterface van het doel </td> 
   <td colname="col2"> <p>Geavanceerd inschakelen <span class="keyword"> Doel </span> het zuiveren hulpmiddelen door een tijdelijk authentificatietoken te creëren. </p> <p>Klikken <span class="uicontrol"> Verificatietoken genereren </span> op de <span class="wintitle"> Implementatiedetails </span> pagina ( <span class="uicontrol"> Beheer </span> &gt; <span class="uicontrol"> Implementatie </span>). Vervolgens kunt u de resulterende parameter toevoegen aan de URL's van uw webpagina voor het oplossen van problemen. </p> <p>Zie "Token voor autorisatie ophalen voor gebruik met foutopsporingsgereedschappen" in <a href="/help/main/c-activities/c-troubleshooting-activities/content-trouble.md#concept_D2548B486C984B1E97ED7A72075B8EEA" format="dita" scope="local"> Problemen met inhoudslevering oplossen </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> Recommendations: Criteria ingesteld op volgorde </td> 
   <td colname="col2"> <p>Gebruik in één ervaring maximaal vijf vooraf gedefinieerde criteria voor meer controle over de aanbevelingen die aan bezoekers worden voorgelegd. </p> <p>Zie voor meer informatie <a href="/help/main/c-recommendations/c-algorithms/create-criteria-sequence.md"> Criteria-reeksen maken </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> Recommendations: Externe aanbiedingen invoegen </td> 
   <td colname="col2"> <p>Voeg gepromoveerde objecten toe en controleer de plaatsing ervan in Recommendations-ontwerpen. </p> <p>Zie voor meer informatie <a href="/help/main/c-recommendations/t-create-recs-activity/adding-promotions.md#task_CC5BD28C364742218C1ACAF0D45E0E14" format="dita" scope="local"> Promoties toevoegen </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="firstlook"> <p><b>Eerste weergave</b> </p> Automatisch aanwijzen in A/B-activiteiten </td> 
   <td colname="col2"> <p> <p>Opmerking: Dit "First Look"-aanbod is voor een paar klanten in deze release beschikbaar voor tests en feedback. </p> </p> <p>Automatisch ervaringen in A/B-tests als doel instellen voor de juiste ervaring voor de juiste bezoeker. </p> <p>Zie voor meer informatie <a href="/help/main/c-activities/auto-target/auto-target-to-optimize.md" format="dita" scope="local"> Auto-Target voor persoonlijke ervaringen </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

### Wijziging van streefcijfers voor Platforms (10 oktober 2016) {#section_0761AED70C3E44EA9D8546107B162CC1}

<table id="table_E3E52A4362724D05A8472DB5F51A2429"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Wijzigen </th> 
   <th colname="col2" class="entry"> Details </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> at.js </span> versie 0.9.3 </p> </td> 
   <td colname="col2"> <p>10 oktober 2016 </p> <p> <span class="codeph"> at.js </span> versie 0.9.3 is beschikbaar. </p> <p> 
     <ul id="ul_E4D300700390433E9EF8D5C9D3AA7669"> 
      <li id="li_E916EB3A77ED4CFF90CF6B4D30F188B1"> <p>Zorgt ervoor dat de box in Microsoft Internet Explorer 11 brand roept wanneer oudere browsers in de <span class="codeph"> at.js </span> instellingen. </p> </li> 
      <li id="li_1130509832CE429DB6DE636404CC54E1"> <p>Zorgt ervoor dat de standaardinhoud wordt teruggegeven als een dynamische verre aanbieding ontbreekt (bijvoorbeeld, als URL onjuist is en een fout 404 terugkeert). </p> </li> 
      <li id="li_21B5225D894B43CB863A775C937F66F4"> <p>Zorgt ervoor dat elementen snel worden onthuld wanneer VEC klik-volgende selecteurs niet in DOM kan worden gevonden. </p> </li> 
     </ul> </p> <p>Zie voor meer informatie <a href="https://developer.adobe.com/target/implement/client-side/atjs/target-atjs-versions/" format="dita" scope="local"> at.js - Versiedetails </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

### Target Standard/Premium 16.9.1 (22 september 2016) {#section_3CD20678B6254DE1A9BD41FDD2255DDD}

Deze release bevat de volgende functies en verbeteringen:

<table id="table_FED049F97C054CA895E0AEA3F2B180BF"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Functie </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Soorten publiek combineren </td> 
   <td colname="col2"> <p>Meerdere soorten publiek combineren (inclusief <span class="keyword"> Adobe Experience Cloud </span> publiek en <span class="keyword"> Doel </span> publiek) tijdens de workflow voor het maken van activiteiten. </p> <p>Bijvoorbeeld, kunt u alle loyaliteitklanten richten door specifieke te omvatten <span class="keyword"> Audience Manager </span> segment voor loyaliteitsstatus en deze combineren met een <span class="keyword"> Doel </span> een segment bestaande uit mensen die zich tijdens de huidige sessie hebben aangemeld voor uw loyaliteitsprogramma in plaats van een derde, permanent publiek te maken. </p> <p>Zie voor meer informatie <a href="/help/main/c-target/combining-multiple-audiences.md#concept_A7386F1EA4394BD2AB72399C225981E5" format="dita" scope="local"> Meerdere soorten publiek combineren </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Doelbezoekers gedurende een specifieke periode </td> 
   <td colname="col2"> <p>Begin- en einddatums toevoegen voor een publiek. </p> <p>Met het nieuwe gecombineerde, ad-hocpubliek dat hierboven is vermeld, kunt u bijvoorbeeld low-spenders met specifieke inhoud aanspreken gedurende de drie dagen voorafgaand aan de Zwarte Vrijdag en andere inhoud na Zwarte Vrijdag. </p> <p>Zie voor meer informatie <a href="/help/main/c-target/c-audiences/c-target-rules/time-frame.md#concept_0FE1E8DACD104F8B870B0BADE3197F0A" format="dita" scope="local"> Tijdschema </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Slimme verzamelingen opslaan </td> 
   <td colname="col2"> <p>Functionaliteit zoeken op de <span class="wintitle"> Inhoud </span> De pagina bevat nu opgeslagen mappen, zogenaamde slimme verzamelingen, waarmee u tijd bespaart wanneer u vergelijkbare zoekopdrachten uitvoert. </p> <p>Zie voor meer informatie <a href="/help/main/c-experiences/c-manage-content/filter-and-search-content.md#concept_3B59B8F025BF4CEA82ECC5199D365276" format="dita" scope="local"> Inhoud zoeken en Slimme verzamelingen maken </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Form-based Experience Composer </td> 
   <td colname="col2"> <p>Voeg een koppeling toe aan een afbeelding. De verbinding kan een klik-door verbinding, bestemmingsverbinding, of een landende verbinding zijn. </p> <p>Zie voor meer informatie <a href="/help/main/c-experiences/form-experience-composer.md#task_FAC842A6535045B68B4C1AD3E657E56E" format="dita" scope="local"> Formuliergebaseerde Experience Composer </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Verbeteringen**

Deze release bevat de volgende verbeteringen:

| Verbetering | Beschrijving |
|---|---|
| Visual Experience Composer (VEC) | Verbeterd foutbericht. |

**Bekende problemen**

* De [!UICONTROL Render Using JavaScript] optie wordt momenteel niet gesteund als het samen met douanecode in de Visuele Composer van de Ervaring wordt gebruikt.

### Wijziging van het streefcijfer voor Platforms (september 2016) {#section_1955146045A247D393DB824669A2A916}

<table id="table_8FDAEED5D84C4C718AB863BD6C383F20"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Wijzigen </th> 
   <th colname="col2" class="entry"> Details </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> at.js </span> versie 0.9.2 </p> </td> 
   <td colname="col2"> <p>21 september 2016 </p> <p> <span class="codeph"> at.js </span> versie 0.9.2 is beschikbaar. </p> <p> 
     <ul id="ul_0778A9049C9D48A7B6CB4B79A95F0F4C"> 
      <li id="li_689FF306179F4EC3B391DEE3C53F4B1D"> <p>Toegevoegde <span class="codeph"> optoutEnabled </span> instelling om de optie Weigeren apparaatgrafiek in of uit te schakelen. Als deze instelling is ingesteld op <span class="codeph"> true </span> en de bezoeker heeft ervoor gekozen het bijhouden te beëindigen , zal browser van de bezoeker geen mbox vraag maken. Apparaatgrafiek bevindt zich momenteel in bètaversie. Deze instelling is ingesteld op <span class="codeph"> false </span> standaard, maar moet worden ingesteld op <span class="codeph"> true </span> als u Apparaatgrafiek gebruikt.</p> </li> 
      <li id="li_663462C0680049F89CA8FE1853F31807"> <p>Toegevoegd <span class="codeph"> CustomEvent </span> steun voor het kennisgevingsmechanisme. Eerder <span class="codeph"> at.js </span> gebeurtenismeldingsmechanisme kan niet worden gebruikt via standaard-DOM-API's, zoals <span class="codeph"> document.addEventListener() </span>. Nu kunt u <span class="codeph"> document.addEventListener() </span> om te abonneren op <span class="codeph"> at.js </span> gebeurtenissen, zoals aanvraaggebeurtenissen en gebeurtenissen voor het renderen van inhoud. </p> </li> 
      <li id="li_3FB2914F8D2F4AFFAA9B4622E8CA1EFF"> <p>Oplossing voor een probleem met betrekking tot aanbiedingen die zijn gemaakt in Visual Experience Composer (VEC). Vóór deze release heeft Target de kiezers verborgen en deze alleen niet verborgen wanneer alle kiezers overeenkomen. In <span class="codeph"> at.js </span> 0.9.2 De kiezers worden door het doel verborgen zodra ze overeenkomen. </p> </li> 
     </ul> </p> <p>Zie voor meer informatie <a href="https://developer.adobe.com/target/implement/client-side/atjs/target-atjs-versions/" format="dita" scope="local"> at.js - Versiedetails </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

### Target Standard/Premium 16.9.1 (22 september 2016) {#section_60ADF842E4A0424E8D2A81FB8B813A7A}

Deze release bevat de volgende functies en verbeteringen:

<table id="table_896218AECE4C4EC691B76E79CC7DC356"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Functie </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Soorten publiek combineren </td> 
   <td colname="col2"> <p>Meerdere soorten publiek combineren (inclusief <span class="keyword"> Adobe Experience Cloud </span> publiek en <span class="keyword"> Doel </span> publiek) tijdens de workflow voor het maken van activiteiten. </p> <p>Bijvoorbeeld, kunt u alle loyaliteitklanten richten door specifieke te omvatten <span class="keyword"> Audience Manager </span> segment voor loyaliteitsstatus en deze combineren met een <span class="keyword"> Doel </span> een segment bestaande uit mensen die zich tijdens de huidige sessie hebben aangemeld voor uw loyaliteitsprogramma in plaats van een derde, permanent publiek te maken. </p> <p>Zie voor meer informatie <a href="/help/main/c-target/combining-multiple-audiences.md#concept_A7386F1EA4394BD2AB72399C225981E5" format="dita" scope="local"> Meerdere soorten publiek combineren </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Doelbezoekers gedurende een specifieke periode </td> 
   <td colname="col2"> <p>Begin- en einddatums toevoegen voor een publiek. </p> <p>Met het nieuwe gecombineerde, ad-hocpubliek dat hierboven is vermeld, kunt u bijvoorbeeld low-spenders met specifieke inhoud aanspreken gedurende de drie dagen voorafgaand aan de Zwarte Vrijdag en andere inhoud na Zwarte Vrijdag. </p> <p>Zie voor meer informatie <a href="/help/main/c-target/c-audiences/c-target-rules/time-frame.md#concept_0FE1E8DACD104F8B870B0BADE3197F0A" format="dita" scope="local"> Tijdschema </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Slimme verzamelingen opslaan </td> 
   <td colname="col2"> <p>Functionaliteit zoeken op de <span class="wintitle"> Inhoud </span> De pagina bevat nu opgeslagen mappen, zogenaamde slimme verzamelingen, waarmee u tijd bespaart wanneer u vergelijkbare zoekopdrachten uitvoert. </p> <p>Zie voor meer informatie <a href="/help/main/c-experiences/c-manage-content/filter-and-search-content.md#concept_3B59B8F025BF4CEA82ECC5199D365276" format="dita" scope="local"> Inhoud zoeken en Slimme verzamelingen maken </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Form-based Experience Composer </td> 
   <td colname="col2"> <p>Voeg een koppeling toe aan een afbeelding. De verbinding kan een klik-door verbinding, bestemmingsverbinding, of een landende verbinding zijn. </p> <p>Zie voor meer informatie <a href="/help/main/c-experiences/form-experience-composer.md#task_FAC842A6535045B68B4C1AD3E657E56E" format="dita" scope="local"> Formuliergebaseerde Experience Composer </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Verbeteringen**

Deze release bevat de volgende verbeteringen:

| Verbetering | Beschrijving |
|---|---|
| Visual Experience Composer (VEC) | Verbeterd foutbericht. |

**Bekende problemen**

* De [!UICONTROL Render Using JavaScript] optie wordt momenteel niet gesteund als het samen met douanecode in de Visuele Composer van de Ervaring wordt gebruikt.

### Adobe [!DNL Target] Standard/Premium 16.8.1 (23 augustus 2016) {#section_A8854D4EDF014AEBB81F49EB104D4A20}

De Adobe Target Standard/Premium 16.8.1-release (23 augustus 2016) bevat de volgende functies en verbeteringen:

<table id="table_AE048CB9EA1C4C7BBC2E9D90D26F7395"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Functie </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Hosts en omgevingsbeheer (hostgroep) </p> </td> 
   <td colname="col2"> <p>Organiseer uw sites en pre-productieomgevingen voor eenvoudig beheer en gescheiden rapportage. </p> <p>Gastheren worden gebundeld in omgevingen voor eenvoudig beheer. De vooraf ingestelde omgevingen zijn onder andere Productie, Staging en Ontwikkeling. U kunt ook nieuwe omgevingen toevoegen. </p> <p>Met deze functie wordt functiepariteit bereikt met <span class="keyword"> Doel - Klassiek </span>. </p> <p>Zie voor meer informatie <a href="/help/main/administrating-target/hosts.md#concept_516BB01EBFBD4449AB03940D31AEB66E" format="dita" scope="local"> Gastheren </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Categorie-affiniteit </p> </td> 
   <td colname="col2"> <p>Met de functie voor affiniteit van categorieën worden automatisch de categorieën vastgelegd die een gebruiker bezoekt en wordt de affiniteit van de gebruiker voor de categorie berekend, zodat deze kan worden geactiveerd en gesegmenteerd. Dit helpt ervoor te zorgen dat de inhoud gericht is op bezoekers die het meest waarschijnlijk op die informatie handelen. </p> <p>Met deze functie wordt functiepariteit bereikt met <span class="keyword"> Doel - Klassiek </span>. </p> <p>Zie voor meer informatie <a href="/help/main/c-target/c-visitor-profile/category-affinity.md#concept_75EC1E1123014448B8B92AD16B2D72CC" format="dita" scope="local"> Categorie-affiniteit </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Enhanced Experience Composer inschakelen/uitschakelen op activiteitsniveau </p> </td> 
   <td colname="col2"> <p>Schakel de <span class="wintitle"> Enhanced Experience Composer </span> op het niveau van de rekening (geldt voor alle activiteiten die in de rekening worden gecreëerd) of op het niveau van de individuele activiteit. </p> <p>Eerder kon u de Enhanced Experience Composer alleen op accountniveau in- en uitschakelen. </p> <p>Zie voor meer informatie <a href="/help/main/c-experiences/experiences.md#concept_A2E10F6AFB3D4AEAB6951EE14688848D" format="dita" scope="local"> Ervaringen </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p class="premium">Automated Personalization: prestatierapport van de aanbieding </p> </td> 
   <td colname="col2"> <p>Download een prestatierapport over de aanbieding met alle succesmaatstaven van Automated Personalization. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Verbeteringen**

Deze release bevat de volgende verbeteringen:

<table id="table_E2E4BE72BD79413A821C6A6D1A3AB0F8"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Verbetering </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Gebruikersinterface van code-editor opnieuw ontwerpen </p> </td> 
   <td colname="col2"> <p>De interface van de code-editor is bijgewerkt zodat deze intuïtiever en gebruiksvriendelijker wordt. </p> <p>Zie voor meer informatie <a href="/help/main/c-experiences/c-visual-experience-composer/c-vec-code-editor/vec-code-editor.md#concept_B3A6E9EE3A60406DB640E205EA1745B5" format="dita" scope="local"> Code-editor </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

De volgende bekende problemen zijn gemeld:

* Enkele UI-tekst voor de [!UICONTROL Category Affinity] wordt alleen in het Engels weergegeven. De tekst in andere talen zal in september beschikbaar zijn [!DNL Target] vrijgeven.

### Wijziging van het streefcijfer voor Platforms (juli 2016) {#section_09C18773707B4059852A41C764F817E4}

<table id="table_33B60910EAE24BAFA778F280F72FB683"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Wijzigen </th> 
   <th colname="col2" class="entry"> Details </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="filepath"> at.js </span> versie 0.9.1 </p> </td> 
   <td colname="col2"> <p>14 juli 2016 </p> <p> <span class="filepath"> at.js </span> versie 0.9.1 is nu beschikbaar. </p> <p>Zie voor meer informatie <a href="https://developer.adobe.com/target/implement/client-side/atjs/target-atjs-versions/" format="dita" scope="local"> at.js - Versiedetails </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

### Adobe [!DNL Target] Standard/Premium 16.7.1 (21 juli 2016) {#section_DB583EF9A30247A488EE319583911F22}

De Adobe Target Standard/Premium 16.7.1-release (21 juli 2016) bevat de volgende functies en verbeteringen:

<table id="table_EBA34BD2F5C745DD9EC5231AD79F6C00"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Functie </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Prioriteitsinstellingen voor activiteiten </td> 
   <td colname="col2"> <p>U kunt activiteit prioritaire niveaus van 0-999 nu plaatsen om voor fijnere controle toe te staan over welke activiteitenvertoningen als de veelvoudige activiteiten aan de zelfde plaats met het zelfde publiek worden toegewezen. </p> <p>Deze optie moet zijn ingeschakeld in <span class="wintitle"> Beheer </span> &gt; <span class="wintitle"> Rapportage </span> . </p> <p>De optie Fine-grained priority is van toepassing op A/B Test-, Automated Personalization-, Experience Targeting- en Multivariate Test-activiteiten. </p> <p>Raadpleeg de volgende onderwerpen voor meer informatie: </p> <p> 
     <ul id="ul_FD92CD06CF25480887AC171274262E18"> 
      <li id="li_D321FAED82944D2685DA69EB310D80BE"><b>A/B-test: </b> <a href="/help/main/c-activities/t-test-ab/t-test-create-ab/ab-goals-and-settings.md#reference_B25389FD6F3A4989801E740364B089CC" format="dita" scope="local"> Doelstellingen en instellingen </a> </li> 
      <li id="li_12ECDFD71DB94E22A85AB13B487E8503"><b>Automated Personalization: </b> <a href="/help/main/c-activities/t-automated-personalization/automated-personalization.md#task_8AAF837796D74CF893CA2F88BA1491C9" format="dita" scope="local"> Automated Personalization </a> </li> 
      <li id="li_84B893C214994246AB36E28E84C51460"><b>Gericht op ervaring: </b> <a href="/help/main/c-activities/t-experience-target/t-xt-create/xt-goals-and-settings.md#reference_B25389FD6F3A4989801E740364B089CC" format="dita" scope="local"> Doelstellingen en instellingen </a> </li> 
      <li id="li_26533B659C0E49D6A6D3B3FEBE9CA930"><b>Multivariatietest: </b> <a href="/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/goals-and-settings.md#reference_B25389FD6F3A4989801E740364B089CC" format="dita" scope="local"> Doelstellingen en instellingen </a> </li> 
      <li id="li_FBACF2B73B2E491BBB85618153AC4568"><b>Activiteiten: </b> <a href="/help/main/c-activities/activity-settings.md#task_C6B2FF8374724933BE79A83549B9CD02" format="dita" scope="local"> Activiteiteninstellingen </a> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> Multigetaxeerde Recommendations-kenmerken </td> 
   <td colname="col2"> <p>Alles, aangepast <span class="keyword"> Recommendations </span> attributen kunnen nu meerdere entiteitswaarden bevatten. </p> <p>Zie voor meer informatie <a href="/help/main/c-recommendations/c-products/custom-entity-attributes.md#concept_E5CF39BCAC8140309A73828706288322" format="dita" scope="local"> Kenmerken Aangepaste entiteit </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Ondersteuning voor dynamische/externe aanbiedingen </td> 
   <td colname="col2"> <p>Dynamische inhoud kan onderdeel zijn van elke op formulieren gebaseerde activiteit in <span class="keyword"> Doelstandaard/Premium </span>. Dynamische inhoud wordt buiten <span class="keyword"> Doel </span>. </p> <p>Zie voor meer informatie <a href="/help/main/c-experiences/c-manage-content/about-remote-offers.md#concept_657016A0E6174C22B89036E9C8A0170F" format="dita" scope="local"> Externe aanbiedingen maken </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Soorten publiek en profielscripts kopiëren </td> 
   <td colname="col2"> <p>U kunt nu een bestaand publiek kopiëren dat u vervolgens kunt bewerken om een vergelijkbaar publiek te maken. </p> <p>Zie voor meer informatie <a href="/help/main/c-target/c-audiences/create-audience.md#task_E18BD77A9A8F4ED0AC50569F94556558" format="dita" scope="local"> Een publiek maken </a>. </p> <p>U kunt ook bestaande profielscripts kopiëren. </p> <p>Zie voor meer informatie <a href="/help/main/c-target/c-visitor-profile/profile-parameters.md#concept_8C07AEAB0A144FECA8B4FEB091AED4D2" format="dita" scope="local"> Profielscriptkenmerken </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Klassen gebruiken om elementkiezers te bepalen </td> 
   <td colname="col2"> <p>Element-kiezers kunnen nu worden gebaseerd op klassen of id's in Automated Personalization en Multivariate Test-activiteiten. In vorige versies was deze optie alleen beschikbaar voor A/B-testactiviteiten. </p> <p>Zie voor meer informatie <a href="/help/main/c-experiences/c-visual-experience-composer/vec-selectors.md#concept_4EB7663E255F439B8D24079D23479337" format="dita" scope="local"> Elementkiezers die worden gebruikt in de composer voor visuele ervaring </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> Recommendations: Overeenkomende inhoud </td> 
   <td colname="col2"> <p> Gebruik de regels voor gelijkenis met inhoud om aanbevelingen te doen op basis van item- of mediakenmerken. </p> </td> 
  </tr> 
 </tbody> 
</table>

<table id="table_699755B33F8F48ECABB6FC7E78289A79"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Verbetering </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Rapportageverbeteringen </p> </td> 
   <td colname="col2"> <p>De metrische het rapportdownloads van het succes tonen nu metrische en segmentnamen in plaats van IDs. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> Evalueer mbox ingangsvoorwaarde op elk verzoek in de activiteiten van Automated Personalization </td> 
   <td colname="col2"> <p>In Automated Personalization-activiteiten worden entry-criteria (URL-adressering, sjabloonregels, doelgroep) geëvalueerd voor elke aanvraag voor een nauwkeurigere levering van aanbiedingen. </p> <p>Zie voor meer informatie <a href="/help/main/c-activities/t-automated-personalization/automated-personalization.md#task_8AAF837796D74CF893CA2F88BA1491C9" format="dita" scope="local"> Automated Personalization </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

### Adobe [!DNL Target] Standard/Premium 16.6.1 (16 juni 2016) {#section_C1E9F43111BF4160AF31482CD53E00BD}

Er is geen klant-onder ogen ziende versie gepland voor Juni.

**Oplossingen**

Deze release bevat de volgende oplossingen:

* Probleem verholpen waarbij sommige klanten een wit scherm zagen toen ze probeerden hun pagina in de Visual Experience Composer te bewerken.

**Bekende problemen**

De volgende bekende problemen zijn gemeld:

* Wanneer JavaScript uitschakelen is geselecteerd voor pagina A in een activiteit met meerdere pagina&#39;s, wordt JavaScript overal uitgeschakeld, ook al is JavaScript uitschakelen niet geselecteerd voor andere pagina&#39;s.
* Probleem met voorbeeld-URL&#39;s voor ervaringen met omleiding. Als tijdelijke oplossing klikt u in de Experience Composer op **[!UICONTROL Configure]** kiest u **[!UICONTROL Multiple Audiences]** en toevoegen **[!UICONTROL All visitors]** als het enige publiek. Sla je activiteit verder op. Dit verandert niets aan de levering van uw activiteit, maar staat voorproef toe om te werken. Dit zal worden vastgesteld in de release van Adobe Target in juli.

* De documentatie toont het verwachte gedrag voor Redirect URL checkbox. Vanwege een bug wordt het selectievakje echter niet standaard ingeschakeld weergegeven. Dit gebrek zal spoedig worden opgelost.

   Als u deze optie wilt controleren in een bestaande activiteit met een omleidingsvoorstel, gebruikt u de volgende tijdelijke oplossing:

   1. Open het pop-upvenster Omleiden naar URL.
   1. Wijzig de URL in een dummy-URL en sla deze op.
   1. Wijzig de dummy-URL opnieuw in de verwachte omleiding van de campagne-URL.
   1. Schakel de optie Inclusief huidige queryparameters in en sla deze op.

   Als u de optie controleert terwijl het creëren van een nieuwe omleidingsaanbieding, kunt u uw vraagparameters verwachten om in redirection worden omvat.

   Voor oudere activiteiten, als deze optie in ervaringscomposer van uw activiteit wordt gecontroleerd, betekent het uw redirection de vraagparameters zal omvatten. Als het niet wordt gecontroleerd, zullen de huidige vraagparameters niet in redirection worden omvat.

### Adobe [!DNL Target] Standard/Premium 16.5.1 (19 mei 2016) {#section_406CE09317994F55A26C2FDB77C77FEA}

De Adobe Target Standard/Premium 16.5.1-release (19 mei 2016) bevat de volgende functies en verbeteringen:

<table id="table_DDC5356FD6B8443EAA6EB81C03ADF73A"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Functie </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Ervaar versies </td> 
   <td colname="col2"> <p>Versies die gericht zijn op verschillende doelgroepen kunnen nu worden opgezet binnen de ervaringen in A/B-activiteiten. </p> <p>Zie <a href="/help/main/c-activities/t-test-ab/t-test-create-ab/target-experience-to-multiple-audiences.md#task_0138112E283A4A5B9F8AB9AAF2FBC2FF" format="dita" scope="local"> Een ervaring voor meerdere doelgroepen </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> URL's voor kwaliteitscontrole/voorvertoning </td> 
   <td colname="col2"> <p>Voorbeeld-URL's zijn nu beschikbaar voor de op formulieren gebaseerde ervaringscomposer. </p> <p>Zie <a href="/help/main/c-activities/t-automated-personalization/experience-preview.md#task_586C6655A6FD4AF08F5678FC3F481EFC" format="dita" scope="local"> Ervaring-URL's weergeven </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> Aangepaste Recommendations-algoritmen </td> 
   <td colname="col2"> <p>Aangepaste algoritme-toewijzingen kunnen worden geüpload in een CSV-bestand. Het is niet meer nodig om de op XML gebaseerde API te gebruiken. </p> <p>Zie <a href="/help/main/c-recommendations/c-algorithms/recommendations-csv.md#task_1BBA49883E794670A09F0ABE1B3F4288" format="dita" scope="local"> Aangepaste criteria uploaden </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Analyses voor doel: Analysescherm </td> 
   <td colname="col2"> <p>Voor een correcte rapportering moet u een volgserver opgeven wanneer u activiteiten maakt of bewerkt die Analytics for Target (A4T) gebruiken. Bestaande activiteiten worden uitgevoerd met de huidige instellingen. </p> <p>Zie <a href="/help/main/c-integrating-target-with-mac/a4t/analytics-tracking-server.md#task_72077BA7E93C4A65A715A18F32228823" format="dita" scope="local"> Een Analytics Tracking Server gebruiken </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Nieuwe instructievideo's </td> 
   <td colname="col2"> <p>De volgende instructievideo's zijn toegevoegd aan de Help: </p> <p> 
     <ul id="ul_47BAE946E764404497B7D81EE4C5D076"> 
      <li id="li_E16E50F94D3748E2985FB78F75140626">DTM gebruiken om parameters aan globale mbox over te gaan </li> 
      <li id="li_A8CCDE3EFF25430580E6C372000CF964">DTM gebruiken om Target te implementeren </li> 
      <li id="li_8897F7B5930B448D87274CEDFCC75AE4">Een multivariatietest instellen </li> 
      <li id="li_2573DF52CE974ED0AF9EA433C97BC4C0">Een A/B-activiteit maken </li> 
      <li id="li_52F28040D54D43E787B763E6AA998614">Werken met activiteitstypen </li> 
      <li id="li_577C8DDEB4CE429CA3C14BE5655F6E11">Instellingen voor activiteit configureren </li> 
      <li id="li_2F7FCA657FD04E02ADD6E6964A8EA1F0">Een activiteit als doel instellen </li> 
      <li id="li_A08B8AFF48764D1B9EA706977F72AA66">Soorten publiek maken </li> 
      <li id="li_493CDC3BEA5F4EA0821B971579177E03">Soorten publiek gebruiken </li> 
      <li id="li_19045C86E1524649B56F82416934EF13">De inhoudsbibliotheek gebruiken </li> 
      <li id="li_8E89F3691A6F4400A2DFDFE5186DFA83">Profielscripts gebruiken </li> 
      <li id="li_2EBB2B61BFA24F5FB858C0551AB20F70">Accountvoorkeuren instellen </li> 
      <li id="li_E1886818C7BF4F36B07EC293F1A45911">De modus Visual Experience Composer </li>  
      <li id="li_A87B876298344B2987BDC5FFD5580EC0">Doelgebruikers maken en beheren </li> 
      <li id="li_F90E1083444E4DBAA8C406AC293C0FD6">Metingen voor succes instellen </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Verbeteringen in de gebruikersinterface </td> 
   <td colname="col2"> <p>Er zijn verbeteringen aangebracht in de gebruikersinterface van Visual Experience Composer en Recommendations. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> Recommendations CSV-download </td> 
   <td colname="col2"> <p>CSV-downloads hebben nu een regel voor alle omgevingen, inclusief omgevingen die geen aanbevelingen voor entiteiten hebben (bijvoorbeeld: 
     <code>
       # environment: 1724 
     </code>). </p> </td> 
  </tr> 
 </tbody> 
</table>

**Verbeteringen**

Verbeteringen om het A4T-inrichtingsproces te verbeteren.

**Bekende problemen**

De volgende bekende problemen zijn gemeld:

* Wanneer JavaScript uitschakelen is geselecteerd voor pagina A in een activiteit met meerdere pagina&#39;s, wordt JavaScript overal uitgeschakeld, ook al is JavaScript uitschakelen niet geselecteerd voor andere pagina&#39;s.
* Probleem met voorbeeld-URL&#39;s voor ervaringen met omleiding. Als tijdelijke oplossing klikt u in de Experience Composer op **[!UICONTROL Configure]** kiest u **[!UICONTROL Multiple Audiences]** en toevoegen **[!UICONTROL All visitors]** als het enige publiek. Sla je activiteit verder op. Dit verandert niets aan de levering van uw activiteit, maar staat voorproef toe om te werken. Dit zal worden vastgesteld in de release van Adobe Target in juli.

### Nieuw [!DNL Target] Implementatiebibliotheek, 0.js 0.8.0 (5 mei 2016) {#section_6A44C277E82D409AB6DCD0901F43794A}

at.js is een nieuwe implementatiebibliotheek voor Doel die voor zowel typische implementaties van het Web als enig-paginatoepassingen wordt ontworpen.

Onder andere voordelen, verbetert at.js de tijden van de paginalading voor de implementaties van het Web, verbetert veiligheid, en verstrekt betere implementatieopties voor single-page toepassingen.

at.js bevat de componenten die in target.js inbegrepen waren, zodat is er niet meer een vraag aan target.js.

Houd rekening met het volgende wanneer u at.js implementeert:

* Omleiding van composer voor visuele ervaring werkt niet.
* Internet Explorer-versies ouder dan 8 worden niet ondersteund.
* Asynchrone implementatie betekent dat verouderde integratie, zoals de insteekmodule Testen en Doel naar SiteCatalyst, mogelijk niet werkt.
* Alle aanroepen naar Target worden uitgevoerd via XMLHTTPRequest en de inhoud wordt geretourneerd via JSON.

### Adobe [!DNL Target] Standard/Premium 16.4.1 Fix (5 mei 2016) {#section_70552F61E83140C7B4D2A245198B630E}

* at.js v 0.8.0 is nu beschikbaar voor download van de interface van het Doel.
* Doel-API&#39;s gewijzigd. `applyOffer` nu vereist `mbox param [0]`.

   ```
   adobe.target.applyOffer({ 
       "mbox": "target-global-mbox", 
    "params": {"test": "true"}, 
       "selector": ".banner-text", 
       "offer": offer 
   });
   ```

### Adobe [!DNL Target] Standard/Premium 16.4.1 (21 april 2016) {#section_C968860FAB81485BA12BD588F4ECA401}

Deze release bevat de volgende functies en verbeteringen:

<table id="table_162CC5A0DB324B38A8A4252A18976686"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Functie </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Verbeteringen in gebruikersinterface </td> 
   <td colname="col2"> <p>De gebruikersinterface is aanzienlijk gewijzigd in deze release. De belangrijkste wijzigingen zijn: </p> <p> 
     <ul id="ul_28F382C60ADE43F5A3A4BD0CD5A5CE52"> 
      <li id="li_C47240826E5844D6843314F453F042FC">Navigatie is van links naar boven verplaatst </li> 
      <li id="li_3BB03504E98C40CC85583DCD9A4CEA06">Verbeterde dialoogvensters </li> 
      <li id="li_AE71506DF1E748A788C40E1F09951732">Verbeterde stroom voor het maken van activiteiten </li> 
     </ul> </p> <p>De manier waarop Experience Cloud-oplossingen, inclusief Target, worden geselecteerd, is ook gewijzigd. Klik op het menupictogram voor toegang tot Experience Cloud-oplossingen en -services: </p> <p> <img src="assets/menu-shell-400.png" id="image_6E9323E0EBEA41B1A7319D6BCC43E769" width="400" height="140" /> </p> <p>Voor meer informatie over de toegang tot van Doel en het maken van Doel uw standaardpagina nadat het programma openen aan de Experience Cloud, zie <a href="/help/main/c-intro/target-access-from-mac.md#task_5467C72DAFCB4BB583762CAAFC00A5CF" format="dita" scope="local"> Toegangsdoel van de Adobe Experience Cloud </a>. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> Opnameregels kunnen worden uitgeschakeld voor aanbevelingen voor back-ups </td> 
   <td colname="col2"> <p>Wanneer de reserveaanbevelingen worden toegelaten, kunt u verkiezen om integratieregels op uw reserveaanbevelingen niet toe te passen. . </p>  </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> Recommendations: Nieuwe mogelijkheden voor foutopsporing in tekstgebied via <span class="codeph"> mboxTrace </span> </td> 
   <td colname="col2"> <p>Toevoegen <span class="codeph"> &amp;mboxTrace </span> op een URL vervangt aanbevelingen op die pagina met het zuiveren details, met inbegrip van informatie over gediende aanbevelingen, criteria, ontwerp, uitsluitingen, inbegrepen, bediende reserveaanbevelingen, en meer. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> Recommendations API: Een CSV uploaden voor de aangepaste criteria </td> 
   <td colname="col2"> <p>U kunt een CSV voor de Aangepaste Criteria via API uploaden. </p> <p>Deze mogelijkheid wordt in een komende release toegevoegd aan de gebruikersinterface van Target Premium. </p>  </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> Recommendations API: Nieuwe ontwerp-API's </td> 
   <td colname="col2"> <p>Met de nieuwe ontwerp-API's kunt u uw Recommendations-ontwerpen beheren via de API. </p>  </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> AP: Metrische gegevens voor afhankelijk succes </td> 
   <td colname="col2"> Automated Personalization ondersteunt nu de mogelijkheid om een succesmetrische waarde te beperken tot alleen tellen als al aan een eerdere succesmaatstaf is voldaan. <p>Zie voor meer informatie <a href="/help/main/c-activities/r-success-metrics/success-metrics.md#reference_D011575C85DA48E989A244593D9B9924" format="dita" scope="local"> Succeswaarden </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> AP: Rapporten overzicht downloaden </td> 
   <td colname="col2"> De downloadoptie staat nu gebruikers toe om summiere mening (d.w.z. het vergelijken van Controle en Geautomatiseerd verkeer) te downloaden zoals die door alle beschikbare succesmetriek wordt verdeeld. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Kenmerken van klanten kunnen als tokens worden gebruikt in aanbiedingen </td> 
   <td colname="col2"> <p>Voorheen kon in profielscripts naar klantkenmerken worden verwezen, opgemaakt als <span class="codeph"> crs.get('&lt; <span class="varname"> Naam gegevensbron </span>&gt;.&lt; <span class="varname"> Kenmerknaam </span>&gt;') </span>. </p> <p>De kenmerken zijn nu beschikbaar als tokens in profielscripts en rechtstreeks in aanbiedingen zonder eerst een profielscript te hoeven schrijven. De token moet de volgende vorm hebben: <span class="codeph"> $crs. <span class="varname"> datasourceName </span>. <span class="varname"> attributeName </span> </span>. </p> <p>Zie <a href="/help/main/c-target/c-visitor-profile/variables-profiles-parameters-methods.md#section_62B4821EB6564FF4A14159A837AD4EDB" format="dita" scope="local"> CRS Tokens </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Verbetering aangepaste code </td> 
   <td colname="col2"> De aangepaste code kan nu de JavaScript-code in het dialoogvenster <span class="codeph"> &lt;head&gt; </span> tag. De uitvoering van code wacht niet langer op de <span class="codeph"> &lt;body&gt; </span> -tag aanwezig in DOM. Eerder was de kiezer het eerste element in de <span class="codeph"> &lt;body&gt; </span> tag. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Nieuwe instructievideo's </td> 
   <td colname="col2"> Instructievideo's zijn toegevoegd aan de Help. U kunt momenteel video's weergeven over de <a href="/help/main/c-experiences/experiences.md#concept_A2E10F6AFB3D4AEAB6951EE14688848D" format="dita" scope="local"> Visual Experience Composer en Form-Based Experience Composer </a>. De komende weken worden meer video's toegevoegd. </td> 
  </tr> 
 </tbody> 
</table>

**Oplossingen**

Deze release bevat de volgende oplossingen:

* De kwestie die door Chrome versie 48 wordt geïntroduceerd die Visual Experience Composer ertoe bracht om verkeerd in Chrome te functioneren is opgelost. Werk een update naar Chrome versie 50 uit om van deze correctie te profiteren.

**Bekende problemen**

De volgende bekende problemen zijn gemeld:

* Wanneer JavaScript uitschakelen is geselecteerd voor pagina A in een activiteit met meerdere pagina&#39;s, wordt JavaScript overal uitgeschakeld, ook al is JavaScript uitschakelen niet geselecteerd voor andere pagina&#39;s.

### Adobe [!DNL Target] Standard/Premium 16.3.1 (15 maart 2016) {#section_A5A9B03A5CCD4213AD656BE722B5FF67}

Deze release bevat de volgende functies en verbeteringen:

<table id="table_F2A89DF1EAB443B4B4C7E0BC6118384B"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Functie </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Eerste weergave: </p> <p>Nieuwe doelimplementatiebibliotheek, at.js </p> </td> 
   <td colname="col2"> <p> <p>Opmerking: Dit "First Look"-aanbod is beschikbaar via API-download. Het zal via de interface van het Doel in een aanstaande versie beschikbaar zijn. In de tussentijd kunt u de bibliotheek at.js downloaden, deze in uw omgeving testen en deze implementeren in de implementatie van het productiedoel. </p> </p> <p> at.js is een nieuwe implementatiebibliotheek voor Doel die voor zowel typische implementaties van het Web als enig-paginatoepassingen wordt ontworpen. </p></p> <p>Onder andere voordelen, verbetert at.js de tijden van de paginalading voor de implementaties van het Web, verbetert veiligheid, en verstrekt betere implementatieopties voor single-page toepassingen. </p> <p>at.js bevat de componenten die in target.js inbegrepen waren, zodat is er niet meer een vraag aan target.js. </p> <p>Houd rekening met het volgende wanneer u at.js implementeert: </p> <p> 
     <ul id="ul_8C50C669AA7B4464A5FDECFCFD8662ED"> 
      <li id="li_6065B208480D46178055B40A2654E0C6">Omleiding van composer voor visuele ervaring werkt niet. </li> 
      <li id="li_A2FABD3C21994511A45DED84283E526E">Internet Explorer-versies ouder dan 8 worden niet ondersteund. </li> 
      <li id="li_04499B391F784B89B09A1D6329B1C790">Asynchrone implementatie betekent dat verouderde integratie, zoals de insteekmodule Testen en Doel naar SiteCatalyst, mogelijk niet werkt. </li>  
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Metrische gegevens voor afhankelijk succes </td> 
   <td colname="col2"> <p>Deze eigenschappen verstrekken de optie per succes metrisch om iemand te tellen zoals het bereiken van metrisch succes slechts als zij eerder een verschillend succes metrisch hebben bereikt. </p> <p> Een test kan bijvoorbeeld de hoofdafbeelding op de startpagina veranderen. De markeerteken wil mogelijk alleen conversies tellen voor mensen die op de hoofdafbeelding hebben geklikt. De markator kan dus een succesmaatstaf instellen voor "geklikt op een homepage held" en een andere maatstaf voor aankoop. Vervolgens kan de markeerteken een regel toevoegen op de metrische waarde voor "kopen" om ervoor te zorgen dat bezoekers eerst de succesmaatstaf "geklikt op de held van de homepage" hebben bereikt. </p> <p> <p>Opmerking: Als het publiek dat zich op een plaats in succes metrisch richt wordt geplaatst, wordt deze eigenschap niet gesteund voor die metrisch. </p> </p> <p> De afhankelijke Metriek van het Succes wordt slechts gesteund in AB, XT, en activiteiten MVT. Automated Personalization- en Recommendations-ondersteuning is later beschikbaar. </p> <p>Zie voor meer informatie <a href="/help/main/c-activities/r-success-metrics/success-metrics.md#reference_D011575C85DA48E989A244593D9B9924" format="dita" scope="local"> Succeswaarden </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Verbeteringen in de bruikbaarheid automatisch toewijzen </td> 
   <td colname="col2"> <p>Nadat het model voor een auto-Wijs activiteit klaar is, worden de volgende verrichtingen van UI niet toegestaan: </p> <p> 
     <ul id="ul_52B790B2B0D746769A3471E09CE1A122"> 
      <li id="li_B9F0FFF019CE4CB697F5D0B60061DC27">De modus "Verkeerstoewijzing" omzetten in "Handmatig" </li> 
      <li id="li_C271B0BE4C5C4B06BB21703239E7B061">De rapportbron wijzigen van "Adobe Target" in "Analytics" en omgekeerd </li> 
      <li id="li_E023DDA7ED9142B58D54F42904ADC994">Het metrische type van het doel wijzigen </li> 
      <li id="li_619F4765CEEC48E0A45E1821C282A082">Opties wijzigen in het deelvenster Geavanceerde instellingen </li> 
     </ul> </p> <p>Zie <a href="/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md#concept_A1407678796B4C569E94CBA8A9F7F5D4" format="dita" scope="local"> Automatische verkeerstoewijzing </a> voor documentatie over Automatisch toewijzen. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Bekende problemen**

De volgende bekende problemen zijn gemeld:

* Wanneer JavaScript uitschakelen is geselecteerd voor pagina A in een activiteit met meerdere pagina&#39;s, wordt JavaScript overal uitgeschakeld, ook al is JavaScript uitschakelen niet geselecteerd voor andere pagina&#39;s.
* Sommige interfaceproblemen kunnen zich voordoen in Internet Explorer 10, inclusief schermflikkering en mogelijke vertraging.
* De update van Chrome versie 48 introduceerde een kwestie die de Visuele Composer van de Ervaring veroorzaakt om verkeerd in Chrome te functioneren. Google werkt aan een oplossing. Zie voor meer informatie [https://code.google.com/p/chromium/issues/detail?id=582603](https://code.google.com/p/chromium/issues/detail?id=582603). U kunt dit probleem als volgt oplossen:

   * Gebruik Firefox of Internet Explorer.
   * De Enhanced Experience Composer inschakelen, die kan worden geconfigureerd vanuit de **[!UICONTROL Administration]** > **[!UICONTROL Visual Experience Composer]** tab.

### Adobe [!DNL Target] Standard/Premium 16.2.1 (18 februari 2016) {#section_47E5CEE2EED24CB3B71D7457673F3200}

Deze release bevat de volgende functies en verbeteringen:

| Functie | Beschrijving |
|---|---|
| Doelstelling activiteit volgens percentage. | U kunt nu items beperken tot [A/B](/help/main/c-activities/t-test-ab/t-test-create-ab/test-create-ab.md) en [multivariëren](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/create-multivariate-test.md#task_BF870FA60A8245AB8F0B775BE32EA710) activiteiten aan een percentage bezoekers of publieksleden. U kunt bijvoorbeeld items beperken tot 50% van alle bezoekers of 45% van uw &quot;Californische&quot; publiek. |
| Ondersteuning voor inkomsten, bestellingen en betrokkenheid bij automatisch toewijzen | U kunt nu de metriek van de Inkomsten (RPV), van Orden, en van de Betrokkenheid als doelstellingen voor A/B activiteiten kiezen met auto-Toewijzing geselecteerd. Eerder werden alleen conversiemetriek ondersteund. Zie [Automatische verkeerstoewijzing](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md#concept_A1407678796B4C569E94CBA8A9F7F5D4). |
| Filteren op bron | U kunt de lijst Activiteiten nu filteren op de bron waar de activiteit is gemaakt. De keuze is Adobe Target en Adobe Experience Manager. Zie [Activiteiten](/help/main/c-activities/activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03). |
| Verbeterde Automated Personalization-prestaties | Automated Personalization is opnieuw ontworpen om beter te presteren met een groot aantal aanbod-/locatiecombinaties. |

**Bekende problemen**

De volgende bekende problemen zijn gemeld:

* Wanneer JavaScript uitschakelen is geselecteerd voor pagina A in een activiteit met meerdere pagina&#39;s, wordt JavaScript overal uitgeschakeld, ook al is JavaScript uitschakelen niet geselecteerd voor andere pagina&#39;s.
* Sommige interfaceproblemen kunnen zich voordoen in Internet Explorer 10, inclusief schermflikkering en mogelijke vertraging.
* De update van Chrome versie 48 introduceerde een kwestie die de Visuele Composer van de Ervaring veroorzaakt om verkeerd in Chrome te functioneren. Google werkt aan een oplossing. Zie voor meer informatie [https://code.google.com/p/chromium/issues/detail?id=582603](https://code.google.com/p/chromium/issues/detail?id=582603). U kunt dit probleem als volgt oplossen:

   * Gebruik Firefox of Internet Explorer.
   * De Enhanced Experience Composer inschakelen, die kan worden geconfigureerd vanuit de **[!UICONTROL Administration]** > **[!UICONTROL Visual Experience Composer]** tab.

### Adobe [!DNL Target] Standard/Premium 16.1.1 (28 januari 2016) {#section_8BF7705B452C449F961AEFC568A0778C}

Deze release bevat de volgende functies en verbeteringen:

<table id="table_8525ECC9B6D0435ABEF8C27F747B7A0C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Functie </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Verbeteringen in de gebruikersinterface. </td> 
   <td colname="col2"> <p>De lijst met activiteiten en het ontwerp van de lijst met doelgroepen zijn verbeterd, net als de functie voor zoeken en sorteren. De extra veranderingen van het gebruikersinterface zullen in volgende versies worden omvat. </p> <p>Zie <a href="/help/main/c-activities/activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03" format="dita" scope="local"> Activiteiten </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> "Superpubliek" </td> 
   <td colname="col2"> <p>Gebruik geneste AND/OR-logica bij het configureren van soorten publiek. </p> <p>Zie <a href="/help/main/c-target/c-audiences/create-audience.md#task_E18BD77A9A8F4ED0AC50569F94556558" format="dita" scope="local"> Een publiek maken </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Hostgroepen selecteren in rapporten </td> 
   <td colname="col2"> <p>De groepen van de gastheer zijn beschikbaar in rapporten. </p> <p> <p>Opmerking: Deze optie is niet beschikbaar voor Automated Personalization. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Ondersteuning voor Internet Explorer 11 </td> 
   <td colname="col2"> <p>Internet Explorer 11 wordt nu ondersteund in de doelinterface. </p> <p>Zie <a href="https://developer.adobe.com/target/before-implement/supported-browsers/" format="dita" scope="local"> Ondersteunde browsers </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Het Interval van het Vertrouwen van de mening in de rapporten van het Doel voor ononderbroken variabelen </td> 
   <td colname="col2"> <p>Toon de Waaier van het Interval van het Vertrouwen voor het opbrengstmetrische type (RPV, AOV, Verkoop, Orders), en voor betrokkenheidsmetriek. </p> <p>Bijvoorbeeld, als RPV = 200.00 en CI Waaier = 50.00, dan zou dit voor RPV moeten worden getoond: 200,00 +/- 50,00 </p> <p>Deze wijziging is van toepassing op tests voor A/B, Experience Targeting en Multivariate. </p> <p>Zie <a href="/help/main/c-reports/statistical-methodology/statistical-calculations.md" format="dita" scope="local"> Vertrouwensniveau en betrouwbaarheidsinterval </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Verbetering van URL-regels voor Visual Experience Composer </td> 
   <td colname="col2"> <p>Eerder vormden de URL-sjabloonregels in de Visual Experience Composer een OF-voorwaarde met de Pagina-URL. Nu kunt u AND of OR kiezen wanneer het specificeren van veelvoudige URLs. OR is de standaardwaarde. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p class="premium">Recommendations: </p> <p>Wijziging in algemene mbox-leveringscodering </p> </td> 
   <td colname="col2"> <p>Wanneer u een ontwerp maakt, is het nu de standaardinstelling om een HTML-ontwerp om te zetten in een <span class="codeph"> &lt;div&gt; </span> element. </p> <p>Voor informatie over het maken van een ontwerp raadpleegt u <a href="/help/main/c-recommendations/c-design-overview/create-design.md#task_CC5BD28C364742218C1ACAF0D45E0E14" format="dita" scope="local"> Een ontwerp maken </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>LTV (Life Time Value) machine learningversterkingtechniek </p> </td> 
   <td colname="col2"> <p>Dit nieuwe algoritme concentreert zich op lange termijn omzetting over vele zittingen in plaats van zich op het verbeteren van omzetting enkel in deze zitting. Deze techniek is geschikt voor sites met veel terugkerende bezoekers, omdat deze de totale inkomsten optimaliseert voor de volledige interactie met de bezoeker. </p> <p>Zie <a href="/help/main/c-activities/t-automated-personalization/automated-personalization.md#task_8AAF837796D74CF893CA2F88BA1491C9" format="dita" scope="local"> Automated Personalization </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Verbetering: Doelgerichtheid toestaan op hash-fragmenten (#) </p> </td> 
   <td colname="col2"> <p>U kunt nu richten op het gedeelte van een URL dat volgt op een hash (#). </p> <p>Zie <a href="/help/main/c-experiences/c-visual-experience-composer/temtest.md#task_2539D51A18044F82B0D9895636546781" format="dita" scope="local"> Dezelfde ervaring opnemen op vergelijkbare pagina's </a> en andere relevante onderwerpen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Rapport met succesmetriek downloaden </p> </td> 
   <td colname="col2"> <p> Download één enkel csv- dossier met al succes metrisch vermeld, in plaats van een rapport dat slechts het definitieve activiteitendoel had. </p> <p>Zie <a href="/help/main/c-reports/reports.md" format="dita" scope="local"> Rapporten </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Oplossingen**

Deze release bevat de volgende oplossingen:

* Probleem opgelost waarbij alle op AEM gebaseerde activiteiten als Experience Targeting (XT)-activiteiten werden veroorzaakt. AEM gebruikt nu de juiste activiteitstypen voor A/B- en XT-activiteiten.
* Verwijderd een optie om niet-omzettingsmetriek als doel in nieuwe Auto Toegewezen activiteiten te gebruiken. Deze beperking wordt in een volgende release opgeheven.
* Probleem verholpen waarbij een profielscript dat in Target Classic is gemaakt, niet kon worden verwijderd uit Target Standard.
* Probleem verholpen waarbij een Recommendations-sjabloon anders dan HTML in een sjabloon werd geplaatst `<div>` -element bij gebruik in een formuliergebaseerde workflow.
* Probleem verholpen waarbij botsingsberekeningen de tijd verlieten met een groot aantal activiteiten.
* Probleem verholpen waarbij de CSV-download het rapport Summary in plaats van het rapport Success Metrics weergaf.
* Het pop-upbericht &#39;Unieke id&#39; is verwijderd dat soms werd weergegeven tijdens het bewerken van elementen.

**Bekende problemen**

De volgende bekende problemen zijn gemeld:

* Wanneer JavaScript uitschakelen is ingeschakeld voor pageA in een activiteit met meerdere pagina&#39;s, blijft JavaScript ingeschakeld voor alle pagina&#39;s, maar blijft de functionaliteit uitgeschakeld.
* Sommige interfaceproblemen kunnen zich voordoen in Internet Explorer 10, inclusief schermflikkering en mogelijke vertraging.
* De update van Chrome versie 48 introduceerde een kwestie die de Visuele Composer van de Ervaring veroorzaakt om verkeerd in Chrome te functioneren. Google werkt aan een oplossing. Zie voor meer informatie [https://code.google.com/p/chromium/issues/detail?id=582603](https://code.google.com/p/chromium/issues/detail?id=582603). U kunt dit probleem als volgt oplossen:

   * Gebruik Firefox of Internet Explorer.
   * De Enhanced Experience Composer inschakelen, die kan worden geconfigureerd vanuit de **[!UICONTROL Administration]** > **[!UICONTROL Visual Experience Composer]** tab.

## Uitzettingen 2015 {#reference_8E940F500A374F9FBCD68CDE9E7E1A00}

### Adobe [!DNL Target] Standard/Premium 15.10.1 (2 november 2015) {#section_B5135D75FA0D42A1A3C2711CA3A1B812}

<!-- 

target/r_release-notes-2015.xml

 -->

Deze release bevat de volgende functies en verbeteringen:

<table id="table_EE13D9B959DA4FB0AD6BC03FBF78AEF6"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Functie </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Automatisch toewijzen in A/B-tests </p> </td> 
   <td colname="col2"> <p> U hebt nu de optie om automatisch verkeer toe te wijzen om de algemene campagnelift te verhogen en het winnen van ervaringen sneller te ontdekken. Dit algoritme verhoogt de algemene campagneprestaties terwijl het handhaven van de integriteit van een A/B test. </p> <p>Het algoritme steunt op gemeten prestaties (b.v. omzettingspercentage) en betrouwbaarheidsintervallen om een verkeersverdeling te veroorzaken die tot tweemaal per uur wordt veranderd. </p> <p>Belangrijkste voordelen </p> <p> 
     <ul id="ul_A41C74C0C7C844F3A923CD6EA5D5D952"> 
      <li id="li_86D3C6A4993F4DC0907BF42986E6CCD1">Behoudt de integriteit van een A/B-test door ervoor te zorgen dat bezoekers in dezelfde ervaring blijven, zoals ze doen bij een handmatige A/B-test </li> 
      <li id="li_B849EB2709F84831A1B7A4F312EAFA7E">Vindt een statistisch significante winnaar sneller dan een handmatige A/B test </li> 
      <li id="li_3F258C6DEB7245E2924115C5628BC3C6">Biedt een hogere gemiddelde campagnelift dan een handmatige A/B-test </li> 
      <li id="li_C9E82388B93E4A298000984B69CBAEDE">Hiermee kunt u op elk gewenst moment overschakelen op een handtest </li> 
     </ul> </p> <p>Zie <a href="/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md#concept_A1407678796B4C569E94CBA8A9F7F5D4" format="dita" scope="local"> Automatische verkeerstoewijzing </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Klantkenmerken </p> </td> 
   <td colname="col2"> <p> Upload gegevens van één partij, genoemd Kenmerken van de Klant, gebruikend de de kerndienst van de Experience Cloud en kies attributen om aan Doel te delen. Deze functionaliteit is in maart voor Analytics gestart en kan nu rechtstreeks met Target worden geïntegreerd. </p> <p> U kunt bijvoorbeeld klantgegevens zoals lidmaatschapsstatus (goud, zilver, enz.), koopgeschiedenis, favoriete bestemming, lokale opslag gebruiken, enzovoort in uw CRM- of eCommerce/POS-systeem. Nu kunt u die gegevens uploaden naar Experience Cloud. Nadat de gebruiker op uw site heeft geverifieerd, kunnen de gegevens door Target worden afgestemd op hun webgedrag. </p> <p>Zie <a href="https://experienceleague.adobe.com/docs/core-services/interface/customer-attributes/attributes.html" format="https" scope="external"> Klantkenmerken </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Er zijn meerdere bedrijven beschikbaar wanneer u Analytics selecteert als rapportagebron voor Target. </p> </td> 
   <td colname="col2"> <p>Wanneer u Analytics selecteert als de rapporteringsbron voor Target, selecteert u een Analytics-rapportsuite die doelactiviteitgegevens ontvangt. Hiervoor kiest u eerst een van de Analytics-bedrijven waaraan uw account is gekoppeld en selecteert u vervolgens de juiste rapportsuite voor de activiteit. Alleen rapportsuites die zijn ingericht voor verbinding met Adobe Target, zijn beschikbaar voor selectie. Als u de rapportsuite(s) die u verwacht niet ziet, meldt u zich eerst af en meldt u zich opnieuw aan bij de Adobe Experience Cloud om het opnieuw te proberen. Neem contact op met de klantenservice als de rapportsuite nog steeds ontbreekt in de lijst. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Nieuwe ingebouwde opties voor het maken van publiek </p> </td> 
   <td colname="col2"> <p>Er zijn nieuwe ingebouwde publieksopties: </p> <p> 
     <ul id="ul_16E7B53E324B4FB79E1B1E97A1CE65AC"> 
      <li id="li_60B55A81119E48FE83639B9740A2FD21">Doelbezoekers op basis van de taal die ze in hun browser gebruiken. Dit is nauwkeuriger dan geo-based taalgerichte richten. </li> 
      <li id="li_84CAAE7E02CA48FA9C7C00C0415046B6">De bezoekers van het doel die op browser versie worden gebaseerd, niet alleen welke browser wordt gebruikt. </li> 
      <li id="li_AAF8170CAF4C45BB965D1A9A4E9204D5">U kunt nu op meerdere browsers in plaats van op slechts één browser gericht zijn. </li> 
     </ul> </p> <p>Zie <a href="/help/main/c-target/c-audiences/c-target-rules/browser.md#concept_221D8EEF53CC45AEACEB17CF336A3658" format="dita" scope="local"> Browseropties </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p class="Premium">Recommendations </p> <p class="Premium">Exclusief aankopen in het verleden </p> </td> 
   <td colname="col2"> <p>Eerder aangeschafte objecten worden nu automatisch uitgesloten van de aanbevelingen van een bezoeker. Deze optie kan voor om het even welke criteria worden onbruikbaar gemaakt. </p> <p>Deze optie is nu ingeschakeld voor alle criteria buiten de box, inclusief de criteria die werden gebruikt in activiteiten die vóór deze release werden uitgevoerd. Als u eerdere aankopen niet wilt uitsluiten, moet u deze activiteiten bewerken. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p class="Premium">Recommendations </p> <p> Kenmerkweging </p> </td> 
   <td colname="col2"> <p> De rangorde in Recommendations is veranderd voor criteria. Deze wijziging is van invloed op bestaande Recommendations. </p> <p> Gebruik kenmerkweging om het algoritme te verschuiven. Marketers kunnen het algoritme beïnvloeden op basis van een belangrijke beschrijving of metagegevens over de inhoudscatalogus. Pas een hogere weging toe op deze onverkochte artikelen, zodat deze vaker in de aanbeveling worden weergegeven. Niet-verkochte objecten worden niet volledig uitgesloten, maar ze worden minder vaak weergegeven. Er kunnen meerdere wegingen worden toegepast op hetzelfde algoritme en de wegingen kunnen in de aanbeveling op gesplitst verkeer worden getest. </p> <p>Deze nieuwe gewichten zijn automatisch toegepast op alle activiteiten. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p class="Premium">Recommendations </p> <p>Tijd instellen voor Feed-verwerking </p> </td> 
   <td colname="col2"> <p>Geef de tijd op waarop u een feed wilt bijwerken. </p> <p>Zie <a href="/help/main/c-recommendations/c-products/feeds.md#task_C6CD9EA905744C2CA0BB8259BB74C867" format="dita" scope="local"> Feed maken </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p class="Premium">Recommendations </p> <p>Gebruik de lijst van het Gegeven om een Diervoeder te plaatsen om nooit te lopen </p> </td> 
   <td colname="col2"> <p>Stel in de lijst met feed een feed in die nooit moet worden uitgevoerd als u die feed niet wilt bijwerken. </p> <p>Zie <a href="/help/main/c-recommendations/c-products/feeds.md#task_C6CD9EA905744C2CA0BB8259BB74C867" format="dita" scope="local"> Feed maken </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p class="Premium">Recommendations </p> <p>Een nieuw type criteria instellen op basis van gelijkenis met inhoud </p> </td> 
   <td colname="col2"> <p>Een op item gebaseerde criteria die kunnen worden gebruikt voor: </p> <p> 
     <ul id="ul_86BDF2DE0FCE4665A2985D0C56E50A53"> 
      <li id="li_D83669F9019B431891E072C973B317D7">Huidige items met vergelijkbare kenmerken </li> 
      <li id="li_4E45848423F2450999C699C64E0EE9E2">Laatst gekocht item met vergelijkbare kenmerken </li> 
      <li id="li_901D4AAF7BE244FCB9277DC7EDD91E32">Aangepaste kenmerken die overeenkomen met een opgegeven entiteit.id en items met vergelijkbare kenmerken gebruiken </li> 
      <li id="li_49D52B0182F346E982C11A0C2DA50B4F">Laatst weergegeven item met vergelijkbare kenmerken </li> 
      <li id="li_2DBAF32476AC435EB57D08D96CB55683">Meest bekeken item met vergelijkbare kenmerken </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Nieuwe activiteitslijstfilters </td> 
   <td colname="col2"> <p>Er zijn verschillende filters toegevoegd om u te helpen de activiteiten weer te geven die u het interessantst vindt in de lijst Activiteiten. </p> <p>Zie <a href="/help/main/c-activities/activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03" format="dita" scope="local"> Activiteiten </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p class="Premium">Recommendations </p> <p>Verbetering: Configuratie van relevante criteria voor de industrie </p> </td> 
   <td colname="col2"> <p>Niet-relevante opties tijdens de installatie zijn verwijderd. In het verleden, waren sommige opstellingsopties voor sommige industrie verticale als, zoals Media, niet altijd relevant. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p class="Premium">Recommendations </p> <p>Nieuwe criteria voor Buiten-de-box </p> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_47E67312A04E414EB797F9AE2A1F7599"> 
      <li id="li_5EDF9006145B4498B2EAD95D642057C5">Meer video's als deze </li> 
      <li id="li_6A8DAACE7CD741D0BB766EBCB52BCD88">Meer artikelen als deze </li> 
      <li id="li_1B44AB35B045416B8D8B72C428750822">Meer inhoud als deze </li> 
      <li id="li_FEC84CCF3DF3444DAB39F4764DE897B0">Meer presentaties als deze </li> 
      <li id="li_5E874ACB5B004CACBDB4F8FF217BC593">Meer producten als deze </li> 
     </ul> </p> <p>Zie <a href="/help/main/c-recommendations/c-algorithms/algorithms.md" format="dita" scope="local"> Criteria </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Verbetering: Verbeterde rapportdetails die worden weergegeven wanneer u Analytics als rapportbron gebruikt. </td> 
   <td colname="col2"> <p>De details die door gebrek in een rapport van de Analyse wanneer het gebruiken van A4T worden getoond passen nu de details aan die in het rapport van het Doel worden getoond. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Oplossingen**

Deze release bevat de volgende oplossingen:

* Probleem verholpen in de globale composer voor ervaring dat het slepen van een hoek om het formaat van een aangepaste viewport te wijzigen, verhinderde.

**Bekende problemen**

De volgende bekende problemen zijn gemeld:

* Wanneer JavaScript uitschakelen is ingeschakeld voor pageA in een activiteit met meerdere pagina&#39;s, blijft JavaScript ingeschakeld voor alle pagina&#39;s, maar blijft de functionaliteit uitgeschakeld.

### Adobe [!DNL Target] Standard/Premium 15.9.1 (30 september 2015) {#section_A54204291A99476688E8C0BD8255F93C}

Deze release bevat de volgende functies en verbeteringen:

<table id="table_907A952F54084C2A9C61F10E2B7A7BFF"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Functie </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Mobiele webervaringscomposer </td> 
   <td colname="col2"> <p> Bekijk uw site zoals deze eruit ziet op verschillende mobiele apparaten en verschillende schermgrootten. Stel responsieve onderbrekingspunten voor sites eenmaal in en gebruik deze voor alle activiteiten om ervoor te zorgen dat uw optimalisatieactiviteiten er goed uitzien op alle apparaten die uw bezoekers gebruiken. </p> <p>Zie <a href="/help/main/c-experiences/c-visual-experience-composer/mobile-viewports.md#concept_8E45527C4ABC41D59AA3553BEDC76FA5" format="dita" scope="local"> Mobiele Viewports voor responsieve ervaringen </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Locatie waarop het maken van formuliergebaseerde activiteiten is gericht </td> 
   <td colname="col2"> <p> Pas het richten op uw mbox plaatsen toe om te beperken waar uw activiteit toont. </p> <p>Zie <a href="/help/main/c-experiences/form-experience-composer.md#task_FAC842A6535045B68B4C1AD3E657E56E" format="dita" scope="local"> Formuliergebaseerde Experience Composer </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Achtergrondkleur selecteren in Visual Experience Composer voor MVT- en Automated Personalization-activiteiten </td> 
   <td colname="col2"> <p>Met een kleurkiezer kunt u achtergrondkleuren instellen tijdens het bewerken van Automated Personalization- en multivariate-testactiviteiten. </p> <p>Deze functie was voorheen alleen beschikbaar voor activiteiten van A/B en Gericht op ervaring. </p> <p>Zie <a href="/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md#reference_3BD1BEEAFA584A749ED2D08F14732E81" format="dita" scope="local"> Opties voor composer visuele ervaring </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Rijke Tekst en HTML het uitgeven in Visual Experience Composer voor MVT en de activiteiten van Automated Personalization </td> 
   <td colname="col2"> <p> Tekst- en HTML-opmaak in een tekstverwerker-achtig venster bij het bewerken van Automated Personalization en Multivariate Test-activiteiten. </p> <p> Deze functie was voorheen alleen beschikbaar voor activiteiten van A/B en Gericht op ervaring. </p> <p>Deze handelingen bieden bewerkingsmogelijkheden met tekstopmaak door HTML-tags toe te voegen of stijlen toe te passen. Deze wijzigingen door de rijke tekstredacteur voor om het even welke actie kunnen in zijn bronmening worden gezien. Gebruikers kunnen op de knop HTML in de RTF-editor drukken om de bronweergave te bekijken. De stijlen die door de rijke redacteur worden toegevoegd kunnen zich met de stijlen van klantenwebsites mengen. In dit geval kunnen gebruikers naar de bronweergave gaan en de wijzigingen bewerken om deze uit te lijnen met de stijlen van hun websites. </p> <p>Zie <a href="/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md#reference_3BD1BEEAFA584A749ED2D08F14732E81" format="dita" scope="local"> Opties voor composer visuele ervaring </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p class="Premium">Recommendations </p> <p class="Premium">Formuliergebaseerde aanbevelingen </p> </td> 
   <td colname="col2"> <p> Aanbevelingsactiviteiten voor locaties buiten de site maken, zoals e-mails, consoles, kiosken, enz. </p> <p>Zie <a href="/help/main/c-experiences/form-experience-composer.md#task_FAC842A6535045B68B4C1AD3E657E56E" format="dita" scope="local"> Formuliergebaseerde Experience Composer </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p class="Premium">Recommendations </p> <p> Informatie weergeven over de sleutel in het ontwerp </p> </td> 
   <td colname="col2"> <p>Toon het belangrijkste item in uw Recommendations-ontwerp. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p class="Premium">Automated Personalization </p> <p>Conversierapport </p> </td> 
   <td colname="col2"> <p> Als het optimalisatiedoel omzettings metrisch is, dan toont het rapport van het Detail van de Aanbieding nu het effect van de hoogste voorspellende variabelen in lift en stijgende omzettingen. Dit verslag was pas eerder gebaseerd op inkomsten, zodat deze mogelijkheid ervoor zorgt dat activiteiten zonder inkomstengegevens nog steeds relevante en activeerbare inzichten produceren. </p> <p>Zie <a href="/help/main/c-reports/personalization-reports/reports-ap.md" format="dita" scope="local"> Automated Personalization-rapporten </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Adobe Campaign e-mailintegratie met Target Standard </td> 
   <td colname="col2"> <p> Eerder was het vereist om Target Classic te gebruiken voor het opzetten van een gerichte e-mailcampagne met Adobe Campaign. Met de release van twee nieuwe functies in Target Standard (op formulieren gebaseerde activiteiten maken en aanbiedingen omleiden) is het nu mogelijk om Target Standard te gebruiken om een doelgerichte e-mailcampagne met Adobe Campaign op te zetten.</p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> Aanbiedingen omleiden in op formulier gebaseerde activiteiten maken </td> 
   <td colname="col2"> <p> Ondersteuning voor de omleiding biedt functionaliteit van Target Classic die is toegevoegd in de formuliergebaseerde workflow voor het maken van activiteiten op basis van Target Standard. </p> <p>Zie <a href="/help/main/c-experiences/form-experience-composer.md#task_FAC842A6535045B68B4C1AD3E657E56E" format="dita" scope="local"> Formuliergebaseerde Experience Composer </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Verbetering: Ervaar URL's in activiteiten die geen onsite cookie meer gebruiken </td> 
   <td colname="col2"> <p> De ervaring URLs beschikbaar per activiteit is nu betrouwbaarder. Kopieer eenvoudig de URL's en deel deze met andere teamleden, zelfs als ze Adobe Target niet gebruiken. </p> <p> <p>Opmerking: Bijgewerkte ervaring URLs werkt slechts aan activiteiten die na 30 juli 2015 worden gecreeerd. Oudere activiteiten blijven gebruikmaken van de voorbeeldfunctionaliteit op basis van cookies. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Verbetering van de rapportage voor Analytics als rapportagebron voor Target </p> </td> 
   <td colname="col2"> <p> Klik om het volledige rapport Analytics rechtstreeks van de pagina van het activiteitenrapport te bekijken. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> Prestatieverbeteringen van de activiteitenlijst </td> 
   <td colname="col2"> <p>De laadtijd voor activiteiten in de lijst is aanzienlijk verbeterd. Zoeken en filteren gaat veel sneller, vooral wanneer de lijst veel activiteiten bevat. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Oplossingen**

Deze release bevat de volgende oplossingen:

* Probleem verholpen waardoor de doelrapportsuites niet konden worden weergegeven in de selector van de doelrapportsuite nadat deze was ingeschakeld voor Analytics for Target.
* Probleem verholpen waardoor het zoeken naar activiteiten via URL niet mogelijk was.

**Bekende problemen**

De volgende bekende problemen zijn gemeld:

* Wanneer JavaScript uitschakelen is ingeschakeld voor pageA in een activiteit met meerdere pagina&#39;s, blijft JavaScript ingeschakeld voor alle pagina&#39;s, maar blijft de functionaliteit uitgeschakeld.

### Adobe [!DNL Target] Standard/Premium 15.8.1 (20 augustus 2015) {#section_1C26CB72316A404DB655EBE655F5B8C1}

Het doel van deze versie is eigenschappariteit van het Klassieke Doel te verstrekken. De meest gebruikte eigenschappen van Doel Klassiek zijn nu beschikbaar in de Norm van het Doel.

Deze release bevat de volgende functies en verbeteringen:

<table id="table_DF5B434D639345B4ACE2467B8966A908"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Functie </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Profielscripts maken en bewerken </td> 
   <td colname="col2"> <p>Profielscripts voeren profielkenmerk 'catchers' uit op elke aanvraag van een box. Wanneer een mbox verzoek wordt ontvangen, stelt het Doel om het even welke relevante profielmanuscripten in werking, bepaalt welke activiteit zou moeten lopen, en toont inhoud die aan die activiteit en die ervaring aangewezen is, dan het succes van de activiteit volgt. Op deze manier kunt u informatie over het bezoek bijhouden, zoals de locatie, het tijdstip van de bezoeker, het aantal keren dat de bezoeker naar de site is geweest, als hij of zij voor en op de site heeft gekocht. Deze informatie wordt vervolgens toegevoegd aan het profiel van de bezoeker, zodat u de activiteiten van die bezoeker op uw site beter kunt bijhouden. </p> <p>Zie <a href="/help/main/c-target/c-visitor-profile/profile-parameters.md#concept_01A30B4762D64CD5946B3AA38DC8A201" format="dita" scope="local"> Profielkenmerken </a>. 
     <!--(Copy help from Classic)--> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Vertrouwensinterval voor binaire metriek </td> 
   <td colname="col2"> <p>De bijgewerkte rapporten die op doel-gebaseerde gegevens gebruiken tonen het betrouwbaarheidsinterval van de lift, in vergelijking met de controle. </p> <p>Zie <a href="/help/main/c-reports/statistical-methodology/statistical-calculations.md" format="dita" scope="local"> Vertrouwensniveau en betrouwbaarheidsinterval </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Gegevens exportactiviteitenrapport downloaden </td> 
   <td colname="col2"> <p>Download gegevens in de CSV-indeling, zodat u deze snel kunt importeren in Excel of andere programma's voor gegevensanalyse. Deze functie werkt voor A/B-, Experience Targeting- en Multivariate-activiteiten. </p> <p>Zie <a href="/help/main/c-reports/reports.md#section_3099BC87DCAE46A2B075E1FF5B6552A6" format="dita" scope="local"> Rapporten downloaden </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Rijke tekst en HTML-bewerking in Visual Experience Composer </td> 
   <td colname="col2"> <p>De het formatteren van de tekst opties zijn beschikbaar wanneer het uitgeven van tekst en HTML voor A/B en Ervaring gerichte activiteiten in de Composer van de Visuele Ervaring. U kunt een lettertype kiezen, een lettertypestijl selecteren, de tekstuitlijning wijzigen en andere standaardopties voor tekstopmaak opgeven. Wanneer u HTML wijzigt, kunt u schakelen tussen de codeweergave en de rijke bewerkingsweergave van de HTML. </p> <p>Zie <a href="/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md#reference_3BD1BEEAFA584A749ED2D08F14732E81" format="dita" scope="local"> Opties voor composer visuele ervaring </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Achtergrondkleur selecteren in Visual Experience Composer </td> 
   <td colname="col2"> <p>Met een kleurkiezer kunt u achtergrondkleuren instellen tijdens het bewerken van A/B en bij het uitvoeren van activiteiten in de Visual Experience Composer. Deze optie is niet beschikbaar als een achtergrondafbeelding is ingesteld. </p> <p>Zie <a href="/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md#reference_3BD1BEEAFA584A749ED2D08F14732E81" format="dita" scope="local"> Opties voor composer visuele ervaring </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Archiefactiviteit </td> 
   <td colname="col2"> <p>Een activiteit naar het archief verzenden. U kunt een gearchiveerde activiteit goedkeuren om het opnieuw actief te maken. Activiteiten in het archief worden niet standaard weergegeven in de lijst Activiteiten. </p> <p>Zie <a href="/help/main/c-activities/activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03" format="dita" scope="local"> Activiteiten </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p>Automated Personalization </p> <p>Aanbiedingsniveau </p> </td> 
   <td colname="col2"> <p>Biedt marketers de mogelijkheid om gerichte regels toe te passen op aanbiedingen in Automated Personalization. Hiermee kunt u uitsluiten dat bepaalde aanbiedingen aan een bepaalde groep personen worden getoond. </p> <p>Zie <a href="/help/main/c-activities/t-automated-personalization/ap-target-offers.md#task_F207ED7A41B84FD39BB6FCBFABF4B23E" format="dita" scope="local"> AP-doelaanbiedingen </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p>Recommendations Premium </p> <p>Aantal activiteiten weergeven die gebruikmaken van ontwerpen </p> </td> 
   <td colname="col2"> <p>In de ontwerpbibliotheek ziet u hoeveel actieve en inactieve activiteiten elk ontwerp gebruiken. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p>Recommendations Premium </p> <p>Aangepaste dynamische titelweergaven in ontwerp </p> </td> 
   <td colname="col2"> <p>Kies een titel die u wilt weergeven wanneer u een bepaald ontwerp gebruikt. Deze titel hoeft niet overeen te komen met de titel die aan bezoekers op de pagina wordt weergegeven. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p>Recommendations Premium </p> <p>API-token </p> </td> 
   <td colname="col2"> <p>U kunt uw client-API-token instellen vanuit Recommendations Premium. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> Verbetering: Veelgebruikte URL's </td> 
   <td colname="col2"> Wanneer u een URL voor een activiteit of een nieuwe pagina binnen een activiteit invoert, wordt in een menu de meest recente en meest gebruikte URL's weergegeven. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Nieuwe opties voor mobiele apparaten </td> 
   <td colname="col2"> <p>U kunt nu meerdere mobiele apparaten activeren zonder een profielscript te vereisen. </p> <p>Zie <a href="/help/main/c-target/c-audiences/c-target-rules/mobile.md#concept_2A794199DC1A4D349FFFBC7DCF1FEB89" format="dita" scope="local"> Mobiel </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

### Adobe [!DNL Target] Standard/Premium 15.7.1 (30 juli 2015) {#section_9C888BFD04A94DD58616D3F67D209CCC}

Deze release bevat de volgende functies en verbeteringen:

<table id="table_46FF5AF77D824ADC941B1E472234F05C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Functie </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Logboek voor wijziging van de activiteit </td> 
   <td colname="col2"> <p>Het veranderingslogboek maakt een lijst van veranderingen die aan een activiteit worden aangebracht. De actie en de gebruiker worden vermeld met een timestamp voor elke verandering. </p> <p>Zie <a href="/help/main/c-activities/change-log.md#task_D6F224E8CE8346699187D21CD9A2B4AB" format="dita" scope="local"> Activiteitenwijzigingslogboek </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Meerdere pagina's </td> 
   <td colname="col2"> <p>Met een activiteit van meerdere pagina's kunt u een artikel op meerdere pagina's maken, met een ontwerp dat specifiek is voor elke pagina. </p> <p>Je kunt bijvoorbeeld een voorstel voor gratis verzending testen met aankopen boven een bepaald bedrag. Mogelijk wilt u dat dit aanbod wordt weergegeven op uw openingspagina, een categoriepagina en bepaalde productpagina's, maar u wilt dat het een ander formaat en op een andere locatie op elk paginatype wordt weergegeven. Je kunt een opvallend voorstel op je homepage weergeven en dat aanbod vervolgens versterken met kleinere aanbiedingen op andere relevante pagina's. </p> <p>U kunt ook een activiteit met meerdere pagina's gebruiken om verschillende lay-outs voor uw bureaublad en mobiele sites te definiëren die niet reageren. </p> <p>Zie <a href="/help/main/c-experiences/c-visual-experience-composer/multipage-activity.md#concept_277E096063E14813AC5D8EDFA1D2ED48" format="dita" scope="local"> Meerdere pagina's </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Op formulieren gebaseerde activiteiten maken </td> 
   <td colname="col2"> <p>Creeer een activiteit zonder de Visuele Composer van de Ervaring te gebruiken. Kies in plaats daarvan locaties en aanbiedingen via een formulier. Met dit, kunnen de Standaardactiviteiten van het Doel in e-mail, mobiele apps, kiosks, en andere plaatsen worden geleverd die niet met een Composer van de Visueel Ervaring werken. </p> <p>Zie <a href="/help/main/c-experiences/form-experience-composer.md#task_FAC842A6535045B68B4C1AD3E657E56E" format="dita" scope="local"> Formuliergebaseerde Experience Composer </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Configureerbare succeswaarden </td> 
   <td colname="col2"> <p> Met de fijnkorrelige opties kunt u bepalen hoe u succesmetingen kunt tellen. U kunt onder andere de metrische waarde per impositie of één keer per bezoeker tellen en kiezen of u de gebruiker in de activiteit wilt houden of deze wilt verwijderen. Dit is gelijk aan de "geavanceerde opties" voor succesmetriek die beschikbaar zijn in Target Classic. </p> <p>Zie <a href="/help/main/c-activities/r-success-metrics/success-metrics.md#reference_D011575C85DA48E989A244593D9B9924" format="dita" scope="local"> Succeswaarden </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Verbetering: Experience Targeting Experience limit removed. </td> 
   <td colname="col2"> De vorige limiet van tien ervaringen in het praktijkgericht is opgeheven. </td> 
  </tr>  
  <tr> 
   <td colname="col1"> Profielsynchronisatie in realtime voor gegevens van derdenId </td> 
   <td colname="col2"> Wanneer een bezoeker van een site zich halverwege de sessie aanmeldt en een 3d-partyId krijgt, zijn alle eerder geladen profielkenmerken die zijn gekoppeld aan de derde partijId nu direct beschikbaar. Zie <a href="/help/main/c-target/c-audiences/c-target-rules/visitor-profile.md#concept_E972690B9A4C4372A34229FA37EDA38E" format="dita" scope="local"> Bezoekerprofiel </a>. </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> Recommendations Premium: Zoeken in factnaam </td> 
   <td colname="col2"> U kunt nu zoeken naar een facetnaam. </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> Automated Personalization: Metrische tracking na het doel </td> 
   <td colname="col2"> <p> Eerder startte Target een ervaring toen de bezoeker het modelleringsdoel bereikte. Gebruikers kunnen nu in de activiteit blijven voor traceringsdoeleinden nadat ze het modelleringsdoel hebben bereikt. </p> <p> Bijvoorbeeld, vaak wordt een activiteit van Automated Personalization gebruikt om kliktarieven te verbeteren, en dat wordt geplaatst als modelleringsdoel. Nochtans, is het belangrijk om te zien hoe de verhoogde klikkoersen tot definitieve omzetting leiden, zodat is het volgen door de definitieve omzetting essentieel. </p> Zie <a href="/help/main/c-activities/t-automated-personalization/automated-personalization.md#task_8AAF837796D74CF893CA2F88BA1491C9" format="dita" scope="local"> Automated Personalization </a>. </td> 
  </tr> 
 </tbody> 
</table>

**Oplossingen**

Deze release bevat de volgende oplossingen:

* Analytics as the reporting source for Target is now supported for XT activities.
* Probleem verholpen waarbij de besturingservaring die in Analytics wordt weergegeven, werd gewijzigd nadat de activiteit actief was geworden.
* Probleem verholpen waarbij waarden na een # in een URL tijdens het maken van het publiek/segment als onderdeel van het pad werden beschouwd.

**Bekende problemen**

De volgende bekende problemen zijn gemeld:

* Wanneer JavaScript uitschakelen is ingeschakeld voor pageA in een activiteit met meerdere pagina&#39;s, blijft JavaScript ingeschakeld voor alle pagina&#39;s, maar blijft de functionaliteit uitgeschakeld.

### Adobe [!DNL Target] Standard/Premium 15.6.1 (25 juni 2015) {#section_43FEA310830E4E8E853FAB56B12B1301}

Deze release bevat de volgende functies en verbeteringen:

<table id="table_C0B37E1730014ADA8C36310093F5C43A"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Functie </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Verbeteringen in de compatibiliteit van Visual Experience Composer </p> </td> 
   <td colname="col2"> <p> Een nieuwe instelling voor de hele account, zodat Target gemakkelijker de juiste CSS-kiezers kan genereren. U kunt bijvoorbeeld opgeven of Doel klassen of id's moet gebruiken. Hierdoor wordt de compatibiliteit met AEM verbeterd. Deze instelling kan per activiteit worden overschreven </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Ervaring Ondersteuning voor Analytics als bron voor rapportage </p> </td> 
   <td colname="col2"> <p>U kunt Analytics nu gebruiken als een rapporteringsbron voor de activiteiten van het Targeting van de Ervaring. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p>Automated Personalization: Visuele indicatie van modelstatus </p> </td> 
   <td colname="col2"> <p> Wanneer een voorspellend model voldoet aan de vereiste kwaliteitscriteria en geldig wordt geacht, wordt het geschikt geacht en gebruikt om een gepersonaliseerde score voor offer decisioning te berekenen. Een klokpictogram verandert in een vinkje wanneer het model klaar is en het Doel kan beginnen met het leveren van gepersonaliseerde inhoud. Aangezien de lift pas wordt verwacht nadat de modellen gereed zijn, kunt u met de visuele indicatie de juiste verwachting instellen. Gebruik de verkeersschatter in Visuele Composer van de Ervaring om een richtlijn te krijgen van wanneer de modellen klaar zullen zijn. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p>Premium Recommendations: Bladeren en navigeren in de composer voor visuele ervaring </p> </td> 
   <td colname="col2"> <p> Hiermee kunt u de composer voor visuele beleving op één pagina openen en vervolgens koppelingen en formulierverzendingen volgen om andere pagina's op uw site te bereiken, zoals een winkelwagentje. Zodra op de pagina u wilt testen, draai de Visuele Composer van de Ervaring terug naar "stelt"wijze samen en creeer uw ervaringen. U kunt bijvoorbeeld een bericht wijzigen op de verzendpagina en het vervolgens testen op de standaardpagina. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p>Premium Recommendations: Zoeken in gefactureerde catalogus </p> </td> 
   <td colname="col2"> <p> Biedt een robuustere manier om uw catalogus te doorzoeken. Ook maakt het gemakkelijker om de onderzoeksresultaten tot zeer specifieke reeks producten te beperken. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Externe campagnes tonen in de lijst Standaardactiviteiten doel </p> </td> 
   <td colname="col2"> <p> In de lijst Standaardactiviteiten doel ziet u nu Klassieke campagnes. Als u uit Klassieke campagnes van het Doel wilt filtreren en slechts de Norm van het Doel bekijkt, kunt u de optie van het "Bron"onderzoeksfilter gebruiken. Als u bijvoorbeeld alleen Adobe Target Standard-activiteiten wilt weergeven, selecteert u het bronfilter en typt u "Adobe Target" als bron. De mogelijkheid om activiteiten te bekijken die in Recommendations Classic of Adobe Mobile Services zijn gemaakt, wordt in een toekomstige release toegevoegd. </p> <p>U kunt in andere oplossingen gemaakte activiteiten activeren en deactiveren via de gebruikersinterface van Doel. Voor alle andere veranderingen zult u de activiteiten in de bronoplossing moeten uitgeven. </p> <p> Voor activiteiten die in andere oplossingen worden gecreeerd, is de publieksinformatie niet zichtbaar op de pagina van het Overzicht. Bekijk de publieksinformatie in de oplossing waar de activiteit werd gecreeerd. </p> <p>Zie <a href="/help/main/c-activities/activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03" format="dita" scope="local"> Activiteiten </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Oplossingen**

Deze release bevat de volgende oplossingen:

* Toegevoegd bericht om aan te geven dat een activiteit die niet kan worden bekeken beschikbaar is voor weergave in Doel Klassiek.
* Probleem opgelost waarbij URL&#39;s traag werden omgeleid.
* Probleem verholpen waarbij de parameters voor het bijhouden van klikken werden verbroken als andere succeswaarden in de activiteit werden verwijderd.
* Probleem verholpen waarbij de afbeelding die naar het Recommendations-ontwerp is geüpload niet correct werd weergegeven in de Visual Experience Composer.
* Probleem verholpen met de verkeersschatter in Automated Personalization-activiteiten waarbij het aantal combinaties werd gebruikt in plaats van de som van aanbiedingen over verschillende locaties.
* Probleem verholpen waarbij mbox-parameters niet altijd op de schermen voor het maken van een publiek werden weergegeven.
* Probleem verholpen waarbij updates op de miniatuur van Recommendations-ontwerpen werden geblokkeerd.

### Adobe [!DNL Target] Standard/Premium 15.5.1_Hotfix (28 mei 2015) {#section_D751F55A3812417FAA72BD6872AE3C2A}

Deze hotfix-release bevat de volgende oplossingen:

* Probleem verholpen waarbij het selectievakje Geschatte optillen in inkomsten niet zichtbaar was.
* Probleem verholpen waardoor de knop Activiteit maken voor sommige gebruikers niet correct werd weergegeven.
* Probleem verholpen dat ertoe leidde dat het tekstvak Naam activiteit in de Visual Experience Composer verdween tijdens het bewerken van A/B en de Experience Targeting-activiteiten.

### Adobe [!DNL Target] Standard/Premium 15.5.1 (21 mei 2015) {#section_FF0F959908784AF0906EFB9E8324F207}

Deze release bevat de volgende functies en verbeteringen:

<table id="table_3985F758176F4884A94AFDFB78B24209"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Functie </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Aangepaste code-invoer en -bewerking in Visual Experience Composer </p> </td> 
   <td colname="col2"> <p>Laat u toe om, nieuwe acties te zien uit te geven en toe te voegen gebruikend een coderedacteur binnen de Visuele Composer van de Ervaring. </p> <p>Zie <a href="/help/main/c-experiences/c-visual-experience-composer/c-vec-code-editor/vec-code-editor.md#concept_B3A6E9EE3A60406DB640E205EA1745B5" format="dita" scope="local"> Code-editor </a> voor meer informatie . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>JavaScript en CSS boven aan de pagina toevoegen </p> </td> 
   <td colname="col2"> <p> JavaScript-code toevoegen aan de pagina('s) direct onder de <span class="codeph"> &lt;body&gt; </span> -tag, zonder dat u een element op de pagina hoeft te selecteren. </p> <p>Zie <a href="/help/main/c-experiences/c-visual-experience-composer/c-vec-code-editor/vec-code-editor.md#concept_B3A6E9EE3A60406DB640E205EA1745B5" format="dita" scope="local"> Code-editor </a> voor meer informatie . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Nieuwe opties voor het maken van publiek </p> </td> 
   <td colname="col2"> <p>U kunt nu als volgt een doel instellen (dit bevindt zich in de sectie Geo wanneer u een publiek maakt): </p> <p> 
     <ul id="ul_FE1E3605FB8042E9B5E80C0DB0C6C2AD"> 
      <li id="li_6D112A4DB2344B4E9F1B84E943A43DD8">ISP </li> 
      <li id="li_5C95F3F55D194D81905F8138FB546288">Netwerkdomein </li> 
      <li id="li_63E3606516BC4FFC8C91E49297542464">Verbindingssnelheid (opties zijn: breedband, dialup, mobiel, t1, t3, satelliet) </li> 
     </ul> </p> <p>Zie <a href="/help/main/c-target/c-audiences/audiences.md#concept_65BE870D290E412D8BBF557EEA67C271" format="dita" scope="local"> Soorten publiek </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p>Recommendations Premium - Nieuwe functies </p> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_6DC206CB52E34498BC762FCCF77807AA"> 
      <li id="li_B26568D642974F17B4B2D6E42CFDC5B9"> <p>Nieuwe modus Voorvertoning om ontwerpen weer te geven met JavaScript </p></li> 
      <li id="li_B8D1ADE874D244F198CBD3387ED3E310"> <p>Catalogus zoeken ondersteunt nu gratis zoeken naar Engelse talen </p> </li> 
      <li id="li_EB8D595EA8A84B37A3262F76543E1B05"> <p>Ondersteuning op accountniveau voor het invoeren van een statische, basis-URL die aan alle relatieve <span class="codeph"> entiteit.thumbnailUrl </span> waarden </p></td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p class="Premium"> Verbeteringen voor Recommendations Premium </p> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_1CF5F2D0CDE84DDC9C445B5CD878EEAA"> 
      <li id="li_EB225752776449C6B21C2B2514B508C5"> <p>Verbeteringen aan ontwerpvoorproef in VEC </p> </li> 
      <li id="li_2CD8267EF166421DBB6EFBF704625848"> <p>Verbeteringen in de layout van out-of-the-box-ontwerpen </p> </li> 
      <li id="li_D737754C200844638B536A3BE02E9C5F"> Verzameling weergegeven in doeldiagram</li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p class="Premium"> Recommendations Classic-functionaliteit wordt nu ondersteund in Recommendations Premium </p> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_E0D6A9C12B514DE3B3EA753BB4D56662"> 
      <li id="li_2A728C8938834162A0C0C1C926AC5DD9"> Gedeeltelijke sjabloonrendering <p>Zie <a href="/help/main/c-recommendations/c-algorithms/create-new-algorithm.md#content" format="dita" scope="local"> Inhoudsinstellingen </a>. </p> </li> 
      <li id="li_B1DFC829D19B4570AB5A7F937C7EF2CC"> Geef back-upregels op volgens criteria </li> 
      <li id="li_F8C9690CEC974E37B72A85C2FACFAA6D"> FTPS voor productfeeds ondersteunen</li> 
      <li id="li_3C0FA493C87345E4BE994936DF0D0162"> Aangepaste algoritmen worden nu automatisch weergegeven als criteria</li> 
      <li id="li_5B074C9FB3CB46EBA6EB4D8B1098480E"> Uurautomatische reïndexering van productcatalogi voor klanten zonder feeds </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p>Automated Personalization: Toegevoegde kwaliteitskoppelingen </p> </td> 
   <td colname="col2"> <p> U kunt nu een voorvertoning bekijken van de weergave van uw ervaringen bij levering. De mening en deelt verbindingen met uw AP ervaringen op uw plaats om een "ware voorproef"van de ervaringen buiten Composer van de Visuele Ervaring van het Doel te krijgen. </p> <p>Zie <a href="/help/main/c-activities/t-automated-personalization/automated-personalization.md#task_8AAF837796D74CF893CA2F88BA1491C9" format="dita" scope="local"> Automated Personalization </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>MVT op basis van analysemogelijkheden: Voorvertoning van prestatierapport </p> </td> 
   <td colname="col2"> <p>Wanneer het gebruiken van Analytics als rapporteringsbron voor multivariate tests, kunt u voorproef uw activiteiten MVT van het rapport van Prestaties. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> A/B-tests en ervaring gericht op: Activiteiten maken in drie stappen </p> </td> 
   <td colname="col2"> <p> <a href="/help/main/c-activities/t-test-ab/t-test-create-ab/test-create-ab.md" format="dita" scope="local"> A/B maken </a>en <a href="/help/main/c-activities/t-experience-target/t-xt-create/xt-create.md#task_D6B3429AC31549E1A70EDF04B3DDC765" format="dita" scope="local"> Gericht op ervaring </a> activiteit in drie stappen in plaats van vier. Deze verandering maakt het proces om deze activiteiten meer als werkschema van andere activiteitentypes, zoals Automated Personalization en Multivariate Tests te creëren. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Analyses als rapportbron zijn beschikbaar voor de meeste typen activiteiten. </p> </td> 
   <td colname="col2"> <p> De A/B met het activiteitstype Analytics bestaat niet meer. De optie om Analytics als uw rapporteringsbron te gebruiken is nu beschikbaar op de pagina van het Beleid &amp; van Montages voor alle activiteitstypes behalve Automated Personalization en het Targeting van de Ervaring. Dientengevolge, is er niet meer een afzonderlijk activiteitstype genoemd A/B Test met de Gegevens van de Analyse. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Externe campagnes tonen in de lijst Standaardactiviteiten doel </p> </td> 
   <td colname="col2"> <p> In de lijst Standaardactiviteiten doel ziet u nu Klassieke campagnes. Als u uit Klassieke campagnes van het Doel wilt filtreren en slechts de Norm van het Doel bekijkt, kunt u de optie van het "Bron"onderzoeksfilter gebruiken. Als u bijvoorbeeld alleen Adobe Target Standard-activiteiten wilt weergeven, selecteert u het bronfilter en typt u "Adobe Target" als bron. De mogelijkheid om activiteiten te bekijken die in Recommendations Classic of Adobe Mobile Services zijn gemaakt, wordt in een toekomstige release toegevoegd. </p> <p>Zie <a href="/help/main/c-activities/activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03" format="dita" scope="local"> Activiteiten </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Controlerapport exportorder </p> </td> 
   <td colname="col2"> <p> Mogelijkheid om het Rapport van de Controle van de Orde uit te voeren/te downloaden dat aan de rapporten van het Doel wordt toegevoegd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Bèta: A4T-lift en -betrouwbaarheid </p> </td> 
   <td colname="col2"> <p> Optillen en vertrouwen zijn nu beschikbaar voor standaardmeetgegevens en aangepaste gebeurtenissen van Analytics. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Oplossingen**

Deze release bevat de volgende oplossingen:

* Probleem verholpen bij het maken van een publiek waarbij gewijzigde operatoren kenmerkwaarden gewist hadden.
* De aangebrachte verbeteringen zodat douane-gecodeerde regionale dozen in Visuele Composer van de Ervaring selecteerbaar zijn.
* Probleem verholpen in Recommendations waarbij kenmerken met double-bytetekens (voor meertalige gevallen) de regels voor het filteren van insluiting omzeilden.
* Alle activiteitstypen ondersteunen nu activiteitennamen van maximaal 200 tekens.

### Adobe [!DNL Target] Standard/Premium15.3.1 (26 maart 2015) {#section_591371851693496C820175753F588E73}

Deze release bevat de volgende functies en verbeteringen:

<table id="table_5A2F2058ACFB455E9F69484CA0C8D3DE"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Functie </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Verbeteringen in Visual Experience Composer </p> </td> 
   <td colname="col2"> <p>Inhoud die alleen op de muisaanwijzer wordt weergegeven, zoals vervolgmenu's en minikaarten, kan nu worden geselecteerd voor bewerking in de composer voor visuele ervaring. </p> <p>Zie <a href="/help/main/c-experiences/experiences.md#concept_A2E10F6AFB3D4AEAB6951EE14688848D" format="dita" scope="local"> Ervaringen </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p class="premium">Automated Personalization: Verkeersschatting </p> </td> 
   <td colname="col2"> <p>De verkeersschatting, die voorheen alleen beschikbaar was bij het type multivariate testactiviteit, is nu beschikbaar voor Automated Personalization-activiteiten. </p> <p>Zie <a href="/help/main/c-activities/t-automated-personalization/ap-traffic-estimator.md#task_71AA6922AFD447EA8C5E610A78ABA714" format="dita" scope="local"> Schatting van het Verkeer Vereist voor Succes </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p class="premium">Automated Personalization: Visuele voorvertoning </p> </td> 
   <td colname="col2"> <p>Bekijk een visuele voorvertoning van elke inhoudscombinatie in de Visual Experience Composer. </p> <p>Zie <a href="/help/main/c-activities/t-automated-personalization/ap-preview-experiences.md#task_21A700587E88453A9FC2210C0DE53A28" format="dita" scope="local"> Voorvertoning van ervaringen weergeven voor een Automated Personalization-test </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p class="premium">Recommendations: Verbeterde weergave van inhoud </p> </td> 
   <td colname="col2"> <p>U kunt nu elk item zien dat in aanmerking komt voor een verzameling of uitsluiting wanneer u de verzameling weergeeft of bewerkt. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p class="premium">Recommendations: Verbeterde zoekresultaten </p> </td> 
   <td colname="col2"> <p>Het totale aantal items dat aan elke zoekreeks voldoet, wordt weergegeven. </p>  </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Klantkenmerken uploaden in Adobe Analytics </p> </td> 
   <td colname="col2"> <p>De gebruikers van Analytics die de gegevens van de ondernemingsklant in een gegevensbestand van het het relatiebeheer van de klant (CRM) vangen kunnen die gegevens in Experience Cloud uploaden. </p> <p>Zodra de gegevens in de Experience Cloud zijn, kunt u, bijvoorbeeld, een publiekssegment in Analytics tot stand brengen die klantenattributen in de segmentdefinitie omvat, en dan dat publiek met Doel delen. </p> <p> <p>Opmerking: Het doel kan nog niet rechtstreeks onbewerkte klantkenmerken gebruiken. </p> </p></td> 
  </tr> 
 </tbody> 
</table>

**Oplossingen**

Deze release bevat de volgende oplossingen:

* Voor Analytics voor op Doel gebaseerde activiteiten, zijn de Lift en de kolommen van het Vertrouwen nu verborgen voor de metriek van de Analyse waar de berekeningen niet kunnen worden uitgevoerd.
* Probleem verholpen waarbij de korte indeling van de `charset` metatag is niet herkend in de Enhanced Experience Composer

**Bekende problemen**

* Doelgebaseerde conversiegebeurtenissen voor multivariate tests in Target Standard/Premium worden niet gerapporteerd wanneer Analytics wordt gebruikt als rapportagebron voor Target. Dit probleem zal naar verwachting binnenkort worden opgelost.

### Adobe [!DNL Target] 15.2.1 (19 februari 2015) {#section_9AA19B060D814E08A673FB752E21D0C3}

Deze release bevat de volgende functies en verbeteringen:

<table id="table_1558E5A5BAB64CC281C193F5A49E2ECE"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Functie </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p class="premium">Type nieuwe activiteit: Recommendations </p> </td> 
   <td colname="col2"> <p>Bij Recommendations-activiteiten worden automatisch producten of inhoud weergegeven die uw klanten interessant kunnen maken op basis van eerdere gebruikersactiviteiten. Recommendations helpt klanten om relevante objecten te sturen waarvan ze anders wellicht niet op de hoogte zijn. </p> <p>Recommendations is beschikbaar als onderdeel van de Target Premium-oplossing. Het is niet inbegrepen bij de Standaard van Doel zonder een vergunning van de Premie van het Doel. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Oplossingen**

Deze release bevat de volgende oplossingen:

* Probleem verholpen waarbij een omleidingsvoorstel niet werkte bij het reviseren van een pagina.

### Adobe [!DNL Target] 15.1.1 (22 januari 2015) {#section_059F9B41804B4FA58D05C4485EDF926D}

Deze release bevat de volgende functies en verbeteringen:

<table id="table_5D4C3C5695BA4A88BC65E2721CFB073A"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Functie </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Type nieuwe activiteit: Multivariatietest </td> 
   <td colname="col2"> <p> In een multivariate test met volledige factorial worden alle mogelijke combinaties van aanbiedingen in uw inhoudsgebieden vergeleken om u te helpen de best mogelijke combinatie van inhoud te bepalen. Uit de multivariatie-tests blijkt ook welke inhoud op welke gebieden de meeste activiteiten succesvol zijn. Een veelvoorkomend gebruik van multivariate tests is een volledige pagina te optimaliseren nadat u een A/B test hebt gebruikt om een optimale lay-out te bepalen. Met de multivariate test kunt u de afzonderlijke elementen op de pagina optimaliseren (zoals de hoofdafbeelding, kopregels of promotionele inhoud). </p> <p>Voor een inleidende video raadpleegt u <a href="https://my.adobeconnect.com/p2k6u8iiu6l/" format="https" scope="external"> https://my.adobeconnect.com/p2k6u8iiu6l/ </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Blader naar pagina's en pagina-elementen in de Visual Experience Composer </td> 
   <td colname="col2"> <p> Hiermee kunt u de composer voor visuele beleving op één pagina openen en vervolgens koppelingen en formulierverzendingen volgen om andere pagina's op uw site te bereiken, zoals een winkelwagentje. Zodra op de pagina u wilt testen, draai de Visuele Composer van de Ervaring terug naar "stelt"wijze samen en creeer uw ervaringen. U kunt bijvoorbeeld een bericht wijzigen op de verzendpagina en het vervolgens testen op de standaardpagina. </p> <p> In de modus Bladeren kunt u ook communiceren met een pagina om de juiste status te krijgen, zoals door een afbeeldingscarrousel gaan, een miniwinkelwagentje openen of een pop-up sluiten. Als de pagina de gewenste status heeft, schakelt u over naar de modus Samenstellen en maakt u de test. </p> <p> Werkt momenteel met A/B-tests, ervaring gericht op en A/B-tests met Analytics. </p> <p>Zie <a href="/help/main/c-experiences/experiences.md#concept_A2E10F6AFB3D4AEAB6951EE14688848D" format="dita" scope="local"> Ervaringen </a> voor meer informatie . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Mobiel apparaat </td> 
   <td colname="col2"> U kunt opties voor mobiele apparaten selecteren wanneer u een publiek maakt. <p>Zie <a href="/help/main/c-target/c-audiences/audiences.md#concept_65BE870D290E412D8BBF557EEA67C271" format="dita" scope="local"> Soorten publiek </a> voor meer informatie . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Klik op Tekstspatiëring (Automated Personalization) </td> 
   <td colname="col2"> <p>U kunt nu klikken bijhouden in Automated Personalization. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> mboxTrace-foutopsporingshulpprogramma </td> 
   <td colname="col2"> <p> Onderzoek details over uw de paginaimplementatie van het Doel en activiteit/ervaringsleveringsstatus voor het betere oplossen van problemen. </p> <p>Zie <a href="/help/main/c-activities/c-troubleshooting-activities/content-trouble.md#concept_D2548B486C984B1E97ED7A72075B8EEA" format="dita" scope="local"> Problemen met inhoudslevering oplossen </a> voor meer informatie . </p> </td> 
  </tr> 
 </tbody> 
</table>

**Oplossingen**

Deze release bevat de volgende oplossingen:

* Probleem verholpen waarbij schuiven niet correct werkte in IE10.

## Uitzettingen 2014 {#reference_A841709C803C4ECEB236F62E6513EB0F}

### Adobe [!DNL Target] 14.10.2 (6 november 2014) {#section_E7036B45DF974FB7B81E67261357A01B}

<!-- 

target/r_release-notes-2014.xml

 -->

Deze kleine release is vooral gericht op serverstabiliteit. Er zijn geen nieuwe functies als onderdeel van deze patch.

### Adobe [!DNL Target] 14.10.1 (30 oktober 2014) {#section_D557CB331A004155B91CFE5B197076F3}

Deze release bevat de volgende functies en verbeteringen:

| Functie | Beschrijving |
|---|---|
| Aanbiedingen omleiden | Leid een ervaring om naar een andere URL zodat u één pagina tegen een andere pagina kunt testen. Zie [Een omleidingsvoorstel maken](/help/main/c-experiences/c-visual-experience-composer/redirect-offer.md#task_9578678D42784F5EB9638F8AC8C911FA). |
| Doelgerichtheid toepassen op succesmetriek | Kies een opgeslagen publiek dat u wilt toepassen op een succesmetrische methode. Met deze functie kunt u beperken wat acties tellen voor een bepaalde succesgebeurtenis. Een voorbeeld zou omzettingen kunnen beperken tot wanneer de orde meer dan $0 is, of slechts telend succes wanneer een gebruiker een bepaalde pagina in de zelfde zitting bekijkt zoals het ingaan van de activiteit. |
| Automated Personalization: Selecteren en rapporteren op basis van RPV/AOV-meetgegevens | U kunt nu de RPV- en AOV-meetgegevens selecteren in de workflow voor het maken van ervaringen met Automated Personalization. Ga voor meer informatie over het maken van een Automated Personalization-activiteit naar [Automated Personalization](/help/main/c-activities/t-automated-personalization/automated-personalization.md#task_8AAF837796D74CF893CA2F88BA1491C9). |
| Verbeterde besturingselementen voor machtigingen | Alleen gebruikers met de juiste machtigingen kunnen het publiek bewerken. |

Deze release bevat de volgende verbeteringen:

* De overzichtspagina toont het activiteitendoel.
* Er wordt een waarschuwing weergegeven wanneer JavaScript wordt ingevoerd in het bewerkingsvak HTML.

### Adobe [!DNL Target] 14.9.1 (19 september 2014) {#section_681F27FBFDFF46FE8A1A8E24A50A26F4}

Deze release bevat de volgende functies en verbeteringen:

| Functie/verbetering | Beschrijving |
|---|---|
| Invoegen en bewerken van JavaScript toestaan | De mogelijkheid om aangepaste JavaScript te bewerken en te injecteren toegevoegd in de ervaringseditor wanneer u **[!UICONTROL Edit HTML]** in het menu Handelingen. |
| Automatisch publiek importeren | Soorten publiek worden automatisch op de achtergrond geïmporteerd wanneer een gebruiker de lijst met doelgroepen opent en het geïmporteerde publiek langer dan 10 minuten oud is. |
| Meer HTML-aanbiedingen dan waarop kan worden gesynchroniseerd [!DNL Target Classic] | De voormalige 64 kB-limiet is verhoogd tot 256 kB. |

Deze release bevat de volgende oplossingen:

* Probleem verholpen waarbij videovoorstellen niet correct werden geleverd op Firefox.
* Probleem verholpen waardoor een ongedaan maken van het bewerken van een koppeling niet kon worden weergegeven als ongedaan gemaakt in de composer voor visuele ervaring.
* Probleem verholpen in de ervaringseditor van Automated Personalization die ertoe leidde dat een gewijzigd videoaanbod niet zo veranderde werd weergegeven.
* Probleem verholpen waarbij de botsingspagina van een activiteit als een lege pagina in Google Chrome werd weergegeven.

### Adobe [!DNL Target] 14.8.1 (21 augustus 2014) {#section_02D0DFA7A8D145B2B3FEFF83591243E1}

Deze release bevat de volgende nieuwe functies en verbeteringen:

| Functie/verbetering | Beschrijving |
|---|---|
| Verbeterde synchronisatie van HTML-aanbiedingen met [!DNL Target Classic] door de tekenlimiet te verhogen | De tekenlimiet van een HTML-aanbieding onder Inhoud aanpassen aan de limiet van 256 kB voor het aantal HTML-aanbiedingen gesynchroniseerd met [!DNL Target Classic]. |
| Verbeterde gebruikerservaring wanneer een fout wordt gecreeerd in de Redacteur van de Ervaring. | De Experience Editor geeft een bericht weer wanneer de wijzigingen in de DOM-structuur op de pagina de kiezers afbreekt. |

**Oplossingen**

* Probleem verholpen waarbij de rapportgrafiek niet werd gegenereerd tijdens het navigeren tussen activiteiten.
* Probleem verholpen waarbij geselecteerde koppelingen niet werden gemarkeerd als geselecteerd wanneer gebruikers op deze koppelingen klikten **[!UICONTROL Select Link]** op de [!UICONTROL Goals and Settings] pagina.

* Correctie van een fout waardoor een nieuwe activiteit niet kon worden weergegeven in het dialoogvenster [!UICONTROL Activity List] na activering op de [!UICONTROL Overview] pagina.

* Probleem verholpen waardoor gebruikers geen koppeling konden selecteren voor klikken op bijhouden.
* Probleem verholpen waarbij dubbele aanbiedingen werden weergegeven in een rapport op aanbiedingsniveau.
* Probleem verholpen waardoor mbox-elementen niet konden worden ingevoegd.
* Correctie van een fout die ervoor zorgde dat de conversies van de verbindingsklik niet werkten.
* Oplossing voor een fout bij klikconversie die is genegeerd `target="_blank" functions.`
* Probleem verholpen waarbij met klikken bijhouden werd genavigeerd buiten de pagina.

### Adobe [!DNL Target] 14.6.1 (25 juni 2014) {#section_A520F01EEE0A4C2CBB3F2A37E6DD6F83}

Deze release bevat de volgende nieuwe functies:

>[!NOTE]
>
>Sommige functies in deze release zijn alleen beschikbaar als onderdeel van de [!DNL Target Premium] oplossing.

<table id="table_A2A978B157D54E17BD7366ADC04C8FC9"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Functie </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="keyword"> Automated Personalization (Target Premium) </span> </td> 
   <td colname="col2"> <p> <span class="keyword"> Automated Personalization </span> biedt geavanceerde computerleeralgoritmen om persoonlijke ervaringen en verbeterde conversiesnelheden voor digitale ervaringen te stimuleren. </p> <p> <p>Opmerking:  <span class="keyword"> Automated Personalization </span> is beschikbaar als onderdeel van de <span class="keyword"> Doelpremie </span> oplossing. Het is niet opgenomen in <span class="keyword"> Doelstandaard </span> zonder <span class="keyword"> Doelpremie </span> licentie. Als u een <span class="keyword"> Doelstandaard </span> of <span class="keyword"> Doelpremie </span> licentie gebruiken <span class="keyword"> Doel </span> in de Adobe Experience Cloud. </p> </p> <p>Eén bestand op uw site implementeren en de mogelijkheid bieden om naar inhoud te wijzen en erop te klikken en vervolgens visueel aanvullende inhoudsopties voor dat gebied maken en selecteren. Vervolgens bepaalt het modelleringssysteem automatisch welk stuk inhoud aan elk individu moet worden geleverd op basis van alle gedragsgegevens die het systeem over de bezoeker heeft. Deze mogelijkheid biedt een persoonlijke ervaring voor elke bezoeker. De markeerteken hoeft geen test uit te voeren, vervolgens de resultaten te analyseren en vervolgens een winnaar te leveren voordat de lift die uit optimalisatie is gevonden, wordt gerealiseerd. </p> <p> <span class="keyword"> Automated Personalization </span> verstrekt: </p> 
    <ul id="ul_9EF654B10FFA46169EE2E033683BA82E"> 
     <li id="li_8D201BF8F37B4B2489D039A0340E065E">Twee machinaal leeralgoritmen: 
      <ul id="ul_E1DF69071C9047EEA692B5EF01176E4B"> 
       <li id="li_1F4ED87AB6D044C1BE04D0360F42D56F"> <span class="keyword"> Willekeurig bos </span> </li> 
       <li id="li_BE6388BA88684501B741713CECF5AE91"> <span class="keyword"> Residuvariatiemodel </span> </li> 
      </ul> </li> 
     <li id="li_36E18493A95B4C96BFA3133CDFD8826A">Eén regel code-implementatie met WYSIWYG-inhoud bewerken </li> 
     <li id="li_79B1878FA64A40E88A973C57C39FC5FF">Het primaire doel voor de activiteit gebruikt momenteel metrisch Conversie. Opbrengsten en betrokkenheid zijn beschikbaar als extra maatstaven. </li> 
     <li id="li_FE94A79767EF4534BD02B2AFD7E27E1B">Verbinding maken met de <span class="keyword"> Master marketingprofiel </span> voor naadloze verzameling van gedragsgegevens van voorafgaande bezoekers </li> 
    </ul> <p>Zie <a href="/help/main/c-activities/t-automated-personalization/automated-personalization.md#task_8AAF837796D74CF893CA2F88BA1491C9" format="dita" scope="local"> Automated Personalization </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Meerdere activiteiten op één pagina </td> 
   <td colname="col2"> <p>Inhoud van meerdere standaardactiviteiten van Target kan op één pagina worden geleverd vanaf één pagina <span class="keyword"> Doel </span> serveraanroep. </p> <p> <p>Opmerking: Dit is niet van invloed op de beoordeling van de Klassieke Doelprioriteiten. </p> </p><p>Voor informatie over hoe Doel bepaalt welke ervaring om te tonen wanneer de veelvoudige activiteiten de zelfde plaats op een pagina richten, zie <a href="/help/main/c-activities/priority.md#concept_1780C11FEA57440499F0047DD6900E0F" format="dita" scope="local"> Prioriteit </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Oplossingen**

* Probleem verholpen waarbij sommige gedeelde soorten publiek die zijn verwijderd, nog steeds worden weergegeven in het dialoogvenster [!UICONTROL Audiences] lijst.
* Probleem verholpen waarbij een onverwachte fout optrad [!UICONTROL Save] weergegeven in Internet Explorer 10.
* Synchronisatiefout bij het opslaan van een campagne gecorrigeerd.
* Probleem verholpen waarbij het publiek voor een ervaring niet werd weergegeven in rapporten.
* Probleem verholpen waarbij de metrische lijsten in [!DNL Target] en [!DNL Analytics] van overeenkomst.

* Probleem verholpen waarbij gebruikers hun globale box konden opgeven als een box die wordt gebruikt om HTML-inhoud te leveren door [!DNL Target Standard]. Het gebruik van de globale box heeft op die manier een negatief effect op de levering van inhoud en [!DNL Target Classic]De mogelijkheid om meerdere campagnes op één pagina te leveren in één aanvraag.

* Probleem verholpen waarbij de weergave van verwijderde items werd voortgezet.

### Adobe [!DNL Target] Standaard 14.5 (28 mei 2014) {#section_530EAB9376414D4989CA0740361DDCC2}

Deze release bevat de volgende opgeloste problemen:

* Probleem verholpen waarbij het voorvertonen van een ervaring niet naar behoren functioneerde.

### Adobe [!DNL Target] Standaard 1.7 (28 april 2014) {#section_2C2B9B6299ED4F48A3B983AB015F381A}

[Doelstandaard 1.7-releasewebinar](https://my.adobeconnect.com/p1oabaz3cxi/)

Deze release bevat de volgende nieuwe functies:

<table id="table_11CD9EE0C9534FF19C9154784C4BFCF0"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Functie </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Adobe Analytics-rapportage voor Adobe Target </td> 
   <td colname="col2"> Adobe Analytics-klanten kunnen Analyse selecteren als de standaard rapportbron tijdens het <a href="/help/main/c-activities/t-test-ab/t-test-create-ab/create-a4t.md#task_FE48F7B077C44A5BA015B087428412EF" format="dita" scope="local"> testprocedure </a>. Het selecteren van alle succesmetriek of publiek dat u wilt gebruiken om uw resultaten te filteren, is niet meer vereist. Binnen rapportering, kunt u om het even welk succes metrisch of publiekssegment selecteren dat in Analytics wordt bepaald en het retroactief toepassen op uw rapportering voor het uitgebreide filtreren en boor-down analyse van uw optimalisatieresultaten. <p> <p>Opmerking: Ga naar <a href="https://survey.adobe.com/jfe/form/SV_ekBHTLSoP5Zki2y" format="http" scope="external"> https://survey.adobe.com/jfe/form/SV_ekBHTLSoP5Zki2y </a>. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Master marketingprofiel in realtime publiek </td> 
   <td colname="col2"> Gebruik het master marketingprofiel dat bezoeker-id's en -gegevens verenigt in één actionabel profiel voor gebruik in verschillende oplossingen. Met een selectievakje tijdens het maken van segmenten in Adobe Analytics kan het segment beschikbaar zijn in de aangepaste publieksbibliotheek van Adobe Target. Een segment dat is gemaakt in Analytics of Audience Manager, kan worden gebruikt voor doelbezoekers. <p> <p>Opmerking: Ga naar <a href="https://survey.adobe.com/jfe/form/SV_ekBHTLSoP5Zki2y" format="http" scope="external"> https://survey.adobe.com/jfe/form/SV_ekBHTLSoP5Zki2y </a>. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Ervaring voor activiteitstype </td> 
   <td colname="col2"> <a href="/help/main/c-activities/t-experience-target/experience-target.md#task_A53DF336CB9F4D7BB87EF2106099EFC4" format="dita" scope="local"> Verschillende ervaringen op verschillende soorten publiek in één activiteit richten </a>. <p> <p>Opmerking: Dit verstrekt gelijkaardige functionaliteit aan de Landing de campagne van de Pagina in Target Advanced. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Testen van meerdere pagina's </td> 
   <td colname="col2"> <p> <a href="/help/main/c-experiences/c-visual-experience-composer/temtest.md#task_2539D51A18044F82B0D9895636546781" format="dita" scope="local"> Kies of u een test- of doelactiviteit wilt uitvoeren op een set webpagina's </a>. U kunt nu tests uitvoeren op elke productpagina of uw algemene nav wijzigen op elke pagina van de site. Gebruik een eenvoudige regelbouwer om op te geven wat de groep pagina's moet zijn. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Opgeloste problemen**

Deze release bevat de volgende opgeloste problemen:

* Probleem verholpen dat was voorkomen `target.js` niet door Edge worden gecomprimeerd.
* Probleem verholpen in rapporten die ervoor zorgden dat het aantal conversies in de rij Activiteit niet kon worden weergegeven voor A/B-activiteiten.
* Probleem verholpen waarbij een rapport niet meer werd weergegeven nadat een ervaring met gegevens was verwijderd.
* Er is een tijdelijke oplossing gemaakt om automatisch een fout in Chrome versie 34 te omzeilen waardoor pagina&#39;s met gemengde inhoud niet konden worden weergegeven. Alle versies van Chrome kunnen nu worden gebruikt.

**Bekende problemen**

Deze release bevat de volgende bekende problemen. Dit probleem wordt in een volgende update opgelost.

* Klik het volgen werkt niet aan elementen die zijn herschikt gebruikend Composer van de Visuele Ervaring. Vermijd het instellen van het bijhouden van klikken op opnieuw gerangschikte elementen totdat deze fout is opgelost.
* Er treedt een synchronisatiefout op als Geo-publiek wordt gemaakt in Target Standard wanneer de geolocatie wordt uitgeschakeld in Target Advanced.
* Kan een afbeelding niet wisselen wanneer naar de afbeelding wordt verwezen in CSS.
* Als u een afbeelding omwisselt en deze vervolgens vergroot of verkleint, worden de ervaringen in de Experience Editor niet correct weergegeven.

### Adobe [!DNL Target] Standaard 1.6 (17 maart 2014) {#section_DB1319CDD8944F6FB749E525EB551017}

Deze release bevat de volgende nieuwe functies:

| Functie | Beschrijving |
|---|---|
| Gelokaliseerde versies beschikbaar | De doelstandaard is in het Frans, Duits, Japans en Spaans gelokaliseerd |
| Vereenvoudigde implementatie | De doelstandaard is verbeterd en kan nu eenvoudiger worden geïmplementeerd voor bestaande Target Advanced-gebruikers. In de nieuwe implementatie worden uw bestaande globale vakjes gebruikt om Adobe Standard-activiteiten uit te voeren. |

**Opgeloste problemen**

Deze release bevat de volgende opgeloste problemen:

* Probleem opgelost waarbij Item verwijderen en HTML bewerken in bepaalde gevallen niet werkte.

**Bekende problemen**

Deze release bevat de volgende bekende problemen. Dit probleem wordt in een volgende update opgelost.

* De winnende werken die op Goal slechts worden gebaseerd en verandert niet gebaseerd op geselecteerde metriek.
* Klik het volgen werkt niet aan elementen die zijn herschikt gebruikend Composer van de Visuele Ervaring. Vermijd het instellen van het bijhouden van klikken op opnieuw gerangschikte elementen totdat deze fout is opgelost.
* Er treedt een synchronisatiefout op als Geo-publiek wordt gemaakt in Target Standard wanneer de geolocatie wordt uitgeschakeld in Target Advanced.
* Kan een afbeelding niet wisselen wanneer naar de afbeelding wordt verwezen in CSS.
* Het nieuwe viztarget mbox-type werkt niet met de Target Advanced/Adobe Analytics-integratie v4, de huidige versie.
* In rapporten komen de getalnotatie en de valuta in de grafiek niet overeen met de tabel als de landinstelling is ingesteld op iets anders dan de dollar.
* Het zoekvak Soorten publiek ondersteunt geen niet-ASCII-tekens.
* Voor gebruikers van de Spaanse en Japanse versie leidt het opslaan van een activiteit na het instellen van de begin- en einddatum tot een fout. U wordt aangeraden op te slaan zonder begin- en einddatum in te stellen en uw activiteit vervolgens te activeren en stop te zetten vanuit de pagina Overzicht van activiteit of Activiteitenlijst wanneer dat nodig is.

### Adobe [!DNL Target] Standaard 1.5 (25 februari 2014) {#section_5E9E3DDBCB82494AA62A21AC9282063F}

Deze release bevat de volgende nieuwe functies:

<table id="table_67115780726F48859DC8E46E34567DC3"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Functie </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Conflicten bij activiteit </td> 
   <td colname="col2"> <p> De Standaard van het doel verstrekt nu een lijst van activiteitenbotsingen. Een activiteitenbotsing komt voor wanneer de veelvoudige activiteiten opstelling zijn om inhoud aan de zelfde pagina te leveren. Als een activiteitenbotsing voorkomt, kunt u niet de verwachte inhoud op uw pagina zien omdat u een verschillende activiteit hebt ingegaan. </p> <p> Alle activiteiten op dezelfde URL worden vermeld, ongeacht de doelgroep in elke activiteit. </p> <p> Als uw activiteit botsingen bevat, a <span class="wintitle"> Botsingdetectie </span> is beschikbaar op de pagina met het activiteitenoverzicht. Open dit tabblad voor een lijst met activiteiten die botsen. Klik op een activiteit in de lijst om de overzichtspagina voor die activiteit weer te geven. </p> <p>Zie <a href="/help/main/c-experiences/c-visual-experience-composer/activity-collisions.md#concept_0BC6B929592744DFA7DA01FF4F91052E" format="dita" scope="local"> Activiteitenconflicten </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Nieuwe doelopties: Profiel, gebruiker </td> 
   <td colname="col2"> U kunt nu profiel- en gebruikersparameters als doel instellen. Zie <a href="/help/main/c-target/c-audiences/audiences.md#concept_65BE870D290E412D8BBF557EEA67C271" format="dita" scope="local"> Soorten publiek </a>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Elementen invoegen </td> 
   <td colname="col2"> <p>U kunt nu elk element aan uw pagina toevoegen en de bestaande inhoud wijzigen. Voeg tekst, code, lijsten en meer toe om geheel verschillende ervaringen te maken die u wilt testen. </p> <p>Zie <a href="/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md#reference_3BD1BEEAFA584A749ED2D08F14732E81" format="dita" scope="local"> Opties voor composer visuele ervaring </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

Deze release bevat de volgende bekende problemen. Dit probleem wordt in een volgende update opgelost.

* De winnende werken die op Goal slechts worden gebaseerd en verandert niet gebaseerd op geselecteerde metriek.
* Klik het volgen werkt niet aan elementen die zijn herschikt gebruikend Composer van de Visuele Ervaring. Vermijd het instellen van het bijhouden van klikken op opnieuw gerangschikte elementen totdat deze fout is opgelost.
* Er treedt een synchronisatiefout op als Geo-publiek wordt gemaakt in Target Standard wanneer de geolocatie wordt uitgeschakeld in Target Advanced.
* Kan een afbeelding niet wisselen wanneer naar de afbeelding wordt verwezen in CSS.

### Adobe [!DNL Target] Standaard 1.4 (20 januari 2014) {#section_CD27AEE32B4F40BDAB422711B96739A5}

Deze release bevat de volgende nieuwe functies en verbeteringen:

<table id="table_9E303FF0CD954795A29369A6D4166DB5"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Functie </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Schatting van inkomstenbelasting </td> 
   <td colname="col2"> <p>Doel kan een schatting maken van de inkomstenbelasting die u kunt bereiken als alle gebruikers de winnende ervaring bekijken. </p> <p>In deze schatting wordt de hoeveelheid lift berekend die door de winnende ervaring wordt behaald en het totale aantal bezoekers gedurende de duur van de test, en wordt de lift weergegeven die u kunt behalen als elke bezoeker de winnende ervaring ziet, als de trends doorzetten zoals ze tijdens de test hebben. </p> <p> De juistheid van de raming hangt af van een aantal factoren, waaronder de geraamde cijfers indien de huidige tendensen aanhouden. Deze waarden zijn schattingen op basis van de in het verleden behaalde resultaten en mogen niet worden gebruikt voor financiële richtsnoeren. Toekomstige resultaten kunnen afwijken. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> Ongedaan maken/Opnieuw </td> 
   <td colname="col2"> <p>Tijdens een bewerkingssessie kunt u wijzigingen in uw activiteiten ongedaan maken. U kunt ongedaan gemaakte wijzigingen ook opnieuw uitvoeren. </p> <p>Zie <a href="/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md#reference_3BD1BEEAFA584A749ED2D08F14732E81" format="dita" scope="local"> Opties voor composer visuele ervaring </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Element verplaatsen </td> 
   <td colname="col2"> <p>U kunt elementen op uw pagina verplaatsen. In tegenstelling tot Elements herschikken, verschuift Verplaatsen andere elementen niet om ruimte te maken voor het element dat wordt verplaatst. Gebruik de pijltoetsen om de verplaatsing te verfijnen. </p> <p>Zie <a href="/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md#reference_3BD1BEEAFA584A749ED2D08F14732E81" format="dita" scope="local"> Opties voor composer visuele ervaring </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Element vergroten/verkleinen </td> 
   <td colname="col2"> <p>U kunt het formaat van een element op uw pagina wijzigen. Wanneer u Formaat wijzigen selecteert, wordt een greep weergegeven in een hoek van het element waarmee u die hoek kunt slepen om het formaat te wijzigen. </p> <p>Zie <a href="/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md#reference_3BD1BEEAFA584A749ED2D08F14732E81" format="dita" scope="local"> Opties voor composer visuele ervaring </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Een locatie kiezen bij het instellen van een publiek </td> 
   <td colname="col2"> <p>Wanneer u een publiek maakt, kunt u een locatie (mbox) selecteren en parameters voor die locatie opgeven. </p> <p>Zie <a href="/help/main/c-target/c-audiences/create-audience.md#task_1D507519D3AD4390B507F188BD294DC1" format="dita" scope="local"> Een nieuw publiek maken </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Koppelingen voorvertonen (verbetering) </td> 
   <td colname="col2"> <p>Voorvertoning van koppelingen werkt naar behoren. </p> </td> 
  </tr> 
 </tbody> 
</table>

Deze release bevat de volgende oplossingen:

* Correctie van problemen waardoor voorvertoningskoppelingen niet naar behoren konden worden weergegeven.

Deze release bevat de volgende bekende problemen. Deze problemen worden in een volgende update opgelost.

* Als Geschatte Lift in de Norm van het Doel wordt toegelaten, en Target Advanced aan een verschillende tijdzone dan browser van de gebruiker wordt geplaatst, zou de voorspelde opbrengstwaarde niet op de lijst van Activiteiten of in de de statusbar van Rapporten voor maximaal één volledige dag kunnen verschijnen. Omdat de Mening van het Rapport datum maar niet tijd gebruikt, verschijnen de gegevens in de Mening van het Rapport maar niet voor geprojecteerde lift.
* Klik het volgen werkt niet aan elementen die zijn herschikt gebruikend Composer van de Visuele Ervaring. Vermijd het instellen van het bijhouden van klikken op opnieuw gerangschikte elementen totdat deze fout is opgelost.
* Er treedt een synchronisatiefout op als Geo-publiek wordt gemaakt in Target Standard wanneer de geolocatie wordt uitgeschakeld in Target Advanced.
* Kan een afbeelding niet wisselen wanneer naar de afbeelding wordt verwezen in CSS.

## Uitzettingen 2013

### Adobe [!DNL Target] Standaard 1.3 (19 november 2013) {#section_D633ACA56FA941648219EB3748D814EC}

Deze release bevat de volgende nieuwe functies en verbeteringen:

| Functie | Beschrijving |
|---|---|
| Geo-targeting | Doel op land, staat, plaats, postcode, of DMA. |
| Gebruik Composer visuele ervaring om elementen opnieuw te rangschikken. | U kunt kindelementen binnen hun ouderelement opnieuw rangschikken gebruikend de Visuele Composer van de Ervaring. |
| Rechtstreeks op uw site wordt een voorvertoning weergegeven. | Nadat u een activiteit hebt opgeslagen, kunt u deze direct op uw site bekijken, zelfs als de activiteit niet actief is. Op deze manier kunt u zien hoe het eruitziet, zonder dat dit via een iFrame wordt weergegeven. U kunt koppelingen naar elke testervaring kopiëren om die ervaringen in uw browser te bekijken of om ze naar uw teamleden te sturen zodat ze deze kunnen bekijken. Personen die deze pagina&#39;s weergeven, worden niet meegeteld in de rapporten. |

Deze release bevat de volgende oplossingen:

* Probleem verholpen waarbij de metrische gegevens voor het bijhouden van klikken niet uit een activiteit zijn verwijderd als de URL voor de ervaring opnieuw is ingesteld.
* Probleem verholpen in de ervaringscomposer die ervoor zorgde dat de standaardervaring snel flitst voordat nieuwe inhoud wordt weergegeven tijdens het navigeren door ervaringen.

Deze release bevat de volgende bekende problemen. Deze problemen worden in een volgende update opgelost.

* Er treedt een synchronisatiefout op als Geo-publiek wordt gemaakt in Target Standard wanneer de geolocatie wordt uitgeschakeld in Target Advanced.
* Kan een afbeelding niet wisselen wanneer naar de afbeelding wordt verwezen in CSS.
* Klik het volgen werkt niet aan elementen die zijn herschikt gebruikend Composer van de Visuele Ervaring. Vermijd het instellen van het bijhouden van klikken op opnieuw gerangschikte elementen totdat deze fout is opgelost.
* Gebruikers kunnen de **[!UICONTROL Remove]** actie voor inhoud die in een mbox verpakt is.

### Adobe [!DNL Target] Standaard 1.2 (31 oktober 2013) {#section_420B5E910D7341AA8DB059C8E1071D53}

Er zijn vier bekende problemen met deze release. Deze problemen worden in een volgende update opgelost.

* Op sommige clusters wordt het bewerken van een herbruikbare aanbieding mogelijk niet weerspiegeld op de locatie van de klant voor activiteiten die buiten een box worden aangeboden.
* Als u afbeeldingen omwisselt in een gebied van een pagina die niet door een box wordt beheerd, treedt mogelijk een fout van 404 op.
* Wanneer u een nieuw publiek maakt of een bestaand publiek bewerkt en opslaat, wordt dit pas weergegeven in de lijst Soorten publiek als u het scherm vernieuwt of naar het publiek zoekt.
* Wanneer u een aanbieding van de HTML van de Norm van het Doel schrapt, wordt het niet geschrapt van Target Advanced.

Deze release bevat de volgende correcties en verbeteringen:

* Meerdere problemen verholpen die ertoe leidden dat sommige activiteiten en ervaringen niet correct werden gesynchroniseerd met Target Advanced.
* Probleem verholpen waarbij [!DNL target.js] Hiermee worden andere scripts uit het deelvenster `<head>` van een pagina.

* Probleem verholpen waarbij bepaalde middelen waarnaar wordt verwezen, werden gekopieerd wanneer een activiteit wordt gekopieerd.
* Probleem verholpen waarbij het bijwerken van inhoud van een bijgewerkte afbeelding zowel in Scene7 als in Target Advanced werd mislukt.
* Probleem verholpen waarbij door het toepassen van een zoekfilter het publiek dat is geselecteerd in &quot;Soorten publiek voor rapportage&quot;, werd gewist.
* Verbeterde grafieken worden standaard op uurresultaten toegepast wanneer een test minder dan twee dagen actief is geweest.
* Probleem verholpen waarbij het kopiëren van een niet-gesynchroniseerde activiteit mislukte.
* Toegevoegde functionaliteit voor toetsenbordinvoer voor vervolgkeuzemenu&#39;s voor locatie.
* Verbeterde de foutmelding die wordt weergegeven wanneer u een aanbieding verwijdert die in een activiteit wordt gebruikt.

### Adobe [!DNL Target] Standaard 1.1 (18 oktober 2013) {#section_79FA6A61D2284D41A34F00014A342F07}

Deze release bevat de volgende correcties en verbeteringen:

* Probleem verholpen waarbij activiteitensynchronisatie mislukte tijdens de eerste synchronisatiepoging nadat er geldige ervaringen waren toegevoegd aan een gedeeltelijke activiteit.
* Probleem verholpen waarbij 500 fouten in het rapport Samenvatting werden gegenereerd nadat een ervaring was verwijderd en toegevoegd.
* Probleem verholpen dat onnauwkeurige bezoekersgegevens veroorzaakte wanneer een bezoeker meerdere ervaringen bekijkt.
* De begin- en eindtijd van de activiteit synchroniseren nu correct tussen Standaard en Geavanceerd.
* De weergave van gemengde inhoud is verbeterd.
* Probleem verholpen waarbij de Visual Experience Composer niet goed functioneerde als JavaScript in de HTML-code de browserdefinitie van het JSON-object overschrijft.
* Probleem verholpen waarbij het weergegeven aantal activiteiten onjuist was tijdens het sorteren op status.
* Probleem verholpen waarbij witruimte in het veld Doel niet correct werd gevalideerd.
* Probleem verholpen waarbij meerdere aanbiedingen voor één functie werden gemaakt in Geavanceerd toen de afbeelding werd gewisseld.
* Probleem verholpen waarbij de zoekopdracht ertoe leidde dat er niet aan afbeeldingen in de inhoudkiezer werd gewerkt.
* Probleem verholpen waarbij de volgorde van de omgekeerde activiteitslijst werd gewijzigd bij het sorteren op naam of status.
* Probleem verholpen waarbij anonieme aanbiedingen niet werden verwijderd wanneer ze niet meer in een activiteit werden gebruikt.
* Probleem verholpen waarbij een onjuiste ervaringsnaam werd weergegeven op een gedeelde kaart tijdens het bewerken van een activiteit.
* Probleem verholpen waarbij de inhoud in Scene7 en Target Advanced niet correct werd bijgewerkt in een bijgewerkte afbeeldingsaanbieding.
* Probleem verholpen waarbij bij het kopiëren van een afbeeldingselement ook Scene7-gerelateerde eigenschappen werden gekopieerd die niet hadden mogen worden gekopieerd.
