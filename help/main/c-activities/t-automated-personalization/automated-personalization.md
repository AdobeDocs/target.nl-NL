---
keywords: geautomatiseerde personalisatie;ap;publiek;ensemble;random forest;multi-gewapende bandit;thompson sampling;ml;machine leren
description: Leren gebruiken [!UICONTROL Automated Personalization] (AP) [!DNL Adobe Target] die gebruik maken van geavanceerd computerleren om verschillende aanbiedingsvariaties voor elke bezoeker op elkaar af te stemmen.
title: Wat is een [!UICONTROL Automated Personalization] (AP) Activiteit?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=nl-NL#premium newtab=true" tooltip="Zie wat er in Target Premium is opgenomen."
feature: Automated Personalization
exl-id: 3654dce4-0d6c-42a3-8be7-e081ec478075
source-git-commit: d5b24f298ae405d57c2ba639082cbe99c4e358fd
workflow-type: tm+mt
source-wordcount: '967'
ht-degree: 0%

---

# [!UICONTROL Automated Personalization] (AP)

[!UICONTROL Automated Personalization] (AP) [!DNL Adobe Target] combineer aanbiedingen of berichten en gebruik geavanceerde computerlessen om verschillende aanbiedingsvariaties voor elke bezoeker af te stemmen op basis van hun individuele klantprofiel, zodat de inhoud wordt aangepast en de lift wordt aangestuurd.

>[!NOTE]
>
>[!UICONTROL Automated Personalization] is beschikbaar als onderdeel van de [!DNL Target Premium] oplossing. Deze functie is niet beschikbaar in [!DNL Target Standard] zonder [!DNL Target Premium] licentie. Voor meer informatie over de geavanceerde functies die deze licentie biedt, raadpleegt u [Doelpremie](/help/main/c-intro/intro.md#premium).

Op dezelfde manier als [!UICONTROL Auto-Target], [!UICONTROL Automated Personalization] gebruikt een [Random Forest-algoritme](/help/main/c-activities/t-automated-personalization/algo-random-forest.md), een toonaangevende methode voor het samenvoegen van gegevens in de wetenschap, als hoofdalgoritme voor het personaliseren van gegevens om de beste ervaring te bepalen om een bezoeker te tonen. [!UICONTROL Automated Personalization] kan waardevol zijn in de detectiefase van het testen. Het is ook handig om machinaal leren toe te staan om de meest effectieve inhoud te bepalen wanneer verschillende bezoekers zich hierop richten. In tijd, leert het algoritme om de meest efficiënte inhoud te voorspellen en toont de inhoud het meest waarschijnlijk om uw doelstellingen te bereiken.

Meer informatie over hoe [!UICONTROL Automated Personalization] verschilt van [!UICONTROL Auto-Target], zie [Automatisch doel](/help/main/c-activities/auto-target/auto-target-to-optimize.md#section_BA4D83BE40F14A96BE7CBC7C7CF2A8FB).

Marketers implementeren één bestand op hun site, waardoor ze inhoud kunnen aanwijzen en klikken en vervolgens visueel aanvullende inhoudsopties voor dat gebied kunnen maken en selecteren met behulp van het [!UICONTROL Visual Experience Composer] (VEC). Vervolgens bepaalt het algoritme automatisch welk stuk inhoud aan elke individuele bezoeker moet worden geleverd op basis van alle gedragsgegevens die het systeem over die bezoeker heeft, wat een gepersonaliseerde ervaring oplevert. Omdat [!UICONTROL Automated Personalization] kan worden aangepast aan wijzigingen in het gedrag van de bezoeker. U kunt dit doen zonder een ingestelde einddatum voor een continue lift en personalisatie. Deze modus wordt soms ook &#39;always-on&#39; genoemd. De markeerteken hoeft geen test uit te voeren, de resultaten te analyseren en vervolgens een winnaar te leveren voordat de lift wordt gerealiseerd die uit optimalisatie is gevonden. Dit is een standaardvolgorde voor bewerkingen om het resultaat van een standaard A/B-activiteit te implementeren.

De volgende termen zijn handig wanneer u discussieert over [!UICONTROL Automated Personalization]:

| Term | Definitie |
|---|---|
| Meervoudig bewapende bandit | Een veelbewapende bandibenadering voor optimalisering brengt een evenwicht tot stand tussen verkennend leren en het benutten van dat leren. |
| Willekeurig bos | Een toonaangevende aanpak voor het leren van machines. In gegevenswetenschappelijk opzicht is het een ensemble classificatie- of regressiemethode die werkt door het aanleggen van veel beslissingsbomen op basis van bezoekers en bezoekkenmerken. |
| Thompson Sampling | Het doel van Thompson Sampling is te bepalen welke ervaring de beste algemene (niet-gepersonaliseerde) ervaring is, terwijl de &#39;kosten&#39; van het vinden van die ervaring tot een minimum worden beperkt. Thompson-steekproeven kiezen altijd een winnaar, zelfs als er geen statistisch verschil tussen twee ervaringen is. Zie voor meer informatie [Thompson Sampling](https://en.wikipedia.org/wiki/Thompson_sampling). |

Houd rekening met de volgende details wanneer u [!UICONTROL Automated Personalization]:

## [!UICONTROL Automated Personalization] gebruikt Willekeurig bosalgoritme om te personaliseren

Random Forest is een toonaangevende machineleesmethode. In gegevenswetenschappelijk opzicht is het een ensemble classificatie- of regressiemethode die werkt door het aanleggen van veel beslissingsbomen op basis van bezoekers en bezoekkenmerken. Within [!DNL Target], wordt Random Forest gebruikt om te bepalen welke ervaring naar verwachting de hoogste waarschijnlijkheid van omrekening (of hoogste inkomsten per bezoek) voor elke specifieke bezoeker zal hebben. Bezoekers die Chrome gebruiken, zijn bijvoorbeeld loyaliteitsleden voor goud en hebben op dinsdagen toegang tot uw site, waardoor ze waarschijnlijk eerder zullen converteren met Experience A. Bezoekers uit New York kunnen waarschijnlijk eerder converteren met Experience B. Voor meer informatie over Random Forest in [!DNL Target], zie [Random Forest Algorithm](/help/main/c-activities/t-automated-personalization/algo-random-forest.md).

## Het verpersoonlijkingsmodel optimaliseert voor elk bezoek

* Het algoritme voorspelt de waarschijnlijkheid van een bezoeker van omzetting (of geschatte opbrengst van omzetting) om de beste ervaring te dienen.
* Een bezoeker komt in aanmerking voor een nieuwe ervaring aan het einde van een bestaande sessie, tenzij die bezoeker deel uitmaakt van de controlegroep. Als de bezoeker deel uitmaakt van de controlegroep, heeft de bezoeker bij het eerste bezoek dezelfde ervaring als bij volgende bezoeken.
* De gepresenteerde ervaring verandert niet binnen een sessie om de visuele consistentie te behouden.

## Het verpersoonlijkingsmodel past zich aan veranderingen in bezoekersgedrag aan

* De multiarmbandit zorgt ervoor dat het model altijd een klein deel van het verkeer &quot;besteedt&quot;om het leren door te zetten tijdens het leven van de activiteit en om overexploitatie van eerder geleerde tendensen te verhinderen.
* De onderliggende modellen worden om de 24 uur opnieuw samengesteld met behulp van de meest recente gedragsgegevens van de bezoeker om ervoor te zorgen dat [!DNL Target] gebruikt altijd gewijzigde voorkeuren voor bezoekers.
* Als het algoritme het winnen van ervaringen voor individuele bezoekers niet kan bepalen, schakelt het automatisch aan het tonen van de algemeen best-presterende ervaring, terwijl nog steeds het zoeken naar gepersonaliseerde winnaars blijft. De best presterende ervaring wordt gevonden gebruikend [Thompson Sampling](https://en.wikipedia.org/wiki/Thompson_sampling).

## Het model optimaliseert voortdurend één doel metrisch

* Deze metrische waarde zou op omzetting-gebaseerd of op opbrengst-gebaseerd (meer specifiek) kunnen zijn, [!UICONTROL Revenue per Visitor]).

## [!DNL Target] verzamelt automatisch informatie over bezoekers om de verpersoonlijkingsmodellen te bouwen

* Meer informatie over de kenmerken die worden gebruikt in [!UICONTROL Auto-Target] en [!UICONTROL Automated Personalization], zie [Automated Personalization-gegevensverzameling](/help/main/c-activities/t-automated-personalization/ap-data.md).

## [!DNL Target] gebruikt automatisch alle [!DNL Adobe Experience Cloud] gedeeld publiek om de personalisatiemodellen op te bouwen

* U hoeft niets specifiek te doen om publiek aan het model toe te voegen. Voor informatie over het gebruik [!DNL Experience Cloud Audiences] with [!DNL Target], zie [Soorten publiek Experience Cloud](/help/main/c-integrating-target-with-mac/mmp.md).

## Marketers kunnen offlinegegevens, concentratiescore of andere aangepaste gegevens uploaden om personalisatiemodellen samen te stellen

Offlinegegevens, zoals CRM-informatie of klantchurn-concentratiescore, kunnen ongelooflijk waardevol zijn bij het samenstellen van personalisatiemodellen. Er zijn verschillende manieren om gegevens in te voeren in [!UICONTROL Automated Personalization] (AP) en [!UICONTROL Auto-Target] personalisatiealgoritmen.

* [mbox-parameters](https://experienceleague.adobe.com/docs/target-dev/developer/implementation/methods/methods-to-get-data-into-target.html?lang=nl-NL){target=_blank}
* [Profielparameters](https://experienceleague.adobe.com/docs/target-dev/developer/implementation/methods/methods-to-get-data-into-target.html?lang=nl-NL){target=_blank}
* [Server-side API&#39;s voor profielupdate](https://experienceleague.adobe.com/docs/target-dev/developer/implementation/methods/methods-to-get-data-into-target.html?lang=nl-NL){target=_blank}

Voor informatie over automatisch verzamelde en gebruikte gegevens door [!UICONTROL Automated Personalization] en [!UICONTROL Auto-Target] verpersoonlijkingsalgoritmen, zie [Automated Personalization-gegevensverzameling](/help/main/c-activities/t-automated-personalization/ap-data.md).

## Trainingsvideo: Activiteitstypen

In deze video wordt uitgelegd welke soorten activiteiten beschikbaar zijn in [!DNL Target]. [!UICONTROL Automated Personalization] wordt om 5:55 besproken.

* Beschrijf de soorten activiteiten die onder [!DNL Adobe Target]
* Selecteer het juiste type activiteit om uw doelen te bereiken
* Beschrijf de driestappenworkflow met instructies die van toepassing is op alle typen activiteiten

>[!VIDEO](https://video.tv.adobe.com/v/17386)
