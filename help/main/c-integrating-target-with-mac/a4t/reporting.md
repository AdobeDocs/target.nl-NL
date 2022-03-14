---
keywords: analytische gegevens voor doel;a4t;analytische gegevens als bron van de rapportage;analytische gegevens
description: Meer informatie over het gebruik van Analytics voor [!DNL Target] (A4T). A4T biedt toegang tot analyserapporten voor [!DNL Target] activiteiten die de metriek van de Analyse en publiekssegmenten gebruiken.
title: Hoe gebruik ik Rapportering in A4T?
feature: Analytics for Target (A4T)
exl-id: cab5dc5f-166a-468e-8382-ae734684afdd
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '655'
ht-degree: 0%

---

# A4T-rapportage

Gebruiken [!DNL Adobe Analytics] als rapportagebron voor [!DNL Adobe Target] (A4T) geeft u toegang tot [!DNL Analytics] rapporten voor uw [!DNL Target] activiteiten.

U kunt rapporten voor uw activiteiten weergeven in beide [!DNL Analytics] en [!DNL Target].

Voor het rapporteren van beste praktijken die [!DNL Analytics] for [!DNL Target], [bezoek een Adobe Spark Page](https://spark.adobe.com/page/Lo3Spm4oBOvwF/).

## Overzicht {#section_035A62D65608423285D8A5A54731E2C5}

Beide [!DNL Analytics] en [!DNL Target] in rapporten worden nieuwkomers ( de personen die de tests uitvoeren ) gemeten in plaats van bezoekers van de site .

Telkens wanneer een bezoeker de inhoud van de activiteit op de pagina ziet, [!DNL Target] maakt een directe server-aan-server vraag aan [!DNL Analytics], met inbegrip van de activiteiten en ervaring die de bezoeker heeft gezien. [!DNL Target] ook oproepen [!DNL Analytics] wanneer de conversie plaatsvindt. [!DNL Analytics] voegt de conversie toe als een specifieke nieuwe [!DNL Analytics] gebeurtenis genaamd &quot;Activiteitenconversie&quot;, die wordt bijgehouden samen met andere gegevens die worden verzameld door [!DNL Analytics].

Wanneer de [!UICONTROL Select] bewerking wordt gebruikt en u sorteert op *Entranten* In dat geval worden in de rapporten alleen ervaringen weergegeven die tijdens de geselecteerde periode binnengekomen zijn.

>[!NOTE]
>
>Rapporten aangedreven door [!DNL Target] hebben een vertraging van vier minuten. Voor activiteiten die door A4T worden aangedreven, zowel in de [!DNL Target] en [!DNL Analytics] rapporten, kan het tot 24 uren vergen nadat de activiteit aanvankelijk wordt bewaard alvorens de rapportgegevens door ervaringen kunnen worden verdeeld. De gegevens die in die eerste 24 uur zijn verzameld, zijn nog steeds correct en worden toegewezen aan de juiste ervaring.

## Rapporten in Analytics {#analytics}

In [!DNL Analytics], zijn er verscheidene dimensies en metriek beschikbaar gemaakt nadat de integratie A4T wordt toegelaten.

### Dimension

* [!UICONTROL Analytics for Target] - De bovenliggende id die door de integratie wordt doorgegeven. De indeling van deze dimensie is `Activity ID:Experience ID:3rd ID`. Onderstaande dimensies zijn classificaties van deze dimensie.
* [!UICONTROL Target Activities]
* [!UICONTROL Target Experiences]
* [!UICONTROL Target Activity] > [!UICONTROL Experience]
* [!UICONTROL 3rd ID] - kan worden genegeerd

### Metrisch

* [!UICONTROL Activity Impressions] - Komt overeen met de [!UICONTROL Entrants] aantal in [!DNL Target] verslag.
* [!UICONTROL Activity Conversions] - Komt overeen met de [!UICONTROL Custom Conversions] aantal in [!DNL Target] verslag.

In [!DNL Analysis Workspace], gebruikt u de [!UICONTROL Analytics for Target] om uw [!DNL Target] activiteiten en ervaringen met liftmogelijkheden en vertrouwen. Zie voor meer informatie [Analyses voor doelvenster (A4T)](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/panels/a4t-panel.html) in de *Handleiding Analysehulpmiddelen*.

>[!IMPORTANT]
>
>Als uw [!UICONTROL Target Activities] rapporteren in [!DNL Analytics] bevat de lijst &quot;niet opgegeven&quot; in plaats van je activiteiten aan te bieden. Er is een update vereist voor je provisioned account. Neem contact op met de klantenservice om dit probleem op te lossen.

Voor gedetailleerde informatie en voorbeelden opent u het dialoogvenster [Analyse en doel: Beste praktijken voor Analyse](https://spark.adobe.com/page/Lo3Spm4oBOvwF/) zelfstudie van Adobe Experience League.

## Rapporten in [!DNL Target] {#section_C0D1F17F88374B6690BF904D7B83B42E}

Wanneer [!DNL Analytics] wordt gebruikt als bron van rapportage, rapporten in [!DNL Target] tonen de gegevens die van worden verzameld [!DNL Analytics]. Het verslag wijkt enigszins af van het andere [!DNL Target] rapporten:

* De [!UICONTROL Audiences] de lijst toont de soorten publiek beschikbaar aan uw [!DNL Analytics] rapportsuite.
* De [!UICONTROL Metric] lijst toont elke metrische waarde beschikbaar door [!DNL Analytics].

   Elke metrisch is beschikbaar, met inbegrip van om het even welke douane of berekende metriek die ingebouwde zijn [!DNL Analytics].

   Om het even welke aantallen die stijgen worden getoond als positieven in het rapport, zelfs wanneer een verhoging ongewenste is. Hoewel u bijvoorbeeld een lagere stuitsnelheid wilt, wordt de hogere stuitsnelheid weergegeven als de winnaar met de hoogste lift. Houd rekening met deze en vergelijkbare cijfers en geef aan of u het aantal wilt verlagen of verhogen wanneer u beslissingen neemt op basis van uw rapporten.

U kunt metrisch of publiek op het rapport in toepassen [!DNL Target] nadat de activiteit is gestart of zelfs nadat de test is voltooid. Je hoeft niet precies te weten wat je vooraf wilt meten.

Klik om de volledige [!DNL Analytics] rechtstreeks vanuit de pagina activiteitenrapport rapporteren.

## Activiteitenschepping {#section_311586E3FF5541E7A91D1A3CE5F9ACE3}

Tijdens het creëren van activiteit, moet u een doel voor de activiteit op specificeren [!UICONTROL Settings] pagina. Dit doel wordt standaard metrisch voor het rapport en is altijd vermeld als eerste optie in de metriekselecteur. U kunt geen segmenten voor rapportering selecteren zoals u voor een regelmatige activiteit van het Doel zou doen. Een test met [!DNL Analytics] gebruik [!DNL Adobe Analytics] segmenten in plaats van [!DNL Target] publiek.

## Offline berekeningen uitvoeren voor Analytics voor Adobe Target (A4T) {#section_33A97A691F3A45D497DAF57A844388F0}

U kunt offlineberekeningen voor A4T uitvoeren, maar het vereist een stap met gegevens het uitvoeren binnen [!DNL Analytics].

Zie voor meer informatie [Offlineberekeningen uitvoeren voor Analytics voor Doel (A4T)](/help/main/c-reports/conversion-rate.md#concept_0D0002A1EBDF420E9C50E2A46F36629B).
