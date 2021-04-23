---
keywords: autotarget;het richten;verkeerstoewijzing;vraag vaak;faq;het oplossen van problemen;het oplossen van problemen
description: Leer hoe een auto-Doelactiviteit in [!DNL Target] de meest op maat gemaakte ervaring aan elke bezoeker op klantenprofielen en het gedrag van gelijkaardige bezoekers wordt gebaseerd.
title: Wat is een automatisch doelactiviteit?
feature: Automatisch doel
exl-id: 59ca30dc-45a0-4129-b832-84e1132d3b69
translation-type: tm+mt
source-git-commit: a92e88b46c72971d5d3c752593d651d8290b674e
workflow-type: tm+mt
source-wordcount: '1927'
ht-degree: 0%

---

# ![Overzicht ](/help/assets/premium.png) van PREMIUMAuto-Target

[!UICONTROL Auto-Target] de activiteiten in  [!DNL Adobe Target] gebruik geavanceerde machine het leren om uit veelvoudige hoog-presterende tellers-bepaalde ervaringen te selecteren om inhoud en aandrijvingsomzettingen aan te passen. Auto-Target biedt elke bezoeker de meest op maat gemaakte ervaring op basis van het individuele klantprofiel en het gedrag van eerdere bezoekers met vergelijkbare profielen.

>[!NOTE]
>
>[!UICONTROL Auto-Target] is beschikbaar als onderdeel van de  [!DNL Target Premium] oplossing. Deze functie is niet beschikbaar in [!DNL Target Standard] zonder een [!DNL Target Premium] licentie. Zie [Doelpremium](/help/c-intro/intro.md) voor meer informatie over de geavanceerde functies die deze licentie biedt.
>
>[!UICONTROL Analytics for Target] (A4T) ondersteunt  [!UICONTROL Auto-Target] activiteiten. Voor meer informatie, zie [A4T steun voor auto-Wijs en auto-Doel activiteiten](/help/c-integrating-target-with-mac/a4t/a4t-at-aa.md).

## Real-world succesverhaal dat Auto-Target {#success} gebruikt

Een grote kledinghandelaar gebruikte onlangs een [!UICONTROL Auto-Target] activiteit met tien op productcategorie-gebaseerde ervaringen (plus gerandomiseerde controle) om de juiste inhoud aan elke bezoeker te leveren. &quot;[!UICONTROL Add to Cart]&quot; is gekozen als primaire optimalisatiemetrisch. De beoogde ervaringen liepen gemiddeld op met 29,09%. Na het bouwen van de [!UICONTROL Auto-Target] modellen, werd de activiteit geplaatst aan 90% gepersonaliseerde ervaringen.

In slechts tien dagen werd meer dan $1.700.000 in lift bereikt.

Lees verder om te leren hoe u [!UICONTROL Auto-Target] kunt gebruiken om de lift en de omzet voor uw organisatie te verhogen.

## Overzicht {#section_972257739A2648AFA7E7556B693079C9}

Terwijl u [een A/B-activiteit maakt met behulp van de driestappenworkflow met instructies](/help/c-activities/t-test-ab/t-test-create-ab/test-create-ab.md), kunt u desgewenst verkeer toewijzen met de optie [!UICONTROL Auto-Target For Personalized Experiences]:

![Automatisch richten voor persoonlijke ervaringen, optie](/help/c-activities/assets/auto-target-ui-new.png)

Met de optie [!UICONTROL Auto-Target] in de activiteitsstroom A/B kunt u automatisch leren aanpassen op basis van een set markeerervaringen met één klik. [!UICONTROL Auto-Target] is ontworpen voor maximale optimalisatie in vergelijking met traditionele A/B-tests of Automatische toewijzing, door te bepalen welke ervaring voor elke bezoeker moet worden weergegeven. In tegenstelling tot een A/B-activiteit waarbij het doel is één winnaar te vinden, bepaalt [!UICONTROL Auto-Target] automatisch de beste ervaring voor een bepaalde bezoeker (op basis van zijn of haar profiel en andere contextuele informatie) om een zeer gepersonaliseerde ervaring te leveren.

Op dezelfde manier als Automated Personalization, [!UICONTROL Auto-Target] gebruikt een Willekeurig algoritme van het Bos, een belangrijke methode van het samenstellen van de gegevenswetenschap, om de beste ervaring te bepalen om aan een bezoeker te tonen. Aangezien [!UICONTROL Auto-Target] zich kan aanpassen aan wijzigingen in het gedrag van de bezoeker, kan het permanent worden uitgevoerd om een lift te leveren. Dit wordt soms ook wel de &quot;always-on&quot;-modus genoemd.

In tegenstelling tot een activiteit A/B waarin de ervaringstoewijzing voor een bepaalde bezoeker kleverig is, [!UICONTROL Auto-Target] optimaliseert het gespecificeerde bedrijfsdoel over elk bezoek. Net als in [!UICONTROL Auto Personalization], [!UICONTROL Auto-Target], door gebrek, reserveert een deel van het verkeer van de activiteit als controlegroep om lift te meten. Bezoekers in de controlegroep krijgen een willekeurige ervaring in de activiteit.

## Overwegingen

Er zijn een paar belangrijke overwegingen in mening wanneer het gebruiken van [!UICONTROL Auto-Target]:

* U kunt een specifieke activiteit niet van [!UICONTROL Auto-Target] aan Automated Personalization, en vice versa schakelen.
* U kunt niet van Handmatige verkeerstoewijzing (traditionele Test A/B) aan [!UICONTROL Auto-Target], en vice versa schakelen nadat een activiteit levend is.
* Één model wordt gebouwd om de prestaties van de gepersonaliseerde strategie tegenover willekeurig gediend verkeer tegenover het verzenden van al verkeer naar het algemene winnen ervaring te identificeren. In dit model worden alleen resultaten en omzettingen in de standaardomgeving bekeken.

   Het verkeer van een tweede reeks modellen wordt gebouwd voor elke modelleringsgroep (AP) of ervaring (AT). Voor elk van deze modellen worden hits en conversies in alle omgevingen in overweging genomen.

   De verzoeken worden gediend met het zelfde model, ongeacht milieu, maar de pluraliteit van verkeer zou van het standaardmilieu moeten komen om ervoor te zorgen dat de geïdentificeerde algemene het winnen ervaring met echt gedrag verenigbaar is.

* Gebruik minimaal twee ervaringen.

## Terminologie {#section_A309B7E0B258467789A5CACDC1D923F3}

De volgende termen zijn handig wanneer u [!UICONTROL Auto-Target] bespreekt:

| Term | Definitie |
|---|---|
| Meervoudig bewapende bandit | Een veelbewapende bandibenadering voor optimalisering brengt een evenwicht tot stand tussen verkennend leren en het benutten van dat leren. |
| Willekeurig bos | Random Forest is een toonaangevende aanpak voor machinaal leren. Op het gebied van gegevenswetenschappen is het een ensemble classificatie, of regressiemethode, die werkt door veel beslissingsbomen te bouwen op basis van bezoekers en bezoekkenmerken. Binnen Target wordt het Willekeurige bos gebruikt om te bepalen welke ervaring naar verwachting de hoogste waarschijnlijkheid van omzetting (of hoogste opbrengst per bezoek) voor elke specifieke bezoeker zal hebben. Voor meer informatie over Willekeurig bos in Doel, zie [Random Forest Algorithm](/help/c-activities/t-automated-personalization/algo-random-forest.md). |
| Thompson Sampling | Het doel van Thompson Sampling is te bepalen welke ervaring de beste algemene (niet-gepersonaliseerde) ervaring is, terwijl de &#39;kosten&#39; van het vinden van die ervaring tot een minimum worden beperkt. Thompson-steekproeven kiezen altijd een winnaar, zelfs als er geen statistisch verschil tussen twee ervaringen is. Zie [Thompson Sampling](https://en.wikipedia.org/wiki/Thompson_sampling) voor meer informatie. |

## Hoe werkt [!UICONTROL Auto-Target] {#section_77240E2DEB7D4CD89F52BE0A85E20136}

Meer informatie over de onderliggende gegevens en algoritmen [!UICONTROL Auto-Target] en Automated Personalization vindt u op de onderstaande koppelingen:

| Term | Details |
|--- |--- |
| [Random Forest Algorithm](/help/c-activities/t-automated-personalization/algo-random-forest.md) | Het belangrijkste verpersoonlijkingsalgoritme van het doel dat in zowel [!UICONTROL Auto-Target] als Automated Personalization wordt gebruikt is Willekeurig bos. Met methoden als Random Forest kunt u meerdere leeralgoritmen gebruiken om betere voorspellende prestaties te verkrijgen dan met elk van de deelleeralgoritmen. Het Random Forest-algoritme in het Automated Personalization-systeem is een classificatiemethode, of regressiemethode, die werkt door een groot aantal beslissingsbomen te bouwen op het moment van training. |
| [Gegevens uploaden voor de Persoonlijke Algoritmen van het Doel](/help/c-activities/t-automated-personalization/algo-random-forest.md) | Er zijn verschillende manieren om gegevens in te voeren voor [!UICONTROL Auto-Target]- en Automated Personalization-modellen. |
| [Gegevensverzameling voor personaliseringsalgoritmen van het Doel](/help/c-activities/t-automated-personalization/ap-data.md) | De personalisatiealgoritmen van het doel verzamelen automatisch diverse gegevens. |

## Verkeerstoewijzing {#section_AB3656F71D2D4C67A55A24B38092958F} bepalen

Afhankelijk van het doel van uw activiteit, zou u een verschillende verkeerstoewijzing tussen controle en gepersonaliseerde ervaringen kunnen kiezen. De beste praktijken moeten dit doel bepalen alvorens u uw activiteit Levend maakt.

In de vervolgkeuzelijst [!UICONTROL Custom Allocation] kunt u de volgende opties kiezen:

* Beoordelen van algoritme voor personalisatie
* Personalisatieverkeer maximaliseren
* Aangepaste toewijzing

![Vervolgkeuzelijst Toewijzingsdoel](/help/c-activities/assets/split-new.png)

| Activiteitsdoelstelling | Voorgestelde verkeerstoewijzing | Aftrekposten |
|--- |--- |--- |
| **Evalueer het Algoritme van de Personalisatie (50/50)**: Als uw doel het algoritme is te testen, gebruik een 50/50 percenten verdeling van bezoekers tussen de controle en het gerichte algoritme. Deze splitsing geeft de meest nauwkeurige schatting van de lift. Voorgesteld voor gebruik met &quot;willekeurige ervaringen&quot; als controle. | 50% controle / 50% persoonlijke ervaring gesplitst | <ul><li>Maximaliseert nauwkeurigheid van lift tussen controle en gepersonaliseerd</li><li>Relatief minder bezoekers hebben een persoonlijke ervaring</li></ul> |
| **Personaliseringsverkeer maximaliseren (90/10)**: Als uw doel het creëren van &quot;altijd op&quot;activiteit is, zet 10% van de bezoekers in de controle om ervoor te zorgen dat er genoeg gegevens voor de algoritmen zijn om in tijd te blijven leren. De handel hier is dat in ruil voor het personaliseren van een groter deel van je verkeer, je minder nauwkeurigheid hebt in wat de exacte lift is. Wat u ook wilt, dit is de aanbevolen verkeerssplitsing wanneer u een specifieke ervaring als besturingselement gebruikt. | De beste manier is om een Controle van 10% - 30% / 70% - 90% Persoonlijke Ervaring te gebruiken verdeeld | <ul><li>Maximaliseert het aantal bezoekers met een persoonlijke ervaring</li><li>Maximaliseert lift</li><li>Minder nauwkeurigheid wat betreft wat de lift voor de activiteit is</li></ul> |
| **Aangepaste toewijzing** | Splits het percentage handmatig naar wens. | <ul><li>U bereikt mogelijk niet de gewenste resultaten. Als u twijfelt, volgt u de suggesties voor een van de voorgaande opties</li></ul> |

Klik op de pictogrammen in de kolom Toewijzing om het percentage voor besturing aan te passen. U kunt de controlegroep niet tot minder dan 10% verminderen.

![Automatische doeltoewijzing wijzigen](/help/c-activities/assets/auto-target-control.png)

U kunt [een specifieke ervaring selecteren om als controle ](/help/c-activities/t-automated-personalization/experience-as-control.md) te gebruiken of u kunt de Willekeurige ervaringsoptie gebruiken.

## Wanneer moet u [!UICONTROL Auto-Target] boven Automated Personalization kiezen? {#section_BBC4871C87944DD7A8B925811A30C633}

Er zijn verschillende scenario&#39;s waarin u [!UICONTROL Auto-Target] liever boven [!UICONTROL Automated Personalization] gebruikt:

* Als u de hele ervaring wilt definiëren in plaats van afzonderlijke aanbiedingen die automatisch worden gecombineerd om een ervaring te vormen.
* Als u de volledige reeks eigenschappen van Visual Experience Composer (VEC) wilt gebruiken die niet door [!UICONTROL Auto Personalization] worden gesteund: de redacteur van de douanecode, veelvoudige ervaringspubliek, en meer.
* Als u structurele wijzigingen in uw pagina wilt aanbrengen in verschillende ervaringen. Als u bijvoorbeeld elementen op uw startpagina opnieuw wilt rangschikken, is [!UICONTROL Auto-Target] geschikter voor gebruik dan Automated Personalization.

## Wat heeft [!UICONTROL Auto-Target] gemeen met Automated Personalization? {#section_2A601F482F9A44E38D4B694668711319}

**Het algoritme optimaliseert voor een gunstig resultaat voor elk bezoek.**

* Het algoritme voorspelt de neiging van een bezoeker voor omzetting (of geschatte opbrengst van omzetting) om de beste ervaring te dienen.
* Een bezoeker komt in aanmerking voor een nieuwe ervaring aan het einde van een bestaande sessie (tenzij de bezoeker deel uitmaakt van de controlegroep, in welk geval de ervaring die de bezoeker tijdens het eerste bezoek heeft opgedaan dezelfde blijft voor volgende bezoeken).
* Binnen een sessie verandert de voorspelling niet om de visuele consistentie te behouden.

**Het algoritme wordt aangepast aan wijzigingen in het gedrag van de bezoeker.**

* De multi-armbandit zorgt ervoor dat het model altijd een klein fractie verkeer &quot;uitgeeft&quot;om door het leven van het activiteit leren te blijven leren en overexploitatie van eerder geleerde tendensen te verhinderen.
* De onderliggende modellen worden elke 24 uur opnieuw samengesteld met behulp van de meest recente gedragsgegevens van de bezoeker, zodat Target altijd misbruik maakt van de veranderende voorkeuren van de bezoeker.
* Als het algoritme het winnen van ervaringen voor individuen niet kan bepalen, schakelt het automatisch aan het tonen van de algemene best-presterende ervaring terwijl nog steeds het zoeken naar gepersonaliseerde winnaars blijft. De best presterende ervaring wordt gevonden gebruikend [Thompson bemonstering](https://en.wikipedia.org/wiki/Thompson_sampling).

**Het algoritme optimaliseert voortdurend voor één enkel doel metrisch.**

* Deze metrische waarde zou op omzettingsbasis of op opbrengst-gebaseerd (meer bepaald Inkomsten per Bezoek) kunnen zijn.

**Het doel verzamelt automatisch informatie over bezoekers om de verpersoonlijkingsmodellen te bouwen.**

* Zie [Automated Personalization Data Collection](/help/c-activities/t-automated-personalization/ap-data.md) voor meer informatie over de parameters die in [!UICONTROL Auto-Target] en Automated Personalization worden gebruikt.

**Het doel gebruikt automatisch alle Experience Cloud gedeelde publiek om de verpersoonlijkingsmodellen te bouwen.**

* U hoeft niets specifiek te doen om publiek aan het model toe te voegen. Voor informatie over het gebruiken van Experience Cloud Soorten publiek met Doel, zie [Experience Cloud Soorten publiek](/help/c-integrating-target-with-mac/mmp.md)

**Marketers kunnen offlinegegevens, proxyscores of andere aangepaste gegevens uploaden om personalisatiemodellen samen te stellen.**

* Meer informatie over [gegevens uploaden voor Auto-Target en Automated Personalization](/help/c-activities/t-automated-personalization/uploading-data-for-the-target-personalization-algorithms.md).

## Hoe verschilt [!UICONTROL Auto-Target] van Automated Personalization? {#section_BA4D83BE40F14A96BE7CBC7C7CF2A8FB}

**[!UICONTROL Auto-Target]vereist vaak minder verkeer dan Automated Personalization voor een gepersonaliseerd model om te bouwen.**

Hoewel de hoeveelheid verkeer *per ervaring* vereist voor [!UICONTROL Auto-Target] of [!UICONTROL Auto Personalization] modellen om te bouwen het zelfde zijn, zijn er gewoonlijk meer ervaringen in een activiteit van Automated Personalization dan een [!UICONTROL Auto-Target] activiteit. Bijvoorbeeld, als u een [!UICONTROL Auto Personalization] activiteit had waar u twee aanbiedingen per plaats met twee plaatsen hebt gecreeerd, zouden er vier (2 = 4) totale ervaringen inbegrepen in de activiteit (zonder uitsluitingen) zijn. Met [!UICONTROL Auto-Target] kunt u ervaring 1 zodanig instellen dat aanbieding 1 op locatie 1 wordt opgenomen en aanbieding 2 op locatie 2, en ervaring 2 gebruiken om aanbieding 1 op locatie 1 op te nemen en aanbieding 2 op locatie 2. Omdat u met [!UICONTROL Auto-Target] meerdere wijzigingen binnen één ervaring kunt uitvoeren, kunt u het aantal ervaringen in uw activiteit verminderen.

Voor [!UICONTROL Auto-Target], kunnen de eenvoudige regels van duim worden gebruikt om verkeersvereisten te begrijpen:

* **Wanneer de Omzetting uw succes metrisch is:** 1.000 bezoeken en minstens 50 omzettingen per dag per ervaring, en daarnaast moet de activiteit minstens 7.000 bezoeken en 350 omzettingen hebben.
* **Wanneer de Opbrengst per Bezoek uw succesmetrisch is:** 1.000 bezoeken en minstens 50 omzettingen per dag per ervaring, en daarnaast moet de activiteit minstens 1.000 omzettingen per ervaring hebben. RPV vereist gewoonlijk meer gegevens om modellen samen te stellen vanwege de hogere gegevensvariantie die gewoonlijk bestaat in de opbrengsten van bezoeken in vergelijking met de omrekeningskoers.

**[!UICONTROL Auto-Target]heeft volledige instellingsfunctionaliteit.**

* Omdat [!UICONTROL Auto-Target] in het A/B activiteitenwerkschema wordt ingebed, [!UICONTROL Auto-Target] van de rijkere en volwaardige Composer van de Visuele Ervaring (VEC) profiteert. U kunt ook gebruikmaken van [QA-koppelingen](/help/c-activities/c-activity-qa/activity-qa.md) met [!UICONTROL Auto-Target].

**[!UICONTROL Auto-Target]biedt een uitgebreid onlinetestframework.**

* De multiarmbandit maakt deel uit van een groter online testkader dat onze data-wetenschappers en onderzoekers in staat stelt de voordelen van hun voortdurende verbeteringen in de reële omstandigheden te begrijpen.
* In de toekomst zullen we met deze testbank ons computerleerplatform kunnen openen voor onze klanten met data-savvy, zodat ze hun eigen modellen kunnen introduceren om de modellen van Target te versterken.

## Rapportage en [!UICONTROL Auto-Target] {#section_42EE7F5E65E84F89A872FE9921917F76}

Zie [Samenvattingsrapport voor automatisch doel](/help/c-reports/auto-target-summary-report.md) in de sectie [Rapporten](/help/c-reports/reports.md) voor meer informatie.

## Trainingsvideo: Werken met Auto-Target-activiteiten ![Overzicht badge](/help/assets/overview.png)

In deze video wordt uitgelegd hoe u een [!UICONTROL Auto-Target] A/B-activiteit instelt.

Nadat u deze training hebt voltooid, kunt u het volgende doen:

* [!UICONTROL Auto-Target] testen definiëren
* [!UICONTROL Auto-Target] vergelijken met Automated Personalization
* [!UICONTROL Auto-Target]-activiteiten maken

>[!VIDEO](https://video.tv.adobe.com/v/18558)
