---
keywords: analytics for target;a4t;analytics as the reporting source
description: Het gebruiken van Analytics als uw rapporteringsbron voor Doel (A4T) geeft u toegang tot de rapporten van Analytics voor uw activiteiten van het Doel.
title: A4T-rapportage
feature: null
subtopic: Multivariate Test
topic: Standard
uuid: bd3a7fa4-ba45-4ea3-81b6-fc2584831ce4
translation-type: tm+mt
source-git-commit: a51addc6155f2681f01f2329b25d72327de36701
workflow-type: tm+mt
source-wordcount: '641'
ht-degree: 0%

---


# A4T-rapportage{#a-t-reporting}

Het gebruiken [!DNL Analytics] als uw rapporteringsbron voor [!DNL Target] (A4T) geeft u toegang tot [!DNL Analytics] rapporten voor uw [!DNL Target] activiteiten.

U kunt rapporten voor uw activiteiten zowel in [!DNL Analytics] als [!DNL Target].

Ga naar deze Adobe Spark-pagina [!DNL Analytics] voor het melden van tips en trucs [!DNL Target]voor [](https://spark.adobe.com/page/Lo3Spm4oBOvwF/)gebruik.

## Overzicht {#section_035A62D65608423285D8A5A54731E2C5}

Zowel [!DNL Analytics] als in [!DNL Target] rapporten worden nieuwkomers (de personen die de tests uitvoeren) gemeten in plaats van bezoekers van de site.

Telkens wanneer een bezoeker activiteiteninhoud op de pagina ziet, [!DNL Target] maakt een directe server-aan-server vraag aan [!DNL Analytics], met inbegrip van welke activiteit en ervaring de bezoeker zag. [!DNL Target] roept ook [!DNL Analytics] wanneer de omzetting wordt gemaakt. [!DNL Analytics] voegt de conversie toe als een specifieke nieuwe [!DNL Analytics] gebeurtenis met de naam &quot;Activiteitenconversie&quot;, die samen met andere gegevens wordt bijgehouden die door [!DNL Analytics].

Wanneer de [!UICONTROL Select] verrichting wordt gebruikt en u op *Entrants* sorteert, dan slechts ervaringen die ingangen tijdens de geselecteerde tijdspanne ontvangen worden getoond in de rapporten.

>[!NOTE]
>
>Rapporten aangedreven door [!DNL Target] hebben een latentie van vier minuten. Voor activiteiten aangedreven door A4T, in zowel het [!DNL Target] als het [!DNL Analytics] rapport, kan het tot 24 uren duren nadat de activiteit aanvankelijk wordt bewaard alvorens de rapportgegevens door ervaringen kunnen worden verdeeld. De gegevens die in die eerste 24 uur zijn verzameld, zijn nog steeds correct en worden toegewezen aan de juiste ervaring.

## Rapporten in Analytics {#analytics}

In [!DNL Analytics], zijn er verscheidene dimensies en metriek beschikbaar gemaakt nadat de integratie A4T wordt toegelaten.

### Dimension

* [!UICONTROL Analytics for Target] - De bovenliggende id die door de integratie wordt doorgegeven. De indeling van deze dimensie is `Activity ID:Experience ID:3rd ID`. Onderstaande dimensies zijn classificaties van deze dimensie.
* [!UICONTROL Target Activities]
* [!UICONTROL Target Experiences]
* [!UICONTROL Target Activity] > [!UICONTROL Experience]
* [!UICONTROL 3rd ID] - kan worden genegeerd

### Metrisch

* [!UICONTROL Activity Impressions] - Komt overeen met het [!UICONTROL Entrants] nummer in het [!DNL Target] rapport.
* [!UICONTROL Activity Conversions] - Komt overeen met het [!UICONTROL Custom Conversions] nummer in het [!DNL Target] rapport.

In [!DNL Analysis Workspace], gebruik het [!UICONTROL Analytics for Target] paneel om uw [!DNL Target] activiteiten en ervaringen met lift &amp; vertrouwen te analyseren. Zie [Analytics for Target (A4T) Panel](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/panels/a4t-panel.html) in the *Analytics Tools Guide* voor meer informatie.

>[!IMPORTANT]
>
>Als je [!UICONTROL Target Activities] rapport in [!DNL Analytics] lijsten &#39;unspecified&#39; bevat in plaats van je activiteiten aan te bieden, is een update vereist voor je provisioned account. Neem contact op met de klantenservice om dit probleem op te lossen.

Voor gedetailleerde informatie en voorbeelden opent u de opties [Analytics &amp; Target: Best Practices for Analysis](https://spark.adobe.com/page/Lo3Spm4oBOvwF/) tutorial, geleverd door Adobe Experience League.

## Rapporten op doel {#section_C0D1F17F88374B6690BF904D7B83B42E}

Wanneer [!DNL Analytics] als rapporteringsbron wordt gebruikt, tonen de rapporten in [!DNL Target] de gegevens die van [!DNL Analytics]. Het verslag wijkt enigszins af van andere [!DNL Target] verslagen:

* In de [!UICONTROL Audiences] lijst staan de soorten publiek die beschikbaar zijn voor uw [!DNL Analytics] rapportsuite.
* De [!UICONTROL Metric] lijst toont elke metrisch beschikbaar door [!DNL Analytics].

   Elke metrisch is beschikbaar, met inbegrip van om het even welke douane of berekende metriek die ingebouwde [!DNL Analytics].

   Houd er rekening mee dat een toename van het aantal positieve punten in het verslag wordt weergegeven, zelfs als een verhoging eigenlijk ongewenst is. Hoewel u bijvoorbeeld een lagere stuitsnelheid wilt, wordt de hogere stuitsnelheid weergegeven als de winnaar met de hoogste lift. Houd rekening met deze en vergelijkbare cijfers en geef aan of u het aantal wilt verlagen of verhogen wanneer u beslissingen neemt op basis van uw rapporten.

U kunt metrisch of publiek op het rapport binnen toepassen [!DNL Target] nadat de activiteit is begonnen, of zelfs nadat de test heeft voltooid. Je hoeft niet precies te weten wat je vooraf wilt meten.

Klik om het volledige [!DNL Analytics] rapport direct van de pagina van het activiteitenrapport te bekijken.

## Activiteitenschepping {#section_311586E3FF5541E7A91D1A3CE5F9ACE3}

Tijdens het creëren van activiteit, moet u een doel voor de activiteit op de [!UICONTROL Settings] pagina specificeren. Dit doel wordt standaard metrisch voor het rapport en is altijd vermeld als eerste optie in de metriekselecteur. U kunt geen segmenten voor rapportering selecteren zoals u voor een regelmatige activiteit van het Doel zou doen. Een test met [!DNL Analytics] gebruikt [!DNL Adobe Analytics] segmenten in plaats van [!DNL Target] publiek.

## Offline berekeningen uitvoeren voor Analytics voor Doel (A4T) {#section_33A97A691F3A45D497DAF57A844388F0}

U kunt offlineberekeningen voor A4T uitvoeren, maar het vereist een stap met gegevens het uitvoeren binnen [!DNL Analytics].

Zie Offlineberekeningen [uitvoeren voor Analytics voor Doel (A4T)](../../c-reports/conversion-rate.md#concept_0D0002A1EBDF420E9C50E2A46F36629B)voor meer informatie.
