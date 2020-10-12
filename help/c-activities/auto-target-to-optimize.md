---
keywords: auto-target;targeting;traffic allocation;frequently aske questions;faq;troubleshooting;trouble shooting
description: Auto-Target in Adobe Target maakt gebruik van geavanceerd leren van computers om te kiezen uit meerdere veeleisende markeervaringen om de inhoud en schijfconversies aan te passen. Auto-Target dient voor elke bezoeker de meest toegesneden ervaring op basis van zijn of haar individuele klantprofiel en het gedrag van vorige bezoekers met gelijkaardige profielen.
title: Automatisch doel
feature: auto-target
topic: Standard
uuid: fce769d2-9e7f-4064-add7-76e1fc394b4f
translation-type: tm+mt
source-git-commit: 5675672777c778676b878dee2f713b16bc62bc1e
workflow-type: tm+mt
source-wordcount: '3639'
ht-degree: 0%

---


# ![PREMIUM](/help/assets/premium.png) Auto-Target

[!UICONTROL Auto-Target] maakt gebruik van geavanceerd leren van computers om uit meerdere veelzijdige, door markers gedefinieerde ervaringen te kiezen voor het aanpassen van inhoud en schijfconversies. Auto-Target dient voor elke bezoeker de meest toegesneden ervaring op basis van zijn of haar individuele klantprofiel en het gedrag van vorige bezoekers met gelijkaardige profielen.

>[!NOTE]
>
>[!UICONTROL Auto-Target] is beschikbaar als onderdeel van de [!DNL Target Premium] oplossing. Deze functie is niet beschikbaar in [!DNL Target Standard] zonder een [!DNL Target Premium] licentie. Zie [Target Premium](/help/c-intro/intro.md)voor meer informatie over de geavanceerde functies die deze licentie biedt.

## Real-world succesverhaal met Auto-Target {#success}

Een grote kledinghandelaar gebruikte onlangs een [!UICONTROL Auto-Target] activiteit met tien op productcategorieën gebaseerde ervaringen (plus gerandomiseerde controle) om de juiste inhoud aan elke bezoeker te leveren. &quot;[!UICONTROL Add to Cart]&quot; is gekozen als de primaire optimalisatiemethode. De beoogde ervaringen liepen gemiddeld op met 29,09%. Na het bouwen van de [!UICONTROL Auto-Target] modellen, werd de activiteit geplaatst aan 90% gepersonaliseerde ervaringen.

In slechts tien dagen werd meer dan $1.700.000 in lift bereikt.

Blijf lezen om te leren hoe u [!UICONTROL Auto-Target] de lift en de inkomsten voor uw organisatie kunt verhogen.

## Overzicht {#section_972257739A2648AFA7E7556B693079C9}

Tijdens het [maken van een A/B-activiteit met behulp van de driestappenworkflow](../c-activities/t-test-ab/t-test-create-ab/test-create-ab.md#task_68C8079BF9FF4625A3BD6680D554BB72)met instructies kunt u ervoor kiezen om verkeer toe te wijzen met behulp van de [!UICONTROL Auto-Target For Personalized Experiences] optie:

![Automatisch richten voor persoonlijke ervaringen, optie](/help/c-activities/assets/auto-target-ui-new.png)

Met de [!UICONTROL Auto-Target] optie in de activiteitsstroom A/B kunt u automatisch leren aanpassen op basis van een set markeerervaringen met één klik. [!UICONTROL Auto-Target] is ontworpen voor maximale optimalisatie in vergelijking met traditionele A/B-tests of Automatische toewijzing, door te bepalen welke ervaring voor elke bezoeker moet worden weergegeven. In tegenstelling tot een A/B-activiteit waarbij het doel is één winnaar te vinden, bepaalt [!UICONTROL Auto-Target] automatisch de beste ervaring voor een bepaalde bezoeker (op basis van zijn of haar profiel en andere contextuele informatie) om een zeer gepersonaliseerde ervaring te leveren.

Op dezelfde manier als Automated Personalization, gebruikt [!UICONTROL Auto-Target] een Random Forest-algoritme, een toonaangevende methode voor het samenvoegen van gegevenswetenschap, om de beste ervaring te bepalen die aan een bezoeker moet worden getoond. Omdat [!UICONTROL Auto-Target] u zich kunt aanpassen aan wijzigingen in het gedrag van de bezoeker, kunt u deze altijd uitvoeren om een lift te maken. Dit wordt soms ook wel de &quot;always-on&quot;-modus genoemd.

In tegenstelling tot een activiteit A/B waarin de ervaringstoewijzing voor een bepaalde bezoeker kleverig is, [!UICONTROL Auto-Target] optimaliseert het gespecificeerde bedrijfsdoel over elk bezoek. Als binnen, [!UICONTROL Auto Personalization][!UICONTROL Auto-Target]door gebrek, reserveert een deel van het verkeer van de activiteit als controlegroep om lift te meten. Bezoekers in de controlegroep krijgen een willekeurige ervaring in de activiteit.

## Overwegingen

Houd rekening met het volgende wanneer u [!UICONTROL Auto-Target]:

* U kunt een specifieke activiteit niet van [!UICONTROL Auto-Target] naar Automated Personalization, en vice versa schakelen.
* U kunt niet van Handmatige verkeerstoewijzing (traditionele Test A/B) aan, [!UICONTROL Auto-Target], en vice versa schakelen nadat een activiteit levend is.
* Één model wordt gebouwd om de prestaties van de gepersonaliseerde strategie tegenover willekeurig gediend verkeer tegenover het verzenden van al verkeer naar het algemene winnen ervaring te identificeren. In dit model worden alleen resultaten en omzettingen in de standaardomgeving bekeken.

   Het verkeer van een tweede reeks modellen wordt gebouwd voor elke modelleringsgroep (AP) of ervaring (AT). Voor elk van deze modellen worden hits en conversies in alle omgevingen in overweging genomen.

   De verzoeken zullen daarom met hetzelfde model worden gediend, ongeacht het milieu, maar de pluraliteit van het verkeer zou van het standaardmilieu moeten komen om ervoor te zorgen dat de geïdentificeerde over het geheel genomen winnende ervaring verenigbaar met echt gedrag is.

* U moet minimaal twee ervaringen gebruiken.

## Terminologie {#section_A309B7E0B258467789A5CACDC1D923F3}

De volgende termen zijn handig wanneer u discussieert over [!UICONTROL Auto-Target]:

| Term | Definitie |
|---|---|
| Meervoudig bewapende bandit | Een veelbewapende bandibenadering voor optimalisering brengt een evenwicht tot stand tussen verkennend leren en het benutten van dat leren. |
| Willekeurig bos | Random Forest is een toonaangevende aanpak voor machinaal leren. Op het gebied van gegevenswetenschappen is het een ensemble classificatie, of regressiemethode, die werkt door een groot aantal beslissingsbomen te bouwen op basis van bezoekers en bezoekkenmerken. Binnen Target wordt het Willekeurige bos gebruikt om te bepalen welke ervaring naar verwachting de hoogste waarschijnlijkheid van omzetting (of hoogste opbrengst per bezoek) voor elke specifieke bezoeker zal hebben. Voor meer informatie over Willekeurig bos in Doel, zie [Willekeurig Bosalgoritme](../c-activities/t-automated-personalization/algo-random-forest.md#concept_48F3CDAA16A848D2A84CDCD19DAAE3AA). |
| Thompson Sampling | Het doel van Thompson Sampling is te bepalen welke ervaring de beste algemene (niet-gepersonaliseerde) ervaring is, terwijl de &#39;kosten&#39; van het vinden van die ervaring tot een minimum worden beperkt. Thompson-steekproeven kiezen altijd een winnaar, zelfs als er geen statistisch verschil tussen twee ervaringen is. Zie [Thompson Sampling](https://en.wikipedia.org/wiki/Thompson_sampling)voor meer informatie. |

## Hoe [!UICONTROL Auto-Target] werkt {#section_77240E2DEB7D4CD89F52BE0A85E20136}

Meer informatie over de onderliggende gegevens en algoritmen [!UICONTROL Auto-Target] en Automated Personalization vindt u op de volgende links:

| Term | Details |
|--- |--- |
| [Random Forest Algorithm](/help/c-activities/t-automated-personalization/algo-random-forest.md) | Het belangrijkste verpersoonlijkingsalgoritme van het doel dat in zowel [!UICONTROL Auto-Target] als Automated Personalization wordt gebruikt is Random Forest. Met methoden als Random Forest kunt u meerdere leeralgoritmen gebruiken om betere voorspellende prestaties te verkrijgen dan met elk van de deelleeralgoritmen. Het algoritme Willekeurig bos in het geautomatiseerde verpersoonlijkingssysteem is een classificatie, of regressiemethode, die door een veelheid van beslissingsbomen in opleidingstijd te construeren werkt. |
| [Gegevens uploaden voor de Persoonlijke Algoritmen van het Doel](/help/c-activities/t-automated-personalization/algo-random-forest.md) | Er zijn verschillende manieren om gegevens in te voeren voor [!UICONTROL Auto-Target] Automated Personalization- en-modellen. |
| [Gegevensverzameling voor personaliseringsalgoritmen van het Doel](/help/c-activities/t-automated-personalization/ap-data.md) | De personalisatiealgoritmen van het doel verzamelen automatisch een verscheidenheid van gegevens. |

## Verkeerstoewijzing bepalen {#section_AB3656F71D2D4C67A55A24B38092958F}

Afhankelijk van het doel van uw activiteit, zou u een verschillende verkeerstoewijzing tussen controle en gepersonaliseerde ervaringen kunnen kiezen. De beste praktijken moeten dit doel bepalen alvorens u uw activiteit Levend maakt.

In de [!UICONTROL Custom Allocation] vervolgkeuzelijst kunt u de volgende opties kiezen:

* Beoordelen van algoritme voor personalisatie
* Personalisatieverkeer maximaliseren
* Aangepaste toewijzing

![Vervolgkeuzelijst Toewijzingsdoel](/help/c-activities/assets/split-new.png)

| Activiteitsdoelstelling | Voorgestelde verkeerstoewijzing | Aftrekposten |
|--- |--- |--- |
| **Evalueer het Algoritme van de Personalisatie (50/50)**: Als uw doel het algoritme is te testen, gebruik een 50/50 percenten verdeling van bezoekers tussen de controle en het gerichte algoritme. Deze splitsing geeft de meest nauwkeurige schatting van de lift. Voorgesteld voor gebruik met &quot;willekeurige ervaringen&quot; als controle. | 50% controle / 50% persoonlijke ervaring gesplitst | <ul><li>Maximaliseert nauwkeurigheid van lift tussen controle en gepersonaliseerd</li><li>Relatief minder bezoekers hebben een persoonlijke ervaring</li></ul> |
| **Personaliseringsverkeer maximaliseren (90/10)**: Als uw doel het creëren van &quot;altijd op&quot;activiteit is, zet 10% van de bezoekers in de controle om ervoor te zorgen dat er genoeg gegevens voor de algoritmen zijn om in tijd te blijven leren. Merk op de handel hier is dat in ruil voor het personaliseren van een groter deel van uw verkeer, u minder precisie in wat de nauwkeurige lift is zult hebben. Wat u ook wilt, dit is de aanbevolen verkeerssplitsing wanneer u een specifieke ervaring als besturingselement gebruikt. | De beste manier is om een Controle van 10% - 30% / 70% - 90% Persoonlijke Ervaring te gebruiken verdeeld | <ul><li>Maximaliseert het aantal bezoekers met een persoonlijke ervaring</li><li>Maximaliseert lift</li><li>Minder nauwkeurigheid wat betreft wat de lift voor de activiteit is</li></ul> |
| **Aangepaste toewijzing** | Splits het percentage handmatig naar wens. | <ul><li>U bereikt mogelijk niet de gewenste resultaten. Als u twijfelt, volgt u de suggesties voor een van de voorgaande opties</li></ul> |

Klik op de pictogrammen in de kolom Toewijzing om het percentage voor besturing aan te passen. U kunt de controlegroep niet tot minder dan 10% verminderen.

![Automatische doeltoewijzing wijzigen](/help/c-activities/assets/auto-target-control.png)

U kunt een specifieke ervaring [selecteren om als controle](/help/c-activities/t-automated-personalization/experience-as-control.md) te gebruiken of u kunt de Willekeurige ervaringsoptie gebruiken.

## Wanneer moet je kiezen [!UICONTROL Auto-Target] over Automated Personalization? {#section_BBC4871C87944DD7A8B925811A30C633}

Er zijn verschillende scenario&#39;s waarin u [!UICONTROL Auto-Target] de voorkeur geeft aan Automated Personalization:

* Als u de hele ervaring wilt definiëren in plaats van afzonderlijke aanbiedingen die automatisch worden gecombineerd om een ervaring te vormen.
* Als u de volledige reeks eigenschappen van Visual Experience Composer (VEC) wilt hefboomwerking die niet door [!UICONTROL Auto Personalization]: de redacteur van de douanecode, veelvoudige ervaringspubliek, en meer.
* Als u structurele wijzigingen in uw pagina wilt aanbrengen in verschillende ervaringen. Als u bijvoorbeeld de volgorde van de elementen op uw startpagina wilt wijzigen, [!UICONTROL Auto-Target] is dit geschikter dan Automated Personalization.

## Wat [!UICONTROL Auto-Target] heeft Automated Personalization gemeen? {#section_2A601F482F9A44E38D4B694668711319}

**Het algoritme optimaliseert voor een gunstig resultaat voor elk bezoek.**

* Het algoritme voorspelt de neiging van een bezoeker voor omzetting (of geschatte opbrengst van omzetting) om de beste ervaring te dienen.
* Een bezoeker komt in aanmerking voor een nieuwe ervaring aan het einde van een bestaande sessie (tenzij de bezoeker deel uitmaakt van de controlegroep, in welk geval de ervaring die de bezoeker tijdens zijn eerste bezoek heeft opgedaan, dezelfde blijft voor latere bezoeken).
* Binnen een sessie verandert de voorspelling niet om de visuele consistentie te behouden.

**Het algoritme wordt aangepast aan wijzigingen in het gedrag van de bezoeker.**

* De multi-armbandit verzekert het model altijd &quot;bestedend&quot;een klein fractie verkeer om door het leven van het activiteit leren te blijven leren en overexploitatie van eerder geleerde tendensen te verhinderen.
* De onderliggende modellen worden elke 24 uur opnieuw samengesteld met behulp van de meest recente gedragsgegevens van de bezoeker, zodat Target altijd gebruikmaakt van veranderende voorkeuren voor bezoekers.
* Als het algoritme het winnen van ervaringen voor individuen niet kan bepalen, schakelt het automatisch aan het tonen van de algemene best-presterende ervaring terwijl nog steeds het zoeken naar gepersonaliseerde winnaars blijft. De best presterende ervaring wordt gevonden gebruikend steekproef [van](https://en.wikipedia.org/wiki/Thompson_sampling)Thompson.

**Het algoritme optimaliseert voortdurend voor één enkel doel metrisch.**

* Deze metrische waarde zou op omzettingsbasis of op opbrengst-gebaseerd (meer bepaald Inkomsten per Bezoek) kunnen zijn.

**Het algoritme steunt niet het gebruiken [!DNL Analytics] als gegeven-bron of een rapporterend eindpunt.**

**Het doel verzamelt automatisch informatie over bezoekers om de verpersoonlijkingsmodellen te bouwen.**

* Voor meer informatie over de parameters die in [!UICONTROL Auto-Target] en Automated Personalization worden gebruikt, zie de Inzameling [van Gegevens van](../c-activities/t-automated-personalization/ap-data.md#reference_255BD3DE7AD04DC9B766E0BC78961058)Automated Personalization.

**Het doel gebruikt automatisch alle Experience Cloud gedeelde publiek om de verpersoonlijkingsmodellen te bouwen.**

* U hoeft niets specifiek te doen om publiek aan het model toe te voegen. Voor informatie over het gebruiken van Experience Cloud Soorten publiek met Doel, zie [Experience Cloud Soorten publiek](../c-integrating-target-with-mac/mmp.md#concept_F4863DE4C92D4805AB690B4B3D487969)

**Marketers kunnen offlinegegevens, proxyscores of andere aangepaste gegevens uploaden om personalisatiemodellen samen te stellen.**

* Meer informatie over het [uploaden van gegevens voor Auto-Target en Automated Personalization](../c-activities/t-automated-personalization/uploading-data-for-the-target-personalization-algorithms.md#concept_85EA505B37E54514A1C8AB91553FEED6).

## Hoe verschilt [!UICONTROL Auto-Target] dit van Automated Personalization? {#section_BA4D83BE40F14A96BE7CBC7C7CF2A8FB}

**[!UICONTROL Auto-Target]vereist vaak minder verkeer dan Automated Personalization voor een gepersonaliseerd model om te bouwen.**

Hoewel de hoeveelheid verkeer *per ervaring* die voor [!UICONTROL Auto-Target] of [!UICONTROL Auto Personalization] modellen wordt vereist om te bouwen het zelfde is, zijn er gewoonlijk meer ervaringen in een activiteit van Automated Personalization dan een [!UICONTROL Auto-Target] activiteit. Bijvoorbeeld, als u een [!UICONTROL Auto Personalization] activiteit had waar u twee aanbiedingen per plaats met twee plaatsen hebt gecreeerd, zouden er vier (2 = 4) totale ervaringen inbegrepen in de activiteit (zonder uitsluitingen) zijn. Met [!UICONTROL Auto-Target]behulp van, zou u ervaring 1 kunnen plaatsen om aanbieding 1 in plaats 1 en aanbieding 2 in plaats 2 te omvatten, en ervaring 2 om aanbieding 1 in plaats 1 en aanbieding 2 in plaats 2 te omvatten. Omdat [!UICONTROL Auto-Target] u meerdere wijzigingen binnen één ervaring kunt doorvoeren, kunt u het aantal ervaringen in uw activiteit verminderen.

Voor [!UICONTROL Auto-Target], kunnen de eenvoudige regels van duim worden gebruikt om verkeersvereisten te begrijpen:

* **Wanneer Conversion uw succes metrisch is:** 1.000 bezoeken en ten minste 50 conversies per dag per ervaring, en daarnaast moeten de activiteiten ten minste 7.000 bezoeken en 350 conversies hebben.
* **Wanneer de Opbrengst per Bezoek uw succesmetrisch is:** 1.000 bezoeken en ten minste 50 conversies per dag per ervaring, en daarnaast moet de activiteit ten minste 1.000 conversies per ervaring hebben. RPV vereist gewoonlijk meer gegevens om modellen samen te stellen vanwege de hogere gegevensvariantie die gewoonlijk bestaat in de opbrengsten van bezoeken in vergelijking met de omrekeningskoers.

**[!UICONTROL Auto-Target]heeft volledige instellingsfunctionaliteit.**

* Omdat [!UICONTROL Auto-Target] in het A/B activiteitenwerkschema ingebed is, [!UICONTROL Auto-Target] profiteert van de rijkere en volwaardige Composer van de Visuele Ervaring (VEC). U kunt ook gebruikmaken van [QA-koppelingen](../c-activities/c-activity-qa/activity-qa.md#concept_9329EF33DE7D41CA9815C8115DBC4E40) met [!UICONTROL Auto-Target].

**[!UICONTROL Auto-Target]biedt een uitgebreid onlinetestframework.**

* De multiarmbandit maakt deel uit van een groter online testkader dat onze data-wetenschappers en onderzoekers in staat stelt de voordelen van hun voortdurende verbeteringen in de reële omstandigheden te begrijpen.
* In de toekomst zullen we met deze testbank ons computerleerplatform kunnen openen voor onze klanten met data-savvy, zodat ze hun eigen modellen kunnen introduceren om de modellen van Target te versterken.

## Rapportage en [!UICONTROL Auto-Target] {#section_42EE7F5E65E84F89A872FE9921917F76}

Voor meer informatie, zie [auto-Doel SamenvattingsRapport](../c-reports/auto-target-summary-report.md#concept_E2171F7B57C1417DAAD7E7909A3FB073) in de sectie van [Rapporten](../c-reports/reports.md#concept_B5077F5503AA4C98901AA99EDCE6CDE6) .

## Veelgestelde vragen over automatisch doel {#section_5C120A2B11D14D9BAF767BBAB50FED23}

Raadpleeg de volgende veelgestelde vragen en antwoorden terwijl u met [!UICONTROL Auto-Target] activiteiten werkt:

### Wat zijn de beste praktijken om een [!UICONTROL Auto-Target] activiteit te vestigen?

* Beslissen of de bedrijfswaarde van een (RPV) succesmetrisch van de Inkomsten per Bezoek de extra verkeersvereisten waard is. RPV heeft doorgaans minstens 1.000 conversies per ervaring nodig om een activiteit te kunnen gebruiken in plaats van conversie.
* Beslis over de toewijzing tussen controle en gepersonaliseerde ervaringen alvorens met de activiteit te beginnen die op uw doelstellingen wordt gebaseerd.
* Bepaal als u voldoende verkeer aan de pagina hebt waar uw [!UICONTROL Auto-Target] activiteit voor verpersoonlijkingsmodellen zal lopen om in een redelijke hoeveelheid tijd te bouwen.
   * Als u het verpersoonlijkingsalgoritme test, moet u geen ervaringen veranderen of profielkenmerken toevoegen/verwijderen terwijl de activiteit actief is.

* Overweeg een A/B activiteit tussen de aanbiedingen en plaatsen te voltooien u in uw [!UICONTROL Auto-Target] activiteit van plan bent te gebruiken om te verzekeren de plaats(en) en de aanbiedingen een effect op het optimalisatiedoel hebben. Als een A/B-activiteit geen significant verschil aantoont, zal het [!UICONTROL Auto-Target] waarschijnlijk ook niet lukken om een lift te genereren.

   * Als een A/B test geen statistisch significante verschillen tussen ervaringen toont, is het waarschijnlijk dat de aanbiedingen u overweegt niet genoeg van elkaar verschillend zijn, beïnvloeden de plaatsen u selecteerde niet succesmetrisch, of het optimalisatiedoel is te ver in de omzettingrechter om door uw gekozen aanbiedingen te worden beïnvloed.

* Probeer de ervaringen tijdens de activiteiten niet ingrijpend te wijzigen.

### Zijn de vinkjes die erop wijzen dat een model voor die ervaring wordt gebouwd update als de waaier van de rapportdatum verandert?

Nee, de vinkjes voor het genereren van modellen geven alleen de modellen weer die tot op heden zijn gemaakt. Er is geen manier om terug te gaan en te zien wanneer een model werd voltooid.

### Als een bezoeker de [!UICONTROL Auto-Target] activiteit NIET ziet en omzet, telt de omzetting in mijn activiteit?

Nee, alleen bezoekers die in aanmerking komen voor de [!UICONTROL Auto-Target] activiteit worden meegeteld in de rapportage.

### Mijn [!UICONTROL Auto-Target] activiteit lijkt geen lift te genereren. Wat is er aan de hand?

Er zijn vier factoren vereist voor een [!UICONTROL Auto-Target] activiteit om lift te produceren:

* De aanbiedingen moeten verschillend genoeg zijn om bezoekers te beïnvloeden.
* De aanbiedingen moeten zich ergens bevinden die een verschil maken met het optimalisatiedoel.
* Er moet voldoende verkeer en statistische &quot;kracht&quot; in de test aanwezig zijn om de lift te detecteren.
* Het verpersoonlijkingsalgoritme moet goed werken.

De beste manier van werken is eerst ervoor te zorgen dat de inhoud en de locaties waaruit de activiteitenervaringen bestaan daadwerkelijk een verschil maken met de totale responspercentages met behulp van een eenvoudige, niet-gepersonaliseerde A/B-test. Zorg ervoor dat u de monstergrootten vooraf berekent om ervoor te zorgen dat er voldoende kracht is om een redelijke lift te zien en de A/B-test voor een vaste duur uit te voeren zonder deze te stoppen of wijzigingen aan te brengen.

Als uit de resultaten van een A/B-test statistisch significante resultaten van een of meer ervaringen blijken, is het waarschijnlijk dat een gepersonaliseerde activiteit zal werken. Natuurlijk kan personalisatie werken zelfs als er geen verschillen zijn in de totale responspercentages van de ervaringen. Doorgaans is het probleem het gevolg van aanbiedingen/locaties die niet voldoende invloed hebben op het optimalisatiedoel en die statistisch significant moeten worden opgespoord.

### Wanneer moet ik mijn [!UICONTROL Auto-Target] activiteit stopzetten?

[!UICONTROL Auto-Target] kan worden gebruikt als &quot;altijd op&quot;verpersoonlijking die constant zal optimaliseren. Met name voor de groengroene inhoud is het niet nodig om uw [!UICONTROL Auto-Target] activiteit te stoppen.

Als u substantiële wijzigingen wilt aanbrengen in de inhoud van uw [!UICONTROL Auto-Target] activiteit, kunt u het beste een nieuwe activiteit starten zodat andere gebruikers die rapporten controleren, oude resultaten niet verwarren of met andere inhoud in verband brengen.

### Hoe lang moet ik wachten op modellen om te bouwen? {#how-long}

De tijdsduur die het voor modellen vergt om in uw [!UICONTROL Auto-Target] activiteit te bouwen hangt typisch van het verkeer aan uw geselecteerde activiteitenplaats(en) en omzettingspercentages verbonden aan u metrische activiteit af.

[!UICONTROL Auto-Target] zal niet proberen om een gepersonaliseerd model voor een bepaalde ervaring te bouwen tot er minstens 50 omzettingen voor die ervaring zijn. Bovendien als het gebouwde model van ontoereikende kwaliteit is (zoals die door off-line evaluatie op greep &quot;test&quot;gegevens wordt bepaald, gebruikend metrisch die als AUC [](https://en.wikipedia.org/wiki/Receiver_operating_characteristic#Area_under_the_curve)wordt bekend), zal het model niet worden gebruikt om verkeer op een gepersonaliseerde manier te dienen.

Nog enkele punten die u in gedachten wilt houden over [!UICONTROL Auto-Target]het modelgebouw:

* Zodra een activiteit levend is, [!UICONTROL Auto-Target] overweegt tot de laatste 45 dagen van willekeurig gediende gegevens wanneer het proberen om modellen (d.w.z. controleverkeer, plus sommige extra willekeurig gediende gegevens die door ons algoritme worden gehouden) te bouwen.
* Wanneer [!UICONTROL Revenue per Visit] uw succes metrisch is, vereisen deze activiteiten typisch meer gegevens om modellen te bouwen wegens de hogere gegevensvariantie die typisch in bezoek-opbrengst in vergelijking met omzettingspercentage bestaat.
* Omdat de modellen op een per-ervaringsbasis worden voortgebouwd, die één ervaring met een andere middelen vervangen die voldoende verkeer (d.w.z. minstens 50 omzettingen) voor de nieuwe ervaring moeten worden verzameld alvorens de gepersonaliseerde modellen kunnen worden herbouwd.

### Eén model is ingebouwd in mijn activiteit. Zijn de bezoeken aan die ervaring gepersonaliseerd?

Nee, er moeten ten minste twee modellen in uw activiteiten zijn ingebouwd voordat de personalisatie begint.

### Wanneer kan ik naar de resultaten van mijn [!UICONTROL Auto-Target] activiteit gaan kijken?

U kunt de resultaten van uw [!UICONTROL Auto-Target] test bekijken nadat u minstens twee ervaringen met gebouwde modellen hebt (groen vinkje) voor de ervaring die modellen heeft gebouwd.

### Kan ik een specifieke ervaring specificeren die als controle moet worden gebruikt?

U kunt een ervaring selecteren die als controle moet worden gebruikt terwijl het creëren van een [Automated Personalization](/help/c-activities/t-automated-personalization/automated-personalization.md) (AP) of [Auto-Doel](/help/c-activities/auto-target-to-optimize.md) (AT) activiteit.

Deze eigenschap laat u het volledige controleverkeer aan een specifieke ervaring leiden, die op het percentage van de verkeerstoewijzing wordt gebaseerd dat in de activiteit wordt gevormd. U kunt de prestatiesrapporten van het gepersonaliseerde verkeer tegen controleverkeer aan die één ervaring dan evalueren.

Zie Een specifieke ervaring [gebruiken als controle](/help/c-activities/t-automated-personalization/experience-as-control.md)voor meer informatie.

### Kan ik het doel metrische middenweg door een auto-Doelactiviteit veranderen? {#change-metric}

Wij adviseren niet dat u het doel metrische middenweg door een activiteit verandert. Hoewel het mogelijk is om doel metrisch tijdens een activiteit te veranderen gebruikend [!DNL Target] UI, zou u altijd een nieuwe activiteit moeten beginnen. Wij garanderen niet wat gebeurt als u het doel metrisch in een activiteit verandert nadat het loopt.

Deze aanbeveling is van toepassing op [!UICONTROL Auto-Allocate], [!UICONTROL Auto-Target]en [!UICONTROL Automated Personalization] activiteiten die ofwel [!DNL Target] of [!DNL Analytics] (A4T) als rapportagebron gebruiken.

### Kan ik de optie Rapportgegevens opnieuw instellen gebruiken tijdens het uitvoeren van een automatisch doelactiviteit?

Het gebruik van de [!UICONTROL Reset Report Data] optie voor [!UICONTROL Auto-Target] activiteiten wordt niet voorgesteld. Hoewel de zichtbare rapportgegevens worden verwijderd, worden met deze optie niet alle trainingsrecords uit het [!UICONTROL Auto-Target] model verwijderd. In plaats van de [!UICONTROL Reset Report Data] optie voor [!UICONTROL Auto-Target] activiteiten te gebruiken, maakt u een nieuwe activiteit en deactiveert u de oorspronkelijke activiteit. (Opmerking: Deze leidraad is ook van toepassing op [!UICONTROL Auto-Allocate] en [!UICONTROL Automated Personalization] activiteiten.)

## Problemen oplossen [!UICONTROL Auto-Target] {#section_23995AB813F24525AF294D20A20875C8}

Soms gaan activiteiten niet zoals verwacht. Hier volgen enkele potentiële uitdagingen die u tijdens het gebruik kunt aangaan [!UICONTROL Auto-Target], en enkele voorgestelde oplossingen.

**Mijn [!UICONTROL Auto-Target] activiteit duurt te lang om modellen te bouwen.**

Er zijn verscheidene veranderingen van de activiteitenopstelling die de verwachte tijd kunnen verminderen om modellen te bouwen, met inbegrip van het aantal ervaringen in uw [!UICONTROL Auto-Target] activiteit, het verkeer aan uw plaats, en uw geselecteerde succesmetrisch.

**Oplossing:** Controleer uw activiteitenopstelling en zie of zijn er om het even welke veranderingen u bereid bent aan te brengen om de snelheid te verbeteren waarop de modellen zullen bouwen.

* Als uw succesmetrisch wordt geplaatst aan RPV, kunt u in omzetting veranderen? De activiteiten van de omzetting neigen om minder verkeer te vereisen om modellen te bouwen. U verliest geen activiteitsgegevens als u de succesmaatstaf wijzigt van RPV in conversie.
* Is uw succes metrisch ver onderaan de verkooptrechter van uw activiteitenervaringen? Een lager tarief van de activiteitenomzetting zal de verkeersvereisten verhogen nodig voor modellen om te bouwen, aangezien een minimumaantal omzettingen wordt vereist.
* Zijn er sommige ervaringen u van uw activiteit kunt laten vallen? Het verminderen van het aantal ervaringen in een activiteit zal de hoeveelheid tijd verminderen om modellen te bouwen.
* Is er een pagina voor hoger verkeer waarop deze activiteit succesvoller zou zijn? Hoe meer verkeer en conversies er in uw activiteitenlocaties plaatsvinden, hoe sneller de modellen worden.

**Mijn [!UICONTROL Auto-Target] activiteit genereert geen lift.**

Er zijn vier factoren vereist voor een AP-activiteit om lift te genereren:

* De aanbiedingen moeten verschillend genoeg zijn om bezoekers te beïnvloeden.
* De aanbiedingen moeten zich ergens bevinden die een verschil maken met het optimalisatiedoel.
* Er moet voldoende verkeer en statistische &quot;kracht&quot; in de test aanwezig zijn om de lift te detecteren.
* Het verpersoonlijkingsalgoritme moet goed werken.

**Oplossing:** Eerst, zorg ervoor dat uw activiteit verkeer personaliseert. Als modellen niet voor alle ervaringen worden gebouwd, dient uw [!UICONTROL Auto-Target] activiteit nog steeds willekeurig een aanzienlijk deel van bezoeken om te proberen om alle modellen zo snel mogelijk te bouwen. Als de modellen niet worden gebouwd, [!UICONTROL Auto-Target] is geen het personaliseren verkeer.

Daarna, zorg ervoor de aanbiedingen en de activiteitenplaatsen werkelijk een verschil aan de algemene reactiesnelheden gebruikend een eenvoudige, niet-gepersonaliseerde test A/B maken. Zorg ervoor dat u de monstergrootten vooraf berekent om ervoor te zorgen dat er voldoende kracht is om een redelijke lift te zien en de A/B-test voor een vaste duur uit te voeren zonder deze te stoppen of wijzigingen aan te brengen. Als een A/B-testresultaten statistisch significante lift op een of meer van de ervaringen laten zien, is het waarschijnlijk dat een gepersonaliseerde activiteit zal werken. Natuurlijk kan personalisatie werken zelfs als er geen verschillen zijn in de totale responspercentages van de ervaringen. Doorgaans is het probleem het gevolg van aanbiedingen/locaties die niet voldoende invloed hebben op het optimalisatiedoel en die statistisch significant moeten worden opgespoord.

**Om het even welk metrisch afhankelijk van omzettingsmetrisch zet nooit om.**

Dit wordt verwacht.

In een [!UICONTROL Auto-Target] activiteit, zodra een omzettingsmetrische (of optimalisatiedoel of post doel) wordt omgezet, wordt de gebruiker vrijgegeven van de ervaring en de activiteit wordt opnieuw begonnen.

Bijvoorbeeld, is er een activiteit met metrisch (C1) en extra metrisch (A1). A1 is afhankelijk van C1. Wanneer een bezoeker de activiteit voor het eerst ingaat, en de criteria voor het omzetten A1 en C1 niet worden omgezet, wordt metrische A1 niet omgezet toe te schrijven aan het succes metrische gebiedsdeel. Als de bezoeker C1 omzet en dan A1 omzet, wordt A1 nog niet omgezet omdat zodra C1 wordt omgezet, de bezoeker wordt vrijgegeven.

## Trainingsvideo: Inzicht in ![overzichtsbadge voor Auto-Target-activiteiten](/help/assets/overview.png)

In deze video wordt uitgelegd hoe u een [!UICONTROL Auto-Target] A/B-activiteit instelt.

Nadat u deze training hebt voltooid, kunt u het volgende doen:

* Testen definiëren [!UICONTROL Auto-Target]
* Vergelijken en contrast [!UICONTROL Auto-Target] met Automated Personalization
* Activiteiten [!UICONTROL Auto-Target] maken

>[!VIDEO](https://video.tv.adobe.com/v/18558)