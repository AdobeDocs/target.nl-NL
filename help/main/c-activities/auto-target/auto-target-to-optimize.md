---
keywords: autotarget;het richten;verkeerstoewijzing;vraag vaak;faq;het oplossen van problemen;het oplossen van problemen
description: Leer hoe een activiteit AutoTarget in [!DNL Target] biedt iedere bezoeker de meest toegesneden ervaring op basis van klantprofielen en het gedrag van vergelijkbare bezoekers.
title: Wat is een automatisch doelactiviteit?
feature: Auto-Target
exl-id: 59ca30dc-45a0-4129-b832-84e1132d3b69
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '1926'
ht-degree: 0%

---

# ![PREMIUM](/help/main/assets/premium.png) Overzicht van automatisch doel

[!UICONTROL Auto-Target] activiteiten in [!DNL Adobe Target] Maak gebruik van geavanceerd computerleren om te kiezen uit verschillende, door de markator gedefinieerde ervaringen om de inhoud en schijfconversies aan te passen. Auto-Target biedt elke bezoeker de meest op maat gemaakte ervaring op basis van het individuele klantprofiel en het gedrag van eerdere bezoekers met vergelijkbare profielen.

>[!NOTE]
>
>[!UICONTROL Auto-Target] is beschikbaar als onderdeel van de [!DNL Target Premium] oplossing. Deze functie is niet beschikbaar in [!DNL Target Standard] zonder [!DNL Target Premium] licentie. Voor meer informatie over de geavanceerde functies die deze licentie biedt, raadpleegt u [Doelpremie](/help/main/c-intro/intro.md).
>
>[!UICONTROL Analytics for Target] (A4T)-ondersteuning [!UICONTROL Auto-Target] activiteiten. Zie voor meer informatie [A4T-ondersteuning voor activiteiten voor automatisch toewijzen en automatisch richten](/help/main/c-integrating-target-with-mac/a4t/a4t-at-aa.md).

## Real-world succesverhaal met Auto-Target {#success}

Een grote kledinghandelaar heeft onlangs een [!UICONTROL Auto-Target] activiteit met tien op productcategorieën gebaseerde ervaringen (plus gerandomiseerde controle) om de juiste inhoud aan elke bezoeker te leveren. &quot;[!UICONTROL Add to Cart]&quot; is gekozen als de primaire optimalisatiemethode. De beoogde ervaringen liepen gemiddeld op met 29,09%. Nadat u het [!UICONTROL Auto-Target] de activiteit werd op 90 % persoonlijke ervaringen ingesteld .

In slechts tien dagen werd meer dan $1.700.000 in lift bereikt.

Lees verder voor meer informatie over het gebruik [!UICONTROL Auto-Target] om de lift en de inkomsten voor uw organisatie te verhogen.

## Overzicht {#section_972257739A2648AFA7E7556B693079C9}

while [een A/B-activiteit maken met behulp van de driestappe geleide workflow](/help/main/c-activities/t-test-ab/t-test-create-ab/test-create-ab.md), kunt u ervoor kiezen om verkeer toe te wijzen met de [!UICONTROL Auto-Target For Personalized Experiences] optie:

![Automatisch richten voor persoonlijke ervaringen, optie](/help/main/c-activities/assets/auto-target-ui-new.png)

De [!UICONTROL Auto-Target] kunt u in de activiteitsstroom van A/B machine-leren gebruiken om zich te personaliseren gebaseerd op een reeks van tellers-bepaalde ervaringen in één klik. [!UICONTROL Auto-Target] is ontworpen voor maximale optimalisatie in vergelijking met traditionele A/B-tests of Automatische toewijzing, door te bepalen welke ervaring voor elke bezoeker moet worden weergegeven. In tegenstelling tot een A/B-activiteit waarbij het doel is één enkele winnaar te vinden, [!UICONTROL Auto-Target] bepaalt automatisch de beste ervaring voor een bepaalde bezoeker (op basis van zijn of haar profiel en andere contextuele informatie) om een hoogst gepersonaliseerde ervaring te leveren.

Evenals Automated Personalization [!UICONTROL Auto-Target] gebruikt een Random Forest-algoritme, een toonaangevende methode voor het samenstellen van gegevenswetenschappen, om de beste ervaring te bepalen die aan een bezoeker moet worden getoond. Omdat [!UICONTROL Auto-Target] Deze functie kan worden aangepast aan wijzigingen in het gedrag van de bezoeker en kan permanent worden uitgevoerd om lift te bieden. Dit wordt soms ook wel de &quot;always-on&quot;-modus genoemd.

In tegenstelling tot een A/B-activiteit waarbij de ervaringstoewijzing voor een bepaalde bezoeker kleverig is, [!UICONTROL Auto-Target] optimaliseert het gespecificeerde bedrijfsdoel over elk bezoek. Zoals in [!UICONTROL Auto Personalization], [!UICONTROL Auto-Target], door gebrek, reserveert een deel van het verkeer van de activiteit als controlegroep om lift te meten. Bezoekers in de controlegroep krijgen een willekeurige ervaring in de activiteit.

## Overwegingen

Er zijn enkele belangrijke overwegingen waarmee u rekening moet houden wanneer u [!UICONTROL Auto-Target]:

* U kunt een bepaalde activiteit niet van [!UICONTROL Auto-Target] naar Automated Personalization en omgekeerd.
* U kunt niet van Handmatige verkeerstoewijzing (traditionele A/B Test) schakelen aan [!UICONTROL Auto-Target]en omgekeerd nadat een activiteit actief is.
* Één model wordt gebouwd om de prestaties van de gepersonaliseerde strategie tegenover willekeurig gediend verkeer tegenover het verzenden van al verkeer naar het algemene winnen ervaring te identificeren. In dit model worden alleen resultaten en omzettingen in de standaardomgeving bekeken.

   Het verkeer van een tweede reeks modellen wordt gebouwd voor elke modelleringsgroep (AP) of ervaring (AT). Voor elk van deze modellen worden hits en conversies in alle omgevingen in overweging genomen.

   De verzoeken worden gediend met het zelfde model, ongeacht milieu, maar de pluraliteit van verkeer zou van het standaardmilieu moeten komen om ervoor te zorgen dat de geïdentificeerde algemene het winnen ervaring met echt gedrag verenigbaar is.

* Gebruik minimaal twee ervaringen.

## Terminologie {#section_A309B7E0B258467789A5CACDC1D923F3}

De volgende termen zijn handig wanneer u discussieert over [!UICONTROL Auto-Target]:

| Term | Definitie |
|---|---|
| Meervoudig bewapende bandit | Een veelbewapende bandibenadering voor optimalisering brengt een evenwicht tot stand tussen verkennend leren en het benutten van dat leren. |
| Willekeurig bos | Random Forest is een toonaangevende aanpak voor machinaal leren. Op het gebied van gegevenswetenschappen is het een ensemble classificatie, of regressiemethode, die werkt door veel beslissingsbomen te bouwen op basis van bezoekers en bezoekkenmerken. Binnen Target wordt het Willekeurige bos gebruikt om te bepalen welke ervaring naar verwachting de hoogste waarschijnlijkheid van omzetting (of hoogste opbrengst per bezoek) voor elke specifieke bezoeker zal hebben. Voor meer informatie over Willekeurig bos in Doel, zie [Random Forest Algorithm](/help/main/c-activities/t-automated-personalization/algo-random-forest.md). |
| Thompson Sampling | Het doel van Thompson Sampling is te bepalen welke ervaring de beste algemene (niet-gepersonaliseerde) ervaring is, terwijl de &#39;kosten&#39; van het vinden van die ervaring tot een minimum worden beperkt. Thompson-steekproeven kiezen altijd een winnaar, zelfs als er geen statistisch verschil tussen twee ervaringen is. Zie voor meer informatie [Thompson Sampling](https://en.wikipedia.org/wiki/Thompson_sampling). |

## Hoe [!UICONTROL Auto-Target] Werken {#section_77240E2DEB7D4CD89F52BE0A85E20136}

Meer informatie over de onderliggende gegevens en algoritmen [!UICONTROL Auto-Target] en Automated Personalization op de onderstaande links:

| Term | Details |
|--- |--- |
| [Random Forest Algorithm](/help/main/c-activities/t-automated-personalization/algo-random-forest.md) | Hoofdpersonalisatiealgoritme van het doel dat in beide wordt gebruikt [!UICONTROL Auto-Target] en Automated Personalization is Random Forest. Met methoden als Random Forest kunt u meerdere leeralgoritmen gebruiken om betere voorspellende prestaties te verkrijgen dan met elk van de deelleeralgoritmen. Het Random Forest-algoritme in het Automated Personalization-systeem is een classificatiemethode, of regressiemethode, die werkt door een groot aantal beslissingsbomen te bouwen op het moment van training. |
| [Gegevens uploaden voor de Persoonlijke Algoritmen van het Doel](/help/main/c-activities/t-automated-personalization/algo-random-forest.md) | Er zijn verschillende manieren om gegevens in te voeren voor [!UICONTROL Auto-Target] en Automated Personalization-modellen. |
| [Gegevensverzameling voor personaliseringsalgoritmen van het Doel](/help/main/c-activities/t-automated-personalization/ap-data.md) | De personalisatiealgoritmen van het doel verzamelen automatisch diverse gegevens. |

## Verkeerstoewijzing bepalen {#section_AB3656F71D2D4C67A55A24B38092958F}

Afhankelijk van het doel van uw activiteit, zou u een verschillende verkeerstoewijzing tussen controle en gepersonaliseerde ervaringen kunnen kiezen. De beste praktijken moeten dit doel bepalen alvorens u uw activiteit Levend maakt.

De [!UICONTROL Custom Allocation] In de vervolgkeuzelijst kunt u de volgende opties kiezen:

* Beoordelen van algoritme voor personalisatie
* Personalisatieverkeer maximaliseren
* Aangepaste toewijzing

![Vervolgkeuzelijst Toewijzingsdoel](/help/main/c-activities/assets/split-new.png)

| Activiteitsdoelstelling | Voorgestelde verkeerstoewijzing | Aftrekposten |
|--- |--- |--- |
| **Beoordelen van Persoonlijkheidsalgoritme (50/50)**: Als uw doel het algoritme is te testen, gebruik een 50/50 percenten verdeling van bezoekers tussen de controle en het gerichte algoritme. Deze splitsing geeft de meest nauwkeurige schatting van de lift. Voorgesteld voor gebruik met &quot;willekeurige ervaringen&quot; als controle. | 50% controle / 50% persoonlijke ervaring gesplitst | <ul><li>Maximaliseert nauwkeurigheid van lift tussen controle en gepersonaliseerd</li><li>Relatief minder bezoekers hebben een persoonlijke ervaring</li></ul> |
| **Personaliseringsverkeer maximaliseren (90/10)**: Als uw doel het creëren van &quot;altijd op&quot;activiteit is, zet 10% van de bezoekers in de controle om ervoor te zorgen dat er genoeg gegevens voor de algoritmen zijn om in tijd te blijven leren. De handel hier is dat in ruil voor het personaliseren van een groter deel van je verkeer, je minder nauwkeurigheid hebt in wat de exacte lift is. Wat u ook wilt, dit is de aanbevolen verkeerssplitsing wanneer u een specifieke ervaring als besturingselement gebruikt. | De beste manier is om een Controle van 10% - 30% / 70% - 90% Persoonlijke Ervaring te gebruiken verdeeld | <ul><li>Maximaliseert het aantal bezoekers met een persoonlijke ervaring</li><li>Maximaliseert lift</li><li>Minder nauwkeurigheid wat betreft wat de lift voor de activiteit is</li></ul> |
| **Aangepaste toewijzing** | Splits het percentage handmatig naar wens. | <ul><li>U bereikt mogelijk niet de gewenste resultaten. Als u twijfelt, volgt u de suggesties voor een van de voorgaande opties</li></ul> |

Klik op de pictogrammen in de kolom Toewijzing om het percentage voor besturing aan te passen. U kunt de controlegroep niet tot minder dan 10% verminderen.

![Automatische doeltoewijzing wijzigen](/help/main/c-activities/assets/auto-target-control.png)

U kunt [een specifieke ervaring selecteren die u als besturingselement wilt gebruiken](/help/main/c-activities/t-automated-personalization/experience-as-control.md) of u kunt de optie Willekeurige ervaring gebruiken.

## Wanneer kiest u [!UICONTROL Auto-Target] over Automated Personalization? {#section_BBC4871C87944DD7A8B925811A30C633}

Er zijn verschillende scenario&#39;s waarin u wellicht liever zult gebruiken [!UICONTROL Auto-Target] over [!UICONTROL Automated Personalization]:

* Als u de hele ervaring wilt definiëren in plaats van afzonderlijke aanbiedingen die automatisch worden gecombineerd om een ervaring te vormen.
* Als u de volledige reeks eigenschappen van Visual Experience Composer (VEC) wilt gebruiken die niet door worden gesteund [!UICONTROL Auto Personalization]: de redacteur van de douanecode, veelvoudige ervaringspubliek, en meer.
* Als u structurele wijzigingen in uw pagina wilt aanbrengen in verschillende ervaringen. Als u bijvoorbeeld de elementen op uw homepage opnieuw wilt rangschikken, [!UICONTROL Auto-Target] is geschikter dan Automated Personalization.

## Wat doet [!UICONTROL Auto-Target] Hebben we hetzelfde met Automated Personalization? {#section_2A601F482F9A44E38D4B694668711319}

**Het algoritme optimaliseert voor een gunstig resultaat voor elk bezoek.**

* Het algoritme voorspelt de neiging van een bezoeker voor omzetting (of geschatte opbrengst van omzetting) om de beste ervaring te dienen.
* Een bezoeker komt in aanmerking voor een nieuwe ervaring aan het einde van een bestaande sessie (tenzij de bezoeker deel uitmaakt van de controlegroep, in welk geval de ervaring die de bezoeker tijdens het eerste bezoek heeft opgedaan dezelfde blijft voor volgende bezoeken).
* Binnen een sessie verandert de voorspelling niet om de visuele consistentie te behouden.

**Het algoritme wordt aangepast aan wijzigingen in het gedrag van de bezoeker.**

* De multi-armbandit zorgt ervoor dat het model altijd een klein fractie verkeer &quot;uitgeeft&quot;om door het leven van het activiteit leren te blijven leren en overexploitatie van eerder geleerde tendensen te verhinderen.
* De onderliggende modellen worden elke 24 uur opnieuw samengesteld met behulp van de meest recente gedragsgegevens van de bezoeker, zodat Target altijd misbruik maakt van de veranderende voorkeuren van de bezoeker.
* Als het algoritme het winnen van ervaringen voor individuen niet kan bepalen, schakelt het automatisch aan het tonen van de algemene best-presterende ervaring terwijl nog steeds het zoeken naar gepersonaliseerde winnaars blijft. De best presterende ervaring wordt gevonden gebruikend [Thompson sampling](https://en.wikipedia.org/wiki/Thompson_sampling).

**Het algoritme optimaliseert voortdurend voor één enkel doel metrisch.**

* Deze metrische waarde zou op omzettingsbasis of op opbrengst-gebaseerd (meer bepaald Inkomsten per Bezoek) kunnen zijn.

**Het doel verzamelt automatisch informatie over bezoekers om de verpersoonlijkingsmodellen te bouwen.**

* Voor meer informatie over de parameters die worden gebruikt in [!UICONTROL Auto-Target] en Automated Personalization, zie [Automated Personalization-gegevensverzameling](/help/main/c-activities/t-automated-personalization/ap-data.md).

**Het doel gebruikt automatisch alle Experience Cloud gedeelde publiek om de verpersoonlijkingsmodellen te bouwen.**

* U hoeft niets specifiek te doen om publiek aan het model toe te voegen. Voor informatie over het gebruiken van het Soorten publiek van Experience Cloud met Doel, zie [Experience Cloud publiek](/help/main/c-integrating-target-with-mac/mmp.md)

**Marketers kunnen offlinegegevens, proxyscores of andere aangepaste gegevens uploaden om personalisatiemodellen samen te stellen.**

* Meer informatie over [Gegevens uploaden voor AutoTarget en Automated Personalization](/help/main/c-activities/t-automated-personalization/uploading-data-for-the-target-personalization-algorithms.md).

## Hoe werkt [!UICONTROL Auto-Target] verschillen van Automated Personalization? {#section_BA4D83BE40F14A96BE7CBC7C7CF2A8FB}

**[!UICONTROL Auto-Target]vereist vaak minder verkeer dan Automated Personalization voor een gepersonaliseerd model om te bouwen.**

Hoewel de hoeveelheid verkeer *per ervaring* vereist voor [!UICONTROL Auto-Target] of [!UICONTROL Auto Personalization] modellen om te bouwen zijn het zelfde, zijn er gewoonlijk meer ervaringen in een activiteit van Automated Personalization dan een [!UICONTROL Auto-Target] activiteit. Als u bijvoorbeeld een [!UICONTROL Auto Personalization] activiteit waar u twee aanbiedingen per plaats met twee plaatsen hebt gecreeerd, zouden er vier (2 = 4) totale ervaringen inbegrepen in de activiteit (zonder uitsluitingen) zijn. Gebruiken [!UICONTROL Auto-Target], kunt u ervaring 1 instellen om aanbieding 1 op locatie 1 en aanbieding 2 op locatie 2 op te nemen, en ervaring 2 om aanbieding 1 op locatie 1 en aanbieding 2 op locatie 2 op te nemen. Omdat [!UICONTROL Auto-Target] kunt u ervoor kiezen om meerdere wijzigingen binnen één ervaring door te voeren, zodat u het aantal ervaringen in uw activiteit kunt verminderen.

Voor [!UICONTROL Auto-Target]Eenvoudige duimregels kunnen worden gebruikt om de verkeersvereisten te begrijpen:

* **Wanneer Conversion uw succes metrisch is:** 1.000 bezoeken en ten minste 50 conversies per dag per ervaring, en daarnaast moeten de activiteiten ten minste 7.000 bezoeken en 350 conversies hebben.
* **Wanneer de Opbrengst per Bezoek uw succesmetrisch is:** 1.000 bezoeken en ten minste 50 conversies per dag per ervaring, en daarnaast moet de activiteit ten minste 1.000 conversies per ervaring hebben. RPV vereist gewoonlijk meer gegevens om modellen samen te stellen vanwege de hogere gegevensvariantie die gewoonlijk bestaat in de opbrengsten van bezoeken in vergelijking met de omrekeningskoers.

**[!UICONTROL Auto-Target]heeft volledige instellingsfunctionaliteit.**

* Omdat [!UICONTROL Auto-Target] is ingebed in de A/B activiteitsworkflow, [!UICONTROL Auto-Target] de voordelen van de rijkere en volwaardige composer voor visuele ervaring (VEC). U kunt ook gebruikmaken van [QA-koppelingen](/help/main/c-activities/c-activity-qa/activity-qa.md) with [!UICONTROL Auto-Target].

**[!UICONTROL Auto-Target]biedt een uitgebreid onlinetestframework.**

* De multiarmbandit maakt deel uit van een groter online testkader dat onze data-wetenschappers en onderzoekers in staat stelt de voordelen van hun voortdurende verbeteringen in de reële omstandigheden te begrijpen.
* In de toekomst zullen we met deze testbank ons computerleerplatform kunnen openen voor onze klanten met data-savvy, zodat ze hun eigen modellen kunnen introduceren om de modellen van Target te versterken.

## Rapportage en [!UICONTROL Auto-Target] {#section_42EE7F5E65E84F89A872FE9921917F76}

Zie voor meer informatie [Samenvattingsrapport autom. doel](/help/main/c-reports/auto-target-summary-report.md) in de [Rapporten](/help/main/c-reports/reports.md) sectie.

## Trainingsvideo: Werken met Auto-Target ![Overzicht badge](/help/main/assets/overview.png)

In deze video wordt uitgelegd hoe u een [!UICONTROL Auto-Target] A/B-activiteit.

Nadat u deze training hebt voltooid, kunt u het volgende doen:

* Definiëren [!UICONTROL Auto-Target] testen
* Vergelijken en contrast [!UICONTROL Auto-Target] naar Automated Personalization
* Maken [!UICONTROL Auto-Target] activiteiten

>[!VIDEO](https://video.tv.adobe.com/v/18558)
