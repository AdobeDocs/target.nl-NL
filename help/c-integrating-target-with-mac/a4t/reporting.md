---
keywords: analytische gegevens voor doel;a4t;analytische gegevens als bron van de rapportage
description: Het gebruiken van Analytics als uw rapporteringsbron voor Doel (A4T) geeft u toegang tot de rapporten van Analytics voor uw activiteiten van het Doel.
title: A4T-rapportage
feature: Analytics for Target (A4T)
translation-type: tm+mt
source-git-commit: 48b94f967252f5ddb009597456edf0a43bc54ba6
workflow-type: tm+mt
source-wordcount: '649'
ht-degree: 0%

---


# A4T-rapportage{#a-t-reporting}

Als u [!DNL Analytics] als rapportagebron voor [!DNL Target] (A4T) gebruikt, hebt u toegang tot [!DNL Analytics]-rapporten voor uw [!DNL Target]-activiteiten.

U kunt rapporten voor uw activiteiten in zowel [!DNL Analytics] als [!DNL Target] bekijken.

Voor het melden van beste praktijken die [!DNL Analytics] voor [!DNL Target], [deze Adobe Spark pagina](https://spark.adobe.com/page/Lo3Spm4oBOvwF/) gebruiken.

## Overzicht {#section_035A62D65608423285D8A5A54731E2C5}

Zowel [!DNL Analytics] als [!DNL Target] melden meetingangen (de mensen die de tests ingaan), eerder dan bezoekers aan de plaats.

Telkens wanneer een bezoeker de inhoud van de activiteit op de pagina ziet, [!DNL Target] een directe server-aan-server vraag aan [!DNL Analytics], met inbegrip van welke activiteit en ervaring de bezoeker zag. [!DNL Target] roept ook  [!DNL Analytics] wanneer de omzetting wordt gemaakt. [!DNL Analytics] voegt de conversie toe als een specifieke nieuwe  [!DNL Analytics] gebeurtenis met de naam &quot;Activiteitenconversie&quot;, die samen met andere gegevens wordt bijgehouden die door  [!DNL Analytics].

Wanneer de [!UICONTROL Select] verrichting wordt gebruikt en u op *Entrants* sorteert, dan slechts ervaringen die ingangen tijdens de geselecteerde tijdspanne ontvingen worden getoond in de rapporten.

>[!NOTE]
>
>Rapporten aangedreven door [!DNL Target] hebben een latentie van vier minuten. Voor activiteiten aangedreven door A4T, in zowel [!DNL Target] als [!DNL Analytics] rapporten, kan het tot 24 uren vergen nadat de activiteit aanvankelijk wordt bewaard alvorens de rapportgegevens door ervaringen kunnen worden verdeeld. De gegevens die in die eerste 24 uur zijn verzameld, zijn nog steeds correct en worden toegewezen aan de juiste ervaring.

## Rapporten in Analytics {#analytics}

In [!DNL Analytics], zijn er verscheidene dimensies en metriek beschikbaar die nadat de integratie A4T wordt toegelaten.

### Dimension

* [!UICONTROL Analytics for Target] - De bovenliggende id die door de integratie wordt doorgegeven. De indeling van deze dimensie is `Activity ID:Experience ID:3rd ID`. Onderstaande dimensies zijn classificaties van deze dimensie.
* [!UICONTROL Target Activities]
* [!UICONTROL Target Experiences]
* [!UICONTROL Target Activity] >  [!UICONTROL Experience]
* [!UICONTROL 3rd ID] - kan worden genegeerd

### Metrisch

* [!UICONTROL Activity Impressions] - Komt overeen met het  [!UICONTROL Entrants] nummer in het  [!DNL Target] rapport.
* [!UICONTROL Activity Conversions] - Komt overeen met het  [!UICONTROL Custom Conversions] nummer in het  [!DNL Target] rapport.

In [!DNL Analysis Workspace] gebruikt u het [!UICONTROL Analytics for Target] paneel om uw [!DNL Target] activiteiten en ervaringen met lift &amp; vertrouwen te analyseren. Zie [Analytics for Target (A4T) Panel](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/panels/a4t-panel.html) in *Analytics Tools Guide* voor meer informatie.

>[!IMPORTANT]
>
>Als in uw [!UICONTROL Target Activities]-rapport in [!DNL Analytics] &quot;niet opgegeven&quot; wordt weergegeven in plaats van uw activiteiten aan te bieden, is een update vereist voor uw provisioned account. Neem contact op met de klantenservice om dit probleem op te lossen.

Voor gedetailleerde informatie en voorbeelden opent u [Analytics &amp; Target: Best Practices for Analysis](https://spark.adobe.com/page/Lo3Spm4oBOvwF/) tutorial, geleverd door Adobe Experience League.

## Rapporten in doel {#section_C0D1F17F88374B6690BF904D7B83B42E}

Wanneer [!DNL Analytics] als rapportbron wordt gebruikt, tonen de rapporten in [!DNL Target] de gegevens die van [!DNL Analytics] worden verzameld. Het rapport verschilt enigszins van andere [!DNL Target] rapporten:

* De [!UICONTROL Audiences] lijst toont de soorten publiek beschikbaar aan uw [!DNL Analytics] rapportreeks.
* De [!UICONTROL Metric] lijst toont elke metrische waarde beschikbaar door [!DNL Analytics].

   Elke metrisch is beschikbaar, met inbegrip van om het even welke douane of berekende metriek die ingebouwde [!DNL Analytics] zijn.

   Houd er rekening mee dat een toename van het aantal positieve punten in het verslag wordt weergegeven, zelfs als een verhoging eigenlijk ongewenst is. Hoewel u bijvoorbeeld een lagere stuitsnelheid wilt, wordt de hogere stuitsnelheid weergegeven als de winnaar met de hoogste lift. Houd rekening met deze en vergelijkbare cijfers en geef aan of u het aantal wilt verlagen of verhogen wanneer u beslissingen neemt op basis van uw rapporten.

U kunt metrisch of publiek op het rapport in [!DNL Target] toepassen nadat de activiteit is begonnen, of zelfs nadat de test heeft voltooid. Je hoeft niet precies te weten wat je vooraf wilt meten.

Klik om het volledige [!DNL Analytics] rapport direct van de pagina van het activiteitenrapport te bekijken.

## Activiteitenschepping {#section_311586E3FF5541E7A91D1A3CE5F9ACE3}

Tijdens het creëren van activiteit, moet u een doel voor de activiteit op [!UICONTROL Settings] pagina specificeren. Dit doel wordt standaard metrisch voor het rapport en is altijd vermeld als eerste optie in de metriekselecteur. U kunt geen segmenten voor rapportering selecteren zoals u voor een regelmatige activiteit van het Doel zou doen. Een test met [!DNL Analytics] gebruikt [!DNL Adobe Analytics] segmenten eerder dan [!DNL Target] publiek.

## Offline berekeningen uitvoeren voor Analytics voor Doel (A4T) {#section_33A97A691F3A45D497DAF57A844388F0}

U kunt offlineberekeningen voor A4T uitvoeren, maar het vereist een stap met gegevens het uitvoeren in [!DNL Analytics].

Zie [Offlineberekeningen uitvoeren voor Analytics voor Target (A4T)](/help/c-reports/conversion-rate.md#concept_0D0002A1EBDF420E9C50E2A46F36629B) voor meer informatie.
