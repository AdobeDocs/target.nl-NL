---
keywords: autotarget;het richten;verkeerstoewijzing;vaak gestelde vragen;faq;het oplossen van problemen;het oplossen van problemen
description: Leer hoe een [!UICONTROL Auto-Target] -activiteit de meest op maat gemaakte ervaring voor elke bezoeker biedt op basis van klantprofielen en het gedrag van vergelijkbare bezoekers.
title: Wat is een [!UICONTROL Auto-Target] activiteit?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=nl-NL#premium newtab=true" tooltip="Kijk wat er in Target Premium is opgenomen."
feature: Auto-Target
exl-id: 59ca30dc-45a0-4129-b832-84e1132d3b69
source-git-commit: 32a91a41cd182d3a55ded7dea8c1c6ea6f46aa71
workflow-type: tm+mt
source-wordcount: '1828'
ht-degree: 0%

---

# [!UICONTROL Auto-Target] overzicht

[!UICONTROL Auto-Target] -activiteiten in [!DNL Adobe Target] maken gebruik van geavanceerd leren van machines om uit meerdere, krachtigere, door de markt gedefinieerde ervaringen te kiezen voor het aanpassen van inhoud en het omzetten van stations. [!UICONTROL Auto-Target] biedt elke bezoeker de meest op maat gemaakte ervaring op basis van het individuele klantprofiel en het gedrag van eerdere bezoekers met vergelijkbare profielen.

>[!NOTE]
>
>* [!UICONTROL Auto-Target] is beschikbaar als onderdeel van de [!DNL Target Premium] -oplossing. Deze functie is niet beschikbaar in [!DNL Target Standard] zonder een [!DNL Target Premium] -licentie. Voor meer informatie over de geavanceerde eigenschappen verstrekt deze vergunning, zie [&#x200B; Target Premium &#x200B;](/help/main/c-intro/intro.md).
>
>* [!UICONTROL Analytics for Target] (A4T) ondersteunt [!UICONTROL Auto-Target] -activiteiten. Voor meer informatie, zie [&#x200B; steun A4T voor auto-Wijs en auto-Doel activiteiten &#x200B;](/help/main/c-integrating-target-with-mac/a4t/a4t-at-aa.md) toe.

## Real-world succesverhaal met Auto-Target {#success}

Een grote kleding die retailer onlangs gebruikte, gebruikte een [!UICONTROL Auto-Target] activiteit met tien op productcategorieën gebaseerde ervaringen (plus gerandomiseerde controle) om de juiste inhoud aan elke bezoeker te leveren. &quot;[!UICONTROL Add to Cart]&quot; is gekozen als primaire optimalisatiemetrische waarde. De beoogde ervaringen liepen gemiddeld op met 29,09%. Nadat de [!UICONTROL Auto-Target] -modellen waren gemaakt, werd de activiteit ingesteld op 90% persoonlijke ervaringen.

In slechts tien dagen werd meer dan $1.700.000 in lift bereikt.

Lees verder om te leren hoe u [!UICONTROL Auto-Target] kunt gebruiken om de lift en de omzet voor uw organisatie te verhogen.

## Overzicht {#section_972257739A2648AFA7E7556B693079C9}

Terwijl [&#x200B; creërend een activiteit A/B &#x200B;](/help/main/c-activities/t-test-ab/t-test-create-ab/test-create-ab.md) gebruikend het driestappe geleide werkschema, kies de **[!UICONTROL Auto-Target for personalized experiences]** optie op de **[!UICONTROL Targeting]** pagina (stap 2).

![&#x200B; montages van de Methode van de Toewijzing van het Verkeer &#x200B;](/help/main/c-activities/automated-traffic-allocation/assets/auto-target.png)

Met de optie [!UICONTROL Auto-Target] in de activiteitsstroom A/B kunt u automatisch leren aanpassen op basis van een aantal ervaringen die met behulp van een marketer zijn gedefinieerd. [!UICONTROL Auto-Target] is ontworpen om maximale optimalisatie te bieden in vergelijking met traditionele A/B-tests of [!UICONTROL Auto Allocate] door te bepalen welke ervaring voor elke bezoeker moet worden weergegeven. In tegenstelling tot een A/B-activiteit waarbij het doel is één winnaar te vinden, bepaalt [!UICONTROL Auto-Target] automatisch de beste ervaring voor een bepaalde bezoeker. De beste ervaring is gebaseerd op het profiel van de bezoeker en andere contextafhankelijke informatie voor een zeer persoonlijke ervaring.

Vergelijkbaar met [!UICONTROL Automated Personalization], [!UICONTROL Auto-Target] gebruikt a [&#x200B; Willekeurig Bosalgoritme &#x200B;](/help/main/c-activities/t-automated-personalization/algo-random-forest.md), een belangrijke methode van het de materiaalensemble van gegevenswetenschap, om de beste ervaring te bepalen om aan een bezoeker te tonen. Omdat [!UICONTROL Auto-Target] zich kan aanpassen aan wijzigingen in het gedrag van de bezoeker, kan het permanent worden uitgevoerd om een lift te leveren. Deze methode wordt soms ook wel de &quot;always-on&quot;-modus genoemd.

In tegenstelling tot een activiteit A/B waarin de ervaringstoewijzing voor een bepaalde bezoeker kleverig is, optimaliseert [!UICONTROL Auto-Target] het gespecificeerde bedrijfsdoel over elk bezoek. Net als in [!UICONTROL Auto Personalization], [!UICONTROL Auto-Target], door gebrek, reserveert een deel van het verkeer van de activiteit als controlegroep om lift te meten. Bezoekers in de controlegroep krijgen een willekeurige ervaring in de activiteit.

## Overwegingen

Houd rekening met het volgende als u [!UICONTROL Auto-Target] gebruikt:

* U kunt niet van [!UICONTROL Auto-Target] naar [!UICONTROL Automated Personalization] gaan en omgekeerd.
* U kunt niet schakelen van [!UICONTROL Manual] verkeerstoewijzing (traditioneel [!UICONTROL A/B Test] ) naar [!UICONTROL Auto-Target] en de tegenovergestelde manier nadat een activiteit als concept is opgeslagen.
* Één model wordt gebouwd om de prestaties van de gepersonaliseerde strategie tegenover willekeurig gediend verkeer tegenover het verzenden van al verkeer naar het algemeen het winnen ervaring te identificeren. In dit model worden alleen resultaten en omzettingen in de standaardomgeving bekeken.

  Het verkeer van een tweede reeks modellen wordt gebouwd voor elke modelleringsgroep (AP) of ervaring (AT). Voor elk van deze modellen worden hits en conversies in alle omgevingen in overweging genomen.

  De verzoeken worden gediend met het zelfde model, ongeacht milieu. De pluraliteit van het verkeer moet echter afkomstig zijn uit de standaardomgeving om ervoor te zorgen dat de geïdentificeerde overkoepelende ervaring consistent is met het gedrag in de praktijk.

* Gebruik minimaal twee ervaringen.

## Terminologie {#section_A309B7E0B258467789A5CACDC1D923F3}

De volgende termen zijn handig wanneer u [!UICONTROL Auto-Target] bespreekt:

| Term | Definitie |
|---|---|
| [&#x200B; Meervoudig-gewapende bandit &#x200B;](https://en.wikipedia.org/wiki/Multi-armed_bandit){target=_blank} | Een veelbewapende bandibenadering voor optimalisering brengt een evenwicht tot stand tussen verkennend leren en het benutten van dat leren. |
| [&#x200B; Willekeurig bos &#x200B;](/help/main/c-activities/t-automated-personalization/algo-random-forest.md) | Random Forest is een toonaangevende aanpak voor machinaal leren. Op het gebied van gegevenswetenschappen is het een ensemble classificatie, of regressiemethode, die werkt door veel beslissingsbomen te bouwen op basis van bezoekers en bezoekkenmerken. Binnen [!DNL Target] wordt Random Forest gebruikt om te bepalen welke ervaring naar verwachting de hoogste kans op conversie (of hoogste inkomsten per bezoek) voor elke specifieke bezoeker zal hebben. |
| [&#x200B; Thompson Steekproef &#x200B;](https://en.wikipedia.org/wiki/Thompson_sampling){target=_blank} | Het doel van Thompson Sampling is te bepalen welke ervaring de beste algemene (niet-gepersonaliseerde) ervaring is, terwijl de &#39;kosten&#39; van het vinden van die ervaring tot een minimum worden beperkt. Thompson-steekproeven kiezen altijd een winnaar, zelfs als er geen statistisch verschil tussen twee ervaringen is. |

## Hoe [!UICONTROL Auto-Target] werkt {#section_77240E2DEB7D4CD89F52BE0A85E20136}

Meer informatie over de onderliggende gegevens en algoritmen [!UICONTROL Auto-Target] en [!UICONTROL Automated Personalization] vindt u op de onderstaande koppelingen:

| Term | Details |
|--- |--- |
| [&#x200B; Willekeurig Bos Algorithm &#x200B;](/help/main/c-activities/t-automated-personalization/algo-random-forest.md) | Het belangrijkste verpersoonlijkingsalgoritme van [!DNL Target] dat zowel in [!UICONTROL Auto-Target] als [!UICONTROL Automated Personalization] wordt gebruikt is Random Forest. Met methoden zoals Random Forest kunt u meerdere leeralgoritmen gebruiken om betere voorspellende prestaties te verkrijgen dan met elk van de deelleeralgoritmen. Het algoritme Random Forest in de [!UICONTROL Automated Personalization] - en [!UICONTROL Auto-Target] -activiteiten is een classificatie- of regressiemethode die werkt door tijdens de training een groot aantal beslissingsbomen te maken. |
| [&#x200B; uploadend Gegevens voor  [!DNL Target] de Algoritmen van Personalization &#x200B;](/help/main/c-activities/t-automated-personalization/algo-random-forest.md) | Er zijn verschillende manieren om gegevens in te voeren voor [!UICONTROL Auto-Target] - en [!UICONTROL Automated Personalization] -modellen. |
| [&#x200B; Inzameling van Gegevens voor  [!DNL Target] de Algoritmen van Personalization &#x200B;](/help/main/c-activities/t-automated-personalization/ap-data.md) | De personalisatiealgoritmen van [!DNL Target] verzamelen automatisch verschillende gegevens. |

## Verkeerstoewijzing bepalen {#section_AB3656F71D2D4C67A55A24B38092958F}

Afhankelijk van het doel van uw activiteit, zou u een verschillende verkeerstoewijzing tussen controle en gepersonaliseerde ervaringen kunnen kiezen. De beste praktijken moeten dit doel bepalen alvorens u uw activiteit Levend maakt.

In de vervolgkeuzelijst [!UICONTROL Custom Allocation] kunt u uit de volgende opties kiezen:

* [!UICONTROL Evaluate Personalization Algorithm (50/50)]
* [!UICONTROL Maximize Personalization Traffic (90/10)]
* [!UICONTROL Custom Allocation]

![&#x200B; drop-down lijst van het Doel van de Toewijzing &#x200B;](/help/main/c-activities/assets/split-new-ui.png)

In de volgende tabel worden de drie opties beschreven:

| Activiteitsdoelstelling | Voorgestelde verkeerstoewijzing | Aftrekposten |
|--- |--- |--- |
| **[!UICONTROL Evaluate Personalization Algorithm (50/50)]**: Als het uw doel is het algoritme te testen, gebruikt u een opsplitsing van bezoekers van 50/50 procent tussen het besturingselement en het doelalgoritme. Deze splitsing geeft de meest nauwkeurige schatting van de lift. Voorgesteld voor gebruik met &quot;willekeurige ervaringen&quot; als controle. | 50% controle / 50% persoonlijke ervaring gesplitst | <ul><li>Maximaliseert nauwkeurigheid van lift tussen controle en gepersonaliseerd</li><li>Relatief minder bezoekers hebben een persoonlijke ervaring</li></ul> |
| **[!UICONTROL Maximize Personalization Traffic (90/10)]**: Als uw doel het maken van een activiteit &#39;always on&#39; is, plaatst u 10% van de bezoekers in het besturingselement om ervoor te zorgen dat er voldoende gegevens zijn voor de algoritmen om te blijven leren in de loop van de tijd. De handel hier is dat in ruil voor het personaliseren van een groter deel van je verkeer, je minder nauwkeurigheid hebt in wat de exacte lift is. Wat u ook wilt, dit is de aanbevolen verkeerssplitsing wanneer u een specifieke ervaring als besturingselement gebruikt. | De beste manier is om een Controle van 10% - 30% / 70% - 90% Persoonlijke Ervaring te gebruiken verdeeld | <ul><li>Maximaliseert het aantal bezoekers dat een persoonlijke ervaring heeft</li><li>Maximaliseert lift</li><li>Minder nauwkeurigheid wat betreft wat de lift voor de activiteit is</li></ul> |
| **Aangepaste Toewijzing** | Splits het percentage handmatig naar wens. | <ul><li>U bereikt mogelijk niet de gewenste resultaten. Als u twijfelt, volgt u de suggesties voor een van de voorgaande opties</li></ul> |

Als u het percentage [!UICONTROL Control] wilt aanpassen, klikt u op [!UICONTROL Experiences] in het deelvenster [!UICONTROL Traffic Allocation] en past u vervolgens de percentages naar wens aan. U kunt de controlegroep niet tot minder dan 10% verminderen.

U kunt [&#x200B; een specifieke ervaring selecteren om als controle &#x200B;](/help/main/c-activities/t-automated-personalization/experience-as-control.md) te gebruiken of u kunt de Willekeurige ervaringsoptie gebruiken.

## Wanneer moet u [!UICONTROL Auto-Target] over [!UICONTROL Automated Personalization] kiezen? {#section_BBC4871C87944DD7A8B925811A30C633}

Er zijn verschillende scenario&#39;s waarin u [!UICONTROL Auto-Target] over [!UICONTROL Automated Personalization] liever gebruikt:

* Als u de hele ervaring wilt definiëren in plaats van afzonderlijke aanbiedingen die automatisch worden gecombineerd om een ervaring te vormen.
* Als u de volledige set [!UICONTROL Visual Experience Composer] (VEC)-functies wilt gebruiken die niet door [!UICONTROL Auto Personalization] worden ondersteund: de aangepaste code-editor, meerdere ervaringssoorten en meer.
* Als u structurele wijzigingen in uw pagina wilt aanbrengen in verschillende ervaringen. Als u bijvoorbeeld de elementen op de startpagina opnieuw wilt rangschikken, is [!UICONTROL Auto-Target] geschikter voor gebruik dan [!UICONTROL Automated Personalization] .

## Wat heeft [!UICONTROL Auto-Target] gemeen met [!UICONTROL Automated Personalization] ? {#section_2A601F482F9A44E38D4B694668711319}

### Het algoritme optimaliseert voor een gunstig resultaat voor elk bezoek.

* Het algoritme voorspelt de neiging van een bezoeker voor omzetting (of geschatte opbrengst van omzetting) om de beste ervaring te dienen.
* Een bezoeker komt in aanmerking voor een nieuwe ervaring aan het einde van een bestaande sessie (tenzij de bezoeker deel uitmaakt van de controlegroep, in welk geval de ervaring die de bezoeker tijdens het eerste bezoek heeft opgedaan dezelfde blijft voor volgende bezoeken).
* Binnen een sessie verandert de voorspelling niet om de visuele consistentie te behouden.

### Het algoritme wordt aangepast aan wijzigingen in het gedrag van de bezoeker.

* De multi-armbandit zorgt ervoor dat het model altijd een klein fractie verkeer &quot;uitgeeft&quot;om door het leven van het activiteit leren te blijven leren en overexploitatie van eerder geleerde tendensen te verhinderen.
* De onderliggende modellen worden elke 24 uur opnieuw samengesteld met behulp van de meest recente gedragsgegevens van de bezoeker, zodat [!DNL Target] altijd misbruik maakt van het wijzigen van de voorkeuren van de bezoeker.
* Als het algoritme het winnen van ervaringen voor individuen niet kan bepalen, schakelt het automatisch aan het tonen van de algemene best-presterende ervaring terwijl nog steeds het zoeken naar gepersonaliseerde winnaars blijft. De best-presterende ervaring wordt gevonden gebruikend [&#x200B; steekproef van Thompson &#x200B;](https://en.wikipedia.org/wiki/Thompson_sampling).

### Het algoritme optimaliseert voortdurend voor één enkel doel metrisch.

* Deze metrische waarde kan gebaseerd zijn op conversie of op inkomsten (meer bepaald [!UICONTROL Revenue per Visit] ).

### [!DNL Target] verzamelt automatisch informatie over bezoekers om de verpersoonlijkingsmodellen samen te stellen.

* Voor meer informatie over de parameters die in [!UICONTROL Auto-Target] en [!UICONTROL Automated Personalization] worden gebruikt, zie [&#x200B; de Inzameling van Gegevens van Automated Personalization &#x200B;](/help/main/c-activities/t-automated-personalization/ap-data.md).

### [!DNL Target] gebruikt automatisch alle [!DNL Adobe Experience Cloud] gedeelde soorten publiek om de aanpassingsmodellen te maken.

* U hoeft niets specifiek te doen om publiek aan het model toe te voegen. Voor informatie over het gebruiken van [!DNL Experience Cloud Audiences] met [!DNL Target], zie [&#x200B; publiek van Experience Cloud &#x200B;](/help/main/c-integrating-target-with-mac/mmp.md).

### Marketers kunnen offlinegegevens, proxyscores of andere aangepaste gegevens uploaden om personalisatiemodellen samen te stellen.

* Meer informatie over [&#x200B; het uploaden van gegevens voor [!UICONTROL Auto-Target] en [!UICONTROL Automated Personalization]](/help/main/c-activities/t-automated-personalization/uploading-data-for-the-target-personalization-algorithms.md).

## Hoe verschilt [!UICONTROL Auto-Target] van [!UICONTROL Automated Personalization] ? {#section_BA4D83BE40F14A96BE7CBC7C7CF2A8FB}

### [!UICONTROL Auto-Target] vereist vaak minder verkeer dan [!UICONTROL Automated Personalization] voor een gepersonaliseerd model om te bouwen.

Hoewel de hoeveelheid verkeer *per ervaring* wordt vereist voor [!UICONTROL Auto-Target] of [!UICONTROL Auto Personalization] modellen om het zelfde te bouwen, zijn er gewoonlijk meer ervaringen in een [!UICONTROL Automated Personalization] activiteit dan een [!UICONTROL Auto-Target] activiteit.

Als u bijvoorbeeld een [!UICONTROL Auto Personalization] -activiteit had waarbij u twee aanbiedingen per locatie met twee locaties hebt gemaakt, zijn er vier (2 = 4) ervaringen in totaal opgenomen in de activiteit (zonder uitsluitingen). Met [!UICONTROL Auto-Target] kunt u ervaring 1 zodanig instellen dat aanbieding 1 op locatie 1 wordt opgenomen en aanbieding 2 op locatie 2. Met ervaring 2 kunt u aanbieding 1 op locatie 1 opnemen en aanbieding 2 op locatie 2. Omdat u in [!UICONTROL Auto-Target] meerdere wijzigingen binnen één ervaring kunt uitvoeren, kunt u het aantal ervaringen in uw activiteit verminderen.

Voor [!UICONTROL Auto-Target], kunnen de eenvoudige regels van duim worden gebruikt om verkeersvereisten te begrijpen:

* **wanneer [!UICONTROL Conversion] uw succes metrisch is:** 1.000 bezoeken en minstens 50 omzettingen per dag per ervaring, en daarnaast moet de activiteit minstens 7.000 bezoeken en 350 omzettingen hebben.
* **wanneer [!UICONTROL Revenue per Visit] uw succes metrisch is:** 1.000 bezoeken en minstens 50 omzettingen per dag per ervaring, en daarnaast moet de activiteit minstens 1.000 omzettingen per ervaring hebben. RPV vereist gewoonlijk meer gegevens om modellen samen te stellen vanwege de hogere gegevensvariantie die gewoonlijk bestaat in de opbrengsten van bezoeken in vergelijking met de omrekeningskoers.

### [!UICONTROL Auto-Target] heeft volledige instellingsfunctionaliteit.

* Omdat [!UICONTROL Auto-Target] is ingesloten in de A/B-activiteitsworkflow, profiteert [!UICONTROL Auto-Target] van de meer volwassen en volledige [!UICONTROL Visual Experience Composer] (VEC). U kunt [&#x200B; verbindingen QA &#x200B;](/help/main/c-activities/c-activity-qa/activity-qa.md) met [!UICONTROL Auto-Target] ook gebruiken.

### [!UICONTROL Auto-Target] biedt een uitgebreid onlinetestframework.

* De bandit met meerdere armen maakt deel uit van een groter online testkader dat [!DNL Adobe] data-wetenschappers en onderzoekers in staat stelt de voordelen van hun voortdurende verbeteringen in de reële omstandigheden te begrijpen.
* In de toekomst kunnen we met deze testbank het platform voor machinaal leren van [!DNL Adobe] openen voor klanten met gegevensbewuste functies, zodat ze hun eigen modellen kunnen gebruiken om de [!DNL Target] -modellen te verfraaien.

## Rapportage en [!UICONTROL Auto-Target] {#section_42EE7F5E65E84F89A872FE9921917F76}

Voor meer informatie, zie [&#x200B; Meldend en auto-Doel &#x200B;](/help/main/c-activities/auto-target/reporting-and-auto-target.md).
