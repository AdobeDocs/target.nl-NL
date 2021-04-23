---
keywords: geautomatiseerde personalisatie;ap;publiek;ensemble;random forest;multi-gewapende bandit;thompson sampling;ml;machine leren
description: Leer hoe u Automated Personalization-activiteiten (AP) gebruikt in Adobe [!DNL Target] die gebruikmaken van geavanceerd leren van computers om verschillende aanbiedingsvariaties voor elke bezoeker op elkaar af te stemmen.
title: Wat is een Automated Personalization-activiteit (AP)?
feature: Automated Personalization
exl-id: 3654dce4-0d6c-42a3-8be7-e081ec478075
translation-type: tm+mt
source-git-commit: a92e88b46c72971d5d3c752593d651d8290b674e
workflow-type: tm+mt
source-wordcount: '996'
ht-degree: 0%

---

# ![](/help/assets/premium.png) PREMIUMAutomated Personalization (AP)

[!UICONTROL Automated Personalization] (AP) de activiteiten in  [!DNL Adobe Target] combineren aanbiedingen of berichten, en gebruikt geavanceerd machine leren om verschillende aanbiedingsvariaties aan elke bezoeker aan te passen die op hun individueel klantenprofiel worden gebaseerd, om inhoud en aandrijfhefboom te personaliseren.

>[!NOTE]
>
>[!UICONTROL Automated Personalization] is beschikbaar als onderdeel van de  [!DNL Target Premium] oplossing. Het is niet inbegrepen met [!DNL Target Standard] zonder een [!DNL Target Premium] vergunning. Als u een [!DNL Target Premium] licentie hebt, vervangt de [!DNL Target Premium] kaart de [!DNL Target Standard] kaart in [!DNL Adobe Experience Cloud].

Op dezelfde manier als [!UICONTROL Auto-Target], gebruikt [!UICONTROL Automated Personalization] een Willekeurig algoritme van het Bos, een belangrijke methode van de wetenschap van gegevens ensemble, als zijn belangrijkste verpersoonlijkingsalgoritme om de beste ervaring te bepalen om een bezoeker te tonen. [!UICONTROL Automated Personalization] kan waardevol zijn in de detectiefase van het testen. Het is ook handig om machinaal leren toe te staan om de meest effectieve inhoud te bepalen wanneer verschillende bezoekers zich hierop richten. In tijd, leert het algoritme om de meest efficiënte inhoud te voorspellen en toont de inhoud het meest waarschijnlijk om uw doelstellingen te bereiken.

Voor meer informatie over hoe [!UICONTROL Automated Personalization] van [!UICONTROL Auto-Target] verschilt, zie [Auto-Doel](/help/c-activities/auto-target/auto-target-to-optimize.md).

Marketers implementeren één bestand op hun site, waarmee ze op elke inhoud kunnen wijzen en klikken en vervolgens visueel aanvullende inhoudsopties voor dat gebied kunnen maken en selecteren met behulp van de VEC ([!UICONTROL Visual Experience Composer]). Vervolgens bepaalt het algoritme automatisch welk stuk inhoud aan elke individuele bezoeker moet worden geleverd op basis van alle gedragsgegevens die het systeem over die bezoeker heeft, wat een gepersonaliseerde ervaring oplevert. Omdat [!UICONTROL Automated Personalization] aan veranderingen in bezoekersgedrag kan aanpassen, kan het zonder een vastgestelde einddatum worden in werking gesteld om aan de gang zijnde lift en verpersoonlijking te verstrekken. Dit wordt soms ook wel de &quot;always-on&quot;-modus genoemd. De markeerteken hoeft geen test uit te voeren, de resultaten te analyseren en vervolgens een winnaar te leveren voordat de lift wordt gerealiseerd die uit optimalisatie is gevonden. Dit is een standaardvolgorde voor bewerkingen om het resultaat van een standaard A/B-activiteit te implementeren.

De volgende termen zijn handig wanneer u [!UICONTROL Automated Personalization] bespreekt:

| Term | Definitie |
|---|---|
| Meervoudig bewapende bandit | Een veelbewapende bandibenadering voor optimalisering brengt een evenwicht tot stand tussen verkennend leren en het benutten van dat leren. |
| Willekeurig bos | Random Forest is een toonaangevende aanpak voor machinaal leren. Op het gebied van gegevenswetenschappen is het een ensemble classificatie- of regressiemethode die werkt door het aanleggen van een groot aantal beslissingsbomen op basis van bezoekers en bezoekkenmerken. Binnen Target wordt het Willekeurige bos gebruikt om te bepalen welke ervaring naar verwachting de hoogste waarschijnlijkheid van omzetting (of hoogste opbrengst per bezoek) voor elke specifieke bezoeker zal hebben. Voor meer informatie over Willekeurig bos in Doel, zie [Random Forest Algorithm](/help/c-activities/t-automated-personalization/algo-random-forest.md). |
| Thompson Sampling | Het doel van Thompson Sampling is te bepalen welke ervaring de beste algemene (niet-gepersonaliseerde) ervaring is, terwijl de &#39;kosten&#39; van het vinden van die ervaring tot een minimum worden beperkt. Thompson-steekproeven kiezen altijd een winnaar, zelfs als er geen statistisch verschil tussen twee ervaringen is. Zie [Thompson Sampling](https://en.wikipedia.org/wiki/Thompson_sampling) voor meer informatie. |

Neem de volgende details in overweging wanneer u [!UICONTROL Automated Personalization] gebruikt:

**[!UICONTROL Automated Personalization]gebruikt een Willekeurig algoritme van het Bos om zich te personaliseren.**

Random Forest is een toonaangevende aanpak voor machinaal leren. Op het gebied van gegevenswetenschappen is het een ensemble classificatie- of regressiemethode die werkt door het aanleggen van een groot aantal beslissingsbomen op basis van bezoekers en bezoekkenmerken. Binnen Target wordt het Willekeurige bos gebruikt om te bepalen welke ervaring naar verwachting de hoogste waarschijnlijkheid van omzetting (of hoogste opbrengst per bezoek) voor elke specifieke bezoeker zal hebben. Bezoekers die Chrome gebruiken, zijn bijvoorbeeld loyaliteitsleden voor goud en hebben op dinsdagen toegang tot uw site, waardoor ze waarschijnlijk eerder zullen converteren met Experience A, terwijl bezoekers uit New York waarschijnlijk eerder zullen converteren met Experience B. Voor meer informatie over Willekeurig bos in Doel, zie [Random Forest Algorithm](/help/c-activities/t-automated-personalization/algo-random-forest.md).

**Het verpersoonlijkingsmodel optimaliseert voor elk bezoek.**

* Het algoritme voorspelt de waarschijnlijkheid van een bezoeker om (of geschatte opbrengst van omzetting) om de beste ervaring te dienen.
* Een bezoeker komt in aanmerking voor een nieuwe ervaring aan het einde van een bestaande sessie (tenzij hij of zij deel uitmaakt van de controlegroep, in welk geval de ervaring die de bezoeker tijdens het eerste bezoek heeft opgedaan, dezelfde is als die hij of zij bij volgende bezoeken zal zien).
* Binnen een sessie verandert de gepresenteerde ervaring niet om de visuele consistentie te behouden.

**Het verpersoonlijkingsmodel past zich aan veranderingen in bezoekersgedrag aan.**

* De multi-armbandit zorgt ervoor dat het model altijd een kleine fractie van verkeer &quot;uitgeeft&quot;om het leren door te zetten tijdens het leven van de activiteit, en om overexploitatie van eerder geleerde tendensen te verhinderen.
* De onderliggende modellen worden elke 24 uur opnieuw samengesteld met behulp van de meest recente gedragsgegevens van de bezoeker, zodat Target altijd gebruikmaakt van veranderende voorkeuren voor bezoekers.
* Als het algoritme het winnen van ervaringen voor individuele bezoekers niet kan bepalen, schakelt het automatisch aan het tonen van de algemeen best-presterende ervaring, terwijl nog steeds het zoeken naar gepersonaliseerde winnaars blijft. De best presterende ervaring wordt gevonden gebruikend [Thompson Sampling](https://en.wikipedia.org/wiki/Thompson_sampling).

**Het model optimaliseert voortdurend één enkele doel metrisch.**

* Deze metrische waarde kan op conversie of op inkomsten gebaseerd zijn (meer bepaald [!UICONTROL Revenue per Visitor]).

**Het doel verzamelt automatisch informatie over bezoekers om de verpersoonlijkingsmodellen te bouwen.**

* Zie [Automated Personalization-gegevensverzameling](/help/c-activities/t-automated-personalization/ap-data.md) voor meer informatie over de kenmerken die worden gebruikt in [!UICONTROL Auto-Target] en [!UICONTROL Automated Personalization].

**Het doel gebruikt automatisch alle  [!DNL Adobe Experience Cloud] gedeelde soorten publiek om de verpersoonlijkingsmodellen te bouwen.**

* U hoeft geen specifieke handelingen uit te voeren om een publiek aan het model toe te voegen. Zie [Experience Cloud Soorten publiek](/help/c-integrating-target-with-mac/mmp.md) voor informatie over het gebruik van [!DNL Experience Cloud Audiences] met [!DNL Target].

**Marketers kunnen offlinegegevens, proxyscores of andere aangepaste gegevens uploaden om personalisatiemodellen samen te stellen.**

Offlinegegevens, zoals CRM-informatie of klantchurn-concentratiescore, kunnen ongelooflijk waardevol zijn bij het maken van personalisatiemodellen. Er zijn verschillende manieren om gegevens in te voeren in [!UICONTROL Automated Personalization] (AP) en [!UICONTROL Auto-Target] verpersoonlijkingsalgoritmen.

* [mbox-parameters](/help/c-implementing-target/c-considerations-before-you-implement-target/c-methods-to-get-data-into-target/methods-to-get-data-into-target.md#concept_0069C0EFB56C4700BB33F2F35C2B9B17)
* [Profielparameters](/help/c-implementing-target/c-considerations-before-you-implement-target/c-methods-to-get-data-into-target/methods-to-get-data-into-target.md#concept_0069C0EFB56C4700BB33F2F35C2B9B17)
* [Server-side API&#39;s voor profielupdate](/help/c-implementing-target/c-considerations-before-you-implement-target/c-methods-to-get-data-into-target/methods-to-get-data-into-target.md#concept_0069C0EFB56C4700BB33F2F35C2B9B17)

Zie [Automated Personalization Data Collection](/help/c-activities/t-automated-personalization/ap-data.md) voor informatie over de gegevens die automatisch worden verzameld en gebruikt door [!UICONTROL Automated Personalization]- en [!UICONTROL Auto-Target]-verpersoonlijkingsalgoritmen.

## ![Video over ](/help/assets/overview.png) badgeTraining in overzicht: Activiteitstypen

In deze video worden de activiteitstypen beschreven die beschikbaar zijn in [!DNL Target Standard/Premium]. [!UICONTROL Automated Personalization] wordt om 5:55 besproken.

* Beschrijf de soorten activiteiten inbegrepen in [!DNL Adobe Target]
* Selecteer het juiste type activiteit om uw doelen te bereiken
* Beschrijf de driestappenworkflow met instructies die van toepassing is op alle typen activiteiten

>[!VIDEO](https://video.tv.adobe.com/v/17386)
