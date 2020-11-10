---
keywords: a4t;A4T;Analytics as the reporting source for Target
description: U kunt een activiteit in de Norm van het Doel/Premium vormen om Adobe Analytics als rapporteringsbron (A4T) te gebruiken.
title: Een activiteit maken die A4T als rapportagebron gebruikt
feature: a4t general
translation-type: tm+mt
source-git-commit: 968d36d65016e51290f6bf754f69c91fd8f68405
workflow-type: tm+mt
source-wordcount: '1346'
ht-degree: 0%

---


# Maak een activiteit die Analytics als rapportbron gebruikt

U kunt een activiteit binnen vormen [!DNL Target] [!DNL Adobe Analytics] om als rapporteringsbron (A4T) te gebruiken.

Voordat u een activiteit instelt die [!DNL Analytics] als bron voor rapportage wordt gebruikt, stelt u het doel voor de activiteit in, zoals het verbeteren van de inkomsten per bezoeker (RPV) of het verhogen van de klik op uw winkelwagentje. Kies een uiteindelijke succesmaatstaf voor de activiteit. Hoewel u extra metriek op elk ogenblik binnen kunt selecteren [!DNL Analytics], moet u bepaalde metrisch nog specificeren u deze test om verwacht te beïnvloeden.

## De activiteit maken

Het maken van een [!DNL Target] activiteit die gebruikt wordt [!DNL Analytics] als de bron van de rapportage is vergelijkbaar met het instellen van een reguliere [!DNL Target] activiteit, met enkele belangrijke verschillen. U kunt bijvoorbeeld geen segment selecteren voor rapportage terwijl u de activiteit maakt, omdat alle segmenten die beschikbaar zijn in, kunnen worden toegepast wanneer u een rapport weergeeft. [!DNL Analytics]

1. Klik op **[!UICONTROL Create Activity]**.

   >[!NOTE]
   >
   >Een activiteitennaam mag niet het teken &quot;%&quot; bevatten als [!DNL Analytics] wordt gebruikt als rapportagebron.

1. Selecteer het type activiteit en stel de activiteit in.
1. Wanneer u aan het **[!UICONTROL Settings]** gedeelte van de stroom van de activiteitenverwezenlijking krijgt, kies **[!UICONTROL Adobe Analytics]** en specificeer uw bedrijf.
1. Selecteer een rapportsuite.

   U kunt elke rapportsuite kiezen die voor u beschikbaar is in [!DNL Analytics]. De rapportsuite definieert waar de verzamelde gegevens beschikbaar zijn. Virtuele rapportsuites zijn niet inbegrepen in de lijst van de rapportreeks.

   U zou twee mogelijke fouten kunnen ontmoeten terwijl het selecteren van de rapportreeks:

   * Er is een fout opgetreden omdat er geen rapportsuites beschikbaar zijn, maar uw account is juist ingesteld.

      Mogelijk moet u uw [!DNL Analytics] bedrijf controleren. Als uw [!DNL Adobe Experience Cloud] account aan meerdere [!DNL Analytics] bedrijven is gekoppeld, meldt u zich af [!DNL Target]en meldt u zich aan bij [!DNL Analytics] het juiste bedrijf. Keer dan terug naar [!DNL Target], en de rapportsuites zullen laden.

   * Je ziet de rapportsuite die je verwacht niet.

      Alleen rapportsuites die zijn ingericht voor verbinding met [!DNL Target] worden geselecteerd. Als u de rapportsuite(s) die u verwacht, niet ziet, meldt u zich eerst af en meldt u zich opnieuw aan bij de [!DNL Adobe Experience Cloud] groep om het opnieuw te proberen.
   Als de rapportsuite(s) nog steeds ontbreekt in de lijst, [neemt u contact op met de klantenservice](/help/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C).

1. Geef de trackingserver op.

   Zie [Een Analytics Tracking Server](/help/c-integrating-target-with-mac/a4t/analytics-tracking-server.md#task_72077BA7E93C4A65A715A18F32228823)gebruiken.

1. Definieer de ervaring.
1. Geef het doel van de activiteit op.

   U moet een succesmetrische waarde selecteren om als doel voor elke activiteit te gebruiken. Uw activiteitendoel is de omzettingsactiviteit die een succesvolle activiteit signaleert. Het is de beste praktijk om nooit een test uit te voeren zonder een doel te hebben om op een bepaalde manier te verbeteren. U kunt elke beschikbare [!DNL Analytics] metrische waarde in de [!DNL Analytics] metrische kiezer kiezen.

   >[!NOTE]
   >
   >U kunt een op doel-Gebaseerde metrisch van de douane verzenden naar [!DNL Analytics] eerder dan het baseren slechts op [!DNL Analytics] gegevens. U kunt bijvoorbeeld controleren of er op een pagina wordt geklikt. Dit wordt meestal niet door [!DNL Analytics]bijgehouden. Deze aangepaste metrische waarde wordt [!DNL Analytics] automatisch van de [!DNL Target] server verzonden en wordt in de metriekkiezer in weergegeven als de metrische waarde &quot;[!DNL Target] Conversie&quot; [!DNL Analytics]. De metrische waarde voor [!DNL Target] omzetten is leeg als u [!DNL Analytics] metriek wilt gebruiken.

   Het plaatsen van een doel betekent niet u kunt geen andere metrisch gebruiken wanneer het evalueren van testresultaten. Het doel is echter een herinnering aan één ding dat u met de activiteit wilt verbeteren.

   De bezoeker blijft in de activiteit nadat zij het doel bereiken. De bezoeker blijft de inhoud van de activiteit zien, maar wordt niet geteld als een nieuwe ingang van de activiteit.

   >[!NOTE]
   >
   >Wanneer u een activiteit instelt nadat u deze hebt ingesteld [!DNL Analytics] als bron voor rapportage, kunt u geen publiek instellen voor rapportage. [!DNL Analytics] de segmenten zijn beschikbaar in het [!DNL Target] activiteitenverslag.

1. Klik op **[!UICONTROL Save]**.

## Analyses voor doelondersteuning (A4T) voor activiteiten voor automatisch toewijzen en automatisch doel {#a4t-aa}

De integratie tussen Adobe Target en Adobe Analytics is nu verbeterd. Dit wordt [Analytics for Target](/help/c-integrating-target-with-mac/a4t/a4t.md)genoemd. Automatische toewijzing en Auto-Target activiteiten ondersteunen nu Analytics for Target.

Dankzij deze integratie kunt u:

* De [auto-Toewijzing](/help/c-activities/automated-traffic-allocation/automated-traffic-allocation.md)van het gebruik van multi-gewapende bandvermogen om verkeer aan het winnen ervaringen te drijven
* Gebruik het ensemble Machine Learning-algoritme van [Auto-Target](/help/c-activities/auto-target/auto-target-to-optimize.md)om een beste ervaring voor elke bezoeker te kiezen op basis van hun profiel, gedrag en context, terwijl u tegelijkertijd een [!DNL Adobe Analytics] doel-metrische en [!DNL Adobe Analytics]&#39; rijke rapportage- en analysemogelijkheden gebruikt.

Zorg ervoor u A4T voor gebruik met A/B Test en Ervaring gerichte activiteiten [hebt](/help/c-integrating-target-with-mac/a4t/a4timplementation.md)uitgevoerd. Als u gebruikt `analyticsLogging = client_side`, moet u ook de `sessionId` waarde tot [!DNL Analytics]. Zie [Analytics for Target (A4T) reporting](https://adobetarget-sdks.gitbook.io/docs/integration-with-experience-cloud/analytics-for-target-a4t-reporting) in the *Adobe Target SDKs* guide voor meer informatie.

Aan de slag:

1. Selecteer op de **[!UICONTROL Targeting]** pagina tijdens het maken van een testactiviteit A/B een van de volgende opties als de **[!UICONTROL Traffic Allocation Method]**:

   * Automatisch toewijzen aan de beste ervaring
   * Automatisch richten voor persoonlijke ervaringen

1. Selecteer **[!UICONTROL Adobe Analytics]** voor uw **[!UICONTROL Reporting Source]** op de **[!UICONTROL Goals & Settings]** pagina en selecteer de rapportreeks die aan uw gewenste optimaliseringsdoel beantwoordt.

1. Kies een maatstaf voor het primaire doel.

   * Kies **[!UICONTROL Conversion]** om het optimalisatiedoel [!DNL Adobe Target] op te geven.
   * Kies **[!UICONTROL Use an Analytics metric]** en selecteer dan metrisch van [!DNL Analytics] voor gebruik als optimalisatiedoel. U kunt een metrische of een [!DNL Analytics] [!DNL Analytics] aangepaste gebeurtenis gebruiken voor het omzetten buiten de doos.

1. Sla uw activiteiten op en activeer deze.

   [!UICONTROL Auto-Allocate] zal uw geselecteerde metrisch gebruiken om de activiteit te optimaliseren, die bezoekers aan de ervaring drijft die uw doel metrisch maximaliseert.

   of

   [!UICONTROL Auto-Target] zal uw geselecteerde metrische waarde gebruiken om de activiteit te optimaliseren, bezoekers naar een gepersonaliseerde beste ervaring drijven.

1. Gebruik het **[!UICONTROL Reports]** tabblad om de rapportage van uw activiteit weer te geven op basis van [!DNL Adobe Analytics] maateenheden. Klik **[!UICONTROL View in Analytics]** om uw rapportgegevens dieper en verder te segmenteren.

### Ondersteunde streefcijfers

[!UICONTROL A4T] voor [!UICONTROL Auto-Allocate] en [!UICONTROL Auto-Target] staat u toe om het even welke volgende metrische types als uw primaire doel metrisch voor optimalisering te kiezen:

* [!DNL Adobe Target] conversiemetingen
* [!DNL Adobe Analytics] conversiemetingen
* [!DNL Adobe Analytics] aangepaste gebeurtenissen

[!UICONTROL A4T] voor [!UICONTROL Auto-Allocate] en [!UICONTROL Auto-Target] vereist u om metrisch te kiezen die op een binomiale gebeurtenis gebaseerd is, namelijk een gebeurtenis die of gebeurt of niet, bijvoorbeeld een klik, een omzetting, een orde, enz. (Deze typen gebeurtenissen worden ook wel Bernoulli, binaire of discrete gebeurtenissen genoemd.)

[!UICONTROL A4T] voor [!UICONTROL Auto-Allocate] en [!UICONTROL Auto-Target] ondersteunt geen optimalisatie voor doorlopende meetgegevens zoals opbrengst, aantal bestelde producten, sessieduur, aantal paginaweergaven tijdens sessies, enz. (Deze niet-ondersteunde typen metriek worden ook wel niet-binomiale of niet-Bernoulli-metriek genoemd.)

De volgende metrische types zijn niet gesteund als primaire doelmetriek:

* [!DNL Adobe Target] service- en inkomstencijfers
* [!DNL Adobe Analytics] service- en inkomstencijfers

   Het kan mogelijk zijn om een metrische [!DNL Analytics] betrokkenheid of opbrengst als uw primaire doel te selecteren omdat [!DNL Target] niet alle overeenkomst en opbrengstmetriek van [!DNL Analytics]. kan identificeren en uitsluiten. Wees voorzichtig met het selecteren van alleen metriek voor binomiale conversie of aangepaste gebeurtenissen van [!DNL Analytics].

* [!DNL Adobe Analytics] berekende meetwaarden

### Beperkingen en opmerkingen

Sommige beperkingen en notities zijn van toepassing op zowel Automatisch toewijzen als Automatisch richten. Andere beperkingen en opmerkingen gelden voor het ene of het andere type activiteit.

#### Automatische toewijzing en automatisch doel

* De rapportagebron kan niet worden gewijzigd van [!DNL Analytics] naar [!DNL Target] of omgekeerd nadat een activiteit is geactiveerd.
* Hoewel de berekende metriek niet als primaire doelmetriek worden gesteund, is het vaak mogelijk om het voorgenomen resultaat te bereiken door in plaats daarvan een douanegebeurtenis als primaire doel metrisch te selecteren. Als u bijvoorbeeld wilt optimaliseren voor metrische gegevens, zoals &#39;formulieraanvullen per bezoeker&#39;, selecteert u een aangepaste gebeurtenis die overeenkomt met &#39;formulieraanvullen&#39; als maatstaf voor het primaire doel. [!DNL Target] normaliseert automatisch omzettingsmetriek op een per-bezoek basis om voor ongelijke verkeersdistributie rekening te houden, zodat is het niet noodzakelijk om berekende metrisch te gebruiken om normalisatie uit te voeren.
* [!DNL Target] gebruikt het attributiemodel &quot;Same Touch&quot; in de [!UICONTROL Auto-Allocate] A4T-implementatie.

#### Automatisch toewijzen

* [!UICONTROL Auto-Allocate] de modellen blijven elke twee uur trainen , zoals gewoonlijk .

#### Automatisch doel

* [!UICONTROL Auto-Target] de modellen blijven elke 24 uur trainen , zoals gewoonlijk . De conversiegegevens die afkomstig zijn van [!DNL Analytics] conversiegebeurtenissen worden echter met nog eens zes tot 24 uur vertraagd. Deze vertraging houdt in dat het verkeer via [!DNL Target] de laatste gebeurtenissen in [!DNL Analytics]het spoor komt. Dit heeft het grootste effect in de eerste 48 uur nadat een activiteit voor het eerst is geactiveerd; de prestaties van de activiteit zullen het [!DNL Analytics] omzettingsgedrag na vijf dagen beter weerspiegelen. U zou moeten overwegen [!UICONTROL Auto-Allocate] in plaats van [!UICONTROL Auto-Target] voor kortdurende activiteiten te gebruiken waar het meeste verkeer binnen de eerste vijf dagen van het leven van de activiteit voorkomt.
* Wanneer het gebruiken [!DNL Analytics] als gegevensbron voor een [!UICONTROL Auto-Target] activiteit, worden de zittingen beschouwd om na zes uren zijn verlopen. Conversies die na zes uur plaatsvinden, worden niet geteld.

Voor meer informatie, zie de modellen van de [Attributie en raadplegingsvensters](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/attribution/models.html) in de Gids *van Hulpmiddelen van de* Analyse.
