---
keywords: geautomatiseerde personalisatie;ap;publiek;ensemble;random forest;multi-gewapende bandit;thompson sampling;ml;machine leren
description: Leer hoe u Automated Personalization-activiteiten (AP) kunt gebruiken in Adobe [!DNL Target] die gebruikmaken van geavanceerd leren van machines om verschillende aanbiedingsvariaties aan te passen aan elke bezoeker.
title: Wat is een Automated Personalization-activiteit (AP)?
feature: Automated Personalization
exl-id: 3654dce4-0d6c-42a3-8be7-e081ec478075
source-git-commit: b1e8ea2370fc15f4bfcd960ab2960cafe2db92b8
workflow-type: tm+mt
source-wordcount: '1012'
ht-degree: 0%

---

# ![PREMIUM](/help/main/assets/premium.png) Automated Personalization (AP)

[!UICONTROL Automated Personalization] (AP) activiteiten in [!DNL Adobe Target] combineer aanbiedingen of berichten, en gebruikt geavanceerd machinaal leren om verschillende aanbiedingsvariaties aan elke bezoeker aan te passen die op hun individueel klantenprofiel worden gebaseerd, om inhoud en aandrijfhefboom te personaliseren.

>[!NOTE]
>
>[!UICONTROL Automated Personalization] is beschikbaar als onderdeel van de [!DNL Target Premium] oplossing. Het is niet opgenomen in [!DNL Target Standard] zonder [!DNL Target Premium] licentie. Als u een [!DNL Target Premium] de [!DNL Target Premium] de kaart vervangt [!DNL Target Standard] in de [!DNL Adobe Experience Cloud].

Op dezelfde manier als [!UICONTROL Auto-Target], [!UICONTROL Automated Personalization] gebruikt een Random Forest-algoritme, een toonaangevende methode voor het samenvoegen van gegevenswetenschap, als hoofdalgoritme voor personalisatie om de beste ervaring te bepalen om een bezoeker te tonen. [!UICONTROL Automated Personalization] kan waardevol zijn in de detectiefase van het testen. Het is ook handig om machinaal leren toe te staan om de meest effectieve inhoud te bepalen wanneer verschillende bezoekers zich hierop richten. In tijd, leert het algoritme om de meest efficiënte inhoud te voorspellen en toont de inhoud het meest waarschijnlijk om uw doelstellingen te bereiken.

Meer informatie over hoe [!UICONTROL Automated Personalization] verschilt van [!UICONTROL Auto-Target], zie [Automatisch doel](/help/main/c-activities/auto-target/auto-target-to-optimize.md).

Marketers implementeren één bestand op hun site, zodat ze op elke inhoud kunnen wijzen en klikken en vervolgens visueel aanvullende inhoudsopties voor dat gebied kunnen maken en selecteren met behulp van de VEC ([!UICONTROL Visual Experience Composer]). Vervolgens bepaalt het algoritme automatisch welk stuk inhoud aan elke individuele bezoeker moet worden geleverd op basis van alle gedragsgegevens die het systeem over die bezoeker heeft, wat een gepersonaliseerde ervaring oplevert. Omdat [!UICONTROL Automated Personalization] kan worden aangepast aan wijzigingen in het gedrag van de bezoeker. U kunt dit doen zonder een ingestelde einddatum voor een continue lift en personalisatie. Dit wordt soms ook wel de &quot;always-on&quot;-modus genoemd. De markeerteken hoeft geen test uit te voeren, de resultaten te analyseren en vervolgens een winnaar te leveren voordat de lift wordt gerealiseerd die uit optimalisatie is gevonden. Dit is een standaardvolgorde voor bewerkingen om het resultaat van een standaard A/B-activiteit te implementeren.

De volgende termen zijn handig wanneer u discussieert over [!UICONTROL Automated Personalization]:

| Term | Definitie |
|---|---|
| Meervoudig bewapende bandit | Een veelbewapende bandibenadering voor optimalisering brengt een evenwicht tot stand tussen verkennend leren en het benutten van dat leren. |
| Willekeurig bos | Random Forest is een toonaangevende aanpak voor machinaal leren. Op het gebied van gegevenswetenschappen is het een ensemble classificatie- of regressiemethode die werkt door het aanleggen van een groot aantal beslissingsbomen op basis van bezoekers en bezoekkenmerken. Binnen Target wordt het Willekeurige bos gebruikt om te bepalen welke ervaring naar verwachting de hoogste waarschijnlijkheid van omzetting (of hoogste opbrengst per bezoek) voor elke specifieke bezoeker zal hebben. Voor meer informatie over Willekeurig bos in Doel, zie [Random Forest Algorithm](/help/main/c-activities/t-automated-personalization/algo-random-forest.md). |
| Thompson Sampling | Het doel van Thompson Sampling is te bepalen welke ervaring de beste algemene (niet-gepersonaliseerde) ervaring is, terwijl de &#39;kosten&#39; van het vinden van die ervaring tot een minimum worden beperkt. Thompson-steekproeven kiezen altijd een winnaar, zelfs als er geen statistisch verschil tussen twee ervaringen is. Zie voor meer informatie [Thompson Sampling](https://en.wikipedia.org/wiki/Thompson_sampling). |

Houd rekening met de volgende details wanneer u [!UICONTROL Automated Personalization]:

**[!UICONTROL Automated Personalization]gebruikt een Willekeurig algoritme van het Bos om zich te personaliseren.**

Random Forest is een toonaangevende aanpak voor machinaal leren. Op het gebied van gegevenswetenschappen is het een ensemble classificatie- of regressiemethode die werkt door het aanleggen van een groot aantal beslissingsbomen op basis van bezoekers en bezoekkenmerken. Binnen Target wordt het Willekeurige bos gebruikt om te bepalen welke ervaring naar verwachting de hoogste waarschijnlijkheid van omzetting (of hoogste opbrengst per bezoek) voor elke specifieke bezoeker zal hebben. Bezoekers die Chrome gebruiken, zijn bijvoorbeeld loyaliteitsleden voor goud en hebben op dinsdagen toegang tot uw site, waardoor ze waarschijnlijk eerder zullen converteren met Experience A, terwijl bezoekers uit New York waarschijnlijk eerder zullen converteren met Experience B. Voor meer informatie over Willekeurig bos in Doel, zie [Random Forest Algorithm](/help/main/c-activities/t-automated-personalization/algo-random-forest.md).

**Het verpersoonlijkingsmodel optimaliseert voor elk bezoek.**

* Het algoritme voorspelt de waarschijnlijkheid van een bezoeker om (of geschatte opbrengst van omzetting) om de beste ervaring te dienen.
* Een bezoeker komt in aanmerking voor een nieuwe ervaring aan het einde van een bestaande sessie (tenzij hij of zij deel uitmaakt van de controlegroep, in welk geval de ervaring die de bezoeker tijdens het eerste bezoek heeft opgedaan, dezelfde is als die hij of zij bij volgende bezoeken zal zien).
* Binnen een sessie verandert de gepresenteerde ervaring niet om de visuele consistentie te behouden.

**Het verpersoonlijkingsmodel past zich aan veranderingen in bezoekersgedrag aan.**

* De multi-armbandit zorgt ervoor dat het model altijd een kleine fractie van verkeer &quot;uitgeeft&quot;om het leren door te zetten tijdens het leven van de activiteit, en om overexploitatie van eerder geleerde tendensen te verhinderen.
* De onderliggende modellen worden elke 24 uur opnieuw samengesteld met behulp van de meest recente gedragsgegevens van de bezoeker, zodat Target altijd gebruikmaakt van veranderende voorkeuren voor bezoekers.
* Als het algoritme het winnen van ervaringen voor individuele bezoekers niet kan bepalen, schakelt het automatisch aan het tonen van de algemeen best-presterende ervaring, terwijl nog steeds het zoeken naar gepersonaliseerde winnaars blijft. De best presterende ervaring wordt gevonden gebruikend [Thompson Sampling](https://en.wikipedia.org/wiki/Thompson_sampling).

**Het model optimaliseert voortdurend één enkele doel metrisch.**

* Deze metrische waarde zou op omzetting-gebaseerd of op opbrengst-gebaseerd (meer specifiek) kunnen zijn, [!UICONTROL Revenue per Visitor]).

**Het doel verzamelt automatisch informatie over bezoekers om de verpersoonlijkingsmodellen te bouwen.**

* Meer informatie over de kenmerken die worden gebruikt in [!UICONTROL Auto-Target] en [!UICONTROL Automated Personalization], zie [Automated Personalization-gegevensverzameling](/help/main/c-activities/t-automated-personalization/ap-data.md).

**Doel gebruikt automatisch alle [!DNL Adobe Experience Cloud] een gedeeld publiek om de personalisatiemodellen op te bouwen.**

* U hoeft geen specifieke handelingen uit te voeren om een publiek aan het model toe te voegen. Voor informatie over het gebruik [!DNL Experience Cloud Audiences] with [!DNL Target], zie [Experience Cloud publiek](/help/main/c-integrating-target-with-mac/mmp.md).

**Marketers kunnen offlinegegevens, proxyscores of andere aangepaste gegevens uploaden om personalisatiemodellen samen te stellen.**

Offlinegegevens, zoals CRM-informatie of klantchurn-concentratiescore, kunnen ongelooflijk waardevol zijn bij het maken van personalisatiemodellen. Er zijn verschillende manieren om gegevens in te voeren in [!UICONTROL Automated Personalization] (AP) en [!UICONTROL Auto-Target] personalisatiealgoritmen.

* [mbox-parameters](https://developer.adobe.com/target/before-implement/methods-to-get-data-into-target/methods-to-get-data-into-target/)
* [Profielparameters](https://developer.adobe.com/target/before-implement/methods-to-get-data-into-target/methods-to-get-data-into-target/)
* [Server-side API&#39;s voor profielupdate](https://developer.adobe.com/target/before-implement/methods-to-get-data-into-target/methods-to-get-data-into-target/)

Voor informatie over automatisch verzamelde en gebruikte gegevens door [!UICONTROL Automated Personalization] en [!UICONTROL Auto-Target] verpersoonlijkingsalgoritmen, zie [Automated Personalization-gegevensverzameling](/help/main/c-activities/t-automated-personalization/ap-data.md).

## ![Overzicht badge](/help/main/assets/overview.png) Trainingsvideo: Activiteitstypen

In deze video worden de activiteitstypen uitgelegd die beschikbaar zijn in [!DNL Target Standard/Premium]. [!UICONTROL Automated Personalization] wordt om 5:55 besproken.

* Beschrijf de soorten activiteiten die onder [!DNL Adobe Target]
* Selecteer het juiste type activiteit om uw doelen te bereiken
* Beschrijf de driestappenworkflow met instructies die van toepassing is op alle typen activiteiten

>[!VIDEO](https://video.tv.adobe.com/v/17386)
