---
keywords: a4t;A4T;Analyses als bron voor rapportage voor Doel;analytische gegevens voor doel
description: Leer hoe u creeert [!UICONTROL Auto-Allocate] en [!UICONTROL Auto-Target] activiteiten in [!DNL Target] die [!DNL Analytics] als bron van rapportage (A4T).
title: Biedt ondersteuning voor A4T [!UICONTROL Auto-Allocate] en [!UICONTROL Auto-Target] Activiteiten?
feature: Analytics for Target (A4T)
exl-id: 3302f26d-c445-4779-8435-be142d5cea8c
source-git-commit: 99bd509988a7d1545a6a1fe59aa59f35ef0a7d11
workflow-type: tm+mt
source-wordcount: '1169'
ht-degree: 0%

---

# A4T-ondersteuning voor [!UICONTROL Auto-Allocate] en [!UICONTROL Auto-Target] activiteiten

De [!DNL Adobe Target]-to-[!DNL Adobe Analytics] integratie, bekend als [Analyses voor doel](/help/main/c-integrating-target-with-mac/a4t/a4t.md) (A4T), ondersteunt [!UICONTROL Auto-Allocate] en [!UICONTROL Auto-Target] activiteiten.

Met de integratie A4T kunt u:

* Gebruik de [Automatisch toewijzen](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md) meervoudig bewapende bankencapaciteit om verkeer naar het winnen van ervaringen te drijven.
* Gebruik de [Automatisch doel](/help/main/c-activities/auto-target/auto-target-to-optimize.md) Hiermee zorgt u ervoor dat een computerleeralgoritme de beste ervaring voor elke bezoeker kan kiezen. [!UICONTROL Auto-Target] kiest u de beste ervaring op basis van het profiel, het gedrag en de context van elke gebruiker tijdens het gebruik van een [!DNL Adobe Analytics] doelstelling metrisch en de rijke rapportering en analysemogelijkheden van [!DNL Adobe Analytics].

Zorg ervoor dat u [geïmplementeerde A4T voor gebruik met A/B test- en ervaringsgerichte activiteiten](/help/main/c-integrating-target-with-mac/a4t/a4timplementation.md). Als u `analyticsLogging = client_side`, moet u ook `sessionId` waarde aan [!DNL Analytics]. Zie voor meer informatie [Analyses voor doelrapportage (A4T)](https://experienceleague.adobe.com/docs/target-dev/developer/server-side/integration/a4t-reporting.html){target=_blank} in de *Adobe Target Developer Guide*.

Aan de slag:

1. while [een [!UICONTROL A/B Test] activiteit](/help/main/c-activities/t-test-ab/t-test-create-ab/test-create-ab.md)over de **[!UICONTROL Targeting]** pagina, selecteert u een van de volgende opties als de **[!UICONTROL Traffic Allocation Method]**:

   * [!UICONTROL Auto-Allocate to best experience]
   * [!UICONTROL Auto-Target for personalized experiences]

   ![Opties voor verkeerstoewijzingsmethoden: Handmatig, automatisch toegewezen en automatisch doel](/help/main/c-integrating-target-with-mac/a4t/assets/traffic-allocation-methods.png)

   Voor meer informatie en stapsgewijze instructies raadpleegt u [Een activiteit voor automatisch toewijzen maken](/help/main/c-activities/automated-traffic-allocation/create-auto-allocate-activity.md) en [Een automatisch doelactiviteit maken](/help/main/c-activities/auto-target/create-auto-target.md).

1. Selecteren **[!UICONTROL Adobe Analytics]** voor uw **[!UICONTROL Reporting Source]** op de **[!UICONTROL Goals & Settings]** en selecteer de rapportsuite die overeenkomt met uw gewenste optimalisatiedoel.

   ![Sectie Bron rapporteren op pagina Doelstellingen en instellingen](/help/main/c-integrating-target-with-mac/a4t/assets/a4t-select.png)

1. Kies een [!UICONTROL Primary Goal] metrisch.

   * Te gebruiken [!DNL Adobe Target] om het optimalisatiedoel op te geven, kiest u **[!UICONTROL Conversion]** .
   * Kies **[!UICONTROL Use an Analytics metric]** en selecteer dan metrisch van [!DNL Analytics] voor gebruik als optimalisatiedoel. U kunt een uit-van-doos gebruiken [!DNL Analytics] conversiemetrisch of [!DNL Analytics] aangepaste gebeurtenis.

   Zie [Ondersteunde streefcijfers](#supported) hieronder voor meer informatie .

1. Sla uw activiteiten op en activeer deze.

   [!UICONTROL Auto-Allocate] gebruikt uw geselecteerde metrisch om de activiteit te optimaliseren, die bezoekers aan de ervaring drijven die uw doel metrisch maximaliseert.

   of

   [!UICONTROL Auto-Target] gebruikt de geselecteerde metrische waarde om de activiteit te optimaliseren, zodat bezoekers naar een persoonlijke beste ervaring kunnen gaan.

1. Gebruik de **[!UICONTROL Reports]** om de rapportage van uw activiteit weer te geven op basis van uw keuze uit [!DNL Adobe Analytics] metriek. Klikken **[!UICONTROL View in Analytics]** om diep te duiken en verder te segmenteren uw rapporteringsgegevens.

## Ondersteunde streefcijfers {#supported}

[!UICONTROL A4T] for [!UICONTROL Auto-Allocate] en [!UICONTROL Auto-Target] laat u om het even welke volgende metrische types als uw primaire doel metrisch voor optimalisering kiezen:

* [!DNL Adobe Target] conversiemetingen
* [!DNL Adobe Analytics] conversiemetingen
* [!DNL Adobe Analytics] aangepaste gebeurtenissen

[!DNL Target] Hiermee kunt u metriek kiezen op basis van binomiale gebeurtenissen of metriek op basis van doorlopende gebeurtenissen wanneer u [!UICONTROL A4T] for [!UICONTROL Auto-Allocate] en [!UICONTROL Auto-Target] activiteiten.

* **Metriek gebaseerd op binomiale gebeurtenissen**: Een binomiale gebeurtenis doet of gebeurt niet. Binomiale gebeurtenissen omvatten een klik, een omzetting, een orde, etc. Deze soorten gebeurtenissen worden ook soms bedoeld als Bernoulli, binaire, of discrete gebeurtenissen.

* **Metriek gebaseerd op continue gebeurtenissen**. De ononderbroken metriek omvat opbrengst, aantal geordende producten, zittingsduur, aantal paginameningen in zitting, etc. Deze gebeurtenissen worden ook wel niet-binomiale of niet-Bernoulli-metriek genoemd.

>[!IMPORTANT]
>
>Vanaf de [!DNL Adobe Target Standard/Premium] release van 22.15.1 (8 en 9 maart 2023), [!DNL Target] bestaande activiteiten blijven ondersteunen met de meetwaarden die nu niet worden ondersteund (weergegeven in de volgende tabellen). Na 9 september 2023 zullen deze cijfers echter niet langer worden ondersteund in bestaande activiteiten en zullen alle activiteiten die niet-ondersteunde metriek gebruiken, worden stopgezet om de migratie van bestaande activiteiten naar het nieuwe gedrag te forceren.

### Gevolgen voor [!UICONTROL Auto-Allocate] activiteiten

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

### Gevolgen voor [!UICONTROL Auto-Target] activiteiten

| Metrische naam | Niet meer ondersteund in: |
| --- | --- |
| [!UICONTROL cartremovals] | Metrische waarde maximaliseren |
| [!UICONTROL pageviews] | Metrische waarde maximaliseren |
| [!UICONTROL visitors] | Conversiesnelheid, metrische waarde maximaliseren |
| [!UICONTROL visits] | Metrische waarde maximaliseren |

## Beperkingen en opmerkingen

Sommige beperkingen en opmerkingen zijn van toepassing op beide [!UICONTROL Auto-Allocate] en [!UICONTROL Auto-Target] activiteiten. Andere beperkingen en opmerkingen gelden voor het ene of het andere type activiteit.

### Automatische toewijzing en automatisch doel {#both}

* Wanneer u [!DNL Adobe Analytics] als bron van rapportage voor [!UICONTROL Auto-Allocate] of [!UICONTROL Auto-Target], moet u rapporten altijd weergeven in [!DNL Analytics].
* De rapportbron kan niet worden gewijzigd vanaf [!DNL Analytics] tot [!DNL Target] of omgekeerd nadat een activiteit is geactiveerd.
* Hoewel de berekende metriek niet als primaire doelmetriek worden gesteund, is het vaak mogelijk om het voorgenomen resultaat te bereiken door in plaats daarvan een douanegebeurtenis als primaire doel metrisch te selecteren. Als u bijvoorbeeld wilt optimaliseren voor metrische gegevens, zoals &#39;formulieraanvullen per bezoeker&#39;, selecteert u een aangepaste gebeurtenis die overeenkomt met &#39;formulieraanvullen&#39; als maatstaf voor het primaire doel. [!DNL Target] normaliseert automatisch omzettingsmetriek op een per-bezoek basis om voor ongelijke verkeersdistributie rekening te houden, zodat is het niet noodzakelijk om berekende metrisch te gebruiken om normalisatie uit te voeren.

### Automatisch toewijzen {#aa}

* **Trainingsfrequentie**: [!UICONTROL Auto-Allocate] de modellen blijven ieder uur trainen , zoals gewoonlijk .
* **Attributiemodellen**: [!DNL Target] gebruikt de [!DNL Adobe Analytics] standaardtoewijzingsmodel voor[!UICONTROL  Auto-Allocate] activiteiten die gebruikmaken van A4T.
* **Vertrouwen**: De betrouwbaarheidsformule die wordt gebruikt door [!UICONTROL Auto-Allocate] de activiteiten verschillen van de standaard in de [!DNL Adobe Analytics] [!UICONTROL A4T] deelvenster. [Zoals hier beschreven](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md), [!UICONTROL Auto-Allocate] gebruikt meer conservatieve betrouwbaarheidsintervallen dan normaal [!UICONTROL A/B Test] activiteiten. Deze conservatieve betrouwbaarheidsniveaus compenseren herhaalde evaluaties (peeks) op gegevens. Dientengevolge, het standaardrapport binnen [!DNL Adobe Analytics] geeft lagere betrouwbaarheidsintervallen weer in vergelijking met de intervallen die door de [!UICONTROL Auto-Allocate] algoritme. Desalniettemin kunt u bepalen welke ervaring door de algoritmen wordt bevorderd die op welke ervaring worden gebaseerd meer unieke bezoekers worden verzonden naar het.
* **Winkelstatus**: Op dit moment worden de [&quot;Nog geen Winner&quot; en &quot;Winner&quot; badges](/help/main/c-activities/automated-traffic-allocation/determine-winner.md) zijn niet beschikbaar in het dialoogvenster [!UICONTROL A4T] in [!DNL Analysis Workspace]. Deze badges zijn ook niet beschikbaar als hetzelfde rapport wordt weergegeven in [!DNL Target]. Een winnares-&quot;ster&quot;-badge weergegeven in een [!DNL Target] verslag voor een [!UICONTROL Auto-Allocate] activiteit die A4T gebruikt zou moeten worden genegeerd. Deze badge weerspiegelt regelmatige vertrouwensberekeningen en niet de berekeningen die door [!UICONTROL Auto-Allocate].

### Automatisch doel {#at}

* [!UICONTROL Auto-Target] de modellen blijven elke 24 uur trainen , zoals gewoonlijk . Omzetgebeurtenisgegevens die echter afkomstig zijn van [!DNL Analytics] 6 tot 24 uur later. Deze vertraging betekent de verdeling van het verkeer door [!DNL Target] traceert de meest recente gebeurtenissen die zijn opgenomen in [!DNL Analytics]. Deze vertraging heeft het grootste effect in de eerste 48 uur nadat een activiteit aanvankelijk wordt geactiveerd. De prestaties van de activiteit zijn beter te spiegelen [!DNL Analytics] omzettingsgedrag na vijf dagen is verstreken.

   Gebruik [!UICONTROL Auto-Allocate] in plaats van [!UICONTROL Auto-Target] voor kortdurende activiteiten waarbij het meeste verkeer plaatsvindt binnen de eerste vijf dagen van de levensduur van de activiteit.

* Wanneer u [!DNL Analytics] als gegevensbron voor een [!UICONTROL Auto-Target] activiteit, sessies eindigen nadat zes uur zijn verstreken. Conversies die na zes uur plaatsvinden, worden niet geteld.

Zie voor meer informatie [Attributiemodellen en terugzoekvensters](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/attribution/models.html) in de *Handleiding Analysehulpmiddelen*.

## Tutorials

Hoewel uitgebreide analysemogelijkheden beschikbaar zijn in [!DNL Adobe Analytics] [!UICONTROL Analysis Workspace], enkele wijzigingen in de standaardwaarde [!UICONTROL Analytics for Target] het deelvenster moet correct worden geïnterpreteerd [!UICONTROL Auto-Allocate] en [!UICONTROL Auto-Target] activiteiten. Deze wijzigingen zijn nodig vanwege verschillen tussen experimentele activiteiten (handleiding A/B en [!UICONTROL Auto-Allocate]) en personaliseringsactiviteiten ([!UICONTROL Auto-Target]).

### A4T-rapporten instellen in [!DNL Analysis Workspace] for [!UICONTROL Auto-Allocate] activiteiten

In deze zelfstudie worden de aanbevolen wijzigingen voor het analyseren van [!UICONTROL Auto-Allocate] activiteiten in [!DNL Analysis Workspace].

Zie voor meer informatie [A4T-rapporten instellen in Analysis Workspace voor activiteiten automatisch toewijzen](https://experienceleague.adobe.com/docs/target-learn/tutorials/integrations/set-up-a4t-reports-in-analysis-workspace-for-auto-allocate-activities.html){target=_blank} in *Adobe Target Tutorials*.

### A4T-rapporten instellen in [!DNL Analysis Workspace] for [!UICONTROL Auto-Target] activiteiten

In deze zelfstudie worden de aanbevolen wijzigingen voor het analyseren van [!UICONTROL Auto-Target] activiteiten in [!DNL Analysis Workspace].

Zie voor meer informatie [A4T-rapporten instellen in Analysis Workspace voor Auto-Target-activiteiten](https://experienceleague.adobe.com/docs/target-learn/tutorials/integrations/set-up-a4t-reports-in-analysis-workspace-for-auto-target-activities.html){target=_blank} in *Adobe Target Tutorials*.


