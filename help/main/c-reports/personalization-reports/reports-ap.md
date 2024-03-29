---
keywords: Doel;AP-rapporten;geautomatiseerde verpersoonlijkingsrapporten;activiteitenniveau-rapport;bied niveaurapport aan;bied detailrapport aan;faq
description: Leer hoe u het Automated Personalization Summary-rapport in Adobe Target interpreteert. U kunt op de Geautomatiseerde Segmenten en de Belangrijke rapporten van Attributen van dit rapport schakelen.
title: Hoe gebruik ik de samenvattingsrapporten van Automated Personalization?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="See what's included in Target Premium."
feature: Reports
exl-id: 2708eba4-72d5-4e6b-b01b-d27de03463b2
source-git-commit: 07062b7df75300bd7558a24da5121df454520e42
workflow-type: tm+mt
source-wordcount: '636'
ht-degree: 0%

---

# Samenvattingsrapporten van Automated Personalization

Gebruikers van [!UICONTROL Automated Personalization] activiteiten in [!DNL Adobe Target].

>[!NOTE]
>
>[!UICONTROL Automated Personalization] is beschikbaar als onderdeel van de [!DNL Target Premium] oplossing. Het is niet opgenomen in [!DNL Target Standard] zonder [Licentie voor doelpremie](/help/main/c-intro/intro.md#premium).

1. Klikken **[!UICONTROL Activities]** klikt u op de gewenste [!UICONTROL Automated Personalization] in de lijst en klik vervolgens op de knop **[!UICONTROL Reports]** tab.

   Als u veel activiteiten hebt, kunt u de lijst filteren door [!UICONTROL Automated Personalization] van de [!UICONTROL Type] vervolgkeuzelijst.

1. (Optioneel) Klik op de knop **[!UICONTROL Download]** pictogram om de summiere mening (bijvoorbeeld, het vergelijken van Controle en Gericht verkeer) te downloaden zoals die door alle beschikbare succesmetriek wordt verdeeld.

[!UICONTROL Automated Personalization] bevat de volgende rapporten:

* Activiteitsniveau
* Aanbiedingsniveau
* Geautomatiseerde segmenten
* Belangrijke kenmerken

## Rapport over activiteitsniveau {#section_6F72FC5C790B4492B3DCECBFFA971337}

De [!UICONTROL Activity Level] het rapport vergelijkt de gezamenlijke prestaties van het gebruiken van [!UICONTROL Automated Personalization] algoritme voor willekeurig bediende inhoud (controle).

![Rapport over activiteitsniveau](/help/main/c-reports/assets/box_plot_ap.png)

De standaardregels voor de interpretatie van resultaten voor A/B-tests zijn nog steeds van toepassing, zoals lift, betrouwbaarheid, trending, duur, enzovoort. Voor meer informatie over het interpreteren van resultaten raadpleegt u [Statistische berekeningen voor A/Bn-tests](/help/main/c-reports/statistical-methodology/statistical-calculations.md).

## Rapport op aanbodniveau {#section_CAA6409879E349C6906E2BE8156D87A1}

De [!UICONTROL Offer Level] het rapport voor de Willekeurige Boservaring vergelijkt de prestaties van elk algoritme-toegepast aanbod met het zelfde willekeurig gediende aanbod (Controle). Daarom mogen de aanbiedingen in dit verband niet met elkaar worden vergeleken.

Klik op het ervaringsalgoritme (Willekeurig bos of besturingselement) om het dialoogvenster [!UICONTROL Offer Level] verslag.

![Rapport op aanbodniveau in Adobe Target](/help/main/c-reports/assets/ap_OfferLevelRpt.png)

>[!NOTE]
>
>Een klokpictogram geeft aan dat het algoritmemodel nog steeds bezig is met samenstellen. Een vinkje geeft aan dat het basisalgoritme is ingesteld.

Aanbiedingen kunnen worden weergegeven binnen [rapportagegroepen](/help/main/c-activities/t-automated-personalization/offer-reporting-groups-in-automated-personalization.md)en deze rapportagegroepen kunnen worden samengevouwen en uitgebreid. Klikken **[!UICONTROL Control]** of **[!UICONTROL Targeted]** in de lijst aan meningsopgerolde informatie door rapporteringsgroepen, eerder dan door aanbiedingen.

## Geautomatiseerde segmenten

Klik op de knop [!UICONTROL Automated Segments] pictogram. Dit rapport laat zien hoe verschillende bezoekers anders reageren op de aanbiedingen/ervaringen in uw AP/AT-activiteit. Dit rapport laat zien hoe verschillende geautomatiseerde segmenten die door de personalisatiemodellen van Target worden gedefinieerd, op de aanbiedingen/ervaringen in de activiteit hebben gereageerd.

![Pictogram Automatisch segment](/help/main/c-reports/assets/icon-automated-sements-ap.png)

Zie voor meer informatie [Rapport Automated Segments](/help/main/c-reports/c-personalization-insights-reports/automated-segments-report.md).

## Belangrijke kenmerken

Klik op de knop [!UICONTROL Important Attributes] pictogram. Dit rapport toont aan hoe, in verschillende activiteiten, verschillende attributen (of minder) belangrijker voor zijn hoe het model besluit om te personaliseren. Dit rapport toont de belangrijkste kenmerken die het model en hun relatieve belang beïnvloedden.

![Pictogram Belangrijke kenmerken](/help/main/c-reports/assets/icon-important-attributes-ap.png)

Zie voor meer informatie [Rapport Belangrijke kenmerken](/help/main/c-reports/c-personalization-insights-reports/important-attributes-report.md).

## Veelgestelde vragen

### Waarom zijn er verschillen in gegevens tussen het activiteitenniveau en de verslagen van het Aanbiedingsniveau?

**[!UICONTROL Activity Level]verslag**: Op de [!UICONTROL Activity Level] het aantal bezoeken aan de controleervaring(en) ten opzichte van &quot;gericht&quot; verkeer. Het gerichte verkeer omvat een mengeling van exploratieverkeer en gepersonaliseerd verkeer.

**Rapport op aanbodniveau**: Op de [!UICONTROL Offer Level] in het rapport wordt het aantal indrukken voor elke aanbieding weergegeven. In een activiteit met meer dan één locatie is het totale aantal bezoeken dat in de [!UICONTROL Offer Level] het rapport over alle Rapporterende Groepen is gelijk aan het veelvoud van het aantal bezoeken dat voor Controle of Gericht verkeer in wordt geregistreerd [!UICONTROL Activity Level] rapport keer het totale aantal plaatsen in de activiteit. Impressies van standaardinhoud die voorkomen op locaties waar de standaardinhoud een beschikbare optie was, worden opgenomen in de aanbiedingsgroep Standaardinhoud. Impressies van aanbiedingen die niet aan een rapportagegroep zijn toegewezen, worden in de &quot;Niet-gegroepeerde&quot; aanbiedingsgroep opgenomen.

>[!NOTE]
>
>Het aantal indrukkingen dat is opgenomen op het tabblad [!UICONTROL Offer Level] rapport is mogelijk geen exact veelvoud van gehele getallen van het aantal bezoeken dat is opgenomen in het dialoogvenster [!UICONTROL Activity Level] verslag. Dit is het gevolg van kleine discrepanties die zich voordoen bij het vastleggen van dataverkeer via internet (de gemiddelde discrepantie bedraagt minder dan 5%). Het aantal weergaven is dus geen exact veelvoud wanneer het aantal beschikbare locaties in de activiteit is gewijzigd nadat de activiteit was geactiveerd.
