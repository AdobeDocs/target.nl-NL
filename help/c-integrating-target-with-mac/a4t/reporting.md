---
keywords: analytics for target;a4t;analytics as the reporting source
description: Het gebruiken van Analytics als uw rapporteringsbron voor Doel (A4T) geeft u toegang tot de rapporten van Analytics voor uw activiteiten van het Doel.
title: A4T-rapportage
subtopic: Multivariate Test
topic: Standard
uuid: bd3a7fa4-ba45-4ea3-81b6-fc2584831ce4
translation-type: tm+mt
source-git-commit: 217ca811521e67dcd1b063d77a644ba3ae94a72c

---


# A4T-rapportage{#a-t-reporting}

Het gebruiken van Analytics als uw rapporteringsbron voor Doel (A4T) geeft u toegang tot de rapporten van Analytics voor uw activiteiten van het Doel.

U kunt rapporten voor uw activiteiten in zowel Analytics als Standaard/Premium van het Doel bekijken.

Voor het melden van beste praktijken die Analytics voor Doel gebruiken, [bezoek deze pagina](https://spark.adobe.com/page/Lo3Spm4oBOvwF/)van de Vonk van Adobe.

## Overzicht {#section_035A62D65608423285D8A5A54731E2C5}

Zowel in de Analytics- als in de Target-rapporten worden nieuwkomers (de personen die de tests uitvoeren) gemeten in plaats van bezoekers van de site.

Telkens wanneer een bezoeker activiteiteninhoud op de pagina ziet, richt Target een directe server-aan-server vraag aan Analytics, met inbegrip van welke activiteit en ervaring de bezoeker zag. Het doel roept ook Analytics wanneer de omzetting wordt gemaakt. Analytics voegt de conversie toe als een specifieke nieuwe gebeurtenis Analytics met de naam &quot;Activity Conversion&quot;, die samen met andere gegevens die door Analytics worden verzameld, wordt bijgehouden.

Wanneer de Uitgezochte verrichting wordt gebruikt en u op *Entrants* sorteert, dan slechts ervaringen die ingangen tijdens de geselecteerde tijdspanne ontvangen worden getoond in de rapporten.

>[!NOTE]
>
>Rapporten die door Doel worden aangedreven hebben een latentie van vier minuten. Voor activiteiten aangedreven door A4T, in zowel het Doel als de rapporten van de Analyse, kan het tot 24 uren vergen nadat de activiteit aanvankelijk wordt bewaard alvorens de rapportgegevens door ervaringen kunnen worden verdeeld. De gegevens die in die eerste 24 uur zijn verzameld, zijn nog steeds correct en worden toegewezen aan de juiste ervaring.

## Rapporten in Analytics {#section_F6884872DC864AE7913587FAED4CD11C}

Klik in Analytics op **[!UICONTROL Target]** > **[!UICONTROL Target Activities]** in het linkermenu. In Doel, tonen de activiteitenrapporten automatisch de gegevens van de Analyse, metriek, en segmenten. De gegevens worden ongeveer een uur nadat deze van de site zijn verzameld, in deze rapporten weergegeven. Alle metriek, publiek, en waarden in de rapporten komen uit de rapportreeks u selecteerde toen u opstelling de activiteit.

In Analytics, gebruik het rapport van de Activiteiten van het Doel om de resultaten van uw activiteit van het Doel te bekijken. Test&amp;Target-rapporten (verouderd) bevatten informatie over de integratie van de oude stijl van de insteekmodule Test&amp;Target en bevatten geen analyses voor doelgegevens. In het Activiteitenrapport, bekijk informatie over uw ervaringen van het Doel. Klik **[!UICONTROL Metrics]** en selecteer het **[!UICONTROL Target]** metrische type. Er zijn twee metriek beschikbaar voor uw rapport:

* **Activiteitenitems:** Komt overeen met het aantal Intrants in het rapport Doel.
* **Activiteitenconversies:** Komt overeen met het aantal van de Omzettingen van de Douane in het rapport van het Doel.

>[!NOTE]
>
>De gegevens over doellift en betrouwbaarheid zijn ook beschikbaar in Analytics. Zie [Doeloptillen en Vertrouwen](https://docs.adobe.com/content/help/en/analytics/components/variables/dimensions-reports/report-target-lift-confidence.html) in de handleiding *Analytics Components (* Analyseonderdelen) voor meer informatie.

>[!IMPORTANT]
>
>Als in uw rapport Doelactiviteiten in Analytics wordt vermeld &quot;unspecified&quot; in plaats van uw activiteiten aan te bieden, is een update vereist voor uw provisioned account. Neem contact op met de klantenservice om dit probleem op te lossen.

## Rapporten op doel {#section_C0D1F17F88374B6690BF904D7B83B42E}

Wanneer Analytics als rapportbron wordt gebruikt, tonen de rapporten in de Norm van het Doel de gegevens die van Analytics worden verzameld. Het verslag wijkt enigszins af van andere standaardverslagen van het Doel:

* In de lijst Soorten publiek worden de soorten publiek weergegeven die beschikbaar zijn voor uw Analytics-rapportsuite.
* In de lijst Metrisch worden alle metrische gegevens weergegeven die beschikbaar zijn via Analytics.

   Elke metrisch is beschikbaar, met inbegrip van om het even welke douane of berekende metriek die ingebouwde in Analytics zijn.

   Houd er rekening mee dat een toename van het aantal positieve punten in het verslag wordt weergegeven, zelfs als een verhoging eigenlijk ongewenst is. Hoewel u bijvoorbeeld een lagere stuitsnelheid wilt, wordt de hogere stuitsnelheid weergegeven als de winnaar met de hoogste lift. Houd rekening met deze en vergelijkbare cijfers en geef aan of u het aantal wilt verlagen of verhogen wanneer u beslissingen neemt op basis van uw rapporten.

U kunt metrisch of publiek op het rapport in Doel toepassen nadat de test is begonnen, of zelfs nadat de test heeft voltooid. Je hoeft niet precies te weten wat je vooraf wilt meten.

Klik om het volledige rapport Analytics rechtstreeks van de pagina van het activiteitenrapport te bekijken.

## Rapporten in de werkruimte Analyse {#reports-in-analysis-workspace}

U kunt [!DNL Adobe Analysis Workspace] het gebruiken om dieper te graven en de gegevens te visualiseren of inzichten te ontdekken die onder de oppervlakte worden verborgen.

Voor gedetailleerde informatie en voorbeelden opent u de opties [Analytics &amp; Target: Best Practices for Analysis tutorial](https://spark.adobe.com/page/Lo3Spm4oBOvwF/), geleverd door Adobe Experience League.

## Activiteiten maken {#section_311586E3FF5541E7A91D1A3CE5F9ACE3}

Tijdens het creëren van activiteit, moet u een doel voor de activiteit op de [!UICONTROL Settings] pagina specificeren. Dit doel wordt standaard metrisch voor het rapport en is altijd vermeld als eerste optie in de metriekselecteur. U kunt geen segmenten voor rapportering selecteren zoals u voor een regelmatige activiteit van het Doel zou doen. Een test met Analytics maakt gebruik van Adobe Analytics-segmenten in plaats van Target Standard-publiek.

## Offlineberekeningen uitvoeren voor Analytics voor Doel (A4T) {#section_33A97A691F3A45D497DAF57A844388F0}

U kunt offlineberekeningen voor A4T uitvoeren, maar het vereist een stap met gegevens het uitvoeren binnen [!DNL Analytics].

Zie Offlineberekeningen [uitvoeren voor Analytics voor Doel (A4T)](../../c-reports/conversion-rate.md#concept_0D0002A1EBDF420E9C50E2A46F36629B)voor meer informatie.
