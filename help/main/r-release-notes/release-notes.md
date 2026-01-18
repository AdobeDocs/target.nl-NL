---
keywords: releaseopmerkingen;nieuwe functies;releases;updates;update;release;verbetering;verbeteringen;correcties;foutoplossingen;updates;huidige updates
description: Leer over de nieuwe eigenschappen, de verhogingen, en de moeilijke situaties inbegrepen in de huidige versie van  [!DNL Adobe Target], met inbegrip van SDKs, APIs, en de bibliotheken van JavaScript.
landing-page-description: Leer over de nieuwe eigenschappen, de verhogingen, en de moeilijke situaties inbegrepen in de huidige versie van  [!DNL Adobe Target].
short-description: Leer over de nieuwe eigenschappen, de verhogingen, en de moeilijke situaties inbegrepen in de huidige versie van  [!DNL Target].
title: Wat is inbegrepen in de huidige Versie?
feature: Release Notes
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
source-git-commit: 550fa1e8d4127babe02403708b73862505bf8c99
workflow-type: tm+mt
source-wordcount: '1772'
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

## [!DNL Target Standard/Premium] 26.1.1 (18 januari 2026)

**Activiteiten**

+++Zie details

* **Onbekwaam om activiteit te kopiëren - ongeldige gebruikersinput.** Het probleem waarbij gebruikers een onhandige fout in de gebruikersinvoer zien wanneer ze een activiteit kopiëren, is opgelost. Eerder, toen een activiteit werd gedupliceerd, werden zijn werkruimte-specifieke bezitstoewijzingen niet bewaard, veroorzakend het achtereind om sparen verzoek te verwerpen omdat ABActivity minstens één bezit vereist die tot een niet-gebrek werkruimte behoort. Dit probleem teweegbracht een generische fout in UI teweeg, verlatend gebruikers zonder begeleiding. Met deze correctie blijven werkruimtetoewijzingen tijdens kopieerbewerkingen op de juiste wijze behouden, zodat gebruikers de gekopieerde activiteit zonder wijzigingen kunnen opslaan en misleidende validatiefouten worden voorkomen. (TGT-54282)
* **laat werkruimtekolom de Web editoraanbieding toe.** Deze update verhelpt klantverwarring die wordt veroorzaakt door aanbiedingen van [!UICONTROL Default Workspace] die in andere werkruimten in de webeditor worden weergegeven. Hoewel dit gedrag werkt zoals het is ontworpen, zijn de aanbiedingen van [!UICONTROL Default Workspace] bewust zichtbaar over alle werkruimten, rapporteerden de klanten dat UI werkruimteoorsprong niet duidelijk maakte, vooral wanneer het creëren van activiteiten in een niet-standaardwerkruimte zoals &quot;Approvers.&quot; Om de duidelijkheid te verbeteren, is de kolom [!UICONTROL Workspace] nu toegelaten in de de aanbiedingslijst van de Redacteur van het Web, die gebruikers toestaat om gemakkelijk te onderscheiden welke werkruimte elke aanbieding tot behoort en misinterpretatie van de extra getoonde aanbiedingen te verhinderen. (TGT-54138)
* **Verbindingen met doel=&quot;_blank&quot;open in een nieuw lusje.** Deze moeilijke situatie verhelpt een kwestie waar authored websites die verbindingen met ~ target= &quot;_blank&quot;~ bevatten op een nieuw browser lusje zouden openen wanneer geklikt op [!UICONTROL Browse] wijze, die de ervaring van de in-redacteursvoorproef onderbreken. Het gedrag trad op omdat de native koppelingskenmerken van de geschreven pagina niet werden onderschept door de geïnjecteerde JavaScript van de extensie, in tegenstelling tot in de oudere UI waar ankerelementen werden getransformeerd en hun doelen werden overschreven om navigatie binnen de editor te houden. De update zorgt ervoor dat de verbindingen die ~ gebruiken target= &quot;_blank&quot;~ nu behoorlijk binnen de Redacteur van het Web worden behandeld zodat openen zij externe lusjes niet meer tijdens het ontwerpen. (TGT-54134)
* **schrap de waarschuwing van het Bezit.** Deze update introduceert een visuele waarschuwing om gebruikers duidelijk te informeren wanneer ze een automatisch gedetecteerde eigenschap in de Activiteiteneditor uitschakelen. Eerder, die een auto-ontdekte bezit verwijdert voorzag geen aanwijzing dat het bezit permanent zou worden geschrapt, dat c0zou leiden tot toevallig verlies van het richten configuratie. Met deze correctie wordt een waarschuwingspictogram toegevoegd dat consistent is met het gedrag in de verouderde gebruikersinterface om gebruikers te laten weten dat de selectie van de eigenschap de toepassing uit de activiteit verwijdert. (TGT-54121)
* **[!UICONTROL Workspaces]-vervolgkeuzelijst is beperkt tot 20 in de [!UICONTROL Users] -sectie.** Met deze oplossing verhelpt u een probleem waarbij het vervolgkeuzemenu [!UICONTROL Workspaces] in de sectie [!UICONTROL Administration] > [!UICONTROL Users] slechts 20 werkruimten weergeeft, zelfs als een gebruiker toegang tot nog veel meer werkruimten had. De onderliggende GraphQL-aanroep naar `licenseGroups` was ook beperkt tot 20 resultaten, waardoor de gebruikersinterface een onvolledige lijst weergeeft ondanks dat de gebruiker toegang heeft tot meer werkruimten in de organisatie. De update verwijdert deze vaste limiet zodat de volledige set beschikbare werkruimten nu wordt geretourneerd en correct wordt weergegeven. (TGT-53820)
* **Vaste een kwestie waar de aanbiedingen modaal niet de werkruimtekollom tonen.** Oplossing voor een probleem waarbij de kolom met werkruimte in de bijgewerkte gebruikersinterface niet werd weergegeven met de modale aanbiedingsmodus. Dit leidde tot verwarring voor klanten omdat aanbiedingen van [!UICONTROL Default Workspace] naast aanbiedingen van de geselecteerde werkruimte werden weergegeven zonder aanduiding van hun oorsprong. De werkruimtekolom is nu ingeschakeld, zodat klanten duidelijk kunnen aangeven tot welke werkruimte elk aanbod behoort. (TGT-52320)

+++

**Eigenschappen**

+++Zie details
* **de Activiteit geeft zou geen auto-ontdekt bezit moeten toevoegen als reeds verwijderd.** Met deze correctie wordt een probleem verholpen waarbij bij het bewerken van een activiteit automatisch een automatisch gedetecteerde eigenschap wordt geïntroduceerd die de gebruiker eerder had verwijderd. Wanneer een activiteit opnieuw wordt geopend voor bewerking, heeft het systeem de verwijderde eigenschap onjuist hersteld, wat leidt tot inconsequent gedrag en verwarring in de [!UICONTROL Properties List] . De update zorgt ervoor dat een automatisch gedetecteerde eigenschap wordt verwijderd als deze tijdens alle volgende bewerkingen wordt verwijderd en niet opnieuw wordt weergegeven, tenzij de gebruiker deze expliciet terugvoegt. (TGT-54182)
* **voeg auto-ontdekte eigenschappen niet toe als reeds verwijderd.** Met deze correctie zorgt u ervoor dat een automatisch gedetecteerde eigenschap niet meer door het systeem wordt geïntroduceerd tijdens volgende navigatie in de activiteiteneditor nadat een gebruiker handmatig een automatisch gedetecteerde eigenschap heeft verwijderd uit een activiteit. Eerder, als een gebruiker een auto-ontdekte bezit schrapte, aan de [!UICONTROL Targeting] stap werd verplaatst, en toen aan [!UICONTROL Experiences] terugkwam, zou de redacteur de verwijderde eigenschap herhalen die op de auto-ontdekte lijst wordt gebaseerd die in het de staatssegment van de Redacteur van de Activiteit wordt opgeslagen. De bijgewerkte logica vergelijkt nu de auto-ontdekte eigenschappen met de huidige eigenschappen in het ~ ~ segment ActivityState en verhindert het opnieuw toevoegen van om het even welk auto-ontdekt bezit dat de gebruiker reeds heeft verwijderd. Dit resulteert in consistent gedrag in verschillende stappen en houdt rekening met de intentie van de gebruiker. (TGT-54181)
* **voeg auto-ontdekte tekst in de eigenschappenlijst toe.** Deze verbetering werkt [!UICONTROL Properties List] bij om eigenschappen duidelijk te etiketteren die automatisch door het systeem werden ontdekt. Wanneer een auto-ontdekt bezit ook in user-visible [!UICONTROL Properties List] aanwezig is, toont het nu de &quot;(Auto-Gedetecteerd)&quot;tekst naast zijn naam, gebruikend de waarde die in de ~ wordt opgeslagen ActivityEditorSegment ~ staat. Dit weerspiegelt het gedrag van erfenis UI en helpt gebruikers gemakkelijk tussen manueel geselecteerde eigenschappen en die eigenschappen onderscheiden die automatisch worden geïdentificeerd. (TGT-54120)
* **voeg auto-ontdekt [!UICONTROL Properties] in het staat toe.** Deze update zorgt ervoor dat de {~ staat 1} ActivityEditorSlice.ExperienceEditor constant een bijgewerkte lijst van alle auto-ontdekte bezit IDs handhaaft die van de Redacteur van het Web in het lusje van de Activiteit ~ worden overgegaan. [!UICONTROL Experiences] Telkens wanneer de gebruiker naar het tabblad [!UICONTROL Experiences] navigeert, wordt de status vernieuwd met de nieuw gedetecteerde eigenschappen en worden duplicaten voorkomen, zodat nauwkeurige tracering en betrouwbaar gedrag verderop in het scherm worden weergegeven. (TGT-54119)

+++

**Aanbevelingen**

+++Zie details
* In de vervolgkeuzelijst **[!UICONTROL Environment]worden slechts 100 resultaten weergegeven.** Met deze correctie wordt een beperking verholpen waarbij klanten met meer dan 100 omgevingen alleen de eerste 100 items in de [!UICONTROL Environment] vervolgkeuzelijst [!UICONTROL Recommendations] konden zien. De onderliggende vraag van GraphQL (~ getEnvironmentsV2 ~) werd gepagineerd met een hard-gecodeerde paginagrootte van 100, veroorzakend UI om slechts een gedeeltelijke lijst te tonen zelfs wanneer de extra pagina&#39;s beschikbaar waren. Voor klanten met meer dan 100 omgevingen leidde dit probleem tot ontbrekende opties en een onvolledige selectie. De update verhoogt de limiet, zodat alle omgevingen worden geretourneerd en weergegeven, zodat volledige zichtbaarheid wordt gegarandeerd, ongeacht het aantal omgevingen. (TGT-53903)

+++

**Rapporten**

+++Zie details

* **verholpen een kwestie waar de [!UICONTROL Reports] pijl niet duidelijk op uitbreidbare kolommen wees.** Oplossing voor een probleem waarbij de rapporttabel niet duidelijk aantoonde dat extra kolommen konden worden uitgebreid in de bijgewerkte gebruikersinterface. De verdwijnende knopinfo is toegevoegd aan de pijl [!UICONTROL Reports] bij de kolomkoppen om klanten te helpen begrijpen dat er meer kolommen beschikbaar zijn.

+++

**Weergaven**

+++Zie details

* **Onbekwaam om wijzigingen te schrappen die op meningen worden toegepast.** Met deze correctie wordt een probleem verholpen waarbij gebruikers geen wijzigingen konden verwijderen binnen een activiteit, tenzij de wijziging eerst opnieuw was toegepast op extra weergaven. Wanneer u een activiteit bewerkt (bijvoorbeeld activiteit-id 302467), hadden pogingen om een wijziging te verwijderen geen effect, zodat gebruikers ongewenste wijzigingen niet kunnen verwijderen. Als een wijziging echter opnieuw is toegepast met &quot;Toepassen op meer weergaven&quot; en toegewezen aan een `Page Load` -gebeurtenis, werkte het verwijderen plotseling zoals verwacht. (TGT-54088)

+++

**[!UICONTROL Visual Experience Composer] (VEC)**

+++Zie details
* **[!UICONTROL Experience Fragment]naam werd afgebroken in nieuwe UI VEC** (TGT-54312)
* **Kan [!UICONTROL Advanced Settings] for [!UICONTROL Revenue] niet gebruiken.** Met deze correctie wordt een probleem verholpen waarbij gebruikers een fout van 403 tegenkwamen bij het configureren van [!UICONTROL Advanced Settings] voor de metrische waarde [!UICONTROL Revenue] in [!UICONTROL Goals & Settings] . Het probleem kwam voor wanneer het toevoegen van een gebiedsdeelvoorwaarde verbonden aan het primaire doel; het backend vereiste verkeerd het redacteursrecht zelfs voor gebruikers die reeds voldoende toestemmingen hadden om activiteiten tot stand te brengen en uit te geven. Als gevolg hiervan is het opslaan van de activiteit mislukt, ondanks een geldige configuratie. De update verbetert de toestemmingscontrole zodat de gebruikers met aangewezen toegang met succes de metrische gebiedsdelen van de Opbrengst kunnen toevoegen zonder een verboden-middelfout te veroorzaken. (TGT-54092)
* **Vaste een kwestie waar de Add knoop niet op geselecteerde beelden van toepassing was.** Oplossing voor een probleem dat ervoor zorgde dat klanten bepaalde afbeeldingen niet mochten toevoegen wanneer ze een afbeelding tijdens het maken van de activiteit selecteren of bijwerken. Wanneer klanten naar specifieke elementen hebben gezocht, bijvoorbeeld, zijn afbeeldingen die zijn geretourneerd bij het zoeken naar &#39;ipp&#39; en op de knop [!UICONTROL Add] klikken, niet van toepassing op de geselecteerde afbeelding en is er geen wijziging gemaakt. Het selecteren van andere afbeeldingen, zoals `Homepage-banner-1-moz.jpg` , bleef werken zoals u had verwacht. Deze update zorgt ervoor dat alle geldige afbeeldingen consistent kunnen worden toegepast in de bijgewerkte gebruikersinterface. (TGT-53610)
* **Vaste een kwestie waar het schrappen van een voorwaarde URL de doel metrische configuratie terugstelt.** Oplossing voor een probleem waarbij door het verwijderen van één URL-voorwaarde in de [!UICONTROL Goal] -norm de volledige configuratie opnieuw werd ingesteld in de bijgewerkte gebruikersinterface. Wanneer klanten een opgeslagen URL-voorwaarde probeerden te verwijderen onder [!UICONTROL Conversion] > [!UICONTROL Viewed a Page] , werd het doeltype onverwachts overgeschakeld naar [!UICONTROL Viewed an Mbox] en werden alle eerder geconfigureerde instellingen verwijderd. Deze update zorgt ervoor dat alleen de geselecteerde URL-voorwaarde wordt verwijderd en dat alle resterende doelinstellingen intact blijven. (TGT-53271)
* **Vaste een kwestie waar het onderzoek niet door subfolders keek.** Oplossing voor een probleem waarbij het zoeken naar voorstellen geen resultaten van submappen in de bijgewerkte gebruikersinterface heeft opgeleverd. Klanten konden een aanbieding slechts vinden als zij manueel aan de omslag navigeerden waar het werd opgeslagen, makend onderzoeksgedrag inconsistent met API mogelijkheden. Zoeken ondersteunt nu recursief zoeken in mappen, zodat klanten aanbiedingen kunnen vinden zonder elke map afzonderlijk te hoeven openen. (TGT-51954)

+++

## Aanvullende opmerkingen bij de release en versiedetails

| Bron | Details |
|--- |--- |
| [&#x200B; de nota&#39;s van de Versie: De Ervaring van het Platform van Adobe Target Web SDK &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=en) | Details over veranderingen in elke versie van het Web SDK van het Platform. |
| [&#x200B; at.js versiedetails &#x200B;](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html){target=_blank} | Informatie over de wijzigingen in elke versie van de JavaScript-bibliotheek [!DNL Adobe Target] at.js. |

## Documentatiewijzigingen, Opmerkingen bij de vorige release en Opmerkingen bij de release van Experience Cloud

Naast de notities voor elke release bevatten de volgende bronnen aanvullende informatie:

| Bron | Details |
|--- |--- |
| [&#x200B; Veranderingen van de Documentatie &#x200B;](/help/main/r-release-notes/doc-change.md) | Gedetailleerde informatie weergeven over updates van deze handleiding die niet zijn opgenomen in deze releaseopmerkingen. |
| [&#x200B; de nota&#39;s van de Versie voor vorige versies &#x200B;](/help/main/r-release-notes/release-notes-for-previous-releases.md). | Informatie weergeven over nieuwe functies en verbeteringen in vorige versies van Target Standard en Target Premium. |
| [&#x200B; de Nota&#39;s van de Versie van Adobe Experience Cloud &#x200B;](https://experienceleague.adobe.com/docs/release-notes/experience-cloud/current.html){target=_blank} | Bekijk de nieuwste releaseopmerkingen voor de Adobe Experience Cloud-oplossingen. |

## Prerelease-informatie {#section_5D588F0415A2435B851A4D0113ACA3A0}

De volgende middelen laten u zien wat in de volgende versie van het Doel komt.

| Bron | Details |
|--- |--- |
| [&#x200B; de Prioritaire Update van het Product van Adobe &#x200B;](https://www.adobe.com/subscription/priority-product-update.html){target=_blank} | Ontvang voorafgaande meldingen over aanstaande productverbeteringen voor [!DNL Target] en andere [!DNL Adobe Experience Cloud] -oplossingen. |
| [&#x200B; de Nota&#39;s van de Versie van het Doel - preRelease &#x200B;](/help/main/r-release-notes/target-release-notes.md){target=_blank} | Informatie over de versies van het Doel van de huidige maand, met inbegrip van pre-releaseinformatie. |
