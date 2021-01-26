---
keywords: a4t;A4T;Analytics as the reporting source for Target
description: U kunt een activiteit in de Norm van het Doel/Premium vormen om Adobe Analytics als rapporteringsbron (A4T) te gebruiken.
title: Een activiteit maken die A4T als rapportagebron gebruikt
feature: Analytics for Target (A4T)
translation-type: tm+mt
source-git-commit: cf47b7f3625bb1c3430b9fba00c573f489efc448
workflow-type: tm+mt
source-wordcount: '1349'
ht-degree: 0%

---


# Maak een activiteit die Analytics als rapportbron gebruikt

U kunt een activiteit in [!DNL Target] vormen om [!DNL Adobe Analytics] als rapporteringsbron (A4T) te gebruiken.

Voordat u een activiteit instelt die [!DNL Analytics] als rapportagebron gebruikt, stelt u het doel voor de activiteit in, zoals het verbeteren van de inkomsten per bezoeker (RPV) of het verhogen van de klik op uw winkelwagentje. Kies een uiteindelijke succesmaatstaf voor de activiteit. Hoewel u extra metriek op elk ogenblik in [!DNL Analytics] kunt selecteren, moet u nog bepaalde metrisch specificeren u deze test om verwacht te beïnvloeden.

## De activiteit maken

Het maken van een [!DNL Target] activiteit die [!DNL Analytics] als rapportbron gebruikt is gelijkaardig aan vestiging een regelmatige [!DNL Target] activiteit, met een paar belangrijke verschillen. U kunt bijvoorbeeld geen segment selecteren voor rapportage terwijl u de activiteit maakt, omdat alle segmenten die beschikbaar zijn in [!DNL Analytics], kunnen worden toegepast wanneer u een rapport weergeeft.

1. Klik op **[!UICONTROL Create Activity]**.

   >[!NOTE]
   >
   >Een activiteitsnaam mag niet het teken &quot;%&quot; bevatten als [!DNL Analytics] wordt gebruikt als rapportagebron.

1. Selecteer het type activiteit en stel de activiteit in.
1. Wanneer u aan het **[!UICONTROL Settings]** gedeelte van de stroom van de activiteitenverwezenlijking krijgt, kies **[!UICONTROL Adobe Analytics]** en specificeer uw bedrijf.
1. Selecteer een rapportsuite.

   U kunt om het even welke rapportreeks kiezen die aan u in [!DNL Analytics] beschikbaar is. De rapportsuite definieert waar de verzamelde gegevens beschikbaar zijn. Virtuele rapportsuites zijn niet inbegrepen in de lijst van de rapportreeks.

   U zou twee mogelijke fouten kunnen ontmoeten terwijl het selecteren van de rapportreeks:

   * Er is een fout opgetreden omdat er geen rapportsuites beschikbaar zijn, maar uw account is juist ingesteld.

      Mogelijk moet u uw [!DNL Analytics] bedrijf controleren. Als uw [!DNL Adobe Experience Cloud]-account aan meerdere [!DNL Analytics]-bedrijven is gekoppeld, meldt u zich af bij [!DNL Target] en meldt u zich aan bij [!DNL Analytics] onder het juiste bedrijf. Keer dan aan [!DNL Target] terug, en de rapportreeksen zullen laden.

   * Je ziet de rapportsuite die je verwacht niet.

      Alleen rapportsuites die zijn ingericht om verbinding te maken met [!DNL Target] zijn beschikbaar voor selectie. Als u de rapportsuite(s) die u verwacht niet ziet, probeert u zich eerst af te melden en zich weer aan te melden bij [!DNL Adobe Experience Cloud] om het opnieuw te proberen.
   Als de rapportsuite(s) nog steeds ontbreekt in de lijst, neemt u [contact op met de klantenservice](/help/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C).

1. Geef de trackingserver op.

   Zie [Een Analytics Tracking Server](/help/c-integrating-target-with-mac/a4t/analytics-tracking-server.md#task_72077BA7E93C4A65A715A18F32228823) gebruiken.

1. Definieer de ervaring.
1. Geef het doel van de activiteit op.

   U moet een succesmetrische waarde selecteren om als doel voor elke activiteit te gebruiken. Uw activiteitendoel is de omzettingsactiviteit die een succesvolle activiteit signaleert. Het is de beste praktijk om nooit een test uit te voeren zonder een doel te hebben om op een bepaalde manier te verbeteren. U kunt om het even welke [!DNL Analytics] metrisch beschikbaar in [!DNL Analytics] metrische selecteur kiezen.

   >[!NOTE]
   >
   >U kunt een aangepaste op doel gebaseerde metrische waarde naar [!DNL Analytics] verzenden in plaats van alleen op [!DNL Analytics]-gegevens te vertrouwen. U kunt bijvoorbeeld controleren of er op een pagina wordt geklikt, wat gewoonlijk niet wordt bijgehouden door [!DNL Analytics]. Deze aangepaste metrische waarde wordt automatisch verzonden naar [!DNL Analytics] van de [!DNL Target] server, en verschijnt als &quot;[!DNL Target] Omzetting&quot;metrische metriek in [!DNL Analytics]. De omrekeningsnorm [!DNL Target] is leeg als u verkiest om [!DNL Analytics] metriek te gebruiken.

   Het plaatsen van een doel betekent niet u kunt geen andere metrisch gebruiken wanneer het evalueren van testresultaten. Het doel is echter een herinnering aan één ding dat u met de activiteit wilt verbeteren.

   De bezoeker blijft in de activiteit nadat zij het doel bereiken. De bezoeker blijft de inhoud van de activiteit zien, maar wordt niet geteld als een nieuwe ingang van de activiteit.

   >[!NOTE]
   >
   >Wanneer u een activiteit instelt nadat u [!DNL Analytics] hebt ingesteld als uw rapporteringsbron, is er geen optie voor het instellen van soorten publiek voor rapportage. [!DNL Analytics] de segmenten zijn beschikbaar in het  [!DNL Target] activiteitenverslag.

1. Klik op **[!UICONTROL Save]**.

## Analyses voor doelondersteuning (A4T) voor activiteiten voor automatisch toewijzen en automatisch doel {#a4t-aa}

We hebben de integratie tussen Adobe Target en Adobe Analytics geüpgraded, ook wel [Analytics for Target](/help/c-integrating-target-with-mac/a4t/a4t.md) genoemd. Automatische toewijzing en Auto-Target activiteiten ondersteunen nu Analytics for Target.

Dankzij deze integratie kunt u:

* Gebruik [Automatische toewijzing](/help/c-activities/automated-traffic-allocation/automated-traffic-allocation.md)&#39;s meervoudige bewapende bandcapaciteit om verkeer naar het winnen van ervaringen te drijven
* Gebruik [Auto-Target](/help/c-activities/auto-target/auto-target-to-optimize.md)&#39;s ensemble machine learning algorithm om een beste ervaring te kiezen voor elke bezoeker op basis van zijn profiel, gedrag en context, en dit alles terwijl u een [!DNL Adobe Analytics] target-metrische en [!DNL Adobe Analytics]&#39; rijke rapportage- en analysemogelijkheden gebruikt.

Zorg ervoor dat u [A4T voor gebruik met A/B Test en Ervaring gerichte activiteiten](/help/c-integrating-target-with-mac/a4t/a4timplementation.md) hebt uitgevoerd. Als u `analyticsLogging = client_side` gebruikt, moet u ook `sessionId` waarde tot [!DNL Analytics] overgaan. Zie [Analytics for Target (A4T) reporting](https://adobetarget-sdks.gitbook.io/docs/integration-with-experience-cloud/analytics-for-target-a4t-reporting) in de handleiding *Adobe Target SDKs* voor meer informatie.

Aan de slag:

1. Selecteer op de pagina **[!UICONTROL Targeting]** een van de volgende opties als **[!UICONTROL Traffic Allocation Method]** tijdens het maken van een A/B-testactiviteit:

   * Automatisch toewijzen aan de beste ervaring
   * Automatisch richten voor persoonlijke ervaringen

1. Selecteer **[!UICONTROL Adobe Analytics]** voor uw **[!UICONTROL Reporting Source]** op **[!UICONTROL Goals & Settings]** pagina en selecteer de rapportreeks die aan uw gewenste optimaliseringsdoel beantwoordt.

1. Kies een maatstaf voor het primaire doel.

   * Kies **[!UICONTROL Conversion]** om [!DNL Adobe Target] te gebruiken om het optimalisatiedoel te specificeren.
   * Kies **[!UICONTROL Use an Analytics metric]** en selecteer dan metrisch van [!DNL Analytics] voor gebruik als optimalisatiedoel. U kunt een uit-van-doos [!DNL Analytics] omzettingsmetrisch of [!DNL Analytics] douanegebeurtenis gebruiken.

1. Sla uw activiteiten op en activeer deze.

   [!UICONTROL Auto-Allocate] zal uw geselecteerde metrisch gebruiken om de activiteit te optimaliseren, die bezoekers aan de ervaring drijft die uw doel metrisch maximaliseert.

   of

   [!UICONTROL Auto-Target] zal uw geselecteerde metrische waarde gebruiken om de activiteit te optimaliseren, bezoekers naar een gepersonaliseerde beste ervaring drijven.

1. Gebruik het tabblad **[!UICONTROL Reports]** om de rapportage van uw activiteit weer te geven op basis van uw keuze voor [!DNL Adobe Analytics]-meetwaarden. Klik op **[!UICONTROL View in Analytics]** om uw rapportgegevens diepgaand en verder te segmenteren.

### Ondersteunde streefcijfers

[!UICONTROL A4T] voor  [!UICONTROL Auto-Allocate] en  [!UICONTROL Auto-Target] staat u toe om het even welke volgende metrische types als uw primaire doel metrisch voor optimalisering te kiezen:

* [!DNL Adobe Target] conversiemetingen
* [!DNL Adobe Analytics] conversiemetingen
* [!DNL Adobe Analytics] aangepaste gebeurtenissen

[!UICONTROL A4T] voor  [!UICONTROL Auto-Allocate] en  [!UICONTROL Auto-Target] vereist u om metrisch te kiezen die op een binomiale gebeurtenis gebaseerd is, namelijk een gebeurtenis die of gebeurt of niet, bijvoorbeeld een klik, een omzetting, een orde, enz. (Deze typen gebeurtenissen worden ook wel Bernoulli, binaire of discrete gebeurtenissen genoemd.)

[!UICONTROL A4T] voor  [!UICONTROL Auto-Allocate] en  [!UICONTROL Auto-Target] ondersteunt geen optimalisatie voor doorlopende metingen, zoals opbrengst, aantal bestelde producten, sessieduur, aantal paginaweergaven tijdens sessies, enz. (Deze niet-ondersteunde typen metriek worden ook wel niet-binomiale of niet-Bernoulli-metriek genoemd.)

De volgende metrische types zijn niet gesteund als primaire doelmetriek:

* [!DNL Adobe Target] service- en inkomstencijfers
* [!DNL Adobe Analytics] service- en inkomstencijfers

   Het kan mogelijk zijn om een [!DNL Analytics] betrokkenheid of opbrengstmetrisch als uw primaire doel metrisch te selecteren omdat [!DNL Target] niet alle overeenkomst en opbrengstmetriek van [!DNL Analytics] kan identificeren en uitsluiten. Wees voorzichtig met het selecteren van alleen binomiale conversiemetriek of aangepaste gebeurtenissen van [!DNL Analytics].

* [!DNL Adobe Analytics] berekende meetwaarden

### Beperkingen en opmerkingen

Sommige beperkingen en notities zijn van toepassing op zowel Automatisch toewijzen als Automatisch richten. Andere beperkingen en opmerkingen gelden voor het ene of het andere type activiteit.

#### Automatische toewijzing en automatisch doel

* De rapportbron kan niet worden gewijzigd van [!DNL Analytics] in [!DNL Target] of vice versa nadat een activiteit is geactiveerd.
* Hoewel de berekende metriek niet als primaire doelmetriek worden gesteund, is het vaak mogelijk om het voorgenomen resultaat te bereiken door in plaats daarvan een douanegebeurtenis als primaire doel metrisch te selecteren. Als u bijvoorbeeld wilt optimaliseren voor metrische gegevens, zoals &#39;formulieraanvullen per bezoeker&#39;, selecteert u een aangepaste gebeurtenis die overeenkomt met &#39;formulieraanvullen&#39; als maatstaf voor het primaire doel. [!DNL Target] normaliseert automatisch omzettingsmetriek op een per-bezoek basis om voor ongelijke verkeersdistributie rekening te houden, zodat is het niet noodzakelijk om berekende metrisch te gebruiken om normalisatie uit te voeren.
* [!DNL Target] gebruikt het attribuutmodel &quot;Same Touch&quot; in de  [!UICONTROL Auto-Allocate] functie: Analyses voor Doel (A4T).

#### Automatisch toewijzen

* [!UICONTROL Auto-Allocate] de modellen blijven elke twee uur trainen , zoals gewoonlijk .

#### Automatisch doel

* [!UICONTROL Auto-Target] de modellen blijven elke 24 uur trainen , zoals gewoonlijk . De conversiegebeurtenisgegevens die afkomstig zijn van [!DNL Analytics] worden echter met nog eens zes tot 24 uur vertraagd. Deze vertraging betekent de verdeling van verkeer door [!DNL Target] zal de recentste gebeurtenissen volgen die in [!DNL Analytics] worden geregistreerd. Dit heeft het grootste effect in de eerste 48 uur nadat een activiteit voor het eerst is geactiveerd; de prestaties van de activiteit zullen na vijf dagen beter het omrekeningsgedrag [!DNL Analytics] weerspiegelen. U zou moeten overwegen [!UICONTROL Auto-Allocate] in plaats van [!UICONTROL Auto-Target] voor kortdurende activiteiten te gebruiken waar het meeste verkeer binnen de eerste vijf dagen van het leven van de activiteit voorkomt.
* Wanneer u [!DNL Analytics] als gegevensbron voor een [!UICONTROL Auto-Target] activiteit gebruikt, worden de zittingen beschouwd als om na zes uren zijn verlopen. Conversies die na zes uur plaatsvinden, worden niet geteld.

Voor meer informatie, zie [Attributiemodellen en terugkijkvensters](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/attribution/models.html) in *de Gids van de Hulpmiddelen van Analytics*.
