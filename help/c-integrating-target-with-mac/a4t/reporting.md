---
keywords: analytics for target;a4t;analytics as the reporting source
description: Het gebruiken van Analytics als uw rapporteringsbron voor Doel (A4T) geeft u toegang tot de rapporten van Analytics voor uw activiteiten van het Doel.
title: A4T-rapportage
subtopic: Multivariate Test
topic: Standard
uuid: bd3a7fa4-ba45-4ea3-81b6-fc2584831ce4
translation-type: tm+mt
source-git-commit: 68f356b0711abf9acf7ef631edf3656bd3dd49e3
workflow-type: tm+mt
source-wordcount: '719'
ht-degree: 0%

---


# A4T-rapportage{#a-t-reporting}

Het gebruiken [!DNL Analytics] als uw rapporteringsbron voor [!DNL Target] (A4T) geeft u toegang tot [!DNL Analytics] rapporten voor uw [!DNL Target] activiteiten.

U kunt rapporten voor uw activiteiten zowel in [!DNL Analytics] als [!DNL Target].

Ga naar deze Adobe Spark-pagina [!DNL Analytics] voor het melden van tips en trucs [!DNL Target]die u kunt gebruiken voor [](https://spark.adobe.com/page/Lo3Spm4oBOvwF/).

## Overzicht {#section_035A62D65608423285D8A5A54731E2C5}

Zowel [!DNL Analytics] als in [!DNL Target] rapporten worden nieuwkomers (de personen die de tests uitvoeren) gemeten in plaats van bezoekers van de site.

Telkens wanneer een bezoeker activiteiteninhoud op de pagina ziet, [!DNL Target] maakt een directe server-aan-server vraag aan [!DNL Analytics], met inbegrip van welke activiteit en ervaring de bezoeker zag. [!DNL Target] roept ook [!DNL Analytics] wanneer de omzetting wordt gemaakt. [!DNL Analytics] voegt de conversie toe als een specifieke nieuwe [!DNL Analytics] gebeurtenis met de naam &quot;Activiteitenconversie&quot;, die samen met andere gegevens wordt bijgehouden die door [!DNL Analytics].

Wanneer de [!UICONTROL Select] verrichting wordt gebruikt en u op *Entrants* sorteert, dan slechts ervaringen die ingangen tijdens de geselecteerde tijdspanne ontvangen worden getoond in de rapporten.

>[!NOTE]
>
>Rapporten aangedreven door [!DNL Target] hebben een latentie van vier minuten. Voor activiteiten aangedreven door A4T, in zowel het [!DNL Target] als het [!DNL Analytics] rapport, kan het tot 24 uren duren nadat de activiteit aanvankelijk wordt bewaard alvorens de rapportgegevens door ervaringen kunnen worden verdeeld. De gegevens die in die eerste 24 uur zijn verzameld, zijn nog steeds correct en worden toegewezen aan de juiste ervaring.

## Rapporten in Analytics {#section_F6884872DC864AE7913587FAED4CD11C}

Klik in [!DNL Analytics]het linkermenu op **[!UICONTROL Target]** > **[!UICONTROL Target Activities]** . In [!DNL Target], tonen de activiteitenrapporten automatisch [!DNL Analytics] gegevens, metriek, en segmenten. De gegevens worden ongeveer een uur nadat deze van de site zijn verzameld, in deze rapporten weergegeven. Alle metriek, publiek, en waarden in de rapporten komen uit de rapportreeks u selecteerde toen u opstelling de activiteit.

In [!DNL Analytics], gebruik het [!UICONTROL Target Activities] rapport om de resultaten van uw [!DNL Target] activiteit te bekijken. Test&amp;Target-rapporten (verouderd) bevatten informatie over de integratie van de oude stijl van de plug-in Test&amp;Target en bevatten geen gegevens [!DNL Analytics] voor [!DNL Target] gegevens. In het [!UICONTROL Activities] rapport bekijkt u informatie over uw [!DNL Target] ervaringen. Klik **[!UICONTROL Metrics]** en selecteer het **[!UICONTROL Target]** metrische type. Er zijn twee metriek beschikbaar voor uw rapport:

* **Activiteitenitems:** Komt overeen met het getal Entrants in het [!DNL Target] rapport.
* **Activiteitenconversies:** Komt overeen met het aantal van de Omzettingen van de Douane in het [!DNL Target] rapport.

>[!NOTE]
>
>[!DNL Target] informatie over lift en vertrouwen is ook beschikbaar in [!DNL Analytics]. Zie [Doeloptillen en Vertrouwen](https://docs.adobe.com/content/help/en/analytics/components/variables/dimensions-reports/report-target-lift-confidence.html) in de handleiding *Analytics Components (* Analyseonderdelen) voor meer informatie.

>[!IMPORTANT]
>
>Als je [!UICONTROL Target Activities] rapport in [!DNL Analytics] lijsten &#39;unspecified&#39; bevat in plaats van je activiteiten aan te bieden, is een update vereist voor je provisioned account. Neem contact op met de klantenservice om dit probleem op te lossen.

## Rapporten op doel {#section_C0D1F17F88374B6690BF904D7B83B42E}

Wanneer [!DNL Analytics] als rapporteringsbron wordt gebruikt, tonen de rapporten in [!DNL Target] de gegevens die van [!DNL Analytics]. Het verslag wijkt enigszins af van andere [!DNL Target] verslagen:

* In de [!UICONTROL Audiences] lijst staan de soorten publiek die beschikbaar zijn voor uw [!DNL Analytics] rapportsuite.
* De [!UICONTROL Metric] lijst toont elke metrisch beschikbaar door [!DNL Analytics].

   Elke metrisch is beschikbaar, met inbegrip van om het even welke douane of berekende metriek die ingebouwde [!DNL Analytics].

   Houd er rekening mee dat een toename van het aantal positieve punten in het verslag wordt weergegeven, zelfs als een verhoging eigenlijk ongewenst is. Hoewel u bijvoorbeeld een lagere stuitsnelheid wilt, wordt de hogere stuitsnelheid weergegeven als de winnaar met de hoogste lift. Houd rekening met deze en vergelijkbare cijfers en geef aan of u het aantal wilt verlagen of verhogen wanneer u beslissingen neemt op basis van uw rapporten.

U kunt metrisch of publiek op het rapport binnen toepassen [!DNL Target] nadat de activiteit is begonnen, of zelfs nadat de test heeft voltooid. Je hoeft niet precies te weten wat je vooraf wilt meten.

Klik om het volledige [!DNL Analytics] rapport direct van de pagina van het activiteitenrapport te bekijken.

## Rapporten in de werkruimte Analyse {#reports-in-analysis-workspace}

U kunt de gegevens dieper graven en [!DNL Adobe Analysis Workspace] de verborgen inzichten onder het oppervlak zichtbaar maken.

Voor gedetailleerde informatie en voorbeelden opent u de opties [Analytics &amp; Target: Best Practices for Analysis tutorial](https://spark.adobe.com/page/Lo3Spm4oBOvwF/), geleverd door [!DNL Adobe Experience League].

## Activiteitenschepping {#section_311586E3FF5541E7A91D1A3CE5F9ACE3}

Tijdens het creëren van activiteit, moet u een doel voor de activiteit op de [!UICONTROL Settings] pagina specificeren. Dit doel wordt standaard metrisch voor het rapport en is altijd vermeld als eerste optie in de metriekselecteur. U kunt geen segmenten voor rapportering selecteren zoals u voor een regelmatige activiteit van het Doel zou doen. Een test met [!DNL Analytics] gebruikt [!DNL Adobe Analytics] segmenten in plaats van [!DNL Target] publiek.

## Offline berekeningen uitvoeren voor Analytics voor Doel (A4T) {#section_33A97A691F3A45D497DAF57A844388F0}

U kunt offlineberekeningen voor A4T uitvoeren, maar het vereist een stap met gegevens het uitvoeren binnen [!DNL Analytics].

Zie Offlineberekeningen [uitvoeren voor Analytics voor Doel (A4T)](../../c-reports/conversion-rate.md#concept_0D0002A1EBDF420E9C50E2A46F36629B)voor meer informatie.
