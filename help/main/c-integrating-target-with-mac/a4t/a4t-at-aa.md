---
keywords: a4t;A4T;Analyses als bron voor rapportage voor Doel;analytische gegevens voor doel
description: Leer hoe te om [!UICONTROL Auto-Allocate] en [!UICONTROL Auto-Target] activiteiten in  [!DNL Target]  tot stand te brengen die  [!DNL Analytics]  als rapporteringsbron (A4T) gebruiken.
title: Biedt A4T ondersteuning voor [!UICONTROL Auto-Allocate] - en [!UICONTROL Auto-Target] -activiteiten?
feature: Analytics for Target (A4T)
exl-id: 3302f26d-c445-4779-8435-be142d5cea8c
source-git-commit: ddced04c730519dae74e70a60bed26462825ad23
workflow-type: tm+mt
source-wordcount: '1276'
ht-degree: 0%

---

# A4T-ondersteuning voor [!UICONTROL Auto-Allocate] - en [!UICONTROL Auto-Target] -activiteiten

De [!DNL Adobe Target] - aan [!DNL Adobe Analytics] integratie, die als [&#x200B; Analytics voor Doel &#x200B;](/help/main/c-integrating-target-with-mac/a4t/a4t.md) (A4T) wordt bekend, steunt [!UICONTROL Auto-Allocate] en [!UICONTROL Auto-Target] activiteiten.

Met de integratie A4T kunt u:

* Gebruik het [&#x200B; auto-Wijs &#x200B;](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md) multi-gewapende bandit vermogen toe om verkeer aan het winnen van ervaringen te drijven.
* Gebruik het [&#x200B; auto-Doel &#x200B;](/help/main/c-activities/auto-target/auto-target-to-optimize.md) ensemble machine-leert algoritme om de beste ervaring voor elke bezoeker te kiezen. [!UICONTROL Auto-Target] kiest de beste ervaring op basis van het profiel, het gedrag en de context van elke gebruiker, en gebruikt daarbij tegelijkertijd een [!DNL Adobe Analytics] doel-meting en de rijke rapportage- en analysemogelijkheden van [!DNL Adobe Analytics] .

Zorg ervoor dat u [&#x200B; A4T voor gebruik met de Test van A/B en Ervaring die activiteiten richten &#x200B;](/help/main/c-integrating-target-with-mac/a4t/a4timplementation.md) hebt uitgevoerd. Wanneer u `analyticsLogging = client_side` gebruikt, moet u ook de `sessionId` waarde aan [!DNL Analytics] doorgeven. Voor meer informatie, zie [&#x200B; Analyses voor Doel (A4T) die &#x200B;](https://experienceleague.adobe.com/docs/target-dev/developer/server-side/integration/a4t-reporting.html?lang=nl-NL){target=_blank} in de *Gids van de Ontwikkelaar van Adobe Target* melden.

Aan de slag:

1. Terwijl [&#x200B; creërend een [!UICONTROL A/B Test] activiteit &#x200B;](/help/main/c-activities/t-test-ab/t-test-create-ab/test-create-ab.md), op de **[!UICONTROL Targeting]** pagina, klik de **[!UICONTROL Traffic Allocation]** controle, dan kies de gewenste methode van de verkeerstoewijzing in de juiste ruit.

   ![&#x200B; montages van de Methode van de Toewijzing van het Verkeer &#x200B;](/help/main/c-activities/assets/auto-target.png)

   De volgende methoden voor verkeerstoewijzing zijn beschikbaar:

   * **[!UICONTROL Manual (Default)]**: geef het percentage van de gegadigden op dat u elke ervaring wilt zien. U kunt de percentages gelijkmatig over alle ervaringen verdelen, of hogere of lagere percentages voor elke ervaring specificeren. Het totaal voor alle ervaringen moet 100% bedragen.

   * **[!UICONTROL Auto-Allocate to best experience]**: De meeste deelnemers aan de activiteit worden automatisch omgeleid naar beter presterende ervaringen. Sommige bezoekers worden toegewezen aan alle ervaringen, om het verkennen van ervaringen te handhaven en veranderingen in prestatietrends te erkennen. Zie [[!UICONTROL Auto-Allocate] overview &#x200B;](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md#concept_A1407678796B4C569E94CBA8A9F7F5D4) voor meer informatie.

   * **[!UICONTROL Auto-Target for personalized experiences]**: [!DNL Target] maakt gebruik van geavanceerd leren van computers om inhoud en stationsomzettingen aan te passen door het identificeren van meerdere hoogwaardige, door markters gedefinieerde ervaringen en vervolgens de meest op maat gemaakte ervaring aan bezoekers te bieden op basis van hun individuele klantprofielen en eerdere gedragingen van vergelijkbare bezoekers. Voor meer informatie, zie [&#x200B; auto-Doel overzicht &#x200B;](/help/main/c-activities/auto-target/auto-target-to-optimize.md).

   Voor meer informatie en geleidelijke instructies, zie [&#x200B; een auto-Wijs activiteit &#x200B;](/help/main/c-activities/automated-traffic-allocation/create-auto-allocate-activity.md) en [&#x200B; creëren een auto-Doelactiviteit &#x200B;](/help/main/c-activities/auto-target/create-auto-target.md) toe.

1. Selecteer **[!UICONTROL Adobe Analytics]** voor uw **[!UICONTROL Reporting Source]** op de **[!UICONTROL Goals & Settings]** pagina, selecteer het bedrijf en rapportsuite die overeenkomen met uw gewenste optimalisatiedoel.

   ![&#x200B; Meldend de sectie van Source over Doelstellingen &amp; pagina van Montages &#x200B;](/help/main/c-integrating-target-with-mac/a4t/assets/a4t-select.png)

1. Geef de volgende server en sandbox op.

1. Kies een metrische waarde [!UICONTROL Primary Goal] .

   * Kies [!DNL Adobe Target] als u **[!UICONTROL Conversion]** wilt gebruiken om het optimalisatiedoel op te geven.
   * Kies **[!UICONTROL Use an Analytics metric]** en selecteer vervolgens een metrische waarde in [!DNL Analytics] voor gebruik als optimalisatiedoel. U kunt een uit-van-doos [!DNL Analytics] omzettingsmetrisch of een [!DNL Analytics] douanegebeurtenis gebruiken.

   Zie [&#x200B; Ondersteunde doelmetriek &#x200B;](#supported) hieronder voor meer informatie.

1. Sla uw activiteiten op en activeer deze.

   [!UICONTROL Auto-Allocate] gebruikt de geselecteerde metrische waarde om de activiteit te optimaliseren, zodat bezoekers de ervaring kunnen opdoen die uw doel metrisch maximaliseert.

   of

   [!UICONTROL Auto-Target] gebruikt de geselecteerde metrische waarde om de activiteit te optimaliseren, waardoor bezoekers naar een gepersonaliseerde beste ervaring kunnen gaan.

1. Gebruik het tabblad **[!UICONTROL Reports]** om de rapportage van uw activiteit weer te geven op basis van uw keuze voor [!DNL Adobe Analytics] -meetgegevens. Klik op **[!UICONTROL View in Analytics]** om uw rapportgegevens dieper en verder te segmenteren.

## Ondersteunde streefcijfers {#supported}

Met [!UICONTROL A4T] for [!UICONTROL Auto-Allocate] and [!UICONTROL Auto-Target] kunt u een van de volgende metrische typen kiezen als primaire doelmaateenheid voor optimalisatie:

* [!DNL Adobe Target] conversiewaarden
* [!DNL Adobe Analytics] conversiewaarden
* [!DNL Adobe Analytics] aangepaste gebeurtenissen

>[!NOTE]
>
>Nadat u [!UICONTROL Use an Analytics Metric] hebt geselecteerd, selecteert u [!UICONTROL Maximize Unique Visitor Conversion Rate] om de beschikbare [!DNL Adobe Analytics] conversiemetriek weer te geven en [!UICONTROL Maximize Metric Value per Visitor] om aangepaste gebeurtenissen te verkennen [!DNL Adobe Analytics] .

Met [!DNL Target] kunt u metrische gegevens kiezen op basis van binomiale gebeurtenissen of maatstaven op basis van doorlopende gebeurtenissen wanneer u [!UICONTROL A4T] for [!UICONTROL Auto-Allocate] - en [!UICONTROL Auto-Target] -activiteiten gebruikt.

* **Metriek die op binomiale gebeurtenissen** wordt gebaseerd: Een binomiale gebeurtenis of doet of gebeurt niet. Binomiale gebeurtenissen omvatten een klik, een omzetting, een orde, etc. Deze soorten gebeurtenissen worden ook soms bedoeld als Bernoulli, binaire, of discrete gebeurtenissen.

* **Metriek die op ononderbroken gebeurtenissen** wordt gebaseerd. De ononderbroken metriek omvat opbrengst, aantal geordende producten, zittingsduur, aantal paginameningen in zitting, etc. Deze gebeurtenissen worden ook wel niet-binomiale of niet-Bernoulli-metriek genoemd.

>[!IMPORTANT]
>
>Vanaf de release [!DNL Adobe Target Standard/Premium] 22.15.1 (8 en 9 maart 2023) blijft [!DNL Target] bestaande activiteiten ondersteunen met de metriek die nu niet wordt ondersteund (weergegeven in de volgende tabellen). Na 9 september 2023 zullen deze cijfers echter niet langer worden ondersteund in bestaande activiteiten en zullen alle activiteiten die niet-ondersteunde metriek gebruiken, worden stopgezet om de migratie van bestaande activiteiten naar het nieuwe gedrag te forceren.

### Effect op [!UICONTROL Auto-Allocate] -activiteiten

| Metrische naam | Niet meer ondersteund in: |
| --- | --- |
| [!UICONTROL averagepagedepth] | Conversiesnelheid, metrische waarde maximaliseren |
| [!UICONTROL averagetimespentonsite] | Conversiesnelheid, metrische waarde maximaliseren |
| [!UICONTROL bouncerate] | Conversiesnelheid, metrische waarde maximaliseren |
| [!UICONTROL bounces] | Conversiesnelheid, metrische waarde maximaliseren |
| [!UICONTROL entries] | Conversiesnelheid, metrische waarde maximaliseren |
| [!UICONTROL exits] | Conversiesnelheid, metrische waarde maximaliseren |
| [!UICONTROL pageviews] | Metrische waarde maximaliseren |
| [!UICONTROL reloads] | Metrische waarde maximaliseren |
| [!UICONTROL visitors] | Conversiesnelheid, metrische waarde maximaliseren |
| [!UICONTROL visits] | Metrische waarde maximaliseren |

### Effect op [!UICONTROL Auto-Target] -activiteiten

| Metrische naam | Niet meer ondersteund in: |
| --- | --- |
| [!UICONTROL cartremovals] | Metrische waarde maximaliseren |
| [!UICONTROL pageviews] | Metrische waarde maximaliseren |
| [!UICONTROL visitors] | Conversiesnelheid, metrische waarde maximaliseren |
| [!UICONTROL visits] | Metrische waarde maximaliseren |

## Beperkingen en opmerkingen

Sommige beperkingen en opmerkingen gelden voor zowel [!UICONTROL Auto-Allocate] - als [!UICONTROL Auto-Target] -activiteiten. Andere beperkingen en opmerkingen gelden voor het ene of het andere type activiteit.

### Automatische toewijzing en automatisch doel {#both}

* Wanneer u [!DNL Adobe Analytics] als rapportagebron voor [!UICONTROL Auto-Allocate] of [!UICONTROL Auto-Target] gebruikt, moet u rapporten altijd weergeven in [!DNL Analytics] .
* De rapportbron kan niet worden gewijzigd van [!DNL Analytics] in [!DNL Target] of andersom nadat een activiteit is geactiveerd.
* Hoewel de berekende metriek niet als primaire doelmetriek worden gesteund, is het vaak mogelijk om het voorgenomen resultaat te bereiken door in plaats daarvan een douanegebeurtenis als primaire doel metrisch te selecteren. Als u bijvoorbeeld wilt optimaliseren voor metrische gegevens, zoals &#39;formulieraanvullen per bezoeker&#39;, selecteert u een aangepaste gebeurtenis die overeenkomt met &#39;formulieraanvullen&#39; als maatstaf voor het primaire doel. [!DNL Target] normaliseert automatisch omzettingsmetriek op een per-bezoek basis om voor ongelijke verkeersdistributie rekening te houden, zodat is het niet noodzakelijk om berekende metrisch te gebruiken om normalisatie uit te voeren.

### Automatisch toewijzen {#aa}

* **de Frequentie van de Opleiding**: [!UICONTROL Auto-Allocate] de modellen blijven elk uur, zoals gebruikelijk trainen.
* **Modellen van de Attributie**: [!DNL Target] gebruikt het [!DNL Adobe Analytics] standaardattributiemodel voor [!UICONTROL &#x200B; Auto-Allocate] activiteiten die A4T gebruiken.
* **Vertrouwen**: De betrouwbaarheidsformule die door [!UICONTROL Auto-Allocate] activiteiten wordt gebruikt is verschillend van de formule die door gebrek in het [!DNL Adobe Analytics] wordt getoond [!UICONTROL A4T] paneel. [&#x200B; Zoals hier beschreven &#x200B;](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md), [!UICONTROL Auto-Allocate] gebruikt conservatievere betrouwbaarheidsintervallen dan regelmatige [!UICONTROL A/B Test] activiteiten. Deze conservatieve betrouwbaarheidsniveaus compenseren herhaalde evaluaties (peeks) op gegevens. Het standaardrapport in [!DNL Adobe Analytics] geeft dan ook kleinere betrouwbaarheidsintervallen weer dan de intervallen die worden gebruikt door het algoritme [!UICONTROL Auto-Allocate] . Desalniettemin kunt u bepalen welke ervaring door de algoritmen wordt bevorderd die op welke ervaring worden gebaseerd meer unieke bezoekers worden verzonden naar het.
* **Status van de Winner**: Momenteel, zijn de [&#x200B; &quot;Geen Winner nog&quot;en &quot;Winner&quot;badges &#x200B;](/help/main/c-activities/automated-traffic-allocation/determine-winner.md) niet beschikbaar in het [!UICONTROL A4T] paneel in [!DNL Analysis Workspace]. Deze badges zijn ook niet beschikbaar als hetzelfde rapport wordt weergegeven in [!DNL Target] . Een winnares-&quot;star&quot;-badge in een [!DNL Target] -rapport voor een [!UICONTROL Auto-Allocate] -activiteit met A4T moet worden genegeerd. Deze badge weerspiegelt regelmatige betrouwbaarheidsberekeningen, en niet die berekeningen die door [!UICONTROL Auto-Allocate] worden gebruikt.

### Automatisch doel {#at}

* [!UICONTROL Auto-Target] -modellen blijven elke 24 uur trainen, zoals gewoonlijk. De conversiegebeurtenisgegevens die afkomstig zijn uit [!DNL Analytics] worden echter met zes tot 24 uur vertraagd. Deze vertraging betekent dat het verkeer door [!DNL Target] wordt verdeeld over de meest recente gebeurtenissen die zijn opgenomen in [!DNL Analytics] . Deze vertraging heeft het grootste effect in de eerste 48 uur nadat een activiteit aanvankelijk wordt geactiveerd. De prestaties van de activiteit weerspiegelen het omzettingsgedrag [!DNL Analytics] na vijf dagen meer.

  Overweeg [!UICONTROL Auto-Allocate] in plaats van [!UICONTROL Auto-Target] te gebruiken voor activiteiten van korte duur waarbij het meeste verkeer plaatsvindt binnen de eerste vijf dagen van de levensduur van de activiteit.

* Wanneer u [!DNL Analytics] als gegevensbron voor een [!UICONTROL Auto-Target] -activiteit gebruikt, worden sessies beëindigd nadat zes uur zijn verstreken. Conversies die na zes uur plaatsvinden, worden niet geteld.

Voor meer informatie, zie [&#x200B; modellen van de Attributie en raadplegingsvensters &#x200B;](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/attribution/models.html?lang=nl-NL) in de *Gids van de Hulpmiddelen van de Analyse*.

## Tutorials

Hoewel uitgebreide analysemogelijkheden beschikbaar zijn in [!DNL Adobe Analytics] [!UICONTROL Analysis Workspace] , zijn enkele wijzigingen in het standaard [!UICONTROL Analytics for Target] -deelvenster vereist voor een juiste interpretatie van [!UICONTROL Auto-Allocate] - en [!UICONTROL Auto-Target] -activiteiten. Deze wijzigingen zijn vereist vanwege verschillen tussen experimentele activiteiten (handleiding A/B en [!UICONTROL Auto-Allocate]) en personalisatieactiviteiten ([!UICONTROL Auto-Target]).

### A4T-rapporten instellen in [!DNL Analysis Workspace] voor [!UICONTROL Auto-Allocate] -activiteiten

In deze zelfstudie worden de aanbevolen wijzigingen voor het analyseren van [!UICONTROL Auto-Allocate] -activiteiten in [!DNL Analysis Workspace] besproken.

Voor meer informatie, zie [&#x200B; hoe te opstelling A4T rapporten in Analysis Workspace voor auto-Wijs activiteiten &#x200B;](https://experienceleague.adobe.com/docs/target-learn/tutorials/integrations/set-up-a4t-reports-in-analysis-workspace-for-auto-allocate-activities.html?lang=nl-NL){target=_blank} in *Zelfstudies van Adobe Target* toe.

### A4T-rapporten instellen in [!DNL Analysis Workspace] voor [!UICONTROL Auto-Target] -activiteiten

In deze zelfstudie worden de aanbevolen wijzigingen voor het analyseren van [!UICONTROL Auto-Target] -activiteiten in [!DNL Analysis Workspace] besproken.

Voor meer informatie, zie [&#x200B; hoe te opstelling A4T rapporten in Analysis Workspace voor activiteiten Auto-Doel &#x200B;](https://experienceleague.adobe.com/docs/target-learn/tutorials/integrations/set-up-a4t-reports-in-analysis-workspace-for-auto-target-activities.html?lang=nl-NL){target=_blank} in *Zelfstudies van Adobe Target*.


