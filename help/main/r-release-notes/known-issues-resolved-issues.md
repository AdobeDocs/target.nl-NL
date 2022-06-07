---
keywords: bekende problemen;opgeloste problemen;releaseopmerkingen;fouten;problemen;oplossingen
description: Meer informatie over bekende problemen in Adobe Target, waaronder informatie over tijdelijke oplossingen. Wanneer problemen zijn opgelost, worden ze verplaatst naar de sectie Opgelost.
title: Waar kan ik informatie vinden over bekende problemen en opgeloste problemen?
feature: Release Notes
exl-id: 6eb854f7-ed46-4673-afeb-0b44970598cd
source-git-commit: a72dab23ce3fc6ac415ec6c75358fb119d2802ce
workflow-type: tm+mt
source-wordcount: '4440'
ht-degree: 0%

---

# Bekende problemen en opgeloste problemen

Informatie over bekende problemen voor [!DNL Adobe Target]. Bevat ook informatie over problemen die zijn opgelost.

>[!NOTE]
>
>De uitgiftenummers tussen haakjes zijn bedoeld voor intern gebruik van Adobe.

## Bekende problemen {#section_AEDC98B67CF24C9F8E0CF0D2EB9ACAEF}

De volgende secties geven een overzicht van de bekende problemen voor [!DNL Target]:

### Locaties verwijderen die een ad-hocaanbieding hebben in activiteiten die zijn gemaakt in de Form-Based Experience Composer {#ad-hoc}

Verwijder geen locaties in een activiteit die is gemaakt in de Form-Based Experience Composer als deze locaties gebruikmaken van ad-hocaanbiedingen (aanbiedingen die binnen de activiteit zijn gemaakt). Als u locaties verwijdert, kan de activiteit beschadigd raken. De [!DNL Target] team werkt aan een oplossing hiervoor. Als tijdelijke oplossing kunt u wereldwijde aanbiedingen maken van de [!UICONTROL Offer library] en gebruik ze op locaties, of u kunt nieuwe ervaringen maken, indien nodig. (kB-2014)

### Verkeersverdeling van activiteiten die automatisch worden toegewezen met behulp van A4T {#aa-a4t}

In sommige gevallen, de verkeersverdeling van [!UICONTROL Auto-Allocate] activiteiten die [!UICONTROL Analytics for Target] (A4T) kan afwijken van wat er zou moeten gebeuren op basis van de gerapporteerde omrekeningskoers van elke ervaring. Dit komt vaker voor bij activiteiten met een hoog percentage retourbezoekers. Betrokken klanten worden op de hoogte gesteld van de betrokken activiteiten.

Gebruik totdat dit probleem is opgelost [!UICONTROL Auto-Allocate] met standaard [!DNL Target] rapportage of gebruik van standaard A/B-tests met [!DNL Analytics] rapportage als alternatief voor [!UICONTROL Auto-Allocate] with [!DNL Analytics] rapportage. (TOP-131)

### Analyses voor Adobe Target (A4T)-meetgegevens voor automatisch toegewezen en automatisch doelactiviteiten

De [!DNL Target] Met de gebruikersinterface kunnen gebruikers niet-ondersteunde gegevens voor betrokkenheid en omzet selecteren als primaire doelmaatstaf voor optimalisatie in [!UICONTROL Auto-Allocate] en [!UICONTROL Auto-Target] activiteiten. Conversiemetriek worden ondersteund; service- en inkomstenwaarden zijn *niet* ondersteund. Als u maatstaven voor betrokkenheid of inkomstendoel selecteert, wordt geen optimalisatiemodel samengesteld.

Voor een lijst van gesteunde en niet gestaafde doelmetriek, zie [A4T-ondersteuning voor activiteiten voor automatisch toewijzen en automatisch richten](/help/main/c-integrating-target-with-mac/a4t/a4t-at-aa.md). (TNT-38409)

### De Enhanced Experience Composer (EEC) ondersteunt geen verzoeken om PUT.

Een probleem met de EEG verhindert momenteel dat het aanvragen van PUTTEN ondersteunt en leidt tot een time-outfout van 504. (TGT-41493)

### [!DNL Adobe Experience Platform] segmentnamen worden niet weergegeven in het dialoogvenster [!UICONTROL Important Attributes] verslag.

[!DNL Adobe Experience Platform] segmentnamen worden niet weergegeven in het dialoogvenster [!UICONTROL Important Attributes] verslag voor [!UICONTROL Automated Personalization] (AP) en [!UICONTROL Auto-Target] (AT) activiteiten. (TOP-3813)

### Archiveren [!UICONTROL Auto-Target] activiteiten kunnen synchronisatieproblemen veroorzaken

Poging om inactief te archiveren [!UICONTROL Auto-Target] activiteiten kunnen leiden tot synchronisatieproblemen. Niet archiveren totdat dit probleem is opgelost [!UICONTROL Auto-Target] activiteiten. Laat ze in de [!UICONTROL Inactive] status. (TGT-40885)

### Aanbiedingen omleiden {#redirect}

* De omleiding van activiteiten in implementaties at.js zou de voorproef URL kunnen veroorzaken om in een lijn in te gaan (de aanbieding wordt herhaaldelijk geleverd). U kunt [QA-modus](/help/main/c-activities/c-activity-qa/activity-qa.md) om Voorvertoning en QA uit te voeren. Deze kwestie heeft geen invloed op de daadwerkelijke levering van het aanbod. (TGT-23019)

### Het laden van een pagina in Visual Experience Composer (VEC) annuleren {#cancel}

* Het volgende bekende probleem bestaat momenteel wanneer u het laden van een [!UICONTROL A/B Test] of [!UICONTROL Experience Targeting] (XT) activiteit binnen VEC die een omleidingsURL bevat.

   Als u in stap een van de VEC-workflow met instructies het laden van pagina&#39;s annuleert, wordt de [!UICONTROL Modifications] in de VEC-weergaven en de omleiding naar de URL-sjabloon wordt toegepast op de ervaring (bijvoorbeeld &#39;Experience B&#39;). Wanneer u naar stap twee of drie gaat en vervolgens terugkeert naar stap één, doet zich de volgende situatie voor.

   Bij &quot;Experience B&quot; wordt standaard de sjabloon voor het laden van de geannuleerde website weergegeven en wordt de [!UICONTROL Modifications] is toegankelijk, wat niet het geval zou moeten zijn omdat deze ervaring een omleiding naar toegepaste malplaatje URL heeft. De omleiding naar URL-sjabloon moet worden weergegeven.

   Om de juiste stand van de ervaring in de VEC aan te tonen:

   Als u overschakelt naar een andere ervaring en vervolgens terugschakelt naar &quot;Experience B,&quot; [!DNL Target] geeft de omleiding naar de URL-sjabloon weer die op deze ervaring is toegepast en de [!UICONTROL Modifications] is niet toegankelijk. (TGT-32138)

* Als u het laden annuleert voor websites van de toepassing Eén pagina (SPA), kunt u handelingen niet bewerken in het kader van de [!UICONTROL Modifications] deelvenster.

### Recommendations

De volgende problemen zijn bekend met: [!UICONTROL Recommendations] activiteiten:

* Wanneer [!DNL Target] retourneert een JSON-aanbieding met getOffer(), het retourneert het type JSON. Als u echter een JSON Recommendations-ontwerp retourneert, retourneert dit met een type HTML.
* Entiteiten zijn na 60 dagen na ontvangst van geen updates via feed of API correct verlopen. de verlopen entiteiten worden echter niet na het verlopen van de zoekindex van de catalogus verwijderd. (IRI-857)
* De &quot;Gebruiksinformatie&quot;-overlays voor Criteria en Ontwerpen weerspiegelen hun gebruik in A/B en de Ervaring gerichte activiteiten (TGT-34331) niet
* Recommendations-aanbiedingen in A/B en Experience Targeting-activiteiten tonen geen visuele voorvertoning van de Recommendations-lade (TGT-33426)
* Verzamelingen, uitsluitingen, criteria en ontwerpen die via de API zijn gemaakt, zijn niet zichtbaar in de doelgebruikersinterface en kunnen alleen via de API worden bewerkt. Op dezelfde manier, als u om het even welk van deze punten in het Doel UI creeert en later hen via API uitgeeft, worden die veranderingen niet weerspiegeld in het Doel UI. Items die via de API worden bewerkt, moeten ook in de toekomst via de API worden bewerkt om te voorkomen dat wijzigingen verloren gaan. (TGT-35777)
* Recommendations-activiteiten die via API zijn gemaakt, kunnen in de gebruikersinterface worden weergegeven, maar kunnen alleen via API worden bewerkt.
* De voedingsstatus van de aangepaste criteria die wordt weergegeven in de weergave Criteria (kaart), wordt elke tien minuten vernieuwd en kan in zeldzame gevallen meer dan tien minuten verouderd zijn. De status die wordt weergegeven in de bewerkingsweergave Aangepaste criteria wordt opgehaald in real-time en is altijd up-to-date. (TGT-35896, TGT-36173)
* De criteria en de ontwerpkaarten geven niet het juiste aantal activiteiten aan waarin zij worden gebruikt. Indien de criteria of het ontwerp in een A/B-activiteit worden gebruikt, kan de kaart ten onrechte aantonen dat het ontwerp of de criteria niet worden gebruikt, zelfs wanneer het ontwerp of de criteria in de activiteit worden gebruikt. (TGT-36621, TGT-37217)

### MVT-activiteiten (Multivariate Test)

In een MVT-activiteit is de winnaar die in de tabel en grafiek wordt weergegeven, niet consistent bij het controleren van de meetwaarden. Deze situatie komt voor als een gebruiker van Samenvatting aan de Mening van de Grafiek schakelt, dan terug naar Samenvattende Mening, metrisch verandert, en dan schakelaars aan de Mening van de Grafiek. Wanneer dit probleem optreedt, wordt in de overzichtsweergave altijd de juiste winnaar weergegeven. Als de gebruiker nooit schakelt tussen de overzichtsweergave, wordt in de grafiekweergave de juiste winnaar weergegeven.

### at.js {#atjs}

De volgende problemen zijn bekend met at.js:

* Wanneer een pagina in Visuele Composer van de Ervaring (VEC) wordt geladen, moet het Doel bepalen als globale mbox het plaatsen wordt toegelaten of onbruikbaar gemaakt en of entiteitID of categoryID aanwezig is op de plaats waar de gebruiker probeert om de aanbeveling in VEC toe te passen. Op basis van deze informatie wordt de lijst met criteria gefilterd. De standaardlijst heeft gefilterde algoritmen, maar [Compatibel selectievakje](/help/main/c-recommendations/t-create-recs-activity/algo-select-recs.md) Hiermee kunt u de volledige lijst met algoritmen weergeven.

   Als u at.js gebruikt, is het selectievakje Compatibiliteit verborgen, zodat incompatibele algoritmen niet zichtbaar zijn.

   Deze kwestie geldt alleen voor Recommendations-activiteiten die gebruikmaken van de VEC.

   **Workaround**: De opdracht [!UICONTROL Filter Incompatible Criteria] optie in [!UICONTROL Recommendations > Settings]. Nadat u deze instelling hebt uitgeschakeld, worden alle (compatibele en niet-compatibele) criteria weergegeven in de kiezer voor criteria. (TGT-25949)

* Mboxen die niet worden geactiveerd in Microsoft Explorer 11-browsers na de upgrade naar at.js versie 1.0 vanwege de interactie tussen at.js en Visitor API 2.2.0. Dit probleem is van toepassing op versie 0.js 0.9.6 en hoger. (TNT-27600)
* at.js werkt mogelijk niet met Cordova/Hybrid-apps omdat cookies van de eerste partij momenteel niet in deze toepassingen worden ondersteund. (TNT-26166)

   **Workaround**: Configureer at.js met de optie &quot;x-only&quot; ingeschakeld en geef door `mboxThirdPartyId` in vraag om gebruikers te beheren.

### Succeswaarden

De metriek van het succes met de geavanceerde optie &quot;hoe de telling&quot;zal worden verhoogd geplaatst aan &quot;elke indruk&quot;of &quot;elke indruk (exclusief vernieuwingen)&quot;kan niet als succes worden gebruikt metrisch dat een andere metrisch afhangt.

Wanneer een succes metrisch aan toename op elke indruk wordt geplaatst, telt Target opnieuw de bezoeker telkens als de bezoeker dit succes metrisch bezoekt. Het doel stelt dan het succes metrische &quot;lidmaatschap&quot;aan 0 terug zodat kan het op de volgende indruk opnieuw tellen. Aldus, als een andere metrisch metrisch vereist om eerst te zijn gezien, erkent het Doel nooit dat de gebruiker eerste metrisch heeft gezien.

### Analyses voor [!DNL Target] (A4T)

Wanneer u de functie Doelactiviteit-impressies en -conversies in Analysis Workspace gebruikt, past u het model Gelijke aanraking toe op de Attribution IQ om een nauwkeurige telling te garanderen. Als u een [niet-standaard toewijzingsmodel](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/build-workspace-project/column-row-settings/column-settings.html), klikt u met de rechtermuisknop op de metrisch naar **Kolominstellingen wijzigen > Niet-standaard toewijzingsmodel gebruiken inschakelen > Zelfde aanraakmodel selecteren**. Als dit model niet wordt toegepast, zijn de meetwaarden te hoog.

Alle huidige pakketten Analytics kunnen dit model met Attribution IQ toevoegen. Als u geen toegang tot Attribution IQ hebt, baseert u zich op A4T-gegevens in Rapporten &amp; Analytics.

### Doel-API&#39;s

Klanten kunnen geen CRUD-bewerkingen uitvoeren op activiteiten voor automatisch toewijzen via de v3-versie van de API voor A/B-activiteiten op Adobe I/O.

### Rapportage - de Inconsistente gegevens in het downloadbare .csv- rapport versus het getoonde rapport in [!DNL Target] UI. {#csv}

Rapporten die worden gegenereerd om te worden gedownload als CSV-bestanden, zijn inconsistent als de activiteit meer dan één metrische waarde gebruikt. Het downloadbare rapport wordt geproduceerd gebaseerd op de rapportmontages slechts en beschouwt de zelfde waarde voor een andere gebruikte metriek.

De bron van de waarheid is altijd het verslag dat in het [!DNL Target] UI.

## Opgeloste problemen {#section_FD2FC86E7C734D60B1EDC9DEF60E1014}

Aangezien bekende problemen hierboven zijn opgelost, worden ze verplaatst naar de volgende secties. Indien nodig worden aanvullende opmerkingen toegevoegd.

### at.js

* Als u een ervaring zonder wijzigingen creeert gebruikend at.js 2.1.1 of vroeger (bijvoorbeeld, een standaardervaring), zou de ervaring niet in rapporten, Analytics voor Doel (A4T), Adobe Analytics, of Google Analytics kunnen worden geteld. Bovendien werkt de insteekmodule ttMeta mogelijk niet correct.

   Als oplossing gebruikt u een witruimte in de ervaringsinhoud.

   Een oplossing voor dit probleem is opgenomen in at.js 2.2.0. Upgrade naar [nieuwste versie of at.js](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md) of gebruik de hierboven vermelde tijdelijke oplossing alleen voor versies van at.js die ouder zijn dan 2.2.0.  (TNT-33366)

* Als u versies at.js gebruikt vóór 2.2.0, klikt u op tracking en worden geen conversies gerapporteerd in [!UICONTROL Analytics for Target] (A4T) als [!DNL Adobe Analytics] code is niet aanwezig op pagina-elementen (zoals knoppen).

   In 0.js 2.2.0 is een oplossing voor dit probleem geïntroduceerd. [Voer een upgrade uit naar de nieuwste versie om.js](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md) als u dit probleem ondervindt.

### GEO-gericht

Op 10 mei 2020 heeft Adobe de bestanden van de GEO-provider bijgewerkt, waardoor enkele inconsistenties zijn ontstaan. Sommige waarden met komma&#39;s zijn bijvoorbeeld toegevoegd. hoewel de waarden bij het bestaande publiek geen komma hebben . Deze wijziging had geen invloed op alle Adobe-leveringsservers. Dientengevolge hebben de kijkers die dergelijke waarden gebruiken, tussen 10 mei en 22 juli 2020 mogelijk niet alle juiste bezoekers gekwalificeerd.

### Een [!UICONTROL Recommendations] activiteit

Bij het kopiëren van een [!UICONTROL Recommendations] activiteiten met een actieve promotie ; elke wijziging in de dubbele activiteit heeft momenteel ook invloed op de oorspronkelijke activiteit , en omgekeerd . (TGT-39155)

Dit probleem is opgelost in het dialoogvenster [!DNL Target Standard/Premium] Release 21.2.1.

### QA-modus voor Recommendations-activiteiten

Een bekend probleem voorkomt een voorvertoning als de criteria die in de activiteit worden gebruikt, op een item of categorie zijn gebaseerd. (TNT-37455)

Dit probleem is in januari 2022 opgelost. (TNT-37455)

### Paginalevering {#page-delivery}

Als u een sjabloonregel toevoegt, zoals de URL, bevat deze regel (/checkout, /cart) in [paginalevering](/help/main/c-activities/t-experience-target/t-xt-create/xt-activity-url.md), extra spaties staan aan uw regels vooraf. Deze extra ruimten zijn cosmetisch en hebben geen invloed op het creëren van publieksdefinities en het aanbieden van levering. (TGT-35920)

### Aanbiedingen voor afbeeldingen met het label &quot;Verwerking&quot;

Afbeeldingsaanbiedingen op de pagina Aanbiedingen behouden soms het label &quot;Verwerking&quot; enkele uren nadat de afbeeldingen zijn geüpload. In de meeste gevallen is dit alleen een probleem met het etiket: de beeldaanbiedingen kunnen nog steeds worden gebruikt in activiteiten en worden geleverd . (MCUI-10264, TGT-37458)

Dit probleem is opgelost in de Target Standard/Premium-versie 20.10.1.

### Analyses voor Adobe Target (A4T)-rapportage

De volgende kwesties in verband met A4T zijn opgelost:

* Een kwestie die A4T activiteiten beïnvloedde gebruikend een [!DNL Analytics] doel metrisch die A4T rapporten veroorzaakte om een onverwachte verkeerssplitsing of kunstmatig opgeblazen omzettingen te tonen.

   Deze kwestie beïnvloedde de A4T-rapportage onder de volgende voorwaarden:

   * De activiteit werd gecreëerd of gered tussen 15 september en 5 november 2020 (4.00 uur PST), en
   * De activiteit had een [!DNL Analytics] metrisch geselecteerd als doel metrisch.

   [!DNL Target] correct gesplitst verkeer tijdens deze tijd. Een splitsing van 50/50 in de activiteiteninstellingen kan echter bijvoorbeeld worden weergegeven als een splitsing van 90/10 in A4T-rapporten.

   Voor betrokken activiteiten is de correcte verkeerssplitsing zichtbaar voor nieuwe bezoekers aan de activiteit na 5 november (4.00 uur PST). De nieuwe activiteiten die na deze tijd worden gecreeerd of worden bewaard zullen de verkeerspleet correct melden.

* Een kwestie die A4T activiteiten beïnvloedde gebruikend [!DNL Target] doel metrisch die A4T rapporten veroorzaakte om laag of geen omzettingen te melden.

   >[!NOTE]
   >
   >Dit probleem betrof alleen de A4T-rapportage. Het had geen invloed op de levering van de activiteit.

   Deze kwestie beïnvloedde de A4T-rapportage onder de volgende voorwaarden:

   * De A4T-activiteit was actief tussen 22 september en 11 november 2020 (2:30 uur PST), en
   * De activiteit had een [!DNL Target] metrisch geselecteerd als doel metrisch, en
   * Wanneer een bezoeker de doelgebeurtenis voor de activiteit heeft bereikt (bijvoorbeeld [!UICONTROL Clicked an Element]) was er ook een activiteit zonder A4T met lagere prioriteit die overeenkwam met de conversiegebeurtenis. Dit zou kunnen gebeuren als de activiteit niet-A4T of met zelfde metrisch zoals de activiteit A4T werd gevormd of als het met metrisch &quot;om het even welke mbox&quot;werd gevormd.

   Deze kwestie beïnvloedde de verslaglegging voor A4T activiteiten die tussen 22 september en 11 november 2020 (14:30 uur PST) leefden. De rapportering voor beïnvloede activiteiten A4T zal correct omzettingen buiten dit datumbereik tonen. De rapportage voor niet-A4T-activiteiten had geen gevolgen.

Als u nog vragen hebt, kunt u contact opnemen met uw Customer Success Manager (CSM) of [Adobe Klantenservice](/help/main/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C). (PB 2011/11/EG)

### Automatische doelrapportage {#at-metrics}

Er is een probleem opgelost dat gevolgen heeft [!DNL Adobe Target Premium] gebruikers&quot; [!UICONTROL Auto-Target] rapportage vanaf 15 september, 2:30 uur (PDT) tot 6 oktober, 9:25 (PDT). Wanneer het bekijken van rapporten voor de beïnvloede omzettingsmetriek (gevormd die of &quot;[!UICONTROL Viewed a page]&quot; of &quot;[!UICONTROL Clicked on mbox]&quot; optie), worden de omrekeningskoersen onjuist gerapporteerd. Er is momenteel geen bekend leveringsprobleem.

Je melding opnieuw synchroniseren en corrigeren:

1. De invloed kopiëren en opslaan [!UICONTROL Auto-Target] activiteiten.
1. Activeer de nieuw opgeslagen activiteiten (als de betrokken activiteiten actief waren).
1. Verwijder de originele (beïnvloede) activiteiten.

(TGT-38522, CSO 201006007)

### Rapportage {#conversions-audiences}

Conversies verhogen momenteel verschillend gebaseerd op welk publiek wordt gebruikt.

Als voor dezelfde bezoeker bijvoorbeeld het aantal conversies is ingesteld op &quot;Eenmaal per binnenkomst:&quot;

* Publiek: &quot;Alle Gekwalificeerde Bezoekers&quot;voor op bezoek-niveau omzettingen verhogen slechts één keer. Dit is het verwachte gedrag.
* Publiek: &quot;Nieuwe Bezoekers&quot;voor op bezoek-niveau omzettingen verhogen verkeerd elke keer, in plaats van slechts één keer te verhogen. Dit is niet het verwachte gedrag.

Als het aantal conversies is ingesteld op &quot;Op elke indruk:&quot;

* Publiek: &quot;Alle gekwalificeerde Bezoekers&quot; voor conversies op bezoekersniveau worden slechts eenmaal incorrect verhoogd in plaats van elke keer te verhogen. Dit is niet het verwachte gedrag.
* Publiek: &quot;Nieuwe Bezoekers&quot; voor conversies op bezoekersniveau nemen telkens toe. Dit is het verwachte gedrag.

Dit probleem houdt verband met [!DNL Target] alleen rapporteren. Dit is geen probleem bij het gebruik [!UICONTROL Analytics for Target] (A4T) rapportage.

Dit probleem is opgelost.

### Pagina&#39;s die niet worden geladen in Visual Experience Composer (VEC) of Enhanced Experience Composer (EEC) bij gebruik van Google Chrome versie 80+

Dit bekende probleem betreft het besluit van Google om het standaardgedrag van cookies te wijzigen zonder het SameSite-kenmerk te beginnen met Chrome versie 80. Voordat de wijzigingsinterface alle cookies zonder het SameSite-kenmerk standaard instelde op &quot;SameSite=None&quot; en nu wordt de standaardwaarde ingesteld op &quot;SameSite=Lax&quot;. Hierdoor wordt de manier gewijzigd waarop cookies worden verzonden op GET- en POST-aanvragen. Zie [SameSite-updates](https://www.chromium.org/updates/same-site).

Zie &quot;Hoe beïnvloedt het onlangs aangekondigde Google Chrome SameSite cookie handhavingsbeleid de VEC en EEC?&quot; voor meer informatie en een oplossing. in [Problemen oplossen met betrekking tot Visual Experience Composer en Enhanced Experience Composer](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/issues-related-to-the-visual-experience-composer-vec-and-enhanced-experience-composer-eec.md#samesite).

### Grafiekrapport voor een activiteit Auto-Doel ontbreekt teruggeven wanneer het gebruiken van een douaneervaring als controle

Het grafiekrapport voor een activiteit auto-Doel ontbreekt om voor &quot;differentiële&quot;wijzen (Gemiddelde Lift en Dagelijkse Lift) terug te geven als er geen gegevens (0 bezoeken) in om het even welke ervaring zijn. Deze situatie kan zich voordoen tijdens de vroege fase van een activiteit als de controleervaring aan douane wordt geplaatst. Voor de andere wijzen (het Lopen Gemiddelde Controle en Gericht, Dagelijkse Controle en Gericht, en Bezoek) werkt het fijn. Zodra er gegevens zijn (bezoeken die niet gelijk zijn aan nul), wordt het rapport weergegeven zoals verwacht.

Dit probleem is opgelost in de Doelversie 19.7.1.

### Implementatie: Automatisch een globale box maken

Op het tabblad Implementatie ([!UICONTROL Administration > Implementation]de [!UICONTROL Global Mbox Auto Create] het gebied zal &quot;vals&quot;door gebrek voor een onlangs provisioned huurder zijn.

Wanneer at.js voor het eerst na levering wordt gedownload, [!UICONTROL Global Mbox Auto Create] field is ingesteld op &quot;true&quot; in het gedownloade bestand at.js en in het dialoogvenster [!DNL Target] back-end, maar deze blijft op de [!UICONTROL Implementation] pagina in de gebruikersinterface tot de pagina is vernieuwd (nadat de pagina is vernieuwd, is de status &quot;true&quot;.)

at.js wordt gedownload met `global_mbox_autocreate = false` voor een nieuwe huurder. Als mbox.js (nu afgekeurd) als eerste is gedownload, wordt global\_mbox\_autocreate ingesteld op &quot;true&quot; en wordt at.js ook gedownload met `global_mbox_autocreate = true`. (TGT-15929)

### Ondersteuning voor Enterprise-machtigingen in [!DNL Target] API&#39;s {#api}

Codeaanbiedingen die zijn gemaakt vanuit de doelinterface in de bibliotheek met aanbiedingen, worden mogelijk weergegeven in de standaardwerkruimte als de lijst met aanbiedingen wordt opgehaald met GET-API&#39;s. Deze kwestie zal in de eerste week van maart 2019 worden geregeld. Nadat deze oplossing is ingesteld, worden de codeaanbiedingen in de juiste werkruimte weergegeven wanneer ze van API&#39;s worden gehaald. Dit probleem doet *niet* beïnvloedt aanbiedingen die van APIs worden gecreeerd. Codeaanbiedingen die zijn gemaakt op basis van API&#39;s worden bijvoorbeeld weergegeven in de werkruimte waarin ze zijn gemaakt, ongeacht of ze zijn opgehaald met GET-API&#39;s of vanuit de doelinterface.

### Rapportage en extreme orders

Van 25 november 2019 tot 26 april 2020, ondervond één Target-server een probleem dat ertoe leidde dat extreme orderwaarden moesten worden geteld in rapporteringsmetriek op basis van inkomsten (AOV, RPV). Van 19 december 2019 tot 23 april 2020 kreeg een andere server hetzelfde probleem. Deze kwestie beïnvloedde niet alle servers van het Doel of alle klanten van het Doel.

U bent *niet* beïnvloed als:

* Uw doelimplementatie gebruikt verschillende servers.
* In uw rapporten zijn extreme bestellingen niet uitgesloten.
* U hebt een omzettingsmaatstaf gebruikt om uw activiteiten te meten.
* Uw doelactiviteiten gebruiken Analytics voor Doel (A4T).
* U bevindt zich in de regio Azië-Pacific (APAC).

Als u wilt bepalen of dit probleem gevolgen heeft voor uw doelrapportage, kunt u [Clientservice](/help/main/cmp-resources-and-contact-information.md#concept_34A1CA16F2244D42930BB77846A5ABBB).

### Recommendations

* Recommendations feed-index kan &#39;Waiting for index&#39; weergeven als de items in de feed gelijk zijn aan de items in de vorige run. De inname van het product voor levering heeft geen invloed op het product. (RECS-6663)

   Dit probleem is opgelost in de doelversie 19.4.2.

* Het verwerken van Recommendations-feeds duurt langer dan u had verwacht. (COR-2836)

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

v1-versie van de API&#39;s van de aanbieding op Adobe I/O behandelt alle aanbiedingen die via Target zijn gemaakt, in de standaardwerkruimte. (TTTEAM-41957)

Dit probleem is opgelost.

### at.js {#at-js-2}

Mboxen die niet worden geactiveerd in Microsoft Explorer 11-browsers na de upgrade naar at.js versie 1.0 vanwege de interactie tussen at.js en Visitor API 2.2.0. Dit probleem is van toepassing op versie 0.js 0.9.6 en hoger. (TNT-27600)

Opgelost met de release van API 2.3.0 of hoger.

### Geo targeting

Het zoeken naar een tekenreeks die speciale tekens bevat (zoals een spatie of komma) werkt momenteel niet wanneer u doelgroepen maakt. Dit probleem doet zich bijvoorbeeld voor bij het creëren van publiek op basis van steden, staten, landen, enz. Wanneer u bijvoorbeeld zoekt naar &quot;new york&quot;, retourneert de zoekopdracht geen geldige resultaten.

Vast in november 2018.

### at.js {#at-js-3}

Wanneer u at.js versie 1.6.0 gebruikt, vindt een omleiding van Analytics voor Target (A4T) plaats, maar zonder activiteitkwalificatie.

Correctie met de release van at.js 1.6.2.

### Activiteiten, werkruimten en activiteit-API verwijderen

De activiteiten in de standaardwerkruimte die via API worden verwijderd, worden nog steeds weergegeven in de doelinterface. Als tussenoplossing, schrap alle activiteiten in de standaardwerkruimte gebruikend het Doel UI. (TGT-31315)

Vast 25 oktober 2018

### Automated Personalization (AP)-rapportage op aanbodniveau

Wanneer u op de beoogde ervaring in een rapport van een Automated Personalization-activiteit (AP) klikt om rapportage op aanbiedingsniveau weer te geven, ziet u momenteel lege resultaten, een foutbericht of een draaiend pictogram. (TNT-30695)

Vast op 27 september 2018.

### Code-editor

Als u VEC op stap 1 van de driestapige geleide werkstroom opnieuw laadt terwijl het werken met de Redacteur van de Code in Firefox en Internet Explorer, geeft het lusje van Wijzigingen niet behoorlijk terug; de functionaliteit van VEC wordt echter niet beïnvloed. (TGT-28730)

Dit probleem is opgelost in de release 18.9.1.

### Recommendations-activiteit die een kenmerkpromotieregel gebruikt

Wanneer u een Recommendations-activiteit bewerkt of kopieert die gebruikmaakt van een kenmerkpromotieregel, wordt de fout &quot;Heeft ontbrekend veld&quot; weergegeven wanneer u op Opslaan klikt.

Dit probleem is opgelost in de release 17.8.1.

### Backup Recommendations

Back-upaanbevelingen geven ten onrechte &quot;Ingeschakeld&quot; weer op recent bekeken itemkaarten in de interface van het doel. (TGT-29308)

Dit probleem is opgelost in de release 18.4.1, zodat &quot;Uitgeschakeld&quot; wordt weergegeven.

### Auto-Target activiteiten en rapportagepubliek

Wanneer de naam van een rapportpubliek in een auto-Doel activiteit wordt gebruikt wordt veranderd, zouden de verdere updates van Doel voor die activiteit met een foutenmelding kunnen ontbreken.

Dit probleem is opgelost met de Target 18.5.1-release (22 mei 2018).

### at.js {#at-js-4}

Het algoritme voor het extraheren van het domein op hoofdniveau dat moet worden gebruikt bij het opslaan van cookies is gewijzigd in versie 0.js 0.9.6. Vanwege deze wijziging kunnen cookies niet worden opgeslagen naar adressen die IP gebruiken. Meestal worden IP-adressen gebruikt voor testdoeleinden, maar als tijdelijke oplossingen kunt u DNS-vermeldingen gebruiken, het hostbestand op een lokaal vak aanpassen of de functie targetGlobalSettings() at.js gebruiken om een codefragment in te voegen ter ondersteuning van IP-adressen.

Dit probleem is opgelost in at.js versie 1.2.

### Machtigingen voor Enterprise-gebruikers voor [!DNL Target] Premium

Als onderdeel van de migratie naar Enterprise-machtigingen is al het gebruikersbeheer voor Target Premium verplaatst van de gebruikersinterface van Adobe Target naar Adobe Admin Console.

Als gevolg van de migratie zijn er twee mogelijke problemen die u dient te kennen:

* Gebruikers die geen beheerder zijn, hebben een e-mail ontvangen waarin wordt aangegeven dat ze nu toegang hebben tot Adobe Target. Dit wijst erop dat de migratie voor uw organisatie werd voltooid. De e-mail zelf kan buiten beschouwing worden gelaten.
* Na de migratie zijn er meldingen geweest dat eerder uitgeschakelde gebruikers opnieuw in de Adobe Admin Console verschenen. Dit kan een probleem voor uw organisatie zijn als uitgeschakelde gebruikers in de Adobe Admin Console nog steeds op uw gebruikerslijst in Target staan vóór de migratie. Wij adviseren dat de beheerders de lijst van gebruikers in Admin Console herzien om toegang te bevestigen.

Dit probleem is opgelost op 30 augustus 2017

### Activiteiten maken

Een probleem met de release 17.6.2 kan van invloed zijn geweest op activiteiten die zijn gemaakt en/of bijgewerkt tussen 22 juni 2017 en 29 juni 2017. De volgende activiteiten werden beïnvloed:

* Ervaringen die opnieuw zijn gerangschikt in Experience Targeting (XT), zouden terugkeren naar de oorspronkelijke volgorde
* Om het even welke segmentregels lokaal aan de activiteit (niet bewaard binnen een publiek) zouden verloren zijn gegaan: gecombineerde doelgroepen, verfijnde locaties en eventuele regels voor succesmetriek.

Dit had geen gevolgen voor andere activiteiten.

**Belangrijk**: Dit probleem wordt niet automatisch opgelost. U moet alle betrokken activiteiten opnieuw opslaan om het probleem op te lossen.

Dit probleem is op 29 juni 2017 opgelost

### Formuliergebaseerde Experience Composer

De volgende bekende problemen zijn gemeld bij gebruik van de Form-Based Experience Composer:

* Als u de Form-Based Composer van de Ervaring met een doos buiten auto-gecreeerde globale mbox ( doel-globaal-mbox) gebruikt, en dan kiest metrisch als succes metrisch, de metrische verhogingen slechts op pagina&#39;s die de mbox hebben die in de activiteit wordt gebruikt. Als uw box bijvoorbeeld homepage\_mbox is, is de metrische waarde Pagina&#39;s per bezoek het aantal hits op de startpagina\_mbox tijdens dat bezoek. (TGT-22789)
* Er wordt een JavaScript-uitzondering gegenereerd wanneer u tijdens stap 1 van het proces een ervaring verwijdert die betrekking heeft op een Experience Targeting-activiteit (XT) wanneer u de Form-Based Experience Composer gebruikt. (TGT-24366)

De eerste kwestie is vastgelegd in de Target 17.3.1-release (maart 2017).

De tweede kwestie is vastgelegd in de Target 17.6.1-release (juni 2017).

### at.js {#at-js-5}

Sinds de versie van Doel 17.4.1 (27 april, 2017), die de actie van het Beeld van het Tussenvoegsel in Visuele Composer van de Ervaring (VEC) gebruikt veroorzaakt dat de aanbiedingsinhoud niet wordt geleverd wanneer het gebruiken van de bibliotheek at.js.

Er is een oplossing voor dit probleem gevonden voor versie 0.js van 22 mei 2017.

### Rapportage: Activiteiten in het kader van A/B en Experience Targeting (XT)

Tussen 27 april om 29.00 uur PST en 5 mei om 6:00 uur PST, A/B en XT activiteiten die met om het even welke metriek worden gecreeerd of worden uitgegeven gebruikend de &quot;Bekeken een actie van de Pagina&quot;omzetting (die niet op andere metriek gebaseerd waren), zouden verkeerd geregistreerde omzettingen kunnen hebben. Dit probleem is nu opgelost. de rapportage over de conversieactie &quot;Bekeken een pagina&quot; voor deze activiteiten tijdens de betrokken periode is echter wellicht niet correct en kan helaas niet worden gecorrigeerd. We raden u aan om voor beslissingen die zijn gebaseerd op conversieacties voor &quot;Bekeken een pagina&quot; voor deze activiteiten alleen te vertrouwen op gegevens die zijn vastgelegd voor of na de betreffende periode.

Rapportage van gegevens voor andere metriek kan nog steeds worden gebruikt omdat ze geen effect hadden.

Opgelost in de hotfix Doel 17.4.3.

### Voorstellen: Activiteiten in het kader van A/B en Experience Targeting (XT)

De levering en voorvertoning werden beïnvloed voor aanbiedingen in A/B- en XT-activiteiten met ten minste twee ervaringen die zijn gemaakt of bewerkt met behulp van de Form-Based Experience Composer tussen vrijdag 28 april (28.00 uur PT) en maandag 1 mei (28.00 uur PT). Er zijn alleen voorstellen met standaardinhoud weergegeven.

Opgelost in de hotfix Doel 17.4.3.

### at.js {#at-js-6}

De volgende acties veroorzaakten de aanbieding om niet te worden geleverd wanneer het gebruiken van Visual Experience Composer (VEC) en at.js: Verplaatsen en opnieuw rangschikken.

Er is een oplossing voor dit probleem gemaakt voor versie 0.js 0.9.6.

### Rapporten

De capaciteit om veelvoudige metriek in een rapport te bekijken, inbegrepen in Doelversie 17.3.1 (30 maart, 2017) is verwijderd toe te schrijven aan onverwacht gedrag. Deze functie is in een volgende release weer beschikbaar.

De capaciteit om veelvoudige metriek in een rapport te bekijken was inbegrepen in Doelversie 17.4.1 (27 april 2017).

### Aanbiedingen

Afbeeldingen die zijn verwijderd uit de bibliotheek met afbeeldingsaanbiedingen ( \> Afbeeldingsaanbiedingen ) blijven zichtbaar in de gebruikersinterface. In een volgende release worden deze verwijderde afbeeldingen niet meer weergegeven. Ondertussen worden verwijderde afbeeldingen weergegeven in de gebruikersinterface, maar hebben ze de status Verwijderd. (TGT-23793)

Opgelost in de doelversie 17.4.1 (27 april 2017).

### Aanbiedingen omleiden

Voor recent bekeken criteria, op entiteit gebaseerde dynamische regels zullen tot geen aanbeveling leiden als de parameter entity.id niet in het mbox verzoek wordt overgegaan. (RECS-6241)

Dit probleem is opgelost na de release van Recommendations (22 maart 2018). Na de release van Recommendations slaat Target de op entiteit gebaseerde dynamische regels over als entity.id niet wordt doorgegeven in de mbox-aanvraag.

### at.js {#at-js-7}

Wanneer gebruikers proberen om te.js van de de detailpagina van Implementaties na het bijwerken van om.js montages te downloaden, wordt gedownload in plaats van at.js. (TGT-23069)

Vast in de Target 17.3.1-release (30 maart 2017).

### Algemene uitsluitingsregels

De wereldwijde uitsluitingsregels duren 10 tot 20 minuten om zich aan de rand van Premium Recommendations te verspreiden. (RECS-5270)

Opgelost in de Recommendations 17.2.2.0-release (6 maart 2017).

### Analyses voor Adobe Target (A4T)-rapportage

De rapporten worden niet bijgewerkt wanneer rapporteringsmetrisch wordt geschakeld. Dit probleem is alleen van invloed op de gebruikersinterface. Er is geen invloed op het verzamelen of leveren van gegevens. (TGT-22970)

Vast in de Target 17.2.2.0-release (24 februari 2017).

### CSV-rapporten

Gedownloade rapporten voldoen niet aan de instelling Extreme Orders uitsluiten. (TGT-21871)

Correctie in de doelversie 17.2.1.0.
