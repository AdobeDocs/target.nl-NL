---
keywords: releaseopmerkingen;nieuwe functies;releases;updates;update;release;verbetering;verbeteringen;correcties;foutoplossingen;updates;huidige updates
description: Leer over de nieuwe eigenschappen, de verhogingen, en de moeilijke situaties inbegrepen in de huidige versie van  [!DNL Adobe Target], met inbegrip van SDKs, APIs, en de bibliotheken van JavaScript.
landing-page-description: Leer over de nieuwe eigenschappen, de verhogingen, en de moeilijke situaties inbegrepen in de huidige versie van  [!DNL Adobe Target].
short-description: Leer over de nieuwe eigenschappen, de verhogingen, en de moeilijke situaties inbegrepen in de huidige versie van  [!DNL Target].
title: Wat is inbegrepen in de huidige Versie?
feature: Release Notes
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
source-git-commit: 693b862bc39fc3b1b7d93988bd80cdd51657354b
workflow-type: tm+mt
source-wordcount: '1430'
ht-degree: 0%

---

# [!DNL Target] releaseopmerkingen (huidig)

Ontdek de nieuwste functies, verbeteringen en oplossingen in [!DNL Adobe Target] . Deze releaseopmerkingen hebben ook betrekking op updates van [!DNL Target] API&#39;s, SDK&#39;s, de [!DNL Adobe Experience Platform Web SDK] , at.js en andere platformcomponenten, indien van toepassing.

(De uitgiftenummers tussen haakjes zijn bedoeld voor intern gebruik door [!DNL Adobe] .)

## Tijdgevoelige updates die u moet weten {#time-sensitive}

[!BADGE &#x200B; Belangrijk &#x200B;]{type=Informative}

Voor tijdgevoelige updates die betrekking hebben op [!DNL Adobe Target] en uw implementatie, verschaft [!DNL Adobe] gedetailleerde opmerkingen en documentatie bij de release via [!UICONTROL Experience League] . Hier volgen enkele belangrijke punten die relevant zijn voor uw implementatie:

### Veroudering van interfaceversie [!DNL Target] in-/uitschakelen

Voor meer informatie, zie [[!DNL Target]  UI update FAQs &#x200B;](/help/main/c-intro/updated-ui-faq.md).

## [!DNL Target Standard/Premium] 25.11.1 (10 november 2025)


**Analytics voor Doel (A4T)**

+++Zie details
* **[!UICONTROL Goals & Settings]foutbericht wanneer u [!DNL Adobe Analytics] als rapportbron in bijgewerkte gebruikersinterface gebruikt.** Oplossing voor een probleem in de bijgewerkte gebruikersinterface van [!UICONTROL Overview] waarin in de sectie Doelen de fout &#39;&#39;Er is iets misgegaan&#39;&#39; werd weergegeven. Je aanvraag kan niet worden voltooid. Neem contact op met [!DNL Adobe Client Care] als het probleem zich blijft voordoen&quot; wanneer [!DNL Adobe Analytics] (A4T) als rapportbron is geselecteerd. De doelen worden nu correct weergegeven met [!UICONTROL Adobe Analytics] -meetwaarden, zodat ze consistent zichtbaar zijn voor alle rapportbronnen. (TGT-54021)

+++

**Soorten publiek**

+++Zie details
* **Onbekwaam om veelvoudige rapporteringspubliek in bijgewerkte UI te selecteren.** Oplossing voor een probleem in de bijgewerkte gebruikersinterface waarbij gebruikers niet meerdere nieuw gecreëerde rapportagesoorten tegelijk konden selecteren tijdens het bewerken van een activiteit. Meerdere doelgroepen kunnen nu tegelijk worden toegewezen, waardoor de flexibiliteit en efficiëntie van de rapportinstellingen worden verbeterd. (TGT-53253)

+++

**Beslissende aanbiedingen**

+++Zie details
* **Onbekwaam om besluitaanbiedingen in bijgewerkte UI uit te geven of te vervangen.** Oplossing voor een probleem in de bijgewerkte gebruikersinterface dat ertoe leidde dat beslissingsvoorstellen niet konden worden bewerkt of vervangen via het deelvenster [!UICONTROL Modifications] . De aanbiedingsnamen werden leeg weergegeven. Beslissingsaanbiedingen zijn nu volledig toegankelijk en bewerkbaar, zodat ze pariteit herstellen met de oudere gebruikersinterface en ervoor zorgen dat klanten aanbiedingen rechtstreeks binnen activiteiten kunnen beheren. (TGT-53884)

+++

**Localization**

+++Zie details
* **Correcteerde verscheidene localisatiefouten in Koreaans en Japans UI.** (TGT-54003, TGT-54004, TGT-54006, TGT-54007 en TGT-54018)

+++

**[!UICONTROL Recommendations]**

+++Zie details
* **Bevordering door Attribuut met de Vergelijking van Attributen van de Entiteit ontbrak om aanbeveling sleutel na activiteit te laden sparen.** Oplossing voor een probleem waarbij speciale acties van het type [!UICONTROL Promotion by Attribute] met regeltype [!UICONTROL Entity Attribute Matching] de aanbevelingssleutel niet laden na het opslaan van een activiteit. Het probleem is veroorzaakt doordat `customKeyId` niet via GraphQL is aangevraagd. Aanbevelingssleutels worden nu correct geladen tijdens promotiebewerkingen. (TGT-53117)
* **Aanbeveling blijft visueel voortbestaan wanneer het schakelen van ExpB aan ExpA.** Oplossing voor een probleem waarbij het invoegen van een aanbeveling in Experience B en het overschakelen naar Experience A het vak met de aanbevolen aanbieding zichtbaar maakten. Dit was slechts een visuele inconsistentie; de wijzigingen geven nu correct terug wanneer het schakelen tussen ervaringen, die nauwkeurige gedrag UI verzekeren. (TGT-53911)
* **de sleutel van de Aanbeveling laadt niet voor [!UICONTROL Promotion by Attribute] met [!UICONTROL Entity Attribute] Vergelijking.** Oplossing voor een probleem waarbij promoties van het type [!UICONTROL Promotion by Attribute] met regeltype [!UICONTROL Entity Attribute Matching] de aanbevelingssleutel niet laden als ze werden bewerkt nadat een activiteit was opgeslagen. De sleutel van de aanbeveling wordt nu correct teruggewonnen door GraphQL, die bevorderingsvertoning verzekert en functioneert zoals verwacht. (TGT-53917)
* **het uitgeven aanbevelingen op verborgen elementen van HTML die niet in bijgewerkte UI werken.** Oplossing voor een probleem in de gebruikersinterface van [!UICONTROL New Create] en VEC dat adviesactiviteiten die zijn toegepast op verborgen HTML-elementen niet konden worden bewerkt. Deze functionaliteit werkt nu zoals verwacht, waarbij de pariteit met de oudere UI wordt hersteld en wordt gecontroleerd of aanbevelingen kunnen worden gewijzigd, ongeacht de zichtbaarheid van elementen. (TGT-53953)
* **Onbekwaam om aanbevelingsactiviteiten op verborgen elementen van HTML in bijgewerkte UI uit te geven.** Oplossing voor een probleem in de bijgewerkte gebruikersinterface waarin de aanbevolen activiteiten die op verborgen HTML-elementen zijn toegepast, niet konden worden bewerkt. Deze functionaliteit werkt nu zoals verwacht, waarbij de pariteit met de oudere UI wordt hersteld en wordt gecontroleerd of aanbevelingen kunnen worden gewijzigd, ongeacht de zichtbaarheid van elementen. (TGT-53951)
* **de catalogus van de Aanbeveling mist periodiek kenmerkwaarden in bijgewerkte UI.** Oplossing voor een probleem in de bijgewerkte gebruikersinterface van [!UICONTROL Recommendations] waarbij zoekopdrachten in catalogi soms bepaalde kenmerkwaarden (bijvoorbeeld bericht) niet konden weergeven, zelfs niet als deze in de productreeks stonden. Kenmerkwaarden worden nu consistent geladen in zoekresultaten zonder dat de kolom opnieuw moet worden geconfigureerd, waardoor de betrouwbaarheid en efficiëntie voor het catalogusbeheer worden verbeterd. (TGT-52769)
* **[!UICONTROL Download Recommendations]ontbreekt voor [!DNL Recommendations] -activiteiten in de bijgewerkte gebruikersinterface.** Oplossing voor een probleem in de bijgewerkte [!DNL Recommendations] UI waarbij de knop [!UICONTROL Download Recommendations] niet zichtbaar was voor A/B-activiteiten aan de hand van aanbevelingen. De knop wordt nu op de juiste wijze weergegeven, zodat gebruikers aanbevelingen kunnen exporteren zoals verwacht, in overeenstemming met de functionaliteit in de oudere gebruikersinterface. (TGT-53768)
* **[!UICONTROL Download Recommendation Data]ontbreekt in de bijgewerkte interface van het Overzicht.** Oplossing voor een probleem in de bijgewerkte [!UICONTROL Overview] UI waarbij de knop [!UICONTROL Download Recommendation Data] niet zichtbaar was voor activiteiten met aanbevelingen. De knop wordt nu op de juiste wijze weergegeven, zodat gebruikers de gegevens met aanbevelingen rechtstreeks kunnen exporteren zonder terug te moeten schakelen naar de oudere gebruikersinterface. (TGT-53772)
* **het uitgeven activiteitencriteria resulteerden soms in leeg scherm in bijgewerkte UI.** Oplossing voor een probleem in de bijgewerkte gebruikersinterface dat er soms leidde tot een leeg scherm wanneer u op [!UICONTROL Edit Criteria in Experiences] klikte voor bepaalde activiteiten. De criteria-editor wordt nu betrouwbaar geladen voor alle activiteiten, zodat gebruikers deze zonder onderbreking kunnen bewerken. (TGT-53961)
* **Onbekwaam om opeenvolgingscriteria in bijgewerkte UI uit te geven.** Oplossing voor een probleem in de bijgewerkte gebruikersinterface waarbij het bewerken van [!UICONTROL Sequence Criteria] ertoe leidde dat popup met criteria vastliep tijdens het laden en vervolgens een leeg scherm weergaf. De criteria-editor wordt nu correct geladen, zodat gebruikers de criteria van de reeks zonder onderbreking kunnen bewerken en bijwerken. (TGT-53985)

+++

**[!UICONTROL Reports]**

+++Zie details
* **[!UICONTROL Multivariate Test] (MVT) plaatsen en grafiekrapporteringskwestie verhinderden rapportgeneratie.** Oplossing voor een probleem waarbij MVT-activiteiten [!UICONTROL Location Contribution] en Grafiekrapporten niet konden genereren in de doelinterface en de fout &#39;Er is iets fout opgetreden. We kunnen uw verzoek niet voltooien.&quot; Rapporten worden nu correct geladen in de gebruikersinterface en zorgen voor volledige zichtbaarheid. (TGT-53654)
* **MVT meldt niet ladend wegens [!UICONTROL Element] fout van het bijdragerapport.** Oplossing voor een probleem waarbij MVT-activiteitenrapporten niet konden worden geladen in de doelinterface en waarbij de fout &quot;Rapport voor elementbijdrage kon niet worden opgehaald&quot; werd weergegeven. Rapporten worden nu correct weergegeven, zodat de bijdragen aan elementen volledig zichtbaar zijn. (TGT-53691)
* **de orderdetails van de uitvoer aan CSV kwestie voor [!UICONTROL Experience Targeting] (XT) activiteiten.** Oplossing voor een probleem waarbij de optie [!UICONTROL Export Order Details to CSV] onjuist werd weergegeven voor XT-activiteiten en een leeg bestand werd geretourneerd. De optie wordt nu alleen weergegeven voor AP-activiteiten, zodat nauwkeurige exportfunctionaliteit wordt gegarandeerd en verwarring wordt voorkomen. (TGT-53798)

+++

**[!UICONTROL Visual Experience Composer] (VEC)**

+++Zie details
* **[!UICONTROL Delete Modification]. Kan wijzigingen in de activiteit niet verwijderen.** Oplossing voor een probleem waarbij de knop [!UICONTROL Delete Modification] in de gebruikersinterface [!DNL Target] niet werkte, zodat gebruikers geen wijzigingen binnen activiteiten konden verwijderen. De knop werkt nu zoals u had verwacht, zodat wijzigingen zonder vertraging op betrouwbare wijze kunnen worden verwijderd. (TGT-53728)
* **Gewenste selecteurs niet erkend in bijgewerkte UI.** Oplossing voor een probleem in de bijgewerkte gebruikersinterface waarbij voorkeurskiezers, zoals `data-target-component-id` , niet werden weergegeven in de lijst met CSS-kiezers in de VEC. De gebruikers kunnen aangewezen attributen in plaats van dynamisch geproduceerde klassennamen nu betrouwbaar selecteren, die het stabiele richten over de pagina van het KUUROORD updates verzekeren. (TGT-53908)
* De **de plaatshulding van de Activiteit tussen [!UICONTROL Edit] en [!UICONTROL Overview] pagina&#39;s.** Oplossing voor een probleem waarbij de paginanummering van de locatie van de activiteit op de [!UICONTROL Overview] -pagina niet werd uitgelijnd met updates die op de [!UICONTROL &#x200B; Edit Experience] -pagina zijn aangebracht. Locaties blijven nu consistent in beide weergaven, zodat u nauwkeurige uitlijning kunt toepassen en ontbrekende of onjuist genummerde posities kunt voorkomen. (TGT-53960 &amp; TGT-53954)
* **Kon niet terug naar [!UICONTROL Design] wijze in bijgewerkte VEC.** Oplossing voor een probleem in de bijgewerkte VEC-gebruikersinterface waarbij gebruikers na het navigeren naar een nieuwe pagina in de modus [!UICONTROL Design] niet konden terugschakelen naar de [!UICONTROL Browse] -modus. De schakeloptie [!UICONTROL Design] werkt nu correct, zodat wijzigingen naadloos op alle pagina&#39;s kunnen worden toegepast. (TGT-53988 &amp; TGT-53993)
* **parameter van de Vraag niet getoond in activiteitenoverzicht.** Oplossing voor een probleem in de bijgewerkte gebruikersinterface dat er op de pagina van [!UICONTROL Overview] geen parameters voor query&#39;s werden weergegeven, waardoor er discrepanties ontstonden tussen de URL&#39;s voor query&#39;s van [!UICONTROL Overview] en van de pagina. De parameters van de vraag tonen nu correct, die ervoor zorgen de activiteitenplaatsen volledig worden vertegenwoordigd en over meningen verenigbaar zijn. (TGT-53701)

+++

## Aanvullende opmerkingen bij de release en versiedetails

| Bron | Details |
|--- |--- |
| [&#x200B; de nota&#39;s van de Versie: De Ervaring van het Platform van Adobe Target Web SDK &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=nl-NL) | Details over veranderingen in elke versie van het Web SDK van het Platform. |
| [&#x200B; at.js versiedetails &#x200B;](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html?lang=nl-NL){target=_blank} | Informatie over de wijzigingen in elke versie van de JavaScript-bibliotheek [!DNL Adobe Target] at.js. |

## Documentatiewijzigingen, Opmerkingen bij de vorige release en Opmerkingen bij de release van Experience Cloud

Naast de notities voor elke release bevatten de volgende bronnen aanvullende informatie:

| Bron | Details |
|--- |--- |
| [&#x200B; Veranderingen van de Documentatie &#x200B;](/help/main/r-release-notes/doc-change.md) | Gedetailleerde informatie weergeven over updates van deze handleiding die niet zijn opgenomen in deze releaseopmerkingen. |
| [&#x200B; de nota&#39;s van de Versie voor vorige versies &#x200B;](/help/main/r-release-notes/release-notes-for-previous-releases.md). | Informatie weergeven over nieuwe functies en verbeteringen in vorige versies van Target Standard en Target Premium. |
| [&#x200B; de Nota&#39;s van de Versie van Adobe Experience Cloud &#x200B;](https://experienceleague.adobe.com/docs/release-notes/experience-cloud/current.html?lang=nl-NL){target=_blank} | Bekijk de nieuwste releaseopmerkingen voor de Adobe Experience Cloud-oplossingen. |

## Prerelease-informatie {#section_5D588F0415A2435B851A4D0113ACA3A0}

De volgende middelen laten u zien wat in de volgende versie van het Doel komt.

| Bron | Details |
|--- |--- |
| [&#x200B; de Prioritaire Update van het Product van Adobe &#x200B;](https://www.adobe.com/subscription/priority-product-update.html){target=_blank} | Ontvang voorafgaande meldingen over aanstaande productverbeteringen voor [!DNL Target] en andere [!DNL Adobe Experience Cloud] -oplossingen. |
| [&#x200B; de Nota&#39;s van de Versie van het Doel - preRelease &#x200B;](/help/main/r-release-notes/target-release-notes.md){target=_blank} | Informatie over de versies van het Doel van de huidige maand, met inbegrip van pre-releaseinformatie. |
