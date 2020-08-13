---
keywords: automated personalization;Audiences;ensemble;random forest
description: Automated Personalization (AP) combineert aanbiedingen of berichten en maakt gebruik van geavanceerd computergebruik om verschillende aanbiedingsvariaties voor elke bezoeker af te stemmen op basis van hun individuele klantprofiel, om de inhoud en het optillen van de drive aan te passen.
title: Automated Personalization
feature: ap
topic: Advanced
uuid: cf9489f2-45b2-4028-8956-36d0afe0ee0a
translation-type: tm+mt
source-git-commit: b2f80c89ecceb6f88a176db7a90e71a162a24641
workflow-type: tm+mt
source-wordcount: '986'
ht-degree: 0%

---


# ![PREMIUM](/help/assets/premium.png) Automated Personalization{#automated-personalization}

[!UICONTROL Automated Personalization] (AP) combineert aanbiedingen of berichten en maakt gebruik van geavanceerd computerleren om verschillende aanbiedingsvariaties voor elke bezoeker af te stemmen op basis van hun individuele klantprofiel, om de inhoud aan te passen en de lift aan te passen.

>[!NOTE]
>
>[!UICONTROL Automated Personalization] is beschikbaar als onderdeel van de [!DNL Target Premium] oplossing. Het is niet inbegrepen met [!DNL Target Standard] zonder een [!DNL Target Premium] vergunning. Als u een [!DNL Target Premium] licentie hebt, vervangt de [!DNL Target Premium] kaart de [!DNL Target Standard] kaart in de [!DNL Adobe Experience Cloud].

Op dezelfde manier als [!UICONTROL Auto-Target], gebruikt [!UICONTROL Automated Personalization] een Willekeurig Bos algoritme, een belangrijke methode van de gegevenswetenschap ensemble, als zijn belangrijkste verpersoonlijkingsalgoritme om de beste ervaring te bepalen om een bezoeker te tonen. [!UICONTROL Automated Personalization] kan waardevol zijn in de detectiefase van het testen. Het is ook handig om machinaal leren toe te staan om de meest effectieve inhoud te bepalen wanneer verschillende bezoekers zich hierop richten. In tijd, leert het algoritme om de meest efficiënte inhoud te voorspellen en toont de inhoud het meest waarschijnlijk om uw doelstellingen te bereiken.

Voor meer informatie over hoe [!UICONTROL Automated Personalization] verschilt van [!UICONTROL Auto-Target], zie [auto-Doel voor Persoonlijke Ervaringen](../../c-activities/auto-target-to-optimize.md#concept_67779E5B7F67427A97D7EA2A6FB919B3).

Marketers implementeren één bestand op hun site, waarmee ze op elke inhoud kunnen wijzen en klikken en vervolgens visueel aanvullende inhoudsopties voor dat gebied kunnen maken en selecteren met behulp van de VEC ([!UICONTROL Visual Experience Composer]). Vervolgens bepaalt het algoritme automatisch welk stuk inhoud aan elke individuele bezoeker moet worden geleverd op basis van alle gedragsgegevens die het systeem over die bezoeker heeft, wat een gepersonaliseerde ervaring oplevert. Omdat [!UICONTROL Automated Personalization] kan aanpassen aan wijzigingen in het gedrag van bezoekers, kan het zonder een vastgestelde einddatum worden uitgevoerd om voortdurende lift en verpersoonlijking te verstrekken. Dit wordt soms ook wel de &quot;always-on&quot;-modus genoemd. De markeerteken hoeft geen test uit te voeren, de resultaten te analyseren en vervolgens een winnaar te leveren voordat de lift wordt gerealiseerd die uit optimalisatie is gevonden. Dit is een standaardvolgorde voor bewerkingen om het resultaat van een standaard A/B-activiteit te implementeren.

De volgende termen zijn handig wanneer u discussieert over [!UICONTROL Automated Personalization]:

| Term | Definitie |
|---|---|
| Meervoudig bewapende bandit | Een veelbewapende bandibenadering voor optimalisering brengt een evenwicht tot stand tussen verkennend leren en het benutten van dat leren. |
| Willekeurig bos | Random Forest is een toonaangevende aanpak voor machinaal leren. Op het gebied van gegevenswetenschappen is het een ensemble classificatie- of regressiemethode die werkt door het aanleggen van een groot aantal beslissingsbomen op basis van bezoekers en bezoekkenmerken. Binnen Target wordt het Willekeurige bos gebruikt om te bepalen welke ervaring naar verwachting de hoogste waarschijnlijkheid van omzetting (of hoogste opbrengst per bezoek) voor elke specifieke bezoeker zal hebben. Voor meer informatie over Willekeurig bos in Doel, zie [Willekeurig Bosalgoritme](../../c-activities/t-automated-personalization/algo-random-forest.md#concept_48F3CDAA16A848D2A84CDCD19DAAE3AA). |
| Thompson Sampling | Het doel van Thompson Sampling is te bepalen welke ervaring de beste algemene (niet-gepersonaliseerde) ervaring is, terwijl de &#39;kosten&#39; van het vinden van die ervaring tot een minimum worden beperkt. Thompson-steekproeven kiezen altijd een winnaar, zelfs als er geen statistisch verschil tussen twee ervaringen is. Zie [Thompson Sampling](https://en.wikipedia.org/wiki/Thompson_sampling)voor meer informatie. |

Houd rekening met de volgende details wanneer u [!UICONTROL Automated Personalization]gebruikt:

**[!UICONTROL Automated Personalization]gebruikt een Willekeurig algoritme van het Bos om zich te personaliseren.**

Random Forest is een toonaangevende aanpak voor machinaal leren. Op het gebied van gegevenswetenschappen is het een ensemble classificatie- of regressiemethode die werkt door het aanleggen van een groot aantal beslissingsbomen op basis van bezoekers en bezoekkenmerken. Binnen Target wordt het Willekeurige bos gebruikt om te bepalen welke ervaring naar verwachting de hoogste waarschijnlijkheid van omzetting (of hoogste opbrengst per bezoek) voor elke specifieke bezoeker zal hebben. Bezoekers die Chrome gebruiken, zijn bijvoorbeeld loyaliteitsleden voor goud en hebben op dinsdagen toegang tot uw site, waardoor ze waarschijnlijk eerder zullen converteren met Experience A, terwijl bezoekers uit New York waarschijnlijk eerder zullen converteren met Experience B. Voor meer informatie over Willekeurig bos in Doel, zie [Willekeurig Bosalgoritme](../../c-activities/t-automated-personalization/algo-random-forest.md#concept_48F3CDAA16A848D2A84CDCD19DAAE3AA).

**Het verpersoonlijkingsmodel optimaliseert voor elk bezoek.**

* Het algoritme voorspelt de waarschijnlijkheid van een bezoeker om (of geschatte opbrengst van omzetting) om de beste ervaring te dienen.
* Een bezoeker komt in aanmerking voor een nieuwe ervaring aan het einde van een bestaande sessie (tenzij hij of zij deel uitmaakt van de controlegroep, in welk geval de ervaring die de bezoeker tijdens het eerste bezoek heeft opgedaan, dezelfde is als die hij of zij bij volgende bezoeken zal zien).
* Binnen een sessie verandert de gepresenteerde ervaring niet om de visuele consistentie te behouden.

**Het verpersoonlijkingsmodel past zich aan veranderingen in bezoekersgedrag aan.**

* De multi-armbandit zorgt ervoor dat het model altijd een kleine fractie van verkeer &quot;uitgeeft&quot;om het leren door te zetten tijdens het leven van de activiteit, en om overexploitatie van eerder geleerde tendensen te verhinderen.
* De onderliggende modellen worden elke 24 uur opnieuw samengesteld met behulp van de meest recente gedragsgegevens van de bezoeker, zodat Target altijd gebruikmaakt van veranderende voorkeuren voor bezoekers.
* Als het algoritme het winnen van ervaringen voor individuele bezoekers niet kan bepalen, schakelt het automatisch aan het tonen van de algemeen best-presterende ervaring, terwijl nog steeds het zoeken naar gepersonaliseerde winnaars blijft. De best presterende ervaring wordt gevonden gebruikend [Thompson Steekproef](https://en.wikipedia.org/wiki/Thompson_sampling).

**Het model optimaliseert voortdurend één enkele doel metrisch.**

* Deze metrische waarde kan op conversie of op inkomsten gebaseerd zijn (meer bepaald, [!UICONTROL Revenue per Visitor]).

**Het doel verzamelt automatisch informatie over bezoekers om de verpersoonlijkingsmodellen te bouwen.**

* Voor meer informatie over de attributen die in [!UICONTROL Auto-Target] en [!UICONTROL Automated Personalization], zie de Inzameling [van Gegevens van](../../c-activities/t-automated-personalization/ap-data.md#reference_255BD3DE7AD04DC9B766E0BC78961058)Automated Personalization worden gebruikt.

**Het doel gebruikt automatisch alle[!DNL Adobe Experience Cloud]gedeelde toehoorders om de verpersoonlijkingsmodellen te bouwen.**

* U hoeft geen specifieke handelingen uit te voeren om een publiek aan het model toe te voegen. Voor informatie over het gebruiken [!DNL Experience Cloud Audiences] met [!DNL Target], zie [Experience Cloud Soorten publiek](../../c-integrating-target-with-mac/mmp.md#concept_F4863DE4C92D4805AB690B4B3D487969).

**Marketers kunnen offlinegegevens, proxyscores of andere aangepaste gegevens uploaden om personalisatiemodellen samen te stellen.**

Offlinegegevens, zoals CRM-informatie of klantchurn-concentratiescore, kunnen ongelooflijk waardevol zijn bij het maken van personalisatiemodellen. Er zijn verschillende manieren om gegevens in te voeren in [!UICONTROL Automated Personalization] (AP)- en [!UICONTROL Auto-Target] personalisatiealgoritmen.

* [mbox-parameters](../../c-implementing-target/c-considerations-before-you-implement-target/c-methods-to-get-data-into-target/methods-to-get-data-into-target.md#concept_0069C0EFB56C4700BB33F2F35C2B9B17)
* [Profielparameters](../../c-implementing-target/c-considerations-before-you-implement-target/c-methods-to-get-data-into-target/methods-to-get-data-into-target.md#concept_0069C0EFB56C4700BB33F2F35C2B9B17)
* [Server-side API&#39;s voor profielupdate](../../c-implementing-target/c-considerations-before-you-implement-target/c-methods-to-get-data-into-target/methods-to-get-data-into-target.md#concept_0069C0EFB56C4700BB33F2F35C2B9B17)

Zie Gegevensverzameling [!UICONTROL Automated Personalization] van [!UICONTROL Auto-Target] Automated Personalization voor informatie over de gegevens die automatisch worden verzameld en gebruikt door [en](../../c-activities/t-automated-personalization/ap-data.md#reference_255BD3DE7AD04DC9B766E0BC78961058)personalisatiealgoritmen.

## ![Video over training badge](/help/assets/overview.png) overzicht: Activiteitstypen

In deze video worden de activiteitstypen uitgelegd die beschikbaar zijn in [!DNL Target Standard/Premium]. [!UICONTROL Automated Personalization] wordt om 5:55 besproken.

* Beschrijf de soorten activiteiten die onder [!DNL Adobe Target]
* Selecteer het juiste type activiteit om uw doelen te bereiken
* Beschrijf de driestappenworkflow met instructies die van toepassing is op alle typen activiteiten

>[!VIDEO](https://video.tv.adobe.com/v/17386)