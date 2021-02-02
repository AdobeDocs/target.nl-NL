---
keywords: a4t;A4T;Analyse als bron voor rapportage voor Target
description: Kan ik A4T met auto-Doel en auto-Wijs activiteiten gebruiken?
title: A4T-ondersteuning voor activiteiten voor automatisch toewijzen en automatisch richten
feature: Analytics for Target (A4T)
translation-type: tm+mt
source-git-commit: 4f0f1df1bcb6baad0e20c4dc1ae7e12751080d91
workflow-type: tm+mt
source-wordcount: '787'
ht-degree: 0%

---


# A4T-ondersteuning voor activiteiten voor automatisch toewijzen en automatisch richten

De integratie [!DNL Adobe Target]-aan-[!DNL Adobe Analytics], die als [Analytics voor Doel wordt bekend](/help/c-integrating-target-with-mac/a4t/a4t.md) (A4T) steunt [!UICONTROL Auto-Allocate] en [!UICONTROL Auto-Target] activiteiten.

Met de integratie A4T kunt u:

* Gebruik [Automatische toewijzing](/help/c-activities/automated-traffic-allocation/automated-traffic-allocation.md)&#39;s meervoudige bewapende bandcapaciteit om verkeer naar het winnen van ervaringen te drijven.
* Gebruik [Auto-Target](/help/c-activities/auto-target/auto-target-to-optimize.md)&#39;s ensemble machine learning algorithm om een beste ervaring te kiezen voor elke bezoeker op basis van zijn profiel, gedrag en context, en dit alles terwijl u een [!DNL Adobe Analytics] target-metrische en [!DNL Adobe Analytics]&#39; rijke rapportage- en analysemogelijkheden gebruikt.

Zorg ervoor dat u [A4T voor gebruik met A/B Test en Ervaring gerichte activiteiten](/help/c-integrating-target-with-mac/a4t/a4timplementation.md) hebt uitgevoerd. Als u `analyticsLogging = client_side` gebruikt, moet u ook `sessionId` waarde tot [!DNL Analytics] overgaan. Zie [Analytics for Target (A4T) reporting](https://adobetarget-sdks.gitbook.io/docs/integration-with-experience-cloud/analytics-for-target-a4t-reporting) in de handleiding *Adobe Target SDKs* voor meer informatie.

Aan de slag:

1. Selecteer op de pagina **[!UICONTROL Targeting]** een van de volgende opties als **[!UICONTROL Traffic Allocation Method]** tijdens het maken van een A/B-testactiviteit:

   * [!UICONTROL Auto-allocate to best experience]
   * [!UICONTROL Auto-target for personalized experiences]

   ![Opties voor verkeerstoewijzingsmethoden: Handmatig, automatisch toegewezen en automatisch doel](/help/c-integrating-target-with-mac/a4t/assets/traffic-allocation-methods.png)

   Zie [Een activiteit voor automatisch toewijzen maken](/help/c-activities/automated-traffic-allocation/create-auto-allocate-activity.md) en [Een activiteit voor automatisch doel maken](/help/c-activities/auto-target/create-auto-target.md) voor meer informatie en stapsgewijze instructies.

1. Selecteer **[!UICONTROL Adobe Analytics]** voor uw **[!UICONTROL Reporting Source]** op **[!UICONTROL Goals & Settings]** pagina en selecteer de rapportreeks die aan uw gewenste optimaliseringsdoel beantwoordt.

1. Kies een maatstaf voor het primaire doel.

   * Kies **[!UICONTROL Conversion]** om [!DNL Adobe Target] te gebruiken om het optimalisatiedoel te specificeren.
   * Kies **[!UICONTROL Use an Analytics metric]** en selecteer dan metrisch van [!DNL Analytics] voor gebruik als optimalisatiedoel. U kunt een uit-van-doos [!DNL Analytics] omzettingsmetrisch of [!DNL Analytics] douanegebeurtenis gebruiken.

1. Sla uw activiteiten op en activeer deze.

   [!UICONTROL Auto-Allocate] zal uw geselecteerde metrisch gebruiken om de activiteit te optimaliseren, die bezoekers aan de ervaring drijft die uw doel metrisch maximaliseert.

   of

   [!UICONTROL Auto-Target] zal uw geselecteerde metrische waarde gebruiken om de activiteit te optimaliseren, bezoekers naar een gepersonaliseerde beste ervaring drijven.

1. Gebruik het tabblad **[!UICONTROL Reports]** om de rapportage van uw activiteit weer te geven op basis van uw keuze voor [!DNL Adobe Analytics]-meetwaarden. Klik op **[!UICONTROL View in Analytics]** om uw rapportgegevens diepgaand en verder te segmenteren.

## Ondersteunde streefcijfers

[!UICONTROL A4T] voor  [!UICONTROL Auto-Allocate] en  [!UICONTROL Auto-Target] laat u om het even welke volgende metrische types als uw primaire doel metrisch voor optimalisering kiezen:

* [!DNL Adobe Target] conversiemetingen
* [!DNL Adobe Analytics] conversiemetingen
* [!DNL Adobe Analytics] aangepaste gebeurtenissen

[!UICONTROL A4T] voor  [!UICONTROL Auto-Allocate] en  [!UICONTROL Auto-Target] vereist u om metrisch te kiezen die op een binomiale gebeurtenis gebaseerd is, namelijk een gebeurtenis die of gebeurt of niet, bijvoorbeeld een klik, een omzetting, een orde, enz. Deze soorten gebeurtenissen worden ook soms bedoeld als Bernoulli, binaire, of discrete gebeurtenissen.

[!UICONTROL A4T] voor  [!UICONTROL Auto-Allocate] en  [!UICONTROL Auto-Target] ondersteunt geen optimalisatie voor doorlopende metingen, zoals opbrengst, aantal bestelde producten, sessieduur, aantal paginaweergaven tijdens sessies, enz. Deze niet-ondersteunde typen metriek worden ook wel niet-binomiale of niet-Bernoulli-metriek genoemd.

De volgende metrische types zijn niet gesteund als primaire doelmetriek:

* [!DNL Adobe Target] service- en inkomstencijfers
* [!DNL Adobe Analytics] service- en inkomstencijfers

   Het kan mogelijk zijn om een [!DNL Analytics] betrokkenheid of opbrengstmetrisch als uw primaire doel metrisch te selecteren omdat [!DNL Target] niet alle overeenkomst en opbrengstmetriek van [!DNL Analytics] kan identificeren en uitsluiten. Wees voorzichtig met het selecteren van alleen binomiale conversiemetriek of aangepaste gebeurtenissen van [!DNL Analytics].

* [!DNL Adobe Analytics] berekende meetwaarden

## Beperkingen en opmerkingen

Sommige beperkingen en opmerkingen gelden voor zowel [!UICONTROL Auto-Allocate]- als [!UICONTROL Auto-Target]-activiteiten. Andere beperkingen en opmerkingen gelden voor het ene of het andere type activiteit.

### Automatische toewijzing en automatisch doel

* De rapportbron kan niet worden gewijzigd van [!DNL Analytics] in [!DNL Target] of vice versa nadat een activiteit is geactiveerd.
* Hoewel de berekende metriek niet als primaire doelmetriek worden gesteund, is het vaak mogelijk om het voorgenomen resultaat te bereiken door in plaats daarvan een douanegebeurtenis als primaire doel metrisch te selecteren. Als u bijvoorbeeld wilt optimaliseren voor metrische gegevens, zoals &#39;formulieraanvullen per bezoeker&#39;, selecteert u een aangepaste gebeurtenis die overeenkomt met &#39;formulieraanvullen&#39; als maatstaf voor het primaire doel. [!DNL Target] normaliseert automatisch omzettingsmetriek op een per-bezoek basis om voor ongelijke verkeersdistributie rekening te houden, zodat is het niet noodzakelijk om berekende metrisch te gebruiken om normalisatie uit te voeren.
* [!DNL Target] gebruikt het attribuutmodel &quot;Same Touch&quot; in de  [!UICONTROL Auto-Allocate] functie: Analyses voor Doel (A4T).

### Automatisch toewijzen

* [!UICONTROL Auto-Allocate] de modellen blijven elke twee uur trainen , zoals gewoonlijk .

### Automatisch doel

* [!UICONTROL Auto-Target] de modellen blijven elke 24 uur trainen , zoals gewoonlijk . De conversiegebeurtenisgegevens die afkomstig zijn van [!DNL Analytics] worden echter met nog eens zes tot 24 uur vertraagd. Deze vertraging betekent de verdeling van verkeer door [!DNL Target] zal de recentste gebeurtenissen volgen die in [!DNL Analytics] worden geregistreerd. Dit heeft het grootste effect in de eerste 48 uur nadat een activiteit voor het eerst is geactiveerd. De prestaties van de activiteit weerspiegelen het omzettingsgedrag [!DNL Analytics] na vijf dagen verstreken zijn. U zou moeten overwegen [!UICONTROL Auto-Allocate] in plaats van [!UICONTROL Auto-Target] voor kortdurende activiteiten te gebruiken waarin het meeste verkeer binnen de eerste vijf dagen van het leven van de activiteit voorkomt.
* Wanneer u [!DNL Analytics] als gegevensbron voor een [!UICONTROL Auto-Target] activiteit gebruikt, worden de zittingen beschouwd als om na zes uren zijn verlopen. Conversies die na zes uur plaatsvinden, worden niet geteld.

Voor meer informatie, zie [Attributiemodellen en terugkijkvensters](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/attribution/models.html) in *de Gids van de Hulpmiddelen van Analytics*.
