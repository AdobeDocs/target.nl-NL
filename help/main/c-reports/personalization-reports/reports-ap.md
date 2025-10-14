---
keywords: Doel;AP-rapporten;geautomatiseerde verpersoonlijkingsrapporten;activiteitenniveau-rapport;bied niveaurapport aan;bied detailrapport aan;faq
description: Leer hoe u het Automated Personalization Summary-rapport in Adobe Target interpreteert. U kunt op de Geautomatiseerde Segmenten en de Belangrijke rapporten van Attributen van dit rapport schakelen.
title: Hoe gebruik ik de samenvattingsrapporten van Automated Personalization?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=nl-NL#premium newtab=true" tooltip="Kijk wat er in Target Premium is opgenomen."
feature: Reports
exl-id: 2708eba4-72d5-4e6b-b01b-d27de03463b2
source-git-commit: c1a71d1fb6fa9b5c14e22fa3199358a4594bb4a1
workflow-type: tm+mt
source-wordcount: '641'
ht-degree: 0%

---

# Samenvattingsrapporten van Automated Personalization

Gespecialiseerde samenvattingsrapporten zijn beschikbaar voor gebruikers van [!UICONTROL Automated Personalization] -activiteiten in [!DNL Adobe Target] .

>[!NOTE]
>
>[!UICONTROL Automated Personalization] is beschikbaar als onderdeel van de [!DNL Target Premium] -oplossing. Het is niet inbegrepen met [!DNL Target Standard] zonder a [&#x200B; Target Premium vergunning &#x200B;](/help/main/c-intro/intro.md#premium).

1. Klik op **[!UICONTROL Activities]** , klik in de lijst op de gewenste [!UICONTROL Automated Personalization] -activiteit en klik vervolgens op de tab **[!UICONTROL Reports]** .

   Als u vele activiteiten hebt, klik het pictogram van de Filter ( ![&#x200B; pictogram van de Filter &#x200B;](/help/main/assets/icons/Filter.svg)) om de lijst te filtreren door opties van [!UICONTROL Type], [!UICONTROL Status], [!UICONTROL Reporting Source], [!UICONTROL Experience Composer], [!UICONTROL Metrics Type], en [!UICONTROL Activity Source] drop-down lijsten te selecteren.

1. (Facultatief) klik **[!UICONTROL Download]** ( ![&#x200B; pictogram van de Download &#x200B;](/help/main/assets/icons/Download.svg)) pictogram om de summiere mening (bijvoorbeeld, het vergelijken van Controle en Gericht verkeer) te downloaden zoals die door alle beschikbare succesmetriek wordt verdeeld.

[!UICONTROL Automated Personalization] geeft de volgende rapporten:

* Activiteitsniveau
* Aanbiedingsniveau
* Geautomatiseerde segmenten
* Belangrijke kenmerken

## Rapport over activiteitsniveau {#section_6F72FC5C790B4492B3DCECBFFA971337}

In het [!UICONTROL Activity Level] -rapport worden de geaggregeerde prestaties van het gebruik van een [!UICONTROL Automated Personalization] -algoritme vergeleken met willekeurig aangeboden inhoud (besturingselement).

De standaardregels voor de interpretatie van resultaten voor A/B-tests zijn nog steeds van toepassing, zoals lift, betrouwbaarheid, trending, duur, enzovoort. Voor meer informatie over het interpreteren van resultaten, zie [&#x200B; Statistische berekeningen in tests A/Bn &#x200B;](/help/main/c-reports/statistical-methodology/statistical-calculations.md).

## Rapport op aanbodniveau {#section_CAA6409879E349C6906E2BE8156D87A1}

In het [!UICONTROL Offer Level] -rapport voor de Random Forest-ervaring worden de prestaties van elk met algoritme toegepast aanbod vergeleken met hetzelfde willekeurig aangeboden aanbod (Control). Daarom mogen de aanbiedingen in dit verband niet met elkaar worden vergeleken.

Klik op het ervaringsalgoritme (Willekeurig bos of besturingselement) om het [!UICONTROL Offer Level] -rapport weer te geven.

>[!NOTE]
>
>Een klokpictogram geeft aan dat het algoritmemodel nog steeds bezig is met samenstellen. Een vinkje geeft aan dat het basisalgoritme is ingesteld.

Aanbiedingen kunnen binnen [&#x200B; worden getoond rapporterend groepen &#x200B;](/help/main/c-activities/t-automated-personalization/offer-reporting-groups-in-automated-personalization.md), en deze rapporteringsgroepen kunnen worden doen ineenstorten en worden uitgebreid. Klik op **[!UICONTROL Control]** of **[!UICONTROL Targeted]** in de tabel om opgerolde gegevens te bekijken door groepen te melden in plaats van op aanbiedingen.

## Geautomatiseerde segmenten

Klik op het pictogram [!UICONTROL Automated Segments] . Dit rapport laat zien hoe verschillende bezoekers anders reageren op de aanbiedingen/ervaringen in uw AP/AT-activiteit. Dit rapport laat zien hoe verschillende geautomatiseerde segmenten die door de personalisatiemodellen van Target worden gedefinieerd, op de aanbiedingen/ervaringen in de activiteit hebben gereageerd.

Voor meer informatie, zie [&#x200B; Geautomatiseerd rapport van Segmenten &#x200B;](/help/main/c-reports/c-personalization-insights-reports/automated-segments-report.md).

## Belangrijke kenmerken

Klik op het pictogram [!UICONTROL Important Attributes] . Dit rapport toont aan hoe, in verschillende activiteiten, verschillende attributen (of minder) belangrijker voor zijn hoe het model besluit om te personaliseren. Dit rapport toont de belangrijkste kenmerken die het model en hun relatieve belang beïnvloedden.

Voor meer informatie, zie [&#x200B; Belangrijk rapport van Attributen &#x200B;](/help/main/c-reports/c-personalization-insights-reports/important-attributes-report.md).

## Veelgestelde vragen

### Waarom zijn er verschillen in gegevens tussen het activiteitenniveau en de verslagen van het Aanbiedingsniveau?

**[!UICONTROL Activity Level]rapport**: De bezoeken die op het [!UICONTROL Activity Level] rapport worden geregistreerd vangen het aantal bezoeken aan de controleervaring(en) versus &quot;gericht&quot;verkeer. Het gerichte verkeer omvat een mengeling van exploratieverkeer en gepersonaliseerd verkeer.

**het rapport van het Niveau van de Aanbieding**: De indrukkingen die op het [!UICONTROL Offer Level] rapport worden geregistreerd vangen het aantal beelden voor elke aanbieding. Daarom in een activiteit met meer dan één plaats, is het totale aantal bezoeken die in het [!UICONTROL Offer Level] rapport over alle Rapporterende Groepen worden geregistreerd gelijk aan het veelvoud van het aantal bezoeken die voor Controle of gericht verkeer in [!UICONTROL Activity Level] worden geregistreerd rapportkeer het totale aantal plaatsen in de activiteit. Impressies van standaardinhoud die voorkomen op locaties waar de standaardinhoud een beschikbare optie was, worden opgenomen in de aanbiedingsgroep Standaardinhoud. Impressies van aanbiedingen die niet aan een rapportagegroep zijn toegewezen, worden in de &quot;Niet-gegroepeerde&quot; aanbiedingsgroep opgenomen.

>[!NOTE]
>
>Het aantal indrukkingen dat in het [!UICONTROL Offer Level] -rapport is opgenomen, is mogelijk geen exact geheel getal dat het aantal bezoeken aangeeft dat in het [!UICONTROL Activity Level] -rapport is opgenomen. Dit is het gevolg van kleine discrepanties die zich voordoen bij het vastleggen van dataverkeer via internet (de gemiddelde discrepantie bedraagt minder dan 5%). Het aantal weergaven is dus geen exact veelvoud wanneer het aantal beschikbare locaties in de activiteit is gewijzigd nadat de activiteit was geactiveerd.
