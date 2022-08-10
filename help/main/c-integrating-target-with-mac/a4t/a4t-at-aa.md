---
keywords: a4t;A4T;Analyse als bron voor rapportage voor Target
description: Leer hoe u Auto-Allocate- en Auto-Target-activiteiten maakt in Adobe [!DNL Target] die Analytics als rapportagebron (A4T) gebruiken.
title: Biedt A4T ondersteuning voor automatisch toegewezen en automatisch doelgerichte activiteiten?
feature: Analytics for Target (A4T)
exl-id: 3302f26d-c445-4779-8435-be142d5cea8c
source-git-commit: e8fc28ef2497c1dfea523a769c9c817cbd74fea2
workflow-type: tm+mt
source-wordcount: '1624'
ht-degree: 0%

---

# A4T-ondersteuning voor activiteiten voor automatisch toewijzen en automatisch richten

De [!DNL Adobe Target]-to-[!DNL Adobe Analytics] integratie, bekend als [Analyses voor doel](/help/main/c-integrating-target-with-mac/a4t/a4t.md) (A4T)-ondersteuning [!UICONTROL Auto-Allocate] en [!UICONTROL Auto-Target] activiteiten.

Met de integratie A4T kunt u:

* Gebruiken [Automatisch toewijzen](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md)De multi-gewapende bandemogelijkheid van de bank om verkeer naar het winnen van ervaringen te drijven.
* Gebruiken [Automatisch doel](/help/main/c-activities/auto-target/auto-target-to-optimize.md)Het ensemble Machine Learning-algoritme van de gebruiker om een beste ervaring voor elke bezoeker te kiezen. Auto-Target kiest de beste ervaring gebaseerd op gebruikersprofielen, gedrag, en context allen terwijl het gebruiken van [!DNL Adobe Analytics] doel metrisch en [!DNL Adobe Analytics]&quot; rijke rapportage- en analysemogelijkheden.

Zorg ervoor dat u [geïmplementeerde A4T voor gebruik met A/B test- en ervaringsgerichte activiteiten](/help/main/c-integrating-target-with-mac/a4t/a4timplementation.md). Als u `analyticsLogging = client_side`, moet u ook `sessionId` waarde aan [!DNL Analytics]. Zie voor meer informatie [Analyses voor doelrapportage (A4T)](https://developer.adobe.com/target/implement/server-side/sdk-guides/integration-with-experience-cloud/a4t-reporting/){target=_blank} in het dialoogvenster *Adobe Target SDK&#39;s* hulplijn.

Aan de slag:

1. Tijdens het maken van een A/B-testactiviteit, kunt u op de knop **[!UICONTROL Targeting]** pagina, selecteert u een van de volgende opties als de **[!UICONTROL Traffic Allocation Method]**:

   * [!UICONTROL Auto-Allocate to best experience]
   * [!UICONTROL Auto-Target for personalized experiences]

   ![Opties voor verkeerstoewijzingsmethoden: Handmatig, automatisch toegewezen en automatisch doel](/help/main/c-integrating-target-with-mac/a4t/assets/traffic-allocation-methods.png)

   Voor meer informatie en stapsgewijze instructies raadpleegt u [Een activiteit voor automatisch toewijzen maken](/help/main/c-activities/automated-traffic-allocation/create-auto-allocate-activity.md) en [Een automatisch doelactiviteit maken](/help/main/c-activities/auto-target/create-auto-target.md).

1. Selecteren **[!UICONTROL Adobe Analytics]** voor uw **[!UICONTROL Reporting Source]** op de **[!UICONTROL Goals & Settings]** en selecteer de rapportsuite die overeenkomt met uw gewenste optimalisatiedoel.

   ![Sectie Bron rapporteren op pagina Doelstellingen en instellingen](/help/main/c-integrating-target-with-mac/a4t/assets/a4t-select.png)

1. Kies een maatstaf voor het primaire doel. In het eerste vervolgkeuzemenu kunt u een van de twee doelen opgeven in [!DNL Adobe Target] (die vervolgens worden gevolgd door [!DNL Adobe Analytics] als de metrische &quot;Activiteitenomzettingen&quot;), of, om een [!DNL Analytics] metrisch als uw doel.

   * Te gebruiken [!DNL Adobe Target] om het optimalisatiedoel op te geven, kiest u **[!UICONTROL Conversion]** en geeft u vervolgens de actie op die door het publiek moet worden uitgevoerd om aan te geven dat het conversiedoel is bereikt.
   * Als u in plaats daarvan **[!UICONTROL Use an Analytics metric]** U kunt dan kiezen welk optimalisatiecriterium moet worden gebruikt.  Zie [Ondersteunde streefwaarden en optimalisatiecriteria](#supported) hieronder voor meer informatie . Nadat u het optimalisatiecriterium hebt opgegeven, kunt u een compatibele metrische waarde selecteren in [!DNL Analytics] voor gebruik als optimalisatiedoel. U kunt een uit-van-doos gebruiken [!DNL Analytics] conversiemetrisch of [!DNL Analytics] aangepaste gebeurtenis.


1. Sla uw activiteiten op en activeer deze.

   [!UICONTROL Auto-Allocate] gebruikt uw geselecteerde metrisch om de activiteit te optimaliseren, die bezoekers aan de ervaring drijven die uw doel metrisch maximaliseert.

   of

   [!UICONTROL Auto-Target] gebruikt de geselecteerde metrische waarde om de activiteit te optimaliseren, zodat bezoekers naar een persoonlijke beste ervaring kunnen gaan.

1. Gebruik de **[!UICONTROL Reports]** om de rapportage van uw activiteit weer te geven en klik op **[!UICONTROL View in Analytics]** om diep en verder te segmenteren uw rapportgegevens in een Adobe Analytics Workspace. U kunt de onderstaande zelfstudies volgen om te zien hoe u rapporten instelt in Workspace:
* Automatisch toewijzen: zie [A4T-rapporten instellen in Analysis Workspace voor activiteiten automatisch toewijzen](https://experienceleague.adobe.com/docs/target-learn/tutorials/integrations/set-up-a4t-reports-in-analysis-workspace-for-auto-target-activities.html) in *Adobe Target Tutorials*
* Automatisch doel: zie [A4T-rapporten instellen in Analysis Workspace voor Auto-Target-activiteiten](https://experienceleague.adobe.com/docs/target-learn/tutorials/integrations/set-up-a4t-reports-in-analysis-workspace-for-auto-target-activities.html) in *Adobe Target Tutorials*.

## Ondersteunde streefwaarden en optimalisatiecriteria {#supported}

[!UICONTROL A4T] for [!UICONTROL Auto-Allocate] en [!UICONTROL Auto-Target] laat u om het even welke volgende metrische types als uw primaire doel metrisch voor optimalisering kiezen:

* [!DNL Adobe Target] conversiemetingen
* [!DNL Adobe Analytics] conversiemetingen
* [!DNL Adobe Analytics] aangepaste gebeurtenissen

Maar [!UICONTROL Auto-Allocate] en [!UICONTROL Auto-Target] modellen worden geoptimaliseerd voor **genormaliseerd** versies van deze metriek, met de nauwkeurige normalisatie afhankelijk van het type van activiteit. De opties voor optimalisatiecriteria voor elk type activiteit worden in de onderstaande tabel uitgelegd:

| Type activiteit | Metrische bron | Optimalisatiecriterium | Beschrijving |
|---------------|---------------|-----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Automatisch toewijzen | Analyse | Unieke conversiesnelheid bezoeker maximaliseren | Modellen proberen de Experience te vinden met de hoogste unieke conversiesnelheid voor bezoekers, die wordt gedefinieerd als het aantal bezoekers voor wie de meetwaarde voor de analyse niet gelijk is aan nul, gedeeld door het totale aantal bezoekers (die deze ervaring hebben ontvangen). Dit betekent dat metrisch als binair wordt behandeld - of 0, of 1 voor elke unieke bezoeker in de activiteit.   Gebruik deze optie als u alleen om het deel van de gebruikers die een bepaalde actie uitvoeren of als meerdere conversiegebeurtenissen voor één gebruiker van betekenis zijn. |
| Automatisch toewijzen | Analyse | Metrische waarde maximaliseren per bezoeker | De modellen proberen om de Ervaring met de hoogste metrische waarde per bezoeker te vinden, die wordt bepaald als de totale waarde van metrisch voor alle gebruikers die aan die Ervaring worden blootgesteld, gedeeld door het totale aantal bezoekers die die Ervaring ontvingen. Dit betekent dat de metrische waarde elke waarde kan hebben voor elke unieke bezoeker in de activiteit. Als een bezoeker bijvoorbeeld meerdere keren converteert, wordt elke conversie geteld.  Gebruik deze optie als u in het maximaliseren van ononderbroken metrisch als totale opbrengst geinteresseerd bent, of als de veelvoudige omzettingsgebeurtenissen voor één enkele gebruiker zinvoller zijn dan één (b.v. de veelvoudige orden zijn waardevoller dan één) |
| Automatisch toewijzen | Doel | (niet configureerbaar) | Metrisch wordt behandeld als binair, en het unieke tarief van de bezoekersomzetting wordt gemaximaliseerd. |
| Automatisch doel | Analyse | Unieke conversiesnelheid bezoek maximaliseren | In tegenstelling tot autotoewijzing of handmatige A/B tests, betekent de gepersonaliseerde aard van auto-doel dat de Ervaring een bezoeker ziet voor elk nieuw bezoek kan veranderen. De juiste koers is dan een op bezoek genormaliseerde omrekeningskoers, die wordt gedefinieerd als het deel van de bezoeken waarin een niet-nulmeting wordt geregistreerd. Dit is de conversiesnelheid die wordt geoptimaliseerd door Auto-target.   Net als bij Automatisch toewijzen moet deze optie worden gekozen wanneer u om het gedeelte van de bezoeken geeft waar een conversie plaatsvindt, dat wil zeggen wanneer meerdere conversiegebeurtenissen die zich voordoen voor een enkel bezoek niet belangrijk zijn. |
| Automatisch doel | Analyse | Metrische waarde maximaliseren per bezoek | Wanneer metrisch die voor ononderbroken (b.v. opbrengst) wordt geoptimaliseerd is, of wanneer de aanwezigheid van veelvoudige omzettingsgebeurtenissen in één enkel bezoek zinvol is (b.v. veelvoudige orden), kunt u verkiezen om de metrische waarde per bezoek te maximaliseren. De &quot;snelheid&quot; die wordt geoptimaliseerd, is de totale waarde van de maatstaf, gedeeld door het aantal bezoeken. |
| Automatisch doel | Doel | (niet configureerbaar) | Metrisch wordt behandeld als binair, en het unieke tarief van de bezoekomzetting wordt gemaximaliseerd. |



Let erop dat, afhankelijk van het optimalisatiecriterium, bepaalde [!DNL Adobe Analytics] metriek wordt niet ondersteund.

* [!DNL Adobe Analytics] berekende meetwaarden worden niet ondersteund.
* [!DNL Adobe Analytics] De meetwaarden moeten altijd segmenteerbaar zijn en als de waarde per bezoeker/bezoek wordt geoptimaliseerd, moet de meetwaarde een positieve polariteit hebben (positieve waarden zijn dus beter dan negatieve waarden).
* [!DNL Adobe Analytics] metrisch gebruikt in [!DNL Auto-Target] de activiteiten moeten beschikbaar zijn bij de uitvoer van DataWarehouse.

## Beperkingen en opmerkingen

Sommige beperkingen en opmerkingen zijn van toepassing op beide [!UICONTROL Auto-Allocate] en [!UICONTROL Auto-Target] activiteiten. Andere beperkingen en opmerkingen gelden voor het ene of het andere type activiteit.

### Automatische toewijzing en automatisch doel {#both}

* Wanneer u [!DNL Adobe Analytics] als bron van rapportage voor [!UICONTROL Auto-Allocate] of [!UICONTROL Auto-Target], moet u rapporten altijd weergeven in [!DNL Analytics].
* De rapportbron kan niet worden gewijzigd vanaf [!DNL Analytics] tot [!DNL Target] of omgekeerd nadat een activiteit is geactiveerd.
* Hoewel de berekende metriek niet als primaire doelmetriek worden gesteund, is het vaak mogelijk om het voorgenomen resultaat te bereiken door in plaats daarvan een douanegebeurtenis als primaire doel metrisch te selecteren. Als u bijvoorbeeld wilt optimaliseren voor metrische gegevens, zoals &#39;formulieraanvullen per bezoeker&#39;, selecteert u een aangepaste gebeurtenis die overeenkomt met &#39;formulieraanvullen&#39; als maatstaf voor het primaire doel. Zoals uiteengezet in [Ondersteunde streefwaarden en optimalisatiecriteria](#supported), afhankelijk van het type activiteit en uw optimalisatiecriterium, [!DNL Target] zal omzettingsmetriek automatisch normaliseren, zodat is het niet noodzakelijk om berekende metrisch te gebruiken om normalisatie uit te voeren.


### Automatisch toewijzen {#aa}

* **Trainingsfrequentie**: [!UICONTROL Auto-Allocate] de modellen blijven ieder uur trainen , zoals gewoonlijk .
* **Attributiemodellen**: [!DNL Target] gebruikt de [!DNL Adobe Analytics] standaardtoewijzingsmodel voor[!UICONTROL  Auto-Allocate] activiteiten die gebruikmaken van A4T.
* **Vertrouwen**: De betrouwbaarheidsformule die wordt gebruikt door [!UICONTROL Auto-Allocate] de activiteiten verschillen van de standaardformule in de [!DNL Adobe Analytics] [!UICONTROL A4T] deelvenster. [Zoals hier beschreven](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md), [!UICONTROL Auto-Allocate] gebruikt meer conservatieve betrouwbaarheidsintervallen dan normaal [!UICONTROL A/B Test] activiteiten. Deze conservatieve betrouwbaarheidsniveaus compenseren herhaalde evaluaties (peeks) op gegevens. Dientengevolge, het standaardrapport binnen [!DNL Adobe Analytics] geeft kleinere betrouwbaarheidsintervallen weer in vergelijking met de intervallen die door de [!UICONTROL Auto-Allocate] algoritme. Desalniettemin kunt u bepalen welke ervaring door de algoritmen wordt bevorderd die op welke ervaring worden gebaseerd meer unieke bezoekers worden verzonden naar het.
* **Winkelstatus**: Op dit moment worden de [&quot;Nog geen Winner&quot; en &quot;Winner&quot; badges](/help/main/c-activities/automated-traffic-allocation/determine-winner.md) zijn niet beschikbaar in het dialoogvenster [!UICONTROL A4T] in [!DNL Analysis Workspace]. Deze badges zijn ook niet beschikbaar als hetzelfde rapport wordt weergegeven in [!DNL Target]. Een winnares-&quot;ster&quot;-badge weergegeven in een [!DNL Target] verslag voor een [!UICONTROL Auto-Allocate] activiteit die A4T gebruikt zou moeten worden genegeerd. Deze badge weerspiegelt regelmatige betrouwbaarheidsberekeningen en niet de berekeningen die door [!UICONTROL Auto-Allocate].

### Automatisch doel {#at}

* **Trainingsfrequentie**: [!UICONTROL Auto-Target] de modellen blijven elke 24 uur trainen , zoals gewoonlijk . Omzetgebeurtenisgegevens die echter afkomstig zijn van [!DNL Analytics] 6 tot 24 uur later. Deze vertraging betekent de verdeling van het verkeer door [!DNL Target] traceert de meest recente gebeurtenissen die zijn opgenomen in [!DNL Analytics]. Deze vertraging heeft het grootste effect in de eerste 48 uur nadat een activiteit aanvankelijk wordt geactiveerd. De prestaties van de activiteit zullen nauwkeuriger spiegelen [!DNL Analytics] omzettingsgedrag na vijf dagen is verstreken. Gebruik [!UICONTROL Auto-Allocate] in plaats van [!UICONTROL Auto-Target] voor kortdurende activiteiten waarbij het meeste verkeer plaatsvindt binnen de eerste vijf dagen van de levensduur van de activiteit.
* Wanneer u [!DNL Analytics] als gegevensbron voor een [!UICONTROL Auto-Target] activiteit, sessies eindigen nadat zes uur zijn verstreken. Conversies die na zes uur plaatsvinden, worden niet geteld.

Zie voor meer informatie [Attributiemodellen en terugzoekvensters](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/attribution/models.html) in de *Handleiding Analysehulpmiddelen*.

## Hoe te opstelling A4T rapporten in Analysis Workspace voor auto-Doel en auto-Wijs activiteiten {#tutorial}

Hoewel uitgebreide analysemogelijkheden beschikbaar zijn in [!DNL Adobe Analytics] [!UICONTROL Analysis Workspace], enkele wijzigingen in de standaardwaarde [!UICONTROL Analytics for Target] zijn vereist voor een juiste interpretatie van activiteiten voor automatisch toewijzen en automatisch richten.

Deze wijzigingen zijn vereist vanwege de nuanceerde definities van omrekeningskoersen die in [Ondersteunde streefwaarden en optimalisatiecriteria](#supported), alsmede de verschillen tussen experimentele activiteiten (handleiding A/B en [!UICONTROL Auto-Allocate]) en personaliseringsactiviteiten ([!UICONTROL Auto-Target]).

Deze zelfstudies leiden u door de aanbevolen wijzigingen voor het analyseren [!UICONTROL A4T] [!UICONTROL Auto-Allocate] en [!UICONTROL Auto-Target] activiteiten in [!UICONTROL Workspace].

Zie voor meer informatie
* [A4T-rapporten instellen in Analysis Workspace voor activiteiten automatisch toewijzen](https://experienceleague.adobe.com/docs/target-learn/tutorials/integrations/set-up-a4t-reports-in-analysis-workspace-for-auto-target-activities.html) in *Adobe Target Tutorials*.
* [A4T-rapporten instellen in Analysis Workspace voor Auto-Target-activiteiten](https://experienceleague.adobe.com/docs/target-learn/tutorials/integrations/set-up-a4t-reports-in-analysis-workspace-for-auto-target-activities.html) in *Adobe Target Tutorials*.
